[GUIDE] Installing macOS Monterey (12.x) / Ventura (13.x) on Gigabyte H610M-H DDR4 [OpenCore 0.8.8]

OPENCORE bootloader for installation on 12-gn processors (Alder Lake)
EFI for Gigabyte H610M-H DDR4 motherboard.

![ventura-installed](https://user-images.githubusercontent.com/27772093/216773817-aed78de2-2998-4cbf-b847-24e050b7865b.png)


Add extra kexts

    IntelMausi for Intel Ethernet
    RealtekRTL8111 for Realtek 8111
    AppleALC for universial patch audio
    WhateverGreen for enable GPU AMD
    Lilu for patches
    USBports for init and mapping USB 2.0/3.0
    VirtualSMC

Custom ACPI (optional)

    SSDT-AWAC-DISABLE.aml
    SSDT-EC-USBX.aml
    SSDT-PLUG-ALT.aml

Disabled:

    Fast Boot
    VT-d (enable if DisableMapper Quirks set True)
    CFG Lock
    Secure Boot
    Parallel Port
    Serial Port
    Resizable BAR Support

Enabled:

    VT-x
    UEFI startup mode
    Above 4G decoding
    Hyper-Threading
    Execute Disable Bit
    EHCI/XHCI Hand-off
    OS type: Windows 10 UEFI Mode
    PCI-e x16 switched to Gen3.0 (If Videocard connect to PCI-e x16 Riser)

OC - boot-args:

    keepsyms=1 debug=0x100 agdpmod=pikera -wegnoigpu alcid=66 -v
