# Härtungsvorgaben für Cortana

## Maßnahmen nach CIS
### Cortana deaktivieren
**Profil:**</br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**</br>
Diese Richtlinieneinstellung gibt an, ob Cortana auf dem Gerät zugelassen ist.</br>
Die empfohlende Einstellung ist: `Deaktiviert`

**Begründung:**</br>
Wenn Cortana aktiviert ist, kann die Suchhistory sensible Informationen enthalten. Diese Informationen werden dann 
an Microsoft gesendet.

**Auswirkung:**</br>
Wenn Sie diese Einstellung aktivieren oder nicht konfigurieren, wird Cortana auf dem Gerät zugelassen. Wenn Sie die Einstellung deaktivieren, wird Cortana ausgeschaltet.</br>
Wenn Cortana ausgeschaltet ist, können Benutzer mithilfe der Suchfunktion trotzdem Informationen 
auf dem Gerät oder im Internet suchen.

**Umsetzung:**</br>
`gpedit.msc > Computerkonfiguration > Administrative Vorlagen > Windows-Komponenten > Suche > Cortana zulassen > Deaktiviert`

**Audit:**
`regedit > HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search : AllowCortana (REG_DWORD) 0`

**Standardeinstellung:**
Aktiviert. (Cortana ist auf dem System erlaubt.)

**Kreuzreferenz:**</br>
*TODO: Verlinkungen zu BSI-Anforderungen*</br>
SYS.2.1.A42.a) Nur zwingend notwendige Online-Funktionen.</br>
SYS.2.1.A42.c) Restriktive Konfiguration bzw. Deaktivierung OS-Funktionen.
