# Alfreds Zinsrechnung-Trainer 🔒

Passwortgeschützte Lern-Website für GitHub Pages.

## 📁 Dateien

| Datei | Beschreibung |
|-------|-------------|
| `index.html` | Login-Seite mit Passwortschutz |
| `trainer.html` | Dein Zinsrechnung-Trainer (hier deinen Code einfügen) |

---

## 🚀 Einrichtung (5 Minuten)

### Schritt 1: GitHub Repository erstellen

1. Gehe zu [github.com](https://github.com) und logge dich ein
2. Klicke auf **"New repository"** (grüner Button)
3. Name: `alfred-zinsrechnung` (oder beliebig)
4. Wähle **"Public"** (für kostenloses GitHub Pages)
5. Klicke **"Create repository"**

### Schritt 2: Dateien hochladen

1. Im neuen Repository klicke auf **"uploading an existing file"**
2. Ziehe beide Dateien (`index.html` und `trainer.html`) hinein
3. Klicke **"Commit changes"**

### Schritt 3: Deinen Trainer-Code einfügen

1. Klicke auf `trainer.html` im Repository
2. Klicke auf das **Stift-Symbol** (Edit)
3. Öffne deine `Zinsrechnung_Trainer_Alfred.html` lokal
4. Kopiere den gesamten Inhalt
5. **WICHTIG:** Behalte das Session-Check Script am Anfang! (die ersten ~20 Zeilen im `<script>` Tag)
6. Füge deinen Trainer-Code nach dem Kommentar ein
7. Klicke **"Commit changes"**

### Schritt 4: GitHub Pages aktivieren

1. Gehe zu **Settings** (Zahnrad oben rechts)
2. Linke Seite: Klicke auf **"Pages"**
3. Bei "Source": Wähle **"Deploy from a branch"**
4. Bei "Branch": Wähle **"main"** und **"/ (root)"**
5. Klicke **"Save"**
6. Warte 1-2 Minuten, dann erscheint oben die URL

---

## 🔑 Passwort ändern

**Standard-Passwort:** `admin`

### So änderst du das Passwort:

1. Gehe zu: https://emn178.github.io/online-tools/sha256.html
2. Gib dein gewünschtes Passwort ein (z.B. `MeinGeheimesPasswort123`)
3. Kopiere den Hash (die lange Zeichenkette)
4. Öffne `index.html` in GitHub zum Bearbeiten
5. Ersetze den Wert bei `CORRECT_PASSWORD_HASH` mit deinem neuen Hash
6. Speichere die Änderung

**Beispiele:**
| Passwort | SHA-256 Hash |
|----------|-------------|
| `admin` | `8c6976e5b5410415bde908bd4dee15dfb167a9c873fc4bb8a81f6f2ab448a918` |
| `alfred2024` | `a1b2c3...` (eigenen Hash generieren) |
| `Zinsrechnung` | `...` (eigenen Hash generieren) |

---

## 📱 Für Alfred

**Link:** `https://DEIN-USERNAME.github.io/alfred-zinsrechnung/`

**Passwort:** (das von dir gewählte Passwort)

Alfred muss sich nur einmal einloggen, dann bleibt er 7 Tage angemeldet (auch wenn er den Browser schließt).

---

## ⚙️ Einstellungen anpassen

### Session-Dauer ändern

In `index.html` findest du:
```javascript
const SESSION_DAYS = 7;
```
Ändere die Zahl für mehr oder weniger Tage.

### Abmelde-Button hinzufügen

Der Code für einen Logout-Button ist bereits in `trainer.html` enthalten. Du kannst ihn an beliebiger Stelle in deinem Trainer einfügen:

```html
<button onclick="logout()">Abmelden</button>

<script>
function logout() {
    localStorage.removeItem('alfred_mathe_session');
    window.location.href = 'index.html';
}
</script>
```

---

## ⚠️ Wichtige Hinweise

- **Sicherheit:** Der Passwortschutz ist client-seitig. Für sensible Daten nicht geeignet, aber für Lern-Apps völlig ausreichend.
- **Öffentlich:** Das Repository muss "Public" sein für kostenloses GitHub Pages.
- **Updates:** Einfach die Datei in GitHub bearbeiten und speichern - Änderungen sind in 1-2 Minuten live.

---

## 🆘 Probleme?

| Problem | Lösung |
|---------|--------|
| Seite lädt nicht | Warte 2-3 Minuten nach Aktivierung von GitHub Pages |
| 404 Fehler | Prüfe ob die Dateien im Root-Verzeichnis liegen |
| Passwort funktioniert nicht | Hash neu generieren und einfügen |
| Session funktioniert nicht | Browser-Cache leeren oder Inkognito-Modus testen |

---

Erstellt mit ❤️ für Alfreds Mathe-Training
