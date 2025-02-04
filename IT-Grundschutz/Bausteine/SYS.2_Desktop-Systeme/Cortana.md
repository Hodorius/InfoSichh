# Härtungsvorgaben für Cortana

## Maßnahmen nach CIS
### 1. Cortana deaktivieren
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

**Audit:**</br>
`regedit > HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search : AllowCortana (REG_DWORD) 0`

**Standardeinstellung:**</br>
Aktiviert. (Cortana ist auf dem System erlaubt.)

**Kreuzreferenz:**</br>
*TODO: Verlinkungen zu BSI-Anforderungen*</br>
SYS.2.1.A42.a) Nur zwingend notwendige Online-Funktionen.</br>
SYS.2.1.A42.c) Restriktive Konfiguration bzw. Deaktivierung OS-Funktionen.</br></br></br>

### 2. Cortana auf Sperrbildschirm deaktivieren
**Profil:**</br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**</br>
Die Richtlinieneinstellung bestimmt, ob der Benutzer mittels Sprache mit Cortana interagieren kann, während das System gesperrt ist.</br>
Die empfohlende Einstellung ist: `Deaktiviert`

**Begründung:**</br>
Es darf nicht möglich sein auf Ressourcen zu zugreifen, wenn das System gesperrt ist.

**Auswirkung:**</br>
Keine, da Cortana in Härtungsmaßnahme 1 deaktiviert wurde. Ansonsten muss erst das System entsperrt werden, damit Cortana genutzt werden kann.

**Umsetzung:**</br>
`gpedit.msc > Computerkonfiguration > Administrative Vorlagen > Windows-Komponenten > Suche > Cortana auf Sperrbildschirm zulassen > Deaktiviert`

**Audit:**</br>
`regedit > HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search : AllowCortanaAboveLock (REG_DWORD) 0`

**Standardeinstellung:**</br>
Aktiviert. (Nutzer kann durch Sprache mit Cortana interagieren, während das System gesperrt ist.)

**Kreuzreferenz:**</br>
*ToDo*
</br></br></br>



### 3. Suche und Cortana die Nutzung des Standorts verbieten
**Profil:**</br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**</br>
Diese Richtlinieneinstellung gibt an, ob von der Suche und Cortana standortabhängige Such- und Cortana-Ergebnisse bereitgestellt werden können.

**Begründung:**</br>
In einer unternehmensverwalteten Umgebung ist es obsolet der Suche und Cortana die Nutzung von Standortdaten zu erlauben. Organisationen möchten normalerweise nicht, dass diese Informationen nach Außen dringen.

**Auswirkung:**</br>
Vernachlässigbar. Suche und Cortana liefert keine standortbezogenen Ergebnisse.</br>
Ist doch mal ein spezifischer Bedarf genauerer Suchergebnisse da, kann der Nutzer trotzdem durch z.B. einen Ortzusatz bei der Suche die Ergebnisse beeinflussen.

**Umsetzung:**</br>
`gpedit.msc > Computerkonfiguration > Administrative Vorlagen > Windows-Komponenten > Suche > Der Suche und Cortana die Nutzung von Positionsdaten erlauben > Deaktiviert`

**Audit:**</br>
`regedit > HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search : AllowSearchToUseLocation (REG_DWORD) 0`

**Standardeinstellung:**</br>
Aktiviert. (Suche und Cortana haben Zugriff auf Positionsdaten.)

**Kreuzreferenz:**</br>
*ToDo*
</br></br></br>
