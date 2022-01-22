# Setting Up Termux

![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) در دست ساخت

# Before installation
Before any installation you should first `update` packages repositories like:   
`apt update`  
then go for installing your target app like:   
`apt install cmatrix`   

# Termux-API
`pass`

# SSH
SSH provides a secure way for accessing remote hosts and replaces tools such as telnet, rlogin, rsh, ftp. Termux provides SSH via two packages: dropbear and openssh. If you never used these tools before, it is recommended to install 'openssh' as it is more common. Installing:   
`apt install openssh`

## Usage
`ssh user@hostname_or_ip-p 8022`   
[more info...](https://wiki.termux.com/wiki/Remote_Access)

# FTP
`apt install busybox termux-services`   
After installation you need to restart session or source this file:   

`source $PREFIX/etc/profile.d/start-services.sh`
Now you ready to enable and start the FTP daemon service:   
```
    sv-enable ftpd
    sv up ftpd
```
default port is 8021   
If you need to stop server, run `sv down ftpd`.   

[more info...](https://wiki.termux.com/wiki/Remote_Access)

# Graphical Environment
Enabling the X11 Repository  
X11 packages are available in a separate APT repository. You can enable it by running the following command:  
`apt install x11-repo`
## Setting up VNC
1. Install package `tigervnc`:  
`apt install tigervnc`  
2. After installation, execute this:  
`vncserver`
3. If everything is okay, you will see this message:  
```
    New 'localhost:1 ()' desktop is localhost:1
    Creating default startup script /data/data/com.termux/files/home/.vnc/xstartup
    Creating default config /data/data/com.termux/files/home/.vnc/config
    Starting applications specified in /data/data/com.termux/files/home/.vnc/xstartup
    Log file is /data/data/com.termux/files/home/.vnc/localhost:1.log
```

It means that X (vnc) server is available on display 'localhost:1'.

4. Finally, to make programs do graphical output to the display 'localhost:1', set environment variable like shown here (yes, without specifying 'localhost'):   
`export DISPLAY=":1"`

[more info...](https://wiki.termux.com/wiki/Graphical_Environment)

# Tor
`pass`


# Random Emoji game
`pass`


# Related to my YouTube video
[![image](https://user-images.githubusercontent.com/24313930/150626014-3018ea4e-0d68-43d1-8124-65cb6ee5459d.png)](https://www.youtube.com/watch?v=IDKTqLLsWNc)

![Aparat](https://aparat.com/v/92iXv)
