1) **Wer macht was – kurz & knackig** 
- **BMG (Bundesministerium für Gesundheit):** politische Leitplanken, Gesetze (z. B. SGB V, Digitalgesetze). 
- **gematik:** Architektur & Standards der **TI**, Zulassungen/Prüfungen von TI- Diensten/Komponenten, Roadmaps. 
- **BSI & BfDI (+ Landesdatenschutz):** Sicherheit (BSI) und Datenschutz (BfDI). 
- **KBV / KVen:** Regeln & Zulassungen für die vertragsärztliche Versorgung; Anforderungen an Praxis-/Primärsysteme für eRezept, eAU, ePA-Workflows etc. 
- **BAS (Bundesamt für Soziale Sicherung):** Aufsicht über die **gesetzlichen** Krankenkassen. 
- **GKV-Spitzenverband / PKV-Verband:** Vertretung der Kassen; GKV-SV für alle gesetzlichen, PKV-Verband für die privaten. 
2) **TI ↔ Kassen (GKV & PKV)** 
- **Alle**: TI ist die sichere Netzinfrastruktur für den Sektor (Praxen, Kliniken, Apotheken, Kassen). 
- **Kassen-Rolle:** betreiben/stellen die **ePA** für Versicherte bereit (über TI-Fachdienste und definierte Schnittstellen). 
- **GKV**: Teilnahme & Finanzierung von TI-Komponenten für Leistungserbringer sind detailliert im SGB V geregelt; Aufsicht: **BAS**. 
- **PKV**: nutzt TI technisch ebenfalls; ePA-Angebote und Erstattungs-/Finanzierungslogik laufen über PKV-Regelwerke; Vertretung: **PKV-Verband**. 
3) **TI ↔ KBV** 
- **KBV** legt (für die Vertragsärzte) fachliche/organisatorische Anforderungen fest und testet/zulässt relevante Praxis-Module (z. B. eRezept-Funktionalität im Primärsystem). 
- **gematik** kümmert sich um **TI-Spezifikationen** (z. B. KIM-Dienst, eRezept-Fachdienst, Identitäten, Konnektor-/SMC-B/Kartenterminals etc.). 
- Ergebnis: Ein Praxis-/Kliniksystem muss **beides** erfüllen: gematik-TI-Vorgaben **und** (wo einschlägig) KBV-Anforderungen. 
4) **Wo passt Doctolib hinein?** 
- **Unternehmen / Praxissoftware & Services:** Terminmanagement, ggf. Praxismanagement, Videosprechstunde, Patienten-Apps/Portale. 
- **An TI angebunden?** 
- Wenn Doctolib (oder ein integriertes Praxis-Primärsystem) **TI-pflichtige Funktionen** anbietet (z. B. eRezept-Workflows, eAU-Versand, ePA-Zugriffe, Kommunikation per **KIM**), muss es die **gematik-Spezifikationen** erfüllen und – in der vertragsärztlichen Versorgung – die **KBV-Zulassungen/Listen** für die jeweiligen Module bestehen. 
- Für **Videosprechstunden** brauchen Anbieter die **KBV-Zertifizierung** für die vertragsärztliche Abrechnung. 
- Für **Kommunikation** mit anderen Leistungserbringern/den Kassen kann Doctolib (oder das angebundene PVS) **KIM** nutzen (TI-Dienst für sichere E-Mail). 
- **Zu den Kassen:** Doctolib rechnet nicht „als Kasse“ ab; es stellt Funktionen bereit, die den Ärzten helfen, **Kassen-Workflows** korrekt zu bedienen (Terminvermittlung, eRezept- Erstellung im PVS, eAU-Versand via KIM, ePA-Zugriffe gemäß Einwilligung des Versicherten). Die **fachliche Hoheit** über Ansprüche/Abrechnung liegt weiterhin bei Arzt/Kasse (GKV oder PKV). 
5) **Typische Daten-/Ablaufbeispiele** 
- **eRezept in der Praxis:** 

  Arzt in Praxissoftware → qualifizierte Signatur (HBA) → **eRezept-Fachdienst (TI)** → Apotheke ruft Rezept ab. 

  *Wer „passt auf“?* gematik (Spezifikationen/Tests), KBV (vertragsärztliche Module), BSI/BfDI (Sicherheit/Datenschutz). 

- **eAU:** 

  Praxis → **KIM** über TI → Krankenkasse (GKV/PKV) → Arbeitgeber erhält separaten Datensatz. 

- **ePA-Zugriff:** 

  Patient steuert Freigaben (App/ePA) → Praxis greift über TI-Dienste zu → Protokollierung über TI-Mechanismen. 

- **Doctolib-Termin → Praxis-Workflow:** 

  Patient bucht → Doctolib synchronisiert mit Praxis/PVS → in der Sprechstunde nutzt der Arzt die TI-Funktionen (eRezept/eAU/ePA) im **zertifizierten** Primärsystem; Doctolib kann – je nach Setup – Funktionen integrieren/andocken, muss dann die jeweiligen **Zulassungen** haben. 

6) **Merkhilfe (superkurz)** 
- **BMG**: Politik & Gesetze. 
- **gematik**: TI-Regeln & Tests. 
- **KBV**: Vertragsärztliche Anforderungen/Zulassungen. 
- **BAS**: Aufsicht GKV; **GKV-SV / PKV-Verband**: Vertretung. 
- **BSI/BfDI**: Sicherheit/Datenschutz. 
- **Doctolib**: Praxis-Service/Software, **kein** Kostenträger; muss TI/KBV-Vorgaben erfüllen, wenn TI-Funktionen betroffen sind. 
