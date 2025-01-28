# $\textcolor{yellow}{🖥️Linux\ OS\ Helper 🐧}$

### $\textcolor{#389cff}{update\ parrot\ os}$
```
sudo parrot-upgrade
sudo apt update && sudo apt full-upgrade
```

### $\textcolor{#389cff}{check\ os\ version}$
```cat /etc/os-release```
### $\textcolor{#389cff}{git\ clone\ with\ access/ token}$
```git clone https://<tokenhere>@github.com/<user>/<repo>.git```

## install supported fonts command
### $\textcolor{#389cff}{web\ browser\ broken\ bangla\ font\ fix}$
Download the “Kalpurush” font from <a class="af nx" href="https://okkhor52.com/download.html?id=_001" rel="noopener ugc nofollow" target="_blank">Okkhor52</a> or any other trusted font provider. Unzip if there’s a zip file and look for <code class="cx pb pc pd pe b">kalpurush.ttf</code> file.</p>

### $\textcolor{#389cff}{or\ install\ with\ commands}$
    /*download fonts */
    sudo apt install fonts-noto-core
    sudo apt install fonts-noto-ui-core
    
    /* remove free-sans and free-serif */
    sudo rm -f /usr/share/fonts/truetype/freefont/FreeSans*
    sudo rm -f /usr/share/fonts/truetype/freefont/FreeSerif*

    /* Now, clear the fonts cache to load the new fonts in the system: */
    fc-cache -f -v
    /* now restart device */

    /* update node version */
    curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
    sudo apt install nodejs
        /* if fails then update CURL */
        sudo apt update
        sudo apt install --reinstall ca-certificates
        date
        sudo timedatectl set-ntp true
        curl -k -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
        sudo apt install curl
    
    /* Install Browsers */
    curl -fsS https://dl.brave.com/install.sh | sh
    
    
### $\textcolor{#389cff}{screen\ zoom\ commands}$
```xrandr --listmonitors // show list
xrandr --output eDP-1 --scale 0.8x0.8 // for zoom
xrandr --auto
xrandr --output eDP-1 --scale 1x1 // for default
```

### $\textcolor{#389cff}{Install\ snap\ for\ install\ Windows\ app}$
```
sudo apt update
sudo apt install snapd
Skype: sudo snap install skype
```

### $\textcolor{#389cff}{Take\ screenshot\ commands}$
```
mate-screenshot --interactive
mate-screenshot --area
```
    
### $\textcolor{#389cff}{Stream\ errror:\ You\ are\ missing\ the\ following\ 32-bit\ libraries,\ and\ Steam\ may\ not\ run:\ libGL.so.1}$
```xrandr --listmonitors // show list
su --login
dpkg --add-architecture i386
apt install libgl1-nvidia-glvnd-glx:i386

// then Enable Stream Play for all other titles - for install PUBG
```

### $\textcolor{#389cff}{linux\ others\ apps\ URL}$
github: https://github.com/shiftkey/desktop/releases/


    
### $\textcolor{#389cff}{Backup\ softwares\ and\ commands}$
#### Option A: backup with software 
```sudo apt update
sudo apt install timeshift
```
#### option B: Manual Backup
## Clear caches
```# Clear user cache
rm -rf ~/.cache/*

# Clear system cache
sudo rm -rf /var/cache/*

# Clear APT cache
sudo apt clean

# Clear trash
rm -rf ~/.local/share/Trash/*

# Clear system logs
sudo journalctl --vacuum-time=1d

# Clear temporary files
sudo rm -rf /tmp/*
rm -rf ~/.tmp/*
```
Backup Installed Packages:
Generate a list of installed packages:
```sudo dpkg --get-selections > package-list.txt```
Save the package-list.txt file to an external drive or cloud storage.
Backup Configuration Files:
Backup your /etc directory (contains system-wide configurations):

```sudo tar -czvf etc-backup.tar.gz /etc
// Backup your home directory (contains user-specific configurations and files):
tar -czvf home-backup.tar.gz /home/your-username
```

Backup Important Data:
Copy any important files or directories to an external drive or cloud storage.
Reinstall Parrot OS (if necessary).
Restore Installed Packages:
Copy the package-list.txt file to your new system.

Reinstall the packages:
```sudo dpkg --set-selections < package-list.txt
sudo apt-get dselect-upgrade

// Restore Configuration Files:
// Extract the etc-backup.tar.gz and home-backup.tar.gz files to their respective locations:

sudo tar -xzvf etc-backup.tar.gz -C /
tar -xzvf home-backup.tar.gz -C /
```
Restore Important Data:

Copy your important files back to their original locations.
