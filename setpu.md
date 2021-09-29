1. setup autologin user to run xibo-player
   1. create user
   2. place /etc/lightdm/lightdm.conf
   3. place /home/{{xibo_user}}/.config/autostart/xibo.desktop
2. install snapd and via apt
3. install snaps core and xibo-player
4. restart snapd daemon
5. create ~/snap/xibo-player/common/resources/
6. place cmsSetings.xml in ~/snap/xibo-player/common/

## Variables
* xibo_cms_address
* xibo_user
* xibo_cms_key
* xibo_display_id
