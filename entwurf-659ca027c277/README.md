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

Newsletter und Buch-Warteliste gehen an Brevo, in zwei getrennte Listen,
das Kontaktformular an Formspree. Die beiden Brevo-Adressen sehen fast
gleich aus; vertauscht man sie, landen beide Gruppen im falschen
Verteiler, ohne dass es auffällt. Konfiguriert wird das an genau einer Stelle, `ZIELE` in
`index.html`.

Brevo erlaubt den Zugriff auf die Antwort und meldet Erfolg oder Fehler
als JSON, nachgemessen. Deshalb ist der Dank dort ehrlich: er erscheint
erst, wenn Brevo die Anmeldung angenommen hat, und schlägt sie fehl,
steht Brevos eigener Grund da.

Formspree genauso: auch dort ist nachgemessen, dass die Antwort
gelesen werden darf. Die beiden Anbieter melden Fehler nur in
unterschiedlicher Form, Brevo als Objekt, Formspree als Liste; beide
werden ausgewertet.

Solange ein Ziel leer ist, sagt das Formular offen, dass es noch nicht
eingerichtet ist. Es zeigt kein „Danke" für etwas, das nie verschickt
wurde.

## Instagram

Vier Beiträge, direkt eingebettet und beim Aufruf sichtbar. Die
Rasterzelle ist `177.78% + 136px` hoch: das Hochformat des Videos plus
Kopf-, Aktions- und Fußleiste, die Instagram mitliefert. Ohne den
Zuschlag wird die Einbettung unten abgeschnitten.

Die Einbettungen laden beim Aufruf der Seite und kontaktieren damit
Meta, bevor jemand zugestimmt hat. Dafür verlangt § 25 TDDDG eine
vorherige Einwilligung. **Das ist vor dem Livegang zu lösen**, entweder
mit einer Einwilligungslösung oder indem die Clips selbst gehostet
werden. Der Datenschutztext benennt die Lücke.

## Schriften

Inter liegt unter `assets/fonts/` und wird von dieser Seite selbst
ausgeliefert, eine Datei mit allen Gewichten von 100 bis 900. Es geht
keine Anfrage an Google; nachgemessen.

## Offen

- **Formspree ohne AVV**: Der Endpunkt steht, aber ein
  Auftragsverarbeitungsvertrag ist dort nicht abschließbar. Damit fehlt
  die Grundlage nach Art. 28 DSGVO, und die Übermittlung in die USA hat
  keine benannte Grundlage nach Art. 44 ff. Vor dem Livegang zu klären:
  AVV beim Anbieter erfragen, Anbieter wechseln oder einen eigenen
  Endpunkt betreiben. Der Datenschutztext behauptet bewusst keinen
  Vertrag, solange keiner existiert.
- **Formspree-Einstellungen**: erlaubte Domains auf `drraphaelrbruno.de`
  begrenzen, falls der Tarif das hergibt. Die Adresse steht offen im
  Quelltext.
- **Einwilligung für die Instagram-Einbettungen**, siehe oben.
- **Bildnachweise** im Impressum bestätigen.
- Vor dem Livegang: Tor entfernen, `noindex` entfernen.
- `assets/portrait.webp` stammt aus der ersten Fassung und wird nicht
  mehr verwendet.
