# 05 – Namensauflösung mit DNS

Damit die Clients den Webserver nicht über eine IP-Adresse, sondern über einen Domainnamen erreichen können, wurde ein DNS-Server im Servernetz eingerichtet.

Der DNS-Server übernimmt die Aufgabe, einen Namen in eine IP-Adresse aufzulösen.

---

## 🌐 Zweck des DNS in diesem Projekt

Ohne DNS müssten Clients den Webserver über die IP-Adresse `134.34.86.30` aufrufen.  
Durch DNS kann stattdessen ein leicht merkbarer Name verwendet werden.

Dies entspricht der Funktionsweise realer Netzwerke und des Internets.

---

## 🖥️ Konfiguration des DNS-Servers

Auf dem DNS-Server wurde ein sogenannter **A-Record** erstellt:

test.ch → 134.34.86.30

Das bedeutet:

- Fragt ein Client nach `test.ch`
- Antwortet der DNS-Server mit der IP-Adresse des Webservers

---

## 🔗 Zusammenhang mit DHCP

Die Clients erhalten die DNS-Adresse `134.34.86.31` automatisch vom DHCP-Server.

Dadurch wissen alle Clients:

> Für Namensauflösungen muss der DNS-Server im Servernetz angefragt werden.

Ohne diese DHCP-Einstellung würde DNS nicht funktionieren.

---

## 🎯 Ziel dieser Konfiguration

Durch die DNS-Einrichtung wird erreicht, dass:

- Clients den Webserver über `http://test.ch` erreichen
- die Infrastruktur realitätsnah aufgebaut ist
- die Kommunikation zwischen Client → DNS → Webserver nachvollziehbar ist

---

## 🧪 Funktionstest der Namensauflösung

Mit dem Befehl:

nslookup test.ch

kann überprüft werden, ob der DNS-Server korrekt antwortet.

---

## 📸 Nachweise (Screenshots)

**Einfügen:**

- Screenshot DNS-Fenster mit A-Record `test.ch`
- Screenshot Konsole mit `nslookup test.ch`






