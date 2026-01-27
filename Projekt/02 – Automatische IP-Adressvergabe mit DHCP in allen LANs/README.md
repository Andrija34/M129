# 02 – Automatische IP-Adressvergabe mit DHCP in allen LANs

Nachdem die vier getrennten LAN-Strukturen aufgebaut wurden, musste sichergestellt werden, dass alle Clients automatisch die korrekten Netzwerkeinstellungen erhalten.  
Dafür wurde in jedem LAN ein eigener DHCP-Server eingerichtet.

---

## ⚙️ Zweck von DHCP in diesem Projekt

DHCP übernimmt in jedem Netz automatisch die Vergabe von:

- IP-Adresse
- Subnetzmaske
- Standardgateway (Router)
- DNS-Server

Dadurch ist keine manuelle Konfiguration an den Clients notwendig und Fehlerquellen werden minimiert.

---

## 🧩 DHCP-Struktur pro Netz

Jedes Clientnetz besitzt **einen eigenen DHCP-Server**.

| Netz | DHCP-Server | Gateway | DNS |
|------|-------------|---------|-----|
| 192.168.1.0 | 192.168.1.10 | 192.168.1.1 | 134.34.86.31 |
| 192.168.2.0 | 192.168.2.10 | 192.168.2.1 | 134.34.86.31 |
| 192.168.3.0 | 192.168.3.10 | 192.168.3.1 | 134.34.86.31 |
| 192.168.4.0 | 192.168.4.10 | 192.168.4.1 | 134.34.86.31 |

---

## 📝 Einheitliche DHCP-Konfiguration

In allen Netzen wurden identische Einstellungen verwendet:

- Adressbereich: `.2 – .240`
- Subnetzmaske: `255.255.255.0`
- Gateway: Routeradresse des jeweiligen Netzes
- DNS-Server: `134.34.86.31`

Diese einheitliche Konfiguration sorgt für Übersichtlichkeit und Konsistenz.

---

## 🎯 Ziel dieser Konfiguration

Durch den Einsatz von DHCP wird sichergestellt, dass:

- alle Clients automatisch korrekt konfiguriert sind
- die Router als Standardgateway gesetzt sind
- die Clients später den DNS-Server erreichen können
- die Kommunikation zwischen den Netzen möglich ist

Ohne korrekt gesetztes Gateway und DNS wäre später weder Routing noch der Zugriff auf den Webserver möglich.

---

## 📸 Nachweise (Screenshots)

Für jedes Netz wird das DHCP-Fenster dokumentiert.

**Einfügen:**
![Netz 1](<Screenshot 2026-01-27 102313.png>)
![Netz 2](<Screenshot 2026-01-27 102302.png>)
![Netz 3](<Screenshot 2026-01-27 102252.png>)
![Netz 4](<Screenshot 2026-01-27 102241.png>)