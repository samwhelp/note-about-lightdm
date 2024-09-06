---
title: lightdm
nav_order: 8030
has_children: false
parent: Fedora
grand_parent: Package
---


# lightdm


## 主題

* [安裝指令](#安裝指令)
* [如何設定採用「lightdm」](#如何設定採用lightdm)
* [檔案列表](#檔案列表)
* [bin](#bin)
* [man](#man)




## Fedora Wiki

* [Lightdm](https://fedoraproject.org/wiki/Lightdm)




## Fedora Search Package

* Search: 「[lightdm](https://packages.fedoraproject.org/search?query=lightdm)」




## Fedora Package

| Fedora Package |
| -------------- |
| [lightdm](https://packages.fedoraproject.org/pkgs/lightdm/lightdm/) |
| [lightdm-gtk](https://packages.fedoraproject.org/pkgs/lightdm-gtk/lightdm-gtk/) |
| [lightdm-settings](https://packages.fedoraproject.org/pkgs/lightdm-settings/lightdm-settings/) |
| [lightdm-gtk-greeter-settings](https://packages.fedoraproject.org/pkgs/lightdm-gtk-greeter-settings/lightdm-gtk-greeter-settings/) |


| Fedora Package |
| -------------- |
| [xorg-x11-server-Xephyr](https://packages.fedoraproject.org/pkgs/xorg-x11-server/xorg-x11-server-Xephyr/) |




## 安裝指令

執行下面指令，安裝「Package: [lightdm](https://packages.fedoraproject.org/pkgs/lightdm/lightdm/)」和「[lightdm-gtk](https://packages.fedoraproject.org/pkgs/lightdm-gtk/lightdm-gtk/)」。

``` sh
sudo dnf install lightdm lightdm-gtk
```




## 如何設定採用「lightdm」

> 關於在「Fedora」的環境，如何選擇採用的「Display Manager」。

> 可以參考「Fedora Wiki / [Lightdm](https://fedoraproject.org/wiki/Lightdm)」的說明。

假如原本採用的是的是「sddm」，先執行下面指令，停用「sddm」

``` sh
sudo systemctl disable sddm
```

會顯示類似如下的訊息

```
Removed "/etc/systemd/system/display-manager.service".
```

接著執行下面指令，啟用「sddm」

``` sh
sudo systemctl enable lightdm
```

會顯示類似如下的訊息

```
Created symlink /etc/systemd/system/display-manager.service → /usr/lib/systemd/system/lightdm.service.
```

可以執行下面指令確認

``` sh
file /etc/systemd/system/display-manager.service
```

顯示

```
/etc/systemd/system/display-manager.service: symbolic link to /usr/lib/systemd/system/lightdm.service
```




## 檔案列表

執行下面指令，觀看「Package: [lightdm](https://packages.fedoraproject.org/pkgs/lightdm/lightdm/)」有哪些「檔案」，安裝在系統上。

``` sh
rpm -ql lightdm
```

顯示

```
/etc/lightdm
/etc/lightdm/keys.conf
/etc/lightdm/lightdm.conf
/etc/lightdm/lightdm.conf.d
/etc/lightdm/users.conf
/etc/logrotate.d
/etc/logrotate.d/lightdm
/etc/pam.d/lightdm
/etc/pam.d/lightdm-autologin
/etc/pam.d/lightdm-greeter
/run/lightdm
/usr/bin/dm-tool
/usr/lib/.build-id
/usr/lib/.build-id/0d
/usr/lib/.build-id/0d/ae16e9264a62ee3a7b2bfced2918c87bf94b50
/usr/lib/.build-id/0f
/usr/lib/.build-id/0f/f6b2fa691f84b4f56a340e5d501c61e42156da
/usr/lib/.build-id/80
/usr/lib/.build-id/80/608bb2ca3640639c686025c6814a57252bc5b0
/usr/lib/systemd/system/lightdm.service
/usr/lib/sysusers.d/lightdm.conf
/usr/lib/tmpfiles.d/lightdm.conf
/usr/lib64/girepository-1.0/LightDM-1.typelib
/usr/libexec/lightdm-guest-session
/usr/sbin/lightdm
/usr/share/accountsservice
/usr/share/accountsservice/interfaces
/usr/share/accountsservice/interfaces/org.freedesktop.DisplayManager.AccountsService.xml
/usr/share/bash-completion
/usr/share/bash-completion/completions
/usr/share/bash-completion/completions/dm-tool
/usr/share/bash-completion/completions/lightdm
/usr/share/dbus-1/interfaces/org.freedesktop.DisplayManager.AccountsService.xml
/usr/share/dbus-1/system.d/org.freedesktop.DisplayManager.conf
/usr/share/doc/lightdm
/usr/share/doc/lightdm/NEWS
/usr/share/help/C/lightdm
/usr/share/help/C/lightdm/autologin.page
/usr/share/help/C/lightdm/config.page
/usr/share/help/C/lightdm/default-greeter.page
/usr/share/help/C/lightdm/default-session.page
/usr/share/help/C/lightdm/diagnostics.page
/usr/share/help/C/lightdm/guest.page
/usr/share/help/C/lightdm/index.page
/usr/share/help/C/lightdm/legal.xml
/usr/share/help/C/lightdm/local-sessions.page
/usr/share/help/C/lightdm/remote-sessions.page
/usr/share/help/C/lightdm/seat.page
/usr/share/help/C/lightdm/standard-authentication.page
/usr/share/help/C/lightdm/user-list.page
/usr/share/help/C/lightdm/user-switching.page
/usr/share/help/C/lightdm/vnc.page
/usr/share/help/C/lightdm/write-greeter.page
/usr/share/help/C/lightdm/xdmcp.page
/usr/share/licenses/lightdm
/usr/share/licenses/lightdm/COPYING.GPL3
/usr/share/lightdm
/usr/share/lightdm/lightdm.conf.d
/usr/share/lightdm/lightdm.conf.d/50-backup-logs.conf
/usr/share/lightdm/lightdm.conf.d/50-disable-guest.conf
/usr/share/lightdm/lightdm.conf.d/50-minimum-vt.conf
/usr/share/lightdm/lightdm.conf.d/50-run-directory.conf
/usr/share/lightdm/lightdm.conf.d/50-session-wrapper.conf
/usr/share/lightdm/lightdm.conf.d/50-user-authority-in-system-dir.conf
/usr/share/lightdm/lightdm.conf.d/50-xserver-command.conf
/usr/share/lightdm/remote-sessions
/usr/share/locale/af/LC_MESSAGES/lightdm.mo
/usr/share/locale/an/LC_MESSAGES/lightdm.mo
/usr/share/locale/ar/LC_MESSAGES/lightdm.mo
/usr/share/locale/ast/LC_MESSAGES/lightdm.mo
/usr/share/locale/az/LC_MESSAGES/lightdm.mo
/usr/share/locale/be/LC_MESSAGES/lightdm.mo
/usr/share/locale/bg/LC_MESSAGES/lightdm.mo
/usr/share/locale/bn/LC_MESSAGES/lightdm.mo
/usr/share/locale/bo/LC_MESSAGES/lightdm.mo
/usr/share/locale/br/LC_MESSAGES/lightdm.mo
/usr/share/locale/bs/LC_MESSAGES/lightdm.mo
/usr/share/locale/ca/LC_MESSAGES/lightdm.mo
/usr/share/locale/ca@valencia/LC_MESSAGES/lightdm.mo
/usr/share/locale/ckb/LC_MESSAGES/lightdm.mo
/usr/share/locale/cs/LC_MESSAGES/lightdm.mo
/usr/share/locale/da/LC_MESSAGES/lightdm.mo
/usr/share/locale/de/LC_MESSAGES/lightdm.mo
/usr/share/locale/el/LC_MESSAGES/lightdm.mo
/usr/share/locale/en_AU/LC_MESSAGES/lightdm.mo
/usr/share/locale/en_CA/LC_MESSAGES/lightdm.mo
/usr/share/locale/en_GB/LC_MESSAGES/lightdm.mo
/usr/share/locale/eo/LC_MESSAGES/lightdm.mo
/usr/share/locale/es/LC_MESSAGES/lightdm.mo
/usr/share/locale/et/LC_MESSAGES/lightdm.mo
/usr/share/locale/eu/LC_MESSAGES/lightdm.mo
/usr/share/locale/fa/LC_MESSAGES/lightdm.mo
/usr/share/locale/fi/LC_MESSAGES/lightdm.mo
/usr/share/locale/fo/LC_MESSAGES/lightdm.mo
/usr/share/locale/fr/LC_MESSAGES/lightdm.mo
/usr/share/locale/fy/LC_MESSAGES/lightdm.mo
/usr/share/locale/gd/LC_MESSAGES/lightdm.mo
/usr/share/locale/gl/LC_MESSAGES/lightdm.mo
/usr/share/locale/gu/LC_MESSAGES/lightdm.mo
/usr/share/locale/he/LC_MESSAGES/lightdm.mo
/usr/share/locale/hi/LC_MESSAGES/lightdm.mo
/usr/share/locale/hr/LC_MESSAGES/lightdm.mo
/usr/share/locale/hu/LC_MESSAGES/lightdm.mo
/usr/share/locale/ia/LC_MESSAGES/lightdm.mo
/usr/share/locale/id/LC_MESSAGES/lightdm.mo
/usr/share/locale/is/LC_MESSAGES/lightdm.mo
/usr/share/locale/it/LC_MESSAGES/lightdm.mo
/usr/share/locale/ja/LC_MESSAGES/lightdm.mo
/usr/share/locale/kk/LC_MESSAGES/lightdm.mo
/usr/share/locale/km/LC_MESSAGES/lightdm.mo
/usr/share/locale/kn/LC_MESSAGES/lightdm.mo
/usr/share/locale/ko/LC_MESSAGES/lightdm.mo
/usr/share/locale/ku/LC_MESSAGES/lightdm.mo
/usr/share/locale/lb/LC_MESSAGES/lightdm.mo
/usr/share/locale/lt/LC_MESSAGES/lightdm.mo
/usr/share/locale/lv/LC_MESSAGES/lightdm.mo
/usr/share/locale/mhr/LC_MESSAGES/lightdm.mo
/usr/share/locale/mi/LC_MESSAGES/lightdm.mo
/usr/share/locale/ml/LC_MESSAGES/lightdm.mo
/usr/share/locale/mr/LC_MESSAGES/lightdm.mo
/usr/share/locale/ms/LC_MESSAGES/lightdm.mo
/usr/share/locale/my/LC_MESSAGES/lightdm.mo
/usr/share/locale/nb/LC_MESSAGES/lightdm.mo
/usr/share/locale/nl/LC_MESSAGES/lightdm.mo
/usr/share/locale/nn/LC_MESSAGES/lightdm.mo
/usr/share/locale/oc/LC_MESSAGES/lightdm.mo
/usr/share/locale/pa/LC_MESSAGES/lightdm.mo
/usr/share/locale/pl/LC_MESSAGES/lightdm.mo
/usr/share/locale/pt/LC_MESSAGES/lightdm.mo
/usr/share/locale/pt_BR/LC_MESSAGES/lightdm.mo
/usr/share/locale/ro/LC_MESSAGES/lightdm.mo
/usr/share/locale/ru/LC_MESSAGES/lightdm.mo
/usr/share/locale/sc/LC_MESSAGES/lightdm.mo
/usr/share/locale/sd/LC_MESSAGES/lightdm.mo
/usr/share/locale/shn/LC_MESSAGES/lightdm.mo
/usr/share/locale/si/LC_MESSAGES/lightdm.mo
/usr/share/locale/sk/LC_MESSAGES/lightdm.mo
/usr/share/locale/sl/LC_MESSAGES/lightdm.mo
/usr/share/locale/sq/LC_MESSAGES/lightdm.mo
/usr/share/locale/sr/LC_MESSAGES/lightdm.mo
/usr/share/locale/sv/LC_MESSAGES/lightdm.mo
/usr/share/locale/ta/LC_MESSAGES/lightdm.mo
/usr/share/locale/te/LC_MESSAGES/lightdm.mo
/usr/share/locale/tg/LC_MESSAGES/lightdm.mo
/usr/share/locale/th/LC_MESSAGES/lightdm.mo
/usr/share/locale/tl/LC_MESSAGES/lightdm.mo
/usr/share/locale/tr/LC_MESSAGES/lightdm.mo
/usr/share/locale/ug/LC_MESSAGES/lightdm.mo
/usr/share/locale/uk/LC_MESSAGES/lightdm.mo
/usr/share/locale/uz/LC_MESSAGES/lightdm.mo
/usr/share/locale/vi/LC_MESSAGES/lightdm.mo
/usr/share/locale/wae/LC_MESSAGES/lightdm.mo
/usr/share/locale/zh_CN/LC_MESSAGES/lightdm.mo
/usr/share/locale/zh_HK/LC_MESSAGES/lightdm.mo
/usr/share/locale/zh_TW/LC_MESSAGES/lightdm.mo
/usr/share/man/man1/dm-tool.1.gz
/usr/share/man/man1/lightdm.1.gz
/usr/share/polkit-1/actions/org.freedesktop.DisplayManager.AccountsService.policy
/usr/share/polkit-1/rules.d/lightdm.rules
/usr/share/xgreeters
/var/cache/lightdm
/var/lib/lightdm
/var/lib/lightdm-data
/var/log/lightdm
```




## bin

執行下面指令，找出相關的指令

``` sh
rpm -ql lightdm | grep bin
```

顯示

```
/usr/bin/dm-tool
/usr/sbin/lightdm
```


## man

執行下面指令，找出相關的「Manpage」

``` sh
rpm -ql lightdm | grep '/man/man.*/' | sort -u
```

顯示

```
/usr/share/man/man1/dm-tool.1.gz
/usr/share/man/man1/lightdm.1.gz
```
