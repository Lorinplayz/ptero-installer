# 🐦 pterodactyl-installer By Lorin

Shellcheck License: GPL v3 Discord made-with-bash

Unofficial scripts for installing Pterodactyl Panel & Wings. Works with the latest version of Pterodactyl!

Read more about Pterodactyl here. This script is not associated with the official Pterodactyl Project.

Features
Automatic installation of the Pterodactyl Panel (dependencies, database, cronjob, nginx).
Automatic installation of the Pterodactyl Wings (Docker, systemd).
Panel: (optional) automatic configuration of Let's Encrypt.
Panel: (optional) automatic configuration of firewall.
Uninstallation support for both panel and wings.
Help and support
For help and support regarding the script itself and not the official Pterodactyl project, you can join the Discord Chat.

Supported installations
List of supported installation setups for panel and Wings (installations supported by this installation script).

Supported panel and wings operating systems
Operating System	Version	Supported	PHP Version

Ubuntu	14.04	🔴
16.04	🔴 *	
18.04	🔴 *	
20.04	🔴 *	
22.04	✅	8.3
24.04	✅	8.3
Debian	8	🔴 *	
9	🔴 *	
10	✅	8.3
11	✅	8.3
12	✅	8.3
13	✅	8.3
CentOS	6	🔴	
7	🔴 *	
8	🔴 *	
Rocky Linux	8	✅	8.3
9	✅	8.3
AlmaLinux	8	✅	8.3
9	✅	8.3`
* Indicates an operating system and release that previously was supported by this script.

Using the installation scripts
To use the installation scripts, simply run this command as root. The script will ask you whether you would like to install just the panel, just Wings or both.

bash <(curl -s https://pterodactyl-installer.se)
Note: On some systems, it's required to be already logged in as root before executing the one-line command (where sudo is in front of the command does not work).

Here is a YouTube video that illustrates the installation process.

Firewall setup
The installation scripts can install and configure a firewall for you. The script will ask whether you want this or not. It is highly recommended to opt-in for the automatic firewall setup.

Development & Ops
Testing the script locally
To test the script, we use Vagrant. With Vagrant, you can quickly get a fresh machine up and running to test the script.

If you want to test the script on all supported installations in one go, just run the following.

vagrant up
If you only want to test a specific distribution, you can run the following.

vagrant up <name>
Replace name with one of the following (supported installations).

ubuntu_jammy
debian_bullseye
debian_buster
debian_bookworm
debian_trixie
almalinux_8
almalinux_9
rockylinux_8
rockylinux_9
Then you can use vagrant ssh <name of machine> to SSH into the box. The project directory will be mounted in /vagrant so you can quickly modify the script locally and then test the changes by running the script from /vagrant/installers/panel.sh and /vagrant/installers/wings.sh respectively.

Creating a release
In install.sh github source and script release variables should change every release. Firstly, update the CHANGELOG.md so that the release date and release tag are both displayed. No changes should be made to the changelog points themselves. Secondly, update GITHUB_SOURCE and SCRIPT_RELEASE in install.sh. Finally, you can now push a commit with the message Release vX.Y.Z. Create a release on GitHub. See this commit for reference.

Contributors ✨
Copyright (C) 2018 - 2025, Vilhelm Prytz, vilhelm@prytznet.se, and contributors!

Created by Vilhelm Prytz
Maintained by Linux123123
Thanks to the Discord moderators sam1370, Linux123123 and sinjs for helping on the Discord server!
