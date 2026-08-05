🎪 Kirmes App 2026 – Kirmesteam Großenritte

Willkommen im offiziellen Repository der Kirmes App 2026 für das Kirmesteam Großenritte!

Diese Web-App dient als zentrales digitales Hauptquartier für das Festwochenende. Sie verbindet einen öffentlichen Bereich für Gäste mit einem geschützten Mitglieder- und Vorstandsbereich zur Schichtplanung, Kommunikation und Verwaltung.

📱 Features im Überblick

🌐 Öffentlicher Bereich (Für Gäste)

Kirmesprogramm: Übersicht über alle Veranstaltungen von Freitag bis Montag.

Eilmeldungen & Hinweise: Aktuelle Infos (z. B. Parkplätze, Programm-Updates) auf einen Blick.

Live-Stream Integration: Einbindung der Festzelt-Kamera (z. B. Raspberry Pi / YouTube Stream).

Foto-Galerie: Bildergalerie des Kirmesteams mit Party-Highlights.

Push-Benachrichtigungen: Web-Push-Simulation & Benachrichtigungs-Einstellungen für das Smartphone.

🔒 Interner Bereich (Für Helfer & Teammitglieder)

Schichtplaner: Einfaches Ein- und Austragen für Arbeitsdienste (Ausschank, Kasse, Auf- und Abbau).

Interne News: Geschützte Hinweise und Vorstands-Updates nur für das Kirmesteam.

Interne Abstimmungen: Schnell-Umfragen (z. B. Biersorten-Auswahl oder Helfer-Termine) ohne WhatsApp-Nachrichtensalat.

Foto-Upload: Direct-Post von Event-Fotos durch das Team.

⭐ Vorstands-Dashboard (Für Administratoren)

Rechte- & Mitgliederverwaltung: E-Mails von Helfern eintragen und Zugriffsrechte freischalten.

Ankündigungen verfassen: Neue Eilmeldungen schreiben und optional sofort als Push-Mitteilung aussenden.

Schichten anlegen: Neue Dienste mit Zeitfenster und benötigter Helferanzahl erstellen.

🛠️ Tech Stack & Architektur

Frontend: Single-Page-Application in HTML5, Tailwind CSS (via CDN) und Vanilla JavaScript.

Icons: FontAwesome 6.

Realtime-Cloud-Sync: Firebase SDK Integration & Broadcast Channel API für geräteübergreifende Echtzeit-Daten.

Kostenloses Backend (Optional): Anbindung an Google Sheets via Google Apps Script API zur einfachen Datenpflege ohne Datenbank-Kosten.

📁 Repository-Struktur

├── index.html                   # Hauptanwendung (Kirmes App SPA)
├── README.md                    # Diese Dokumentation
├── hosting_anleitung.md         # Schnell-Anleitung zum Online-Stellen
├── google_sheets_anleitung.md   # Anleitung zur Einrichtung des Google-Sheets-Backends
└── kirmes_app_konzept.html      # Interaktives Pitch-Deck / Konzept-Präsentation



🚀 Schnellstart & Installation

Die App benötigt keinen komplexen Build-Prozess (kein Node.js / NPM erforderlich). Sie läuft direkt im Webbrowser.

Local testen

Repository klonen oder ZIP herunterladen.

index.html per Doppelklick in einem beliebigen Browser (Chrome, Safari, Firefox, Edge) öffnen.

Online stellen (30 Sekunden)

Netlify Drop: Ordner mit der index.html einfach per Drag & Drop auf app.netlify.com/drop ziehen.

GitHub Pages: Repository auf GitHub hochladen und in den Repository-Einstellungen unter Settings ➔ Pages den Branch main aktivieren.

📊 Google Sheets als Datenbank verbinden

Damit der Vorstand Termine und Hinweise direkt in einer normalen Excel/Google-Tabelle pflegen kann:

Befolge die Schritte in der google_sheets_anleitung.md.

Trage deine erstelle Google Apps Script URL in der index.html ein:

const GOOGLE_SHEETS_API_URL = "https://script.google.com/macros/s/DEINE_WEB_APP_ID/exec";



👥 Rollen- & Rechtekonzept

In der App-Kopfzeile kann für Vorführ- und Testzwecke das Rollen-Auswahlmenü genutzt werden:

Rolle

Symbol

Zugriff & Rechte

Gast

👁️

Nur öffentliche Inhalte (Programm, öffentliche News, Live-Cam, Galerie)

Team-Mitglied

👥

Öffentliche Inhalte + Schichtplaner, interne News, Umfragen & Foto-Upload

Vorstand / Admin

⭐

Vollzugriff + Mitglieder-Verwaltung, Schichten erstellen & Eilmeldungen verfassen

📱 Als App auf dem Smartphone speichern (PWA-Workflow)

Gäste und Helfer können die Webseite ohne App Store wie eine native App nutzen:

iOS (iPhone / Safari): Teilen-Button drücken ➔ "Zum Home-Bildschirm".

Android (Chrome): Drei-Punkte-Menü drücken ➔ "App installieren" oder "Zum Startbildschirm hinzufügen".

📄 Lizenz & Nutzung

Erstellt für das Kirmesteam Großenritte 2026. Freie Nutzung und Anpassung für Vereins- und Festveranstaltungen gestattet.
