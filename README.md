# EFI-X99-JINGSHA-E8I-H87-INTEL-XEON-E5-2650-V3-RX-6600M-8GB

![MacPro7,1](https://user-images.githubusercontent.com/88504218/208508130-8ce3643c-963d-4869-af7f-6371935fb658.png)

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
|OS|Ventura 13.1|
|Opencore|0.8.7|


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

## Informções Essenciais

ATENÇÃO ANTES DE USAR ESSA EFI

1 - Recomendo usar uma EFI diferente para fazer a instalação do OS.

2 - Por alguma razão desconhecida, a EFI não prossegue com a instalação.

3 - Após a instalação, a utilização da EFI ocorre perfeitamente, sem nenhum erro, até o presente momento.

## Alterações Futuras/Future Changes

- [] Fazer dar boot pela mesma EFI de pós-instalação.
- []
- []
- []
# References/Referências

https://github.com/luchina-gabriel/BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E
<br>
https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/haswell-e.html
<br>
https://dortania.github.io/Getting-Started-With-ACPI/