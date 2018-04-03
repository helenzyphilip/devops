Modul 300
=============
Installation
-------------
1.	Ubuntu Server Image herunterladen
2.	VM auf VirtualBox erstellen 
3.	Testen in dem man VBoxManage list vms
3.	Beim Netzwerk unter NAT: Port 80 als Weiterleitung zu Port 8080 (Host) eintragen
4.	installiere die Linux Server Umgebung
5.	Apache Server installieren mit sudo apt-get install apache2
6.	Testen ob es funktioniert hat indem man Browsers lokal öffnet und
http://localhost:8080 eingibt.

| Befehle | Was sie machen? |
| ------ | ------ |
| sudo -i | Superuser Warden, ein Password ist nicht erforderlich |
| sudo service servicename start / stop|  Starten/ Stoppen eines Services|
| sudo shutdown -r now | Restart des Betriebssystems |
| sudo shutdown -h now | Stoppen des Betriebssystems |
| cd | Wechsel Verzeichnis |
| rm | löschen |
| mv | verschieben |
| Ls | Anzeigen Von Dateien |
| Nano oder vi | Texteditoren |
| Df -h | Diskbelegung |
| free -m | Speicherbelegung |
| w | Auslastung CPU |
| Ifconfig | Ausgabe der eigenen IP-Adresse |
| Netstat -a oder netstat -tulpen | Ausgabe der verwendeten Network Ports |
| Net lookup *hostname* | IP-Adresse für Hostname ausgeben |
| Ps -ef oder top | Anzeige der aktiven Prozesse |
| Kill *pid* | Prozess laut Prozess-ID beenden |
| Curl http:*//server* | löschen |
| Wget http://server/datei | Kopieren einer Datei von einem Webserver |
| Dos2unix datei | Datei vom DOS ins UNIX/Linux Format umwandeln. Wird immer dann benötigt wenn eine Datei von Windows nach Linux kopiert wird und überflüssige CR enthält.|

Advanced Packaging Tool
-----------------------
Das Advanced Packaging Tool (APT) ist ein Paketverwaltungssystem und dpkg zur Paketverwaltung benutzt. Es ermöglicht eine einfache suche, Installation und Aktualisierung von Programmpaketen zur Verfügung zu stellen. 

| Befehle | Was sie machen? |
| ------ | ------ |
| sudo apt-get update | Repositories aktualisieren |
| sudo apt-get -y install apache2  | Webserver Apache installieren|
| sudo apt-get -y upgrade  | Bestehende Software aktualisieren|
| sudo apt-get -y autoremove |Aufräumen, nicht mehr benötigte Software entfernen|
| sudo apt-cache search *keyword* |Suchen nach einem bestimmten Programmpaket|
sudo dpkg -i programmpaket |Installieren eines vorher downloadeten Programmpaketes|

REST Client: cURL
-----------------------
cURL (Client for URLs oder Curl URL Request Library) ist ein Kommandozeilen-Programm zum Übertragen von Dateien in Rechnernetzen. cURL wird auch sehr oft zum Testen von aktiven Ports oder Services benützt. 

210 Versionsverwaltung 
-----------------------
Eine Versionsverwaltung ist ein System. Die zur Erfassung von Änderungen dient an den Dokumenten oder Dateien. Alle Versionen werden in einem Archiv mit Zeitstempel und Benutzerkennung gesichert und können später wiederhergestellt werden. Das wird in der Softwareentwicklung eingesetzt, um Quelltexte zu verwalten.  

Repository
-----------------------
Ein Repository ist ein verwaltetes Verzeichnis zur Speicherung und Beschreibung von digitalen Objekten für ein digitales Archiv. Bei den verwalteten Objekten kann es sich beispielsweise um Programme (Software-Repository), Publikationen (Dokumentenserver), Datenmodelle (Metadaten-Repository) oder betriebswirtschaftliche Verfahren handeln. Häufig beinhaltet ein Repository auch Funktionen zur Versionsverwaltung der verwalteten Objekte.

GitHub ist ein webbasierter Online-Dienst, der Software-Entwicklungsprojekte auf seinen Servern bereitstellt. Zusätzlich bietet er diverse Management und Bug-Tracking-Funktionalitäten.

