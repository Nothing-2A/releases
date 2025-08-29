# LineageOS Downloads

### Requirements
The latest Android 15 firmware (Pacman-V3.2-250815-1642), an [unlocked bootloader](https://github.com/spike0en/nothing_archive#ii-unlocking-bootloader-) and USB debugging enabled from developer options.

The latest LineageOS .zip package and boot, super_empty and vendor_boot .img files for Pacman available [here](https://github.com/Nothing-2A/releases/releases).

The latest version of [Google's platform-tools](https://developer.android.com/tools/releases/platform-tools?hl=en#downloads) and a computer.

### First flash steps
Reboot to bootloader
```
adb reboot bootloader
```

Flash LineageOS recovery
```
fastboot flash boot boot.img
fastboot flash vendor_boot vendor_boot.img
fastboot wipe-super super_empty.img
```

Reboot to recovery
```
fastboot reboot recovery
```

Do a factory reset (Factory Reset > Format data / factory reset)

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from recovery
Reboot to recovery
```
adb reboot recovery
```

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

Reboot to System

### Manually updating from LineageOS Updater
Look at the [FAQS](https://github.com/Nothing-2A/releases#faqs), question 5

### Reporting bugs / requesting features
Create an issue [here](https://github.com/Nothing-2A/releases/issues) with the LineageOS exact version and steps on how to reproduce if it's an issue or what you want to be added into LineageOS.

Google Apps, Magisk, KSU and SafetyNet/Play Integrity related bugs/requests will be ignored and immediately closed !

Additionnally, if you aren't using exactly the same files available on the release section (ex: Using a different recovery like TWRP, a different kernel or being rooted), your issue will be ignored and immediately closed !

### FAQS
**Q1: How do I update my firmware after flashing LineageOS ?**

Answer: The latest firmware available for Pacman is included on the LineageOS .zip package, hence keeping your firmware updated on each updates.

**Q2: Are Google Apps included with LineageOS ?**

Answer: Yes they are, however it's a very minimal list of Google Apps that are included with the LineageOS .zip package which give you access to the Google Mobile Services.

**Q3: Will there be any Google Apps free release of LineageOS ?**

Answer: Maybe, but it isn't planned at the moment with the **UNOFFICIAL** release of LineageOS, however they will most likely come Google Apps free and without any [fenrir]() support if I apply for **OFFICIAL** one day.

**Q4: Is the LineageOS .zip package is signed and passes SafetyNet and Play Integrity ?**

Answer: No, however you can flash fenrir to pass BASIC_INTEGRITY, DEVICE_INTEGRITY and STRONG_INTEGRITY !

I personnally recommend you to flash fenrir on both lk slots from the bootloader directly after flashing LineageOS.

**Q5: How do I update to another release of LineageOS ?**

Answer: Simply download the latest .zip package of LineageOS available [here](https://github.com/Nothing-2A/releases/releases) from your smartphone and then go to Settings -> System -> System Update -> Click on the three dots -> Local update and select the downloaded .zip package from here. It will run the update process automatically afterwards.

**Q6: I've followed the steps for updating LineageOS localy but the update disapeared from the list before I clicked on the reboot option from the Updater**

Answer: It's a known bug with LineageOS updater with local updates, simply follow again the steps to add the LineageOS .zip packages from your smartphone storage into the updater and the update will be available again from the Updater app.

**Q7: How long can I expect a new release of LineageOS ?**

Answer: Most likely the following month or a few weeks later if it's not an **HOTFIX** release, you won't have an exact date/time however since I do this out of my free time.

**Q8: I love your work ! Can I give you a donation ?**

Answer: Of course ! You can simply do your donation at my PayPal [here](https://paypal.me/eliasgheeraert).

### Copyrights
Your warranty is now voided and I am not responsible for any bricks or bootloop.

Any apropriation/stealing and/or unauthorized redistribition of my work on the Internet without my constent is stricly forbidden.
