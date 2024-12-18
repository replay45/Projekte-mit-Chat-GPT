# PDF Dokumente mit einem von Chat GPT erstellten Pyton-Programms verschlüsseln


Da jedoch auf die Verlässlichkeit sowie Richtigkeit von Code, der mit Chat GPT erstellt wurde, kein Verlass ist,
empfielt es sich, den Code gründlich zu prüfen und nur in einer gesicherten Testumgebung auszuführen.


`Der Code wurde mit Chat GPT erstellt.`

`Chat GPT Version: 3.5`

`Diese Anleitung wurde am 30.1.2024 verfasst.`


-----------------------------------------------------------------------------------------------------------------------------


1. Zunächst muss die PyPDF2 Bibliothek installiert werden.

```
$ pip install PyPDF2
```


-----------------------------------------------------------------------------------------------------------------------------


2. Code erstellen:

- Nun kann Chat GPT geöffnet werden und der gewünschte Python Code erstellt werden.

- Dafür kann z.B. in die Eingabe von Chat GPT Folgendes eingegeben werden:
`"Schreibe ein Python-Programm, womit man PDFs mit einem Passwort schützen kann."`

- Bei dem erstellten Code müssen natürlich die Platzhalter mit dem Pfad und dem gewünschten Passwort ersetzt werden !


-----------------------------------------------------------------------------------------------------------------------------


3. PDF mit einem Passwort schützen:

- Code kopieren und in eine Datei einfügen.
- Diese als `pdf-pw-schutz.py` speichern.
- Es empfiehlt sich, ein Backup der PDF-Datei zu erstellen, falls der Verschlüsselungsvorgang fehlschlägt.


-----------------------------------------------------------------------------------------------------------------------------


4. Den Code ausführen:

```
$ python3 pdf-pw-schutz.py
```

- Nun sollte die folgende Meldung erscheinen: `"PDF wurde erfolgreich mit dem Passwort geschützt"`

- Jetzt kann die ausgewählte PDF geöffnet werden, um zu verifizieren, dass das Passwort erfolgreich gesetzt wurde.


-----------------------------------------------------------------------------------------------------------------------------


5. PDF Passwort-Cracking:
- Im Anschluss könnte das Passwort z.B. mit `John the Ripper` über Bruteforce, ermittelt werden.


-----------------------------------------------------------------------------------------------------------------------------


Die fertige Python-Datei ist in diesem Ordner zu finden.


------------------------------------------------------------------------------------------------------------------
