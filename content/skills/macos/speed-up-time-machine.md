---
title: "Time Machine on Mac backup is too slow (speed up backup command)"
date: 2019-10-25T19:28:14+08:00
url: /macos/speed-up-time-machine.html
type: "macos"
image: "https://cdn.jsdelivr.net/gh/Rhinocros/minorpatch-static@pics/uPic/cmwOF1.jpg"
categories:
  - "macos"
tags:
  - Time Machine
  - macOS
  - frequent backups
  - prevent accidents
  - Catalina
  - WiFi
  - machine backup
  - time machine backup slow
  - network storage
keywords:
- Time Machine
- macOS
- frequent backups
- prevent accidents
- Catalina
- WiFi
- machine backup
- time machine backup slow
- network storage
description: "I believe that anyone who has used a computer for a while knows the importance of frequent backups. Especially recently, many people need to upgrade their Mac to the latest version of macOS Catalina"
comments: true
---


I believe that anyone who has used a computer for a while knows the importance of frequent backups. Especially recently, many people need to upgrade their Mac to the latest version of macOS Catalina. To prevent accidents, it is even more necessary to make a backup before you start.

The "Time Machine" that comes with macOS is definitely the most convenient backup tool on the Mac. It is completely free and can back up in the background silently for you, "because it was developed by Apple itself." Compatibility is also the best, so everyone is recommended to use Time Machine to back up Mac computers.

Solve the problem that the time machine backup speed is too slow
However, when some students tried to use the time machine to back up the system data, they found that its first backup speed was very slow. It didn't seem to match their network and machine configuration, and sometimes it took more than 48 hours to complete it. After closing all apps, the backup speed did not increase significantly.

In fact, the time machine backup is too slow because macOS itself restricts the flow of it. It limits the frequency of hard disk reads and writes and the use of memory. It is mainly to prevent users from using the computer during the backup. . But if you are waiting for it to complete the backup, and then go to the system upgrade or other operations, it is more tragedy.

macOS Time Machine Backup Acceleration Command
If you really intend to let the time machine work at full speed and full speed, then there is a way, that is, through the command line, use the command to force the system to restrict the time machine's current limit, commonly known as "unsealing". Open a terminal and enter the following command:

```
sudo sysctl debug.lowpri_throttle_enabled = 0
```


At this time you will find that the backup time of the time machine has become much faster! !! Basically can reach the speed that the network and hard disk read and write. After it completes the first backup, you can execute the following command to restore the original current-limiting state to ensure that when using the computer in the future, the time machine backup will not take up too many resources and cause card changes.

```
sudo sysctl debug.lowpri_throttle_enabled = 1
```

Of course, if your time machine backup is saved on the NAS or router's network storage, it is recommended to connect a “network cable” for the first backup, which is much more stable than the speed of WiFi. Also, if you use a MacBook, remember to turn on the power and back up to get the best speed.
