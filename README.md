# thinkpad10-linux-config

Thinkpad 10 is nearly works out-of-the-box with Manjaro Linux(18.0.2 Kernel 4.19.14-1).

## What is works
- Bluetooth
- Acpi (Battery charge level,charging status)
- Touch screen
- Pen input
- Sleep

## what is not
- WiFi (Can be fixed with nvram copy)
- Sound

## Other
- random freeze.Can be fixed by adding <code>intel_idle.max_cstate=0</code> to <code>GRUB_CMDLINE_LINUX_DEFAULT</code>

## How to fix WiFi
- copy nvram to /lib/firmware/brcm/   
<code>cat /sys/firmware/efi/efivars/nvram-74b00bd9-805a-4d61-b51f-43268123d113 > /lib/firmware/brcm/brcmfmac43241b5-sdio.txt</code>
- run modprobe   
<code>modprobe -r brcmfmac ; modprobe brcmfmac</code>
