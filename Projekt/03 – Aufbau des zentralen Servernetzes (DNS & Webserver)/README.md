# 03 – Aufbau des zentralen Servernetzes (DNS & Webserver)

Neben den vier Client-LANs wurde ein separates Servernetz aufgebaut.  
Dieses Netz stellt zentrale Dienste für alle Clientnetze bereit und ist logisch von ihnen getrennt.

---

## 🧭 Zweck des Servernetzes

Das Servernetz dient dazu:

- zentrale Dienste bereitzustellen (DNS und Webserver)
- diese Dienste kontrolliert für bestimmte Netze freizugeben
- eine klare Trennung zwischen Clients und Servern zu schaffen

Diese Struktur entspricht dem Aufbau realer Firmennetzwerke.

---

## 🖥️ Komponenten im Servernetz

| Gerät | IP-Adresse | Funktion |
|------|-------------|----------|
| Router | 134.34.86.1 | Gateway ins Servernetz |
| DNS-Server | 134.34.86.31 | Namensauflösung |
| Webserver | 134.34.86.30 | Bereitstellung der Webseite |
| Switch | — | Verbindung der Server |

---

## 🔌 Netzwerkeinstellungen der Server

Beide Server wurden **manuell** konfiguriert:

### DNS-Server

- IP-Adresse: `134.34.86.31`
- Subnetzmaske: `255.255.255.0`
- Gateway: `134.34.86.1`

### Webserver

- IP-Adresse: `134.34.86.30`
- Subnetzmaske: `255.255.255.0`
- Gateway: `134.34.86.1`
- DNS: `134.34.86.31`

---

## 🎯 Ziel dieser Struktur

Durch das separate Servernetz:

- sind die Server nicht direkt in den Clientnetzen
- kann der Zugriff gezielt über Routing und Firewall gesteuert werden
- können alle Netze zentral auf DNS und Webserver zugreifen (sofern erlaubt)

Diese Trennung ist entscheidend für das spätere Sicherheitskonzept.

---

## 📸 Nachweise (Screenshots)

Hier wird das Servernetz dokumentiert.

**Einfügen:**
![Netz 5](<Screenshot 2026-01-27 102320.png>)
![DNS-Server](<Screenshot 2026-01-27 103141.png>)
![DNS-Einstellungen](<Screenshot 2026-01-27 142726.png>)
![Webserver-Einstellungen](<Screenshot 2026-01-27 103209.png>)
