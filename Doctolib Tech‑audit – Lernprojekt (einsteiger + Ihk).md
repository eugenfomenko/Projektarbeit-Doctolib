Doctolib Tech‑Audit – Lernprojekt 

Ziel: Eine Arztpraxis von der Planung bis zum Go‑Live auditieren, dokumentieren und migrieren. Diese Vorlage führt dich Schritt für Schritt – inkl. Tabellen, Definitionen und Checklisten – und bildet eine **chronologische Ereigniskette** ab. 

1) Mini‑Glossar (einfache Worte) 
- **TI (Telematikinfrastruktur):** Sicheres Netz des Gesundheitswesens in DE. 
- **Konnektor:** „TI‑Modem“ der Praxis; verbindet lokal zur TI. 
- **SMC**‑**B / HBA:** Praxiskarte / Heilberufsausweis für Authentisierung/Signatur. 
- **KIM:** Sichere E‑Mail in der TI (Arzt‑zu‑Arzt, etc.). 
- **DDV:** Lokale Doctolib‑Komponente für Geräte/TI/Druck. 
- **GDT:** Austauschformat zwischen PVS und Medizingeräten. 
- **Direktdruck (IPP/PDF):** Druck direkt an definierte Drucker/Schächte. 
2) Praxis‑Inventur (Bestandsaufnahme) 

**Ziel:** Alle Geräte, Anschlüsse und Rollen erfassen. Diese Tabelle ist die Basis für TI‑, Druck‑ und GDT‑Konfiguration. 

Praxis-Inventur (Bestandsaufnahme) – ausformuliert ohne Tabellen

Die Praxis-Inventur soll alle Geräte, Anschlüsse und Rollen vollständig erfassen und bildet damit die Grundlage für die spätere TI-, Druck- und GDT-Konfiguration. Für jeden Raum hältst du in ganzen Sätzen fest, welches Gerät dort steht, wie es angebunden ist und wofür es genutzt wird. Am Empfang vermerkst du beispielsweise, dass ein PC-Arbeitsplatz per LAN angebunden ist und als Anmeldungsplatz dient. Direkt daneben beschreibst du, dass ein eGK-Terminal entweder per USB am PC oder per LAN angeschlossen ist und als Kartenleser für eGK/KVK fungiert. Im Raum „B1“ notierst du, dass ein Netzwerkdrucker über LAN erreichbar ist, vorrangig Formulare druckt und für A4-Dokumente einen bestimmten Schacht (etwa Schacht 1 für Überweisungen oder Schacht 2 für E-Rezepte) verwendet. Im Technikraum dokumentierst du, dass der TI-Konnektor per LAN angeschlossen ist, alternativ ein TI-Gateway bereitsteht und Port/Verkabelung eindeutig beschriftet sind. Im Labor hältst du fest, dass ein Diagnosegerät entweder per USB am Client oder per LAN angebunden ist und Befunde über GDT an das Praxis-System übergibt; zusätzlich schreibst du den Dateipfad für Ein- und Ausgänge dazu.

Für eine eindeutige Zuordnung vergibst du Inventar-IDs nach einem festen Schema. Du notierst ausdrücklich, dass „RCP-EMP-01“ für den PC am Empfang steht, „PRN-B1-01“ den Drucker im Raum B1 kennzeichnet, „CT-KONN-01“ den Konnektor bezeichnet und „SW-01“ den zentrales Switch markiert. Dieses Nomenklaturschema schreibst du einmal ausführlich auf, damit jede:r in der Praxis es anwenden kann.

3) Netzwerk-Skizze (Topologie & ISA) – in Worten beschrieben

Du beschreibst den Signalfluss von außen nach innen in einem Satz: „Das Internet führt auf unseren Router mit integrierter Firewall; von dort geht es in den Core-Switch; daran hängen die PCs, die Netzwerkdrucker, der TI-Konnektor, die eGK-Terminals und die Laborgeräte.“
Anschließend benennst du die IP-Segmente: Das Praxis-LAN nutzt zum Beispiel den Adressbereich 192.168.10.0/24. Ein optionales Geräte-VLAN für Drucker, Terminals und Laborgeräte läuft getrennt im Bereich 192.168.20.0/24. Du hältst fest, dass Routing zwischen den Netzen nur dort erlaubt ist, wo es technisch notwendig ist, und dass Broadcast-Domänen durch VLANs klar getrennt bleiben.

