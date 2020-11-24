---
title: "How to disable SIP system integrity protection"
date: 2020-05-24T07:53:06+08:00
type: page
image: "https://i.imgur.com/bWBmr5h.jpg"
cover: ""  # image show on top
url: "/solutions/disable-sip-system-integrity-protection.html"
comments: true
single: false  # display as a single page, hide navigation on bottom, like as about page.
---

<br/>
<br/>
{{< alert-multi-line theme="info" >}}

Many Mac users have reported that they cannot open after installing some software. It may be that the integrity of the ```SIP system``` has not been closed.
 
  Let's take a look at how to turn off sip system integrity.

```System Integrity Protection``` is a security technology adopted by OS X El Capitan and later, which can help prevent potential malware from modifying protected files and folders on your Mac. System integrity protection can restrict the root user account and the operations that the root user can complete in the protected part of the Mac operating system.

{{< /alert-multi-line >}}
 


The above is the official introduction, which is a bit scary. `Let’s put it another way, SIP is similar to windows firewall and Android phone Root. This should solve many people’s confusion.

The software in the Apple App Store runs in a sandbox and cannot access system files, so most of the software is castrated. Many excellent softwares are not on the Apple Store because they require SIP system permissions. Apple does not review. Some software adopts dual versions, divided into official version and App Store version. App Store is a simple and simple version, and the full-featured version needs to be downloaded separately. 

By default, macOS only allows software downloaded through the Apple App Store to run.

If you want to install third-party applications on macOS, you need to enable the option to allow App Store and approved developers in `System Preferences>> Security and Privacy>> General

If you want to install a third-party unsigned application on macOS, you need to execute the command line `sudo spctl --master-disable` in the terminal to enable any source option. In `System Preferences> Security and Privacy> General`, this option is not available by default. 

---

If you want to install some decompiled and cracked applications on macOS, you need to turn off SIP.

From the above, everyone should be able to see that Apple is working hard for everyone's safety, but is it really just what everyone sees?


If you want to install software from any source, you need to open the terminal and enter commands. If you want to close SIP, you need to shut down to operate (in the early macOS system, you don't need to shut down). Why is it more and more troublesome?

It is put on the Apple App Store, and every time it is sold, Apple takes 1/3. For example, if your software sells for $100 , Apple takes $33.33.

The so-called approved developer is to go to Apple to buy a developer account, and then use the developer account to sign the application. 

Purchasing Apple’s developer account, personally 99 US dollars per year. The enterprise is 299 US dollars per year.


<br/>
<br/>
<br/>
<br/>


**Stop talking nonsense, let's get to the point.**

At present, the latest 10.15.x system using cracked software basically needs to close SIP to open it, even if it is genuine software, there are a lot of apps that need to be closed SIPs, which needs to be closed permanently! 

`Don't ask questions like [Can I open Sip again after it is off?].`

After reading the above instructions, if you still don’t worry about opening the system permissions, you have the following options, ***I will never close SIP, I don't want to use this software!***

<br/>
<br/>
<br/>
<br/>

---
#### Check status

Before closing the SIP system integrity, we first check whether the SIP system integrity protection is enabled.

Open the `terminal` and enter the following command and press Enter:

```
csrutil status
```

You will see one of the following messages, indicating SIP status

enabled is not closed:

`System Integrity Protection status: enabled.`

disabled:

`System Integrity Protection status: disabled`

If it is not closed, you need to close SIP!

<br/>
<br/>

#### Shut Down

1. Shut down and restart your Mac, keep pressing `Command+R` while booting to enter `Recovery Mode`.

2. Open the terminal after entering Recovery mode, as shown in the figure:

![Recovery Mode](https://i.imgur.com/sH27F09.jpg)


3. Enter the command csrutil disable on the terminal and press Enter.

The terminal prompt: `Successfully disabled System Integrity Protection. Please restart the machine for changes to take effect. ` indicating that you have successfully turned off SIP protection.

4. Click the Apple icon in the upper left corner, and then click Restart, you can use the application downloaded from the website normally.
