# OpenCore EFI for ASRock x570 Taichi and AMD RX 6800XT hackintosh

### Since 2021/04/25,my video card change to RX6800XT,but this EFI should also working with other video card,such as Radeon VII,5700XT,RX 580

#### Since 2021/07/27,AMD_Vanilla changed patch method.You need to find the three algrey - Force cpuid_cores_per_package patches and alter the Replace value only.

#### Changing B8000000 0000/BA000000 0000/BA000000 0090 to B8 <CoreCount> 0000 0000/BA <CoreCount> 0000 0000/BA <CoreCount> 0000 0090 substituting <CoreCount> with the hexideciamal value matching your physical core count. 

### See the table below for the values matching your CPU Core Count.

| CoreCount | Hexidecimal|
|--------|---------|
|   6 Core  | `06` |
|   8 Core  | `08` |
|   12 Core | `0C` |
|   16 Core | `10` |
|   32 Core | `20` |

If you are 4 cores or 2 cores,you can try to use `04` or `02`

#### Note: MacOS Monterey installation requires Misc -> Security -> SecureBootModel to be disabled in the config.Also TPM nneds to be disabled in the BIOS. Both can be enabled after install.

#### Note: If you can't update macos from System Upgrade,you can try to upgrade system like new install.(when you reinstall macos,if you did not format system disk,the data will be remainded).you can download new InstallAssistant.pkg by gibMacOS.you can install the InstallAssistant.pkg and then you will get an Install macOS Big Sur application in your application folder.

----

Change Log:

----

2021/07/27
+ change platforminfo to MacPro7,1...
+ change kernel patch method.Please visit https://github.com/AMD-OSX/AMD_Vanilla to get help
----

2021/07/14
+ change platforminfo to iMacPro1,1.because it's easier to get a correct System Serial Number.
----

2021/07/13
+ remap usb port to make sleep working.
----

2021/07/07
+ update kexts to newest
+ update oc to 0.7.1
----

2021/06/29
+ update kexts to newest
+ update oc to 0.7.0
----

2021/05/06
+ update kexts to newest
+ update oc to 0.6.9

2021/04/25
+ In order to drive RX 6800XT, change platform from iMacPro1,1 to MacPro7,1
+ Disable WhatEverGreen( if you need it,you can enable it by yourself.)
----

You need to add your own platform data.The product is MacPro7,1

+ base on OpenCore 0.7.0 release
+ support macOS 10.15.7 and 11 ( if you are use 6800,6800XT or 6900XT,you need macOS 11.4 + )

----
+ asrock x570 taichi
+ amd ryzen 7 3700x
+ ddr4 32G x 4
+ amd RX 6800 XT
+ sata 1t ssd + asgard 2t nvme ssd
+ bcm943602cdp wifi & bt

----
+ virtual machines not working
+ sleep is partly working.(must restart from windows to macos)
+ the internal Intel AX200 Bluetooth is blocked,because if it is not shielded,other Bluetooth devices will not work properly.

----
BIOS setup:
+ Disable csm
+ Enable Above 4g Decoding
+ Disable ResizeBAR

## DO NOT UPGRADE BIOS to 4.30 or above,otherwise, the shutdown won't work.

## IF YOU DID NOT USE RX5000 OR RX 6000 SERIES GPU,PLEASE REMOVE BOOT ARGUMENTS agdpmod=pikera