GitLab ist eine Webanwendung zur Versionsverwaltung für Softwareprojekte. Sie bietet diverse Management und Bug-Tracking-Funktionalitäten, sowie mit GitLab CI ein System zur Kontinuierlichen Integration.

Markdown
-----------------------
Markdown ist eine vereinfachte Auszeichnungssprache.

Ein Ziel von Markdown ist, dass schon die Ausgangsform ohne weitere Konvertierung leicht lesbar ist. Als Auszeichnungselemente wurden daher vor allem Auszeichnungsarten verwendet, die in Plain text und E-Mails üblich sind.

Genutzt wird Markdown vorwiegend auf Plattformen mit eher technikaffinem Publikum wie GitHub, Stack Overflow oder der Blogging-Plattform Ghost. Markdown wird häufig bei Readme-Dateien verwendet.

Markdown Dateien (.md) können über die Weboberfläche von GitLab editiert werden. Alternativen sind die Wiki Erweiterungen von Eclipse, der GitBook Editor oder Visual Studio Code.

220 Apache + MySQL
-----------------------
### Apache http Web Server
Der Apache HTTP Server ist ein quelloffenes und freies Produkt der Apache Software Foundation und der meistbenutzte Webserver im Internet.
Der Apache-Server kann sehr gut mit sogenannten Modulen erweitert werden, die bestimmte Zusatzfunktionen mitbringen und immer mit 'mod_' beginnen.

### Installation (Apache mit cgi Module)
 - sudo apt-get install apache2 apache2-doc
 - sudo a2enmod cgi
 - sudo service apache2 restart

### http (Hypertext  Transfer Protocol)
Das Hypertext Transfer Protocol (HTTP, englisch für Hypertext-Übertragungsprotokoll) ist ein Protokoll zur Übertragung von Nachrichten und Daten. Es wird hauptsächlich eingesetzt, um Webseiten (Hypertext-Dokumente) aus dem World Wide Web (WWW) in einen Webbrowser zu laden. Es ist jedoch nicht prinzipiell darauf beschränkt und auch als allgemeines Dateiübertragungsprotokoll sehr verbreitet.

Jede Nachricht besteht dabei aus zwei Teilen, dem Nachrichtenkopf (englisch Message Header, kurz: Header oder auch HTTP-Header genannt) und dem Nachrichtenrumpf (englisch Message Body, kurz: Body). Der Nachrichtenkopf enthält die Anfragemethode und Informationen über den Nachrichtenrumpf wie etwa verwendete Kodierungen oder den Inhaltstyp. Der Nachrichtenrumpf enthält die Nutzdaten (siehe HTML unten).

Von den Nachrichten gibt es zwei unterschiedliche Arten: die Anfrage (englisch Request) vom Client an den Server und die Antwort (englisch Response) als Reaktion darauf vom Server zum Client. Die mbed Board's können als HTTP Client oder als HTTP Server Eingesetzt werden.

**http-Anfragemethoden**
-	GET: ist die gebräuchlichste Methode. Mit ihr wird eine Ressource (zum Beispiel eine HTML Datei) vom Server angefordert.
-	POST: schickt Daten zur weiteren Verarbeitung zum Server.
-	PUT: dient dazu eine Ressource (zum Beispiel eine Datei) auf einen Webserver hochzuladen.
-	DELETE: löscht die angegebene Ressource auf dem Server.

**HTML (Nachrichtenrumpf)**
Die Hypertext Markup Language (engl. für Hypertext-Auszeichnungssprache), abgekürzt HTML, ist eine textbasierte maschinenlesbare Sprache (markup language) zur Strukturierung digitaler Dokumente wie Texte mit Hyperlinks, Bildern und anderen Inhalten.

HTML-Dokumente sind die Grundlage des World Wide Web und werden von Webbrowsern dargestellt.

REST
-----------------------
Representational State Transfer (abgekürzt REST, seltener auch ReST) bezeichnet ein Programmierparadigma für verteilte Systeme.

REST ist eine Abstraktion der Struktur und des Verhaltens des World Wide Web (HTTP GET, PUT, POST, DELETE).

REST hat das Ziel, einen Architekturstil zu schaffen, der die Anforderungen des modernen Web besser darstellt. Dabei unterscheidet sich REST vor allem in der Forderung nach einer einheitlichen Schnittstelle von anderen Architekturstilen.

Wird über HTTP zugegriffen, entsprechen die REST Operationen den HTTP-Abfragemethoden.

