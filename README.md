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
