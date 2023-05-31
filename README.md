
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Die besten Filme aller Zeiten

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_1561a196c2e3852533bad64d9b0d4e9f.gif)

## Einführung


Wir haben gerade einige nützliche Methoden gelernt, die uns helfen werden, **Objekte und Arrays** zu manipulieren. In dieser Übung werden wir üben, mit diesen Methoden zu arbeiten, und du solltest mindestens eine von ihnen in jeder Iteration verwenden.

Der beste Weg zum Üben besteht darin, mit realen Daten zu arbeiten. In der Datei **`src/data.js`** findest du ein Array von Informationen über **die besten 250 Filme aller Zeiten** laut [IMDB Ranking](http://www.imdb.com/chart/top?ref_=nv_mv_250_6), die du verwenden wirst, um anzuzeigen, was jede Iteration verlangt! :muscle:

<br>   

## Anforderungen

- Fork dieses Repo.
- Klone dieses Repo.
- Übe fortgeschrittene JavaScript-Methoden (`map`, `reduce`, `filter` und `sort`) zur Manipulation von Arrays.  
  <br>

## Abgabe

- Führe nach Abschluss des Labs folgende Befehle aus:

```bash 
git add .
git commit -m "Solved lab"
git push origin master
```   
- Erstelle einen Pull Request, damit Deine TAs Deine Arbeit überprüfen können.

<br>   

## Einführung

Die `src/data.js` enthält ein Array von 250 Filmen. Es ist ein Array von 250 _Objekten_, die die Informationen über jeden Film enthalten. Hier ist ein Beispiel, wie die Daten angezeigt werden:

```javascript 
{
  "title": "The Shawshank Redemption",
  "year": 1994,
  "director": "Frank Darabont",
  "duration": "2h 22min",
  "genre": ["Crime","Drama"],
  "score": 9.3
}
```   

Du wirst tiefer in einige "Fakten" eintauchen, die dieser Datensatz hat. Zum Beispiel können wir diesen Datensatz verwenden, um herauszufinden, welcher der beliebtesten Filme ist, wie lange im Durchschnitt die Filme dauern, die Liste der Filme eines bestimmten Regisseurs usw. Nun kommt deine Herausforderung. In den nächsten Iterationen wirst du dein JS-Wissen nutzen, um diese Daten zu manipulieren.

Denke daran, jede Iterationsbeschreibung sorgfältig zu lesen, bevor du an der Lösung arbeitest.

<br>   


## Anweisungen


Du arbeitest an der Datei `src/movies.js`, die bereits in der `index.html`-Datei geladen wird.

Die Datei `src/data.js`, die das Array von Filmen enthält, wird ebenfalls in der `index.html`-Datei geladen.

Um den JavaScript-Code auszuführen, öffne die `index.html`-Datei mit der [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)-VSCode-Erweiterung.

Um die Ausgabe deines JavaScript-Codes zu sehen, öffne die [Konsole in den Entwicklertools](https://developer.chrome.com/docs/devtools/open/#console).



<br>   
<hr>   

### Hinweis zu Tests

Dieses LAB verfügt über Unit-Tests, um automatisiertes Feedback zu Ihrem Fortschritt im Labor zu geben.

Nach Abschluss der Grunditerationen gehen Sie zum Abschnitt **"Test Your Code"** am Ende. Dort werden Sie aufgefordert, die Test-Abhängigkeiten zu installieren und die Tests auszuführen, um zu überprüfen, wie viele Tests Ihr Code besteht. Wenn Sie die Tests ausführen, korrigieren Sie Ihren Code, um die fehlgeschlagenen Tests zu bestehen.

<hr>   
<br>   

### Iteration 1: Alle Regisseure

Wir müssen das Array aller Regisseure erhalten. Da dies ein Warm-up ist, geben wir Dir einen Hinweis: Du musst durch das Array der Filme _mappen_ und alle Regisseure als ein endgültiges Ergebnis in einem Array sammeln. Erstelle eine Funktion namens `getAllDirectors()`, die ein Array von Filmen als Argument erhält und ein neues (_gemapptes_) Array zurückgibt.

<br>   

#### Bonus - Iteration 1.1: Das Array von Regisseuren _bereinigen_

Es scheint, dass einige Regisseure mehrere Filme gedreht haben, daher tauchen sie mehrmals im Array der Regisseure auf. Wie könntest Du dieses Array "bereinigen" und vereinheitlichen (d.h. ohne Duplikate)? _Priorisiere jetzt nicht den Bonus-Teil, Du kannst darauf zurückkommen, wenn Du mit den Pflichtiterationen fertig bist._ :wink:

<br>   

### Iteration 2: Steven Spielberg. Der Beste?

Einer der berühmtesten Regisseure des Kinos ist **[Steven Spielberg](https://de.wikipedia.org/wiki/Steven_Spielberg)**, und er hat einige wirklich großartige Dramafilme auf unserer Liste. Wir möchten jedoch wissen, wie viele davon vorhanden sind.

Erstelle eine Funktion `howManyMovies()`, die ein Array als Parameter erhält und das Array `filtert`, damit wir nur die **Dramafilme** haben, bei denen **Steven Spielberg** Regie geführt hat.

<br>   

### Iteration 3: Durchschnitt aller Bewertungen

Dies sind die besten Filme basierend auf ihren Bewertungen, also haben alle einen bemerkenswerten Wert. In dieser Iteration möchten wir den durchschnittlichen Wert aller Filme berechnen und auf der Konsole anzeigen. Erstelle eine Funktion `scoresAverage()`, die ein Array als Parameter erhält und die Herausforderung löst.

Der Wert muss auf 2 Dezimalstellen gerundet zurückgegeben werden!

**:bulb: Möglicherweise möchtest Du die Daten auf einen einzigen Wert _"reduzieren"_. :wink:**

<br>   

### Iteration 4: Drama-Filme

Drama ist das Genre, das in unserem `array` am häufigsten vorkommt. Offenbar lieben die Menschen Drama! :eyes:

Erstelle eine `dramaMoviesScore()` Funktion, die ein Array als Parameter erhält, um den durchschnittlichen Score aller Drama-Filme zu erhalten! Mal sehen, ob er besser ist als der allgemeine Durchschnitt.

Wieder gerundet auf 2 Dezimalstellen!

<br>   

### Iteration 5: Nach Jahr sortieren

Wir müssen die Filme in aufsteigender Reihenfolge nach ihrem Veröffentlichungsjahr sortieren. Das sollte mit einer der Methoden, die wir gerade gelernt haben, einfach sein. :wink:    
Erstelle eine Funktion `orderByYear()`, die ein Array als Parameter erhält und ein _neues sortiertes Array_ zurückgibt.

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_3db351079827c0acba42cf1e397dd8a3.gif)


Wenn zwei Filme das gleiche Jahr haben, ordne sie alphabetisch nach ihrem Titel! :heavy_check_mark:

**:bulb: Stelle sicher, dass das ursprüngliche Array nicht mutiert wird :wink:**

<br>   

### Iteration 6: Alphabetische Reihenfolge

Eine weitere beliebte Möglichkeit, die Filme zu sortieren, besteht darin, sie alphabetisch nach dem `title` Schlüssel zu sortieren. Allerdings müssen wir in diesem Fall nur den Titel der ersten 20 Filme ausgeben. Für einen Experten wie Dich ist das einfach. :wink:

Erstelle eine `orderAlphabetically()` Funktion, die ein Array empfängt und ein Array von den ersten 20 alphabetisch sortierten Titeln zurückgibt. Gib nur den Titel jedes Films zurück, und wenn das empfangene Array weniger als 20 Filme enthält, gib alle von ihnen zurück.

<br>   

### BONUS - Iteration 7: Zeitanzeige

Wir bekommen die Informationen von der **IMDB**-Webseite, aber die Dauerinformationen wurden in einem Format gespeichert, das es uns schwer macht, Filme zu vergleichen.

Den längsten Film zu finden, ist mit diesem Format fast unmöglich, also lass uns das ändern!

- Erstelle eine Funktion `turnHoursToMinutes()`, die ein Array als Parameter empfängt und mit ein wenig _Magie_, die von Dir implementiert wurde, die Dauerinformation jedes der Filme durch deren Äquivalent in Minuten ersetzt. Zum Beispiel:

```javascript 
{
  "title": "The Shawshank Redemption",
  "year": 1994,
  "director": "Frank Darabont",
  "duration": "2h 22min",
  "genre": ["Crime","Drama"],
  "score" :9.3
}
```   
Sollte sein:

```javascript 
{
  "title": "The Shawshank Redemption",
  "year": 1994,
  "director": "Frank Darabont",
  "duration": 142,
  "genre": ["Crime","Drama"],
  "score": 9.3
}
```   
**Beachte**, dass Du ein neues Array mit allen Informationen über Filme zurückgeben musst. Das bedeutet, dass Du das ursprüngliche Array nicht verändern solltest.

<br>   

### BONUS - Iteration 8: Durchschnittliche Bewertung des besten Jahres

Wir hören immer so viel über klassische Filme, aber wir möchten wissen, welches Jahr die beste durchschnittliche Bewertung hat, damit wir das **BEST YEAR FOR CINEMA** offiziell erklären können!

Finde heraus, welches Jahr die beste durchschnittliche Bewertung für die Filme hat, die in diesem Jahr veröffentlicht wurden! Erstelle eine Funktion `bestYearAvg()`, die ein Array von Filmen erhält und uns die Antwort gibt, welches Jahr das beste Jahr für das Kino war und was seine durchschnittliche Bewertung war. Die `bestYearAvg()` sollte einen **String** mit folgender Struktur zurückgeben:

**The best year was \<YEAR\> with an average score of \<RATE\>**

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_dfc3fe557576abca4dba274e3aabe9a3.gif)



<br>   

## Teste Deinen Code

Ja! Wir haben unsere Tests und Du weißt bereits, wie es funktioniert. Öffne Dein Terminal, wechsle in das Root-Verzeichnis des Labors und führe `npm install` aus, um den Test-Runner zu installieren. Führe anschließend die Tests aus, indem Du den Befehl `npm run test:watch` ausführst.

Zusammenfassend sind die Schritte:

```shell 
$ cd lab-javascript-greatest-movies
$ npm install
$ npm run test:watch  
```   
Zuletzt öffnest Du die generierte Datei `lab-solution.html` mit der VSCode-Erweiterung "Live Server", um die Testergebnisse zu sehen.

Denke daran, Dich auf einen Test nach dem anderen zu konzentrieren und die Anweisungen sorgfältig zu lesen, um zu verstehen, was Du tun musst.

Die Tests findest Du in der Datei `tests/movies.spec.js`.



<br>   

**Viel Spaß beim Coden!** :heart: