Doctolib 

1 | Begriff & Einordnung 

**Doctolib** (der Name wird oft als „Doctorlib“ ausgesprochen) ist ein 2013 gegründetes, heute in Deutschland, Frankreich und Italien führendes E-Health-Anbieter-Ökosystem für Arztpraxen, Kliniken und Patient*innen. In Deutschland nutzen laut Firmenangabe rund       **100 000 Leistungserbringer** den Dienst; mehr als 60 Millionen Patient*innen haben einen Account.* 

**Doctolib -** Eine Online-Plattform, die mit Praxis-IT (PVS, TI-Dienste) zusammenspielt - Patienten können Termine selbst buchen – Praxis spart Telefonzeit. 

Also: **Doctolib** ist diese digitale Plattform, die Praxen und Patienten hilft, Termine und Abläufe einfacher zu gestalten. Wenn wir das mit der **Telematik-Infrastruktur (TI)** verbinden, bedeutet das, dass Doctolib in Praxen genutzt wird, die auch an diese sichere Gesundheits-Datenautobahn angeschlossen sind. Die TI sorgt dafür, dass etwa E-Rezepte oder elektronische Arbeitsunfähigkeitsbescheinigungen sicher übermittelt werden und mit den Krankenkassen verknüpft sind. 

In der Praxis heißt das: Doctolib kümmert sich um die Termin- und Patientenverwaltung, während die TI die Brücke zu den Krankenkassen und anderen medizinischen Akteuren bildet. So läuft alles Hand in Hand: Doctolib macht den Praxisalltag reibungsloser, die TI sorgt für die sichere Anbindung an Krankenkassen und gesetzliche Vorgaben – und so fügt sich das ganze Thema nahtlos zusammen. 

Was ist Doctolib – einfach erklärt 

**Doctolib** ist eine digitale Plattform für Arztpraxen und Patient: innen. Sie hilft Praxen bei Terminmanagement, Dokumentation und Technik-Anbindung – und (in Deutschland) kann sie mit der **Telematikinfrastruktur (TI)** verbunden werden, dem sicheren Gesundheitsnetz. So lassen sich z. B. Gesundheitskarten einlesen, eRezepte nutzen oder sicher Nachrichten über KIM senden.  

**Doctolib** — это платформа для клиник и пациентов. В Германии она может работать с гос. мед-сеткой TI: читать карты (eGK), отправлять eРецепты, общаться через KIM. Для этого в клинике ставят локальный компонент (DDV), настраивают коннектор (IP/порт/сертификаты), подключают терминалы для карт, принтеры (прямой печати IPP), а медприборы обмениваются данными через формат GDT. 

Die zwei Seiten von Doctolib in der Praxis 

1. **Online-Organisation & Kalender** 

   Termine planen, auslasten und Kommunikation vereinfachen. (Allgemein) 

2. **Praxissoftware (EHR/PVS) mit lokaler Komponente („DDV“)** 
- Für TI-Funktionen braucht Doctolib eine **lokale Installation** in der Praxis. Dadurch können Arbeitsplätze, Kartenterminals und der TI-**Konnektor** eindeutig zugeordnet und sicher angesprochen werden.  
- **Konnektor + Kartenleser**: Doctolib wird so eingerichtet, dass der Konnektor (mit IP-Adresse/Port) erreichbar ist. Arbeitsplätze werden den Kartenterminals zugeordnet.  
- **Direktdruck**: Dokumente (z. B. AU, Rezepte) lassen sich direkt an Netzwerk- oder (am Mac auch USB-)Drucker senden, die IPP und PDF unterstützen. Für jeden **Dokumententyp** kann ein bestimmter Drucker/Einzug definiert werden.  
- **Medizingeräte per GDT**: Befunde/ Aufträge können zwischen Doctolib und Geräten (z. B. EKG) über das **GDT-Format** ausgetauscht werden – Export (Auftrag an Gerät) und Import (PDF-Befund zurück in die Akte).  
- **Mobile Kartenterminals**: Tragbare Leser (z. B. Orga 930 Care/ M Online, Cherry ST-1530) lesen eGK/KVK unterwegs ein; später wird in der Praxis per Treiber/ DDV synchronisiert. Hinweis: Treiber sind teils älter; ARM-Macs werden nicht unterstützt.  

