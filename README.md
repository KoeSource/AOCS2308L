# Supermicro AOC-S2308L-L8i

Firmware - IT & IR

Version:

- Date: 2016
- Firmware: 20.00.07.00
- OPROM: 7.39.02.00

Inhalt:

- sas2flash UEFI / DOS
  - Achtung: SMC2308T/R.bat sind nicht getestet!
- mptsas2.rom
- x64sas2.rom
- firmware.rom

# UEFI USB Boot Stick erstellen

- Rufus FreeDOS boot stick erstellen
- den Ordner "efi" auf den Datenträger kopieren
- Firmware ins Hauptverzeichnis des USB-Sticks kopieren

Beispiel:  
E:\2308T207.ROM  
E:\mptsas2.rom  
E:\sas2flash.efi  
E:\SMC2308T.NSH  
E:\x64sas2.rom  
E:\efi\boot\bootx64.efi  
E:\efi\boot\bootia32.efi  

- Per UEFI auf dem Datenträger booten
- "fs0:" eingeben, mit "dir" kontrollieren ob man auf dem richtigen Datenträger ist.
- UEFI: "runIT.NSH", "runIR.NSH" eingeben -> instruktionen befolgen.
- BIOS: "runIT.bat", "runIR.bat" eingeben -> instruktionen befolgen.

# Linux Commands

```
unzip Test.zip
zip -r Supermicro_AOC_S2308L_P20.zip ./*        -> -r ZWINGEND!!!
sha256sum Supermicro_AOC_S2308L_P20.zip
sha256sum Supermicro_AOC_S2308L_P20.zip | tr '[:lower:]' '[:upper:]' > sha256sum.txt
```
