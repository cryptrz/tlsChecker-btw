# Description
**tlschecker-btw.sh** is the **Arch Linux** version of **tlschecker.sh**. It verfies the validity of the **TLS certificate** for a given domain name or IP address.

For **Debian-based**, **Fedora-based** and **openSUSE-based** systems, please use this version: https://github.com/cryptrz/tlsChecker

# Requirements
For using **tlschecker-btw.sh**, **nmap** is required (It's installed automatically if needed): 
https://nmap.org/download

# Manual usage
```
# First usage only
chmod +x tlschecker-btw.sh

# Then:
sudo ./tlschecker-btw.sh example.com
sudo ./tlschecker-btw.sh 1.1.1.1
```
The result will tell you if the certificate is valid for at least one more month or you need to update now. The same result will be saved in a text file in /root/TLS_Reports/

```
sudo ./tlschecker-btw.sh mozilla.org
Getting the information for mozilla.org, please be patient...
Everything is fine, the TLS certificate for mozilla.org is valid until:  2025-04-12

sudo ./tlschecker-btw.sh fb.com
Getting the information for fb.com, please be patient...
Update NOW the TLS certificate for fb.com!
```

# Installation and usage

## Installation
```
git clone https://github.com/cryptrz/tlschecker-btw.git

cd tlschecker-btw

makepkg -si

sudo pacman -U tlschecker-btw-1.0.0-1-any.pkg.tar.zst
```

## Usage examples
```
sudo tlschecker-btw example.com

sudo tlschecker-btw 1.1.1.1
```
