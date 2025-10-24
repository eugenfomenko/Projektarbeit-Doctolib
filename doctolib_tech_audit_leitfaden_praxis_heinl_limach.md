# Doctolib Tech‑Audit – Schritt‑für‑Schritt‑Leitfaden (für Einsteiger)

> Ziel: Eine klare, reproduzierbare Vorgehensweise, um **TI‑Konformität**, **Netzwerksicherheit** und **System‑/Geräte‑Inventar** einer Arztpraxis zu prüfen, die **Doctolib Praxissoftware (PVS)** installieren bzw. migrieren will. Der Leitfaden erklärt jeden Begriff, liefert Checklisten und zeigt, wie man aus vorhandenen Dateien (Excel/Logdateien) **eine chronologische Ereigniskette** und **eine Netzwerkübersicht** erstellt.

---

## 1. Vorbereitung & Begriffe (Glossar)

- **PVS (Praxisverwaltungssystem):** Die Software zur Verwaltung von Patienten, Terminen, Abrechnung usw. (hier: Doctolib PVS oder Migration dorthin).
- **TI (Telematikinfrastruktur):** Sichere Gesundheits‑Netzinfrastruktur in Deutschland, über die eGK, eAU, eRezept etc. laufen.
- **Konnektor:** Sicherheitsgateway in die TI (steht meist im Praxisnetz; hat eigene IP).
- **KIM (Kommunikation im Medizinwesen):** Sichere E‑Mail‑Dienste innerhalb der TI.
- **eHBA / SMC‑B:** Elektronische Heilberufsausweise bzw. Praxis‑Institutionskarten für Authentisierung/Signatur.
- **GDT (Geräte‑Datenträger‑Schnittstelle):** Standard, mit dem Diagnosegeräte (z. B. EKG) Daten ans PVS liefern.
- **ISA (Informations‑Sicherheits‑Architektur):** Strukturierte Darstellung der Schutzmaßnahmen (Firewall, VLAN, Rollen, Backup usw.).
- **ZVT:** Protokoll zur Anbindung von EC‑Kartenterminals.
- **Direktdruck:** Druckt ohne Dialog direkt auf definierten Drucker/Schacht – wichtig für eAU, Rezepte, Etiketten.

> **Unterlagen bereitlegen:** Zugang zum Router/Firewall, Switch‑Übersicht, ggf. VLAN‑Plan, Konnektor‑Dokumentation, Geräte‑/Druckerlisten, Logbücher, Excel‑Inventar, Verträge (Internet, Payment).

---

## 2. Audit‑Fahrplan (Überblick)

1) **TI‑Konformität prüfen**  
2) **Internet & Perimeter** (Router, Firewall, VPN) prüfen  
3) **Netzwerkinfrastruktur (ISA) erfassen**  
4) **Konnektor & TI‑Peripherie** (IP, Zertifikate, Kartenleser) bestimmen  
5) **PVS‑Datenbankserver & Pfade** ermitteln  
6) **Geräte‑Inventar** (Computer, Diagnose, Drucker, EC, etc.) klassifizieren  
7) **Direktdruck & GDT** Konfiguration prüfen  
8) **Sicherheitsmaßnahmen** (AV/EDR, Patch, Backup, Rechte) bewerten  
9) **Chronologische Ereigniskette** aus Dateien/Logs rekonstruieren  
10) **Netzwerk‑Gesamtstruktur** visualisieren  
11) **Ergebnis‑Checkliste & To‑Dos** ableiten

---

## 3. TI‑Konformität – Checkliste

- **Konnektor Status**: Betriebsbereit, aktuelle Firmware, gültige Zertifikate?  
- **eHBA/SMC‑B**: Gültig, PIN bekannt, Kartenleser funktionsfähig?  
- **KIM**: Konto aktiv, Client/Connector‑Anbindung getestet (Senden/Empfangen).  
- **Zeitdienste**: NTP korrekt (wichtig für Signaturen).  
- **Protokolle**: TI‑Logs ohne kritische Fehler.

**Nachweis/Erfassung:** Konnektor‑Weboberfläche Screenshots, IP/Seriennummer, Firmwarestand, Logauszug.