Wichtige Begriffe (kurz & klar) 

- **TI (Telematikinfrastruktur)**: Das sichere Gesundheitsnetz in DE, verbindet Praxen, Kassen und Patient: innen; Basis für ePA, eRezept, KIM u. a. Dienste.  
- **Konnektor**: Das „TI-Modem“ der Praxis. Stellt die sichere Verbindung zur TI her. In Doctolib wird er mit Host (IP), Port (443) und Zertifikaten hinterlegt.  
- **eGK / KVK**: Elektronische Gesundheitskarte / ältere Krankenversichertenkarte, wird am Kartenterminal gelesen. 
- **HBA**: Heilberufsausweis – digitale Identität der Ärztin/des Arztes, z. B. zum Signieren. **SMC-B**: Institutionskarte der Praxis. Beide stecken am Kartenterminal.  
- **PVS/EHR (Praxisverwaltungssystem/Elektronische Patientenakte der Praxis)**: Die Praxissoftware – hier: Doctolib mit lokaler Komponente (DDV) für Geräte/TI.  
- **KIM**: Sicherer E-Mail-Dienst im Gesundheitswesen (z. B. für Arzt-zu-Arzt- Kommunikation).  
- **GDT**: Standard zum Datenaustausch mit Medizingeräten (Aufträge raus, Befunde rein).  
- **Direktdruck/IPP**: Direktes Senden von PDFs an kompatible Netzwerk-/USB-Drucker; IPP ist das Druck-Protokoll.  

Wie spielt das in der Praxis zusammen? (typischer Ablauf) 

1. Patient kommt → **eGK** wird am **Kartenterminal** gelesen. 
1. Doctolib (lokal) spricht über den **Konnektor** mit der **TI** – z. B. für eRezept oder KIM.  
1. Befunde aus Geräten laufen per **GDT-Import** in die Patientenakte zurück.  
1. Formulare/Rezepte gehen per **Direktdruck** auf den richtigen Drucker/Einzug. 

2 | Kernfunktionen der Plattform 

**Modul  Nutzen für die Praxis  Hinweis** 

