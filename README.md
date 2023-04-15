## Recovery Device Tree for the Samsung Galaxy A32 4G (MTK)

## How-to compile it:

```sh
. build/envsetup.sh
lunch ofox_a32-eng
make recoveryimage
```

Blobs version:
> Kernel base: A325FXXU2BVD6

> Ramdisk, DTB, DTBO base: A325FXXU2BVD6

Kernel source:
> https://github.com/captaincookie200/android_kernel_samsung_a32-recovery

Current Workaround for fixing settings ressetting after reboot.

> edit bootable/recovery/twrp.cc and at line 396 (as of now) Change the bool to true. This makes the recovery load the themes twice. THis should only be for decrypted devices but since it has fixed our issue we'll use this workaround until a proper solution has been found.
