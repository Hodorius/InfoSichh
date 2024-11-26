# Gatekeeper

## Umsetzungshinweise BSI
Zusätzlich enthält macOS mit dem sogenannten "Gatekeeper" eine Funktion, welche die Ausführung von
Anwendungen kontrolliert. Standardmäßig erlaubt Gatekeeper nur die Ausführung von Programmen, die
entweder über den App Store bezogen oder von Apple signiert wurden (das Programm stammt von einem
Entwickler, der von Apple verifiziert wurde). Die Funktion Gatekeeper muss in dieser Standardkonfiguration
betrieben werden, solange unsignierte Programme nicht absolut nötig sind.

## Umsetzungshinweise NIST
### 3.2 Gatekeeper
Gatekeeper was a new feature in OS X 10.8 that essentially enforces high-level application
whitelisting for installing applications. Already-installed applications are unaffected by
Gatekeeper settings. There are two configuration options for Gatekeeper: to allow only
applications from the App Store and to allow only applications from the App Store and
“identified developers.”[^1] These settings can be overridden by right-clicking a restricted
application in Finder, selecting “Open” and then providing administrator-level credentials, if
requested. These actions only need to be performed once for each application.

[^1]: Apple provides what it calls a “safe downloads list”, which identifies the developers whose applications can be downloaded through this Gatekeeper option.

### 6.5.1 Software Restriction for Gatekeeper
It is recommended to configure Gatekeeper to “App Store” for all systems. Gatekeeper’s
configuration options are not marked as pertaining to Gatekeeper, but rather are all bundled into
the System Preferences / Security & Privacy / General. This pane has two options related to
“Allow applications downloaded from”, as described in Section 3.1. By default, the option to
limit downloads to “App Store and identified developers” is enabled. To use the strictest
Gatekeeper controls, select the “App Store” option. These options are shown in Figure 9 below.

The commands to enable Gatekeeper are:

`spctl --master-enable`

`spctl --enable`
