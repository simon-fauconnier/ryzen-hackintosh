# ryzen-hackintosh (opencore)
Hackintosh powered by amd ryzen 3900x and Aorus x570 pro (ATX), Opencore 0.6.4

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

macOS Catalina v10.15.6

EFI configured with the vanilla-opencore tutorial : https://dortania.github.io/OpenCore-Install-Guide/

The information in config.plist/platormInfo/Generic has been deleted. Please generate new ones with GenSMBIOS (https://github.com/corpnewt/GenSMBIOS), with the SMBIOS *MacPro7.1*

ACPI/SSDT-EC_USBX built manually following the "Getting started with ACPI" tutorial : https://dortania.github.io/Getting-Started-With-ACPI/

## BIOS settings

Now works with the latest motherboard BIOS versions (tested with versions F30, F31q).

Access the bios by pressing the F2 key on computer startup.

Boot/Fast Boot -> Disabled

Boot/CSM Support -> Disabled

Boot/Secure Boot/Secure Boot -> Disabled

Settings/IO Ports/Above 4G Decoding -> Enabled

Settings/IO Ports/USB Configuration/XHCI Hand-off -> Enabled

## Kext

* [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) (v1.5.5)
* [IntelMausi.kext](https://github.com/acidanthera/IntelMausi/releases) (v1.0.4)
* [Lilu.kext](https://github.com/acidanthera/Lilu/releases) (v1.5.0)
* [MacProMemoryNotificationDisabler.kext](https://github.com/IOIIIO/MacProMemoryNotificationDisabler/releases) (v1.1)
* [SmallTreeIntel82576.kext](https://github.com/khronokernel/SmallTree-I211-AT-patch/releases) (v1.3.0)
* [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) (v1.1.9)
* [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) (v1.4.5)
* [NVMeFix.kext](https://github.com/acidanthera/NVMeFix/releases) (v1.0.4)

CPU Management:

* [AMDRyzenCPUPowerManagement.kext](https://github.com/trulyspinach/SMCAMDProcessor/releases) (v0.6.4)
* [SMCAMDProcessor.kext](https://github.com/trulyspinach/SMCAMDProcessor/releases) (v0.6.4)

## What works?

* Very stable
* Audio (Audio codec : ALC1220-VB)
* iMessage
* HandOff, continuity
* AirDrop
* Time Machine
* USB (2.0 and 3.0)

* If the characters are displayed strangely on the screen, uncheck the option *Allow extended dynamic range* in system settings / monitor.

## What's not working yet?

* Sleep :(

## USB Mapping

I did a custom USB mapping for the "Aorus x570 Pro (ATX)" motherboard, all ports are mapped except USB-C. 
This kext must be used with MacPro7.1 smbios.

## Usefull tools

* **AMD Power Gadget:** (https://github.com/trulyspinach/SMCAMDProcessor) -> Monitoring CPU
* **Liquidctl:** (https://github.com/jonasmalacofilho/liquidctl/releases) -> Fan settings (light and speed)
* **MonitorControl:** (https://github.com/MonitorControl/MonitorControl) -> Monitor brightness and contrast control
* **ProperTree:** (https://github.com/corpnewt/ProperTree) -> .plist reader

## Fix Adobe products crashes

https://gist.github.com/naveenkrdy/26760ac5135deed6d0bb8902f6ceb6bd
