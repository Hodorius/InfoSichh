# SYS.2.2.3 Clients unter Windows
## 1. Beschreibung
### 1.1 Einleitung
Mit Windows 10 hat Microsoft sein Client-Betriebssystem Windows an eine neue Unternehmensstrategie angepasst. Verändert hat sich insbesondere auch die grundlegende Philosophie, weg vom bisherigen Prinzip des „lokalen Betriebssystems“ hin zu einer Dienstleistung („Windows as a Service“). Das bedeutet, dass das Betriebssystem
neben den bisherigen Funktionen auch darüber hinausgehende, insbesondere cloudbasierte, Anwendungen enthält und deswegen auf eine enge Anbindung an die Server-Infrastruktur von Microsoft angewiesen ist. Wichtige
neue Aspekte im Vergleich zu den bisherigen Windows-Versionen sind vor allem der tief verankerte und teilweise
nicht beeinflussbare Datenaustausch zwischen den Clients und der Herstellerinfrastruktur sowie die zunehmende
Auslagerung von sicherheitskritischen Kernbestandteilen einer Windows-Infrastruktur (z. B. Authentisierung) in die
Cloud.

Mit Windows 11 wurde im Oktober 2021 eine Nachfolgeversion veröffentlicht. Diese enthält neue Funktionen, hat
eine überarbeitete Bedienoberfläche und im Vergleich zu Windows 10 deutlich erhöhte Systemvoraussetzungen.
Insbesondere setzt Windows 11 offiziell eine 64-Bit-fähige CPU, UEFI SecureBoot sowie ein TPM 2.0 voraus. Windows 11 ist trotz des Versionssprungs jedoch keine komplette Neuentwicklung, sondern basiert auf Windows 10.
Dieser Baustein ist daher sowohl für Windows 10 als auch für Windows 11 anwendbar.

### 1.2 Zielsetzung
Ziel dieses Bausteins ist der Schutz von Informationen, die durch und auf Windows-Clients mit Windows 10 oder 11 verarbeitet werden.

### 1.3 Abgrenzung und Modellierung
Der Baustein SYS.2.2.3 Clients unter Windows ist für alle Clients anzuwenden, auf denen das Betriebssystem Microsoft Windows 10 oder 11 eingesetzt wird.

Dieser Baustein enthält spezifische Anforderungen, die zum sicheren Betrieb von Clients unter dem Betriebssystem
Windows zusätzlich zu den Anforderungen aus dem Baustein SYS.2.1 Allgemeiner Client zu beachten und zu erfüllen sind. Für Anwendungsprogramme, die auf den Windows-Clients verwendet werden, sind die Anforderungen
der entsprechenden Bausteine zu erfüllen, beispielsweise APP.1.1 Office-Produkte oder APP.1.2 Webbrowser. Beim
Einsatz in einer Windows-Domäne sind die Anforderungen der entsprechenden Bausteine wie APP.2.2 Active Directory Domain Services zu erfüllen.