Die Informationssicherheits-Aspekte (ISA) formulierst du ebenfalls in ganzen Sätzen. Du schreibst, dass die Firewall eingehende Verbindungen grundsätzlich blockiert und ausgehende Verbindungen auf definierte Ziele beschränkt sind, zum Beispiel nur KIM-, Update- und Zeitdienste. Du erklärst, dass die Fernwartung ausschließlich per VPN mit starker Authentisierung erfolgt. Außerdem beschreibst du euer Patch-Management, die Backup-Strategie sowie die Rollen- und Rechtevergabe für Benutzerkonten und Dienste.

4) TI & Kartenleser – Daten und Zuordnung verständlich notiert

Für den Konnektor (oder das TI-Gateway) beschreibst du Hersteller und Modell, die IP-Adresse oder den Hostnamen, die verwendeten Ports, den Standort im Gebäude sowie den Firmwarestand. Du erwähnst die Zertifikate und wie deren Ablauf überwacht wird.
Zur SMC-B schreibst du die Seriennummer und den Steckplatz auf, an dem sie betrieben wird. Für die Heilberufsausweise (HBA) ordnest du jede Karte einem konkreten Arbeitsplatz zu und beschreibst, wie die HBA-Nutzung bei Signaturen organisatorisch geregelt ist.

Das Terminal-Mapping formulierst du als klare Zuordnung in Sätzen: „Der Arbeitsplatz RCP-EMP-01 ist mit dem Kartenleser eGK-EMP-LAN-01 verbunden, der per LAN angebunden ist und den aktuellen Treiberstand x.y.z verwendet. Der Arbeitsplatz RCP-B1-02 nutzt das USB-Terminal eGK-B1-USB-01; USB-Port und Treiberversion sind dokumentiert.“ So ist jederzeit nachvollziehbar, welcher Arbeitsplatz welchen Kartenleser nutzt und welcher Treiberstand installiert ist.

5) Direktdruck – Matrix als Fließtext

Statt einer Druck-Matrix beschreibst du pro Dokumententyp den zugeordneten Drucker, die Druck-Queue und den Papier- oder Schachteinzug.
Du schreibst beispielsweise: „Arbeitsunfähigkeitsbescheinigungen (AU) werden über den Drucker PRN-B1-01 ausgegeben. Die IPP-Queue lautet ipp://192.168.10.25/ipp/print. Verwendet wird Schacht 2 mit gelbem Papier.“
Für Rezepte hältst du fest: „Rezepte werden standardmäßig am Empfang über PRN-EMP-01 gedruckt. Als Alternative steht PRN-B1-01 bereit. Die zweite Druck-Queue ist unter ipp://192.168.10.26/ipp/print erreichbar. Für E-Rezepte auf Blankopapier wird Schacht 1 verwendet; für klassische Rezeptrollen ist der Rollen-Einzug definiert.“
Für Überweisungen formulierst du analog, welcher Drucker, welche Queue und welcher Schacht zu nutzen ist. Zusätzlich notierst du Besonderheiten wie Duplexdruck, Briefpapier oder die Anforderung, dass bestimmte Dokumente ohne Dialog per Direktdruck ausgegeben werden.

6) GDT-Anbindung (Medizingeräte) – Import/Export und Testfälle in Prosa

Für jedes Medizingerät beschreibst du Typ, Anschlussart und die GDT-Pfade. Du formulierst etwa: „Das EKG-Gerät ist per USB am Client angebunden und nutzt GDT. Aufträge werden in den Ordner C:\GDT\OUT exportiert. Befunde werden aus C:\GDT\IN vom Praxis-System eingelesen. Die Befunde werden als PDF mit zugehöriger GDT-Steuerdatei abgelegt.“
Analog beschreibst du weitere Geräte (zum Beispiel Spirometrie, Langzeit-RR oder Audiometrie) und hältst fest, auf welchen UNC-Pfaden im Netzwerk die Dateien liegen, wenn sie über LAN angebunden sind.
Du ergänzt Testfälle in ganzen Sätzen: „Zur Abnahme wird ein Test-Patient angelegt. Aus dem PVS wird ein GDT-Auftrag erzeugt; das Gerät empfängt den Auftrag und erstellt einen Befund. Der Befund erscheint anschließend automatisch in der Patientenakte. Der Test gilt als OK, wenn Auftrag, Messung und Befund ohne Fehlermeldung durchlaufen und die Zuordnung zum richtigen Patienten stimmt.“

