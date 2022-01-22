# termux-setup
Related to my YouTube video about setting up Termux



![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) در دست ساخت


# First Time
Before ay installation you should first `update` packages repositories like:   
`apt update`

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


