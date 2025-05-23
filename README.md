# Haskell in Docker #

Es gibt zwei Möglichkeiten, Haskell in Docker zu entwickeln.
Einerseits mit VS Code und Docker zusammen. Das hat den Vorteil, dass man dann auch Autocompletion und Syntax Highlithing hat.
Andererseits geht es aber auch einfach nur mit Docker, ohne VS Code.


## VS Code mit Docker ##

### Voraussetzungen ###

Installiert sowohl [**Docker**](https://www.docker.com/) als auch [**Visual Studio Code**](https://code.visualstudio.com/) auf eurem Gerät.
Beide Programme gibt es für *Windows, Linux, MacOS*.

Danach müsst ihr dieses Git Repository mittels
```bash
git clone --recursive https://git.informatik.uni-kiel.de/stu223745/dockerprog.git
```
klonen (alternativ ssh) oder euch [hier](https://git.informatik.uni-kiel.de/stu223745/dockerprog/-/archive/main/dockerprog-main.zip) die zip Datei herunter laden und entpacken. Allerdings fehlt dann das deklprog-template und kann nicht genutzt werden (nicht empfohlen!)


### Einrichtung ###

Öffnet Visual Studio Code.
Dann geht ihr in den Extensions Tab (linke Seitenleiste) und installiert die **Remote Developement** Extension.
Nun solltet ihr in den linken unteren Ecke des Fensters ein blauen Rechteck sehen.

Anschließend klickt ihr auf File->Open Folder und öffnet das repo bzw. das entpackte Zip.

Euch sollte unten rechts ein Dialog Fenster angezeigt werden, dass folgende Möglichkeit bietet: **Reopen in Container**. Das müsst ihr anklicken.
Wenn dieser Dialog nicht erscheint, klickt ihr auf das quadrat unten Links und anschließend auf *Rebuild Container*. ***Das kann einige Minuten dauern!***

### Benutzung ###

Ihr könnt nun eure Haskell Dateien Links im File Explorer erstellen/ablegen (dort existiert bereits test.hs).
Um dann den ghci zu starten, klickt ihr auf *Terminal->New Terminal* und gebt dann `ghci` in die Kommandozeile ein.

Über das so erzeugte Terminal könnt ihr auch cabal benutzen. Wenn ihr also das mitgelieferte Prokjekt-Template nutzen wollt, dann könnt ihr dieses via `cabal repl deklprog-temlate` laden.
**Dies ist der empfohlene Weg** Eure Aufgaben könnt ihr dann in `deklprog-template/src/Exercises/WeekX.hs` bearbeiten und mit `:l Exercises.WeekX` (für passendes X) in `ghci/cabal` laden.

## Nur Docker ##

### Voraussetzungen ###

Ihr müsst euch lokal [**Docker**](https://www.docker.com/) installieren.
Das Programm gibt es für Windows, MacOS und Linux.

### Benutzung ###

Führt folgenden Befehl in der Kommandozeile aus:
```
docker run -it --rm --mount type=bind,source=<Pfad zum Ordner mit euren Haskell Dateien>,target=/hs_files thewombat/dockerprog
```
