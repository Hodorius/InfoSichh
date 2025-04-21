# Härtungsvorgaben für Kennwortrichtlinien
## Maßnahmen nach CIS
### 1. Komplexitätsvoraussetzungen
**Profil:**<br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**<br>
Mit dieser Sicherheitseinstellung wird festgelegt, dass Kennwörter die Komplexitätsvoraussetzungen erfüllen müssen.

Wenn diese Richtlinie aktiviert ist, müssen Kennwörter die folgenden Mindestvoraussetzungen erfüllen:
* Das Kennwort darf nicht den Kontonamen des Benutzers oder mehr als zwei Zeichen enthalten, die nacheinander im vollständigen Namen des Benutzer vorkommen.
* Das Kennwort muss mindestens sechs Zeichen lang sein.
* Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten:
  * Großbuchstaben (A bis Z)
  * Kleinbuchstaben (a bis z)
  * Zahlen zur Basis 10 (0 bis 9)
  * Nicht alphabetische Zeichen (zum Beispiel !, $, #, %)

Die Komplexitätsvoraussetzungen werden erzwungen, wenn Kennwörter geändert oder erstellt werden.

Die empfohlende Einstellung ist: ```Aktiviert```

**Begründung:**<br>
Kennwörter, die nur alphabetische Zeichen enthalten sind extrem einfach zu cracken, selbst mit öffentlich verfügbaren Tools.

**Auswirkung:**</br>
Es könnte zu Anrufen beim Helpdesk kommen, da die meisten Nutzer bislang nicht mit nicht-alphabetischen Zeichen vertraut sind.
Trotzdem sollte es jedem möglich sein mit nur wenig Aufwand die Komplexitätsvoraussetzungen zu erfüllen.

Sollten in der Institution noch strengere Kennwortrichtlinien entwickelt werden, dann gibt es die Möglichkeit ein eigenen
Passwortfilter (Passfilt.dll) zu erstellen. Es sei aber nochmals erwähnt, dass immer strengere Richtlinien zwangläufig zu frustrierteren
Nutzern und somit zu Mehrarbeit beim Helpdesk führen.

**Umsetzung:**</br>
```gpedit.msc > Computerkonfiguration > Windows-Einstellungen > Sicherheitseinstellungen > Kontorichtlinien > Kennwortrichtlinien > Kennwort muss Komplexitätsvoraussetzungen entsprechen : Aktiviert```

**Audit:**</br>
Laut CIS kein Registry-Eintrag vorhanden.<br>
Audit über den Pfad im Gruppenrichtlinien Editor.

**Standardeinstellung:**</br>
Auf Systemen in einer Domain: ```Aktiviert```<br>
Auf Standalone-Systemen: ```Deaktiviert```

**Kreuzreferenz:**</br>



### 2. Kennwortchronik erzwingen
**Profil:**<br>
Diese Maßnahme sollte bei jedem System vorgenommen werden.

**Beschreibung:**<br>
Mit dieser Sicherheitseinstellung wird die Anzahl von eindeutigen neuen Kennwörtern ermittelt, die mit einem Konto verknüpft werden müssen,
bevor ein altes Kennwort wieder verwendet werden kann. Der Wert muss zwischen 0 und 24 Kennwörtern liegen.

Mit dieser Richtlinie können Administratoren die Sicherheit erhöhen, indem sichergestellt wird, dass alte Kennwörter nicht
ständig wieder verwendet werden.

Die empfohlende Einstellung ist: ```24 gespeicherte Kennwörter```

**Begründung:**<br>
Je länger ein Nutzer das gleiche Passwort nutzt, desto größer wird die Wahrscheinlichkeit, dass sein Passwort durch Brute-Force-Attacken geknackt wird.
Ist ein Passwort geknackt, ist der Account so lange komprommitiert, bis das Passwort geändert wird. Selbst wenn die Sicherheitsrichtlinie die Nutzer
dazu auffordert, ihre Passwörter nach einer gewissen Zeit zu wechseln, sinkt trotzdem die Sicherheit, wenn Nutzer ständig die selben Passwörter nutzten.

Selbst wenn eine kleine Zahl in dieser Richtlinie eingetragen ist, zeigt die Praxis, dass Nutzer auch nur einen kleinen Pool an Passwörtern
erstellen, die sie nacheinander durchrotieren.

**Auswirkung:**</br>
Die Haupt-Auswirkung ist, dass Nutzer jedes mal ein komplett neues Passwort erstellen müssen, wenn sie dazu vom System aufgefordert werden.
Dies führt allerdings auch dazu, dass Nutzer anfangen ihre Passwörter irgendwo aufzuschreiben, damit sie diese nicht vergessen. 

Ein weiteres Risiko besteht auch darin, dass die Passwörter Inkremente enthalten (z.B. passwort01, passwort02, etc.). Dadurch fällt es den 
Nutzern leichter ihr Passwort zu merken und jedes mal ein neues zu erstellen, halt nur mit der Änderung des Inkrements. Das führt aber auch dazu,
dass das Passwort wieder leichter zu knacken ist.

In Kombination mit einem kurzen Passwortalter, führt diese Richtlinie dazu, dass Nutzer ihr Passworter öfters vergessen und dadurch auch
öfters beim Helpdesk anrufen, um ein Passwortreset anzufordern.

**Umsetzung:**</br>
```gpedit.msc > Computerkonfiguration > Windows-Einstellungen > Sicherheitseinstellungen > Kontorichtlinien > Kennwortrichtlinien > Kennwortchronik erzwingen : 24```

**Audit:**</br>
Laut CIS kein Registry-Eintrag vorhanden.<br>
Audit über den Pfad im Gruppenrichtlinien Editor.

**Standardeinstellung:**</br>
Bei Systemen in einer Domain: ```24```<br>
Bei Standalone-Systemen: ```0```

**Kreuzreferenz:**</br>



### X. TODO
**Profil:**<br>
**Beschreibung:**<br>
**Begründung:**<br>
**Auswirkung:**</br>
**Umsetzung:**</br>
**Audit:**</br>
**Standardeinstellung:**</br>
**Kreuzreferenz:**</br>
