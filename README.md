# FSChk-Script
#Shell Script for monitoring filesystem usage and filesystem mount points in a linux server

#Pre-requisites

1.Linux server
2.Shell scripting
3.Passwordless login from Jump box to linux servers 

#Script functions

1.Script will continously monitor the filsystem usage & filesystem mount points every 15mins
2.Script will run from jump box, it will read the configuration file and then it will ssh to each server & fetch the data.
3.Script will send mail alert if the filesystem usage exceeds threshold and if any files are missing under the directories where filesystem is mounted on.
4.During multiple tasks, We don’t need to login to each server explicitly and validate the mount points, we can invoke a single script for validation.

