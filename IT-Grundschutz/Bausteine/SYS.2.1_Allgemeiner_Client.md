# SYS.2.1 Allgemeiner Client

## 1. Beschreibung

### 1.1. Einleitung
Als „Allgemeiner Client“ wird ein IT-System mit einem beliebigen Betriebssystem bezeichnet, das die
Trennung von Benutzenden zulässt und nicht dazu dient, Server-Dienste bereitzustellen. Auf einem
Client sollten mindestens getrennte Umgebungen zur Administration und zur Benutzung eingerichtet
werden können. Das IT-System verfügt in der Regel über Laufwerke und Anschlussmöglichkeiten für
externe bzw. wechselbare Datenträger, weitere Schnittstellen für den Datenaustausch sowie andere
Peripheriegeräte. Typischerweise ist ein solches IT-System in ein Client-Server-Netz eingebunden. Bei
dem IT-System kann es sich beispielsweise um einen PC mit oder ohne Festplatte, um ein mobiles oder
stationäres Gerät, aber auch um eine Linux-Workstation oder einen Apple Mac handeln.

### 1.2. Zielsetzung
Ziel dieses Bausteins ist der Schutz von Informationen, die auf jeglicher Art von Clients, unabhängig
vom verwendeten Betriebssystem, erstellt, gelesen, bearbeitet, gespeichert oder versendet werden.

### 1.3. Abgrenzung und Modellierung
Der Baustein SYS.2.1 Allgemeiner Client ist für alle Clients unabhängig vom konkreten Betriebssystem
anzuwenden.

In der Regel werden Clients unter einem Betriebssystem ausgeführt, das jeweils eigene
Sicherheitsmaßnahmen erfordert. Für verbreitete Client-Betriebssysteme sind spezifische Bausteine in
der Schicht SYS.2 Desktop-Systeme vorhanden, die auf dem vorliegenden Baustein aufbauen und
zusätzlich anzuwenden sind. Falls für eingesetzte Clients kein spezifischer Baustein existiert, müssen
die Anforderungen des vorliegenden Bausteins geeignet für das Zielobjekt konkretisiert und es muss
eine ergänzende Risikobetrachtung durchgeführt werden.

Sicherheitsempfehlungen für mobile Endgeräte mit festem Betriebssystem, wie Smartphones oder
Tablets, sind in der Schicht SYS.3 Mobile Devices zu finden. Falls ein Client weitere Schnittstellen zum
Datenaustausch hat, wie z. B. USB, Bluetooth, LAN oder WLAN, müssen diese gemäß den
Sicherheitsvorgaben der Institution so abgesichert werden, wie es in den entsprechenden Bausteinen
beschrieben ist. Hierzu sind Anforderungen beispielsweise in SYS.4.5 Wechseldatenträger oder NET.2.2
WLAN-Nutzung zu finden.

Regelmäßig sind außerdem die Anforderungen der Bausteine OPS.1.1.3 Patch- und
Änderungsmanagement und CON.3 Datensicherungskonzept für Clients zu berücksichtigen. Clients sind
oft durch Schadsoftware gefährdet, daher sind die Anforderungen des Bausteins OPS.1.1.4 Schutz vor
Schadprogrammen bei Clients besonders relevant.

## 2. Gefährdungslage
Da IT-Grundschutz-Bausteine nicht auf individuelle Informationsverbünde eingehen können, werden
zur Darstellung der Gefährdungslage typische Szenarien zugrunde gelegt. Die folgenden spezifischen
Bedrohungen und Schwachstellen sind für den Baustein SYS.2.1 Allgemeiner Client von besonderer
Bedeutung.
* [2.1. Schadprogramme (G 0.39)](../Gefährdungen/G0.39_Schadprogramme.md)
* 2.2. Datenverlust durch lokale Datenhaltung
* 2.3. Hardware-Defekte bei Client-Systemen
* 2.4. Unberechtigte Nutzung von Clients
* 2.5. Installation nicht benötigter Betriebssystemkomponenten und Applikationen
* 2.6. Abhören von Räumen mittels Mikrofon und Kamera
* 2.7. Fehlerhafte Administration oder Nutzung von Geräten und Systemen