---

## 4. Internetanbindung & Perimeter

- **Zugang**: Anschlussart (VDSL/Glasfaser/LTE), Bandbreite, Provider, Vertrags‑SLA.  
- **Router/Firewall**: Hersteller/Modell, Firmware, NAT/Portfreigaben, VPN (z. B. für Remote‑Support).  
- **DNS/NTP**: Vertrauenswürdige Resolver, Zeitquellen.  
- **Segmentierung**: Praxis‑LAN, Gäste‑WLAN, IoT/Diagnose getrennt? (VLANs)

**Ergebnisartefakte:** Export/Backup der Firewall‑Konfig, Netzplan, Liste der aktiven Port‑Forwards.

---

## 5. Netzwerkinfrastruktur (ISA)

- **Topologie**: Router → Firewall → Core‑Switch → Access‑Switches → Endgeräte.  
- **Adressierung**: IP‑Netze/VLANs (z. B. Praxis‑LAN 192.168.10.0/24, TI‑Segment 192.168.20.0/24).  
- **DHCP/DNS**: Wer vergibt Adressen? Reservierungen für Konnektor/Server.  
- **WLAN**: SSIDs, Verschlüsselung, Controller.  
- **Monitoring/Logging**: Syslog, Netflow, SNMP.

**Vorlage (ausfüllen):**  
| Segment | VLAN | Netz | Gateway | DHCP | Bemerkung |
|---|---:|---|---|---|---|
| Praxis‑LAN | 10 | 192.168.10.0/24 | 192.168.10.1 | Firewall |  |
| TI‑/Konnektor | 20 | 192.168.20.0/24 | 192.168.20.1 | Static |  |
| Diagnose/GDT | 30 | 192.168.30.0/24 | 192.168.30.1 | DHCP |  |
| Gäste‑WLAN | 99 | 192.168.99.0/24 | 192.168.99.1 | DHCP |  |

---

## 6. Konnektor & TI‑Peripherie ermitteln

- **Konnektor IP** (statisch), **Hostname**, **Firmware**, **Seriennr.**  
- **Kartenleser** (eGK): Modell, USB/Netz, Firmware, Arbeitsplatz‑Zuordnung.  
- **KIM‑Client**: Konto, Zertifikate, Testmail durchführen.  

**Vorlage (ausfüllen):**  
| Komponente | IP/Anschluss | Standort | Firmware | Status |
|---|---|---|---|---|
| Konnektor | 192.168.20.10 | Serverraum | x.y.z | OK |
| eGK‑Leser 1 | USB/Client01 | Anmeldung | a.b.c | OK |

---

## 7. PVS‑Datenbankserver & Pfade

- **Server/Instanz**: Hostname/IP, OS, Version, CPU/RAM.  
- **DB‑Engine & Pfad**: z. B. PostgreSQL/MSSQL – Daten‑ und Backup‑Pfad.  
- **Freigaben**: UNC‑Pfade (\\Server\Freigabe), Zugriffsrechte (NTFS/Share).  

**Vorlage (ausfüllen):**  
| Server | Rolle | IP | DB‑Engine | DB‑Pfad | Backup‑Pfad |
|---|---|---|---|---|---|

---

## 8. Geräte‑Inventar klassifizieren (1–11)

Nutzen Sie die Excel‑Inventardaten. Ordnen Sie jedes Gerät einer Kategorie zu:

1. **Computer** (Clients/Server)  
2. **Laboranbindung** (LIS/GDT‑Exports)  
3. **Diagnosegeräte** (EKG, Sono, Spirometrie …)  
4. **Drucker** (Laser, MFP, Etikett)  
5. **Kartenleser** (eGK)  
6. **EC Kartenleser** (ZVT/SumUp/Payone)  
7. **Telematik** (Konnektor, KIM)  
8. **IT‑Sicherheit** (AV/EDR, Patch, Backup)  
9. **Internet** (Router/Provider)  
10. **Netzwerk** (Switches, APs, NAS)  
11. **Weiteres** (alles Übrige)

**Tabelle (aus Excel ableiten):**  
| Bezeichnung | Kategorie | IP | Standort | Anschlüsse | Bemerkung |
|---|---|---|---|---|---|

