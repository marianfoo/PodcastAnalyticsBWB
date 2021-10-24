# Analyse des Podcasts 'Baywatch Berlin'

# Einleitung

Der Markt der Podcasts ist in den letzten Jahren stark gewachsen. Viele neue Podcasts treffen auf viele neue Hörer.
Dies ermöglicht auch einen Podcasts zu vermarkten und in dessen Werbung zu schalten.
Dies macht auch der Podcast von Klaas Heufer-Umlauf, Thomas Schmitt und Jakob Lundt, genannt 'Baywatch Berlin'.
Die Werbeeinblendungen sind klar vom Content durch einen Insert getrennt.

# Ziel

Durch diesen Insert, sollte es einfach sein den Anfang und Ende der Werbeeinblendungen klar herauszufiltern.
So kann einfach der Insert aus einer Folge herausgeschnitten werden, und in allen Folgen gesucht werden

# Vorgehenweise

Hier werden die einzelnen Schritte beschrieben wie vorgegangen worden ist.

## Recherche

Als Grundlage wird die Python Programmiersprache genutzt. Als IDE wird Jupyter mit Anaconda hergenommen.
Es sollte eine möglich einfacher herangehensweise genutzt werden.
Nach kurzer Recherche wurde eine Stackoverflow Antwort gefunden die nützlich sein könnte.
https://stackoverflow.com/a/67469084

Diese Antwort wurde angepasst und auf diesen Use Case zugeschnitten.

## MP3 Dateien umformatieren

Für die Analyse mussten die Dateien in das wav Format gebracht werden.

Für eine geringere Datei Größe und eine schnellere Bearbeitung wurden vorher die Dateien zu einer kleineren mp3 Datei konvertiert:

mp3 Original --> mp3 kleinere Bitrate --> wav

## Werbung Timestamp finden

Das [Snippet](https://stackoverflow.com/a/67469084) wurde hier angepasst und verwendet.
Einzig die Korrelationswerte mussten angepasst werden, die steuert ab wann ein Übereinstimmung markiert wird.
Da nur die Daten gespeichert wurden, sind die Grafiken auch nicht notwendig und wurden entfernt.

## Analyse der Timestamps

Für die Analyse wurden die Daten aufbereitet und mit plotly dargestellt.

## Analyse der Metadaten

Für die Analyse der Metadaten wurden diese von den mp3s ausgelesen.
Dargestellt wurde die Laufzeit je Episode sowie die Laufzeit der Episode mit einer Trendlinie

# Ergebnis

Schlussendlich wurde das Ziel erreicht und die Timestamps konnten erfolgreich herausgelesen werden.
Bei der Auswertung wurde deutlich dass es immer zwei Werbeblöcke gibt.
Erstaunlicherweise beträgt die Summe dieser Blöcke so gut wie immer 284 Sekunden.
Seit Folge 94 ist die jedoch anscheinend nicht mehr der Fall.

Die Länge der Folgen hat auch an Volatilität zugenommen.
Zwischen Folge 30 und 66 waren die Folgen meist rund 90 Minuten lang.
So konsequent sind diese Ergebisse nicht und die Folgenlänge schwankt stark zwischen 93 und 67 Minuten.