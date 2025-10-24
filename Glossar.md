**Doctolib** – Online-Plattform für Arztpraxen. Ermöglicht u. a. Online-Terminbuchung durch Patient\*innen und verbindet sich über Schnittstellen mit der Praxis-IT, um Abläufe zu automatisieren und Telefonzeit zu sparen. 

**PVS – Praxisverwaltungssoftware** – Herzstück der Praxis-IT. Verwalten von Patient\*innen, Terminen, Abrechnung und Befunden. Doctolib greift über Standardschnittstellen auf das PVS zu bzw. tauscht Daten aus. 

**TI – Telematikinfrastruktur** – Geschütztes, bundesweites Gesundheitsnetz. Darüber laufen sichere Fachanwendungen wie E-Rezept, elektronische Patientenakte und KIM. PVS und (künftig) Doctolib- Module docken daran an. 

**TI-Konnektor** – Zertifizierter Router in der Praxis, der die sichere Verbindung zur TI herstellt. Bindet das PVS ans Gesundheitsnetz an und authentifiziert Vorgänge mit Praxis-/Arztkarten. 

**TI-Gateway (TI 2.0)** – Cloud-basierter Nachfolger/Ersatz für den lokalen Konnektor. Ziel: sichere TI- Anbindung ohne eigenen TI-Router in der Praxis, weniger Wartungsaufwand. 

**E-Rezept (elektronisches Rezept)** – TI-Anwendung zum digitalen Verordnen. Rezepte werden elektronisch erstellt, qualifiziert signiert und z. B. als QR-Code eingelöst statt auf Papier. 

**ePA – elektronische Patientenakte** – TI-Anwendung; dient als zentraler, von Patient\*innen kontrollierter Speicher für gesundheitsbezogene Daten. Geplante Anzeige/Integration in „Doctolib Praxis“. 

**eGK – elektronische Gesundheitskarte** – Chipkarte der gesetzlich Versicherten. Wird im Kartenterminal eingelesen und liefert Daten für das VSDM (Gültigkeitsprüfung der Versicherung). 

**Kartenterminal (Kartenlesegerät)** – Gerät zum Einlesen von Chipkarten (eGK, eHBA, SMC-B). Voraussetzung für VSDM, E-Rezept-Signatur u. a. TI-Fachanwendungen. 

**VSDM – Versichertenstammdaten-Management** – Pflichtdienst in der TI. Beim Einlesen der eGK wird online geprüft, ob Versicherungsdaten gültig/aktuell sind. 

**KIM – Kommunikation im Medizinwesen** – Sicherer E-Mail-Dienst innerhalb der TI. Dient z. B. zum Versand von Arztbriefen und Befunden zwischen Leistungserbringern, als Ersatz für Fax. 

**eHBA – elektronischer Heilberufsausweis** – Persönliche Chipkarte von Ärztinnen/Ärzten (und anderen Heilberufen). Ermöglicht die qualifizierte elektronische Signatur (z. B. E-Rezept) und den Zugriff auf TI-Dienste. 

**SMC-B – Security Module Card Typ B (Institutionskarte)** – Chipkarte der Praxis/Betriebsstätte. Weist die Institution in der TI aus und wird zusammen mit dem eHBA genutzt. 

**HL7 – Health Level 7** – Internationaler Standard für Austausch/Struktur medizinischer Daten (z. B. Patienten-, Befund-, Auftragsdaten) zwischen Softwaresystemen. 

**GDT – Geräteschnittstelle Datentransfer** – In Deutschland verbreitete, einfache Standardschnittstelle zur Anbindung von Medizin-/Diagnosegeräten an Praxissoftware (z. B. Messwerte übernehmen). 

**FHIR – Fast Healthcare Interoperability Resources** – Moderner HL7-Standard (meist REST/JSON) für strukturierte, interoperable Gesundheitsdaten. Erleichtert Integration zwischen PVS, Doctolib- Diensten und externen Systemen. 

**Doctolib Praxis (Cloud-PVS)** – Doctolib-eigene, cloudbasierte All-in-One-Praxissoftware (geplanter Start: Herbst 2025). Bündelt Terminbuchung, medizinische Dokumentation und TI-Funktionen in einer Lösung. 

— 

Краткое резюме 

Doctolib — платформа для клиник, связанная со **ПВС** (система управления практикой) через стандарты **HL7/GDT/FHIR**. Безопасные сервисы работают через **TI** (телемедицинская инфраструктура): **eRezept**, **ePA**, **KIM**, **VSDM**. Подключение делается через **TI-коннектор** или облачное **TI-шлюз (TI 2.0)**. Карты **eGK**, **SMC-B** и **eHBA** используются для идентификации и квалифицированной электронной подписи. **Doctolib Praxis** — облачное ПВС, объединяющее запись, документацию и TI-функции. 

