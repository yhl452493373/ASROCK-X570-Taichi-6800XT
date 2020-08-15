# OpenCore ASROCK-X570-Taichi---Radeon-VII

----

opencore efi for asrock x570 taichi hackintosh

you need to add your own platform data.the product is iMacPro1,1

base on opencore 0.6.1 dev

support MacOS 10.15.5 and 10.15.6 and 11 (big sur)

----
+ asrock x570 taichi
+ amd ryzen7 3700x
+ ddr4 32G x 4
+ amd radeon vii (HIS with Sapphire bios)
+ sata 1t ssd + asgard 2t nvme ssd
+ bcm943602cdp wifi & bt

----
+ sleep not work

----
bios only to do is close csm

do not enable above 4g decoding

bios version <= 3.0

----

first,clean nvram by opencore.

now do not set csr-active-config.please delete it,and then boot into recovery.

for 10.15, use csrutil disable to close sip;

for big sur,also need csrutil authenticated-root disable . 

after that ,reboot into recovery and execute mount -uw /Volumes/BigSur\ Volume to make big sur system partition writeable.

use diskutil list to find which disk is big sur(not big sur data),it look like 

APFS Volume ⁨macOS Big Sur⁩           15.5 GB    disk4s5

remember disk4s5

follow this command step:

diskutil apfs listSnapshots disk4s5

diskutil apfs deletesnapshop  disk4s5 -name snapshotname

you may need many times of diskutil apfs deletesnapshop  disk4s5 -name snapshotname util there is no snapshot

when all snapshot delete,you can restart.

for more information,please visit http://bbs.pcbeta.com/viewthread-1863022-1-1.html

----

thanks for https://github.com/dangthaison91/Ryzen-Hackintosh
