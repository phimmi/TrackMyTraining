# Projektvorschlag TrackMyTraining

**Hochschule Worms CSA 151 WS 2018/19** 

Philipp Schmitt

Gruppe 36 ( Soloprojekt )

Matrikelnummer 674617

Philipp.Schmitt@hs-worms.de
inf3182@hs-worms.de


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
    - User registrieren.
    - User einloggen.
    - Übung hinzufügen.
    - Übung bearbeiten.
    - Übung löschen.
    - Training erstellen.
    - Übung zum Training hinzufügen.
    - Ergebnis zu einer Übung hinzufügen.
    - Ergebnis zu einer Übung bearbeiten.
    - Ergebnis zu einer Übung löschen.
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

Nach einem Klick auf den FloatingActionButton gelangt man auf diesen Übung-Hinzufügen-Screen. Der Übung-Hinzufügen-Screen soll auch zum Bearbeiten von bereits existierenden Übungen genutzt werden und öffnet sich dann mit den entsprechenden Daten.

![TrackMyTraining Mobile Übung Hinzufügen](./wireframes/mobile/TrackMyTraining%20Neue%20Übung.PNG)

Hat man alle erwünschten Übungen erstellt, so kann man nun ein Training starten.
Dazu klickt man auf dem Training-Bildschirm auf den großen FloatingActionButton mit dem "Start/Play"-Symbol und gelangt zum folgenden Screen.

![TrackMyTraining Mobile Training Hinzufügen Default](./wireframes/mobile/TrackMyTraining%20Neues%20Training%20Default.PNG)

Man fügt nach und nach die erwünschten Übungen mitsamt Ergebnis hinzu.
Wenn man fertig mit dem Training ist, beendet man das Training durch Drücken des großen roten "Stop"-Buttons. Dieser Bildschirm dient auch wiederum zum Bearbeiten des Trainings.

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

