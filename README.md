# mountr
Script to mount iso images to PC(Mountr/Drivedroid functionality) on Android 9 and 10

Strung from moto g7(ocean) and moto g8(sofiap) init files. 

I named it after "mountr" since I found the first working variables I needed by studying it.

Examples to find correct values such as usbdevice drivers and serial ids, also where to write the corresponding links/files in the /config and /sys directories.

su

strings /init.* |grep lun

strings /vendor/etc/init/hw/* |grep lun

strings /vendor/etc/init/hw/* |grep cdimage

strings /system/etc/init/*

su

getprop | grep usbcontroller


This script may need to be modified for your device. Simple concept, sometimes difficult to determine correct usb config. Your linking an iso and device identifiers to the corresponding files somewhere in /config or /sys (likely). I have been using Mountr and DriveDroid for this up until Android 9/10. This same approach also worked on SAMSUNG/HTC/LG devices I have had. "usbcontroller" variable is often different per device/ROM.

Script as givin is working in Android Q on moto g8(sofiap)
