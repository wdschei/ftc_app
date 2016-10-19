## Instructions referenced at:
* http://ftcforum.usfirst.org/showthread.php?6849-Having-trouble-updating-Moto-G3-s-to-Android-6-0&highlight=moto
## Instructions located at:
* https://drive.google.com/file/d/0B1dw7NAR9N9KZUlvZXhmZV9ac0E/view
## Referencing Debug mode from:
* https://developer.android.com/studio/run/device.html#developer-device-options
## Referencing Motorola Bootloader Unlock from:
* https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-a
## Using image from:
* https://drive.google.com/open?id=0B1dw7NAR9N9KNnkteEJVakh6dGM

```
sudo ~/Android/Sdk/platform-tools/adb reboot bootloader
sudo ~/Android/Sdk/platform-tools/fastboot oem get_unlock_data
--- Copy paste formatted Unlock String response into website and wait for the Unlock Key email ---
sudo ~/Android/Sdk/platform-tools/fastboot oem unlock <UNLOCK_KEY>
sudo ~/Android/Sdk/platform-tools/fastboot flash partition gpt.bin
sudo ~/Android/Sdk/platform-tools/fastboot flash bootloader bootloader.img
sudo ~/Android/Sdk/platform-tools/fastboot flash logo logo.bin
sudo ~/Android/Sdk/platform-tools/fastboot flash boot boot.img
sudo ~/Android/Sdk/platform-tools/fastboot flash recovery recovery.img
sudo ~/Android/Sdk/platform-tools/fastboot flash system system.img_sparsechunk.0
sudo ~/Android/Sdk/platform-tools/fastboot flash system system.img_sparsechunk.1
sudo ~/Android/Sdk/platform-tools/fastboot flash system system.img_sparsechunk.2
sudo ~/Android/Sdk/platform-tools/fastboot flash system system.img_sparsechunk.3
sudo ~/Android/Sdk/platform-tools/fastboot flash system system.img_sparsechunk.4
sudo ~/Android/Sdk/platform-tools/fastboot flash modem NON-HLOS.bin
sudo ~/Android/Sdk/platform-tools/fastboot erase modemst1
sudo ~/Android/Sdk/platform-tools/fastboot erase modemst2
sudo ~/Android/Sdk/platform-tools/fastboot flash fsg fsg.mbn
sudo ~/Android/Sdk/platform-tools/fastboot erase cache
sudo ~/Android/Sdk/platform-tools/fastboot erase userdata
sudo ~/Android/Sdk/platform-tools/fastboot reboot
```
