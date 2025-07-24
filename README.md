# BeamMP Server Index

A simple utility that scans BeamMP server folders for `ServerConfig.toml` files, extracts their Port and AuthKey information, and generates a clean, organized `servers.html` file. It highlights any **duplicate Ports or AuthKeys in red**, helping prevent configuration conflicts at a glance.

---

## 🔧 Features

- Automatically scans all subfolders from where the tool is placed
- Extracts:
  - Server Name (folder name)
  - Local IPv4 address (auto-detected)
  - Port
  - AuthKey
- Groups servers visually by root directory (`moddedServers`, `vanillaServers`, etc.)
- Generates a neat HTML report
- Highlights **duplicate Ports or AuthKeys** in red
- Automatically opens the HTML file after running
- Optional `DEBUG_MODE` to pause after completion

---

## 📂 Folder Structure

Place the `.exe` or `serverIP.py` in the root of your BeamMP servers folder like this:

/YourServerDirectory/
├── moddedServers/
│ ├── MyTrack1/
│ │ └── ServerConfig.toml
│ └── MyTrack2/
│ └── ServerConfig.toml
├── vanillaServers/
│ └── DefaultMap/
│ └── ServerConfig.toml
├── BeamMP_Server_Index.exe ← OR serverIP.py
└── icon.ico (optional)


---

## 🚀 How to Use
1. Place the `.exe` in the server root directory where your BeamMP servers are.
2. Run it. It will:
   - Detect the IP
   - Scan all folders
   - Generate and open `servers.html`
  
   <h1>BeamMP Server List</h1>


## 📄 Example Output (servers.html)

<h2>moddedServers</h2>
<table>
<tr><th>Server Name</th><th>IP</th><th>Port</th><th>AuthKey</th></tr>
<tr><td>LagunaSeca</td><td>192.168.1.100</td><td>3320</td><td>abc123</td></tr>
<tr><td>EastCoast</td><td>192.168.1.100</td><td style="color:red">3320</td><td style="color:red">abc123</td></tr>
</table>

<h2>vanillaServers</h2>
<table>
<tr><th>Server Name</th><th>IP</th><th>Port</th><th>AuthKey</th></tr>
<tr><td>IndustrialMap</td><td>192.168.1.100</td><td>3333</td><td>xyz789</td></tr>
</table>