Zusammenfassung
Inventur: Jedes Gerät wird räumlich, technisch und funktional beschrieben; die Inventar-ID folgt einem festen Schema wie RCP-EMP-01 oder PRN-B1-01.
Netz: Die Topologie verläuft von Internet über Router/Firewall und Core-Switch zu Endgeräten; VLANs trennen Praxis-LAN und Geräte-Netz; Firewall- und VPN-Regeln sind klar formuliert.
TI: Konnektor/Gateway, SMC-B, HBA und Kartenleser-Mapping sind in Sätzen dokumentiert, einschließlich Firmware, Treiberstand und Zertifikatsverwaltung.
Druck: Für jeden Dokumententyp steht ein definierter Drucker mit Queue und Schacht fest; Besonderheiten wie Papierfarbe oder Direktdruck sind erläutert.
GDT: Geräte, Anschlüsse, GDT-Pfade und Testverfahren sind beschrieben; der Abnahmetest ist als verständlicher Ablauf formuliert.
Damit liegen alle vormals tabellarischen Inhalte als vollständige, nachvollziehbare Sätze vor und können direkt in die Praxis-Doku übernommen werden.


7) Chronologische Ereigniskette (Projektlogbuch) 

Ziel: Von der Planung bis zum Go-Live wird das Projekt in nachvollziehbaren Schritten beschrieben, jeweils mit Aufgabe, Verantwortlichen und Ergebnis.

T-21 (Planung): Das Projekt startet mit einem Kick-off, in dem die Ziele verbindlich definiert werden; verantwortlich ist die Projektleitung (PM), und als Ergebnis entsteht ein abgestimmtes Protokoll.

T-14 (Audit): Die technische Inventur ist abgeschlossen; die Durchführung liegt beim Technikteam, und das Ergebnis ist eine vollständige Asset-Liste.

T-10 (Netz): Die Netzwerktopologie einschließlich der Informationssicherheitsaspekte (ISA) ist dokumentiert; zuständig ist das Technikteam, und als Artefakt liegt eine geprüfte Netz-Skizze vor.

T-7 (TI): Der TI-Konnektor und alle Kartenterminals sind konfiguriert; verantwortlich ist das Technikteam, und das Ergebnis ist ein ausgefülltes TI-Datenblatt.

T-5 (Druck): Die Direktdruck-Matrix wurde erfolgreich getestet; das Technikteam führt die Tests durch, und als Nachweis entsteht ein Testprotokoll.

T-3 (GDT): Die Geräteimporte über GDT sind getestet; verantwortlich ist das Technikteam, und als Ergebnis wird ein repräsentatives Befund-Beispiel abgelegt.

T-1 (Migration): Der Downtime-Plan mit Backup ist final; Projektleitung und Technikteam verantworten diesen Schritt gemeinsam, und als Artefakt liegt ein freigegebener Plan mit Checkliste vor.

T (Go-Live): Die Abnahme des Systems ist erfolgt; verantwortlich zeichnet die Praxisleitung, und das Ergebnis ist ein unterschriebenes Abnahmeprotokoll.


8) Checklisten (Kurzform) 
- **TI**‑**Konformität:** Karten/Slots, Zertifikate, Firmware, KIM. 
- **Internet & Sicherheit:** Bandbreite, Router/Firewall, VPN, Updates. 
- **Netzwerk (ISA):** Segmente/VLANs, IP‑Plan, DNS/DHCP, Logging. 
- **Geräte:** PCs, Drucker (IPP), Kartenleser, Labor/Diagnose. 
- **Druck:** Dokumententypen, Schachtzuordnung, Testausdrucke. 
- **GDT:** Pfade, Dateiformate, Round‑Trip‑Test. 
- **Migration:** Datenpfade PVS, Backup, Fallback, Abnahme. 

Tipp: Nach jedem Abschnitt eine Mini‑Probe (1–2 Tests) dokumentieren. 

[ref1]: Aspose.Words.d9215745-d6c5-4cab-aa8f-3d55001fff64.008.png
[ref2]: Aspose.Words.d9215745-d6c5-4cab-aa8f-3d55001fff64.002.png

