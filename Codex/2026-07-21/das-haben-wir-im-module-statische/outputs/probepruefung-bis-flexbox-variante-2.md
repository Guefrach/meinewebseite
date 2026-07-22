# Probepruefung Variante 2: Bis einschliesslich Flexbox

**Arbeitszeit: 60 Minuten.** Nur HTML, CSS und Flexbox aus den Kursunterlagen.

## Teil A - Multiple Choice

1. Welche Aufgabe hat ein Webserver? b
   A) Er interpretiert CSS im Browser. B) Er beantwortet HTTP-Anfragen und liefert Dateien aus. C) Er ersetzt DNS. D) Er schreibt HTML automatisch.

2. Welcher Statuscode steht fuer eine erfolgreiche HTTP-Anfrage? a
   A) 200 B) 301 C) 404 D) 500

3. Welche Aussage zu IPv4 ist richtig? a
   A) Vier durch Punkte getrennte Zahlen. B) Acht Hexadezimal-Bloecke. C) Ein Dateiformat. D) Eine CSS-Einheit.

4. Wozu dient das lang-Attribut im html-Element? b
   A) Es setzt die Schriftgroesse. B) Es gibt die Sprache der Seite an. C) Es setzt ein Passwort. D) Es laedt CSS.

5. Welches Element erzeugt eine ungeordnete Liste?b
   A) ol B) ul C) li D) dl

6. Welches Attribut gibt das Ziel eines Links an?b
   A) src B) href C) alt D) target

7. Welcher Link startet eine E-Mail an info@beispiel.de?b
   A) href="email:info@beispiel.de"
   B) href="mailto:info@beispiel.de"
   C) href="tel:info@beispiel.de"
   D) href="#info@beispiel.de"

8. Welches Attribut verhindert Layout-Spruenge beim Laden eines Bildes?a
   A) width und height B) target C) colspan D) method

9. Wann verwendet man figure mit figcaption?a
   A) Fuer ein Bild mit sichtbarer Bildunterschrift. B) Fuer jeden Link. C) Fuer ein Formular. D) Fuer CSS.

10. Wofuer ist tfoot gedacht?c
    A) Tabellenkopf B) Hauptdaten C) Summen oder Anmerkungen am Tabellenende D) Bildunterschrift

11. Was bewirkt rowspan="2"?b
    A) Zelle belegt zwei Spalten. B) Zelle belegt zwei Zeilen. C) Zwei Tabellen entstehen. D) Zwei Bilder werden geladen.

12. Welche Eingabe erlaubt genau eine Wahl aus einer Gruppe?b
    A) checkbox B) radio C) password D) textarea

13. Welche CSS-Einbindung ist in der Praxis bevorzugt?c
    A) Inline style B) style-Tag C) externes Stylesheet D) Kein CSS

14. Welche Regel gilt bei gleicher Spezifitaet?b
    A) Die fruehere Regel gewinnt. B) Die spaetere Regel gewinnt. C) ID gewinnt immer. D) Browser-Standard gewinnt immer.

15. Was ist ein Aussenabstand?b
    A) padding B) margin C) border D) content

16. Welcher display-Wert nimmt normalerweise die volle Breite und beginnt eine neue Zeile?b
    A) inline B) block C) inline-block D) flex-item

17. Welche Einheit ist relativ zur Schriftgroesse des Wurzelelements?b
    A) px B) rem C) em D) fr

18. Was ist der Standardwert von flex-grow?a
    A) 0 B) 1 C) auto D) 100

19. Was setzt flex-basis?a
    A) Die Startgroesse vor grow und shrink. B) Die Farbe. C) Die HTML-Reihenfolge. D) Den Aussenabstand.

20. Welche Aussage zu order stimmt?b
    A) Es aendert die HTML-Reihenfolge. B) Es aendert nur die visuelle Reihenfolge. C) Es macht ein Item unsichtbar. D) Es ist ein Bildformat.

## Teil B - Fehlersuche und Korrektur

1. Liste:

~~~html
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ol>
~~~

2. Link:

~~~html
<a src="kontakt.html">Kontaktseite</a>
~~~

3. Bild: Das Logo ist im Ordner images, es hat einen transparenten Hintergrund und ist wichtiger Inhalt.

~~~html
<img src="logo.png" alt="">
~~~

4. Tabelle: Die Zelle Wochenplan soll ueber drei Spalten gehen.

~~~html
<table>
  <tr><th rowspan="3">Wochenplan</th></tr>
  <tr><td>Montag</td><td>Dienstag</td><td>Mittwoch</td></tr>
</table>
~~~

5. Formular: Beide Radio-Buttons sollen eine Gruppe bilden, aus der man genau einen Kurs waehlt.

~~~html
<input type="radio" id="html" name="html">
<label for="html">HTML</label>
<input type="radio" id="css" name="css">
<label for="css">CSS</label>
~~~

6. CSS: Nur Links innerhalb der Navigation sollen weiss werden.

~~~css
nava {
  color: white;
}
~~~

7. CSS: Der Button soll 200px Gesamtbreite inklusive padding und border haben.

~~~css
.button {
  width: 200px;
  padding: 12px;
  border: 1px solid black;
  box-sizing: content-box;
}
~~~

8. Flexbox: Drei Karten sollen gleich viel Restplatz bekommen. Sie stehen als direkte Kinder in karten.

~~~css
.karten { display: flex; }
.karte { flex-grow: 0; }
~~~

9. Flexbox: Die Linkliste soll im Navbar-Container horizontal mit 24px Abstand erscheinen.

~~~css
.nav-links {
  display: block;
  gap: 24px;
}
~~~

## Loesungen

Teil A: 1 B, 2 A, 3 A, 4 B, 5 B, 6 B, 7 B, 8 A, 9 A, 10 C, 11 B, 12 B, 13 C, 14 B, 15 B, 16 B, 17 B, 18 A, 19 A, 20 B.

Teil B:

1. ul muss mit /ul geschlossen werden.
2. Ein Link braucht href: a href="kontakt.html".
3. Der richtige Pfad ist images/logo.png; ein wichtiges Logo braucht einen beschreibenden alt-Text.
4. colspan="3" verwenden, nicht rowspan="3".
5. Beide Radio-Buttons brauchen denselben Namen, etwa name="kurs".
6. Der Nachfahr-Selektor braucht ein Leerzeichen: nav a.
7. box-sizing: border-box verwenden.
8. Die Karten erhalten flex-grow: 1 oder kurz flex: 1.
9. display: flex verwenden. Dann wirkt gap zwischen den Listenelementen.
