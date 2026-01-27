# 11 – Reflexion und mögliche Erweiterungen

Nach der erfolgreichen Umsetzung der Netzwerkinfrastruktur lassen sich aus diesem Projekt wichtige Erkenntnisse gewinnen. Gleichzeitig gibt es verschiedene Möglichkeiten, wie diese Struktur in einer realen Umgebung weiter ausgebaut oder verbessert werden könnte.

---

## 🧠 Erkenntnisse aus dem Projekt

Während der Umsetzung wurde deutlich, wie stark die einzelnen Netzwerkkomponenten voneinander abhängig sind:

- Ohne korrektes DHCP funktioniert keine Kommunikation
- Ohne Routing bleiben die Netze voneinander getrennt
- Ohne DNS müssten IP-Adressen verwendet werden
- Ohne Firewall gäbe es keine Zugriffskontrolle
- Erst das Zusammenspiel aller Elemente ergibt ein funktionierendes Netzwerk

Besonders sichtbar wurde, dass funktionierendes Routing **nicht automatisch** bedeutet, dass alle Zugriffe erlaubt sind.  
Die Firewallregel zeigt klar den Unterschied zwischen **Erreichbarkeit** und **Zugriffsberechtigung**.

---

## 🔍 Verständnis für reale Netzwerkstrukturen

Dieses Projekt bildet eine vereinfachte Version eines echten Firmennetzwerks ab:

- getrennte Abteilungen (LANs)
- zentrale Serverdienste
- kontrollierter Zugriff auf Server
- klare Struktur und saubere Adressierung

---

## 🚀 Mögliche Erweiterungen

Folgende Erweiterungen wären in einer realen Umgebung sinnvoll:

- Einsatz eines zentralen DHCP-Servers mit DHCP-Relay
- Verwendung von VLANs statt physisch getrennten Netzen
- Einsatz dynamischer Routingprotokolle (z. B. OSPF) statt statischer Routen
- Absicherung der Server durch zusätzliche Firewallregeln
- Einbindung weiterer Dienste (z. B. Mailserver, Fileserver)

---

## 🏁 Schlussgedanke

Das Projekt zeigt, wie aus einzelnen Netzwerkbausteinen eine vollständige, strukturierte und sichere Netzwerkinfrastruktur entsteht.  
Es vermittelt ein gutes Verständnis dafür, wie Netzwerke geplant, aufgebaut und abgesichert werden.
