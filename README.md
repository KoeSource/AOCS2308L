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

SHA256-*.zip: 76ECFC1F363C8D363D2C215FAD8E63FAB6BCD10ECD216E659AFA554FA74FCF2F

# UEFI USB Boot Stick erstellen

- FAT32 Formatieren
- den Ordner "efi" auf den Datenträger kopieren
- Firmware ins Hauptverzeichnis des USB-Sticks kopieren

Beispiel:  
E:\2308T207.ROM  
E:\mptsas2.rom  
E:\sas2flash.efi  
E:\SMC2308T.NSH  
E:\x64sas2.rom  
E:\efi\boot\BOOTX64.efi  

- Per UEFI auf dem Datenträger booten
- "fs0:" eingeben, mit "dir" kontrollieren ob man auf dem richtigen Datenträger ist.
- "SMC2308T.NSH" eingeben -> instruktionen befolgen.