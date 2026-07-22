# Uebungspruefungen - Statische Webseiten

Bearbeite jede Pruefung zuerst ohne Unterlagen. Die Loesungen stehen unten.

## Pruefung 1 - HTML

### Multiple Choice

1. HTML beschreibt: B 
   A) Layout  B) Struktur und Inhalt  C) Interaktion  D) Datenbanken
2. Richtige Reihenfolge beim Seitenaufruf: b
   A) HTTP, DNS, Rendering  B) DNS, HTTP-Anfrage, HTTP-Antwort, Rendering  C) Rendering, DNS, HTTP  D) Server fragt Browser
3. HTTP 404 bedeutet: c 
   A) Weiterleitung  B) OK  C) Seite nicht gefunden  D) Serverfehler
4. head enthaelt: b
   A) sichtbaren Inhalt  B) Metadaten wie title und charset  C) nur CSS  D) nur Bilder
5. br ist passend: b
   A) zwischen Absaetzen  B) fuer einen Umbruch in einer Adresse  C) fuer Fettdruck  D) fuer eine Liste
6. Dekoratives Bild: c 
   A) alt="Bild"  B) alt="datei.png"  C) alt=""  D) ohne alt
7. Relativer Bildpfad von index.html zu bilder/foto.jpg:b
   A) /bilder/foto.jpg  B) bilder/foto.jpg  C) https://bilder/foto.jpg  D) ../index.html/bilder/foto.jpg
8. Skalierbares Icon: b
   A) JPEG  B) SVG  C) GIF  D) BMP
9. caption steht:b
   A) vor table  B) als erstes Kind von table  C) in jedem tr  D) im tfoot
10. colspan="3" bedeutet:b
    A) drei Zeilen  B) drei Spalten  C) drei Tabellen  D) drei Kopfzeilen
11. name bei input ist: b
    A) sichtbares Label  B) Bezeichner beim Absenden  C) CSS-Klasse  D) Linkziel
12. Korrekte Label-Verbindung:a
    A) label for="mail" und input id="mail"
    B) label id="mail" und input for="mail"
    C) label href="mail"
    D) label name="mail"

### Fehlersuche

1. Korrigiere den Fehler:

~~~html
<h1>Anna</h2>
<p>Ich lerne HTML.</p>
~~~

2. Finde den Barrierefreiheitsfehler:

~~~html
<img src="bilder/profil.jpg">
<p>Mein Profilbild</p>
~~~

3. Kopfzeilen semantisch korrekt machen, inklusive scope:

~~~html
<table>
  <thead><tr><td>Technologie</td><td>Level</td></tr></thead>
  <tbody><tr><th>HTML</th><td>Gut</td></tr></tbody>
</table>
~~~

4. Warum ist das Label nicht verbunden?

~~~html
<label for="email">E-Mail</label>
<input type="email" id="mail" name="email">
~~~

5. Finde Sprungziel- und Linktext-Problem:

~~~html
<a href="#kontakt">Hier klicken</a>
<h2 id="contact">Kontakt</h2>
~~~

## Pruefung 2 - CSS, Flexbox und Grid

### Multiple Choice

1. Externes CSS:b
   A) style src  B) link rel="stylesheet" href="css/style.css"  C) script href  D) css-Tag
2. Selektor fuer class="karte":c
   A) #karte  B) karte  C) .karte  D) *karte
3. Welche Regel gewinnt?b
   A) p vor .intro  B) .intro vor p  C) immer die letzte  D) Browser-Standard
4. Welche Eigenschaft wird vererbt? c
   A) padding  B) border  C) color  D) width
5. width mit box-sizing: border-box umfasst:b
   A) nur content  B) content, padding und border  C) padding und border  D) auch margin
6. Flexbox aktivieren:b
   A) position:flex  B) display:flex  C) flex:true  D) layout:flex
7. Bei flex-direction:row wirkt justify-content auf:a
   A) Hauptachse/horizontal  B) Querachse/vertikal  C) erstes Item  D) Schrift
