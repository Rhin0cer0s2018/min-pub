---
title: "Mac apps that cannot be opened or files are damaged"
type: page
date: 2020-08-20T13:06:46+08:00
url: /solutions/caption-of-apps-cant-be-opened.html
image: https://i.imgur.com/D2mDT6g.jpg
alert: info
comments: false
---

After some users downloaded some programs, but could not be installed in MAC, a warning box as shown in the figure below popped up during installation: "Cannot open xxx because it is from an unidentified developer". 

So how to solve this problem?

When installing some software under MAC, it prompts "from unidentified developer". In fact, this is the new security mechanism of the new MAC system.

By default, only software downloaded from the Mac App Store and applications signed by a developer ID are trusted.

In other words, by default, the MAC system can only install software downloaded from reliable channels (Mac App Store audited by Apple) or software developed by approved people.

This is of course so that users will not be fooled into installing rogue software, but "honest software" without the developer's signature is also affected. The installation will pop up a warning box as shown in the figure below: "Cannot open xxx, because it comes from identity Unknown developer".

There are two solutions to this problem:





1. The easiest way: After pressing Control, click the software icon again. 

2. Modify the system configuration: System Preferences... 

System Preferences -> Security and Privacy -> Authentication -> Modify to any source


{{< alert-multi-line theme="info" >}}

Without this option (macOS Sierra 10.12)

A. Open the terminal and enter ```sudo spctl --master-disable```

B. Press Enter

C. You will see a key icon behind the password, and then you can continue to enter your own computer unlock password without worrying about it (the password you entered is not displayed when you enter it)

D. Go back to privacy and you will see any source.

{{< /alert-multi-line >}}




