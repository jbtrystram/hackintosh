# hackintosh
Required files for my Hackintosh to run High Sierra
Files on this repo are the only necessary files to be copied into the EFI partition after a multibeast install.  

## Hardware
* Intel Core i7 6700K
* MSI Z170a Tomahawk
* Gskill 2x8Go DDR4
* Samsung 960 Evo 256Go (NVMe SSD)
* Crucial M500 128Go SSD (used for install)
* MSI GTX 1080 Sea Hawk

## Working
- Audio and audio after sleep
- HiDPI scaling (retina)
- Sleep / Deep sleep
- Boot on NVMe SSD
- Network


## Not Working
headphone jack detection after sleep

### Notes
if upgrading from Sierra remove all HackrNVMeFamily kexts.
Update Clover (v4220 is working fine)

## Credits / resources 

- make clover look good : [display 4k](https://www.tonymacx86.com/threads/clover-uefi-boot-with-4k-and-200-scaling.224313/) and [theme](https://github.com/al3xtjames/clover-theme-minimal)
- high sierra update : [tonymacx86](https://www.tonymacx86.com/threads/update-directly-to-macos-high-sierra.232707/)

- Initial guide for el capitan : [tonymacx86](https://www.tonymacx86.com/threads/guide-skylake-el-capitan-msi-z170a-tomahawk-i5-6600k-gtx-970.187255/)
- patch audio : [tonymac guide](https://www.tonymacx86.com/threads/audio-realtek-alc-applehda-guide.143757/#post886744) see **Unsupported/Non-working Realtek ALC AppleHDA** I applied method 3 : ssdt injection then audio_cloverALC script.
- get the NVME SSD working : [RehabMan Patch](https://github.com/RehabMan/patch-nvme) then [clone install into NVME](https://www.tonymacx86.com/threads/nvme-on-a-hackintosh.173230/page-5#post-1457549)
- Boot without nv_disable=1 : [OsxAptioFixDrv](https://nickwoodhams.com/x99-hackintosh-osxaptiofixdrv-allocaterelocblock-error-update/)
- USB limit patch. (if you have lot of USB devices / hubs that are not recognized) [plist patch - tonymacx86](https://www.tonymacx86.com/threads/usb-new-raise-port-limit-patch-for-macos-10-12-sierra.202329/)
- EAPD Codec Fix (no audio after sleep) : [RehabMan's Codec Commander](https://www.tonymacx86.com/threads/no-audio-after-sleep-wake-realtek-alc-applehda-fixes.151504/)
