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

**Modul**  
1. Online-Terminmanagement
2. Digitale Rezeption & KI- Telefonassistent
3. Videosprechstunde & Patientennachrichten
4. Überweisernetz & Siilo- Messenger
 
**Nutzen für die Praxis  Hinweis** 
1. 24/7-Buchung, automatische Erinnerungen, Wartelisten
2. Telefon wird entlastet, Anfragen werden strukturiert erfasst  
3.  DSGVO-konforme Fernbehandlung, Rezept- oder Überweisungswünsche
4.  Sichere Kollaboration mit Kolleg\*innen
5.  
[(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) 
[(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) 
[(doctolib.zendesk.com)](https://doctolib.zendesk.com/hc/de/articles/23956437661332-Tipps-und-Hinweise-zur-Verwendung-von-E-Rezepten-mit-Doctolib) online 
[(info.doctolib.de)](https://info.doctolib.de/allgemeinarzt/) 

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

**Baustein: - Kurzbeschreibung** 

**TI-Konnektor:** - Hardware-Router, der PVS/Kartenterminals via VPN ans Gesundheitsnetz anschließt, damit eGK-Daten, E-Rezept, ePA, KIM-Mails usw. sicher 
ausgetauscht werden können. 

**TI-Gateway:** - Moderne Alternative ohne eigene Box; VPN-Dienst aus zertifiziertem **(TI 2.0)**  Rechenzentrum. 

**eHBA & SMC-B**-  Elektronischer Heilberufsausweis & Praxis-Smartcard für Signatur und Authentifizierung. 

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

**Plus**  
+ Hohe Reichweite für Neupatient\*innen,  weniger Telefonlast  
+ Automatische Terminerinnerungen, weniger No-Shows 
+ TI-fähige Module (KIM, eRezept) 
+ Eigene Konnektoren beschleunigen Datenabgleich mit PVS 

**Minus** 
- Doppelte Kalenderführung, falls keine Schnittstelle 
- Externe Buchungsseite – Patient verlässt Praxis-Website 
- Kostenpflichtiges Abo-Modell 
- Abhängigkeit von Cloud-Dienst & Internetverbindung 

Infografik (Darstellung aller Begriffe und ihrer Beziehungen) 

- [Begriffsliste und Zusammenhänge](file:///D:/IHK%20-%20PrÃ¼fungen%20\(AP1,%20AP2\)/AP%202/Projektarbeit%20\(IHK-AbschlussprÃ¼fung\)/Projektarbeit%20-%20Doctolib/Doctolib_Begriffe.docx)

![images](ASPOSE~1.JPE) 


Begriffsliste und Zusammenhänge – in ganzen Sätzen

Doctolib ist eine Online-Plattform, die mit der Praxis-IT zusammenarbeitet, insbesondere mit der Praxisverwaltungssoftware (PVS) und mit Diensten der Telematikinfrastruktur (TI). Patientinnen und Patienten können damit Termine selbst buchen, wodurch Praxen spürbar Telefonzeit sparen. In der Praxis ist die PVS das Herzstück der IT: Sie verwaltet Patientendaten, Termine, Abrechnungen und Befunde und stellt die zentrale Oberfläche für das Behandlungsteam dar. Doctolib nutzt dabei definierte Schnittstellen zur PVS, um Informationen sicher und verlässlich auszutauschen.

Die TI ist das geschützte Gesundheitsnetz in Deutschland, an das PVS-Systeme und Doctolib-Module andocken. Über die TI werden Anwendungen wie das E-Rezept, die elektronische Patientenakte (ePA) und der sichere Nachrichtendienst KIM bereitgestellt. Der Zugang zur TI erfolgt entweder über einen lokalen TI-Konnektor oder über ein TI-Gateway. Der TI-Konnektor ist ein Hardware-Router in der Praxis, der die sichere Verbindung vom lokalen Netzwerk zur TI herstellt. Das TI-Gateway ist die moderne Cloud-Variante, die den physischen Router ersetzt und den TI-Zugang als Dienst bereitstellt.

Das E-Rezept ist eine TI-Anwendung, die Rezepte digital und rechtssicher ermöglicht. Ärztinnen und Ärzte können E-Rezepte aus der PVS oder — je nach Integration — direkt aus Doctolib heraus signieren und an die TI übermitteln. Die ePA ist die elektronische Patientenakte, in der ärztliche Informationen der Patientinnen und Patienten an einem Ort zusammengeführt werden; eine Anzeige innerhalb einer integrierten Praxissoftware wie „Doctolib Praxis“ ist vorgesehen. Die elektronische Gesundheitskarte (eGK) wird im Kartenterminal gesteckt und liefert die für das Versichertenstammdaten-Management (VSDM) notwendigen Informationen. Das VSDM ist ein Pflichtdienst der TI und prüft beim Einlesen der eGK online, ob die Karte gültig ist und ob die Versichertenstammdaten aktuell sind.

KIM ist der sichere E-Mail-Dienst des Gesundheitswesens. Doctolib-Module können KIM-Postfächer anbinden, sodass Arztbriefe und andere sensible Dokumente statt per Fax verschlüsselt per E-Mail übertragen werden. Für die rechtssichere Nutzung der TI werden zwei Chipkarten benötigt: der elektronische Heilberufsausweis (eHBA) identifiziert die Ärztin oder den Arzt persönlich und ermöglicht rechtssichere qualifizierte elektronische Signaturen; die SMC-B ist die Institutionskarte der Praxis und weist die Betriebsstätte innerhalb der TI aus. Beide Karten werden typischerweise im Zusammenspiel mit dem Kartenterminal und der Praxissoftware genutzt.

Damit unterschiedliche Systeme zusammenarbeiten, kommen Standardschnittstellen wie HL7, FHIR und GDT zum Einsatz. HL7 und FHIR beschreiben strukturierte medizinische Daten und deren Austausch zwischen Anwendungen. GDT ist ein schlanker Standard, über den Praxissoftware und Medizingeräte Aufträge und Befunde austauschen. Durch diese Standards „verstehen“ sich Doctolib, PVS und angeschlossene Geräte, was doppelte Datenerfassung und Fehler reduziert.

„Doctolib Praxis“ ist als Cloud-Praxissoftware konzipiert und bündelt Terminbuchung, medizinische Dokumentation und TI-Funktionen in einer Oberfläche. Das Ziel ist es, Medienbrüche zu vermeiden und Aufgaben wie das Versenden von E-Rezepten, den KIM-Nachrichtenaustausch und die Terminorganisation in einem durchgängigen Workflow zu ermöglichen.

Der „unabhängige Konnektor zu Medatixx“ beschreibt eine technische Integration zwischen Doctolib und dem PVS-System Medatixx. Eine kleine Windows-Middleware läuft auf jedem Praxis-PC oder auf dem PVS-Server. Diese Middleware kommuniziert lokal mit Medatixx über dessen Datenbank beziehungsweise SDK und verbindet sich gleichzeitig online mit der Doctolib-API. Die Praxis behält dadurch die Datenhoheit, weil kein externer Direktzugriff von außen auf die PVS-Datenbank erforderlich ist.

In der Praxis bedeutet das: Stammdaten wie Name, Geburtsdatum, Kontaktdaten und KV-Nummer werden in regelmäßigen Abständen oder bei Bedarf aus Medatixx zu Doctolib synchronisiert. Online gebuchte Termine greifen so stets auf den aktuellen Patientendatensatz zu. Wenn Patientinnen oder Patienten ihre Kontaktdaten im Doctolib-Portal ändern, zeigt Medatixx beim nächsten Aufruf einen Update-Vorschlag an, den das Team mit einem Klick übernehmen kann. Das reduziert Tippfehler und verhindert doppelte Pflege. Darüber hinaus erlaubt ein Kontext-Start aus Doctolib heraus das direkte Öffnen der passenden Patientenakte in Medatixx; die Patient-ID wird übergeben, sodass die Suche entfällt und besonders bei Namensgleichheit keine Zeit verloren geht. Ist in Medatixx eine Akte geöffnet, kann die Mitarbeitende direkt aus dem PVS einen verfügbaren Doctolib-Termin buchen, ohne in die Browsersuche wechseln zu müssen. Diese Integration spart Klicks, vermeidet Medienbrüche und macht die Terminorganisation schneller und sicherer.

Zusammenfassend lässt sich sagen: Doctolib organisiert die patientennahe Kommunikation und Terminwelt, die PVS führt die medizinische und organisatorische Kernakte, und die TI liefert die sichere Infrastruktur für Anwendungen wie E-Rezept, ePA und KIM. TI-Konnektor oder TI-Gateway stellen den Zugang her, eHBA und SMC-B sorgen für Identität und Signatur, und Standards wie HL7, FHIR und GDT schaffen die technische Verständigung. Integrierte Lösungen wie „Doctolib Praxis“ und der unabhängige Konnektor zu Medatixx verbinden diese Bausteine zu einem nahtlosen Praxisworkflow


3. Wie die Bausteine zusammenspielen --> vom Check-in bis zum Versand

  1. Patient:in kommt an --> eGK ins Kartenterminal, VSDM läuft automatisch.
  2. PVS liest/aktualisiert Stammdaten; Doctolib zeigt den Termin im Kalender.
  3. Ärztin/Arzt erstellt eRezept --> Signatur mit eHBA → Versand über TI.
  4. Befunde/Kommunikation laufen sicher via KIM; Dokumentation liegt im PVS.
  5. Online-Termine, Erinnerungen und Wartelisten steuert Doctolib.



4. Standards & Schnittstellen: HL7 / GDT / FHIR

HL7/FHIR: Austausch klinischer Daten (z. B. Befunde, Ressourcen) zwischen Systemen.

GDT: Einfache Datei-Schnittstelle zu Medizingeräten (Auftrags-Export, Befund-Import).
Nutzen: Diese Standards sorgen dafür, dass Doctolib, PVS und Geräte ohne proprietäre Sonderwege miteinander kommunizieren können.

5. Doctolib Praxis (Cloud-PVS)

Was es verspricht: Eine integrierte Oberfläche für Terminbuchung, Dokumentation und TI-Funktionen.
Praktischer Effekt: Weniger Medienbrüche, klare Rollenrechte, direkte Nutzung von TI-Diensten (eRezept, KIM) innerhalb eines Workflows.

6. „Unabhängiger Konnektor zu Medatixx“ – was passiert technisch?

Technische Rolle (Ebene):
Ein kleines Windows-Programm (Middleware) läuft auf jedem Praxis-PC oder dem PVS-Server. Es spricht lokal mit Medatixx by Medatixx (Datenbank/SDK) und online mit der Doctolib-API.
Warum nützlich? Die Praxis behält die Datenhoheit – kein externer Direktzugriff auf die PVS-Datenbank.

Was genau passiert – typische Flows

Datensynchron PVS → Doctolib
Stammdaten (Name, Geburtsdatum, Kontakt, KV-Nr.) werden periodisch oder on demand zu Doctolib gespiegelt.
→ Online-Termine nutzen stets den aktuellsten Patientendatensatz.
Quelle: community.doctolib.de

Datensynchron Doctolib → PVS
Ändert der/die Patient:in z. B. die Mobilnummer im Online-Portal, zeigt Medatixx beim nächsten Aufruf einen Update-Vorschlag an – die MFA klickt nur noch „Speichern“.
→ Weniger Tippfehler & keine Doppelpflege.
Quelle: community.doctolib.de

Kontext-Start (Sprung aus Doctolib ins PVS)
Aus Doctolib lässt sich per Klick die passende Patientenakte in Medatixx öffnen (Patient-ID wird übergeben).
→ Spart Suche im PVS, besonders bei Namensgleichheit.
Quelle: community.doctolib.de

Terminbuchung aus dem PVS heraus
Ist eine Akte in Medatixx geöffnet, kann direkt ein Doctolib-Slot gebucht werden – ohne separaten Browser-Wechsel.
→ Ein Klick, weniger Kontextwechsel.

Kurzfazit zum Medatixx-Konnektor:
Saubere bidirektionale Stammdatensynchronisation, Kontext-Start und Direktbuchung reduzieren Fehler und Klickwege – bei voller Kontrolle der Praxis über ihre Daten.

7. Mini-Glossar (ein Satz pro Begriff)

Doctolib: Online-Kalender & Patientenkommunikation mit TI-Anbindung.

PVS: Zentrales System für Verwaltung, Abrechnung und Dokumentation.

TI: Sicheres Netz, über das eRezept, ePA, KIM & Co. laufen.

TI-Konnektor/TI-Gateway: Lokale Box bzw. Cloud-Variante als TI-Zugang.

eRezept: Digital signiertes Rezept als QR-Code.

ePA: Elektronische Patientenakte für Befunde/Informationen.

eGK/VSDM: Chipkarte & Online-Prüfung des Versicherungsstatus.

KIM: Ende-zu-Ende-gesicherte Mails im Medizinwesen.

eHBA/SMC-B: Persönliche/Institutionelle Chipkarten für Signatur & Nachweis.

HL7/GDT/FHIR: Interoperabilitäts-Standards, die Systeme verständlich machen.

Doctolib Praxis: Cloud-PVS, das mehrere Funktionen in einer UI bündelt.



**Was steckt hinter dem „unabhängigen Konnektor zu Medatixx“?**

Der unabhängige Konnektor zu Medatixx ist eine kleine Windows-Middleware, die auf jedem Praxis-PC oder alternativ auf dem PVS-Server läuft. Diese Middleware kommuniziert lokal mit Medatixx by Medatixx über Datenbank- oder SDK-Schnittstellen und verbindet sich zugleich online mit der Doctolib-API. Dadurch bleibt die Datenhoheit vollständig in der Praxis: Es ist kein externer Direktzugriff auf die PVS-Datenbank nötig, und alle Bewegungen der Daten sind transparent und kontrollierbar.

Bei der Datensynchronisation von der PVS zu Doctolib werden Stammdaten wie Name, Geburtsdatum, Kontaktdaten und die KV-Nummer entweder regelmäßig in Intervallen oder bei Bedarf sofort an Doctolib übertragen. Auf diese Weise greifen Online-Termine stets auf den aktuellsten Patientendatensatz zu, was Falschzuordnungen und Rückfragen vermeidet (vgl. community.doctolib.de).

In der Gegenrichtung, also bei der Datensynchronisation von Doctolib zur PVS, fließen Änderungen, die Patient:innen im Doctolib-Portal vornehmen, zurück nach Medatixx. Ändert beispielsweise jemand die Mobilnummer, zeigt Medatixx beim nächsten Öffnen der Akte einen Update-Vorschlag an, den das Praxisteam mit einem Klick übernehmen kann. Das reduziert Tippfehler, verhindert doppelte Pflege und beschleunigt den Alltag deutlich (vgl. community.doctolib.de).

Der Kontext-Start sorgt für nahtlose Arbeitsabläufe: Aus Doctolib heraus lässt sich mit einem Klick die passende Patientenakte direkt in Medatixx öffnen. Dabei wird die Patient-ID übertragen, sodass keine zeitaufwändige Suche im PVS erforderlich ist. Das ist vor allem bei Namensgleichheiten hilfreich und spart spürbar Zeit (vgl. community.doctolib.de).

Auch die Terminbuchung aus dem PVS heraus wird vereinfacht. Wenn in Medatixx eine Akte geöffnet ist, kann das Team unmittelbar einen freien Doctolib-Slot buchen. Der Konnektor übergibt dabei alle relevanten IDs, und die Online-Agenda steht ohne zusätzlichen Browser-Wechsel bereit. So genügt ein einziger Klick, um einen Termin sicher zu reservieren (vgl. community.doctolib.de).

Als Ergänzung bietet die Middleware Zusatzfenster an, mit denen sich aus Medatixx heraus Ansichten wie die Doctolib-„Tagesliste“ oder die „Terminhistorie“ öffnen lassen. Das liefert dem Team einen schnellen Überblick über alle Online-Termine eines Tages oder die bisherigen Termine eines konkreten Patienten, ohne zwischen Programmen springen zu müssen (vgl. community.doctolib.de).

Kurz gesagt: Die Middleware verbindet Medatixx und Doctolib sicher und bidirektional, hält Stammdaten automatisch konsistent, ermöglicht den direkten Sprung zwischen den Systemen, vereinfacht die Terminbuchung und liefert Zusatzansichten für den Alltag – und das alles bei voller Datenhoheit der Praxis.


8. Praxisnutzen auf einen Blick

- Telefon entlasten: Online-Buchung & automatische Erinnerungen.
- Datenqualität erhöhen: Bidirektionaler Sync verhindert Dubletten.
- Sicher kommunizieren: KIM statt Fax, eHBA-Signaturen für Rechtsgültigkeit.
- Workflows beschleunigen: Kontext-Start & Direktbuchung sparen Zeit.
- Zukunftssicher: Standards (HL7/FHIR/GDT) + TI-Gateway-Option.



Installation & Voraussetzungen in 5 Schritten 

1. **Termin mit Doctolib-Support buchen** (Fernwartung).[ doctolib.zendesk.com ](https://doctolib.zendesk.com/hc/de/articles/21756642591124-Termin-buchen-zur-Installation-des-unabh%C3%A4ngigen-Medatixx-Konnektor-per-Fernwartung)
1. **System-Check**: Windows 10/11, Medatixx ≥ V.2.15, Internetzugang, Admin-Rechte. 
1. **Connector-Setup pro PC** – der Support installiert Dienst & Tray-App, hinterlegt API- Token.  
1. **Initiale ID-Zuordnung**: einmaliges Matching aller bestehenden Patientennummern zwischen Medatixx und Doctolib. 
1. **Kurzschulung**: Wie starte ich Buchung/Listen, wie bestätige ich Update-Vorschläge? 

**Kosten:** 
Der Connector selbst ist seit 12/2023 kostenfrei; ggf. verlangt Medatixx für die Aktivierung der lokalen Schnittstelle (X-API) eine kleine Lizenzgebühr.
[ community.doctolib.de ](https://community.doctolib.de/t/entdecken-sie-unsere-konnektoren-und-erleichtern-sie-ihre-arbeitsablaeufe/77154?utm_source=chatgpt.com)



**Begriff  Was ist das?  Wozu dient es?** 

Dienst (Service):
Ein Dienst ist ein kleines Programm, das unter Windows im Hintergrund läuft, automatisch mit dem Start des PCs hochfährt und kein eigenes Fenster besitzt. Es arbeitet dauerhaft weiter, auch wenn niemand angemeldet ist.
Der Dienst hält die Verbindung zwischen dem Praxis-PC und Doctolib stabil am Laufen, ohne dass sich jemand einloggen muss. Dadurch bleiben Synchronisationen, Signaturen oder Terminabrufe zuverlässig aktiv, selbst nach einem Neustart oder wenn gerade niemand am Rechner sitzt.

Tray-App:
Die Tray-App ist eine sehr kleine Zusatz-Anwendung, deren Symbol unten rechts im System-Tray neben der Uhr angezeigt wird.
Sie dient als sichtbare Bedienhilfe für das Team: Die Tray-App zeigt den aktuellen Status des Connectors (grün bedeutet „alles in Ordnung“, rot weist auf einen Fehler hin) und bietet per Rechtsklick praktische Funktionen wie „Neu synchronisieren“ oder „Log-Datei öffnen“. So lassen sich Störungen schnell erkennen und Routineaktionen unmittelbar auslösen.

API-Token:
Ein API-Token ist eine lange, zufällig erzeugte Zeichenfolge (zum Beispiel „d4f9…e8c2“), die wie ein digitaler Schlüssel funktioniert und den Zugriff auf die Doctolib-Schnittstelle (API) erlaubt.
Das Token weist den Connector eindeutig gegenüber Doctolib aus, ohne dass jedes Mal Benutzername und Passwort übertragen werden müssen – vergleichbar mit einem sicheren Zugangstoken in Banking-Apps. Das erhöht die Sicherheit und vereinfacht die automatische Kommunikation zwischen Praxis-System und Doctolib.

Kurzfazit:
Der Dienst sorgt im Hintergrund für den kontinuierlichen Betrieb und die Autostart-Verfügbarkeit.
Die Tray-App macht den technischen Zustand sichtbar und ermöglicht schnelle Aktionen mit zwei Klicks.
Das API-Token stellt die eindeutige, sichere Identität des Connectors gegenüber Doctolib her und erlaubt automatisierte, passwortlose Anfragen.


**Grenzen & Best Practices** 

- **Kalenderführung**: Termine liegen weiterhin allein in Doctolib; Medatixx bleibt Kalender-passiv. 
- **Datenumfang**: Es werden nur Stammdaten synchronisiert, **keine Befunde** oder Dokumente. 
- **Versionspflege**: Nach PVS-Updates kurz prüfen, ob der Connector-Dienst läuft (Tray-Icon = grün). 
- **Datenschutz**: Datenverkehr zwischen Connector und Doctolib-API ist TLS- verschlüsselt; sämtliche Zugriffe erscheinen im Praxis-Log des PMS. 

Wo passt ORM (Object-Relational Mapping) ins Bild? 

ORM ist eine „Schicht“, die SQL-Tabellendatensätze (Patienten, Termine) in Codeobjekte und wieder zurück verwandelt. 

Bei der Integration von Doctolib in das Klinikprogramm liest/schreibt der Konnektor über ORM einfach Daten in die lokale PVS-Datenbank und sendet sie an die Doctolib-API, ohne manuell SQL zu schreiben. 

**Typisches Szenario in einer Ebene Doctolib-Integration** 
1  Lokaldatenbank des PVS 
2  Middleware / Connector
3  Cloud-Backend von Doctolib
4  Eigenentwicklung / Reporting 

**Rolle von ORM** 
1  Praxis¬verwaltungs¬systeme wie Medatixx, tomedo oder x.isynet speichern Patienten-, Termin- und Abrechnungs¬daten in relationalen SQL-Datenbanken 
(PostgreSQL, MS SQL, MySQL …). 
2  Beim bidirektionalen Abgleich holt die Middleware neue Patienten¬einträge aus der PVS-Datenbank und übergibt sie als JSON an die Doctolib-API – und umgekehrt. 
3  Auch im Doctolib-Backend (Microservices) liegen Termin- und Nutzer¬daten in relationalen Clustern; API liefert sie als REST/FHIR-Objekte.
4  Praxis oder IT-Dienstleister schreibt ein kleines Tool, das PVS-Daten analysiert (Fehlzeiten-Statistik, Recall-Listen) und mit Doctolib-Daten mergen soll. 




**Kurz gesagt:** 

Wenn Entwickler\*innen einen Connector oder ein Analyse-Tool rund um Doctolib bauen, erleichtert ORM die Arbeit mit den relationalen Praxisdatenbanken: man programmiert auf Objektebene („termin.startzeit“), während das Framework die passende SQL-Abfrage erledigt. 

**Kalender in Doctolib:** 

- Der Doctolib-Kalender ist der zentrale Arbeitsplan für die Klinik. 
- In ihm werden Terminarten und Öffnungszeiten im Voraus festgelegt; Patienten buchen freie Zellen online. 
- Ein Mitarbeiter kann manuell Termine hinzufügen/verschieben, Patienten in eine digitale Warteschlange stellen, automatische Erinnerungen und „Recall“-Serien aktivieren. 
- Urlaube und Vertretungen sind mit ein paar Klicks markiert, und die Patientendaten werden mit dem lokalen Register synchronisiert. Auf diese Weise vermeidet die Klinik doppelte Einträge und Leerlaufzeiten. 




