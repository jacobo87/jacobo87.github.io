---
layout: default
---
# COMANDOS Y HERRAMIENTAS
> 2021 

## Herramientas para Windows
**Links**: 
- [Malwarebytes](https://www.malwarebytes.com/mwb-download/thankyou/)
- [Superantispyware](https://www.superantispyware.com/downloadfile.html?productid=SUPERANTISPYWAREFRE*E)
- [Eset Scan](http://download.eset.com/special/eos/ESETOnlineScanner_ESL.exe)
- [Windows Slimmer](https://www.auslogics.com/es/software/windows-slimmer/)

Desinstalador:
- [Geek Uninstaller](https://www.geekuninstaller.com/geek.zip)
- [IObit Unlocker](https://iobit-unlocker.uptodown.com/windows)
> IObit Unlocker es una aplicación que nos permitirá eliminar aquellos archivos que por cualquier motivo se encuentran bloqueados en nuestro ordenador y que al intentar borrarlos recibimos un mensaje de error que nos comunica que es imposible. 

HHD / SSD:
- [CrystalDisk info](https://crystalmark.info/en/software/crystaldiskinfo/)

Hardware:
- [HWmonitor](https://download.cpuid.com/hwmonitor/hwmonitor_1.43.zip)
---  

### Liberador de espacio en disco
Borra archivos innecesarios del disco duro del equipo. Puede usar las opciones de línea de comandos para especificar que cleanmgr Limpie los archivos temporales, los archivos de Internet, los archivos descargados y los archivos de la papelera de reciclaje.
```c
cleanmgr
```
---

### Restablecer TCP/IP
```c
netsh winsock reset
```
```c
netsh int ip reset
```
---

### Limpiar cache DNS
```c
ipconfig /flushdns
```
---

### Limpiar ```WinsockFix```
Para hacerlo de **forma manual** vamos a hacer lo siguiente:

- En Windows XP:
Hacemos click en ```INICIO/EJECUTAR``` y escribimos ```cmd```.

En la consola escribimos 
```
netsh winsock reset catalog
``` 
y presionamos **ENTER**, luego escribimos 
```
netsh int ip reset resetlog.txt
``` 
y **ENTER** nuevamente, reiniciamos nuestro sistema y debería estar funcionando.

- Para Windows 7:
Hacemos click en ```INICIO``` y en el cuadro de búsqueda escribimos ```cmd```.
Hacemos click derecho sobre ```cmd.exe``` y seleccionamos **Ejecutar como Administrador**

Escribimos: 
```
netsh winsock reset catalog
``` 
y presionamos **ENTER**. Luego escribimos: 
```
netsh int ip reset resetlog.txt
``` 
y **ENTER** nuevamente, reiniciamos nuestro sistema.
---

### Updates Windows
**DISM** crea un archivo de registro (```%windir%/Logs/CBS/CBS.log```) que captura cualquier problema que la herramienta encontró o corrigió. ```%windir%``` es la carpeta en la que está instalado Windows. Por ejemplo, la carpeta ```%windir%``` es ```C:\Windows```.
```c
DISM.exe /Online /Cleanup-image /Restorehealth
```
```c
DISM.exe /Online /Cleanup-Image /RestoreHealth /Source:C:\RepairSource\Windows /LimitAccess
```
---
El comando ```sfc /scannow``` examinará todos los archivos de sistema protegidos y remplaza los archivos dañados con una copia en caché ubicada en una carpeta comprimida en ```%WinDir%\System32\dllcache```.
El marcador de posición ```%WinDir%``` representa la carpeta del sistema operativo Windows. Por ejemplo, ```C:\Windows```. (Fuente: [Microsoft](https://support.microsoft.com/es-es/topic/use-la-herramienta-comprobador-de-archivos-de-sistema-para-reparar-los-archivos-de-sistema-que-faltan-o-est%C3%A1n-da%C3%B1ados-79aa86cb-ca52-166a-92a3-966e85d4094e))
```c
sfc /scannow
```
O bien podemos usar la herramienta [Tweaking](https://www.tweaking.com/files/setups/tweaking.com_windows_repair_aio_setup.exe).
---

### Habilitar Windows Defender
En ```regedit```:
```
HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows 
```
Borrar el valor DisableAntiSpyware. 

- Aplica a WinXp, Win Vista, Win7, Win8.x y Win10.

---

### Matar un proceso usando ```Taskkill```
Matar un proceso usando Taskkill
> Nota: Algunos procesos se ejecutan como Administrador (elevado). Para matarlos, debe abrir una instancia de símbolo del sistema elevada. 

Abra el símbolo del sistema como el usuario actual o como Administrador.
Escriba tasklist para ver la lista de procesos en ejecución y sus PID. Como la lista puede ser muy larga, puede utilizar un carácter de tubería con el comando more.
```
tasklist | more
```
Lista de tareas de Windows 10
Para matar un proceso por su PID, escriba el comando
```
taskkill /F /PID pid_number
```
Para matar un proceso por su nombre, escriba el comando
```
taskkill /IM "nombre del proceso" /F
```
Por ejemplo, para matar un proceso por su PID
```
taskkill /F /PID 1242
```
Windows 10 ```Taskkill``` por ```Pid```
Para matar un proceso por su nombre:
```
taskkill /IM "notepad.exe" /F
```
> Nota: Para matar un proceso que se ejecuta de forma elevada, es necesario abrir PowerShell como Administrador. 

Abrir **PowerShell**. Si es necesario, ejecútelo como **Administrador**.
Escriba el comando ```Get-Process``` para ver la lista de procesos en ejecución.
Para matar un proceso por su nombre, ejecute el siguiente ```cmdlet```:
```
Stop-Process -Name "ProcessName" -Force
```
Para matar un proceso por su PID, ejecute el comando
```
Stop-Process -ID PID -Force
```

Ejemplos:
Este comando cerrará el proceso notepad.exe.
```
Stop-Process -Nombre "Notepad" -Force
```

Windows 10 Powershell Matar un Proceso
El siguiente comando cerrará un proceso con PID 2137.
```
Stop-Process -ID 2137 -Force
```
([Fuente: Winaero](https://winaero.com/kill-process-windows-10/))

---

## Herramientas para Mac
**Links** de interés:
- [Optimizar Mac](https://store.bananacomputer.com/blog/mac/7-formas-de-optimizar-tu-mac/84.html)

## Puesta a punto Windows/MAC
Instalación y actualización de programas:
- [Ninite](https://ninite.com/)

## REFERENCIAS
- [Microsoft docs](https://docs.microsoft.com/es-es/)
- [Cleanmgr](https://docs.microsoft.com/es-es/windows-server/administration/windows-commands/cleanmgr)

>  [&copy; Jacobo IT](http://jacoboazmani.org/)

[Inicio](./)
