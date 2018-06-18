---
title: 'Tablet Installation and Configuration'
---

Tablets from the Ideas Box come pre-configured. However, last-minute needs may arise on-site. 

You must therefore be responsive to these needs!

>>>>>**We strongly recommend that you use a computer with Linux for all operations described below.**

## Installation

You can choose from two procedures for the installation of new applications on the tablets.

**You decide to activate Google Play store on all tablets**

* This requires you to create a Google account
* You must configure each tablet to configure the Google account
* Select each application to be installed
  Check and where necessary configure some tablets to reboot any that were unable to download all the applications

**You decide not to use Google play store and conduct a bulk installation of applications via a computer**

* This means that you must have all the applications with you. If you do not, you will probably have to follow the procedure above, but only on one tablet 
* Use a computer with Linux \(as it is very easy to install the utility\)
* Have the script required for bulk installation 
* Be aware that each tablet must be connected to the computer

### Advantages and disadvantages of the two solutions

**The Google Play Store** solution could be practical if your partner wishes to enjoy a level of independence and plans to install new applications regularly. However, this procedure is not recommended in areas with low-speed Internet access, as the applications must be downloaded onto each tablet. \(One application may take up to 150Mo\). That said, this procedure could be reassuring for a partner with limited technical skills. You must know that you are entering into the Google universe at your own risk, but this is practically unavoidable if you wish to use applications which must be purchased.

**The solution without Google Play Store** is very interesting but requires some technical skills and a transfer of knowledge to the partner in this regard. In addition, as we are using the bash script with the ADB utility, we can also take the opportunity to remove unnecessary applications or those that do not work. In this case, the applications are only downloaded once, which could be appropriate in areas with low-speed Internet access. Either you already have the applications on your computer, or you can download them directly with [Google Play Downloader](http://codingteam.net/pro%20ject/googleplaydownloader), in which case you must configure a valid Google account in the "settings" in order to download the applications.

## Using Google Play Downloader

This software is used to download Android applications directly from the Play Store. It should be noted, however, that some applications are not visible on this tool, although they are well and truly present on the Play Store... If you manage to find all your applications, we strongly advise that you use this method instead of the much more fastidious method described above. Skip directly to the section on **Installing and removing applications in bulk.**

## Activating the Play Store and downloading

The idea is to install the latest applications.

1. Create a Gmail account to access Google Play
2. Configure the Google Apps on the tablet with the previously created account

   * The Google Play Store icon may be hidden on Danew tablets, if this is the case
     * Application menu
     * Click on Paramètres -&gt; Applications -&gt; Toutes tab \(Settings -&gt; Applications -&gt; All\)
     * Select the Google play store application
     * Then click on Lancer \(Run\) in the middle/end of the page
     * A new window will open to request your Gmail user name and password

3. Once saved, download the applications required

4. Also, download the [File Expert](https://play.google.com/store/apps/details?id=xcxin.filexpert) application to keep a back-up copy of your downloaded applications.

At this point, you have downloaded your free applications and purchased others. You must now create a back-up of your new applications so they can be applied to all your tablets.

**ATTENTION** This application ONLY saves applications and does **not save data**. This means that some applications saved AND restored on another tablet will not work. To save data, your tablet must be ROOTED!

1. Open **File Expert**

2. Open the left-hand menu, Icon \(=\)

3. Scroll down to **Categories** and click on **Applications**

4. Select **Applications installées \(Installed Applications\)**

5. In the panel that opens, select \(by holding down\) the applications you wish to save.

6. Once completed, click on the icon on the top-right, of a circle with a dot in the middle. This will start to save all the applications that you selected.

7. Once the back-up is made, open the left-hand menu again and select **Stockage interne \(Internal storage\)**, click on **backup\_apps** and you should find all your applications saved.

8. Lastly, to recover them on your workstation, connect the tablet to your computer using the USB cable.

9. When the window opens, select **Stockage interne \(Internal storage\)** and copy all the saved applications onto your computer.

You now have all the applications you have downloaded and are ready to install them on your tablets.

# Installing and removing applications in bulk

## For Danew tablets

If this is the first time you are connecting a Danew tablet to your computer, the latter may not be able to communicate correctly with Danew tablets. You must therefore run this command in a terminal

```
echo "0x0e8d" > ~/.android/adb_usb.ini
```

And add this line  
`SUBSYSTEM=="usb", ATTR{idVendor}=="0e8d", MODE="0666", GROUP="plugdev"` in the file `/etc/udev/rules.d/51-android.rules`

## The ADB utility

A utility called  `ADB`  available for Linux uses a command line to install a collection of files **.apk** \(Android application\) on an Android device.

> If the ADB utility is not installed on your PC, here is the command to run to install it on a Linux system: `sudo apt-get install android-tools-adb`

The default setting does not enable you to install applications directly from the command line. If the Google Play pack is not installed on the device, the only way to install applications is via the utility with the ABD command line.

[**You must therefore start by authorising the installation of third-party applications in the Android settings.**](http://www.frandroid.com/comment-faire/lemultimedia/231266_autoriserlessourcesinconnues)

### Uninstalling applications

You may have the nasty surprise of having to uninstall some applications in order to install others \(lack of memory space\).

To do so, you must find the name of the application.

Ex : [Helium - App Sync and Backup](https://play.google.com/store/apps/details?id=com.koushikdutta.backup&hl=fr)

The URL bar contains the application’s full name : [https://play.google.com/store/apps/details?id=com.koushikdutta.backup&hl=fr](https://play.google.com/store/apps/details?id=com.koushikdutta.backup&hl=fr)

The name is just after `id=` therefore `com.koushikdutta.backup`

Find and note all the applications you wish to remove in a file  `app_a_supprimer.csv`

### Transferring APK files

If your applications were on a tablet, send them to your computer in a folder named `apk`

* Create a folder  `android_app`  somewhere on your computer \(e.g.:  `/home/`\)
* Move the file  app\_a\_supprimer.csv  and the folder  apk  to your new folder  android\_app
* Create a file  and paste the content below

  ```
  #!/bin/bash
  while IFS='' read -r line || [[ -n "$line" ]]; do
     adb uninstall $line
  done < "app_a_supprimer.csv"
  ```

* `find apk/ -name '*.apk' -exec adb install -r {} \;`

* Open a terminal

* Move to your work folder, e.g.  `cd /home/android_app`

* Authorise file `delete_install_android_app.sh` to run with  `chmod +x delete_install_android_app.sh`

* Run the application deletion and installation  `script./delete_install_android_app.sh`
* The script above will uninstall the applications listed in the CSV file and will install all applications available in the APK folder.
* You must then manually place the icons of the new applications on the desktop.