**TI – Telematikinfrastruktur** – Sicheres Gesundheitsnetz in Deutschland. Verbindet Praxen, Krankenkassen und Patient:innen. Basis für digitale Fachanwendungen wie elektronische Patientenakte (ePA), elektronisches Rezept (eRezept) und Kommunikation im Medizinwesen (KIM). 

**Konnektor (TI-Konnektor)** – „TI-Modem“ in der Praxis. Stellt die geschützte Verbindung zur TI her. In Doctolib wird er mit Host/IP, Port (meist 443) und Zertifikaten hinterlegt. 

**eGK / KVK – elektronische Gesundheitskarte / Krankenversichertenkarte** – Chipkarte der Versicherten. Wird am Kartenterminal gelesen; die eGK liefert u. a. Daten für VSDM (Gültigkeitsprüfung). 

**HBA – Heilberufsausweis (eHBA)** – Persönliche Chipkarte der Ärztin/des Arztes. Dient der qualifizierten elektronischen Signatur (QES) und der Authentisierung in TI-Prozessen. 

**SMC-B – Security Module Card Typ B (Betriebsstättenkarte)** – Institutionskarte der Praxis. Authentisiert die Betriebsstätte in der TI; wird zusammen mit eHBA im Kartenterminal genutzt. 

**PVS / EHR – Praxisverwaltungssystem / Elektronische Gesundheitsakte der Praxis** – Führende Praxissoftware (z. B. Dokumentation, Abrechnung, Termine) mit TI-Anbindung. Im Doctolib-Kontext ergänzt durch die lokale Doctolib-Desktop-Komponente (DDV) für Geräte-/Druck-/Dateifunktionen. 

**KIM – Kommunikation im Medizinwesen** – Sicherer E-Mail-Dienst innerhalb der TI, z. B. für Arzt-zu- Arzt-Kommunikation oder eAU-Versand an Krankenkassen. 

**GDT – Geräte-Datentransfer** – Deutscher Standard für den Datenaustausch zwischen Praxissoftware und Medizin-/Diagnosegeräten (Aufträge hinaus, Befunde hinein). 

**Direktdruck / IPP – Internet Printing Protocol** – Direktes Senden von PDFs an kompatible Netzwerk- oder USB-Drucker; IPP ist das zugrunde liegende Druckprotokoll. 

**(n)BSNR / NBSNR – (Neben-)Betriebsstättennummer** – Kennzeichen der Praxisstandorte. Die SMC-B ist auf die jeweilige (Neben-)Betriebsstätte ausgestellt; jeder Standort benötigt i. d. R. eigene SMC-B und eigene KIM-Adresse. TI-Datensätze (VSDM, eRezept, eAU) müssen die korrekte (n)BSNR des behandelnden Standortes tragen. Im PVS sorgt der **Mandant** dafür, dass Formulare, Druckköpfe, Absenderdaten, KIM-Absender und Abrechnung zum richtigen Standort passen. 

**KIM-Echo-Protokoll** – Test-/Nachweisfunktion: Versand einer Nachricht an eine Echo-Adresse, um KIM-Postfach und Versandweg zu prüfen und zu protokollieren. 

**VSDM – Versichertenstammdaten-Management** – Online-Prüfung und Aktualisierung der Versichertenstammdaten über die TI, i. d. R. beim ersten Quartalskontakt. 

**eRezept (eRp)** – Elektronisches Rezept. Wird mit eHBA qualifiziert signiert und über TI bereitgestellt; Einlösung in der Apotheke (z. B. via QR-Code). 

**eAU – elektronische Arbeitsunfähigkeitsbescheinigung** – Digitale AU. Versand i. d. R. per KIM an die Krankenkasse. 

**ePA – elektronische Patientenakte** – Von den Krankenkassen bereitgestellte, patientengeführte Akte. Zugriffe erfolgen über die TI und werden von Patient:innen freigegeben. 

**Doctolib** – Plattform für Online-Terminbuchung, Kommunikation und Video. Kein Kostenträger und kein Ersatz der TI; dockt über Schnittstellen ans PVS an. 

**DDV – Doctolib Desktop Version** – Lokale Doctolib-Bridge/App für Druck- und Datei-Handling. Nutzt die Betriebssystem-Druckwarteschlangen; keine eigene TI-Funktion. 

**HL7 v2 / CDA / FHIR** – Interoperabilitäts-Standards: HL7 v2 für Nachrichten, CDA (Clinical Document Architecture) für strukturierte Dokumente, FHIR für ressourcenbasierte Web-APIs (meist JSON/REST). In Deutschland breit in ePA/eRezept-Projekten verwendet. 

**FHIR (HL7 FHIR)** – Moderner HL7-Standard mit modularen „Resources“ (Patient, Encounter, Observation etc.) und Profilen; erleichtert interoperable Integrationen. 

**DICOM – Digital Imaging and Communications in Medicine** – Standard für medizinische Bilder (z. B. Radiologie) inkl. Metadaten-Struktur. 

