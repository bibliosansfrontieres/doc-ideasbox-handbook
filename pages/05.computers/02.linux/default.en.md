---
title: 'Linux Ubuntu'
---

## Ubuntu

Ubuntu is a user-friendly Linux distribution with a "simple, intuitive, and secure" interface.

By default, the computer starts up using Ubuntu.

### Installation

LTS (Long Term Support) versions, which are supported for five years, are preferred.  Version 16.04 recently replaced 14.04.  There are currently some concerns regarding guest sessions on version 18.04.

On top of Ubuntu, we install the [```edubuntu-desktop```](https://packages.ubuntu.com/xenial/edubuntu-desktop) package, which pulls a set of educational applications.

The installation and configuration can both be done using an ansible playbook (an automization tool for configuration and management) called `idbuntu`
([that is available on Github](https://github.com/bibliosansfrontieres/idbuntu)). The reading, although technical, describes the implementation in its entirety.

## Sessions

There are three types of user sessions.

### Guest Session

**The Guest session** is designed for users.

Among other characteristics, this session hais amnesia: once opened, it is a completely new session, recreated based on a model, and the session is erased once it is closed.  Because of this, we don't have to worry about potential information left by each user, such as personal documents or log-in information for websites.

### `ideasbox` Session

**The `ideasbox` Session** serve as a model for guest sessions.

Any customizations, such as wallpaper or shortcuts, made in the ideasbox session will be replicated in the guest session model. Thus, the ideasbox session is not meant to be used daily.

To login to an ideasbox session, use the username `ideasbox`.  BSF will send the password to you upon request.

### Admins Sessions

**The `Local Admin` Session** can be used for the administration and maintenance of the system. This is the only session with administrative rights, and thus the only one that permits you to add or delete software or programs, change the network configuration, and edit other system components.

The first time you open a session using this account, a password change is required. The initial password is `ChooseAStrongPasswordPLZ` and you're kindly invited to do so.

There is an other admin account, which is `bsfadmin`, used for maintenance/troubleshooting from the BSF team. The BSF technicians' SSH keys remain present in the root account.  If they are deleted, no support can be provided.

### See Also

  * [Script to create accounts](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/users/tasks/main.yml)
  * [Customization of  guest sessions](https://help.ubuntu.com/community/CustomizeGuestSession) on the Ubuntu Wiki

## The Programs

The list of programs generally installed appear in [the playbook](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/software/tasks/main.yml).

These include office, image creation, video editing, photo retouching, music editing and publishing, programming, discovering, and gaming programs.

We also added the Tor browser (to surf the web anonymously), as well as Skype.

## Administration

To proceed to system administration, you must first of all contact BSF to put in place a dedicated account.  This account is not created automatically because it is rarely needed.  However, on some projects that have the necessary resources, having this account is a plus.

By default, Ubuntu automatically downloads and applies security updates.

## Upgrades

### From Ubuntu 14.04

The 14.04 version of Ubuntu is aa LTS (Long Term Support), for which support will be terminated in early 2019. It is time to upgrade to 16.04 at least, following the [standard process](https://tutorials.ubuntu.com/tutorial/tutorial-upgrading-ubuntu-desktop). But first, we have to deal with Skype.

Skype was removed from the partners repository, and a 64bits version was released. We first uninstall the old version:
```
sudo apt-get remove skype
sudo dpkg --remove-architecture i386
```
Then we reinstall Skype from a PPA:
```
sudo add-apt-repository ppa:andykimpe/skype
sudo apt-get update
sudo apt-get install skype
`
