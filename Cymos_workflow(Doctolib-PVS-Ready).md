Übersicht des Prozessflusses (in Alltagssprache) 

1. **Anfrage Tech-Audit kommt rein** 

   *Trigger:* E-Mail an das zentrale Postfach (im Board genannt). 

   *Ziel:* Audit anstoßen, Basisinfos einsammeln 

2. **CK leitet an den Helpdesk weiter** 

   *Rolle:* „CK“ (= Christian Kokot) fungiert als Intake/Dispatcher. 

   *Ziel:* Ticket im Helpdesk anlegen, Standard-Workflow starten. 

3. **Helpdesk legt Kund\*in in Autotask an & terminiert** 

   *Aktionen:* Account/Standort anlegen, Termin(e) vorschlagen, technische Vorab-Infos anfordern (z. B. Ansprechpartner, Geräte-/Passwort-Bereitstellung, Netzwerkzugang). 

4. **Tech-Audit vor Ort / remote beim Kunden** 

   *Inhalte (Beispiele aus deinem Projektumfang):* 

- **TI-Konformität:** Konnektor-Daten (IP/Port 443, Zertifikate, Client-System-ID), Kartenterminals je Arbeitsplatz, SMC-B/HBA Zuordnung. Doctolib-seitig liegen die Konnektor-Parameter in den TI-Einstellungen (Standort, Mandant-ID, Zertifikate usw.).  
- **GDT-Anbindung medizinischer Geräte:** Export (Auftrag aus DL ans Gerät) + Import (Befundrücklauf via synchronisierten Ordner mit Pfad/Zeichensatz/Untersuchungscode).  
- **Mobile Kartenterminals:** Treiberpfade prüfen (Windows/macOS), DDV- Konfiguration, Architektur-Einschränkungen (keine ARM64-Unterstützung auf Apple Silicon).  
- **Direktdruck:** Prüfen, ob IPP-Drucker korrekt entdeckt sind; Standard- und Dokumenttyp-Profile (z. B. AU) einrichten.  
- **Netzwerk/ISA/Firewall/VPN/Internet:** IP-Plan, VLANs, DHCP/DNS, NAT/ACLs, Site-to-Site-/Remote-VPN, Gast-/Med-Netz-Trennung. 
- **Inventarisierung PVS/DB-Server:** PVS-Servername & -Pfad der DB-Verbindung dokumentieren. 
- **Peripherie:** Drucker, Scanner, Kartenleser (TI/eGK/EC), Labor- /Diagnoseanbindungen. 
- **IT-Sicherheit:** Updates, AV/EDR, Backup (3-2-1), Rechte, Protokollierung. 
5. **Interne Nachbearbeitung** 

   *Aktion:* Audit-Sheet vervollständigen, in „Mail-Sheet“/zentrales Sheet übertragen, Dateien ablegen (z. B. SharePoint, ITGlue). 

   *Ziel:* Saubere, durchsuchbare Wissensbasis. 

6. **Audit-Bericht & Angebotserstellung** 

   *Aktion:* E-Mail mit Bericht (Vorlage) an Endkund\*in, CC CK und „Ranger“, ggf. **Angebot für „Doctolib-PVS-Ready“** beilegen/auslösen. 

   *Tipp:* Berichts-PDF + Angebotsbezug im selben Thread; Vorlage zentral ablegen. 

7. **Vertrieb übernimmt** 

   *Aktion:* Kontakt zum Endkunden bzgl. Wartungsvertrag; Nachfassen zu „Doctolib PVS-Ready“ Komponenten. 

   *Ziel:* Abschluss/Beauftragung. 

8. **Ende & Follow-ups** 

   *Aktion:* Warten/gezielt nachfassen, ob Kund\*in **PVS bei Doctolib bucht**. Offene Punkte in Logbuch pflegen. 

**RACI (wer macht was?)** 

