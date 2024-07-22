# Läuft ein Keylogger auf meinem PC ?


## Inhaltsverzeichnis

1. Was ist ein Keylogger ?
2. Windows Freihand-& Eingabeanpassung - oder auch "Microsofts Keylogger" ?
3. Überprüfen laufender Prozesse
4. Überprüfen von Autostart-Einträgen
5. Überprüfen verdächtiger Dateien
6. Netzwerkaktivität überwachen
7. Antivirus- oder Anti-Malware-Software
8. lokale Dateien nach Python-Skripten durchsuchen
9. Wie erkenne ich, ob eine Python-Datei ein Keylogger ist ?


----------------------------------------------------------------------------------------------------------------


### Disclaimer

Auch wenn diese Anleitung einige Anhaltspunkte liefert, gibt es durch die genannten Punkte dennoch KEINE Garantie, dass nicht doch Schadsoftware oder ein Keylogger Aktivitäten aufzeichnet.

Wer zudem nicht möchte, dass Microsoft ein benutzerdefiniertes Wörterbuch aus allen Eingaben, die auf dem Windows PC erfolgen, erstellt, kann dies ebenfalls deaktivieren - mehr dazu unter Punkt 2. 


----------------------------------------------------------------------------------------------------------------


# 1.  Was ist ein [Keylogger](https://de.wikipedia.org/wiki/Keylogger) ?


Ein Keylogger ist eine Soft- oder Hardware, die Tastatureingaben aufzeichnet.
Somit ist es möglich, an vertrauliche Daten, wie z.B. Passwörter zu gelangen.

