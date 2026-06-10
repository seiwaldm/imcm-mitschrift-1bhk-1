# IMCM-Mitschrift der 1BHK (Gruppe 1)

Das ist das README.md File unseres Repositories. Die Dateieendung .md steht für Markdown - eine heute sehr weit verbreitete [Auszeichnungssprache](https://de.wikipedia.org/wiki/Auszeichnungssprache). Weitere bekannte Auszeichnungssprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

> **Achtung!**
> Die Abkürzung ML steht nicht immer für _Markup Language_, sie kann auch _Machine Learning_ heißen.

## Playlist zur Funktionsweise des Internets

![TCP-IP-Modell](/assets/tcp-ip-stack.webp)

### Teil 1 - What is the Internet?

- das Internet wurde in den 1970er-Jahren entwickelt
- Motivation: Schaffung eines dezentralen Netzwerks, das auch nach einem Atomschlage noch funktioniert (Kontext des Kalten Krieges)
- Funktionsweise: Paketvermittlung (_Packet Switching_) - Nachrichten bzw. Dateien werden in kleine Pakete aufgeteilt und unabhängig voneinander über das Netzwerk verschickt
- Internet: das Netz der Netze - besteht aus vielen kleineren Netzen unterschiedlicher Internetanbieter (_Internet Service Provider - ISP_, z.B.: Salzburg AG, Magenta, A1, ...)

### Teil 2 - The Internet: Wires, Cables and WiFi

Informationen werden im Internet als Bits übertragen. Bits haben zwei Werte: 0 und 1. 8 Bits zusammengefasst ergeben 1 Byte. Mit einem Byte kann man 256 verschiedene Werte speichern (2^8).

Bits können über verschiedene Übertragungsmedien zwischen Computern versendet werden. Die Anzahl der übertragenen Bits pro Sekunde wird als **Bandbreite** bezeichnet. Bei einer Bandbreite von 300MBit/s können beispielsweise 300 Millionen Bit pro Sekunde über die Leitung laufen. Übertragungsmedien können sein:

**1. Elektrizität / Kupferdraht (Ethernet)**

- billig
- einfach in der Verarbeitung
- weit verbreitet
- hohe Verluste über mittlere und lange Distanzen (hunderte Meter)

**2. Licht / Glasfaserkabel**

- schnelle Übertragung
- verlustfrei
- geeignet für Ozeankabel
- teuer und schwierig in der Verarbeitung

**3. Funk / Radiowellen**

- hoher Komfort, Internet überall

### Teil 3 - The Internet: IP-Addresses & DNS

- Protokolle sind die Regeln der Kommunikation
- eines der wichtigsten Protokolle im Internet ist das Internet Protocol (IP)
- jedes Gerät im Internet hat zumindest eine (eindeutige) IP-Adresse, viele Geräte haben aber eine externe IP (ähnlich wie die Hausnummer) und eine interne IP (ähnlich wie die Raumnummer)
- das Domain Name System (DNS) übersetzt menschenlesbare Domainnamen (z.B.: www.google.com) in IP-Adressen
- DNS-Server führen Tabellen mit Domainnamen und den entsprechenden IP-Adressen

### Teil 4 - The Internet: Packets, Routing & Reliability

- über das Internet versendete Daten werden in Pakete aufgeteilt
- einzelne Pakete haben eine Größe von ca. 1,5kB. D.h., ein Foto mit einer Größe von 10MB wird in ca. 6700 Pakete aufgeteilt, bevor es über das Internet versendet wird
- Pakete können unterschiedliche Routen durch das Internet nehmen. Die Route wird je nach Auslastung, Störungen etc. durch spezielle Computer - die Router - dynamisch bestimmt.
- jedes Paket enthält die Quell- und Ziel-IP-Adresse sowie eine eindeutige Paketnummer
- das _Transmission Control Protocol_ (TCP) prüft am Ziel, ob alle Pakete einer Übertragung angekommen sind. Falls Pakete fehlen, fordert es diese erneut vom Absender an.
- TCP und IP bilden gemeinsam das Rückgrat des Internets. Man spricht daher auch vom TCP/IP-Modell bzw. _TCP/IP-Stack_.

### Teil 5 - The Internet: HTTP & HTML

- HTTP steht für _Hypertext Transport Protocol_. HTTP arbeitet nach dem Client-Server-Prinzip:

  - ein Web-Client (Browser) sendet eine Anfrage (_request_) an einen Web-Server
  - der Web-Server verarbeitet die Anfrage und sendet eine Antwort (_response_) zurück. Die Antwort enthält u.a. einen sogenannten [HTTP-Statuscode](https://de.wikipedia.org/wiki/HTTP-Statuscode), der Auskunft über die Verarbeitung der Anfrage gibt.

  > #### HTTP-Statuscodes
  >
  > - **1xx** - die Anfrage dauert noch an
  > - **2xx** - die Anfrage war erfolgreich
  > - **3xx** - Um- oder Weiterleitung
  > - **4xx** - Clienfehler (z.B. 404 - _Page not found_)
  > - **5xx** - Serverfehler 💀

### Teil 8 - The Internet: How Search Works

- Suchmaschinen-Bots (_Crawler_) durchstreifen ständig das WWW und katalogisieren Websites. Der so enstehende Katalog wird auch **Index** genannt.
- wenn wir einen Suchbegriff bei Google (oder einer anderen _Search Engine_) eingeben, wird NICHT das WWW durchsucht, sondern lediglich der zuvor erstellte Index
- Suchergebnisse werden auf Basis eines (geheimen) Algorithmus geranked - Ergebnisse, die weiter oben stehen, werden öfter angeklickt
- Einfluss auf das Ranking haben u.a.:
  - im Text vorkommende Suchbegriffe (_Keywords_)
  - Links, die auf meine Seite zeigen (_Backlinks_)
- die Suchergebnisse werden an die Benutzer\*innen angepasst! D.h., nicht jede/r sieht die gleichen Informationen, selbst wenn sie idente Suchanfragen durchführen!
- [Startpage](https://www.startpage.com/) ist eine datensparsame Suchmaschine, die ihren Benutzern\*innen die Verwendung von Google ohne Tracking oder Personalisierung erlaubt
