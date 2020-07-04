# ryzen-hackintosh (opencore)
Hackintosh powered by amd ryzen 3900x and Aorus x570 pro (ATX), Opencore 0.5.9

## The Build

* **CPU:** Amd ryzen 3900x
* **CPU Cooler:** NZXT Kraken x63
* **Motherboard:** x570 Aorus Pro (ATX)
* **Memory:** Corsair Vengeance RGB Pro 2x8 GB DDR4-3200
* **Storage (macOS):** Sabrent Rocket PCIe M.2 2280 SSD 1TB
* **Storage (Windows):** Sabrent Rocket PCIe M.2 2280 SSD 1TB + Crusial MX500 1TB SSD
* **Video Card:** Sapphire Radeon RX 5700 XT Nitro+ SE
* **Power Supply:** SeaSonic GX-1000
* **Wifi-bluetooth card:** Fenvi FV-T919 (native support)
* **Case:** NZXT H510 Elite
* **Monitor:** BenQ EX3501R (21/9)

## Information

macOS Catalina v15.15.5

EFI configured with the vanilla-opencore tutorial : https://dortania.github.io/OpenCore-Desktop-Guide/

The information in config.plist/platormInfo/Generic has been deleted. Please generate new ones with GenSMBIOS (https://github.com/corpnewt/GenSMBIOS), with the SMBIOS *MacPro7.1*

ACPI/SSDT-EC_USBX built manually following the "Getting started with ACPI" tutorial : https://dortania.github.io/Getting-Started-With-ACPI/

## BIOS settings

Access the bios by pressing the F2 key on computer startup.

Boot/Fast Boot -> Disabled

Boot/CSM Support -> Disabled

Boot/Secure Boot/Secure Boot -> Disabled

Settings/IO Ports/Above 4G Decoding -> Enabled

Settings/IO Ports/USB Configuration/XHCI Hand-off -> Enabled

## Kext

* [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) (v1.5.0)
* [IntelMausi.kext](https://github.com/acidanthera/IntelMausi/releases) (v1.0.3)
* [Lilu.kext](https://github.com/acidanthera/Lilu/releases) (v1.4.5)
* [MacProMemoryNotificationDisabler.kext](https://github.com/IOIIIO/MacProMemoryNotificationDisabler/releases) (v1.0.0)
* [SmallTreeIntel82576.kext](https://github.com/khronokernel/SmallTree-I211-AT-patch/releases) (v1.0)
* [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) (v1.1.4)
* [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) (v1.4.0)

CPU Management:

* [AMDRyzenCPUPowerManagement.kext](https://github.com/trulyspinach/SMCAMDProcessor/releases) (v0.6.4)
* [SMCAMDProcessor.kext](https://github.com/trulyspinach/SMCAMDProcessor/releases) (v0.6.4)

## What works?

* Very stable
* Audio (Audio codec : ALC1220-VB)
* iMessage

* If the characters are displayed strangely on the screen, uncheck the option *Allow extended dynamic range* in system settings / monitor.

## What's not working yet?

* Sleep (kernel panic) -> Possible solution: add a custom SSDT USB mapping in /ACPI

## Usefull tools

* **AMD Power Gadget:** (https://github.com/trulyspinach/SMCAMDProcessor) -> Monitoring CPU
* **Liquidctl:** (https://github.com/jonasmalacofilho/liquidctl/releases) -> Fan settings (light and speed)
* **MonitorControl:** (https://github.com/MonitorControl/MonitorControl) -> Monitor brightness and contrast control
* **iCue:** (https://www.corsair.com/us/en/icue-mac) -> Monitoring and ram settings (light)
