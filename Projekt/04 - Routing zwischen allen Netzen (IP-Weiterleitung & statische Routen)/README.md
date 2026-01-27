# 04 – Routing zwischen allen Netzen (IP-Weiterleitung & statische Routen)

Da sich alle Clientnetze sowie das Servernetz in unterschiedlichen IP-Bereichen befinden, ist Routing notwendig, damit die Geräte netzübergreifend kommunizieren können.

Ohne Routing könnten sich die Netze gegenseitig nicht erreichen.

---

## 🔁 Aktivierung der IP-Weiterleitung

Auf **allen Routern** wurde die Option **IP-Weiterleitung aktivieren** eingeschaltet.

Diese Funktion erlaubt es dem Router, Datenpakete von einem Netzwerk in ein anderes weiterzuleiten.

Ohne diese Aktivierung würde der Router nur innerhalb seines eigenen Netzes arbeiten.

---

## 🗺️ Statische Routingtabellen

Zusätzlich zur IP-Weiterleitung wurden auf jedem Router statische Routen eingetragen.

Diese Routen enthalten:

- Zielnetz (z. B. 192.168.2.0)
- Subnetzmaske (255.255.255.0)
- Nächster Router (Next Hop)

Jeder Router kennt dadurch den Weg:

- zu allen anderen Clientnetzen
- zum Servernetz

---

## 🧩 Beispiel einer Route (vereinfacht)

Ein Router im Netz `192.168.1.0` besitzt u. a. folgende Einträge:

| Zielnetz | Maske | Weiterleitung an |
|----------|-------|------------------|
| 192.168.2.0 | 255.255.255.0 | Router Richtung Netz 2 |
| 192.168.3.0 | 255.255.255.0 | Router Richtung Netz 3 |
| 192.168.4.0 | 255.255.255.0 | Router Richtung Netz 4 |
| 134.34.86.0 | 255.255.255.0 | Serverrouter |

Diese Logik ist auf allen Routern vorhanden.

---

## 🎯 Ziel dieser Konfiguration

Durch diese Routingtabellen wird erreicht, dass:

- alle Netze sich gegenseitig anpingen können
- Clients den DNS-Server erreichen
- Clients den Webserver erreichen (sofern nicht durch Firewall blockiert)

Das Routing ist die technische Grundlage für die gesamte Kommunikation im Projekt.

---

## 📸 Nachweise (Screenshots)

**Einfügen:**

- Screenshot Routerfenster mit aktivierter IP-Weiterleitung
- Screenshot Weiterleitungstabelle Router Netz 1
- Screenshot Weiterleitungstabelle Router Netz 2
- Screenshot Weiterleitungstabelle Router Netz 3
- Screenshot Weiterleitungstabelle Router Netz 4
- Screenshot Weiterleitungstabelle Serverrouter
