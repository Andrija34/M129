## 09 – Nachvollzug des Datenflusses im Netzwerk

Zum besseren Verständnis wird hier der komplette Kommunikationsweg eines Clients zum Webserver Schritt für Schritt nachvollzogen.

Dieses Beispiel zeigt, wie DHCP, DNS, Routing und Firewall zusammenarbeiten.

---

## 🖥️ Ausgangssituation

Ein Client aus dem Netz **192.168.4.0** mit der Adresse `192.168.4.3` möchte die Webseite `http://test.ch` aufrufen.

---

## 🔁 Schritt 1 – IP-Konfiguration durch DHCP

Beim Start erhält der Client automatisch vom DHCP-Server:

- IP-Adresse: z. B. `192.168.4.3`
- Subnetzmaske: `255.255.255.0`
- Gateway: `192.168.4.1`
- DNS: `134.34.86.31`

Der Client weiss nun, wohin er Anfragen ausserhalb seines Netzes senden muss.

---

## 🌐 Schritt 2 – DNS-Anfrage

Der Client kennt nur den Namen `test.ch` und fragt den DNS-Server:

> „Welche IP-Adresse hat test.ch?“

Der DNS-Server antwortet:

test.ch → 134.34.86.30

---

## 🗺️ Schritt 3 – Routing zum Servernetz

Da sich die IP `134.34.86.30` nicht im eigenen Netz befindet, sendet der Client das Paket an sein Gateway `192.168.4.1`.

Die Router leiten das Paket anhand der Routingtabellen weiter, bis es das Servernetz erreicht.

---

## 🔐 Schritt 4 – Firewallprüfung

Bevor das Paket den Webserver erreicht, prüft der Switch im Servernetz die Firewallregel:

- Netz 4 → erlaubt ✅
- Andere Netze → blockiert ❌

Da der Client aus Netz 4 stammt, wird das Paket weitergeleitet.

---

## 🖥️ Schritt 5 – Antwort des Webservers

Der Webserver verarbeitet die Anfrage und sendet die Webseite über denselben Weg zurück zum Client.

---

## ❌ Vergleich: Client aus Netz 1

Ein Client aus `192.168.1.0` durchläuft dieselben Schritte, wird jedoch bei Schritt 4 von der Firewall blockiert.

---

## 🎯 Bedeutung dieses Ablaufs

Dieser Datenfluss zeigt deutlich:

- DHCP liefert die Grundlage für Kommunikation
- DNS übersetzt Namen in IP-Adressen
- Routing verbindet die Netze
- Firewall kontrolliert den Zugriff
- Alle Komponenten arbeiten zusammen






