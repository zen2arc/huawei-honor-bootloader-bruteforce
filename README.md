# Huawei & Honor OEM Unlock bruteforce Linux certified :D (HAS TO BE INSTALLED INTO AN EXISTING PLATFORM TOOLS FOLDER)

## Summary

After closing the official EMUI website,
which allowed you to retrieve the code to unlock the bootloader of Huawei/Honor phones, 
here is a python script to test many possible codes.

It uses a bruteforce method, based on the IMEI identifier to generate unlocking codes.

This will most likely only work on European versions, 
because these only use numbers in the bootloader unlock code.

Currently is in testing on the device (Russian region)
- Honor 7A DUA-L22

## Instructions

1. Enable developer options in Android.
1. Enable USB debugging in Android.
1. Connect your device to the computer and launch the script.


    Linux:
    ```shell
    $ python3 unlock.py
    ```
    The device is going to ask for authorisation, which you'll have to allow.  
    Please also check the checkbox "Always allow from this computer".
1. Wait for the application to detect your device. The device info should appear.
1. Enter the (first) IMEI.
1. Start the bruteforce.  
    (this may take several ~~hours~~ days) so get a cup of coffee ☕ and go to sleep. 💫 
1. If the correct code is found, your phone will either be instantly unlocked or prompt you with an additional confirmation dialogue on the target device.  
    (all data will be erased on unlock!)


## FAQ & Troubleshooting

**- The application doesn't work. Is there anything I should have installed?**  
Yes, it was developed in python so it needs it to run, version 3. You can install the latest version from [here](https://www.python.org/downloads/) or by using Windows Store.

**- My phone reboots every 5 failed attempts**  
We are aware of this and have implemented an automatic intentional reboot after 4 attempts.  
You can manually enable this feature in the code.  
The script will also automatically detect this behaviour. For this to work reliably, please check the checkbox "Always allow from this computer" in the adb dialogue.

**- The script displays "command invalid"**  
Huawei has removed the unlock command in EMUI 10.  
Downgrade your software and try again.
