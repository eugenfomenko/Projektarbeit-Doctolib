# Vorlage: Topologie- & ISA‑Dokumentation für Praxis/KMV (TI‑Umfeld)

> Ziel: Eine **prüfungs- und auditfähige** Dokumentation, die Netz‑Topologie, Datenflüsse und ein kompaktes **Information Security Assessment (ISA)** für eine Arztpraxis/medizinische Versorgungseinrichtung abdeckt – inkl. TI/Doctolib/PVS.

---

## 1) Scope & Kontext
- **Organisation/Betriebsstätte:** Name, BSNR, IK, Standorte.
- **Geltungsbereich:** Praxisnetz, Heimarbeitsplätze (falls), Cloud‑Dienste (Doctolib), TI‑Anbindung, Druck/Scan.
- **Recht/Normen:** SGB V, gematik‑Vorgaben, KBV‑Anforderungen, DSGVO/AV, ISO 27001 (optional Bezug), BSI‑Grundschutz (optional Bezug).

## 2) Rollen & Verantwortlichkeiten
- **IT‑Verantwortlicher/ISB:** Name, Stellvertretung.
- **Praxisleitung/Datenverantwortung.**
- **Dienstleister:** PVS‑Hersteller, TI‑Dienst (Konnektor/KIM), Doctolib, Druckerwartung.
- **Kontaktmatrix & Eskalation:** Wer/Wie im Incident.

## 3) Systemlandschaft (Übersicht)
Kurze Beschreibung und Systemliste:
- **Endpunkte:** Arzt‑PC, MFA‑PC, Anmeldung, Behandlungsraum, Kiosk.
- **Server/Appliances:** PVS‑Server, Fileserver, Domain‑Controller (falls), Backup.
- **TI‑Komponenten:** Konnektor, Kartenterminal(e), eHBA/SMC‑B, KIM‑Clientmodul.
- **Cloud‑Dienste:** Doctolib (SaaS), E‑Mail (extern, getrennt von KIM), VPN/Remote.
- **Peripherie:** Drucker/Scanner/Etikettendrucker, eGK‑Terminals.

## 4) Netz‑Topologie
### 4.1 Logische Topologie & Segmente
- **VLANs/Zonen:** Praxis‑Clients, Server, Medizingeräte, Gast‑WLAN, Verwaltung, TI‑Zone.
- **Firewall‑Zonen/ACLs:** erlaubte Flüsse tabellarisch (Quelle → Ziel → Ports → Zweck → Owner).
- **Adressierung:** Subnetze, DHCP‑Scopes, Reservierungen.

### 4.2 Physische Topologie
- **Standortplan:** WAN‑Router, Firewall, Switches, Access‑Points, TI‑Konnektor‑Anschluss, Kartenterminals.
- **Redundanzen:** Internet‑Fallback (LTE), USV, Ersatz‑Konnektor/Terminal (falls).

### 4.3 Remote‑Zugriff
- **VPN/Jump‑Host**, MFA, Rollen, Protokollierung, zeitlich begrenzte Freischaltungen.

## 5) Datenflüsse (Swimlanes)
(Ein Diagramm pro Kernprozess, je 1 Seite)
- **eRezept:** PVS → QES(eHBA) → TI eRp‑Fachdienst → Apotheke.
- **eAU:** PVS → KIM → Krankenkasse.
- **ePA:** PVS ↔ TI ePA‑Dienst ↔ ePA der Kasse (Patientenfreigaben).
- **Doctolib‑Termin:** Patient/App ↔ Doctolib ↔ PVS (API/Webhook) → Praxis.
- **Druckausgabe:** PVS/Doctolib → OS‑Queues → definierte Fächer (Briefpapier/Blanko/Etikett).

## 6) Asset‑Inventar (Beispiel‑Tabelle)
| ID | Asset | Typ | Standort | Besitzer | Kritikalität | Verfügbarkeit | Patch‑Status | Backup |
|---|---|---|---|---|---|---|---|---|
| A‑01 | PVS‑Server | VM | RZ/Praxis | IT | hoch | 99,5% | aktuell | voll/täglich |
| A‑02 | TI‑Konnektor | Appliance | IT‑Rack | IT | hoch | 99,9% | FW x.y | n/a |
| A‑03 | Arzt‑PC 1 | Client | Zimmer 1 | Praxis | mittel | 98% | aktuell | Profil‑Backup |
| A‑04 | Kartenterminal 1 | Peripherie | Anmeldung | Praxis | hoch | 99,9% | FW ok | n/a |

## 7) Trust Boundaries & Schutzbedarf
- **Zonen:** Internet, Cloud (Doctolib), Praxisnetz, TI‑Zone.
- **Schutzbedarf personenbezogener/medizinischer Daten:** Vertraulichkeit **hoch**, Integrität **hoch**, Verfügbarkeit **mittel/hoch**.
- **Rechte/Identitäten:** eHBA (Person), SMC‑B (Praxis), KIM‑Adresse.

