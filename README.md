# Minecraft Resource Pack Manager v2026 - resource pack manager 2026

> **Minecraft Resource Pack Manager is a browser-based utility for combining and arranging Minecraft resource packs into one ZIP, with project data stored locally and a current 2026 release.**

[![Platform](https://img.shields.io/badge/Platform-browser-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/leo-fisher55/minecraft-resource-pack-manager?style=flat-square)](https://github.com/leo-fisher55/minecraft-resource-pack-manager)

---

<p align="center">
  <a href="https://leo-fisher55.github.io/minecraft-resource-pack-manager/">
    <img src="https://img.shields.io/badge/Download-Minecraft%20Resource%20Pack%20Manager%20Latest-brightgreen?style=for-the-badge" alt="Download Minecraft Resource Pack Manager">
  </a>
</p>

> **[Direct Download - Minecraft Resource Pack Manager v2026](https://leo-fisher55.github.io/minecraft-resource-pack-manager/)**

---

[Download Latest Build](https://leo-fisher55.github.io/minecraft-resource-pack-manager/)

---

## What Minecraft Resource Pack Manager Does

Minecraft Resource Pack Manager is built to take several Minecraft resource packs and turn them into one consolidated export. Because it runs fully in the browser, there is no installation process, no server to provision, and no backend service to maintain. That makes it useful for players, pack authors, and anyone who wants a fast way to assemble textures, sounds, and metadata into a single ZIP file.

Project state is preserved locally through localStorage and IndexedDB, so work can carry over between sessions. The app also offers priority-based source ordering, conflict resolution, and automatic regeneration of `pack.mcmeta` for the chosen Minecraft version, reducing the amount of manual cleanup needed during pack assembly.

---

## Main Features

- Combine several resource packs into one ZIP archive
- Runs entirely in the browser without requiring a server
- Saves projects locally with localStorage and IndexedDB
- Lets you set source priority with ordered pack layers
- Resolves conflicts when assets overlap during rebuilds
- Regenerates `pack.mcmeta` for the selected Minecraft version
- Imports packs from Modrinth with direct download support
- Handles custom item textures, block textures, and sounds
- Exports and imports projects as JSON for backup or transfer

---

## Getting Started

You can open the hosted build directly in a compatible browser:

[Download Latest Build](https://leo-fisher55.github.io/minecraft-resource-pack-manager/)

If you want to run from source, clone the repository and open the app in a browser-based environment:

```bash
git clone https://github.com/leo-fisher55/minecraft-resource-pack-manager.git
cd resource-packs-minecraft-manager
```

From there, load the HTML entry point in your browser or serve the directory with any static file host.

---

## How to Use It

1. Open the app in your browser.
2. Start a new project or load one you already saved.
3. Add resource packs from local files or supported online sources.
4. Reorder packs to control priority and handle overlapping content.
5. Check textures, sounds, and metadata before exporting.
6. Build the merged pack and download the ZIP output.

Example workflow for project management:

- Import a pack from Modrinth when available.
- Adjust source order to control which files take precedence.
- Regenerate the output for the target Minecraft version.
- Export the project as JSON if you want to save a portable copy.
- Import that JSON later to continue editing.

---

## Configuration

Most project state lives in the browser instead of a separate config file. Settings, saved projects, and persisted data are stored via localStorage and IndexedDB.

Typical project options include:

```json
{
  "targetMinecraftVersion": "1.21",
  "sourceOrder": ["base-pack", "override-pack"],
  "exportFormat": "zip"
}
```

If your workflow depends on a specific pack version or asset priority, update those values before rebuilding the final ZIP.

---

## Requirements

- A modern browser with support for browser storage APIs
- Enough local storage space for projects and imported assets
- Access to ZIP export features in the browser environment
- Internet access only if you want to use online imports such as Modrinth support

---

## FAQ

**Does it need a backend server?**  
No. The app is browser-only and does not require a server component.

**Where are projects saved?**  
Projects are kept locally in the browser using localStorage and IndexedDB.

**Can I move a project to another device?**  
Yes. Export the project as JSON, then import it on the other device.

**How do I handle pack conflicts?**  
Use source ordering to decide which pack should take priority when files overlap.

**Can it import from online pack sources?**  
It includes Modrinth import support with direct download handling.

**What if I need a different Minecraft version?**  
Update the target version before rebuilding, and the tool can regenerate `pack.mcmeta` for that version.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