24/7-Buchung, automatische \
**Online-Terminmanagement**  [(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) 

Erinnerungen, Wartelisten 

**Digitale Rezeption & KI- Telefonassistent** 

**Videosprechstunde & Patientennachrichten** 

**Überweisernetz & Siilo- Messenger** 

Telefon wird entlastet, Anfragen 

[(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) werden strukturiert erfasst 

DSGVO-konforme Fernbehandlung, 

Rezept- oder Überweisungswünsche  [(doctolib.zendesk.com)](https://doctolib.zendesk.com/hc/de/articles/23956437661332-Tipps-und-Hinweise-zur-Verwendung-von-E-Rezepten-mit-Doctolib) online 

Sichere Kollaboration mit Kolleg\*innen [(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) 

3 | Was ist ein PVS (Praxisverwaltungssystem)? 

Ein PVS bildet **Patientendaten, Termin-, Befund-, Abrechnungs- und Dokumentationsprozesse** digital ab und ist in jeder niedergelassenen Praxis Pflichtausstattung. 

4 | Doctolib ↔ PVS – drei Integrationswege 

1. **Stand-Alone-Nutzung** – Praxis führt zwei Kalender (Doctolib + PVS). 
1. **Standardschnittstellen (GDT, HL7, FHIR)** – laut Doctolib können „für verschiedene Systeme Schnittstellen eingerichtet werden“. 
1. **Spezielle Konnektoren** – Doctolib entwickelt eigene Plug-ins, z. B. den **„unabhängigen Konnektor zu Medatixx“**; er synchronisiert Patientenstammdaten bidirektional und erlaubt das Buchen von Terminen direkt aus dem PVS. 

**Medatixx** ist eine deutsche Firma, die Computerprogramme für Arzt- und Therapiepraxen herstellt. Damit können Praxen Patientendaten, Termine und Abrechnungen zentral verwalten und haben gleichzeitig einen sicheren Zugang zur Telematikinfrastruktur (E-Rezept u. ä.). Durch Zusatzmodule wie Online-Terminbuchung oder Videosprechstunde lässt sich die Software bei Bedarf erweitern, ohne dass die Praxis unterschiedliche Systeme pflegen muss. 

Bidirektional bedeutet, dass Änderungen an Patientenprofilen automatisch von Doctolib in die Kliniksoftware und umgekehrt übertragen werden, so dass die Informationen immer einheitlich und ohne manuelle Doppelarbeit aktualisiert werden. 

**Ausblick 2025:** Doctolib bringt eine **vollwertige Cloud-Praxissoftware („Doctolib Praxis“)** auf den Markt, die PVS-Funktionalitäten, Terminbuchung und KI-gestützte Dokumentation in einer Oberfläche bündelt. Launch für Haus- und Fachärzt:innen ist für Herbst 2025 geplant. 

5 | Telematikinfrastruktur (TI) & TI-Konnektor 

**Baustein  Kurzbeschreibung** 

Hardware-Router, der PVS/Kartenterminals via VPN ans Gesundheitsnetz **TI-Konnektor** anschließt, damit eGK-Daten, E-Rezept, ePA, KIM-Mails usw. sicher 

ausgetauscht werden können. 

**TI-Gateway**  Moderne Alternative ohne eigene Box; VPN-Dienst aus zertifiziertem **(TI 2.0)**  Rechenzentrum. 

**eHBA &**  Elektronischer Heilberufsausweis & Praxis-Smartcard für Signatur und **SMC-B**  Authentifizierung. 

6 | Doctolib im TI-Kontext 

**Gematik-bestätigt:** „Doctolib Praxis“ erhält 2025 die Konformitätsbestätigung für **eRezept (stufe eRp) und Medication-Service (ePA 3.0)**. 

Bereits 2021 wurden Module für **VSDM (Versichertenstammdaten-Management) und KIM 1.0** zertifiziert. 

Für das E-Rezept braucht die Praxis weiterhin ein PVS, einen TI-Konnektor bzw. TI- Gateway, eHBA-Signatur – Doctolib zeigt in seiner Hilfe Schritt-für-Schritt, wie beides zusammenspielt. 

Die **gematik – Nationale Agentur für Digitale Medizin** gestaltet und verantwortet Deutschlands Telematikinfrastruktur (TI) – die zentrale Plattform, über die digitale Anwendungen wie elektronische Patientenakte (ePA) und E-Rezept sicher, performant und interoperabel laufen. Ihre Kernaufgaben sind: 

- **Standardisierung & Sicherheit:** Festlegung und Durchsetzung verbindlicher technischer und organisatorischer Standards, damit alle TI-Dienste zuverlässig zusammenarbeiten.[ gematik.de ](https://www.gematik.de/ueber-uns)
- **Orchestrierung & Beratung:** Vermittlung zwischen Politik, Selbstverwaltung, Industrie und internationalen Partnern, um Innovationen gemeinsam voranzubringen. [gematik.de](https://www.gematik.de/ueber-uns)[gematik.de ](https://www.gematik.de/ueber-uns/struktur)
- **TI 2.0 & zentrale Dienste:** Aufbau einer weiterentwickelten TI als „nationale Arena für digitale Medizin“ und Bereitstellung essenzieller Basisdienste, um Kosten zu senken und neue Angebote zu beschleunigen. [gematik.de ](https://www.gematik.de/ueber-uns)
- **Open-Source-Kultur:** Veröffentlichung von Produktiv-Code (z. B. E-Rezept-App) und API-Spezifikationen auf GitHub/Simplifier, unterstützt von einem internen Open Source Program Office; Ziel sind Transparenz und Community-Mitwirkung.  

7 | Datenschutz & Sicherheit 

Doctolib betreibt seine Plattform in **BSI-C5-zertifizierten Cloud-Umgebungen**. 

Diskussionen gibt es 2025 um die Absicht, **anonymisierte Patientendaten für KI-Training zu nutzen**; Praxen sollten die jeweils aktuelle Datenschutzerklärung prüfen.** 

**BSI-C5** bzw. **C5 („Cloud Computing Compliance Criteria Catalogue“)** ist ein Katalog von Sicherheits- und Transparenzanforderungen des Bundesamts für Sicherheit in der Informationstechnik (BSI) für Cloud-Dienstleister. Er definiert das *Mindestschutzniveau*, das ein professioneller Cloud-Anbieter nachweisen muss, damit Behörden und Unternehmen seine Services sicher nutzen können.[ bsi.bund.de ](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/Empfehlungen-nach-Angriffszielen/Cloud-Computing/Kriterienkatalog-C5/kriterienkatalog-c5_node.html?utm_source=chatgpt.com)

8 | Praktische Vor- & Nachteile 

**Plus  Minus** 

Hohe Reichweite für Neupatient\*innen,  Doppelte Kalenderführung, falls keine weniger Telefonlast  Schnittstelle 

**Plus** 

Automatische Terminerinnerungen, weniger No-Shows 

TI-fähige Module (KIM, eRezept) 

Eigene Konnektoren beschleunigen Datenabgleich mit PVS 

**Minus** 

Externe Buchungsseite – Patient verlässt Praxis-Website 

Kostenpflichtiges Abo-Modell 

Abhängigkeit von Cloud-Dienst & Internetverbindung 

Infografik (Darstellung aller Begriffe und ihrer Beziehungen) 

- [Begriffsliste und Zusammenhänge](file:///D:/IHK%20-%20PrÃ¼fungen%20\(AP1,%20AP2\)/AP%202/Projektarbeit%20\(IHK-AbschlussprÃ¼fung\)/Projektarbeit%20-%20Doctolib/Doctolib_Begriffe.docx)

![images](ASPOSE~1.JPE) Aspose.Words.fda18144-91ed-440a-9085-a95e3ddae147.001

Begriffsliste und Zusammenhänge 

Begriff Doctolib  

PVS (Praxisverwaltungssoftware) 

TI (Telematikinfrastruktur) 

TI-Konnektor TI-Gateway eRezept 

ePA (elektronische Patientenakte) 

eGK (elektronische Gesundheitskarte) 

VSDM (Versichertenstammdaten‑Ma nagement) 

KIM (Kommunikation im Medizinwesen) 

eHBA (elektronischer Heilberufsausweis) 

SMC-B (Institutionskarte) 

Zusammenhang 

Online-Plattform, die mit Praxis- IT (PVS, TI-Dienste) zusammenspielt 

Herzstück jeder Praxis-IT; Doctolib nutzt Schnittstellen zu PVS 

Geschütztes Gesundheitsnetz, an das PVS & Doctolib-Module andocken 

Router im Praxisraum, stellt TI‑Verbindung her 

Cloud-Ersatz für den Konnektor (TI 2.0) 

TI-Anwendung, lässt sich aus PVS/Doctolib signieren & versenden 

TI-Anwendung; Doctolib plant Anzeige in „Doctolib Praxis“ 

Steckt im Kartenterminal, liefert Daten fürs VSDM 

Pflicht‑TI‑Dienst; läuft beim Einlesen der eGK 

TI-Maildienst; Doctolib-Module können KIM-Postfächer anbinden 

Persönliche Chipkarte der Ärztin/des Arztes 

Chipkarte der Praxis, wird mit eHBA genutzt 

Sinn / Nutzen 

Patienten können Termine selbst buchen 

- Praxis spart Telefonzeit 

  Verwaltet Patienten, Termine, Abrechnungen, Befunde 

  Sichere Übermittlung von E‑Rezept, ePA u. a. 

  Bringt das PVS ans Gesundheitsnetz 

  Kein eigener Router mehr nötig 

  Rezept als QR‑Code statt Papier 

  Alle Arztinfos der Patient\*innen an einem Ort 

  Versicherungsnachwei s auf Chipkarte 

  Prüft online, ob die Karte gültig ist 

  Arztbriefe sicher als E- Mail statt Fax 

  Digital unterschreiben & TI-Anwendungen nutzen 

  Weist die Betriebsstätte in der TI aus 

HL7 / GDT / FHIR 

Doctolib Praxis (Cloud-PVS) 

Standard‑Schnittstellen  Sorgen dafür, dass zwischen Doctolib und diversen  Systeme Daten PVS  verstehen 

Eigene All-in-One-Praxissoftware  Bündelt 

(Start Herbst 2025)  Terminbuchung, 

Dokumentation & TI- Funktionen 

Was steckt hinter dem „unabhängigen Konnektor zu Medatixx“? 

**Ebene Technische Rolle** 

**Was genau passiert?** 

Kleines Windows-Programm (Middleware) läuft auf jedem Praxis-PC oder dem PVS-Server. Es spricht **lokal** mit *Medatixx by Medatixx* (Datenbank / SDK) **und** online mit der Doctolib-API. 

**Warum ist das nützlich?** 

Kein fremder Zugriff auf das PVS – die Praxis behält die Datenhoheit. 

- Stammdaten (Name, Geburts-

**Datensynchron (Patient** datum, Kontakt, KV-Nr.) werden 

**→ Doctolib)**  periodisch oder „On Demand“ zu 

Doctolib gespiegelt. 

Sorgt dafür, dass Online- Termine immer den aktuellsten Patienten- datensatz nutzen. [(community.doctolib.de)](https://community.doctolib.de/t/neuer-unabhaengiger-konnektor-zu-medatixx-by-medatixx-verfuegbar/38753) 

Ändert der Patient z. B. seine 

Mobilnummer im Online-Portal, 

Vermeidet Tippfehler & **Datensynchron**  zeigt Medatixx beim nächsten 

Doppelpflege. **(Doctolib → PVS)**  Aufruf einen **Update-Vorschlag** an 

[(community.doctolib.de)](https://community.doctolib.de/t/neuer-unabhaengiger-konnektor-zu-medatixx-by-medatixx-verfuegbar/38753) 

- die MFA klickt nur noch 

  „Speichern“. 

Aus Doctolib lässt sich per Klick 

**die passende Patientenakte in Kontext-Start** 

**Medatixx öffnen** (Patient-ID wird übergeben). 

Spart Suche im PVS, besonders bei gleichen Namen. [(community.doctolib.de)](https://community.doctolib.de/t/neuer-unabhaengiger-konnektor-zu-medatixx-by-medatixx-verfuegbar/38753) 

Wenn die MFA in Medatixx eine 

Akte geöffnet hat, kann sie **direkt**  Nur ein Klick, kein Wechsel **Terminbuchung aus** 

**dort** einen Doctolib-Slot buchen;  zur Browsersuche. 

**dem PVS** 

der Konnektor übergibt alle IDs und [(community.doctolib.de)](https://community.doctolib.de/t/neuer-unabhaengiger-konnektor-zu-medatixx-by-medatixx-verfuegbar/38753) zeigt sofort die Online-Agenda. 

„Tagesliste“ oder „Terminhistorie“ **Zusatzfenster**  von Doctolib lässt sich aus 

Medatixx heraus anzeigen. 

Schneller Überblick über alle Online-Termine eines Tages oder Patienten. [(community.doctolib.de)](https://community.doctolib.de/t/neuer-unabhaengiger-konnektor-zu-medatixx-by-medatixx-verfuegbar/38753) 

Installation & Voraussetzungen in 5 Schritten 

1. **Termin mit Doctolib-Support buchen** (Fernwartung).[ doctolib.zendesk.com ](https://doctolib.zendesk.com/hc/de/articles/21756642591124-Termin-buchen-zur-Installation-des-unabh%C3%A4ngigen-Medatixx-Konnektor-per-Fernwartung)
1. **System-Check**: Windows 10/11, Medatixx ≥ V.2.15, Internetzugang, Admin-Rechte. 
1. **Connector-Setup pro PC** – der Support installiert Dienst & Tray-App, hinterlegt API- Token.  
1. **Initiale ID-Zuordnung**: einmaliges Matching aller bestehenden Patientennummern zwischen Medatixx und Doctolib. 
1. **Kurzschulung**: Wie starte ich Buchung/Listen, wie bestätige ich Update-Vorschläge? 

**Kosten:** Der Connector selbst ist seit 12/2023 kostenfrei; ggf. verlangt Medatixx für die Aktivierung der lokalen Schnittstelle (X-API) eine kleine Lizenzgebühr.[ community.doctolib.de ](https://community.doctolib.de/t/entdecken-sie-unsere-konnektoren-und-erleichtern-sie-ihre-arbeitsablaeufe/77154?utm_source=chatgpt.com)

**Begriff  Was ist das?  Wozu dient es?** 

Ein kleines Programm, das unter 

Windows im Hintergrund läuft  Hält die Verbindung zwischen Praxis-PC und **Dienst** 

und **automatisch startet**,  Doctolib am Laufen, ohne dass jemand **(Service)** 

sobald der PC hochfährt. Es hat  eingeloggt sein muss. 

kein eigenes Fenster. 

Winzige Zusatz-Anwendung,  Zeigt den Status des Connectors (grün = OK, 

deren Symbol (Icon) unten  rot = Fehler) und bietet per Rechtsklick **Tray-App** 

rechts im **System-Tray** neben  Funktionen wie „Neu synchronisieren“ oder der Uhr erscheint.  „Log-Datei öffnen“. 

Eine lange, zufällig erzeugte  Damit weist sich der Connector eindeutig Zeichenfolge (z. B.  gegenüber Doctolib aus, ohne jedes Mal 

**API-**

„d4f9…e8c2“). Sie funktioniert  Benutzername/Passwort senden zu müssen – **Token** 

wie ein **digitaler Schlüssel** zur  ähnlich wie ein Zugangstoken bei Online- Schnittstelle (API) von Doctolib.  Banking-Apps. 

**Grenzen & Best Practices** 

- **Kalenderführung**: Termine liegen weiterhin allein in Doctolib; Medatixx bleibt Kalender-passiv. 
- **Datenumfang**: Es werden nur Stammdaten synchronisiert, **keine Befunde** oder Dokumente. 
- **Versionspflege**: Nach PVS-Updates kurz prüfen, ob der Connector-Dienst läuft (Tray-Icon = grün). 
- **Datenschutz**: Datenverkehr zwischen Connector und Doctolib-API ist TLS- verschlüsselt; sämtliche Zugriffe erscheinen im Praxis-Log des PMS. 

Wo passt ORM (Object-Relational Mapping) ins Bild? 

ORM ist eine „Schicht“, die SQL-Tabellendatensätze (Patienten, Termine) in Codeobjekte und wieder zurück verwandelt. 

Bei der Integration von Doctolib in das Klinikprogramm liest/schreibt der Konnektor über ORM einfach Daten in die lokale PVS-Datenbank und sendet sie an die Doctolib-API, ohne manuell SQL zu schreiben. 

**Typisches Szenario in einer Ebene** 

**Doctolib-Integration** 

1  Lokaldatenbank des PVS 

2  Middleware / Connector 

3  Cloud-Backend von Doctolib 4  Eigenentwicklung / Reporting 

**Rolle von ORM** 

Praxisverwaltungssysteme wie **Medatixx, tomedo oder x.isynet** speichern Patienten-, Termin- und Abrechnungsdaten in relationalen SQL-Datenbanken (PostgreSQL, MS SQL, MySQL …). 

Beim bidirektionalen Abgleich holt die Middleware neue Patienteneinträge aus der PVS-Datenbank und übergibt sie als JSON an die Doctolib-API – und umgekehrt. 

Auch im Doctolib-Backend (Microservices) liegen Termin- und Nutzerdaten in relationalen Clustern; API liefert sie als REST/FHIR-Objekte. 

Praxis oder IT-Dienstleister schreibt ein kleines Tool, das PVS-Daten analysiert (Fehlzeiten-Statistik, Recall-Listen) und mit Doctolib-Daten mergen soll. 

**Kurz gesagt:** 

Wenn Entwickler\*innen einen Connector oder ein Analyse-Tool rund um Doctolib bauen, erleichtert ORM die Arbeit mit den relationalen Praxisdatenbanken: man programmiert auf Objektebene („termin.startzeit“), während das Framework die passende SQL-Abfrage erledigt. 

Doctolib-Kalender – so arbeitet das Praxisteam damit 

**Schritt /  Was sieht & tut die Praxis im** 

**Warum ist das nützlich?** 

**Modul  Alltag?** 

Grundstruktur anlegen 

- Terminarten (z. B. „HNO-

  Erstuntersuchung 30 min“) 

  definieren, Farbe & Dauer  Alles geschieht in den **Einstellungen →** festlegen.  **Terminmanagement**; Drag-&-Drop & 

1  Farbwahl machen den Plan sofort lesbar. 

- Sprechzeiten (Öffnung, Pausen,  [(doctolib.zendesk.com,](https://doctolib.zendesk.com/hc/de/articles/360055550492-Meine-bestehenden-Terminarten-verwalten-anpassen) 

  Urlaube) als farbige Blöcke  [doctolib.zendesk.com)](https://doctolib.zendesk.com/hc/de/articles/201750096-Warum-ist-ein-freies-Zeitfenster-im-Kalender-f%C3%BCr-Patient-innen-online-nicht-buchbar) 

  einzeichnen. 

- Terminarten einzelnen Sprechzeiten zuordnen. 

Kalender zeigt farbige Slots; Filter links 

2  Tages-/Wochenansicht  blenden einzelne Ärzt:innen, Räume oder 

Geräte ein/aus. 

- Klick auf freien Slot → „Mini-Terminkarte“ öffnet sich. 
- Praxis sucht Patient*in oder legt Neu- patient*in an. 

3  Termine anlegen / ändern 

- Drag-&-Drop oder Doppelklick zum Verschieben / Verlängern. 
- Spontan-Termine möglich, sogar wenn Pat. kein Online-Konto hat. 

Online reservierte Slots erscheinen sofort 4  Online-Buchungen  (grau schraffiert, 15-Min-Reservierung 

schützt vor Doppelgriff). 

Praxis kann Pat. auf Warteliste setzen; bei 5  Digitale Warteliste  Absage verschickt das System 

automatisch Einladungen an Vormerker. 

SMS/E-Mail-Reminder vor dem Termin; Automatische Erinnerungen &  bei zyklischen Leistungen (z. B. Kontroll- 

6 

Recall  untersuchung) lassen sich **Recalls** in 

festen Abständen planen.  

7  Vertretungen & Ressourcen  In den Sprechzeiten lässt sich für Urlaube eine **Vertretung** (anderer Arzt, PA, Raum) 

**Schritt /  Was sieht & tut die Praxis im** 

**Warum ist das nützlich?** 

**Modul  Alltag?** 

hinterlegen; Rechte werden granular vergeben. 

Klick auf Termin öffnet Patientenkarte (Kontaktdaten, Historie). Bei 

8  Patientenkarte & Datenabgleich 

angeschlossenem PVS (Medatixx, tomedo 

u. a.) laufen Stammdaten bidirektional. Balken in der Kopfzeile zeigt neue 

Termine, Terminänderungen oder 

9  Benachrichtigungen & Aufgaben 

Patientennachrichten; Aufgaben lassen sich als *dringend* markieren. 

CSV-Export, iCal-Feed oder API-Zugriff für Controlling, Dienstplanung (z. B. via 

10  Auswertungen & Export  Planerio). 

**Typische Workflows** 

1. **Montagmorgen:** MFA öffnet Wochenansicht, zieht per Maus einen Urlaubblock für 5 Tage → alle Online-Slots verschwinden sofort. 
1. **Patient ruft an:** MFA klickt freien Slot, wählt schon gespeicherte Patientin; Terminkarte füllt sich automatisch, SMS-Bestätigung geht raus. 
1. **Kurzfristige Absage:** Slot wird frei → System informiert drei Pat. auf Warteliste; der Schnellste übernimmt. 
1. **Recall:** Für jede HPV-Impfung wird beim Abschließen des Termins ein 6-Monats- Recall gesetzt; Erinnerung läuft automatisch. 

**Fazit daraus:**  

Die Fernsehsendung SWR Marktcheck zeigt die Vorteile von Doctolib (schnelle Online- Registrierung, weniger Anrufe in Kliniken) und die Nachteile: 

- Das System kann persönliche Daten von Patienten enthalten, die sich nie registriert haben, weil Ärzte ihre Datenbanken hochladen; 

  Kurz & einfach (RU) 

- Der Doctolib-Kalender ist der zentrale Arbeitsplan für die Klinik. 
- In ihm werden Terminarten und Öffnungszeiten im Voraus festgelegt; Patienten buchen freie Zellen online. 
- Ein Mitarbeiter kann manuell Termine hinzufügen/verschieben, Patienten in eine digitale Warteschlange stellen, automatische Erinnerungen und „Recall“-Serien aktivieren. 
- Urlaube und Vertretungen sind mit ein paar Klicks markiert, und die Patientendaten werden mit dem lokalen Register synchronisiert. Auf diese Weise vermeidet die Klinik doppelte Einträge und Leerlaufzeiten. 


