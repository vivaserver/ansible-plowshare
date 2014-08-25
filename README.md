# Ansible role for plowshare

Installs the **plowshare** package from it's [official Ubuntu PPA][ppa].

[plowshare][plw] is a command-line (CLI) download/upload tool for around 70+ different file sharing websites (hosters).
It has a small footprint (few shell scripts). No java, no python!

This role addresses the fact that the `plowshare` package for Ubuntu 12.04 depends on curl >= 7.24, 
but the latest curl version for that Ubuntu release is 7.22, a [known bug][bug].

Thus the *unstable* PPA [costamagnagianfranco/ettercap-stable-backports][ppa] is used for get an updated version of Curl that fulfills the plowshare package dependency.

## Requirements

Ubuntu 12.04 "Precise Pangolin" or later, including [elementaryOS][eos] 0.2 "Luna".

## Installation

    $ ansible-galaxy install vivaserver.plowshare 

## Example Playbook

    - hosts: localhost
      roles:
        - vivaserver.plowshare

## License

MIT

## Copyright

(c)2014 Cristian R. Arroyo

[plw]: https://code.google.com/p/plowshare/
[ppa]: https://launchpad.net/~plowsharepackagers/+archive/ppa
[eos]: http://elementaryos.org
[bug]: https://bugs.launchpad.net/plowshare/+bug/1254152
[ppa]: https://code.launchpad.net/~costamagnagianfranco/+archive/ubuntu/ettercap-stable-backports/+index?field.series_filter=precise

[pin]: https://help.ubuntu.com/community/PinningHowto
[blo]: http://www.jaredlog.com/?p=1820