8. Horizontal und vertikal zentrieren: 
   A) justify-content:center; align-items:center;
   B) text-align:center; C) margin:auto; D) align-content:center;
9. flex:1 bedeutet:b
   A) 1px breit  B) flex:1 1 0  C) nur flex-grow:1  D) deaktiviert Flexbox
10. gap ist:b
    A) Aussenabstand  B) Abstand zwischen Items  C) Rahmenfarbe  D) Reihenfolge
11. order aendert nicht:b
    A) sichtbare Reihenfolge  B) HTML-Reihenfolge fuer Screenreader  C) Flex-Darstellung  D) Item-Position
12. Grid ist besonders passend:a
    A) zweidimensionales Raster  B) ein Button  C) Textfarbe  D) ein Link

### Fehlersuche

1. CSS wird nicht geladen:

~~~html
<link rel="stylesheets" href="css/style.css">
~~~

2. Die Navigation soll blaue Links erhalten:

~~~css
#navigation a { color: white; }
a { color: blue; }
~~~

3. Karte wird breiter als 300px:

~~~css
.karte { width:300px; padding:20px; border:2px solid #333; }
~~~

4. Logo links, Linkliste rechts:

~~~css
.navigation { display:flex; justify-items:space-between; align-items:center; }
~~~

5. Ungueltige Grid-Spalten:

~~~css
.seite { display:grid; grid-template-columns:250px, 1fr; }
~~~

## Loesungen

Pruefung 1, Multiple Choice: 1 B, 2 B, 3 C, 4 B, 5 B, 6 C, 7 B, 8 B, 9 B, 10 B, 11 B, 12 A.

Pruefung 1, Fehlersuche:

1. h1 muss auch mit /h1 geschlossen werden.
2. Einen sinnvollen Alternativtext ergaenzen, etwa alt="Portraet von Anna".
3. Kopfzeile: th scope="col"; Zeilenkopf: th scope="row".
4. for und id muessen identisch sein, z. B. for="mail".
5. href und id beide kontakt; Linktext z. B. "Zum Kontaktbereich".

Pruefung 2, Multiple Choice: 1 B, 2 C, 3 B, 4 C, 5 B, 6 B, 7 A, 8 A, 9 B, 10 B, 11 B, 12 A.

Pruefung 2, Fehlersuche:

1. rel="stylesheet".
2. #navigation a ist spezifischer; diese Regel auf color:blue aendern oder gleich spezifisch selektieren.
3. box-sizing:border-box ergaenzen, am besten global.
4. justify-content:space-between verwenden.
5. grid-template-columns:250px 1fr; - ohne Komma.

## Kurz-Checkliste

- HTML: Grundgeruest, Semantik, Links und Pfade, alt, Tabellen, Labels.
- CSS: Klasse, ID, Spezifitaet, box-sizing, margin versus padding.
- Flexbox: display:flex, Achsen, justify-content, align-items, gap, flex-wrap.
- Grid: display:grid, fr, Spaltenwerte ohne Komma.

---

## Pruefung 3 - Neue Beispiele, nur Kursstoff aus den PDFs

### Multiple Choice

1. Welche Rolle hat DNS beim Aufrufen von https://example.com?
   A) DNS gestaltet die Seite.  B) DNS uebersetzt den Domainnamen in eine IP-Adresse.
   C) DNS ersetzt HTTP.  D) DNS speichert nur Bilder.

2. Welche HTTP-Methode ist fuer eine Suchanfrage besonders geeignet?
   A) GET  B) POST  C) DELETE  D) PATCH

3. Wofuer steht Port 443 standardmaessig?
   A) HTTP  B) HTTPS  C) FTP  D) SSH

4. Welche HTML-Schicht beschreibt das Aussehen einer Webseite?
   A) HTML  B) CSS  C) JavaScript  D) DNS

