# Doctolib Tech‑Audit – Lernprojekt

> Ziel: Eine Arztpraxis von der Planung bis zum Go‑Live auditieren, dokumentieren und migrieren. Diese Vorlage führt dich Schritt für Schritt – inkl. Tabellen, Definitionen und Checklisten – und bildet eine **chronologische Ereigniskette** ab.

---

## 1) Mini‑Glossar (einfache Worte)
- **TI (Telematikinfrastruktur):** Sicheres Netz des Gesundheitswesens in DE.
- **Konnektor:** „TI‑Modem“ der Praxis; verbindet lokal zur TI.
- **SMC‑B / HBA:** Praxiskarte / Heilberufsausweis für Authentisierung/Signatur.
- **KIM:** Sichere E‑Mail in der TI (Arzt‑zu‑Arzt, etc.).
- **DDV:** Lokale Doctolib‑Komponente für Geräte/TI/Druck.
- **GDT:** Austauschformat zwischen PVS und Medizingeräten.
- **Direktdruck (IPP/PDF):** Druck direkt an definierte Drucker/Schächte.

---

## 2) Praxis‑Inventur (Bestandsaufnahme)
**Ziel:** Alle Geräte, Anschlüsse und Rollen erfassen. Diese Tabelle ist die Basis für TI‑, Druck‑ und GDT‑Konfiguration.

| Standort/Raum | Gerätetyp | Hersteller/Modell | Anschluss (LAN/USB/WLAN) | IP/Adresse | Rolle/Zweck | Inventar‑ID | Notizen |
|---|---|---|---|---|---|---|---|
| Empfang | PC‑Arbeitsplatz |  | LAN |  | Anmeldung |  |  |
| Empfang | eGK‑Terminal |  | USB→PC / LAN |  | Kartenlesen (eGK/KVK) |  |  |
| B1 | Drucker A4 |  | LAN |  | Formulare/Rezepte |  | Schacht 1/2 Zuordnung |
| Technik | Konnektor |  | LAN |  | TI‑Gateway |  | Port/Verkabelung |
| Labor | Diagnosegerät |  | USB→Client / LAN |  | Befunde (GDT) |  | Dateipfade |

**Nomenklatur (Beispiel):** RCP‑EMP‑01 (PC Empfang), PRN‑B1‑01 (Drucker B1), CT‑KONN‑01 (Konnektor), SW‑01 (Switch).

---

## 3) Netzwerk‑Skizze (Topologie & ISA)
**Ziel:** Überblick über Internet → Firewall/Router → Switches → Endgeräte.

```
Internet → Router/Firewall → Switch(core) → PCs / Drucker / Konnektor / eGK‑Terminals / Laborgeräte
```

**IP‑Segmente (Beispiel):**
- Praxis‑LAN: 192.168.10.0/24
- Geräte‑VLAN (optional): 192.168.20.0/24

**ISA (Informationssicherheits‑Aspekte):**
- Firewall‑Regeln (eingehend/ausgehend)
- VPN (Fernwartung)
- Patch‑Management, Backup, Rollen/Rechte

---

## 4) TI & Kartenleser
**Konnektor‑Daten:** Host/IP, Port, Zertifikate, Firmware.

| Feld | Wert |
|---|---|
| Hersteller/Modell |  |
| IP/Hostname |  |
| Port(e) |  |
| Standort |  |
| SMC‑B (Praxis) | Seriennr. / Slot |
| HBA (Ärzt:innen) | Zuordnung je Arbeitsplatz |

**Terminal‑Mapping:** Arbeitsplatz ↔ Kartenleser (USB/LAN, Port, Treiberstand).

---

## 5) Direktdruck‑Matrix
**Ziel:** Dokumententyp → Drucker → Schacht/Einzug.

| Dokumententyp | Druckername | IP/Queue (IPP) | Einzug/Format | Bemerkung |
|---|---|---|---|---|
| AU | PRN‑B1‑01 | ipp://192.168.10.25/ipp/print | Schacht 2 | Gelbes Papier |
| Rezept | PRN‑EMP‑01 | ipp://192.168.10.26/ipp/print | Schacht 2 | Rezeptrolle |
| Überweisung | PRN‑B1‑01 |  | Schacht 1 | Blanko |

---

## 6) GDT‑Anbindung (Medizingeräte)
**Ziel:** Import/Export‑Pfade und Testfälle definieren.

| Gerät | Typ | Anschluss | Export‑Pfad (Aufträge) | Import‑Pfad (Befunde) | Dateiformat | Test OK? |
|---|---|---|---|---|---|---|
| EKG | GDT | USB→Client | C:\\GDT\\OUT | C:\\GDT\\IN | PDF/GDT |  |

---

## 7) Chronologische Ereigniskette (Projektlogbuch)
**Ziel:** Von Planung bis Go‑Live in nachvollziehbaren Schritten.

| Datum | Phase | Ereignis/Task | Verantwortlich | Ergebnis/Artefakt |
|---|---|---|---|---|
| T‑21 | Planung | Kick‑off, Zieldefinition | PM | Protokoll |
| T‑14 | Audit | Inventur abgeschlossen | Tech | Asset‑Liste |
| T‑10 | Netz | Topologie/ISA dokumentiert | Tech | Netz‑Skizze |
| T‑7 | TI | Konnektor/Terminals konfiguriert | Tech | TI‑Blatt |
| T‑5 | Druck | Direktdruck‑Matrix getestet | Tech | Testprotokoll |
| T‑3 | GDT | Geräteimporte getestet | Tech | Befund‑Beispiel |
| T‑1 | Migration | Downtime‑Plan/Backup | PM/Tech | Plan/Checkliste |
| T | Go‑Live | Abnahme | Praxisleitung | Abnahmeprotokoll |

---

## 8) Checklisten (Kurzform)
- **TI‑Konformität:** Karten/Slots, Zertifikate, Firmware, KIM.
- **Internet & Sicherheit:** Bandbreite, Router/Firewall, VPN, Updates.
- **Netzwerk (ISA):** Segmente/VLANs, IP‑Plan, DNS/DHCP, Logging.
- **Geräte:** PCs, Drucker (IPP), Kartenleser, Labor/Diagnose.
- **Druck:** Dokumententypen, Schachtzuordnung, Testausdrucke.
- **GDT:** Pfade, Dateiformate, Round‑Trip‑Test.
- **Migration:** Datenpfade PVS, Backup, Fallback, Abnahme.

> Tipp: Nach jedem Abschnitt eine Mini‑Probe (1–2 Tests) dokumentieren.

