# apparmor-runit

* [Overview](#overview)
* [Changes](#changes)
* [Install](#install)
* [Licence](#licence)
* [Contact](#contact)

## Overview

This a rewrite of the stage 1 runit script of Apparmor from Void Linux. The current
script doesn't allow you to set some profiles to complain mode. You could only set one
mode to all of the profiles. This script allows you to set some of the profiles to
complain mode so that you could use the confined program without breakage while still
refining the profile with `aa-logprof`

## Changes

- Script now primarity consists of functions instead of nested if statements
- Added functionality to specify the profiles you'd want to set to complain mode.

Add values to the `complain_list` array from /etc/rc/apparmor.conf

    #!/bin/bash

    # AppArmor configuration
    # Possible options:
    # - disable
    # - complain
    # - enforce
    APPARMOR="enforce"

    # Complain profiles
    complain_list=(
    "usr.bin.newsboat"
    "usr.bin.w3m"
    "usr.bin.qbittorrent"
    "usr.bin.curl"
    "usr.bin.aria2c"
    "usr.bin.yt-dlp"
    )

## Install

    git clone https://github.com/snowstorm3842/apparmor-runit.git
    cd apparmor-runit/
    sudo cp ./apparmor /usr/lib/rc/sv.d/apparmor

## Licence

    GPLv3

## Contact

- **Email**: snowstorm3842@mailbox.org
