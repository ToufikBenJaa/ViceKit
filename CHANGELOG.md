# Changelog

All notable changes to ViceKit are documented in this file.

## [0.2.0] - 2026-11-26

This version adds a texture viewer and an interactive 3D model viewer.

### Textures
- Open texture dictionaries (`.ztd`) to see every texture they contain, with their size, format and mip levels.
- Zoom and pan, and choose the mip level, the array slice or cube face, the colour channels and the background.
- Supports BC1 to BC7 and uncompressed formats, including texture arrays, cube maps and volume textures.
- Save any texture as a DDS file.
- Open standalone `.dds` files with **File › Open file…**.

### 3D models
- Open models (`.zdr`), fragments (`.zft`) and model dictionaries (`.zdd`) in an interactive 3D view.
- **Camera:** orbit around the point under the cursor, pan, zoom towards the cursor, and fly with the keys in the W A S D position (whatever your keyboard layout). Front, back, side and top views, and an orthographic mode.
- **Meshes:** list a model's meshes and show or hide them. Click a mesh in the 3D view to select it, Ctrl+click to add to the selection, or Shift+drag a box. Hide the selection, show only the selection, or show everything again. Hover a mesh to see its name and shader slot.
- **Detail levels:** switch between the levels of detail, or compare two side by side or overlaid.
- **Dictionaries and fragments:** pick one model, or show all of them at once.
- **Display:** shaded, colour per mesh, UV checker, UV coordinates, face orientation and face normals, wireframe, ground grid, axis gizmo, statistics, and adjustable lighting and background.
- **Materials** page: the shaders each mesh uses and the textures they reference.
- Jump from a mesh to its material, or to its vertex and index data in the Hex view.
- Save screenshots as PNG at 1×, 2× or 4× the view size, optionally with a transparent background.
- Export the visible meshes to glTF (`.glb`) or OBJ for Blender and other 3D tools.

### Browsing
- Over 575,000 known file names, up from 65,000.
- Search updates as you type. Clearing the search box returns to the folder you were in, and archives found by a search open like any other archive.
- Clearer file types and a "Size in archive" column.
- A simpler properties pane: file name, name hashes and a readable path such as `levels.rpf → /levels/americas/…`.
- Installation details now open in their own window (**View › Installation details…**).
- Viewer windows show the file's size and full path at the bottom.

### Metadata
- The structure view of `.zmt` files shows each section in its own tab, with tables and highlighted values.
- Fixed: definitions with several members in the LSCH and LENM sections did not list their members.

### Other
- **About** shows the version and has a **Report a bug** button.
- Failed saves and exports are reported in a message box instead of silently.
- Cancelling an extraction started from a viewer returns to that viewer.

### Known limitations
- Models are shown without their textures for now.
- Some textures are stored in the streamed texture packages (`ttdb`) and cannot be opened yet.
- Vertex normals are not decoded yet, so models are lit per face.
- Characters are made of separate parts (head, hair, clothes…) that open one by one; they are not assembled.
- Search covers the archives you have opened, including the ones nested inside them once opened.
- Read-only: files cannot be modified or repacked.
- Only the Xbox Series X|S build 1.0.2.1 is supported for now.

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
