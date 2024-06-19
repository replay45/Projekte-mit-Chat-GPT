
# Läuft ein Keylogger auf meinem PC?


## Inhaltsverzeichnis
1. Überprüfe laufende Prozesse
2. Überprüfe Autostart-Einträge
3. Überprüfe verdächtige Dateien
4. Netzwerkaktivität überwachen
5. Antivirus- oder Anti-Malware-Software
6. Python-Skripte suchen


------------------------------------------


Die **meisten** Keylogger werden in der Sprache Python geschrieben und werden als .py-Datei gespeichert. Deswegen folgt hier eine Anleitung, wie nach Python-Skripte auf einem Gerät gesucht werden kann. 

Keylogger können jedoch auch in anderen Sprachen programmiert werden:
JavaSkript, AutoHotkey (ahk), PowerShell und Ruby.
Um vollständig ausschließen zu können, dass kein Keylogger mitschreibt müsste eine Ausschließung auch von diesen Sprachen folgen. 


------------------------------------------------------------------


### Disclaimer
**Es besteht keine absolute Garantie, dass nicht dennoch ein Keylogger auf dem Gerät läuft.**

**Es gibt verschiedene Möglichkeiten, um nach einem Keylogger in Pythonsprache zu suchen. Hier werden sechs Optionen für Windows, macOS und Linux aufgelistet:**


--------------------------------------------------------------


**1. Überprüfe laufende Prozesse**

Windows: 
- öffne den Task-Manager und suche nach Python-Prozesse
- Drücke `Strg + Umschalt + Esc` um den Task-Manager zu öffnen, und schaue unter "Prozesse" nach `python.exe` oder `pythonw.exe`

macOS:
- Öffne den den Aktivitätsmonitor und suche nach Python-Prozesse 
- suche im nach Aktivitätsmonitor `python`

Linux:
- nutze das Terminal und suche nach Python-Prozessen
- führe hier den Befehl `ps aux | grep python` aus

---------------------------------------------------------------

**2. Überprüfe Autostart-Einträge**

Manchmal können solche Skripte so eingestellt sein, dass sie beim Hochfahren des Systems automatisch starten. Überprüfe daher die Autostart-Einträge:

Windows:
- Öffne den Task-Manager und gehe zu "Autostart"

macOS:
- Gehe zu `Systemeinstellungen` -> Benutzer & Gruppen -> Anmeldeobjekte`

Linux:
- Überprüfe die `.bashrc`, `.bash_profile`, `.profile` oder die `crontab`-Einträge (`crontab -l` im Terminal)

-----------------------------------------------------------------------------------------------------------------

**3. Überprüfe verdächtige Dateien**

Solche Skripte speichern die Tasteneingaben oft in einer Datei. Suche nach kürzlich geänderten Dateien:

Windows: 
- Benutze die Dateisuche, um Dateien zu finden, die kürzlich geändert wurden

macOS und Linux: 
- Verwende das Terminal und führe den Befehl `find / -type f -mtime -1` aus, um Dateien zu finden, die in den letzten 24 Stunden geändert wurden. Du kannst die Zeitspanne     nach Bedarf anpassen

----------------------------------------------------------------------

**4. Netzwerkaktivität überwachen**

Einige Keylogger senden die gesammelten Daten über das Netzwerk:

Windows:
- Benutze den Ressourcenmonitor (`Ressourcenmonitor` im Task-Manager) und überprüfe die Netzwerkaktivität

macOS: 
- Verwende das Netzwerk-Dienstprogramm (`netstat` Befehl im Terminal)

Linux: 
- Verwende `netstat -tuln` oder `iftop` (muss eventuell installiert werden)

----------------------------------------------------------------------------------

**5. Antivirus- oder Anti-Malware-Software**

Führe einen vollständigen Systemscan mit einer aktuellen Antivirus- oder Anti-Malware-Software durch. Viele dieser Programme können bekannte Keylogger erkennen und entfernen.

-------------------------------------------------------

**6. Python-Skripte suchen**

Durchsuche dein Dateisystem nach Python-Skripten:

Windows: 
- Verwende die Dateisuche im Explorer, um nach `*.py`-Dateien zu suchen

macOS und Linux:
- Verwende das Terminal und führe `find / -name "*.py"` aus

------------------------------------------------------------------------------

**Wenn du ein verdächtiges Python-Skript gefunden hast, öffne es in einem Texteditor und suche nach Bibliotheken wie pynput, keyboard oder pyxhook, die zur Überwachung von Tastatureingaben verwendet werden. Dies hilft dir zu überprüfen, ob die verdächtige Datei ein Keylogger ist.**
