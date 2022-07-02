# apparmor-runit

* [Overview](#overview)
* [Changes](#changes)
* [Install](#install)
* [Licence](#licence)
* [Contact](#contact)

## Overview

This a rewrite of the stage 1 runit script of Apparmor from Void Linux.

## Changes

- Script now primarity consists of functions instead of nested if statements

## Install

    git clone https://github.com/snowstorm3842/apparmor-runit.git
    cd apparmor-runit/
    sudo cp ./apparmor /usr/lib/rc/sv.d/apparmor

## Licence

    GPLv3

## Contact

- **Email**: snowstorm3842@mailbox.org
