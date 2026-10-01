# drraphaelrbruno.de

Eine Seite, keine Bauschritte. `index.html` enthält alles, daneben nur
`assets/`.

Ausgeliefert über GitHub Pages, Domain per `CNAME`.

## Was die Seite lädt

Nichts von Dritten. Die Schrift liegt unter `assets/fonts`, die Bilder
daneben. Es werden **keine Cookies gesetzt** und nichts im Browser
gespeichert, auch kein lokaler Speicher. Deshalb braucht die Seite
keinen Einwilligungs-Hinweis.

Erst beim Absenden eines Formulars geht etwas nach außen.

## Layout

Die Maße, die im Artboard aus dem Zustand kamen, kommen hier aus dem
Stylesheet: `:root` plus zwei Mediengrenzen bei 760 und 1100 Pixeln.
Dadurch sitzt das Layout schon beim ersten Anstrich richtig, statt nach
dem ersten Skriptlauf zu springen.

Die Navigationsleiste liegt fest und misst sich damit am Fenster, der
Inhalt darunter am Dokument. Wo eine Scrollleiste Platz wegnimmt, liefen
beide auseinander. Deshalb bekommt sie per Skript die Inhaltsbreite.

Bilder liegen als WebP vor.

## Die drei Formulare

Newsletter und Buch-Warteliste gehen an Brevo, in zwei getrennte Listen,
das Kontaktformular an Formspree. Konfiguriert wird das an genau einer
Stelle, `ZIELE` in `index.html`.

Die beiden Brevo-Adressen unterscheiden sich erst ab dem zwölften
Zeichen. Vertauscht man sie, landen beide Gruppen im falschen Verteiler,
ohne dass es auffällt.

Beide Anbieter erlauben den Zugriff auf ihre Antwort, das ist
nachgemessen. Deshalb wird sie gelesen, und Erfolg wie Fehler sind echt
— kein Dank für etwas, das der Dienst abgelehnt hat. Die Antworten sehen
unterschiedlich aus, Brevo meldet ein Objekt, Formspree eine Liste;
`grundFinden()` packt beide aus.

Ist ein Ziel leer, sagt das Formular das offen, statt eine Anmeldung
vorzutäuschen.

## Handouts

`/handouts/` ist eine Uebersicht mit allen zehn Blaettern, nach
Ueberblick, Werten, Alltag und Vorsorge gruppiert. Titel und
Einleitungssatz jeder Karte stammen woertlich aus dem jeweiligen PDF,
damit nichts dazuerfunden ist.

Darunter liegt je Thema ein Ordner mit dem PDF und einer schlanken
Seite, die es anzeigt und zum Herunterladen anbietet:

    /handouts/ausdauer/            /handouts/blutzucker-und-niere/
    /handouts/blutdruck/           /handouts/cholesterin/
    /handouts/deine-werte/         /handouts/ernaehrung/
    /handouts/krafttraining/       /handouts/krebsfrueherkennung/
    /handouts/rauchen/             /handouts/schlaf/

Von der Hauptseite ist nichts davon verlinkt. Indexierung ist erlaubt,
die Seiten tragen kein `noindex` mehr.

Beides zusammen heisst praktisch: gefunden wird vorerst nichts. Ohne
einen Verweis von irgendwoher und ohne Eintrag in einer `sitemap.xml`
kennt keine Suchmaschine die Adressen. Soll das anders sein, braucht es
eine Sitemap oder einen Verweis.

## Offen

- **Formspree ohne AVV**: Ein Auftragsverarbeitungsvertrag ist dort
  nicht abschließbar. Damit fehlt die Grundlage nach Art. 28 DSGVO, und
  die Übermittlung in die USA hat keine benannte Grundlage nach
  Art. 44 ff. Zu klären: AVV beim Anbieter erfragen, Anbieter wechseln
  oder einen eigenen Endpunkt betreiben. Der Datenschutztext behauptet
  bewusst keinen Vertrag, solange keiner existiert, nennt aber auch
  keine Grundlage für die Übermittlung in die USA. Das bleibt
  unvollständig, bis der AVV steht.
- **Formspree-Einstellungen**: erlaubte Domains auf
  `drraphaelrbruno.de` begrenzen, falls der Tarif das hergibt. Die
  Adresse steht offen im Quelltext.
- **Bildnachweise**: Der Block ist aus dem Impressum entfernt. Falls die
  Lizenzen der Fotografen eine Namensnennung verlangen, muss sie zurück,
  entweder im Impressum oder an den Bildern selbst.
- `assets/portrait.webp` stammt aus der ersten Fassung und wird nicht
  mehr verwendet.
