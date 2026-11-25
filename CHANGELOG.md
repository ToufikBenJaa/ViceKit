# Changelog

All notable changes to ViceKit are documented in this file.

## [0.1.0] - 2026-11-25

Initial release. ViceKit is a read-only toolkit for exploring Grand Theft Auto VI game files. This first version supports the **Xbox Series X|S** release (build 1.0.2.1).

### Game folder
- Choose your game folder once; ViceKit remembers it (and recent folders) and checks it again at every start.
- Verifies `game_scarlett_master.exe` and reads the data it needs to open the archives directly from your own copy of the game. Nothing from the game is included with ViceKit or saved to disk.
- Clear messages when the selected folder is not a supported installation.

### Browsing
- Explorer-style layout: folders and RPF archives on the left, the selected folder's content on the right.
- Browse the whole game folder, including its subfolders and loose files.
- Open RPF archives and the archives nested inside them.
- Over 65,000 known file names; unnamed entries are shown by their hash.
- Sortable columns (name, type, size, stored size) and details such as compression, encryption and entries that cannot be read yet.
- Back, Forward and Up navigation, an address bar, and multiple selection.
- Search the opened archives by name or hash.
- Properties pane with the technical details of the selected item.

### Viewing
- Open any file in its own window.
- **Hex** view for files of any size.
- **Text** view for files of any size, with automatic or manual encoding (UTF-8, UTF-16, Latin-1).
- **Structure** view for `.zmt` metadata files.
- Compressed and encrypted entries are decoded automatically.

### Extracting
- Extract single files, multiple selections, whole folders or whole archives.
- File names are made safe for Windows, and unfinished extractions are cleaned up.

### Requirements
- Windows 10 version 1809 or later (x64).
- Your own copy of the Xbox Series X|S release of Grand Theft Auto VI (build 1.0.2.1).
- No installation needed: unzip and run `ViceKit.exe`.

### Known limitations
- Read-only: files cannot be modified or repacked.
- Only the Xbox Series X|S build 1.0.2.1 is supported for now.
- Some entries cannot be read yet (external volumes and a few unsupported formats); they are listed and marked as such.
- No texture or 3D model viewers yet.
