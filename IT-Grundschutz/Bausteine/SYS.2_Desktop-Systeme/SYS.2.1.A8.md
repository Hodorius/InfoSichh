# SYS.2.1.A8 Absicherung des Bootvorgangs
* **Der Startvorgang des IT-Systems („Booten“) MUSS gegen Manipulation abgesichert werden.**<br>
Umsetzung: Um den Bootvorgang kryptographisch abzusichern, sollten bei Systemen mit UEFI-Firmware die Option SecureBoot aktiviert werden.<br>
[Dell Latitude 7490](https://github.com/Hodorius/InfoSichh/blob/main/Hardening/BIOS/Dell.md#secure-boot)

* Es MUSS festgelegt werden, von welchen Medien gebootet werden darf.

* Es SOLLTE entschieden werden, ob und wie der Bootvorgang kryptografisch geschützt werden soll.

* Es MUSS sichergestellt werden, dass nur Administrierende die Clients von einem anderen als den voreingestellten Laufwerken oder externen Speichermedien booten können.

* NUR Administrierende DÜRFEN von wechselbaren oder externen Speichermedien booten können.

* Die Konfigurationseinstellungen des Bootvorgangs DÜRFEN NUR durch Administrierende verändert werden können.

* Alle nicht benötigten Funktionen in der Firmware des Client-Systems MÜSSEN deaktiviert werden.
