# 🌐 FILIUS Netzwerkprojekt – Routing, DHCP, DNS, Webserver & Firewall

**Name:** Andrija Milosevic  
**Umgebung:** FILIUS

Dieses Projekt zeigt den Aufbau einer mehrstufigen Netzwerkinfrastruktur mit mehreren getrennten LAN-Netzen, zentralen Serverdiensten und gezielter Zugriffskontrolle.

Die Dokumentation ist **nach Anforderungen strukturiert**.  
Jede Anforderung befindet sich in einem eigenen Ordner und beschreibt:

- Ziel der Anforderung
- Umsetzung im Netzwerk
- Konfiguration der Geräte
- Nachweise durch Screenshots und Tests

---

## 📁 Aufbau der Dokumentation

| Ordner | Inhalt |
|--------|-------|
| `01_LAN_Struktur` | Aufbau der getrennten Client-Netze |
| `02_DHCP` | Automatische IP-Adressvergabe in allen Netzen |
| `03_Servernetz` | Zentrales DNS- und Webservernetz |
| `04_Routing` | IP-Weiterleitung und statische Routingtabellen |
| `05_DNS` | Namensauflösung für den Webserver |
| `06_Webserver` | Konfiguration und Erreichbarkeit des Webservers |
| `07_Firewall` | Zugriffskontrolle auf den Webserver |
| `08_Tests` | Funktionsnachweise (Ping, DNS, Web) |
| `09_Datenfluss` | Technische Erklärung der Kommunikation |

---

## 🎯 Ziel des Projekts

- Trennung mehrerer LAN-Netze
- Routing zwischen Subnetzen
- DHCP in jedem Netz
- Zentrale Dienste (DNS & Webserver)
- Sicherheitsregel mittels Firewall
- Vollständiger Funktionsnachweis
