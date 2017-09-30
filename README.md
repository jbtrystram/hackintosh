# hackintosh
Required files to boot OSX sierra 10.12.5 from a NVME drive.
See the branch usb\_install\_sierra to boot the USB installer.

Files on this repo are the only necessary files to be copied into the EFI partition after a multibeast install. 

## Hardware
* Intel Core i7 6700K
* MSI Z170a Tomahawk
* Gskill 2x8Go DDR4
* Samsung 960 Evo 256Go (NVMe SSD)
* Crucial M500 128Go SSD (used for install)
* MSI GTX 1080 Sea Hawk

## Working
- Audio 
- HiDPI scaling (retina)
- Sleep / Deep sleep
- Boot on NVMe SSD
- Network


## Not Working
nothing found so far

### Notes

presence of HackrNVMeFamily-10_12_5.kext in the kexts folder requires to delete IONVMeFamilly.kext in the original OSX kext folders. (easy way is to install OSX on a regular SSD and deal with NVME after install)

You should use a spoof class code and *NOT* remove IONVMeFamily.kext to avoid your OS to be killed by a sierra update. See [tonymacx86 guide] and [tonymacx86 thread](https://www.tonymacx86.com/threads/10-12-6-auto-updated-before-i-could-update-my-hackrnvmefamily-kext.229150/page-3#post-1591133)


## Credits / resources 
- Initial guide for el capitan : [tonymacx86](https://www.tonymacx86.com/threads/guide-skylake-el-capitan-msi-z170a-tomahawk-i5-6600k-gtx-970.187255/)
- patch audio : [tonymac guide](https://www.tonymacx86.com/threads/audio-realtek-alc-applehda-guide.143757/#post886744) see **Unsupported/Non-working Realtek ALC AppleHDA** I applied method 3 : ssdt injection then audio_cloverALC script.
- get the NVME SSD working : [RehabMan Patch](https://github.com/RehabMan/patch-nvme) then [clone install into NVME](https://www.tonymacx86.com/threads/nvme-on-a-hackintosh.173230/page-5#post-1457549)
- Boot without nv_disable=1 : [OsxAptioFixDrv](https://nickwoodhams.com/x99-hackintosh-osxaptiofixdrv-allocaterelocblock-error-update/)
- USB limit patch. (if you have lot of USB devices / hubs that are not recognized) [plist patch - tonymacx86](https://www.tonymacx86.com/threads/usb-new-raise-port-limit-patch-for-macos-10-12-sierra.202329/)


