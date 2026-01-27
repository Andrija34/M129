# 01 – Aufbau der getrennten LAN-Struktur

In diesem Schritt wurde die grundlegende Netzwerkstruktur erstellt.  
Ziel war es, mehrere logisch getrennte Client-Netze aufzubauen, die unabhängig voneinander funktionieren und später über Router miteinander verbunden werden können.

---

## 🧱 Struktur der Client-Netze

Es wurden vier voneinander getrennte LAN-Netze erstellt.  
Jedes dieser Netze besitzt:

- einen eigenen Switch
- einen eigenen Router als Gateway
- einen eigenen DHCP-Server
- mehrere Clients

| Netz | Gateway (Router) | Zweck |
|------|-------------------|------|
| 192.168.1.0 | 192.168.1.1 | Clientnetz 1 |
| 192.168.2.0 | 192.168.2.1 | Clientnetz 2 |
| 192.168.3.0 | 192.168.3.1 | Clientnetz 3 |
| 192.168.4.0 | 192.168.4.1 | Clientnetz 4 |

Durch diese Aufteilung entstehen **vier separate Broadcast-Domänen**.

---

## 🖥️ Verwendete Komponenten pro Netz

Jedes LAN besteht aus:

- 1× Switch
- 1× Router
- 1× DHCP-Server
- mehreren PCs (Clients)

Diese identische Struktur sorgt dafür, dass jedes Netz gleich aufgebaut ist und später einfacher konfiguriert werden kann.

---

## 🎯 Ziel dieser Struktur

Die Trennung der Netze ist notwendig, um:

- Routing zwischen Subnetzen zu ermöglichen
- zentrale Dienste später gezielt freizugeben oder zu blockieren
- eine realistische Netzwerkstruktur wie in Unternehmen nachzubilden

Ohne diese Trennung wäre weder Routing noch eine gezielte Firewall-Regel möglich.

---

## 📸 Nachweis (Screenshots)

Hier wird die komplette Übersicht aller Netze eingefügt.

**Einfügen:**  
> Screenshot mit der Gesamtübersicht aller vier LANs (ohne Detailfenster)
