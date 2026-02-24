🎨 Willi's Kunst- und Bilderkatalog

Eine elegante, responsive Single-Page-Webanwendung (SPA) zur Präsentation einer privaten Kunstsammlung. Die Seite bietet detaillierte Beschreibungen und Analysen zu verschiedenen historischen und modernen Kunstwerken in einem professionellen Galerie-Layout.

✨ Features

Elegantes Galerie-Design: Inspiriert von echten Ausstellungskatalogen, mit zweispaltigem Textlayout auf großen Bildschirmen und edler Typografie (Google Fonts: Playfair Display und Lora).

Interaktive Sidebar-Navigation: Eine fixierte Seitenleiste ermöglicht das schnelle Springen zu bestimmten Kunstwerken. Die Navigation erkennt automatisch, welches Bild gerade betrachtet wird (Scroll-Tracking).

Custom Cursor Animation: Ein moderner, künstlerischer Mauszeiger, der sanft den Bewegungen folgt und bei interaktiven Elementen (Links, Bilder) organisch reagiert.

Scroll-Animationen (Fade-In): Die Kunstwerke blenden beim Herunterscrollen weich ein, was für ein flüssiges und modernes Nutzererlebnis sorgt.

Vollständig Responsive: Das Layout passt sich nahtlos an alle Bildschirmgrößen an. Auf mobilen Geräten verwandelt sich die Sidebar in ein platzsparendes, aufklappbares Menü.

📁 Projektstruktur

Das Projekt besteht aus einer einzigen HTML-Datei, in der CSS (Styling) und JavaScript (Logik für Cursor und Navigation) direkt integriert sind.

/
├── index.html        # Die Hauptdatei (HTML, CSS, JS)
└── src/              # Ordner für alle Bilddateien
    ├── Bild der Mythen.jpg
    ├── Rigi Original Zeichnung von Bullinger.jpg
    ├── Wunderschönes Altes Gemälde signiert.jpg
    └── ...           # Weitere Kunstwerke


Wichtig: Die Bilddateien im Ordner src/ müssen exakt so benannt sein, wie sie im src-Attribut der <img>-Tags in der index.html referenziert werden (inklusive Leerzeichen und Dateiendungen).

🚀 Deployment (Cloudflare Pages)

Dieses Projekt ist statisch und benötigt keinen Build-Prozess. Es ist perfekt für das Hosting über Cloudflare Pages geeignet.

Lade alle Dateien (die index.html und den src-Ordner mit den Bildern) in ein GitHub-Repository hoch.

Melde dich bei Cloudflare an und wechsle zu "Pages".

Erstelle ein neues Projekt und verbinde dein GitHub-Repository.

Wähle den main oder master Branch aus.

Framework-Voreinstellung: None (Keines)

Build-Befehl: (leer lassen)

Build-Ausgabeverzeichnis: (leer lassen, bzw. der Standard / ist korrekt)

Klicke auf Speichern und Bereitstellen.

Die Webseite ist nach wenigen Sekunden online und wird bei jedem Push auf GitHub automatisch aktualisiert!

✏️ Ein neues Kunstwerk hinzufügen

Um ein neues Bild zum Katalog hinzuzufügen, musst du zwei Dinge in der index.html anpassen:

In der Sidebar (<nav class="sidebar-nav">):
Füge einen neuen Link hinzu:

<a href="#neue-id">Titel des neuen Kunstwerks</a>


Im Hauptbereich (<main class="main-content">):
Füge den HTML-Block für das Kunstwerk hinzu. Achte darauf, dass die id mit dem href in der Sidebar übereinstimmt:

<section id="neue-id" class="artwork">
    <div class="artwork-image-container">
        <img src="./src/DeinNeuesBild.jpg" alt="Beschreibung">
    </div>
    <h2>Titel des Kunstwerks</h2>
    <div class="description">
        <p>Dein Beschreibungstext Absatz 1...</p>
        <p>Dein Beschreibungstext Absatz 2...</p>
    </div>
</section>
