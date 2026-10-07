# Ableton Set Cleaner

Analysiert ein Ableton Live Set (`.als`) und bereinigt den zugehörigen Projektordner – nur die tatsächlich benötigten Dateien bleiben übrig.

## Web-App

**https://github.com/BatzeBitBuilder/Ableton-Set-Cleaner**

Läuft komplett lokal im Browser, es werden keine Dateien hochgeladen. Für den Ordnerzugriff wird Chrome oder Edge empfohlen.

## Windows-Programm

`ALS-Cleaner.exe` unter [Releases](../../releases) herunterladen.

## Python-Skript

Nur Standardbibliothek (Python 3.8+), Live 9–12.

```
python ableton_set_cleaner.py                       # Web-Oberfläche (127.0.0.1)
python ableton_set_cleaner.py gui                   # Tk-Oberfläche
python ableton_set_cleaner.py analyze "Song.als"    # Bericht
python ableton_set_cleaner.py clean   "Song.als" [--name "Song v2"] [--out DIR] [--collect]
python ableton_set_cleaner.py clean   "Song.als" --in-place
```

`clean` erzeugt ein neues Projekt, das Original bleibt unverändert. `--in-place` verschiebt ungenutzte Dateien in einen Quarantäne-Ordner, es wird nichts gelöscht.

EXE selbst bauen: `build_exe.bat` (benötigt PyInstaller).
