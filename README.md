# Projektvorschlag TrackMyTraining

**Hochschule Worms CSA 151 WS 2018/19** 

Philipp Schmitt

Philipp.Schmitt@hs-worms.de


---

## Abstract
Entwicklung einer Plattform zum Nachverfolgen der persönlichen Trainingsentwicklung

### Motivation
Ich trainiere regelmäßig in einem Sportstudio und verfolge meinen persönlichen Trainingsfortschritt bisher - wie üblich - auf Papier in tabellarischer Form.
Leider bin ich was diesen Plan angeht nicht sonderlich sorgfältig und er wird oft in meiner Sporttasche zerknüllt, zerrissen und umgeknickt, weshalb ich regelmäßig eine neue Tabelle ausdrucken muss.
Damit meine Ergebnisse über längeren Zeitraum nachverfolgbar sind, muss ich daraufhin die vorherigen Ergebnisse immer wieder übertragen.
Dies möchte ich für mich (und für andere Nutzer) lösen, indem ich eine entsprechende Client-Server-Anwendung entwickele, die es mir ermöglicht ein Training aus einer Liste an Übungen zusammenzustellen und das Ergebnis für jede Übung für jede Trainingseinheit abzuspeichern.

### Anforderungsanalyse

1. Funktionale Anforderungen
    - Übung hinzufügen.
    - Übung bearbeiten.
    - Übung löschen.
    - Training erstellen.
    - Übung zum Training hinzufügen.
    - Ergebnis zu einer Übung hinzufügen.
    - Ergebnis zu einer Übung bearbeiten.
    - Training bearbeiten.
    - Training löschen.
    
2. Nicht-Funktionale Anforderungen
    - Die Daten sollen persistent in einer Datenbank gespeichert werden.
    - Die Anwendung soll schnell sein.
    - Die Anwendung soll hübscher und übersichtlicher sein als die tabellarische Darstellung auf Papier.
    - Die Anwendung soll selbsterklärend sein.
 
## Client
Die Anwendung besteht aus zwei essentiellen Teilen:
1. Übungsverwaltung
2. Trainingsverwaltung

### Übungsverwaltung
Die Übungsverwaltung ist die Übersichtseite der Übungen. Übungen stellen den Hauptteil der Anwendung dar.
Eine Übung besteht aus einem Namen und einer Beschreibung.
Optional soll zu einer Übung zusätzlich ein Bild abgespeichert werden können.

Die Übungsseite stellt eine Liste aller vom Nutzer hinzugefügten Übungen dar. Ein Button in der rechten unteren Ecke soll zum Hinzufügen von Übungen dienen.

### Trainingsverwaltung

Die Trainingsverwaltung ist die Übersichtseite der abgeschlossenen Trainings. Hier können alle Trainingseinheiten nachgesehen werden.
Dies soll in Listenform geschehen. Die einzelnen Trainings sind untereinander gelistet und können aufgeklappt werden, um zu sehen welche Übungen abgeschlossen wurden.
Ein großer "Training starten"-Button startet ein neues Training.
Einem Training kann nun nach und nach eine Übung aus seiner bereits erstellten Übungen inklusive entsprechendem Trainingsergebnisse hinzugefügt werden.
Das Training kann nach mindestens einem Trainingssatz einer einzelnen Übung mit dem Drücken eines "Training beenden"-Buttons beendet werden und wird daraufhin abgespeichert.

Ein Training besteht also aus einer Liste an Trainingsübungen, Übungen mit einem Ergebnis. Ergebnisse sollen als Text eingegeben werden.

## Design
Ich möchte das Projekt hübsch gestalten und mich mit den neuesten Gestaltungsmöglichkeiten und Komponenten der Webentwicklung auseinander setzen.
Das Design soll mit modernen Mitteln Gestalten und dabei trotzdem möglichst schlicht bleiben, weshalb ich auf aufwändige Animationen verzichte.
Die Anwendung soll selbsterklärend sein und der Nutzer soll die Möglichkeiten selbstständig erkunden, weshalb ich moderne Bausteine wie einen FloatingActionButton setzen möchte.

https://material.io/develop/web/ bietet umfangreiche Komponenten für die Gestaltung moderner Nutzeroberflächen. Diese Plattform möchte ich nutzen, um moderne Webentwicklungskomponenten in mein Projekt einfließen zu lassen.

