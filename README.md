# OpenCore EFI for ASRock x570 Taichi and AMD RX 6800XT hackintosh

---
since 2021/04/25,my video card change to RX6800XT,but this EFI should also working with other video card,such as Radeon VII,5700XT,RX 580

Change Log:

2021/05/06
+ update kexts to newest
+ update oc to 0.6.9

2021/04/25
+ In order to drive RX 6800XT, change platform from iMacPro1,1 to MacPro7,1
+ Disable WhatEverGreen( if you need it,you can enable it by yourself.)
----

You need to add your own platform data.The product is MacPro7,1

+ base on OpenCore 0.6.8 release
+ support macOS 10.15.7 and 11 ( if you are use 6800,6800XT or 6900XT,you need macOS 11.4 Beta+ )

----
+ asrock x570 taichi
+ amd ryzen 7 3700x
+ ddr4 32G x 4
+ amd RX 6800 XT
+ sata 1t ssd + asgard 2t nvme ssd
+ bcm943602cdp wifi & bt

----
+ sleep not working
+ virtual machines not working

----
BIOS setup:
+ Disable csm
+ Enable Above 4g Decoding
+ Disable ResizeBAR