5. Welche Liste verwendet man fuer eine Schritt-fuer-Schritt-Anleitung?
   A) ul  B) ol  C) dl  D) nav

6. Welches Attribut oeffnet einen Link in einem neuen Tab?
   A) href="_blank"  B) target="_blank"  C) rel="tab"  D) link="new"

7. Welche Aussage zu figure stimmt?
   A) figure ist fuer jedes Logo Pflicht.
   B) figure gruppiert ein Bild mit einer sinnvollen Beschriftung.
   C) figure ersetzt img.
   D) figure darf kein figcaption enthalten.

8. Welches Bildformat ist laut Kurs besonders passend fuer Fotos?
   A) SVG  B) WebP  C) BMP  D) TXT

9. Welche Kombination ist fuer eine externe Schrift im Dokument richtig?
   A) Ein link-Element im head und font-family im CSS
   B) Ein img-Element im body
   C) Nur color im CSS
   D) Eine ID auf body

10. Welche CSS-Einheit ist relativ zur Schriftgroesse des Elternelements?
    A) px  B) rem  C) em  D) fr

11. Welche Aussage zu margin und padding stimmt?
    A) margin ist Innenabstand, padding ist Aussenabstand.
    B) padding ist Innenabstand, margin ist Aussenabstand.
    C) Beide sind immer dasselbe.
    D) Beide werden immer vererbt.

12. Was ist der Standardwert von flex-direction?
    A) column  B) row  C) wrap  D) grid

13. Welche Eigenschaft verhindert, dass ein Flex-Item bei Platzmangel schrumpft?
    A) flex-grow: 0  B) flex-shrink: 0  C) flex-basis: 0  D) gap: 0

14. Was bedeutet flex-wrap: wrap?
    A) Die Items werden unsichtbar.
    B) Items duerfen auf eine neue Zeile umbrechen.
    C) Die Items werden immer gleich hoch.
    D) Der Container wird zu Grid.

15. Welche Grid-Spalten ergeben eine feste Sidebar und einen flexiblen Inhalt?
    A) 1fr 1fr  B) 250px 1fr  C) 250px, 1fr  D) auto auto auto

16. Welche Eigenschaft setzt die visuelle Reihenfolge von Flex-Items, ohne die HTML-Reihenfolge zu aendern?
    A) order  B) gap  C) align-self  D) flex-basis

### Fehlersuche

1. Der Link soll in einem neuen Tab sicher geoeffnet werden. Finde den fehlenden Teil.

~~~html
<a href="https://developer.mozilla.org" target="_blank">MDN</a>
~~~

2. Die Tabelle soll eine Ueberschrift haben, die Screenreader vor der Tabelle ansagen. Korrigiere die Position von caption.

~~~html
<caption>Wochenplan</caption>
<table>
  <tr><th>Tag</th><th>Thema</th></tr>
</table>
~~~

3. Der Text in p.intro soll gruen werden, tut es aber nicht. Warum?

~~~html
<p class="intro">Willkommen</p>
~~~

~~~css
p .intro { color: green; }
~~~

4. Die drei Karten sollen nebeneinander stehen und bei wenig Platz umbrechen. Korrigiere die CSS-Regel.

~~~css
.karten {
  display: flexbox;
  flex-wrap: wrap;
  gap: 1rem;
}
~~~

5. In einer Navigation soll das Logo links und die Linkliste rechts stehen. Welche Regel fehlt?

~~~css
.navbar {
  display: flex;
  align-items: center;
}
~~~

### Loesungen zu Pruefung 3

Multiple Choice: 1 B, 2 A, 3 B, 4 B, 5 B, 6 B, 7 B, 8 B, 9 A, 10 C, 11 B, 12 B, 13 B, 14 B, 15 B, 16 A.

Fehlersuche:

