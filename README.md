## Enable x11 to install MATLAB Product



---

## Part 1 : Update Linux Standard Based Package

### Ubuntu, Debian
```
sudo apt-get update && sudo apt-get install 
```

### CentOS
```
sudo yum update && sudo yum install redhat-lsb-core 
```

### Fedora
```
sudo dnf update && sudo dnf install redhat-lsb-core
```

### OpenSUSE
```
sudo zypper update && sudo zypper install lsb-core
```

### Arch
```
pacman -Syu lsb-release
```

Display all LSB information specific to your Linux distribution
```
lsb_release -a
```

---

## Part 2 : Install Xming X Server for Windows

Download Link:
https://sourceforge.net/projects/xming/

choosing "Full" for installation type.

After installation, start the Xming X Server for Windows. You should see an icon with an "X" in the system tray if it started successfully.

---

## Part 3 : Enable x11 in ssh(Putty)

1. Install the Putty SSH clients on Windows.
2. Navigate to Connection => SSH => X11 and check the box labeled "Enable X11 forwarding" as shown in the screenshot below:

![photo_01](X11.png)

3. On the remote X server machine, edit the "/etc/ssh/sshd_config" file and make sure that "X11Forwarding" option is set to "Yes" and that the "X11DisplayOffset" is set to an appropriate value (by default, 10).
4. Use Putty to connect to the remote machine, and launch the desired GUI application using the command line (e.g. "./install").

---

## Part 4 : Troubleshooting :

!x what(): Unable to launch the MATLABWindow application during installation

