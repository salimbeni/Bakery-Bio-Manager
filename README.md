# Bakery-Bio-Manager
Ein modernes, hybrides System für Bäckereien, spezialisiert auf Bio-Zertifizierung, Rückverfolgbarkeit und Inventur.

# 🥐 alesite BioLog - Bio-Bäckerei Manager

Entwickelt mit **Python** und **Streamlit**.

![Status](https://img.shields.io/badge/Status-Active-success)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Database](https://img.shields.io/badge/DB-SQLite%20%7C%20MySQL-orange)

## 🚀 Highlights & Architektur

Dieses Projekt nutzt einen **Smart-Client Ansatz**:
* **⚡ Lokal zuerst (Offline-First):** Die tägliche Arbeit passiert auf einer lokalen SQLite-Datenbank. Das garantiert maximale Geschwindigkeit und Unabhängigkeit vom Internet.
* **☁️ Cloud Sync (Backup):** Alle 5 Minuten (oder beim Start) synchronisiert sich die App automatisch mit einer zentralen MySQL-Datenbank.
* **🔄 Auto-Update:** Beim Start zieht sich der Client automatisch den neuesten Code von GitHub, ohne die lokalen Daten zu überschreiben.

### Funktionen
* **📦 Lagerverwaltung:** Bestände, Chargen und Lieferanten.
* **📄 Lieferschein-Scanner:** Automatische PDF-Auslesung von Lieferscheinen.
* **🍰 Rezeptur-Management:** Zutaten verknüpfen und Rohstoffmengen berechnen.
* **🔍 Rückvergbarkeit (Traceability):** Lückenlose Dokumentation vom Mehl-Sack bis zum verkauften Brot.
* **⚙️ White-Labeling:** Jede Bäckerei kann ihr eigenes Logo und Namen hinterlegen.

---

## 🛠️ Installation (Für Anwender)

### Voraussetzung
* Ein Computer mit Windows oder macOS.
* Internetverbindung (für Installation und Sync).

### Schritt 1: Herunterladen
1.  Lade dieses Repository herunter (Code -> Download ZIP) oder nutze `git clone`.
2.  Entpacke den Ordner an einen Ort deiner Wahl (z.B. Desktop).

### Schritt 2: Einrichten (Mac)
1.  Öffne den Ordner.
2.  Doppelklicke auf **`Starten.command`**.
    * *Hinweis:* Beim ersten Mal musst du evtl. `Rechtsklick -> Öffnen` wählen oder im Terminal `chmod +x Starten.command` eingeben.
3.  Das Skript installiert alle nötigen Pakete automatisch.

### Schritt 3: Konfiguration
Nach dem ersten Start erstellt das Programm eine Datei `bakery_config.json`.
Gehe in der App auf **⚙️ Einstellungen**, um:
1.  Den Namen deiner Bäckerei einzugeben.
2.  Dein Logo hochzuladen.
3.  Die Cloud-Datenbank (MySQL) zu verbinden (optional).

---

## 💻 Entwicklung (Für Programmierer)

### Setup
```bash
# Repo klonen
git clone [https://github.com/DEIN_USER/dreipunkt-biolog.git](https://github.com/DEIN_USER/dreipunkt-biolog.git)
cd dreipunkt-biolog

# Virtuelle Umgebung (optional aber empfohlen)
python -m venv venv
source venv/bin/activate  # Mac/Linux
# .\venv\Scripts\activate # Windows

# Abhängigkeiten installieren
pip install -r requirements.txt

Starten

Bash
streamlit run app.py
Projektstruktur

app.py: Haupt-Einstiegspunkt der App.

utils.py: Enthält die gesamte Logik (Datenbank, Sync, PDF-Parser).

pages/: Die einzelnen Menüpunkte (Lager, Rezepte, Einstellungen).

Starten.command: Das Start-Skript für Endanwender (Mac).

🔒 Datenschutz & Sicherheit
Dieses Repository enthält keine echten Daten.

Die Datenbank lokal_daten.db wird lokal bei jedem Nutzer neu generiert.

Passwörter und Zugangsdaten gehören in die secrets.toml (wird nicht hochgeladen) oder in die bakery_config.json (wird lokal gespeichert).

📄 Lizenz
Open Source - Nutzung und Anpassung erlaubt. Copyright © 2026 alesite.ch


-----------------



# 🥐 alesite BioLog - Organic Bakery Manager

A modern, hybrid management system for bakeries, specialized in organic certification (Bio), traceability, and inventory management.

Built with **Python** and **Streamlit**.

![Status](https://img.shields.io/badge/Status-Active-success)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Database](https://img.shields.io/badge/DB-SQLite%20%7C%20MySQL-orange)

## 🚀 Highlights & Architecture

This project utilizes a **Smart-Client Approach**:
* **⚡ Local First (Offline-First):** Daily operations are performed on a local SQLite database. This guarantees maximum speed and independence from internet connectivity.
* **☁️ Cloud Sync (Backup):** Every 5 minutes (or upon startup), the app automatically synchronizes with a central MySQL database in the background.
* **🔄 Auto-Update:** Upon startup, the client automatically pulls the latest code from GitHub without overwriting your local data or configurations.

### Key Features
* **📦 Inventory Management:** Manage stock levels, batches, and suppliers.
* **📄 Delivery Note Scanner:** Automatic PDF extraction and parsing of delivery notes.
* **🍰 Recipe Management:** Link ingredients to recipes and calculate raw material quantities.
* **🔍 Traceability:** Seamless documentation from the flour sack to the sold bread.
* **⚙️ White-Labeling:** Each bakery can upload its own logo and set its own business name.

---

## 🛠️ Installation (For Users)

### Prerequisites
* A computer running macOS or Windows.
* Internet connection (required for installation and synchronization).

### Step 1: Download
1.  Download this repository (Code -> Download ZIP) or use `git clone`.
2.  Unzip the folder to a location of your choice (e.g., Desktop).

### Step 2: Setup (Mac)
1.  Open the folder.
2.  Double-click on **`Starten.command`**.
    * *Note:* On the first run, you might need to right-click and select `Open`, or run `chmod +x Starten.command` in your terminal if permission is denied.
3.  The script will automatically install all necessary Python packages.

### Step 3: Configuration
After the first launch, the program creates a `bakery_config.json` file locally.
Navigate to **⚙️ Settings** in the app menu to:
1.  Enter your bakery's name.
2.  Upload your custom logo.
3.  Connect your Cloud Database (MySQL) for backups (optional).

---

## 💻 Development (For Developers)

### Setup
```bash
# Clone repository
git clone [https://github.com/YOUR_USER/dreipunkt-biolog.git](https://github.com/YOUR_USER/dreipunkt-biolog.git)
cd dreipunkt-biolog

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # Mac/Linux
# .\venv\Scripts\activate # Windows

# Install dependencies
pip install -r requirements.txt

Run

Bash
streamlit run app.py
Project Structure

app.py: Main entry point of the application.

utils.py: Contains core logic (Database connection, Sync, PDF Parser).

pages/: Individual application pages (Inventory, Recipes, Settings).

Starten.command: Startup script for end-users (Mac).

🔒 Privacy & Security
This repository contains no real data.

The database lokal_daten.db is generated locally and empty for every new user.

Passwords and credentials belong in secrets.toml (not uploaded) or the local bakery_config.json (stored locally).

📄 License
Open Source. Copyright © 2026 alesite.ch
