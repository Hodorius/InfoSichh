# Editor für lokale Gruppenrichtlinien unter Windows 10 Home aktivieren
Unter Windows 10 Home ist der Gruppenrichtlinien-Editor standardmäßig nicht installiert.
Probiert man den Befehl "gpedit.msc" unter WIN+R auszuführen, erscheint folgende Fehlermeldung:

![image](https://github.com/user-attachments/assets/e34b5ed7-b7c0-45d6-afb9-00efedbec381)

## gpedit nachinstallieren
Man erstellt eine .bat Datei mit folgendem Inhalt:
```bat
@echo off
pushd "%~dp0"
dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt
dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt
for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"
pause
```
Anschließend die Bat-Datei als Administrator ausführen. Daraufhin wird der Gruppenrichtlinien-Editor nachinstalliert und kann wie gewohnt ausgeführt werden.

![image](https://github.com/user-attachments/assets/905150f5-89fe-465c-a250-5ba1a2e17657)

