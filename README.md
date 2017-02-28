KernelConfig-ThinkPadX260
==========================
My Linux Kernel configuration for a Lenovo ThinkPad X260

## Minimal but I still need:
* btrfs
* luks
* systemd
* qemu
* docker
* The gcc  optimisations [patch](https://github.com/graysky2/kernel_gcc_patch) for Intel Skylake
* Gentoo [experimental patches](https://wiki.gentoo.org/wiki/Project:Kernel/Experimental)
* The dm-crypt [options](https://wiki.gentoo.org/wiki/Dm-crypt)

## My 'lspci -nnk':
```
00:00.0 Host bridge [0600]: Intel Corporation Sky Lake Host Bridge/DRAM Registers [8086:1904] (rev 08)
        Subsystem: Lenovo Sky Lake Host Bridge/DRAM Registers [17aa:504a]
00:02.0 VGA compatible controller [0300]: Intel Corporation Sky Lake Integrated Graphics [8086:1916] (rev 07)
        Subsystem: Lenovo Sky Lake Integrated Graphics [17aa:504a]
        Kernel driver in use: i915
        Kernel modules: i915
00:14.0 USB controller [0c03]: Intel Corporation Device [8086:9d2f] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
        Kernel driver in use: xhci_hcd
        Kernel modules: xhci_pci
00:14.2 Signal processing controller [1180]: Intel Corporation Device [8086:9d31] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
00:16.0 Communication controller [0780]: Intel Corporation Device [8086:9d3a] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
00:16.3 Serial controller [0700]: Intel Corporation Device [8086:9d3d] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
        Kernel driver in use: serial
00:17.0 SATA controller [0106]: Intel Corporation Device [8086:9d03] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
        Kernel driver in use: ahci
        Kernel modules: ahci
00:1c.0 PCI bridge [0604]: Intel Corporation Device [8086:9d10] (rev f1)
        Kernel driver in use: pcieport
00:1c.2 PCI bridge [0604]: Intel Corporation Device [8086:9d12] (rev f1)
        Kernel driver in use: pcieport
00:1f.0 ISA bridge [0601]: Intel Corporation Device [8086:9d48] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
00:1f.2 Memory controller [0580]: Intel Corporation Device [8086:9d21] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
00:1f.3 Audio device [0403]: Intel Corporation Device [8086:9d70] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
        Kernel driver in use: snd_hda_intel
        Kernel modules: snd_hda_intel
00:1f.4 SMBus [0c05]: Intel Corporation Device [8086:9d23] (rev 21)
        Subsystem: Lenovo Device [17aa:504a]
        Kernel driver in use: i801_smbus
        Kernel modules: i2c_i801
00:1f.6 Ethernet controller [0200]: Intel Corporation Ethernet Connection I219-LM [8086:156f] (rev 21)
        Subsystem: Lenovo Ethernet Connection I219-LM [17aa:2233]
        Kernel driver in use: e1000e
        Kernel modules: e1000e
02:00.0 Unassigned class [ff00]: Realtek Semiconductor Co., Ltd. Device [10ec:522a] (rev 01)
        Subsystem: Lenovo Device [17aa:504a]
04:00.0 Network controller [0280]: Intel Corporation Wireless 8260 [8086:24f3] (rev 3a)
        Subsystem: Intel Corporation Wireless 8260 [8086:0130]
        Kernel driver in use: iwlwifi
        Kernel modules: iwlwifi
```

## The 'lsusb'
```
Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 001 Device 005: ID 138a:0017 Validity Sensors, Inc. Fingerprint Reader
Bus 001 Device 004: ID 04ca:7058 Lite-On Technology Corp. 
Bus 001 Device 003: ID 8087:0a2b Intel Corp. 
Bus 001 Device 002: ID 058f:9540 Alcor Micro Corp. AU9540 Smartcard Reader
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```

## Links
Links form inspirations:
* Gentoo Pappy's Kernel Seeds: https://forums.gentoo.org/viewtopic-t-887894.html
* KernelHub: http://www.kernelhub.org/
* Gentoo Kernel Seeds: https://wiki.gentoo.org/wiki/Kernel/Configuration/Kernel_Seeds
* Funtoo Kernel Seeds: http://www.funtoo.org/Talk:Kernel_Seeds