Eine Übung kann sehr schön mit sogenannten "Cards" dargestellt werden.
![Material.io Webdesign Components Cards](https://material.io/components/images/mdc_web_screenshots/cards.png)

Cards können in einem Grid gut angeordnet werden und eignen sich damit hervorragend zur Darstellung der Übungsverwaltung.

Des Weiteren soll ein "FloatingActionButton" das zentrale funktionale Element der Anwendung sein. Er soll in der Übungsverwaltung dazu dienen eine Übung hinzuzufügen, während er in der Trainingsverwaltung dazu dienen soll ein neues Training zu erstellen.
Hierfür möchte ich Icons aus der Font-Awesome-Familie nutzen: [Font Awesome Icons](https://fontawesome.com/icons/)



## Mobil
Die mobile Version startet mit dem Login-Bildschirm.

![TrackMyTraining Mobile Login](./wireframes/mobile/TrackMyTraining%20Login.PNG)

Nach dem erfolgreichen Login gelangt man auf die Trainings-Übersichtsseite. Es werden dort die absolvierten Trainings angezeigt.

![TrackMyTraining Mobile Training](./wireframes/mobile/TrackMyTraining%20Training.PNG)

Beim Klicken auf "Übungen" in der Navigationsleiste gelangt man in die Übungsübersicht. Hier werden alle Übungen in einem zweispaltigen Grid untereinander angezeigt.
Ein großer FloatingActionButton in der Mitte am unteren Ende des Screens dient zum Hinzufügen einer neuen Übung.

![TrackMyTraining Mobile Übung](./wireframes/mobile/TrackMyTraining%20Übungen.PNG)

Nach einem Klick auf den FloatingActionButton gelangt man auf diesen Übung-Hinzufügen-Screen.

![TrackMyTraining Mobile Übung Hinzufügen](./wireframes/mobile/TrackMyTraining%20Neue%20Übung.PNG)

Hat man alle erwünschten Übungen erstellt, so kann man nun ein Training starten.
Dazu klickt man auf dem Training-Bildschirm auf den großen FloatingActionButton mit dem "Start/Play"-Symbol und gelangt zum folgenden Screen:

![TrackMyTraining Mobile Training Hinzufügen Default](./wireframes/mobile/TrackMyTraining%20Neues%20Training%20Default.PNG)

Man fügt nach und nach die erwünschten Übungen mitsamt Ergebnis hinzu.
Wenn man fertig mit dem Training ist, beendet man das Training durch Drücken des großen roten "Stop"-Buttons.

![TrackMyTraining Mobile Training Hinzufügen Gefüllte Liste](./wireframes/mobile/TrackMyTraining%20Neues%20Training%20Liste.PNG)

Daraufhin gelangt man wieder zum Trainings-Ausgangs-Bildschirm und das abgeschlossene Training wurde eingefügt.

## Desktop
Die Desktop Version ist eine modifizierte und angepasste Mobile-Version.

Die Elemente werden neu angeordnet, sodass sie auf dem größeren Bildschirm besser Platz finden.
### Login

![TrackMyTraining Desktop Start / Login](./wireframes/desktop/TrackMyTraining%20Login.PNG)

### Training

![TrackMyTraining Desktop Training](./wireframes/desktop/TrackMyTraining%20Training.PNG)

![TrackMyTraining Desktop Training Hinzufügen Leer](./wireframes/desktop/TrackMyTraining%20Neues%20Training.PNG)

![TrackMyTraining Desktop Training Hinzufügen Gefüllte Liste](./wireframes/desktop/TrackMyTraining%20Neues%20Training%20Liste.PNG)

### Übungen

![TrackMyTraining Desktop Übungen](./wireframes/desktop/TrackMyTraining%20Übung.PNG)

![TrackMyTraining Desktop Übung Hinzufügen](./wireframes/desktop/TrackMyTraining%20Neue%20Übung.PNG)

## Server

Der Server stellt eine REST-API bereit, um die Daten innerhalb einer Datenbank zu erstellen, zu bearbeiten und zu lesen.
Hierzu definiere ich mir nach dem REST-API-Prinzip verschiedene Routen, welche die unterschiedlichen Daten liefern.
Die Daten bauen grundsätzlich aufeinander auf:

Nutzer und Übungen stellen den Grundbaustein der Anwendung dar und sind miteinander verknüpft.
Ein Training enthält eine Liste von Trainingsübungen. Trainingsübungen sind Übungen mit einem Ergebnis und werden dargestellt durch die Referenz der Übungs-Id und einem Ergebnis.

Die Authentifizierung und Authorizierung möchte ich anhand von JSON Webtokens vornehmen. Ich orientiere mich dabei am Tutorial von medium.com [Securing your node.js RESTFUL Api with JSON Webtokens](https://medium.freecodecamp.org/securing-node-js-restful-apis-with-json-web-tokens-9f811a92bb52) wie man eine Middleware baut um auf allen Routen Authorizierung zu benutzen.



## ORM
![TrackMyTraining UML Diagramm](./orm/TrackMyTraining%20UML.PNG)

Es werden folgende Tabellen benötigt, um das obige Diagramm darzustellen:
1. Users
```SQL
CREATE TABLE IF NOT EXISTS users(
    user_id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL UNIQUE,
    email TEXT NOT NULL UNIQUE,
    password TEXT NOT NULL    
);
```
2. Übungen
```SQL
CREATE TABLE IF NOT EXISTS übungen(
    übung_id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    beschreibung TEXT,
    creator INTEGER,
    FOREIGN KEY (creator) REFERENCES users (user_id) 
);
```
3. Training
```SQL
CREATE TABLE IF NOT EXISTS training(
    training_id INTEGER PRIMARY KEY AUTOINCREMENT,
    user_id INTEGER,
    FOREIGN KEY (user_id) REFERENCES users (user_id)  
);
```
4. TrainingsÜbungen
```SQL
CREATE TABLE IF NOT EXISTS trainingsübungen(
    training_id INTEGER,
    übung_id INTEGER,
    ergebnis TEXT,
    PRIMARY KEY (training_id, übung_id),
    FOREIGN KEY (training_id) REFERENCES training (training_id),
    ON DELETE CASCADE ON UPDATE NO ACTION,
    FOREIGN KEY (übung_id) REFERENCES übungen (übung_id) 
    ON DELETE CASCADE ON UPDATE NO ACTION
);
```

## API-Beschreibung
Alle Routen außer der Login-Route benötigen eine Authentifizierung, welche aber durch eben Jene erlangt werden kann.

### `GET /login`
**Get**
Route nimmt Nutzerdaten entgegen und liefert JSON Webtoken zurück, wenn die Daten korrekt sind
- **INPUT**  `{name: String,password: String}`
- **RESULT** `{token: String}`

### `POST /register`
**Create** 
Erstellt einen neuen Nutzer
Route nimmt Nutzerdaten entgegen und liefert Nutzerobjekt mit id zurück
- **INPUT**  `{name: String, email: String, password: String}`
- **RESULT** `{id: Number, name: String, email: String, password: String`

### `GET /user`
**Get**
Route nimmt WebToken entgegen und liefert Nutzerobjekt zurück
- **INPUT** `{token: String}`
- **RESULT** `{id: Number, name: String, email: String`

### `PUT /user/:id`
**Update**
Aktualisiert den Nutzer anhand der Route
Route nimmt Webtoken und aktualisierte Nutzerdaten entgegen und liefert aktualisiertes Nutzerobjekt zurück
- **INPUT**  `{token: String, {name_new: String, email_new: String, password_new: String}}`
- **RESULT** `{id: Number, name_new: String, email_new: String, password_new: String`

### `DELETE /user/:id`
**Delete** 
Löscht den Nutzer anhand der Route sowie alle mit ihm verknüpften Datensätze
Route nimmt Webtoken entgegen

### `GET /übung/:id`
**Get**
liefert Übungsobjekt anhand der Route zurück
Route nimmt Webtoken entgegen
- **RESULT** `{id: Number, name: String, beschreibung: String}`

### `POST /übung`
**Create** 
Erstellt eine neue Übung.
Route nimmt Übungsdaten entgegen und liefert Übungsobjekt mit id zurück
Route nimmt Webtoken entgegen
- **INPUT**  `{name: String, beschreibung: String}`
- **RESULT** `{id: Number, name: String, beschreibung: String}`

### `DELETE /übung/:id`
**Delete**
Löscht die Übung anhand der Route
Route nimmt Webtoken entgegen

### `POST /training`
**Create**
Erstellt ein neues Training
liefert Trainingsobjekt zurück
Route nimmt Webtoken entgegen und speichert Training anhand von mit dem Token assoziierten User
- **INPUT**  `{token: String, [{übung_id: Number, ergebnis: String},{übung_id: Number, ergebnis: String},...]}`
- **RESULT** `{training_id: Number, übungen: [{übung_id: Number, ergebnis: String},{übung_id : Number, ergebnis: String},...]`

### `GET /übungen`
**Get List**
Route nimmt Webtoken entgegen und liefert Liste an Übungen, die vom Nutzer mit dem assoziierten Webtoken erstellt wurden

### `GET /training`
**Get List**
Route nimmt Webtoken entgegen und liefert Liste an Trainings, die vom Nutzer mit dem assoziierten Webtoken erstellt wurden

## Data Template Objects

### Allgemein
```javascript
{
  success: Boolean,
  msg: String,
  data: JSON
}
```

### Error
```javascript
{
  success: Boolean,
  msg: String
  data: []
}
```

### User
```javascript
{
    id: Number,
    name: String,
    email: String,
    password: String
}
```

### Übung
```javascript
{
    id: Number,
    name: String,
    beschreibung: String
}
```

### Trainingsübungen

```javascript
{
    übung_id: Number,
    ergebnis: String
}
```

### Training
```javascript
{
    id: Number,
    übungen: {
        {
            übung_id: Number,
            ergebnis: String
        },
        {
            übung_id: Number,
            ergebnis: String
        },
        ...
    }
}
```

## Aufwandsschätzungen

### Projektvorbereitung & Projektvorschlag


| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Einrichtung von Git und GitHub in WebStorm | 1 |
| Motivation                   |       0,5     |
| Anforderungsanalyse               |   0,5         |
| Client            |    0,5        |
| Design inklusive Recherche auf Material.io                     |    1        |
| WireFrames Mobile erstellt und WorkFlow / Funktionen beschrieben         |     5       |
| Wireframes Desktop erstellt und WorkFlow / Funktionen beschrieben                       |       4    |
| Backend Endpunkte / API - Beschreibung / Daten   | 5          |
| ORM                                      |     2       |
| Verfassen des Projektvorschlags          |      3      |
| **Summe**                                |  ****    |

### Client
#### Implementierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| HTML-Grundgerüst Allgemein               |             |
| HTML-Grundgerüst Training                |            |
| HTML-Grundgerüst Training hinzufügen             |            |
| HTML-Grundgerüst Übungen              |            |
| HTML-Grundgerüst Übung hinzufügen              |            |
| HTML-Grundgerüst Einstellungen             |            |
| SCSS-Styling Breakpoint small            |            |
| SCSS-Styling Breakpoint medium           |            |
| SCSS-Styling Breakpoint large            |            |
| Implementierung JS Navigation           |            |
| Implementierung JS Login              |             |
| Implementierung JS Login - Fehlerbehandlung             |             |
| Implementierung JS Klassen mit TS            |             |
| Implementierung JS Init Trainings              |             |
| Implementierung JS Init Übungen              |             |
| Implementierung JS Bilder            |             |
| Implementierung JS Übung hinzufügen           |             |
| Implementierung JS Training hinzufügen           |             |
| Implementierung JS Trainings           |             |
| Implementierung JS Übungen           |             |
| Implementierung JS Übung löschen           |             |
| Implementierung JS Übung bearbeiten          |             |
| ...                                      |  ...        |
| **Summe**                                |  **...**    |

#### Dokumentation / Tests

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Dokumentation Funktion Lorem             |            |
| Dokumentation Funktion Lorem2            |            |
| Dokumentation Funktion Lorem3            |            |
| ...                                      |  ...        |
| Vergleich SOLL / IST Stunden             |            |
| **Summe**                                |  **...**    |

#### Zusammenfassung
| Teil                                     | Zeit in Std |
|------------------------------------------|------------:|
| Projektvorbereitung                      |  20        |
| Implementierung                          |  40        |
| Dokumentation / Tests                    |  15        |
| **Summe**                                |  75        |

### Backend

#### Implementierung und Validierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Framework                          |             |
| - Framework express                      |         |
| - Framework jest                         |          |
| - Framework passport                          |         |
| DB SQLITE3                                 |            |
| - Setup                                  |            |
| Implementierung Auth                     |      ?      |
| Implementierung Lorem-Route              |            |
| Implementierung Lorem2-Route             |            |
| Implementierung Lorem3-Route             |            |
| Implementierung Lorem4-Route             |            |
| Implementierung Validierungsschemata     |            |
| Implementierung Validierung Route 1      |          |
| Implementierung Validierung Route 2      |          |
| ...                                      |  ...        |
| **Summe**                                |  **30**    |

#### Dokumentation / Tests

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Tests                              |            |
| Test DB                                  |            |
| Test Lorem1-Route                        |            |
| Test Lorem2-Route                        |          |
| Test Lorem3-Route                       |            |
| API-Dokumentation Lorem1-Route           |            |
| API-Dokumentation Lorem2-Route           |            |
| API-Dokumentation Lorem3-Route           |            |
| API-Dokumentation Lorem4-Route           |            |
| Dokumentation Lorem1-Route               |          |
| Dokumentation Lorem2-Route               |            |
| Dokumentation Lorem3-Route               |            |
| Dokumentation Lorem4-Route               |          |
| ...                                      |  ...        |
| Vergleich SOLL / IST Stunden             |            |
| **Summe**                                |  **10**    |


#### Zusammenfassung
| Teil                                     | Zeit in Std |
|------------------------------------------|------------:|
| Projektvorbereitung                      |  ...        |
| Implementierung                          |  ...        |
| Dokumentation / Tests                    |  ...        |
| **Summe**                                |  115        |
