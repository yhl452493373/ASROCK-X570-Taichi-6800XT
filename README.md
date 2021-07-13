# OpenCore EFI for ASRock x570 Taichi and AMD RX 6800XT hackintosh

---
since 2021/04/25,my video card change to RX6800XT,but this EFI should also working with other video card,such as Radeon VII,5700XT,RX 580

Change Log:

----
2021/07/13
+ remap usb port to make sleep working.(must restart from windows to macos)
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