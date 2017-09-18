**hello**

Hello web.
Hello web!

Some new text

i3 reference card

The command to launch a recently downloaded Blackboard Collaborate file is: `/usr/lib/jvm/java-7-oracle/bin$ javaws ~/Downloads/nativeplayback.jnlp`

Linux commands

```find -name *s383*```

`ls | grep *s383* > outputfile`

Using ffmpeg to change video file size, rotate video, preserve audio:

`ffmpeg -i MVI_3602.MOV -vf "transpose=2" -b:v 256k -c:a copy pip.mov`

Navigating the terminal: ctrl-left and -right, home, end, ctrl-u (clear whole line), ctrl-w (clear word), ctrl-r (search command history), tab. Drag files into terminal window. To run the last command except with sudo: sudo !! To RUN the last command that used cat: !cat. To see what it was: !cat:p. This represents the arguments from your last command: !$. The command

```history```

will output your command history to the command line so it's easy to look for something by typing

`history | grep mkdir`

to find the last time you created a directory.
Setting the screen resolution:

 xrandr --output HDMI1 --mode 1280x720`

This should be put into ~/.xprofile (which should be set to executable) if you want it to execute during the login process. However, XFCE4 will override this so if using XFCE4 then instead change ~/.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml. Alternatively, delete displays.xml and then reconfigure your screens using Settings -\> Displays

**Login scripts**

More information can be found in the man pages for bash.

/bin/bash The bash executable

/etc/profile The systemwide initialization file, executed for login shells

~/.bash_profile The personal initialization file, executed for login shells

~/.bashrc The individual per-interactive-shell startup file

~/.bash_logout The individual login shell cleanup file, executed when a login shell exits

~/.inputrc Individual readline initialization file

**Setting audio output with pulseaudio pacmd/pactl**

`pactl set-card-profile 0 output:hdmi-stereo`

**Using openvpn.**

`openvpn /etc/openvpn/verylongfilename.ovpn`

See if a package is installed:

You can type

`which cmd`

to see which program owns the command cmd.
Alternatively you can use

`dpkg -s \ `

Finally you can use

`dpkg-query -l \ `

which allows wildcards

VPS Login

`ssh admin@123.123.123.123 -p 6000`

By default all new users have the ability to use sudo.

**Installing MySQL-JDBC connector**

Download from dev.mysql.com and install to /usr/local. Read the File System Hierarchy standard (FHS) for details about what each of the Linux directories is supposed to be for.

**Using tar to extract/unzip a file**

`tar -xvf thefile.tar.gz -C the/destination/folder`

**Vim**

You can change the colour scheme by typing 

`:colo <TAB>`

Keep pressing <TAB> to cycle through the available colour schemes. Many of them are designed only to work in GVim, rather than the terminal version of Vim.

**Java**

You can set the classpath with

``sudo gvim /etc/environment``

After saving this file use the following terminal command:

``export CLASSPATH``

**Environment Variables**

Changing `/etc/environment` to include

`CLASSPATH="/path/to/jar"`

means you need to reboot. (You don't put `export CLASSPATH` into the `/etc/environment` file because it's not a script and doesn't run; indeed you MUSTN'T use the export command like this or changes to the environment variables won't be registered. Similarly it is wrong to try to execute `source /etc/environment` for the same reason. The `etc/environment` file is read during _login_ by the pam.env.so, or something, so any change to it can be reloaded by logging out and logging back in. A restart is not required.

Alternatively, you can change

`/etc/bash.bashrc`

which will run when any user opens a shell.

Finally you can change 

`~/bash.bashrc`

which will run if the user whose home directory it is opens a shell.

The problem that I had with the mysql jdbc driver was that I had set (a) I had used `export CLASSPATH` in the `/etc/environment` file and (b) the path I had used was `/usr/local/mysql-connector-java-5.1.44.jar` when it should have been `/usr/local/mysql-connector-java-5.1.44/mysql-connector-java-5.1.44.jar`.

**MySQL**

`CREATE DATABASE "DBNAME";`

`CREATE TABLE "TBLNAME" (
id INT not null autoincrement,
name varchar(32),
comment varchar(200));`

`create user "fred[@localhost]"
identified by "hispassword";`

`insert into TBLNAME (name, comment)
values ("Jeff", "Interesting chap");`

I couldn't connect to the mysql server from my laptop and I didn't know if the server was listening to 3306 or perhaps there was a firewall in the way. As it turned out, I got onto the terminal on the server and ran `telnet localhost 3306` and found that mysql was running. This didn't work from a remote host though and it turned out that I needed to change the `bind-address = 127.0.0.1` line in the `/etc/mysql/my.cnf` configuration file to use the external ip address.

You can bounce the server with

`service mysql restart`

**Telnet**

`telnet myserver.com 3306`

This will try to connect on 3306. If the connection is refused it could be a firewall or it could be that the port is not open. SSH to the server and try

`telnet localhost 3306`

to see which it is.

