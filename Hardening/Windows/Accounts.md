# Windows Accounts
Mit Accounts sind die Benutzer unter lusrmgr.msc gemeint. Folgende Benutzer sind nach einer Systeminstallation vorhanden:

<img width="573" alt="Screenshot 2025-03-30 213846" src="https://github.com/user-attachments/assets/d70459a2-f339-421b-bacf-641d340d9cf9" />

Der kleine Pfeil neben dem Männchen zeigt an, dass das Benutzerkonto deaktiviert ist (Rechtsklick > Eigenschaften > Allgemein > Konto ist deaktiviert).

## Administrator


## DefaultAccount


## defaultuser0
Wenn Windows installiert wird erscheint das Out-Of-Box Experience (OOBE) Setup. Also das Setup indem man nach Land, Sprache, Tastaturlayout, etc. gefragt wird.
Während dieses Setups erstellt Windows im Hintergrund einen Benutzer defaultuser0. Er wird am Ende des OOBE durch eine Routine wieder gelöscht.
Wird das Setup nicht ordnungsgemäß durchlaufen, wird die Löschroutine nie erreicht und der defaultuser0 bleibt bestehen. Das passiert z.B. wenn man einen OOBE-Bypass durchgeführt hat,
da man Windows ohne initiale Internetverbindung aufsetzten will.<br>
Da der defaultuser0 nur Konfigurationscharakter aufweißt, kann und sollte dieser im lusmrgr.msc gelöscht werden.

## Gast


## Mustermann


## WDAGUtilityAccount
