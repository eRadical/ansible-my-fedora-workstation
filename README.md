Ansible Playbook to make some adjustments to a Fedora Workstation
====================================================================
[![Build Status](https://travis-ci.org/eRadical/ansible-my-fedora-workstation.svg?branch=master)](https://travis-ci.org/eRadical/ansible-my-fedora-workstation)

This is my setup. It was created to be of help when re-installing a Fedora Workstation... or keeping it up to date.
By no means this is complete or suitable as is for you... but if you want something don't hesitate to ask in [Issues](https://github.com/eRadical/ansible-my-fedora-workstation/issues) or even better a [Pull request](https://github.com/eRadical/ansible-my-fedora-workstation/pulls).

Workstation role changes:
=========================
- Installs RPM Fusion repos (free & non free)
- Installs Slack repo
- Installs a lot of packages (see them in roles/machine.workstation/defaults/main.yml) and also removes others (evolution)
- Enables some services (numad, tuned, ntpd) and also disables others (iio-sensor-proxy)
- Installs Google Chrome (stable by default, it can also do beta and/or unstable)

Developer role changes:
=======================
- Installs a lot of packages used by sysadmins and/or developers (awscli, s3cmd, docker, golang, php, meld, strace, etc.)
- Installs development tools
- Installs PyCharm Community Edition
- Installs PhpStorm
- Installs GoLand
- Installs Atom

How to run...
=============

- You should make sure you can `sudo` to `root` without password,
- Clone the repo,
- Change variables from the symlink `customize-me` as you wish,
- Open a terminal in the folder it was cloned,
- Run the script `./configure-fedora`