Authentifizierung nehme ich mit dem Modul [Basic Auth](https://www.npmjs.com/package/basic-auth) vor. Ich behalte mir vor etwaige Verschlüsselung mit einzubauen. Des Weiteren möchte ich mich daran versuchen ein Mini-Token-System mittels dem Basic-Auth zu schreiben.


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
Route nimmt Nutzerdaten entgegen und liefert einen Login-Token und ein Nutzerobjekt, wenn die Authentifizierung erfolgreich war
- **INPUT**  `{name: String, password: String}`
- **RESULT** `{token: String, {name: String, email: String}`

### `POST /user/register`
**Create** 
Erstellt einen neuen Nutzer
Route nimmt Nutzerdaten entgegen
- **INPUT**  `{name: String, email: String, password: String}`

### `GET /user`
**Get**
Route nimmt Token entgegen und liefert Nutzerobjekt zurück
- **INPUT** `{token: String}`
- **RESULT** `{id: Number, name: String, email: String}`

### `PUT /user/:id`
**Update**
Aktualisiert den Nutzer anhand der Route
Route nimmt Token und aktualisierte Nutzerdaten entgegen und liefert aktualisiertes Nutzerobjekt zurück
- **INPUT**  `{token: String, {name_new: String, email_new: String, password_new: String}}`
- **RESULT** `{id: Number, name_new: String, email_new: String}`

### `DELETE /user/:id`
**Delete** 
Löscht den Nutzer anhand der Route sowie alle mit ihm verknüpften Datensätze
Route nimmt Token entgegen

### `GET /users`
**DEBUG**
**Get List**
Liefert Liste aller User zum Debuggen

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

### `PUT /übung/:id`
**Update**
Route nimmt aktualisierte Übungsdaten und Token entgegen
- **INPUT** `{token:String, {id: Number, name: String, beschreibung: String}`

### `DELETE /übung/:id`
**Delete**
Löscht die Übung anhand der Route
Route nimmt Webtoken entgegen

### `GET /übungen`
**DEBUG**
**Get List**
Liefert Liste aller Übungen zum Debuggen

### `POST /training`
**Create**
Erstellt ein neues Training
liefert Trainingsobjekt zurück
Route nimmt Webtoken entgegen und speichert Training anhand von mit dem Token assoziierten User
- **INPUT**  `{token: String, übungen: [{übung_id: Number, ergebnis: String},{übung_id: Number, ergebnis: String},...]}`
- **RESULT** `{training_id: Number, übungen: [{übung_id: Number, ergebnis: String},{übung_id : Number, ergebnis: String},...]`

### `PUT /training/:id`
**Update**
nimmt aktualisierte Trainingsdaten und Token entgegen
- **INPUT** `{token: String, training: {training_id: Number, übungen: [{übung_id: Number, ergebnis: String},{übung_id: Number, ergebnis: String},...]`

### `GET /trainings`
**DEBUG**
**Get List**
Liefert Liste aller Trainings zum Debuggen

### `GET user/:id/übungen`
**Get List**
Route nimmt Token entgegen und liefert Liste an Übungen, die vom Nutzer mit id erstellt wurden


### `GET user/:id/training`
**Get List**
Route nimmt Token entgegen und liefert Liste an Trainings, die vom Nutzer mit id erstellt wurden

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
| Verfassen des Projektvorschlags          |      4      |
| **Summe**                                |  **23,5**    |

### Client
#### Implementierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| HTML-Grundgerüst Allgemein               |     0,5        |
| HTML-Grundgerüst Login                   |    1           |
| HTML-Grundgerüst Registration            |    1         |
| HTML-Grundgerüst Training                |      2,5      |
| HTML-Grundgerüst Training hinzufügen / bearbeiten     |    1        |
| HTML-Grundgerüst Übungen                 |     3,5       |
| HTML-Grundgerüst Übung hinzufügen / bearbeiten |     1       |
| HTML-Grundgerüst Einstellungen           |     1       |
| SCSS-Styling Breakpoint small            |      4      |
| SCSS-Styling Breakpoint large            |      4      |
| Implementierung JS Navigation            |       0,5    |
| Implementierung JS Login                 |    5         |
| Implementierung JS Registration          |        1     |
| Implementierung JS Bilder                |       3      |
| Implementierung JS Übung hinzufügen      |      2       |
| Implementierung JS Übungen               |       3      |
| Implementierung JS Übung löschen         |      0,5       |
| Implementierung JS Übung bearbeiten      |      2       |
| Implementierung JS Training hinzufügen   |      3       |
| Implementierung JS Trainings             |     4        |
| Implementierung JS Training bearbeiten   |    3        |
| **Summe**                                |  **46,5**    |

Die Grundgerüste Allgemein, Login, Registration, Training hinzufügen / bearbeiten, Übung hinzufügen / bearbeiten sind statische Seiten und müssen nicht dynamisch erzeugt werden, weshalb ich denke, dass ich damit sehr schnell voran komme.
Das Grundgerüst für Training und Übungen hingegen muss dynamisch mit Hilfe von JS generiert werden, weshalb ich beiden Teilen einen höheren Zeitaufwand anrechne. Dies spiegelt sich auch in der JS Implementierung wieder. Die restlichen Bildschirme müssen ggf. mit passendem Inhalt gefüllt werden.
#### Dokumentation / Tests

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Dokumentation Funktion Login             |      0,25      |
| Dokumentation Funktion Registrieren            |    0,1        |
| Dokumentation Funktion Übung hinzufügen            |   0,1         |
| Dokumentation Funktion Übung bearbeiten            |      0,1      |
| Dokumentation Funktion Übung löschen            |     0,1       |
| Dokumentation Funktion Training hinzufügen            |    0,1        |
| Dokumentation Funktion Training bearbeiten            |       0,1     |
| Dokumentation Funktion Training löschen            |      0,1      |
| Dokumentation Token / Authenthifizierung / Session-Cookie | 1 |
| Dokumentation Trainingsliste anzeigen | 0,5 |
| Dokumentation Übungsliste anzeigen | 0,5 |
| Test Login | 0,5 |
| Test Registrierung | 0,5 |
| Test Übung hinzufügen | 0,25 |
| Test Übung bearbeiten | 0,25 |
| Test Übung löschen | 0,25 |
| Test Training hinzufügen | 0,25 |
| Test Training löschen | 0,25 |
| **Summe**                                |  **5,1**    |

Die meisten Funktionen sollten sehr schnell dokumentiert werden können, lediglich die Anzeige der Übersichtsseiten werden ein paar mehr Dokumentationen notwendig machen.
Beim Testen möchte ich einen Fokus auf den richtigen Login und Registrierung legen.

#### Zusammenfassung Client
| Teil Client                                    | Zeit in Std |
|------------------------------------------|------------:|
| Implementierung                          |  46,5       |
| Dokumentation / Tests                    |  5,1        |
| **Summe**                                |    51,6      |

### Backend

#### Implementierung und Validierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Framework                          |      6,5       |
| - Framework express                      |   1      |
| - Framework jest                         |    0,5      |
| - Framework Basic-Auth                          |    1     |
| - Framework Basic-Auth als Tokenizer     |    4     |
| DB SQLITE3                                 |     3       |
| - Setup                                  |      3      |
| Implementierung get /login-Route                     |     3       |
| Implementierung post /user/register-Route              |     0,5       |
| Implementierung get /user/:id/übungen-Route             |       2     |
| Implementierung get /user/:id/training-Route             |     3       |
| Implementierung post /übung            |     0,5       |
| Implementierung post /training         |    1        |
| Implementierung restliche Routen | 2 |
| Implementierung Validierungsschemata für Routen    |     5       |
| **Summe**                                |  **26,5**    |

Das Setup der Frameworks dürfte nicht zu viel Zeit in Anspruch nehmen. Lediglich ein eigenes kleines Tokensystem dürfte ein paar Stunden Arbeit sein.
Die Datenbank einzurichten bedarf neben Fleißarbeit auch Einiges an Hirnschmalz und Vorsicht, weshalb ich - selbst für die paar kleinen Tabellen - etwas mehr Zeit eingerechnet habe.

Die Funktionalität der einzelnen Routen sollte schnell vonstatten gehen, während die Validierung der Daten jeweils auch nochmal gut Zeit in Anspruch nehmen wird.
Alles in Allem sollte die Implementierung des Server - aus dem Bauch raus - innerhalb einer guten Arbeitswoche von 30-35 Stunden zu schaffen sein. Meine Schätzung der einzelnen Arbeitsschritte bestätigt mich darin.

#### Dokumentation / Tests

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Tests                              |      1      |
| Test DB                                  |      1,5     |
| Test get /login-Route                     |     1       |
| Test post /user/register-Route              |     0,5       |
| Test get /user/:id/übungen-Route             |       0,5     |
| Test get /user/:id/training-Route             |     0,5      |
| Test post /übung            |     0,25      |
| Test post /training         |    0,25       |
| Test restliche Routen | 0,5 |
| API-Dokumentation get /login-Route                     |     1       |
| API-Dokumentation post /user/register-Route              |     0,25       |
| API-Dokumentation get /user/:id/übungen-Route             |       0,25     |
| API-Dokumentation get /user/:id/training-Route             |     0,25       |
| API-Dokumentation post /übung            |     0,25      |
| API-Dokumentation post /training         |    0,25        |
| API-Dokumentation restliche Routen | 0,5 |
| **Summe**                                |  **9**    |



#### Zusammenfassung Server
| Teil Server                                  | Zeit in Std |
|------------------------------------------|------------:|
| Implementierung                          |  24,5        |
| Dokumentation / Tests                    |  9        |
| **Summe**                                |  33,5        |

### Zusammenfassung Gesamt
| Teil Gesamt                                 | Zeit in Std |
|------------------------------------------|------------:|
| Projektvorbereitung                      |  23,5       |
| Client                        |  51,6        |
| Server                   |     35,5    |
| **Summe**                                |  110,6        |

Als Einzelprojekt ist es meines Erachtens angemessen, dass ich Etwas über die angepeilten 100 Stunden hinaus komme.
Ich denke jedoch, dass ich durch auftretende Probleme länger brauchen könnte als geschätzt. Ich plane final mit <130 Stunden für das Projekt.
