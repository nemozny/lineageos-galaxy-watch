# lineageos-galaxy-watch
Enable Galaxy Watch on LineageOS with Samsung Galaxy S10

If you attempt to install the Galaxy Wear app from the App Store, it will likely exit due to LineageOS detection. This OS check appears to be more lenient on non-Samsung phones. The goal is to install a Magisk/Lygisk module to pass this OS check.

Github repo [lineageos-galaxy-watch](https://github.com/nemozny/lineageos-galaxy-watch) for any issues or comments.

&nbsp;

## Prerequisites
1. Ensure you are running the latest LineageOS on your phone. In this example, it is a one-day-old build, updated weekly via OTA.
2. LineageOS version 21-20241025-nightly-beyondlte
3. Have your PC ready with all required drivers and ADB set up, used initially for the LineageOS installation. Follow the official guide if not already set.
4. Do NOT install Samsung Wear app yet.

&nbsp;
## Lygisk Installation

[Lygisk repo](https://github.com/programminghoch10/Lygisk)

_**Do not install Magisk, it will NOT survive the first OTA update.**_

&nbsp;

Follow the official [Lygisk Installation guide](https://github.com/programminghoch10/Lygisk?tab=readme-ov-file#installation):

1. **Download Lygisk:**  
    - Download the latest APK to your PC. Do not install it on your phone.
  
2. **Rename the APK to ZIP**
   - Change the file extension from APK to ZIP.

2. **Reboot to Recovery:**  
    - Hold the power button on your phone, select "Reboot," then "Recovery."
    - In the Recovery mode, select "Apply update" followed by "Apply from ADB."

3. **Install Magisk via ADB:**  
    - On your PC, navigate to the folder where you downloaded the Magisk installation file.
    - Use the command:
      ```shell
      adb sideload app-release.zip
      ```
      (Replace `app-release.zip` with the actual filename if different).

4. **Handle Signature Verification:**  
    - When prompted with "Signature verification failed. Install anyway?" select Yes.

5. **Reboot:**  
    - Restart your phone. Open the Lygisk app to complete the installation.
  
6. **App Requires Additional Setup**
   - Hit OK
   - "Direct install", let's go!
   - another reboot

&nbsp;

## Install Lygisk Module

1. **Download Module:**  
    - Obtain the [GoogleSpoofForWear.zip](https://xdaforums.com/t/magisk-module-use-galaxy-wearable-app-with-any-custom-rom.4459715/) module from the XDA forums to your phone.

2. **Load Module in Lygisk:**  
    - Open the Lygisk app, go to Modules, and load the downloaded ZIP file.
    - Reboot your phone.

&nbsp;
## Install Samsung Wear

1. **Download and Install:**  
    - Install the Samsung Wear app and start the setup for your Samsung Watch.

2. **Pairing Process:**  
    - Perform the following steps:
        - Pair your Watch with the phone.
        - Confirm the code on both devices.
        - Agree to Samsung terms, including sending diagnostic data and enabling automatic updates.

3. **Application Crash:**  
    - If the app crashes (repeatedly):
        - Follow with the next step **Fix Galaxy Watch5 Manager Permissions**.

&nbsp;
## Fix Galaxy Watch5 Manager permissions
I was suspicious of permissions, so I granted everything to "Galaxy Wearable" and "Galaxy Watch5 Manager". I did not help with the crash.

However during the Wear crash, I noticed there was a "missing permissions" notification. I tapped it and it opened a different Android dialog saying "This setting can't be changed unless you allow restricted settings" for Watch5 Manager.

2. **Adjust Settings:**  
    - Go to Android settings: 
      ```
      Settings > Apps > Galaxy Watch5 Manager
      ```
    - Do not open "Permissions"!
    - Tap the three dots in the top right corner and select "Allow restricted settings."
    - Allow notifications.
  
&nbsp;

## Final Steps

**Complete Setup:**  
- Finish pairing and setup without crashes.

Good job!

&nbsp;

## References

- YouTube Guide: https://www.youtube.com/watch?v=8o5YILpoIvs
- XDA Forums Magisk Module: https://xdaforums.com/t/magisk-module-use-galaxy-wearable-app-with-any-custom-rom.4459715/

&nbsp;

## Credits

- Reddit u/lfikhl for information on Magisk module and Lygisk.
- [victoriam8a](https://xdaforums.com/m/victoriam8a.12171217/) for the GoogleSpoofforWear module.
- The [Magisk community](https://github.com/topjohnwu/Magisk).
- The [Lygisk community](https://github.com/programminghoch10/Lygisk)

Special thanks to Samsung.
