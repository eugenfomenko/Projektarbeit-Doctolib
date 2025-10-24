**Architektur-Skizze: Doctolib ↔ Praxis/PVS ↔ TI/ KIM ↔ Kassen/Apotheke**

Überblick für Systemintegration in Arztpraxis/KMV – Fokus auf Termin/Kommunikation (Doctolib), Primärsystem (PVS) und TI-Workflows (eRezept/eAU/ePA).![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.001.png)

1) **Komponenten (High-Level)**

[Patient: Web/App]![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.002.png)

`      `│  (TLS/HTTPS)

`      `▼

[Doctolib SaaS]  ──────────────┐

`  `(Termin, Benachr., Video)   │ REST/API/Webhooks                                │

`                               `▼

`                        `[Praxisnetz]

`                          `│

`                          `▼

`                  `[PVS / Primärsystem] ────────────────┐                       │  (lokal/Client)                │

`                      `│                                 │

▼                                 │

`                 `[TI-Konnektor] —— [Kartenterminal]     │

`                      `│                                 │                       ├── KIM (TI-Mail) ────────────────┼──▶ [Krankenkassen (GKV/PKV)]

`                      `│                                 │        (eAU, Meldungen)

`                      `├── eRezept-Fachdienst ───────────┼──▶ [Apotheke]                       │                                 │        (Abholung eRp)

`                      `└── ePA-Fachdienst ───────────────┼──▶ [ePA-Instanz der Kasse]

Identitäten/Schlüssel: HBA (Arzt), SMC‑B (Praxis), KIM‑Adresse

**Rollen kurz:**  - **Doctolib**: Termin, Patientenkommunikation, Video; kann an PVS andocken. - **PVS**: medizinische Dokumentation, Abrechnung, TI-Workflows (eRezept/eAU/ePA) über Konnektor. - **TI**: sichere Netzinfrastruktur (KIM, Fachdienste), Policies durch gematik. - **Kassen**: ePA-Bereitstellung, Empfänger eAU; **Apotheken**: eRezept-Abholung.![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.003.png)

2) **Kernflüsse (vereinfacht)**
1) **Online-Termin (Patient → Doctolib → Praxis)**
1. Patient bucht in Doctolib (Fachgebiet/Slot/Anamnese).
1. Doctolib synchronisiert per API/Webhook mit PVS/Terminplan.
1. Praxis erhält Erinnerung/Anamnese; Patient bekommt Bestätigung + Reminder.
2) **eRezept (Praxis → TI → Apotheke)**
1. Arzt erstellt Verordnung im **PVS**.
1. QES mit **HBA**; PVS übergibt an **eRezept-Fachdienst** (TI).
1. Patient erhält Rezept-Token (App/Code); **Apotheke** löst über TI ein.
3) **eAU (Praxis → Kasse via KIM)**
1. PVS erzeugt eAU.
1. Versand via **KIM** über TI an **Krankenkasse** (GKV/PKV).
1. Arbeitgeber erhält separaten Datensatz durch Kasse.
4) **ePA-Zugriff (Praxis ↔ TI ↔ ePA der Kasse)**
1. Patient erteilt Rechte (ePA-App/Kasse).
1. Praxis greift über PVS/TI auf ePA-Dokumente zu (Protokollierung in TI).
5) **Videosprechstunde (Patient ↔ Doctolib ↔ Praxis)**
1. Doctolib stellt Video-Plattform; **KBV-zertifiziert** für vertragsärztliche Nutzung.
1. Medizinische Dokumentation/Abrechnung erfolgt im **PVS**.



|<p>**3) Trust Boundaries & Sicherheit**</p><p>- **Internetzone**: Patient ↔ Doctolib (HTTPS, 2FA optional, AV-Vertrag/DSGVO).</p><p>- **Praxisnetz**: Härtung Endpunkte, Rollen im PVS, zentrale Protokollierung.</p><p>- **TI-Zone**: Konnektor, KIM, Fachdienste; AuthN mit **HBA/SMC‑B**; gematik/BSI-Vorgaben.</p><p>**Schlüssel/Identitäten**  - **HBA**  (Heilberufsausweis): qualifizierte Signatur (QES) für eRezept/eAU etc. - **SMC‑B**: Institutionskarte der Praxis; Authentisierung ggü. TI. - **KIM-Adresse**: sichere TI-„Mail“ für eAU/ Kommunikation LErb ↔ Kassen.</p>|
| - |
|<p>**4) Schnittstellen & Integrationen**</p><p>- **Doctolib ↔ PVS**: Termin-/Patientenstammdaten, Anamneseformulare (API/Webhooks).</p><p>- **PVS ↔ TI**: Konnektorprotokolle, **KIM**, eRezept-/ePA-Fachdienste.</p><p>- **PVS ↔ Kassen**: v. a. über TI (KIM/ePA/eRp); Abrechnung über KV-Schnittstellen.</p>|
5) **Betriebs-Checkliste (kurz)**
- Karten & Zertifikate: HBA, SMC‑B, KIM-Adresse aktiv.
- Konnektor/Updates: aktuell, Zulassungen erfüllt, Logs überwachen.
- PVS: KBV-gelistete Module (eRezept, eAU, Video) aktiv & getestet.
- Doctolib: Rollen/Rechte, API-Anbindung, Reminder-Templates, Datenschutz/AV.
- Tests: eAU an Testkasse, eRezept Probe, ePA-Leseprobe, Video-Call Dry-Run.
- Notfallpfade: TI-Ausfall (Ersatzverfahren), Offline-Token, Backup-KIM.![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.004.png)
6) **Sequenz (eRezept) – Mini-Swimlane**

Patient    Doctolib      PVS           TI/eRp          Apotheke   |           |           |              |                |   | Termin →  |           |              |                |   |           |  Sync →   |              |                |![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.005.png)

`  `|           |           |  Verordnung  |                |   |           |           | —QES(HBA)→   |                |   |           |           |  eRp Upload →|                |   |  Token ←  |           |              |← eRp-Abholung  |

`  `|  Abholung |           |              |   (TI)         |

`  `|──────────▶|──────────▶|────────────▶ |──────────────▶ |![](Aspose.Words.3d66581b-c7e7-4a4a-a942-83b6965e991a.006.png)

**Hinweis**

TI- und KBV-Vorgaben sind maßgeblich für Zulassung/Abrechnung. Doctolib ergänzt den Praxis- Workflow, **PVS bleibt führend** für medizinische/abrechnungsrelevante TI-Prozesse.
3
