```
       ______
      (  mu  )
       ------
          \   ^__^
           \  (oo)\_______                s i g h t
              (__)\       )\/\
                  ||----w |
                  ||     ||

```

<br/>

## 1: howtostart

[alpine](https://alpinelinux.org/downloads/) standard | extended | virtual image & [installation](https://docs.alpinelinux.org/user-handbook/0.1a/Installing/manual.html)

```bash
# example
setup-keymap → setup-hostname → setup-interfaces  ↓
  rc-service networking start → setup-timezone    ↓
setup-apkrepos → passwd → setup-sshd → setup-ntp  ↓
rc-update add networking boot → setup-disk → reboot


# note: do not create a user account (since 3.16.0)
```

## 2: git, clone

```
# apk add git
# git clone https://github.com/llightcb/sight.git
```

## 3: run script

```
# sh sight/install.sh
```

## overview

```
https://raw.githubusercontent.com/llightcb/sight/main/screen.png
```

## trivials

```
.. but non-self-explanatory

 - enable xwayland → comment sway config line 2
 ~ resolution, refresh rate sway config line 10
 ~ cursor theme and/or size sway config line 34
 ~ default terminal font - size foot.ini line 7
 + gpu accel. for browser → sway config line 64

 - execute commands as another user → run: doas
 - local-video-profile: $ mpvl <_path_to_file_>
 - if laptop: $ doas powertop --html=power.html
 - interrupt key = ctrl+shift+c (ctrl+c = copy)
 - VMSVGA → $ set -Ux WLR_NO_HARDWARE_CURSORS 1

 $ dnv /etc/dnscrypt-proxy/dnscrypt-proxy.toml
 | list → https://dnscrypt.info/public-servers
 $ dnv /etc/chrony/chrony.conf → change to nts
 | an _example_: branch platonic → chrony.conf
 - if you poweroff/reboot, some error messages
 | will appear. but there's nothing to see via
 | $ rcl -v if $ rcl is enabled? answer on irc

 |→ "if you poweroff/reboot, stuff gets killed
 | randomly & something errors in the stack of
 | stuff, running in the wm. _these errors are
 | harmless_ - they would be outputted by sway
 | itself, so it's logging to stdout/stderr &&
 | so it's logs are still there when it closes
 | right before poweroff/reboot." ------------

 - run: $ ipt --sf / $ bll -r / $ bll -g # end
```

## function

```bash
$ cbb       # <cmd> busybox ?
$ nnn       # tiny adjustment
$ dnv       # doasnvim ~/init
$ 2fa       # <foo>  oathtool
$ cpu       # (oo) → $ cpu -h
$ esa       # eval → ssh agent
$ img       # picture overview
$ chc       # chrony check ntp
$ iso       # wipe -a/-o write
$ cfn       # cleanup filename
$ bit       # suid / sgid bits
$ trim      # fstrim / +output
$ logs      # (oo) → $ logs -h
$ mpvl      # mpv localprofile
$ pkgi      # info: $ pkgi -h
$ fhd       # <foo> dd fish ↓
$ ffp       # (oo) → $ ffp -h
$ sfm       # (oo) → $ sfm -h
$ man       # more less 4 man
$ ipt       # (oo) → $ ipt -h
$ bll       # (oo) → $ bll -h
$ mpc       # kernel ↓modules
$ sh2       # sync /home/ to:
$ rcl       # rclog: $ rcl -h
$ ff        # ? → $ ff --help
$ pw        # pass: → $ pw -h
$ cd        # cd + list files
$ nt        # note: → $ nt -h
$ se        # hwmon  coretemp
$ pv        # ⏎ search/stream
$ rs        # reset  terminal
$ vi        # stands 4 neovim
$ gd        # git diff less+c
```

## shorten

```bash
$ fhd      # no shell history
$ 2fa      # no shell history
$ pw       # no shell history
$ nt       # no shell history
$ rm       # careful +verbose
$ fp       # fish record: off
$ rca      # status: services
$ pdf      # zathura:  --fork
# git commands: $ abbr --show
```
