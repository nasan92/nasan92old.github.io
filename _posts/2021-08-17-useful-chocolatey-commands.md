---
title: 'useful chocolatey commands '
date: 2021-08-17
permalink: /posts/2021-08-17/08/useful-chocolatey-commands/
tags:
  - Chocolatey
---

# Useful Chocolatey commands

search a package:
````powershell
choco search appname
````

Install a package
````powershell
choco install appname
````

list all installed packages
````powershell
choco list -localonly
````

list specific package
````powershell
choco list appname
# example
choco list bicep
````

upgrade specific package:
````powershell
choco upgrade appname
````

upgrade all packages
````powershell
choco upgrade all
````

