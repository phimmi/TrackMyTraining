# Projektvorschlag TrackMyTraining

**Hochschule Worms CSA 151 WS 2018/19** 

Philipp Schmitt

Philipp.Schmitt@hs-worms.de


---

## Abstract
Entwicklung einer Plattform zur persönlichen Trainingsentwicklung

###Motivation
Ich trainiere regelmäßig in einem Sportstudio und verfolge meinen persönlichen Trainingsfortschritt bisher - wie üblich - auf Papier in tabellarischer Form.
Leider bin ich was diesen Plan angeht nicht sonderlich sorgfältig und er wird oft in meiner Sporttasche zerknüllt, zerrissen und umgeknickt, weshalb ich regelmäßig eine neue Tabelle ausdrucken muss.
Damit meine Ergebnisse über längeren Zeitraum nachverfolgbar sind, muss ich daraufhin die vorherigen Ergebnisse immer wieder übertragen.
Dies möchte ich für mich (und für andere Nutzer) lösen, indem ich eine entsprechende Client-Server-Anwendung entwickele, die es mir ermöglicht ein Training aus einer Liste an Übungen zusammenzustellen und das Ergebnis für jede Übung für jede Trainingseinheit abzuspeichern.

###Anforderungsanalyse

1. Funktionale Anforderungen
    - Übung hinzufügen.
    - Übung bearbeiten.
    - Übung löschen.
    - Training erstellen.
    - Übung zum Training hinzufügen.
    - Ergebnis zu einer Übung hinzufügen.
    - Ergebnis zu einer Übung bearbeiten.
    - Ergebnis zu einer Übung löschen.
    - Übung aus einem Training entfernen.
    - Training bearbeiten.
    
2. Nicht-Funktionale Anforderungen
    - Die Daten sollen persistent in einer Datenbank gespeichert werden.
    - Die Anwendung soll schnell sein.
    - Die Anwendung soll hübscher sein als die tabellarische Darstellung auf Papier.
    - Die Anwendung soll selbsterklärend sein.
 
## Client
Ich möchte das Projekt hübsch gestalten und mich mit neusten Gestaltungsmöglichkeiten und Komponenten auseinander setzen.

https://material.io/develop/web/ bietet umfangreiche Komponenten für die Gestaltung moderner Nutzeroberflächen.

Ich möchte die Übungen mittels "Cards" sowie Einstellungsmöglichkeiten mittels "Chips" umsetzen und den "FloatingActionButton" nutzen um Dialoge zu triggern zum Erstellen und Bearbeiten von Übungen und Trainings.

## Mobil

## Desktop

### Dashboard


### Training


### Exercises

### Registration / Login

## Server


## ORM


## API-Beschreibung


### `GET /user/:id`
**Get** 
Liefert den Nutzer mit der id zurück

### `POST /user`
**Create** Erstellt einen neuen Nutzer und liefert als Antwort ein Nutzerobjekt mit id zurück.

### `PUT /user/:id`
**Update** aktualisiert den Nutzer mit id

### `DELETE /user:id`
**Delete** löscht den Nutzer mit der id und alle damit verknüpften weiteren Datenbankeinträge


#### Error


```javascript
{
  success: Boolean,
  msg: String
}
```

#### Get ..

```javascript
{
  success: Boolean,
  msg: String,
  data: {
    id: Number
    name: String 
  }
}
```

#### Gets ...

```javascript
{
  success: Boolean,
  msg: String,
  data: [
    {
        id: Number
        name: String 
    },
    {
      id: Number
      name: String 
    },
    ...
  ]
}
```
## Aufwandsschätzungen

### Client

#### Projektvorbereitung 


| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Wireframe Mobil Lorem                    |            |
| Wireframe Desktop Lorem                  |            |
| Beschreibung Funktionen Lorem            |            |
| Wireframe Lorem2                         |            |
| Beschreibung Funktionen Lorem2           |            |
| Wireframe Lorem3                         |            |
| Beschreibung Funktionen Lorem4           |            |
| Verfassen des Projektvorschlags          |            |
| ...                                      |  ...        |
| **Summe**                                |  **...**    |


#### Implementierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| HTML-Grundgerüst Lorem                   |            |
| HTML-Grundgerüst Lorem2                  |            |
| HTML-Grundgerüst Lorem3                  |            |
| SCSS-Styling Breakpoint small            |            |
| SCSS-Styling Breakpoint medium           |            |
| SCSS-Styling Breakpoint large            |            |
| Implementierung Funktion Lorem           |            |
| Implementierung Funktion Lorem2          |            |
| Implementierung Funktion Lorem3          |            |
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
| Projektvorbereitung                      |  15        |
| Implementierung                          |  ...        |
| Dokumentation / Tests                    |  ...        |
| **Summe**                                |  75        |

### Backend

Verantwortlicher: Johannes Meier

#### Projektvorbereitung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Backend Endpunkte / API - Beschreibung   |            |
| ORM                                      |            |
| Verfassen des Projektvorschlags          |            |
| Verfassen ...                            |            |
| Markdown                                 |            |
| ...                                      |  ...        |
| **Summe**                                |  **...**    |

#### Implementierung und Validierung

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Framework                          |             |
| - Framework express                      |         |
| - Framework jest                         |          |
| - Framework ...                          |         |
| DB ...                                   |            |
| - Setup                                  |            |
| Implementierung Auth                     |            |
| Implementierung Lorem-Route              |            |
| Implementierung Lorem2-Route             |            |
| Implementierung Lorem3-Route             |            |
| Implementierung Lorem4-Route             |            |
| Implementierung Validierungsschemata     |            |
| Implementierung Validierung Route 1      |          |
| Implementierung Validierung Route 2      |          |
| ...                                      |  ...        |
| **Summe**                                |  **...**    |

#### Dokumentation / Tests

| Aufgabe                                  | Zeit in Std |
|------------------------------------------|------------:|
| Setup Tests                              |            |
| Test DB                                  |            |
| Test Lorem1-Route                        |            |
| Test Lorem2-Route                        |          |
| Test Lorem3-Route                        |            |
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
| **Summe**                                |  **...**    |


#### Zusammenfassung
| Teil                                     | Zeit in Std |
|------------------------------------------|------------:|
| Projektvorbereitung                      |  ...        |
| Implementierung                          |  ...        |
| Dokumentation / Tests                    |  ...        |
| **Summe**                                |  40        |
