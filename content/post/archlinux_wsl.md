---
title: "How to install ArchLinux on WSL2 from scratch"
date: 2022-06-15T17:43:38+08:00
author:      "pompipi"
image:       ""
tags:        ["coding"]
categories:  ["Tech" ]
draft: false
---

# How to install ArchLinux on WSL2 from scratch
19 Feb 2022

1. Install Docker desktop on windows and enable WSL2 integration
2. Need an existing WSL2 distribution already installed, because we need to run Docker from there. Use Ubuntu.
3. Install ArchLinux Docker container from Ubuntu WSL2. This will be the basis of the distribution installed on WSL2.
4. Run the container, and setup some things like users etc.
5. Add user to `wheel` group, and enable by `visudo` and uncomment:
```
## Uncomment to allow members of group wheel to execute any command with no passwd
%wheel ALL=(ALL) ALL NOPASSWD: ALL
```
6. Export image into tar file
7. Register ArchLinux tar file to WSL2
8. To set default login user, edit wsl.conf to include [user] default=username 
9. Edit /etc/pacman.conf to enable pacman progress bar and color
