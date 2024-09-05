---
title: Start
nav_order: 1010
has_children: false
parent: lightdm-gtk-greeter
grand_parent: 設定
---


# Start




## 主題

* [Link](#link)
* [入門](#入門)
* [設定範本](#設定範本)
* [設定範例](#設定範例)




## Link

| Link |
| ---- |
| Arch Wiki / [LightDM](https://wiki.archlinux.org/title/LightDM) |




## 入門

> 這篇是關於「lightdm」採用「lightdm-gtk-greeter」的設定入門。

相關的「設定範本」，可以在下面兩個專案找到

| Data |
| ---- |
| GitHub / lightdm / [data](https://github.com/canonical/lightdm/tree/main/data) |
| GitHub / lightdm-gtk-greeter / [data](https://github.com/Xubuntu/lightdm-gtk-greeter/tree/master/data) |




## 設定範本

| 原始設定範本 |
| ---------- |
| [/etc/lightdm/lightdm.conf](https://github.com/canonical/lightdm/blob/main/data/lightdm.conf) |
| [/etc/lightdm/users.conf](https://github.com/canonical/lightdm/blob/main/data/users.conf) |
| [/etc/lightdm/keys.conf](https://github.com/canonical/lightdm/blob/main/data/keys.conf) |
| [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/Xubuntu/lightdm-gtk-greeter/blob/master/data/lightdm-gtk-greeter.conf) |


> 我將上面的「原始設定範本」做了點排版，整理如下


| [設定範本](https://github.com/samwhelp/lightdm-adjustment/tree/main/prototype/main/lightdm-config/template/lightdm-gtk-greeter/asset/overlay/etc/lightdm) |
| ---------- |
| [/etc/lightdm/lightdm.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/template/lightdm-gtk-greeter/asset/overlay/etc/lightdm/lightdm.conf) |
| [/etc/lightdm/users.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/template/lightdm-gtk-greeter/asset/overlay/etc/lightdm/users.conf) |
| [/etc/lightdm/keys.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/template/lightdm-gtk-greeter/asset/overlay/etc/lightdm/keys.conf) |
| [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/template/lightdm-gtk-greeter/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf) |




## 設定範例

> 以下是採用不同的「GTK 佈景主題」的設定範例 。

| Style | Config Path |
| ----- | ----------- |
| [Materia-Dark](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Materia-Dark) | [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Materia-Dark/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103) |
| [Arc-Dark](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark) | [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103) |
| [Arc-Light](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Light) | [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Light/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103) |
| [Numix](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Numix) | [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Numix/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103) |


以「[Arc-Dark](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark)」這個範例，來做說明。

主要的設定檔，是下面兩個檔案

| [設定檔](https://github.com/samwhelp/lightdm-adjustment/tree/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm) |
| ----- |
| [/etc/lightdm/lightdm.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm/lightdm.conf#L142) |
| [/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103) |


> 關於「[/etc/lightdm/lightdm.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm/lightdm.conf#L142)」的設定，主要是如下的「設定片段」。

``` ini
[Seat:*]
greeter-session=lightdm-gtk-greeter
```

> 登入畫面，則是參考「[/etc/lightdm/lightdm-gtk-greeter.conf](https://github.com/samwhelp/lightdm-adjustment/blob/main/prototype/main/lightdm-config/lightdm-gtk-greeter/profile/simple/Arc-Dark/asset/overlay/etc/lightdm/lightdm-gtk-greeter.conf#L103)」這個檔案的內容。

``` ini


################################################################################
### Head: Info
##

##
## ## Path
##
## * /etc/lightdm/lightdm-gtk-greeter.conf
##
## ## Link
##
## * https://github.com/Xubuntu/lightdm-gtk-greeter/blob/master/data/lightdm-gtk-greeter.conf
##

##
### Tail: Info
################################################################################




################################################################################
### Head: Section / greeter
##

##
## ## LightDM GTK Configuration
##
## > Available configuration options listed below.
## > Please list the configuration options that you want to use after [greeter] without the # for example:
## [greeter]
## example-option=example-value
##
## > Appearance:
## theme-name = GTK theme to use
## icon-theme-name = Icon theme to use
## cursor-theme-name = Cursor theme to use
## cursor-theme-size = Cursor size to use
## background = Background file to use, either an image path or a color (e.g. #772953)
## user-background = false|true ("true" by default)  Display user background (if available)
## transition-duration = Length of time (in milliseconds) to transition between background images ("500" by default)
## transition-type = ease-in-out|linear|none  ("ease-in-out" by default)
##
## > Fonts:
## font-name = Font to use
## xft-antialias = false|true  Whether to antialias Xft fonts
## xft-dpi = Resolution for Xft in dots per inch (e.g. 96)
## xft-hintstyle = none|slight|medium|hintfull  What degree of hinting to use
## xft-rgba = none|rgb|bgr|vrgb|vbgr  Type of subpixel antialiasing
#
## > Login window:
## active-monitor = Monitor to display greeter window (name or number). Use #cursor value to display greeter at monitor with cursor. Can be a semicolon separated list
## position = x y ("50% 50%" by default)  Login window position
## default-user-image = Image used as default user icon, path or #icon-name
## hide-user-image = false|true ("false" by default)
## round-user-image = false|true ("true" by default)
## highlight-logged-user  = false|true ("true" by default)
##
## > Panel:
## panel-position = top|bottom ("top" by default)
## clock-format = strftime-format string, e.g. %H:%M
## indicators = semi-colon ";" separated list of allowed indicator modules. Built-in indicators include "~a11y", "~language", "~session", "~power", "~clock", "~host", "~spacer", "~layout". Unity indicators can be represented by short name (e.g. "sound", "power"), service file name, or absolute path
## keyboard-layouts = semi-colon ";" separated list keyboard layouts to be listed by the "~layout" indicator (empty by default which provides all available layouts)
##
## > Accessibility:
## a11y-states = states of accessibility features: "name" - save state on exit, "-name" - disabled at start (default value for unlisted), "+name" - enabled at start. Allowed names: contrast, font, keyboard, reader.
## keyboard = command to launch on-screen keyboard (e.g. "onboard")
## keyboard-position = x y[;width height] ("50%,center -0;50% 25%" by default)  Works only for "onboard"
## reader = command to launch screen reader (e.g. "orca")
## at-spi-enabled = false|true ("true" by default) Enables accessibility at-spi-command if the greeter is built with it enabled
##
## Security:
## allow-debugging = false|true ("false" by default)
## screensaver-timeout = Timeout (in seconds) until the screen blanks when the greeter is called as lockscreen
##
## > Session:
## default-session = session manager to be started when none has been selected by the user and no one is set as last used (unset by default)
##
## > Template for per-monitor configuration:
## [monitor: name]
## background = overrides default value
## user-background = overrides default value
## laptop = false|true ("false" by default) Marks monitor as laptop display
## transition-duration = overrides default value
##

[greeter]

##
### Tail: Section / greeter
################################################################################




################################################################################
### Head: Section / greeter / Appearance
##

background = /usr/share/backgrounds/default-login.jpg
theme-name = Arc-Dark
icon-theme-name = Papirus-Dark
cursor-theme-name = breeze_cursors
cursor-theme-size = 24

##
### Tail: Section / greeter / Appearance
################################################################################




################################################################################
### Head: Section / greeter / Font
##

font-name = Ubuntu 11
xft-antialias=true
xft-dpi=96
xft-hintstyle=hintslight
xft-rgba=rgb

##
### Tail: Section / greeter / Font
################################################################################




################################################################################
### Head: Section / greeter / Login window
##

position = 50%,center 57%,center
default-user-image = #face-smile
#default-user-image = #avatar-default

##
### Tail: Section / greeter / Login window
################################################################################




################################################################################
### Head: Section / greeter / Panel
##

panel-position = top
#panel-position = bottom
indicators = ~host;~spacer;~clock;~spacer;~language;~session;~a11y;~power
clock-format = %A %Y-%m-%d %H:%M:%S
show-clock = true

##
### Tail: Section / greeter / Panel
################################################################################




################################################################################
### Head: Section / greeter / Accessibility
##

keyboard = onboard

##
### Tail: Section / greeter / Accessibility
################################################################################




################################################################################
### Head: Section / greeter / Security
##

allow-debugging = true
screensaver-timeout = 60

##
### Tail: Section / greeter / Security
################################################################################
```
