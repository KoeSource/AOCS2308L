# Supermicro AOC-S2308L-L8i

Firmware - IT & IR

Version:

- Date: 2016
- Firmware: 20.00.07.00
- OPROM: 7.39.02.00

Inhalt:

- '/efi'     = UEFI boot shell
- '/IR'      = IR Firmware (Raid)
- '/IT'      = IT Firmware (HBA)
- '/scripts' = Diverse scripts, auslesen der Temperatur, write test
- Achtung: SMC2308T/R.bat sind nicht getestet!

# UEFI USB Boot Stick erstellen

- Rufus FreeDOS boot stick erstellen
- den Ordner "uefiFlash" auf den Datenträger kopieren
- IR=Raid, IT=HBA

Beispiel:  
E:\uefiFlash\2308T207.ROM  
E:\uefiFlash\mptsas2.rom  
E:\uefiFlash\sas2flash.efi  
E:\uefiFlash\SMC2308T.NSH  
E:\uefiFlash\x64sas2.rom  
E:\efi\boot\bootx64.efi  
E:\efi\boot\bootia32.efi  

- Per UEFI auf dem Datenträger booten
- "fs0:" eingeben, mit "dir" kontrollieren ob man auf dem richtigen Datenträger ist.
- uefiFlash: "runIT.NSH", "runIR.NSH" eingeben -> instruktionen befolgen.
- dosFlash: "runIT.bat", "runIR.bat" eingeben -> instruktionen befolgen.

# Temperatur auslesen des HBAs

cd scripts/  
chmod +x ./backup_temp.bash  
./backup_temp.bash  

# HBA Testen, daten schreiben mit dd

Achtung: dd löscht alle Daten!  

cd scripts/  
chmod +x ./test.bash  
./test.bash  

# Linux Commands

```
unzip Test.zip
zip -r Supermicro_AOC_S2308L_P20.zip ./*        -> -r ZWINGEND!!!
sha256sum Supermicro_AOC_S2308L_P20.zip
sha256sum Supermicro_AOC_S2308L_P20.zip | tr '[:lower:]' '[:upper:]' > sha256sum.txt
```
