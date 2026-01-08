# Kiosk installer for Debian based Linux distros, ZoneMinder version, screen doesn't go to sleep
Small installer script to setup a minimal Xorg kiosk with Chromium for Debian based Linux distros. This installer is heavily based on the excellent [instructions by Will Haley](http://willhaley.com/blog/debian-fullscreen-gui-kiosk/)  and is forked from [github.com/josfaber/debian-kiosk-installer](github.com/josfaber/debian-kiosk-installer) .

## Usage
* Setup a minimal Debian without display manager, like netboot install
* Login as root or with root permissions
* Download this installer, make it executable and run it

  ```shell
  wget https://raw.githubusercontent.com/lienardj/debian-kiosk-installer/master/kiosk-installer.sh; chmod +x kiosk-installer.sh; ./kiosk-installer.sh
  ```
* Configure the network htrough CLI with "nmtui"

## What will it do?
It will create a normal user `kiosk`, install software (check the script) and setup configs (it will backup existing) so that on reboot the kiosk user will login automaticaly and run chromium in kiosk mode with one url. It will also hide the mouse. 

## Change the url
Change the url at the bottom of the script,

## Is it secure?
No, but many stuff like the terminal are removed. It's still possible to mess up (close the session, etc...).
