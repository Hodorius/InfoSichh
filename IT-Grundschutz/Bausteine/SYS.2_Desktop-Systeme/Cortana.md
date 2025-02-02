# Härtungsvorgaben für Cortana

## Maßnahmen nach CIS
### Cortana deaktivieren
**Profil:**</br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**</br>
Diese Richtlinie entscheidet, ob Cortana auf dem System erlaubt ist.</br>
Die empfohlende Einstellung ist: `Deaktiviert`

**Begründung:**</br>
Wenn Cortana aktiviert ist, kann die Suchhistory sensible Informationen enthalten. Diese Informationen werden dann 
an Microsoft gesendet.

**Auswirkung:**</br>
Cortana wird deaktiviert. Benutzer werden weiterhin in der Lage sein Daten auf dem System, sowie im Internet über die 
Suchfunktion zu finden.

**Umsetzung:**</br>
`gpedit.msc > Computerkonfiguration > Administrative Vorlagen > Windows-Komponenten > Suche > Cortana zulassen > Deaktiviert`

**Audit:**
`regedit > HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search : AllowCortana (REG_DWORD) 0`

**Standardeinstellung:**
Aktiviert. (Cortana ist auf dem System erlaubt.)

**Kreuzreferenz:**
*TODO: Verlinkungen zu BSI-Anforderungen*</br>
Deinstallierung oder Deaktivierung nicht benötigter Software.</br>

