# Related to my YouTube video 
[![image](https://user-images.githubusercontent.com/24313930/150628353-81b697e3-7bd9-4746-b55d-31b752516616.png)](https://www.youtube.com/watch?v=IDKTqLLsWNc)

# Setting Up Termux

![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) در دست ساخت

# Before installation
Before any installation you should first `update` packages repositories like:   
`apt update`  
then go for installing your target app like:   
`apt install cmatrix`   

# Termux-API
For access termux command list like the list below you should first install `termux-api` apk via Google play store
![termux-api](https://user-images.githubusercontent.com/24313930/150627496-1590c4b2-8eca-434d-b966-7a72825d88db.png)
[Download Termux-api - Google play store](https://play.google.com/store/apps/details?id=com.termux.api&hl=en&gl=US)


# SSH
SSH provides a secure way for accessing remote hosts and replaces tools such as telnet, rlogin, rsh, ftp. Termux provides SSH via two packages: dropbear and openssh. If you never used these tools before, it is recommended to install 'openssh' as it is more common. Installing:   
`apt install openssh`

## Usage
`ssh user@ipaddress -p 8022`   
[more info...](https://wiki.termux.com/wiki/Remote_Access)

# FTP
`apt install busybox termux-services`   
After installation you need to restart session or source this file:   

`source $PREFIX/etc/profile.d/start-services.sh`
Now you ready to enable and start the FTP daemon service:   
```bash
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
## XFCE
`apt install xfce4`   
`xfce4-session &`

Additional recommended packages for installation:

netsurf - Simple graphical web browser. Javascript is not supported.
xfce4-terminal - Terminal emulator for XFCE. It is not included as part of XFCE installation to allow use of aterm or st.

[more info...](https://wiki.termux.com/wiki/Graphical_Environment)

# Windows 3.1
First [download](https://github.com/peymanmajidi/termux-setup/raw/main/Windows3-1.zip) the zip file then extract the file in the root of home folder   
then install `Dosbox`:   
`apt install dosbox`   
run Dosbox and mount the home folder as drive c like:   
`mount c: ~`   
![image](https://user-images.githubusercontent.com/24313930/150628155-b92775ac-1511-43df-80d1-f905df8d5b06.png)

the go to `C` drive:   
```cmd
    c:
    cd WINDOWS
    WIN.COM
```    

# Tor
```bash
    apt install tor
    tor
    tor --HTTPTunnelPort 8118 #by pass filter all over the phone
```


# Random Emoji game
`pass`


# Links
[Watch the video](https://www.youtube.com/watch?v=IDKTqLLsWNc)   
[Aparat](https://aparat.com/v/0KhNu)
