# Patching YouTube using ReVanced CLI

* Assuming you have built [ReVanced CLI](https://github.com/CriticalRange/revanced-cli/wiki/Building-the-ReVanced-CLI), [ReVanced Patcher](https://github.com/CriticalRange/revanced-cli/wiki/Building-ReVanced-Patcher), [ReVanced Patches](https://github.com/CriticalRange/revanced-cli/wiki/Building-ReVanced-Patches) and ready to build the YouTube APK

## Setting Up Directory

* (It is recommended to use file explorer for this part, again)

* Create a new folder in root directory called `revanced`

* Copy the builds of both [ReVanced Patches](https://github.com/CriticalRange/revanced-cli/wiki/Building-ReVanced-Patches) and [ReVanced CLI](https://github.com/CriticalRange/revanced-cli/wiki/Building-the-ReVanced-CLI) (builds are in `build/libs`), paste them into the revanced folder you created and name them `revancedpatches.jar` and `revancedcli.jar` respectively.

* Copy the downloaded YouTube APK into that folder as well and rename it to `youtube.apk`

* Create a new folder inside revanced folder named `output`

Set up [ADB](https://www.xda-developers.com/all-in-one-guide-to-adb/) if you haven't already.

You're ready to go!

## Patching YouTube with ReVanced CLI

* Firstly, get into your terminal and change directory to revanced folder

`cd revanced`

* Then start patching

`java -jar revancedcli.jar -a youtube.apk -p revancedpatches.jar -o output --run-on yourdevicename`

For `yourdevicename*`, type `adb devices` and copy the IP of your device and replace it with `yourdevicename`

If you set ADB correctly, YouTube should be opened in your device, if not, you should have an APK sitting at revanced/output/ named `revanced.apk`, send it to your device and sideload it.

## Congratulations🎉!

You have just patched the YouTube APK and built it into your device
Remember to share this wiki with your friends and thank the devs at discord for their hard work!

