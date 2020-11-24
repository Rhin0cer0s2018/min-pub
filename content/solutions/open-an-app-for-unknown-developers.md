---
title: "Open the application of an unidentified developer"
type: page
date: 2019-02-21T15:55:40+08:00
url: /solutions/open-an-app-for-unknown-developers.html
image: https://i.imgur.com/SusIlhm.jpg
comments: false
---

Mac OS X itself has a relatively complete set of security mechanisms (such as Gatekeeper), which can be very effective in preventing the automatic running of some potential malware, but sometimes these security mechanisms will also prevent some completely safe applications from running. .

---

▲ Unable to open the application prompt of an unidentified developer

### How Gatekeeper works

Gatekeeper was first introduced in OS X Mountain Lion. When you run an application, Gatekeeper will determine whether the application meets certain settings of the system security settings. If these settings are met, the application can run directly; otherwise, it refuses to open The application.

### Gatekeeper settings

Gatekeeper provides three different security settings: Mac App Store, Mac App Store and approved developers, any source.

1. __Mac App Store__：By default, if the application you want to open is from the Mac App Store, it will automatically approve the opening. Because before Apple puts the application on the Mac App Store, it will conduct a series of security checks on it, which can completely guarantee the security of the application.

2. __Mac App Store and approved developers__：Compared with the previous option, the condition of this option is a little looser. If an application cannot be listed on the Mac App Store, but the developer has a digital signature and certificate issued by Apple and built it into the application, the application can also be opened with Gatekeeper approval.

3. __Any source__：Gatekeeper has no restrictions on the running of applications. In view of the increasing trend of malware on the Mac OS X platform, I strongly recommend against choosing this setting.

### How to open an application from an unidentified developer

Remember, if you want to run an application identified as ```"From an unidentified developer"```, make sure you know where it came from.

__First step:__ Download the application and drag it into the ```Applications``` folder.

__Step 2: __ Hold down the ```control key``` and click (or ```right-click```), after the option menu pops up, select ```Open```.

You will see a pop-up window asking if you want to open this program.

__Step 3: __ Select the ```Open``` button.

> Note: From now on, Mac will remember that you allow this application to run, and when you run it again in the future, you won't have to go through this process again.

If you double-click to run and do not open the application, you can also refer to the Others Solution "[Mac apps that cannot be opened or files are damaged](/solutions/caption-of-apps-cant-be-opened.html)".