## 8) Risikobewertung (kompakt)
| Risiko | Ursache | Auswirkung | Ist‑Kontrolle | R(est) | Maßnahme |
|---|---|---|---|---|---|
| TI‑Ausfall | Konnektor defekt | eAU/eRezept nicht nutzbar | Ersatzverfahren, Hotline | M | 2. Konnektor/Spare‑Terminal |
| Falscher Druckschacht | Queue falsch | Fehlversand/Datenschutz | Testprofile, feste Queues | M | Schulung, Sperren von „Auto“ |
| KIM‑Störung | DNS/MTU/Provider | eAU verzögert | Monitoring, Echo‑Test | M | 2. KIM‑Provider/Retry |
| Datenabfluss | Compromised Client | DSGVO‑Verstoß | EDR, Least Priv., MFA | M | Härtung, Patch‑Mgmt |

Legende R(est): Niedrig/Mittel/Hoch.

## 9) Kontrollen (SoA‑Auszug)
- **Zugriff:** MFA, Rollen, least privilege, Admin‑Trennung.
- **Kryptografie:** TLS mind. 1.2 intern/extern; eHBA‑QES; SMC‑B‑Auth.
- **Netzwerk:** Segmentierung/VLAN, FW‑Regeln „deny‑all“ + allow‑lists.
- **Protokollierung:** zentrale Logs (Syslog/SIEM), Zeitserver/NTP, Aufbewahrung ≥ 6 Monate.
- **Endpoint:** EDR/AV, Device Control (USB), Härtung (CIS/BSI‑Empfehlungen).
- **Lieferanten/AV:** Verträge (Doctolib, KIM‑Provider, PVS), TOMs geprüft.

## 10) Verfahren & Runbooks
- **TI‑Ausfall/Ersatzverfahren:** Papier‑Workflow nach KV‑Vorgaben, spätere Nacherfassung.
- **KIM‑Fehlerleitfaden:** Echo‑Adresse, Zertifikatsprüfungen, MTU/DNS‑Fix, Fallback.
- **eHBA/SMC‑B gesperrt/verloren:** Meldeweg, Ersatzkarte, PIN‑Reset.
- **Patch‑/Change‑Fenster:** Wartungsfenster, Rollback‑Plan, Info an Praxis.

## 11) Backup/BCP/DR
- **Backup‑Klassen:** Voll/inkrementell, Retention, Offsite.
- **Wiederanlaufzeiten (RTO/RPO):** PVS, Files, Konfigurationen.
- **Testrestores:** 2×/Jahr protokolliert.

## 12) Monitoring & Kennzahlen
- **Verfügbarkeit:** Internet, TI‑Konnektor, KIM, PVS‑Dienste.
- **Security:** EDR‑Alarme, fehlgeschlagene Logins, Admin‑Sitzungen.
- **Druck:** Fehlerraten je Queue/Schacht.

## 13) Compliance‑Evidenzen (Checkliste)
- Konnektor‑Firmware/Release‑Notes dokumentiert.
- **KBV‑Liste**: aktivierte Module (eRezept, eAU, Video) gelistet.
- **KIM‑Test**: Echo‑Mail/Protokoll.
- **SMC‑B/eHBA** gültig (Ablaufdaten, PIN‑Dokumentation sicher).
- **AV‑Verträge/TOMs** (Doctolib, PVS, KIM‑Provider) abgelegt.

## 14) Anhänge/Vorlagen
- **Change‑Protokoll (Formblatt)**
- **Incident‑Report (Formblatt)**
- **Joiner‑Mover‑Leaver‑Liste**
- **Druck‑Queues‑Mapping** (Dokumenttyp → Queue/Schacht)
- **Netz‑Adressplan** (CIDR, Gateways, DHCP)

---

## 1‑Pager „ISA‑Summary“ (für Prüfung/Audit)
**Kontext:** Praxis mit PVS, TI (Konnektor/KIM), Doctolib (SaaS).
**Wesentliche Risiken:** TI‑Ausfall, Fehladressierung Druck, Endpunkt‑Kompromittierung.
**Top‑Kontrollen:** Segmentierung+FW, eHBA/SMC‑B‑basierte Auth, EDR+MFA, feste Druck‑Queues, AV‑Verträge geprüft.
**BCP:** Ersatzverfahren TI, Internet‑Fallback, tägliche Backups + getestete Restores.
**Compliance‑Evidenzen:** KBV‑Modul‑Liste, KIM‑Echo‑Protokoll, Karten‑Gültigkeiten, Change/Incident‑Nachweise.

---

### Hinweise zur Pflege
- Jede Änderung (neuer Drucker/VLAN/Provider) → **Change‑Protokoll**.
- Quartalsweise **Review** der Firewall‑Regeln & Queues.
- Halbjährlich **Restore‑Test** dokumentieren.

