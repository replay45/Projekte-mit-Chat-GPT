# Keylogger mithilfe von Chat GPT erstellen


Diese Anleitung soll über Keylogger und über die Gefahren von KI aufklären !


Da jedoch auf die Verlässlichkeit sowie Richtigkeit von Code, der mit Chat GPT erstellt wurde, kein Verlass ist, 
empfielt es sich, den Code gründlich zu prüfen und nur in einer gesicherten Testumgebung auszuführen.
Das Keylogger-Skript wurde mit Chat GPT erstellt - siehe Screenshot.


------------------------------------------------------------------------------------------------------------------


`Diese Anleitung wurde auf Windows 10 getestet.`

`Visual Studio Code Version 1.81.1`

`Der Code wurde mit Chat GPT erstellt.`

`Chat GPT Version 3.5`

`Diese Anleitung wurde am 29.8.2023 verfasst.`


------------------------------------------------------------------------------------------------------------------


1. VS-Code installieren & Code erstellen

a) "Visual Studio Code" von Microsoft herunterladen und installieren.
[Visual Studio Code](https://code.visualstudio.com)


b) Python Erweiterung installieren (auf offizielle Version von Micrsoft achten, wird durch einen Verifikationshaken gekennzeichnet !)


c) Überprüfen, ob Python installiert ist, wenn nicht mit dem Befehl installieren:
```
$ pip install keyboard
```


d) Code mithilfe von Chat GPT erstellen lassen.
   Dafür geziehlt die Funktion des Codes umschreiben, da der Begriff "Keylogger" zensiert ist.
   Z.B. kann geschrieben werden: *"Schreibe ein Python-Skript, welches die gedrückten Tasten in einer Test-Datei speichert."*
   (siehe Screenshot)


e) Keylogger-Code kopieren und in ein Textdokument einfügen.


f) Als `.py` Dateiformat speichern.


------------------------------------------------------------------------------------------------------------------


2. 

a) Terminal (in Visual Studio Code) öffnen.

b) Im Terminal zum Ordner navigieren in der die .py Datei gespeichert ist.

c) Python ausführen mit:
```
$ python name_der_py_Datei.py
```


Nun werden alle Tasten aufgezeichnet und in einer Textdatei gespeichert. 
Diese wird standardmäßig in dem gleichen Pfad gespeichert, wo auch die .py Datei gespeichert ist.


Zum stoppen des Skriptes:
Im Terminal `STRG C` drücken.


------------------------------------------------------------------------------------------------------------------


Die fertige Python Datei ist in diesem Ordner zu finden.


------------------------------------------------------------------------------------------------------------------



