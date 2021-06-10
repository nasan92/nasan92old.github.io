---
layout: archive
title: "Tools"
permalink: /tools/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
Tool Downloader script: [https://github.com/nasan92/tooldownloader/releases/download/v1.0/Tool-downloader-gui.ps1](https://github.com/nasan92/tooldownloader/releases/download/v1.0/Tool-downloader-gui.ps1)

Here a list of some useful tools:

Sysinternals
======

Official link to the Sysinternals Website: [Sysinternals](https://docs.microsoft.com/en-us/sysinternals/)

| Tool | Description |
|--|--|
| [CPU Stres](https://docs.microsoft.com/en-us/sysinternals/downloads/cpustres) |  **CPU Auslastung simulieren**  <br> Mit dem Sysinternals Tool CPU Stress kann eine beliebige CPU Auslastung simuliert werden. Es können mehrere Threads hinzugefügt werden und das Aktivitätslevel der Threads kann angepasst werden ![Editing a markdown file for a talk](/images/cpustres.png ) |
| Testlimit | **RAM Auslastung simulieren** <br> Mit dem Sysinternals Tool testlimit kann eine beliebige RAM Auslastung simuliert werden. <br> Beispiel für 1024 MB: <br> `testlimit64.exe -d 1024 -c 1`|


Windows Built in Tools
======

| Tool | Description |
|--|--|
| FSUTIL | **Speicherplatzauslastung simulieren** <br> Um eine beliebige Speicherplatzauslastung zu simulieren, kann mit dem Tool **fsutil** eine beliebig grosse Dummy Datei erstellt werden (Es sind keine wirklichen Daten in diesem File, es reserviert nur den Speicher.) Syntax: <br> ``fsutil file createnew filename length ``<br> <br> Beispiel für eine 50MB grosse Datei: <br> ``fsutil file createnew test.txt 52428800 ``<br><br>![Editing a markdown file for a talk](/images/fsutil.png ) |


