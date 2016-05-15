# selinux-permissive
Force Enable Selinux to Permissive mode on Android 5+ (Sample)

You can try via emulator or terminal in your devices by command<br />
<pre>su
/system/bin/getenforce</pre>
if output are "enforcing" may you can use the patch<br />
if output are "Permissive" you already to rocks!<br />

#Set Temporary
You can set the SELinux to Permissive temporarily by running the bellow two commands in terminal<br />
<pre>su
setenforce 0 </pre>

#Create script in init.d
Set the SELinux to permissive on boot itself, if your rom support init.d script you can easy added new script to run script above<br />
For Example in <code>/etc/init.d</code> dir, create a file <b>09setperm</b>, add the below lines in the file and save it.. <br />
<pre>#!/system/sh
setenforce 0</pre>
Dont forget to set permission file to 777 (rwxrwxrwx), full<br />
or you can use SelinuxModeChange app
