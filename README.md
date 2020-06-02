# FSChk-Script
#Shell Script for monitoring filesystem usage and filesystem mount points in a linux server, We dont need any tool for monitoring purpose. 

#Pre-requisites

1.Linux server

2.Shell scripting

3.Passwordless login from Jump box to linux servers 

#Script functions

1.Script will continously monitor the filsystem usage & filesystem mount points every 15mins

2.Script will run from jump box, it will read the configuration file and then it will ssh to each server & fetch the data.

3.Script will send mail alert if the filesystem usage exceeds threshold and if any files are missing under the directories where filesystem is mounted on.

4.During multiple tasks, We don’t need to login to each server explicitly and validate the mount points, we can invoke a single script for validation.

#Installation steps

1.FS_chkScript.sh & FSchkMount.cfg files should be staged in Jump Box server(Main server)

2.FS_chkScript.sh - Main script for checking filesystem of each servers. 

3.FSchkMount.cfg - Configuration of various apps.

cat FSchkMount.cfg - We can mention any number of apps here and configure the servers. 

applid:/path/serverconfiguration list

applid:/path/serverconfiguration list

eg:

me0:/tools/scripts/me0/ocp11/ortApp.cfg

4. Configuration of servers  - serverconfiguration list can be staged here and Main script will ssh to these servers & check the fileystem

eg:

cat /tools/scripts/me0/ocp11/ortApp.cfg

#servername instancename

tvmk*       ss01

5.Passwordless is required to ssh to individual servers & check the filsystem.

Please go through https://www.tecmint.com/ssh-passwordless-login-using-ssh-keygen-in-5-easy-steps/ for setting up passwordless login.
