# PANASONIC Let's Note CF-SV7 (CF-SV7RDAVS) BIOS
## ※ INTEL-SA-00289 (Plundervolt) PATCHED ※

System information:
BIOS revision: V300L23
CPU: Intel(R) Core(TM) i5-8350U
Memory: 8GB

BIOS backup of Panasonic Let's Note CF-SV7RDAVS. My system uses the **WINBOND-W25Q128JV**. The dump was made using a CH341a flash programmer.  

This is for reference and backup purposes only. You can use it to repair a corrupted BIOS for the same model of notebook.

Caution about BIOS modding:
The Let's Note SV7 after the Plundervolt patch **cannot be undervolted**. The 0x634 (Overclocking Lock) NVRAM value is already set to 0x0 (disabled), a PXE driver within the firmware instead writes the bit `20` to the MSR `0x194`. Removing this is **impossible**. The Let's Note CF-SV7 uses Intel Boot Guard, so patching out the "write bit 20 to 0x194" code and programming it onto the WINBOND chip makes the system refuse to turn on at all— this is Intel Boot Guard working as intended.  