- **Anfrage/Weiterleitung:** Kunde → CK (R/A) 
- **Ticket/Terminierung:** Helpdesk (R), CK (C) 
- **Audit vor Ort/remote:** Techniker:in/ITSP (R), Kunde (A für Zugänge), CK (C) 
- **Nachbearbeitung/ITGlue/Sheets:** Techniker:in (R), CK (C) 
- **Bericht/Angebot:** Techniker:in (R für Bericht), Vertrieb (R für Angebot), CK (C) 
- **Vertrieb & Nachfassen:** Vertrieb (R), CK (C), Kunde (A) 

**Begriffserklärungen (Einsteiger-freundlich)** 

- **TI (Telematikinfrastruktur):** Deutsches, sicheres Gesundheitsnetz, z. B. für ePA/eRezept/KIM. Anschluss via zertifiziertem **Konnektor**, Kartenterminals, SMC- B/HBA. Doctolib nutzt hierfür eine TI-Konfiguration (Konnektor-Host/IP, Port 443, Zertifikate, Client-System-ID).  
- **Konnektor:** „TI-Router“ der Praxis; stellt die gesicherten TI-Dienste bereit, üblicherweise per IP:443 erreichbar.  
- **SMC-B/HBA:** Chipkarten zur Identifikation der Praxis (SMC-B) bzw. der Leistungserbringer (HBA) in der TI.  
- **DDV / Doctolib EHR (lokal):** Lokale Komponente, die u. a. Geräte, GDT, Druck und TI-Arbeitsplätze verbindet; Voraussetzung für eindeutige Geräte-IDs in der TI.  
- **GDT (Gerätedatenträger-Schnittstelle):** Standard zum Austausch von Aufträgen/Befunden mit Medizingeräten. Export = Auftrag ans Gerät; Import = Befund zurück ins PVS.  
- **Direktdruck/IPP:** Direktes Senden von PDFs an netzwerkfähige Drucker via IPP; Dokumenttyp-spezifische Profile (z. B. AU) sind möglich.  

**Minimal-Artefaktliste (was ihr je Auditfall ablegt)** 

- **01\_Intake:** Ticket, Stammdaten, Terminbestätigung 
- **02\_Vorbereitung:** Audit-Sheet (leer), Projektordner-Link 
- **03\_Audit:** TI-Screenshots + Werte (Standort, Mandant-ID, Zertifikate, Konnektor- IP:443, Client-System-ID), GDT-Export/Import-Konfig (Dateiname, Ordnerpfade, Zeichensatz, Untersuchungsgruppe/-code), Drucker-Profile, Netzskizze/Portliste, DB- Verbindungsdaten, Gerätematrix (Drucker, Kartenleser, Labor, Diagnose) 
- **04\_Nacharbeit:** Finales Audit-Sheet, Bericht-PDF, Angebot, Follow-up-Termin 

**Häufige Stolpersteine & schnelle Checks** 

- **TI-Handshake schlägt fehl:** Zertifikat/Passwort/Client-System-ID prüfen, Port **443** offen?  
- **GDT kein Befund:** Falscher **Ordnerpfad** oder kein Sync-Ordner in DDV; Zeichensatz/Untersuchungscode prüfen.  
- **Mobiler Leser tut nicht:** Treiberpfad falsch oder Gerät zu früh angesteckt; **keine ARM64-Macs** unterstützt.  
- **Direktdruck „nicht kompatibel“:** IP/Hostname am Drucker kontrollieren, IPP & PDF-Fähigkeit sicherstellen.  

Если кратко по-русски (итог): 

1\.  Получаем запрос на тех-аудит → 2) Диспетчер отправляет в хелпдеск → 3) 

Создаём тикет и назначаем дату → 4) Проводим аудит (TI/коннектор, GDT, карты, печать, сеть, БД) → 5) Заполняем отчёт и базу знаний → 6) Отправляем отчёт + оффер «Doctolib-PVS-Ready» → 7) Продажи связываются по договору обслуживания → 8) Фоллоу-ап: подтверждаем, что клиент оформил PVS в Doctolib. Основные тех-точки: корректная TI-конфигурация (IP:443, сертификаты), GDT экспорт/импорт (путь/кодировки), драйверы мобильных картридеров (нет поддержки ARM64 Mac), IPP-печать с профилями по типам документов. 