---

## 9. GDT‑ & Direktdruck‑Konfiguration

- **GDT**: Prüfen, welche Geräte Daten liefern, GDT‑Ordner (Import/Export‑Pfad), Rechte, Dateinamenmuster, Mapping im PVS.  
- **Direktdruck**: Pro Arbeitsplatz definierte Standarddrucker/Schächte (Rezept A6, Etikett, A4). Testdrucke dokumentieren.

**Vorlage:**  
| Arbeitsplatz | Anwendung | Drucker | Schacht/Format | Test OK |
|---|---|---|---|---|

---

## 10. Sicherheitsmaßnahmen (IT‑Sicherheit)

- **Endpoint‑Schutz**: AV/EDR aktiv, zentrale Verwaltung.  
- **Patch‑Management**: OS/Anwendungen aktuell, Zeitplan.  
- **Backup & Recovery**: 3‑2‑1‑Regel, tägliche Prüf‑Restore, Protokoll.  
- **Rechte & Admin**: Least Privilege, MFA für Remote, starke Passwörter.  
- **Protokollierung**: Ereignisanzeige, Syslog, Alarme.

**Vorlage:**  
| Maßnahme | Tool/Prozess | Status | Nachweis |
|---|---|---|---|

---

## 11. Chronologische Ereigniskette aus Dateien

**Ziel:** Nachvollziehen, wann Geräte installiert/geändert wurden (z. B. aus Excel/Logs).  
**Vorgehen:**  
1. **Datumsfelder** in Excel erkennen (Installiert/Änderung/Letzte Wartung).  
2. **Kontext** der Zeile als Kurzbeschreibung übernehmen.  
3. **Sortieren nach Datum** → Timeline.  
4. **Auffälligkeiten** markieren (z. B. viele Änderungen an einem Tag).  

**Tabelle:**  
| Zeitpunkt | Quelle | Feld | Kontext |
|---|---|---|---|

---

## 12. Netzwerk‑Gesamtstruktur (How‑to visualisieren)

- **Inventar → Knoten:** Router, Firewall, Switches, Server, Konnektor, Clients, Drucker, Diagnose.  
- **IP/VLANs → Kanten:** Verbinden Sie nach Segmenten (z. B. VLAN 10 = Praxis‑LAN).  
- **Notation:** Rechteck = System, Wolke = Internet/TI, Pfeile = Richtungen (optional).  
- **Tipp:** Starten Sie grob (Perimeter → Core → Access → Endgeräte) und verfeinern nach Bedarf.

---

## 13. Ergebnis‑Checkliste & To‑Dos

- **Alle Pflichtpunkte TI erfüllt?** (Signaturen, KIM, Kartenleser)  
- **Netzwerk sauber segmentiert?** (VLAN/Gäste/Diagnose)  
- **Sicherheits‑Baseline erfüllt?** (AV, Patch, Backup, MFA)  
- **GDT/Druck** getestet und dokumentiert?  
- **Migrationsplan PVS** (Downtime, Fallback, Backup verifiziert) erstellt?

**To‑Do‑Liste:**  
- [ ] Offene Punkte aus Checklisten schließen  
- [ ] Verantwortliche & Termine zuweisen  
- [ ] Abschlussbericht mit Netzplan, Inventar, Ereigniskette ablegen

---

### Anhang: Mini‑Glossar

- **VLAN**: Virtuelles LAN, logische Netztrennung auf Switch‑Ebene.  
- **NAT**: Network Address Translation, interne IPs → öffentliche IP.  
- **UTM**: Unified Threat Management (Firewall mit Zusatzfunktionen).  
- **EDR**: Endpoint Detection & Response (angereicherte Endpoint‑Security).  
- **3‑2‑1‑Backup**: 3 Kopien, 2 Medien, 1 Offsite.

> **Nächster Schritt:** Nutzen Sie die bereitgestellten Excel‑Auszüge (Inventar, IP‑Funde, Ereigniskette), um die Vorlagen **konkret** für die Praxis Heinl/Limach auszufüllen und anschließend den Netzplan zu zeichnen.