1. rel="noopener noreferrer" ergaenzen.
2. caption muss innerhalb von table stehen und dort das erste Kind sein.
3. p .intro sucht ein Element mit Klasse intro innerhalb eines p. Richtig ist p.intro { color: green; }.
4. display:flex verwenden, nicht display:flexbox.
5. justify-content:space-between; ergaenzen.

---

## Pruefung 4 - Responsive, Semantik, Barrierefreiheit und SEO

Diese Pruefung bezieht sich auf part05.pdf.

### Teil A: Multiple Choice

1. Was bedeutet Responsive Design? b 
   A) Eine Seite laedt nur auf Desktop-Computern.
   B) Dieselbe Seite passt sich an unterschiedliche Bildschirmgroessen an.
   C) Jede Geraeteart braucht eine eigene HTML-Datei.
   D) Nur die Schriftgroesse aendert sich.

2. Welcher Tag ist fuer eine responsive Webseite im head wichtig? a 
   A) meta name="viewport" content="width=device-width, initial-scale=1.0"
   B) meta name="desktop" content="true"
   C) link rel="mobile"
   D) img width="100%"

3. Was ist Mobile-first? b
   A) Erst Desktop gestalten und dann Mobile loeschen.
   B) Erst CSS fuer kleine Bildschirme schreiben, dann fuer groessere erweitern.
   C) Nur eine App entwickeln.
   D) Immer max-width verwenden.

4. Welche Media Query gilt ab einer Bildschirmbreite von 600px? b 
   A) @media (max-width: 600px)
   B) @media (min-width: 600px)
   C) @media (width: mobile)
   D) @media (screen: 600px)

5. Was bedeutet 1vw? b 
   A) 1 Pixel
   B) 1 Prozent der Viewport-Breite
   C) 1 Prozent der Schriftgroesse
   D) Eine Grid-Spalte

6. Was macht clamp(1.5rem, 5vw, 2.5rem)? b 
   A) Es setzt die Schrift immer auf 5px.
   B) Es laesst die Schrift zwischen Minimum und Maximum fliessend skalieren.
   C) Es versteckt die Schrift auf Mobile.
   D) Es setzt einen Rahmen.

7. Welche zwei Regeln machen Bilder meistens responsiv? b 
   A) width: 100%; height: 100%;
   B) max-width: 100%; height: auto;
   C) min-width: 100%; height: 200px;
   D) display: flex; gap: 1rem;

8. Was bewirkt object-fit: cover bei einem Bild in einer Karte? b 
   A) Das Bild wird immer vollstaendig mit Luecken angezeigt.
   B) Das Bild fuellt den Bereich, Teile duerfen abgeschnitten werden.
   C) Das Bild wird absichtlich verzerrt.
   D) Das Bild wird unsichtbar.

9. Welches Element darf als Hauptinhalt nur einmal pro Seite vorkommen? c 
   A) header  B) footer  C) main  D) section

10. Welches Element passt zu einer Link-Navigation? b 
    A) article  B) nav  C) address  D) time

11. Wann ist article passend? a
    A) Fuer einen eigenstaendigen Inhalt wie eine News oder Karte.
    B) Fuer jeden normalen Absatz.
    C) Nur fuer das Seitenlogo.
    D) Fuer den gesamten Browser-Tab.

12. Welche Aussage zu section stimmt? b 
    A) section ist immer ohne Ueberschrift.
    B) section gruppiert thematisch zusammengehoerige Inhalte und hat eine Ueberschrift.
    C) section ersetzt main.
    D) section ist nur fuer CSS erlaubt.

13. Wofuer steht :focus? c 
    A) Maus befindet sich ueber dem Element.
    B) Element wird gerade angeklickt.
    C) Element hat Tastaturfokus.
    D) Element ist das erste Kind.

14. Warum soll outline: none nicht ohne Ersatz verwendet werden?
    A) Es macht Bilder groesser.
    B) Tastaturnutzer sehen sonst nicht, welches Element fokussiert ist.
    C) Es verhindert alle Links.
    D) Es macht CSS langsamer.

