# Virtuelle Maschine aufsetzen
> VMWare Workstation Pro 17 über Broadcom-Webseite

> VMWare für macOS freischalten: https://github.com/DrDonk/unlocker

> Maschine mit macOS aufsetzten: https://www.wisecleaner.com/think-tank/413-How-to-Install-a-macOS-in-VMware-Workstation-PRO-17.html

# Hardening-macOS

## 3.1. Basis-Anforderungen

### SYS.2.4.A2 Nutzung der integrierten Sicherheitsfunktionen von macOS
Die in macOS integrierten Schutzmechanismen „System Integrity Protection“ (SIP), „Xprotect“ und
„Gatekeeper“ MÜSSEN aktiviert sein.

> [Umsetzung SIP](/SIP.md)

> [Umsetzung Gatekeeper](/Gatekeeper.md)

> [Umsetzung Xprotect](/Xprotect)

Gatekeeper DARF NUR die Ausführung signierter Programme
erlauben, sofern unsignierte Programme nicht zwingend notwendig sind.
