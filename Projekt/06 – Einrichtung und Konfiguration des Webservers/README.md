# 06 – Einrichtung und Konfiguration des Webservers

Im Servernetz wurde ein Webserver eingerichtet, der eine Webseite für die Clientnetze bereitstellt.  
Dieser Webserver ist das zentrale Ziel, auf das später gezielt zugegriffen bzw. der Zugriff eingeschränkt wird.

---

## 🌐 Zweck des Webservers im Projekt

Der Webserver dient dazu:

- einen zentralen Dienst bereitzustellen
- die Funktion von DNS, Routing und Firewall sichtbar zu machen
- den Zugriff aus verschiedenen Netzen zu testen

Er ist somit das praktische Beispiel für die Netzkommunikation.

---

## 🖥️ Netzwerkkonfiguration des Webservers

Der Webserver wurde manuell konfiguriert:

| Einstellung | Wert |
|-------------|------|
| IP-Adresse | `134.34.86.30` |
| Subnetzmaske | `255.255.255.0` |
| Gateway | `134.34.86.1` |
| DNS | `134.34.86.31` |

Diese Einstellungen sind notwendig, damit der Webserver:

- Anfragen aus anderen Netzen beantworten kann
- selbst den DNS-Server erreichen kann
- korrekt über den Router kommuniziert

---

## 🔗 Verbindung zum DNS

Durch den DNS-Eintrag:

test.ch → 134.34.86.30

kann der Webserver über einen Domainnamen erreicht werden.

---

## 🎯 Ziel dieser Konfiguration

Durch die korrekte Einrichtung des Webservers wird erreicht, dass:

- Clients aus den Netzen die Webseite aufrufen können
- Routing, DNS und Firewall praktisch getestet werden können
- die Kommunikation sichtbar nachvollzogen werden kann

---

## 🧪 Funktionstest

Der Zugriff erfolgt über den Browser mit:

http://test.ch

Ob der Zugriff möglich ist, hängt später von der Firewallregel ab.

---

## 📸 Nachweise (Screenshots)

**Einfügen:**

- Screenshot Netzwerkeinstellungen des Webservers
- Screenshot Browser mit aufgerufener Seite `http://test.ch`
