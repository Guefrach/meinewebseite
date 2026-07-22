# Probepruefung: HTML, CSS und Flexbox

Nur Kursstoff bis einschliesslich Flexbox. Kein Grid, Responsive Design, Semantik, Barrierefreiheit oder SEO.

**Arbeitszeit: 60 Minuten** - Teil A etwa 20 Minuten, Teil B etwa 40 Minuten. Bearbeite zuerst alles ohne Unterlagen.

## Teil A - Multiple Choice

Kreuze jeweils genau eine Antwort an.

1. Was macht der Browser mit HTML, CSS und Bildern vom Server? a
   A) Er rendert die Webseite. B) Er wird zum Server. C) Er erzeugt DNS. D) Er loescht die Dateien.

2. Welche HTTP-Methode ruft Daten ab? c
   A) POST B) DELETE C) GET D) PATCH

3. Welche Datei ist normalerweise die Startseite einer statischen Website? c
   A) start.html B) homepage.css C) index.html D) main.js

4. Was steht im body-Element? b
   A) Nur Metadaten B) Sichtbarer Seiteninhalt C) IP-Adresse D) Nur CSS

5. Welches Element zeichnet wichtigen Text semantisch aus?b
   A) b B) strong C) big D) color

6. Welcher Link verweist auf einen Abschnitt mit der ID kontakt?c
   A) href="kontakt" B) href="/kontakt" C) href="#kontakt" D) href="id:kontakt"

7. Wofuer ist rel="noopener noreferrer" bei target="_blank"?a
   A) Sicherheit bei externen Links B) Schriftgroesse C) Tabellen D) Bildformat

8. Welcher Pfad zeigt vom Projekt-Hauptordner auf images/logo.svg?b
   A) /logo.svg B) images/logo.svg C) ../images/logo.svg D) logo.svg/images

9. Wann ist alt="" bei einem Bild richtig?b
   A) Bei einem wichtigen Foto B) Bei einem dekorativen Bild C) Immer D) Nie

10. Was ist der Unterschied zwischen th und td?a
    A) th ist Kopfzelle, td Datenzelle B) th ist eine Zeile C) td ist fuer Bilder D) Kein Unterschied

11. Wozu dient scope="row"?b
    A) Kopfzelle gehoert zur Spalte darunter B) Kopfzelle gehoert zur Zeile daneben C) Drei Spalten verbinden D) Tabelle verstecken

12. Welcher Input-Typ prueft das E-Mail-Format?c
    A) text B) number C) email D) password

13. Welche Aussage zu GET und POST ist richtig?a
    A) GET-Daten stehen meist in der URL, POST-Daten im Request-Body.
    B) POST ist fuer Bilder. C) GET ist gut fuer Passwoerter. D) Beide sind gleich.

14. Welcher Selektor spricht nur p-Elemente mit der Klasse intro an?b
    A) .intro p B) p.intro C) #intro p D) p #intro

15. Welcher Selektor hat die hoechste Spezifitaet?c
    A) p B) .hinweis C) #hinweis D) Alle gleich

16. Was ist bei box-sizing: content-box nicht in width enthalten?b
    A) Inhalt B) padding und border C) Text D) content

17. Was ist bei flex-direction: column die Hauptachse?b
    A) Horizontal B) Vertikal C) Keine D) Grid

18. Welche Eigenschaft verteilt Flex-Items auf der Hauptachse?b
    A) align-items B) justify-content C) align-self D) flex-shrink

19. Was bewirkt flex-shrink: 0?a
    A) Ein Item schrumpft bei Platzmangel nicht.
    B) Es bekommt keinen Abstand. C) Es steht zuerst. D) Es ist unsichtbar.

20. Was bewirkt flex-wrap: wrap?a
    A) Items duerfen in eine neue Zeile umbrechen.
    B) Items werden immer vertikal zentriert.
    C) Flexbox wird beendet.
    D) Items haben feste Breite.

## Teil B - Fehlersuche und Korrektur

Nenne jeweils den Fehler und schreibe den korrigierten Code.

1. HTML-Grundstruktur:

~~~html
<!DOCTYPE html>
<html lang="de">
  <head><title>Meine Seite</title></head>
  <body><h1>Willkommen</h1></head>
</html>
~~~

2. Bild: Die Datei liegt in images/urlaub.jpg. Das Foto zeigt eine Bergwanderung und ist wichtig fuer den Inhalt.

~~~html
<img src="/urlaub.jpg" alt="">
~~~

3. Tabelle: Kurs und Status sollen Kopfzeilen sein. HTML ist ein Zeilenkopf.

~~~html
<table>
  <thead><tr><td>Kurs</td><td>Status</td></tr></thead>
  <tbody><tr><td>HTML</td><td>Fertig</td></tr></tbody>
</table>
~~~

4. Formular: Newsletter soll die Checkbox beschriften. Der Button soll das Formular absenden.

~~~html
<label for="newsletter">Newsletter</label>
<input type="checkbox" id="news" name="newsletter">
<button type="button">Anmelden</button>
~~~

5. Spezifitaet: Der Text soll blau sein.

~~~html
<p id="meldung" class="info">Ergebnis gespeichert.</p>
~~~

~~~css
#meldung { color: red; }
.info { color: blue; }
~~~

6. Box-Modell: Die Gesamtbreite der Karte soll 320px sein, einschliesslich padding und border.

~~~css
.karte {
   box-sizing: border-box
  width: 320px;
  padding: 24px;
  border: 2px solid #222;
}
~~~

7. Flexbox: Die Items sollen untereinander stehen und vertikal im Container zentriert sein.

~~~css
.menue {
  display: flex;
  flex-direction: column;
  align-items: center;
   justify-content: center
}
~~~

8. Navigation: Logo links, Linkliste rechts; alles vertikal zentriert. Die Links sollen nebeneinander stehen.

~~~css
.navbar {
  display: flex;
  justify-content: center;
  align-items: stretch;
}
.nav-links {
  list-style: none;
  gap: 1rem;
}
~~~

---

## Loesungen

Teil A: 1 A, 2 C, 3 C, 4 B, 5 B, 6 C, 7 A, 8 B, 9 B, 10 A, 11 B, 12 C, 13 A, 14 B, 15 C, 16 B, 17 B, 18 B, 19 A, 20 A.

Teil B:

1. body muss mit /body geschlossen werden, nicht mit /head.
2. Richtig: img src="images/urlaub.jpg" alt="Bergwanderung ...". Der Pfad ist relativ, das wichtige Bild braucht einen beschreibenden Alternativtext.
3. Die Spaltenkoepfe werden th scope="col". HTML wird th scope="row".
4. for und id muessen gleich sein, zum Beispiel for="news". Der Button braucht type="submit".
5. #meldung ist spezifischer als .info. Aendere die ID-Regel zu color: blue oder entferne sie fuer dieses Styling.
6. box-sizing: border-box ergaenzen, idealerweise global fuer alle Elemente.
7. Bei column ist die Hauptachse vertikal. justify-content: center zentriert vertikal; align-items: center ist horizontal.
8. navbar braucht justify-content: space-between und align-items: center. nav-links braucht display: flex, damit die Links nebeneinander stehen.