15. Was waehlt li:nth-child(even)? b
    A) Jedes erste Listenelement.
    B) Jedes gerade Kind.
    C) Jedes letzte Kind.
    D) Alle ausser dem ersten Kind.

16. Wofuer verwendet man aria-label?
    A) Fuer einen direkten Namen, wenn kein sichtbarer Text vorhanden ist.
    B) Fuer die Schriftfarbe.
    C) Um ein Bild zu laden.
    D) Als Ersatz fuer jedes HTML-Element.

17. Welcher Kontrast ist fuer normalen Text nach WCAG AA mindestens noetig?
    A) 2:1  B) 3:1  C) 4,5:1  D) 7:1

18. Welche Taste geht zum naechsten fokussierbaren Element? b
    A) Escape  B) Tab  C) Shift  D) Pfeil rechts

19. Was ist die Aufgabe von meta description?
    A) Sie ist der sichtbare Haupttext der Seite.
    B) Sie liefert meist den Kurztext in Suchergebnissen.
    C) Sie ersetzt title.
    D) Sie macht Bilder responsive.

20. Wie viele h1 soll eine Seite laut Kurs haben?b
    A) Keine  B) Genau eine  C) Genau zwei  D) Beliebig viele

### Teil B: Fehlersuche

1. Korrigiere den Viewport-Tag.

~~~html
<meta name="viewport" content="width=device, initial-scale=1">
~~~

2. Auf kleinen Bildschirmen sollen die Karten untereinander stehen, ab 600px nebeneinander. Was ist an der Media Query falsch?

~~~css
.karten { display: flex; flex-direction: column; }

@media (max-width: 600px) {
  .karten { flex-direction: row; }
}
~~~

3. Das Bild darf nicht breiter als seine Karte werden und soll sein Seitenverhaeltnis behalten. Korrigiere:

~~~css
.karte img {
  width: 100%;
  height: 100%;
}
~~~

4. Ersetze die div-Suppe durch passende semantische Elemente: Kopfbereich, Navigation, Hauptinhalt, Seitenfuss.

~~~html
<div class="kopf">...</div>
<div class="navigation">...</div>
<div class="inhalt">...</div>
<div class="unten">...</div>
~~~

5. Der Link sieht beim Tastatur-Tabben nicht mehr aus wie ein fokussiertes Element. Korrigiere den Fokus-Stil barrierefrei.

~~~css
a:focus {
  outline: none;
}
~~~

6. Korrigiere die SEO-Ueberschriftenhierarchie.

~~~html
<h1>Portfolio von Samira</h1>
<h3>Ueber mich</h3>
<h4>Meine Skills</h4>
~~~

7. Der Icon-Button hat keinen sichtbaren Text. Ergaenze das passende ARIA-Attribut.

~~~html
<button><span aria-hidden="true">ICON</span></button>
~~~

Hinweis: Im echten Beispiel stuende hier nur ein Suchsymbol.

### Loesungen zu Pruefung 4

Teil A: 1 B, 2 A, 3 B, 4 B, 5 B, 6 B, 7 B, 8 B, 9 C, 10 B, 11 A, 12 B, 13 C, 14 B, 15 B, 16 A, 17 C, 18 B, 19 B, 20 B.

Teil B:

1. meta name="viewport" content="width=device-width, initial-scale=1.0".
2. Mobile-first: @media (min-width: 600px) verwenden, damit row erst ab 600px gilt.
3. max-width: 100%; height: auto; verwenden.
4. header, nav, main und footer verwenden.
5. Einen sichtbaren Ersatz setzen, zum Beispiel outline: 2px solid #7c6e58; outline-offset: 2px;.
6. Nach h1 folgt h2, zum Beispiel h2 fuer Ueber mich und h2 fuer Meine Skills.
7. Bei einem echten Icon ohne sichtbaren Text: button aria-label="Suche oeffnen". Ein normaler Text-Button braucht kein aria-label.
