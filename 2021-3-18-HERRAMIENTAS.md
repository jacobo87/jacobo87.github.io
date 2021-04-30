![Sosmatic](../images/wall.jpg)
> 2021 

## Herramientas para Windows
**Links**: 
- [Malwarebytes](https://www.malwarebytes.com/mwb-download/thankyou/)
- [Superantispyware](https://www.superantispyware.com/downloadfile.html?productid=SUPERANTISPYWAREFRE*E)
- [Eset Scan](http://download.eset.com/special/eos/ESETOnlineScanner_ESL.exe)
- [Windows Slimmer](https://www.auslogics.com/es/software/windows-slimmer/)

Desinstalador:
- [Geek Uninstaller](https://www.geekuninstaller.com/geek.zip)

HHD / SSD:
- [CrystalDisk info](https://crystalmark.info/en/software/crystaldiskinfo/)

Hardware:
- [HWmonitor](https://download.cpuid.com/hwmonitor/hwmonitor_1.43.zip)

Reparación **Windows Update**:
- [Tweaking](https://www.tweaking.com/files/setups/tweaking.com_windows_repair_aio_setup.exe)

### Liberador de espacio en disco
```bash
cleanmgr
```
### Restablecer TCP/IP
```bash
netsh winsock reset
```
```bash
netsh int ip reset
```
**Limpiar cache DNS**
```bash
ipconfig /flushdns
```
### Updates Windows
```c
DISM.exe /Online /Cleanup-image /Restorehealth
```
---
```c
DISM.exe /Online /Cleanup-Image /RestoreHealth /Source:C:\RepairSource\Windows /LimitAccess
```
---
DISM crea un archivo de registro (%windir%/Logs/CBS/CBS.log) que captura cualquier problema que la herramienta encontró o corrigió. %windir% es la carpeta en la que está instalado Windows. Por ejemplo, la carpeta %windir% es C:\Windows.

### Habilitar Windows Defender
En ```regedit```:
```
HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows 
```
Borrar el valor DisableAntiSpyware. 
- Aplica a WinXp, Win Vista, Win7, Win8.x a Win10.

## Herramientas para Mac
**Links** de interés:
- [Optimizar Mac](https://store.bananacomputer.com/blog/mac/7-formas-de-optimizar-tu-mac/84.html)

## Puesta a punto Windows/MAC
Instalación y actualización de programas:
- [Ninite](https://ninite.com/)
