# SaNa Trainer

Eine responsive Lernapp für die Schweizer SaNa-Fischereiprüfung. Sie enthält alle 150 Multiple-Choice-Fragen aus dem bereitgestellten Fragenkatalog, 17 direkt aus dem PDF extrahierte Fischabbildungen sowie weitere Abbildungen zu Ruten, Rolle und Ködern.

## Funktionen

- Lernmodus in acht sinnvoll gegliederten Themenbereichen
- Lösung und richtige Antwort sofort nach jeder Antwort
- eigener Schwerpunkt «Fische erkennen» mit freigestellten Originalabbildungen
- Prüfungsmodus mit 50 zufälligen Fragen aus dem Gesamtpool
- keine Rückmeldung im Prüfungsmodus vor dem Abschluss
- bestanden ab 40 von 50 richtigen Antworten
- Auswertung nach Kapiteln und Wiederholung aller Fehler
- lokaler Lernstand im Browser; keine Anmeldung und kein Serverkonto
- optimiert für Desktop, Tablet und Smartphone

Der aktuelle offizielle Prüfungsmodus wurde beim [Netzwerk Anglerausbildung](https://www.anglerausbildung.ch/erfolgskontrolle) verifiziert: 50 Fragen aus einem Katalog von 150, bestanden ab 40 richtigen Antworten. Eine feste Anzahl pro Kapitel wird dort nicht veröffentlicht; die App zieht deshalb 50 Fragen zufällig aus dem Gesamtpool und zeigt die entstandene Kapitelverteilung in der Auswertung.

## Lokal starten

Voraussetzung: Node.js 22.13 oder neuer.

```bash
npm ci
npm run dev
```

Danach die im Terminal angezeigte lokale Adresse öffnen.

## Prüfen und bauen

```bash
npm test
```

Der Befehl erstellt den Produktions-Build und prüft unter anderem:

- Vollständigkeit der 150 Fragen
- Kapitelgrössen 53 / 26 / 28 / 33 / 10
- drei Antwortmöglichkeiten und gültiger Lösungsschlüssel pro Frage
- Vorhandensein aller 23 Bilddateien
- Zuordnung der 17 Fischbilder zu den korrekten Arten

Nur bauen:

```bash
npm run build
```

Produktiv lokal starten:

```bash
npm run start
```

## GitHub

Das Projekt kann unverändert in ein GitHub-Repository übernommen werden. Der Workflow unter `.github/workflows/ci.yml` führt bei jedem Push und Pull Request automatisch den vollständigen Build und die Datentests aus.

## Inhaltlicher Stand

- Fragenbasis: bereitgestellter «Fragenkatalog 1–150», Ausgabe 2020
- Prüfungsmodus: offiziell verifiziert am 1. September 2026
- Sprache: Deutsch, Schweizer Rechtschreibung

Fragenkatalog und Abbildungen sind nicht Bestandteil der MIT-Lizenz für den App-Code; für eine öffentliche Weiterverbreitung sind die Rechte des jeweiligen Herausgebers zu beachten.
