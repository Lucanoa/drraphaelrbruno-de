# Entwurf

Umgesetzt aus dem Artboard `Landingpage Dr Bruno v2.dc.html`.

Nicht öffentlich. `noindex, nofollow`, nirgends verlinkt, der Pfad ist zufällig.

Davor liegt ein Tor mit dem Wort `1000`. Das ist **kein Schutz**: das Wort steht
im Quelltext und das Repo ist öffentlich. Es hält zufällige Besucher ab, mehr
nicht.

## Wie der Entwurf gebaut ist

Alles steckt in `index.html`, es gibt keinen Bauschritt.

Die Maße, die im Artboard aus dem Zustand kamen, kommen hier aus dem
Stylesheet (`:root` plus zwei Mediengrenzen bei 760 und 1100 Pixeln).
Dadurch sitzt das Layout schon beim ersten Anstrich richtig, statt nach
dem ersten Skriptlauf zu springen.

Bilder liegen als WebP vor. Die Vorlagen aus dem Handoff wogen zusammen
5,6 MB, als WebP sind es 288 KB.

## Die drei Formulare

Newsletter und Buch-Warteliste gehen an Brevo, das Kontaktformular an
Formspree. Konfiguriert wird das an genau einer Stelle, `ZIELE` in
`index.html`.

Brevo erlaubt den Zugriff auf die Antwort und meldet Erfolg oder Fehler
als JSON, nachgemessen. Deshalb ist der Dank dort ehrlich: er erscheint
erst, wenn Brevo die Anmeldung angenommen hat, und schlägt sie fehl,
steht Brevos eigener Grund da.

Formspree läuft über einen unsichtbaren Rahmen, weil dort noch nicht
nachgemessen ist, ob die Antwort gelesen werden darf. Dabei wissen wir
nur, DASS gesendet wurde.

Solange ein Ziel leer ist, sagt das Formular offen, dass es noch nicht
eingerichtet ist. Es zeigt kein „Danke" für etwas, das nie verschickt
wurde.

## Instagram

Vier Beiträge, im Zwei-Klick-Verfahren. Vor dem Klick geht keine Anfrage
an Meta; nachgemessen. Erst der Klick öffnet ein Overlay mit der
Einbettung. Inline ging nicht, weil die Einbettung Kopf- und Fußleiste
mitbringt und in der schmalen Rasterzelle beschnitten würde.

## Offen

- **Buch-Warteliste**: eigenes Brevo-Formular anlegen, Adresse in `ZIELE`.
  Die Newsletter-Adresse dort einzutragen würde beide Gruppen in dieselbe
  Liste werfen.
- **Kontaktformular**: Formspree-Adresse in `ZIELE`, dazu dort den AVV
  abschließen und die erlaubten Domains auf `drraphaelrbruno.de` setzen.
- **Inter selbst hosten**, damit beim Aufruf keine Verbindung zu Google
  entsteht. Der Datenschutztext sagt das zu.
- **Bildnachweise** im Impressum bestätigen.
- Vor dem Livegang: Tor entfernen, `noindex` entfernen.
- `assets/portrait.webp` stammt aus der ersten Fassung und wird nicht
  mehr verwendet.
