# Ableton Set Cleaner

Analyzes an Ableton Live set (.als) and cleans up the associated project folder—only the files that are actually needed remain.

## Web-App

**[https://github.com/BatzeBitBuilder/Ableton-Set-Cleaner](https://batzebitbuilder.github.io/Ableton-Set-Cleaner/)**

Runs entirely locally in the browser; no files are uploaded. Chrome or Edge is recommended for accessing folders.

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
