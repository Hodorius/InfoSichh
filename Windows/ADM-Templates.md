# Gruppenrichtlinien Administrative Vorlagen in Windows
Begriffsdefinitionen:<br>
GPO = Group Policy Object (deutsch: Gruppenrichtlinien-Objekt)<br>
ADM = Administrative Template (deutsch: Administrative Vorlage)<br>
ADMX = Administrative Template in XML Format<br>
ADML = Administrative Template Language (Dies sind die Beschreibungen in den jeweiligen Sprachen im Active Directory Editor)

Alle Administrativen Vorlagen sind unter ```C:\Windows\PolicyDefinitions``` zu finden.<br>
Hat man die ADMX-/ADML-Dateien von einer anderen Quelle als Microsoft geupdated, sind diese unter 
```C:\Program Files (x86)\Microsoft Group Policy\<version-specific>\PolicyDefinitions``` zu finden!

Empfehlung: Vierteiliges Tutorial über Microsoft Gruppenrichtlinien.<br>
https://www.infrastrukturhelden.de/microsoft-infrastruktur/active-directory/gruppenrichtlinen/microsoft-gruppenrichtlinien-ein-umfassender-ueberblick-teil-1/

Microsoft Learn: https://learn.microsoft.com/en-us/troubleshoot/windows-client/group-policy/create-and-manage-central-store

## ADMX- und ADML-Dateien
Das Folgende bezieht sich auf die **Konfiguration von Standalone Systemen**.

Bevor Gruppenrichtlinien über gpedit.msc richtig konfiguriert werden können, müssen die aktuellen ADMX- und ADML-Dateien eingespielt werden.
Diese werden direkt von Microsoft für die jeweilige Windowsversion bereitgestellt.

Zunächst also erstmal nachschauen welche Windows Version installiert ist:<br>
``` Einstellungen > System > Info > Windows-Spezifikationen > Edition & Version ```
![image](https://github.com/user-attachments/assets/a2b27092-cec4-4ad5-823f-6a22ab473b8d)

Auf der Microsoft-Webseite unter Suchen nach "ADMX Windows 11 23H2" suchen:
<img width="490" alt="image" src="https://github.com/user-attachments/assets/355be102-2b77-45e8-b42b-eebdc504c974" />
![image](https://github.com/user-attachments/assets/a3795e37-b256-48da-8f30-94c6dcd5b826)

Alternativ sind die jeweiligen Links zu den aktuellen ADMX-Versionen in dem Microsoft Learn Artikel (siehe oben) zu finden.
