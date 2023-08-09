# EFI-X99-JINGSHA-E8I-H87-INTEL-XEON-E5-2650-V3-RX-6600M-8GB

![Untitled-1](https://github.com/carlospelegrin/EFI-X99-JINGSHA-E8I-H87-INTEL-XEON-E5-2650-V3-RX-6600M-8GB/assets/88504218/3f032df1-f6cc-4785-9226-80ab01d8abd7)

![Screenshot 2023-06-24 at 01 24 19](https://github.com/carlospelegrin/EFI-X99-JINGSHA-E8I-H87-INTEL-XEON-E5-2650-V3-RX-6600M-8GB/assets/88504218/8fe09c69-a72e-4241-9783-4f084dfaa9ba)

|Item|Description|
|-|:-------:|
|Plataform|Desktop|
|Motherboard|JINGSHA X99-E8I|
|CPU|Intel Xeon E5-2650 v3, 2.30GHz (10C/20T)|
|Memory|32 GB DDR4 - 4x8GB|
|Storage|SSD Goldenfir 1TB - SATA 3|
|GPU|AMD Radeon RX6600M 8GB 51RISC|
|Ethernet|Realtek GBe Family (RTL8111)|
|Audio|Realtek ALC892|
|SMBIOS|MacPro7,1|
|OS|Sonoma 14.0 beta 4 update (Atualmente)|
|Opencore|0.9.3 (Atualmente)|

Comando para atualizar via terminal seu **`Hackintosh`**.

```
sudo softwareupdate -i -a -R
```

# BIOS Settings/Configurações de BIOS

### Disable/Desativar

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set `DisableIoMapper` to YES)
- Compatibility Support Module (CSM).
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)
  - This must be off, if you can't find the option then **`ENABLE`** `AppleXcpmCfgLock`. 
  - Your hack will not boot with CFG-Lock enabled.
  - For 10.10 and older, you'll need to **`ENABLE`** `AppleCpuPmCfgLock` as well.

### Enable/Ativar

- VT-x
- Above 4G decoding. 
  - This must be on, if you can't find the option then add `npci=0x2000` to `boot-args`. 
  - Do not have both this option and `npci` on `boot-args` enabled at the same time.
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10/11 UEFI Mode
- SATA Mode: AHCI

## Essential Information/Informações Essenciais

ATENÇÃO ANTES DE USAR ESSA EFI

1 - Recomendo usar o GenSMBIOS para gerar a SMBIOS que gostaria de usar. Ela já vai como `MacPro7,1`.

2 - Não vai com a kext **`USBMap.ketx`**. Já vai com o `ACPI` do `SSDT-USB-Reset.aml`. Faça o seu próprio mapeamento das portas `USB`.

3 - Após isso é so desfrutar do seu **`Hackintosh`**.

# References/Referências

https://github.com/luchina-gabriel/BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E
<br>
https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html
<br>
https://dortania.github.io/Getting-Started-With-ACPI/