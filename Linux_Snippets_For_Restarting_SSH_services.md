# mylinux


# LINUX SNIPPET FOR 

## HowTo: Restart SSH Service under Linux / UNIX operating systems

The command to restart ssh are as follows (you must login as root user). 

You must run command as per your Linux distro or Unix variant: restart-ssh-command


#### CentOS / RHEL / Fedora / Redhat Linux Restart SSH

```Linux
# /etc/init.d/sshd restart

OR
# service sshd restart
```

#### If you are using RHEL/CentOS/Fedora Linux with systemd, enter:
```
$ sudo systemctl restart sshd
```
#### Debian / Ubuntu Linux Restart SSH
```
$ /etc/init.d/ssh restart

OR
$ service ssh restart

OR
$ sudo service ssh restart
```
#### If you are using Debian/Ubuntu/Mint Linux with systemd, enter:
```
$ sudo systemctl restart ssh
```
#### FreeBSD Restart SSH
```
$ /etc/rc.d/sshd restart

OR
$ sudo service sshd restart
```
OpenBSD Restart SSH
```
$ /etc/rc.d/sshd restart

OR
$ doas /etc/rc.d/sshd restart
```
#### UNIX Restart SSH
```
$ kill -HUP `cat /var/run/sshd.pid`

OR
$ kill -HUP $(cat /var/run/sshd.pid)
```
Please note that the location of /var/run/sshd.pid may change. 
So just search a bit through /var/run/ directory.

##### END OF SNIPPET 3:31 PM 9/12/2017