# Hasekll in Docker #

Es gibt zwei Möglichkeiten, Haskell in Docker zu entwickeln.
Einerseits mit VS Code und Docker zusammen. Das hat den Vorteil, dass man dann auch Autocompletion und Syntax Highlithing hat.
Andererseits geht es aber auch einfach nur mit Docker, ohne VS Code.


## VS Code mit Docker ##

### Voraussetzungen ###

Installiert sowohl [**Docker**](https://www.docker.com/) als auch [**Visual Studio Code**](https://code.visualstudio.com/) auf eurem Gerät.
Beide Programme gibt es für *Windows, Linux, MacOS*.

Danach müsst ihr dieses Git Repository mittels
```bash
git clone git@informatik.....
```
klonen oder euch [hier]() die zip Datei herunter laden und entpacken.


### Einrichtung ###

Öffnet Visual Studio Code.
Dann geht ihr in den Extensions Tab (linke Seitenleiste) und installiert die **Remote Developement** Extension.
Nun solltet ihr in den linken unteren Ecke des Fensters ein blauen Rechteck sehen.

Anschließend klickt ihr auf File->Open Folder und öffnet das repo bzw. das entpackte Zip.

Euch sollte unten rechts ein Dialog Fenster angezeigt werden, dass folgende Möglichkeit bietet: **Reopen in Container**. Das müsst ihr anklicken.
Wenn dieser Dialog nicht erscheint, klickt ihr auf das quadrat unten Links und anschließend auf *Rebuild Container*. ***Das kann einige Minuten dauern!***


### Nutzen ###

Ihr könnt nun eure Haskell Dateien Links im File Explorer erstellen/ablegen (dort existiert bereits test.hs).
Um dann den ghci zu starten, klickt ihr auf *Terminal->New Terminal* und gebt dann *ghci* in die Kommandozeile ein.

Über das so erzeugte Terminal könnt ihr auch cabal benutzen.

## Nur Docker ##

## Voraussetzungen ##

Ihr müsst euch lokal [**Docker**](https://www.docker.com/) installieren.
Das Programm gibt es für Windows, MacOS und Linux.

## Benutzung ##

Führt folgenden Befehl in der Kommandozeile aus:
```
docker run -it --rm --mount type=bind,source=<Pfad zum Ordner mit euren Haskell Dateien>,target=/hs_files thewombat/dockerprog
```