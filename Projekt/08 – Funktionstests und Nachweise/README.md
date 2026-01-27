# 08 – Funktionstests und Nachweise

Nach der vollständigen Einrichtung aller Komponenten wurden gezielte Tests durchgeführt, um die korrekte Funktion des gesamten Netzwerks nachzuweisen.

Diese Tests belegen, dass DHCP, Routing, DNS, Webserver und Firewall wie geplant zusammenarbeiten.

---

## 🧪 Test 1 – Erreichbarkeit zwischen den Netzen (Ping)

Von Clients aus verschiedenen Netzen wurden Ping-Tests durchgeführt:

- Clients können ihre jeweiligen Gateways erreichen
- Clients können Geräte in anderen Netzen erreichen
- Clients können den DNS-Server und den Webserver anpingen

➡️ Beweis, dass das Routing korrekt funktioniert.

![Ping-Test](<Screenshot 2026-01-27 103318.png>)

---

## 🧪 Test 2 – DNS-Namensauflösung

Mit dem Befehl:

nslookup test.ch

wurde überprüft, ob der DNS-Server den Domainnamen korrekt in die IP-Adresse des Webservers auflöst.

➡️ Beweis, dass die DNS-Konfiguration korrekt ist.

![nslookup](<Screenshot 2026-01-27 103517.png>)

---

## 🧪 Test 3 – Zugriff auf den Webserver

Der Webserver wurde über den Browser mit folgender Adresse aufgerufen:

http://test.ch

Beobachtung:

- Zugriff aus Netz 192.168.4.0 funktioniert
- Zugriff aus Netz 192.168.1.0, 2.0, 3.0 wird blockiert

➡️ Beweis, dass die Firewallregel korrekt greift.

![Browser](<Screenshot 2026-01-27 103235.png>)

---

## 🧪 Zusammenfassung der Testergebnisse

| Test | Erwartung | Ergebnis |
|------|-----------|----------|
| Ping zwischen Netzen | möglich | ✅ |
| DNS-Auflösung | korrekt | ✅ |
| Webzugriff nur aus Netz 4 | korrekt | ✅ |

Diese Tests zeigen, dass alle Komponenten korrekt zusammenspielen.






