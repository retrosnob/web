**hello**

Hello web.
Hello web!

Some new text

i3 reference card

The command to launch a recently downloaded Blackboard Collaborate file is: /usr/lib/jvm/java-7-oracle/bin$ javaws ~/Downloads/nativeplayback.jnlp

Linux commands

find -name *s383*
ls | grep *s383* > outputfile
Using ffmpeg to change video file size, rotate video, preserve audio:

ffmpeg -i MVI_3602.MOV -vf "transpose=2" -b:v 256k -c:a copy pip.mov
Navigating the terminal: ctrl-left and -right, home, end, ctrl-u (clear whole line), ctrl-w (clear word), ctrl-r (search command history), tab. Drag files into terminal window. To run the last command except with sudo: sudo !! To RUN the last command that used cat: !cat. To see what it was: !cat:p. This represents the arguments from your last command: !$. The command

history
will output your command history to the command line so it's easy to look for something by typing
history | grep mkdir
to find the last time you created a directory.
Setting the screen resolution:

 xrandr --output HDMI1 --mode 1280x720
.
This should be put into ~/.xprofile (which should be set to executable) if you want it to execute during the login process. However, XFCE4 will override this so if using XFCE4 then instead change ~/.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml. Alternatively, delete displays.xml and then reconfigure your screens using Settings -\> Displays
Login scripts

More information can be found in the man pages for bash.

/bin/bash The bash executable

/etc/profile The systemwide initialization file, executed for login shells

~/.bash_profile The personal initialization file, executed for login shells

~/.bashrc The individual per-interactive-shell startup file

~/.bash_logout The individual login shell cleanup file, executed when a login shell exits

~/.inputrc Individual readline initialization file

Setting audio output with pulseaudio pacmd/pactl

`pactl set-card-profile 0 output:hdmi-stereo`

Using openvpn.

`openvpn /etc/openvpn/verylongfilename.ovpn`
See if a package is installed:

You can type

`which cmd`
to see which program owns the command cmd.
Alternatively you can use

`dpkg -s \`
Finally you can use

`dpkg-query -l \`
which allows wildcards
