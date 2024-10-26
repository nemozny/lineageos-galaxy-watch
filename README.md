# lineageos-galaxy-watch
Galaxy Watch on LineageOS with Samsung Galaxy S10

If you try and install Galaxy Wear app from the App store, it will exit, because it can identify running LineageOS. From what I have read, this OS check is more lenient on non-Samsung phones.
The goal is to install one Magisk module that will enable you to run Galaxy Wear on your Samsung S10 with LineageOS.

&nbsp;
## Prerequisite
You are running the latest LineageOS on your phone. For me it is one day old LineageOS build. I am updating LineageOS weekly with OTA.
You have your PC that you used for LineageOS installation, with all the drivers and ADB working. If not, then follow the official guide.
You did NOT install Samsung Wear yet.

&nbsp;
## Magisk
(Following [this Youtube guide](https://www.youtube.com/watch?v=8o5YILpoIvs))

- Download the latest [Magisk](https://github.com/topjohnwu/Magisk/releases/) apk to your PC. Do not install Magisk to your phone!
- Reboot your phone to Recovery - hold your power button and select "Reboot" - "Recovery". Then in Recovery select "Apply update" - "Apply from ADB".
- On your PC navigate to folder, where have you downloaded the Magisk apk.

- `adb sideload Magisk.apk` or whatever is your apk file name.
- "Signature verification failed. Install anyway?" 
Yes.
- Reboot.
- You have now the Magisk installed to your phone. Running the app should finish the installation (as you can see on the video), however in my case the app just somehow flashed and closed. Nothing happened.
- If your Magisk crashed like mine, download the Magisk apk again to your phone and run the apk as you would normally install any application. However since it installed some root files during the earlier Recovery step, it will now just finish the installation properly.
- I was following a different guide and enabled Zygisk in Magisk settings and rebooted my phone. But I don't think you actually need to do this step.

&nbsp;
## Magisk module
- Now download [GoogleSpoofForWear.zip from xdaforums](https://xdaforums.com/t/magisk-module-use-galaxy-wearable-app-with-any-custom-rom.4459715/) to your phone and load it in Magisk - Modules.
- Reboot.

&nbsp;
## Samsung Wear
Now install Samsung Wear and start setting up your Samsung Watch.
However the process in my case always crashed.
- Pairing
- Confirm code on your phone and watch
- Agree to Samsung terms + send diagnostic data + automatic updates
- Now the app always crashed and the process restarted infinitely.

&nbsp;
## Fix Galaxy Watch5 Manager permissions
I was suspicious of permissions, so I granted everything to "Galaxy Wearable" and "Galaxy Watch5 Manager". I did not help.

However during the Wear crash, I noticed there was a "missing permissions" notification. I tapped it and it opened a different Android dialog saying "This setting can't be changed unless you allow restricted settings" for Watch5 Manager.

You need to go to Android settings - Apps - Galaxy Watch5 Manager, don't go to Permissions! Tap three dots in the top right corner and select "Allow restricted permissions". Then you can allow notifications.

&nbsp;
## Done
Now you can finish the pairing and setup.

Good job!

&nbsp;
## References
https://www.youtube.com/watch?v=8o5YILpoIvs

https://xdaforums.com/t/magisk-module-use-galaxy-wearable-app-with-any-custom-rom.4459715/

&nbsp;
## Credits
to /u/lfikhl for giving me info about the Magisk module.

[victoriam8a](https://xdaforums.com/m/victoriam8a.12171217/) for the Google Spoof for Wear module,

and of course the [Magisk crowd](https://github.com/topjohnwu/Magisk).

You too, Samsung.