Die meisten Keylogger werden in der [Programmiersprache Python](https://www.python.org/) geschrieben und als `.py`-Datei gespeichert.
Daher folgen hier einige Punkte, die zeigen, wie man Python Skripte, die möglicherweise unerwünscht sind, finden kann.

Keylogger können jedoch auch in anderen Sprachen programmiert werden, wie z.B. [JavaScript](https://wiki.selfhtml.org/wiki/JavaScript), [PowerShell](https://de.wikipedia.org/wiki/PowerShell) oder [Ruby](https://www.ruby-lang.org/de/).
Um ausschließen zu können, dass kein Keylogger aktiv ist, sollte man auch Skripte u.a. in diesen Sprachen überprüfen.


## WICHTIG

Es gibt auch Hardware-Keylogger, die zwischen die Tastatur und den PC gesteckt werden, um die Tastatureingaben aufzuzeichnen.
Es ist daher ratsam, auch die USB-Verbindungen zum PC zu prüfen.


----------------------------------------------------------------------------------------------------------------


**Es gibt verschiedene Möglichkeiten, um nach einem Python-Keylogger zu suchen. Hier werden einige Optionen für [Windows](https://www.microsoft.com/de-de/windows?r=1), [MacOS](https://support.apple.com/de-de/macos) und [Linux](https://de.wikipedia.org/wiki/Linux) aufgelistet:**


----------------------------------------------------------------------------------------------------------------


# 2. Windows Freihand-& Eingabeanpassung - oder auch "Microsofts Keylogger" ?


Die Windows Freihand- & Eingabeanpassung ist eine Funktion, die Eingaben in Anwendungen verbessert, indem sie das Nutzerverhalten analysiert, ein persönliches Wörterbuch anlegt und Vorschläge macht. Dies kann die Geschwindigkeit und Effizienz bei der Eingabe von Texten, auf Kosten des Datenschutzes, erhöhen.


Auch wenn die Freihand-& Eingabeanpassung genaugenommen kein Keylogger ist, empfiehlt es sich jedoch, diese datenschutzunfreundliche Funktion zu deaktivieren, damit Windows keine Tastatureingaben aufzeichnet.


## Deaktivierung der Windows Freihand- & Eingabeanpassung:

- Öffnen der Einstellungen.
- Zu Datenschutz & Sicherheit gehen.
- Im Menü „Freihand und Eingabeanpassung“ wählen.
- Deaktivieren der Funktion.


----------------------------------------------------------------------------------------------------------------


# 3. Überprüfen laufender Prozesse


Windows:
- [Taskmanager](https://de.wikipedia.org/wiki/Taskmanager) öffnen und nach Python-Prozessen suchen:
- `Strg + Umschalt + Esc` drücken, um den [Taskmanager](https://de.wikipedia.org/wiki/Taskmanager) zu öffnen und unter `Prozesse` nach `python.exe` oder `python` suchen.


MacOS:
- Den [Aktivitätsmonitor](https://support.apple.com/de-de/guide/activity-monitor/welcome/mac) öffnen und nach Python-Prozessen suchen:
- Im [Aktivitätsmonitor](https://support.apple.com/de-de/guide/activity-monitor/welcome/mac) kann nach `python` gesucht werden.


Linux:
- Systemmonitor nutzen, um laufende Prozesse nach Python-Dateien zu durchsuchen.

- Alternativ das Terminal nutzen, um nach Python-Prozessen zu suchen:
- Folgenden Befehl ausführen:

```
$ ps aux | grep python
```


----------------------------------------------------------------------------------------------------------------


# 4. Überprüfen von Autostart-Einträgen


Häufig können solche Skripte so eingestellt sein, dass sie beim Hochfahren des Systems automatisch starten.


Windows:
- Öffnen des [Taskmanagers](https://de.wikipedia.org/wiki/Taskmanager) und zu `Autostart` wechseln.
- Programme/Dateien im Autostart überprüfen.


MacOS:
- Zu `Systemeinstellungen` -> `Benutzer & Gruppen` -> `Anmeldeobjekte` gehen, um Autostart-Einträge zu prüfen.


Linux:
- Die gängigen Benutzeroberflächen, wie z.B. [GNOME](https://www.gnome.org/) haben eine App, in der die Autostart-Einträge geprüft werden können.

- Alternativ die `.bashrc`, `.bash_profile`, `.profile` oder die `crontab`-Einträge (` $ crontab -l` im Terminal) überprüfen.


----------------------------------------------------------------------------------------------------------------


# 5. Überprüfen verdächtiger Dateien

Solche Skripte speichern die Tasteneingaben oft in einer Datei.

Daher kann man auch nach einer kürzlich geänderten Datei suchen:


Windows: 
- Es kann die Dateisuche im [Explorer](https://de.wikipedia.org/wiki/Windows-Explorer), um Dateien zu finden, die kürzlich geändert wurden, genutzt werden.


MacOS und Linux: 
- Verwende das Terminal und führe den Befehl `$ find / -type f -mtime -1` aus, um Dateien zu finden, die in den letzten 24 Stunden geändert wurden. 
- Die Zeitspanne kann nach Bedarf angepasst werden.


----------------------------------------------------------------------------------------------------------------


# 6. Netzwerkaktivität überwachen

Einige Keylogger senden die gesammelten Daten über das Netzwerk:


Windows:
- Benutzen des `Ressourcenmonitors` im [Taskmanager](https://de.wikipedia.org/wiki/Taskmanager), um Netzwerkaktivitäten einsehen zu können.


MacOS:
- Verwenden das Netzwerk-Dienstprogramms
- Im Terminal kann `netstat` genutzt werden.

```
$ netstat
```


Linux:
- Verwenden von `$ netstat -tuln` oder `$ iftop` im Terminal.
- Diese müssen evtl. noch nachinstalliert werden.


----------------------------------------------------------------------------------------------------------------


# 7. Antivirus- oder Anti-Malware-Software

Bei Bedarf kann ein vollständiger Systemscan mit einer aktuellen Antivirus-/ Anti-Malware-Software durchgeführt werden.
Viele dieser Programme können bekannte Keylogger erkennen und entfernen.

Windows
- Generell empfiehlt sich der [Windows Defender Anti-Virus](https://de.wikipedia.org/wiki/Microsoft_Defender), der bereits von Haus aus `auf Windows vorinstalliert` ist, zumindest für `Privatpersonen`.


MacOS / Linux
- Auf MacOS sowie Linux ist in der Regel `kein Anti-Virus nötig`. Wer allerdings dennoch auf einen Anti-Virus zurückgreifen möchte, kann in dem Repository [Linux_Ethical-Hacking_RaspberryPI - unter Sicherheit-auf-Linux](https://github.com/replay45/Linux_Ethical-Hacking_RaspberryPI/tree/main/linux)` wissenswertes über Sicherheit auf Linux` erfahren.



----------------------------------------------------------------------------------------------------------------


# 8. lokale Dateien nach Python-Skripten durchsuchen

Durchsuchen des Dateisystems nach Python-Skripten:


Windows: 
- Verwenden der Dateisuche im [Explorer](https://de.wikipedia.org/wiki/Windows-Explorer), um nach `.py`-Dateien zu suchen.


MacOS und Linux:
- Auch hier kann der Dateimanager verwendet werden, um nach Python-Dateien zu suchen.
- Alternativ: Verwenden des Terminals und folgenden Befehl ausführen `$ find / -name "*.py"`.


----------------------------------------------------------------------------------------------------------------


# 9. Wie erkenne ich, ob eine Python-Datei ein Keylogger ist ?

Sollte ein verdächtiges Python-Skript gefunden werden, kann dies auf  `Bibliotheken` wie `pynput`, `keyboard` oder `pyxhook` überprüft werden, denn diese werden häufig für einen Keylogger verwendet und könnten ein Hinweis darauf sein, dass die Python-Datei ggf. unerwünschte Aktivitäten der Tastatur aufzeichnet.

Das Skript kann in einem beliebigen Texteditor geöffnet werden, um eine manuelle Überprüfung vorzunehmen.


----------------------------------------------------------------------------------------------------------------

