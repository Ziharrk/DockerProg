# DeklProg Haskell VS Code #


## Voraussetzungen ##

Installiert sowohl [**Docker**](https://www.docker.com/) als auch [**Visual Studio Code**](https://code.visualstudio.com/) auf eurem Gerät.
Beide Programme gibt es für *Windows, Linux, MacOS**.

Danach müsst ihr dieses git repository mittels
```bash
git clone git@informatik.....
```
klonen oder euch [hier]() die zip Datei herunter laden und entpacken.


## Starten ##

Öffnet Visual Studio Code.
Dann geht ihr in den Extensions Tab (linke Seitenleiste) und installiert die **Remote Developement** Extension.
Nun solltet ihr in den linken unteren Ecke des FEnsters ein blauen Rechteck sehen.

Anschließend klickt ihr auf File->Open Folder und öffnet das repo bzw. das entpackte Zip.

Nun klickt ihr auf das quadrat unten Links und anschließend auf *Rebuild Container*. Das kann einige Minuten dauern.


## Nutzen ##

Ihr könnt nun eure Haskell Dateien Links im File Explorer erstellen/ablegen (dort existiert bereits test.hs).
Um dann den ghci zu starten, klickt ihr auf Terminal->New Terminal und gebt dann *ghci* ein.

Über das so erzeugte Terminal könnt ihr auch cabal benutzen.