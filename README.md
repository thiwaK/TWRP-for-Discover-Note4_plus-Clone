# TWRP-for-Discover-Note4_plus-Clone
---

**DISCLAIMER**
`I AM NOT RESPONSIBLE VOIDING YOUR WARRANTY OR ANY DAMAGE CAUSED TO YOUR DEVICE`

This is a port of TWRP 3.7.0 to Discover Note4 plus Clone only.

Firmware for this particular device could not be found on the internet (maybe bad luck). So I extracted the firmware by using SP Flash Tool and build the partition images, preloader, and scatter file from scratch. Here I attached some necessary files, assuming you may require them in the flashing or restoring process. 

## Device Info
- Manufacturer: Discover
- Model: Note4_plus
- Platform: mt6582
- ABI : armeabi-v7a (32-bit)
- Resolution: 1280x800 (hdpi)
- RAM : 2GB(fake) / 1GB(actual)
- Android Version : 8.0(fake) / 4.4(actual)
- Internal Storage : 64GB(fake) / 16GB(actual)
 
## File/Folder Description
- `port_recovery`: Unpacked port recovery.
- ~~`stock_recovery`: Unpacked stock recovery.~~ Removed.

<details>
<summary>Additional files</summary>

- `MT6582_Android_scatter.txt`: Device memory structure file.
- `preloader_bird82_cwet_a_kk.bin`: Device partition index file.
- `boot_magisk.img`: Magisk patched stock boot.img
- `stock_recovery.img`: Extracted stock recovery image(ALPS.KK1.MP1.V2.10).
- ~~`twrp-3.7.0_9-0-tilapia.img`: Pre-build TWRP image. Use for porting.~~ Removed.

</details>


## Instructions

- The ported custom recovery image can be found in the [releases](https://github.com/thiwaK/TWRP-for-Discover-Note4_plus-Clone/releases).

- Use SP Flash Tool (fastboot is not allowed to flash almost all partitions) to flash recovery.

- Install necessary MTK drivers (preloader, adb, usb). You may need to disable signature verification if you are using higher Windows versions.

- To flash, power off and disconnect the device from pc. Then hold the volume up and connect the device to pc by USB. The device will automatically boot into preloader mode. Start flashing immediately while holding the volume up. You can release the key after the process starts to progress.

- Use any MTK image unpacking/repacking tool if you want to customize. [Android_ROM_Tool_v2.0.3.zip](https://download2268.mediafire.com/h6kjg21odziglCYkoeFkibhrztjT4pZvd_MsYMt7pZbWlKjpjRmlYfEt9a75C5H8ejdKK0c2jQnVbVPNNUka3KVzyYK5wzcuR04kfEjknPQany-12115CzdDbSOS19A_V2H_J2Yi9zAMgxYHH6EPJeuIoObXWAxrBdIqhwsNKGc6ytY/vgqe6w7sfxqd8ur/Android_ROM_Tool_v2.0.3.zip) recommed.



## Changes
- remove unwanted files (fstab.x, ueventd.x.rc)
- fstab edited
- default.prop edited
- recovery.fstab edited