REST Serverseite: CGI Script
-----------------------
**Common Gateway Interface (CGI)**
Das Common Gateway Interface (CGI) ist ein Standard für den Datenaustausch zwischen einem Webserver und dritter Software, die Anfragen bearbeitet.

MYSQL
-----------------------
Eine Datenbank, auch Datenbanksystem (DBS) genannt, ist ein System zur elektronischen Datenverwaltung. Die wesentliche Aufgabe eines DBS ist es, große Datenmengen effizient, widerspruchsfrei und dauerhaft zu speichern und benötigte Teilmengen in unterschiedlichen, bedarfsgerechten Darstellungsformen für Benutzer und Anwendungsprogramme bereitzustellen.

MySQL ist eines der weltweit verbreitetsten relationalen Datenbankverwaltungssysteme. Es ist als Open-Source-Software sowie als kommerzielle Enterprise Version für verschiedene Betriebssysteme verfügbar und bildet die Grundlage für viele dynamische Webauftritte.

**Installation Datenbank**
Sudo apt-get install mysql-server mysql-client

**Konfiguration**
1.	Anmelden bei der Datenbank: mysql -u root -p t11
2.	Datenbank auf dem Prompt anlegen: create database if not exists sensoren;
3.	Neue Datenbank-Benutzer www-data mit dem Kennwort mbed erstellen: 
create user 'www-data'@'localhost' identified by 'mbed';
grant usage on *.* to 'www-data'@'localhost' identified by 'mbed';
4.	Zugriff auf die neue Datenbank für den Benutzer www-data erlauben:grant all privileges on sensoren.* to 'www-data'@'localhost';
flush privileges;
5.	Datenbank wechseln: use sensoren;
6.	Tabelle für die Sensordaten erstellen: 
create table data ( seq INT PRIMARY KEY AUTO_INCREMENT, poti FLOAT, light FLOAT, hall FLOAT, temp FLOAT, created TIMESTAMP DEFAULT CURRENT_TIMESTAMP );
7.	Abmelden mit: quit

**CGI-Script (Daten in SQL Datenbank schreiben)**
1.	Folgende Befehle eingeben:
sudo cp restsql.txt /usr/lib/cgi-bin/restsql
sudo chmod +x /usr/lib/cgi-bin/restsql
sudo dos2unix /usr/lib/cgi-bin/restsql
2.	Testen mit:
a.	Daten in MySQL Datenbank schreiben:
 curl -v -X POST http://localhost/cgi-bin/restsql -d "poti=0.5&hall=0.1&light=0.8&temp=26"
b.	Abfrage im Browser mittels: http://localhost:8080/cgi-bin/restsql

### Firewall
Eine Firewall (von englisch firewall ‚Brandwand‘ oder ‚Brandmauer‘) ist ein Sicherungssystem, das ein Rechnernetz oder einen einzelnen Computer vor unerwünschten Netzwerkzugriffen schützt und ist weiter gefasst auch ein Teilaspekt eines Sicherheitskonzepts.

Jedes Firewall-Sicherungssystem basiert auf einer Softwarekomponente. Die Firewall-Software dient dazu, den Netzwerkzugriff zu beschränken, basierend auf Absender- oder Zieladresse und genutzten Diensten. Sie überwacht den durch die Firewall laufenden Datenverkehr und entscheidet anhand festgelegter Regeln, ob bestimmte Netzwerkpakete durchgelassen werden oder nicht. Auf diese Weise versucht sie, unerlaubte Netzwerkzugriffe zu unterbinden.

| Befehle | 
| ------ | 
| netstat -tulpen| 
| sudo apt-get install ufw | 
| sudo ufw status
sudo ufw enable| 
sudo ufw disable| 
| Test: curl -f 192.168.55.101|
Test: curl -f 192.168.55.100:3306| 
sudo ufw status numbered |
sudo ufw delete 1|

Test
-------------

VM: 
- VBoxManage list vms mit diesem Befehl konnte ich schauen was für VM erstellt wurden.

GitHub: 
- git pull
- git status mit diesen Befehlen konnte man nachschauen ob alles im aktuellen Stand ist.

Vagrant:
- mkdir ubuntu
- cd ubuntu
- vagrant init ubuntu/xenial64
- vagrant up --provider virtualbox




