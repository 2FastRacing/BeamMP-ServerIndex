# BeamMP Server HTML Generator

A simple utility that automatically scans all BeamMP server directories, extracts IP/Port/AuthKey information from `ServerConfig.toml` files, and generates a clean, readable HTML file (`servers.html`) containing the full server list.

---

## 📦 Features

- Automatically detects all BeamMP servers within the same folder hierarchy.
- Extracts:
  - Server Name (folder)
  - Local IPv4 Address
  - Port
  - AuthKey
- Groups results by root directory (e.g. `moddedServers`, `vanillaServers`, etc.)
- Generates `servers.html` for easy viewing.
- Automatically opens the HTML in your default browser.
- Optional debug mode to pause execution after completion.

---

## 📁 Folder Structure

Place the tool in the **root directory** that contains all of your BeamMP server folders, like this:

