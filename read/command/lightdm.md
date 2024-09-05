---
title: lightdm
nav_order: 8010
has_children: false
parent: Command
---


# lightdm




## Usage


### help

執行

``` sh
lightdm --help
```

顯示

```
Usage:
  lightdm [OPTION?] - Display Manager

Help Options:
  -h, --help                Show help options

Application Options:
  -c, --config=FILE         Use configuration file
  -d, --debug               Print debugging messages
  --test-mode               Run as unprivileged user, skipping things that require root access
  --pid-file=FILE           File to write PID into
  --log-dir=DIRECTORY       Directory to write logs to
  --run-dir=DIRECTORY       Directory to store running state
  --cache-dir=DIRECTORY     Directory to cache information
  --show-config             Show combined configuration
  -v, --version             Show release version

```




### version

執行

``` sh
lightdm --version
```

顯示

```
lightdm 1.32.0
```




### show-config

執行

``` sh
lightdm --show-config
```

顯示

```
   [Seat:*]
B  allow-guest=false
E  session-wrapper=/etc/X11/xinit/Xsession
G  xserver-command=X -core -noreset
I  greeter-session=lightdm-gtk-greeter

   [LightDM]
C  minimum-vt=1
D  run-directory=/run/lightdm
F  user-authority-in-system-dir=true

Sources:
A  /usr/share/lightdm/lightdm.conf.d/50-backup-logs.conf
B  /usr/share/lightdm/lightdm.conf.d/50-disable-guest.conf
C  /usr/share/lightdm/lightdm.conf.d/50-minimum-vt.conf
D  /usr/share/lightdm/lightdm.conf.d/50-run-directory.conf
E  /usr/share/lightdm/lightdm.conf.d/50-session-wrapper.conf
F  /usr/share/lightdm/lightdm.conf.d/50-user-authority-in-system-dir.conf
G  /usr/share/lightdm/lightdm.conf.d/50-xserver-command.conf
H  /usr/share/lightdm/lightdm.conf.d/60-lightdm-gtk-greeter.conf
I  /etc/lightdm/lightdm.conf

```




## test-mode

執行

``` sh
lightdm --test-mode --debug
```

顯示

```
Running inside an X server requires Xephyr to be installed but it cannot be found.  Please install it or update your PATH environment variable.
```

所以要先安裝「Xephyr」，然後再執行「`lightdm --test-mode --debug`」才可以看到預覽。
