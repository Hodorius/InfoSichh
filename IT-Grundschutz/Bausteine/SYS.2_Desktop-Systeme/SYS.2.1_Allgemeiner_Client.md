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
* 2.1. Schadprogramme [(G 0.39)](../Gefährdungen/G0.39_Schadprogramme.md)
* 2.2. Datenverlust durch lokale Datenhaltung
* 2.3. Hardware-Defekte bei Client-Systemen
* 2.4. Unberechtigte Nutzung von Clients
* 2.5. Installation nicht benötigter Betriebssystemkomponenten und Applikationen
* 2.6. Abhören von Räumen mittels Mikrofon und Kamera
* 2.7. Fehlerhafte Administration oder Nutzung von Geräten und Systemen

## 3. Anforderungen
Im Folgenden sind die spezifischen Anforderungen des Bausteins SYS.2.1 Allgemeiner Client aufgeführt.
Der oder die Informationssicherheitsbeauftragte (ISB) ist dafür zuständig, dass alle Anforderungen
gemäß dem festgelegten Sicherheitskonzept erfüllt und überprüft werden. Bei strategischen
Entscheidungen ist der oder die ISB stets einzubeziehen.
Im IT-Grundschutz-Kompendium sind darüber hinaus weitere Rollen definiert. Sie sollten besetzt
werden, insofern dies sinnvoll und angemessen ist.

| Zuständigkeiten         | Rollen                  |
| ----------------------- | ----------------------- |
| Grundsätzlich zuständig | IT-Betrieb              |
| Weitere Zuständigkeiten | Benutzende, Haustechnik |

Genau eine Rolle sollte Grundsätzlich zuständig sein. Darüber hinaus kann es noch Weitere
Zuständigkeiten geben. Falls eine dieser weiteren Rollen für die Erfüllung einer Anforderung vorrangig
zuständig ist, dann wird diese Rolle hinter der Überschrift der Anforderung in eckigen Klammern
aufgeführt. Die Verwendung des Singulars oder Plurals sagt nichts darüber aus, wie viele Personen
diese Rollen ausfüllen sollen.

### 3.1. Basis-Anforderungen
Die folgenden Anforderungen MÜSSEN für diesen Baustein vorrangig erfüllt werden.
* SYS.2.1.A1 Sichere Authentisierung von Benutzenden
* SYS.2.1.A2 ENTFALLEN
* SYS.2.1.A3 Aktivieren von Autoupdate-Mechanismen
* SYS.2.1.A4 ENTFALLEN
* SYS.2.1.A5 ENTFALLEN
* SYS.2.1.A6 Einsatz von Schutzprogrammen gegen Schadsoftware
* SYS.2.1.A7 ENTFALLEN
* SYS.2.1.A8 Absicherung des Bootvorgangs
* SYS.2.1.A42 Nutzung von Cloud- und Online-Funktionen (Benutzende)