**PACS – Picture Archiving and Communication System** – Bildarchiv- und Kommunikationssystem für DICOM-Daten; Speichern, Abrufen und Verteilen von Bildstudien. 

**CIDR – Classless Inter-Domain Routing** – Schreibweise für IP-Netze/Subnetze, z. B. 192.168.20.0/24. 

**Netzsegmentierung & Firewall (FW)** – Sicherheitsprinzip „Segmentieren und minimieren“: VLANs/Zonen trennen Systeme, Firewalls lassen nur benötigte Verbindungen zu („deny-all, allow- needed“), z. B. nur PVS ↔ Konnektor. 

**Direktdruck-/Queue-Mapping** – Feste Zuordnung von Dokumenttypen zu Drucker-Queues und Schächten (z. B. AU-Formular → Drucker „A4\_Blanko“, Schacht 1). 

**EDR – Endpoint Detection & Response** – Sicherheitstechnologie zur Erkennung und Reaktion auf Bedrohungen am Endgerät (Verhaltensanalyse, Isolierung, Forensik). 

**CIS – Center for Internet Security** – Organisation mit Härtungs-Benchmarks (z. B. CIS Windows 10 Level 1) für sichere Systemkonfigurationen. 

**KV-Vorgaben** – Regeln/Verfahren der Kassenärztlichen Vereinigungen, z. B. Ersatzverfahren bei TI- Ausfall oder Dokumentationspflichten. 

**KBV-Modul-Liste** – Nachweis, welche PVS-Module KBV-zugelassen und in der Praxis aktiviert sind (etwa eRezept, eAU, Videosprechstunde). 

**AV-Vertrag & TOMs – Auftragsverarbeitungsvertrag & Technisch-Organisatorische Maßnahmen** – DSGVO-Verträge nach Art. 28/32 mit Dienstleistern (z. B. PVS-Hoster, Doctolib, KIM-Provider) inkl. Beschreibung der Sicherheitsmaßnahmen. 

**ISA – Information Security Assessment** – Kompakte Sicherheitsbewertung/-Selbstaudit (z. B. nach VDA-ISA/TISAX oder als praxisinterne ISA-Zusammenfassung). 

**Behörden & Verbände – Überblick** 

**BMG – Bundesministerium für Gesundheit** – Verantwortlich für Gesundheitsgesetze und Strategie (z. B. SGB V, Digitalgesetze). 

**gematik** – Legt Vorgaben/Standards der TI fest und lässt TI-Dienste/Komponenten zu. 

**BSI – Bundesamt für Sicherheit in der Informationstechnik** – Setzt IT-Sicherheitsvorgaben (Kryptografie, Protokolle). 

**BfDI – Bundesbeauftragter für den Datenschutz und die Informationsfreiheit** – Datenschutzaufsicht des Bundes; in den Ländern: Landesdatenschutzbehörden. 

**KBV – Kassenärztliche Bundesvereinigung** – Regelt und zertifiziert vertragsärztliche IT-Module (z. B. Video, eRezept/eAU). 

**KVen – Kassenärztliche Vereinigungen** – Regionale Umsetzung, Abrechnung, Prüfungen. 

**BAS – Bundesamt für Soziale Sicherung** – Aufsicht über die gesetzliche Krankenversicherung (GKV). **GKV-Spitzenverband** – Dachverband der gesetzlichen Krankenkassen. 

**PKV-Verband** – Verband der privaten Krankenversicherer. 

**BaFin – Bundesanstalt für Finanzdienstleistungsaufsicht** – Finanzaufsicht; u. a. zuständig für PKV- Unternehmen. 

**Krankenkassen & Mitgliedschaft – Überblick** 

**GKV – Gesetzliche Krankenversicherung** – Pflicht- oder freiwillige Mitgliedschaft (über/unter JAEG); unter Aufsicht des BAS. 

**PKV – Private Krankenversicherung** – Private, vertragliche Absicherung; Aufsicht durch BaFin. **Freiwillige GKV-Mitgliedschaft** – Möglichkeit, trotz Wegfall der Versicherungspflicht in der GKV zu bleiben; Beiträge abhängig vom Einkommen mit Mindest-/Höchstgrenzen. ![](Aspose.Words.94c12318-e002-47e8-b271-d765681e932e.001.png)

Краткое резюме 

Это расширенный глоссарий по инфраструктуре клиники и TI. Охватывает TI, коннектор, карты **eHBA/SMC-B/eGK**, сервисы **KIM, VSDM, eRezept, eAU, ePA**, роль **PVS/Doctolib/DDV**, стандарты **HL7/FHIR/CDA/DICOM/PACS/GDT**, сетевые и печатные концепции (**CIDR**, сегментация, **IPP**, очереди печати), безопасность (**EDR**, **CIS**), а также регуляторов (**BMG, gematik, BSI, BfDI, KBV/KVen, BAS, BaFin**) и основы членства в страховых системах (**GKV/PKV**). Всё дано кратко и без таблиц, чтобы начинающему было проще ориентироваться. 

