# Git & GitHub Workflow Anleitung

Diese Anleitung beschreibt die gängigsten Befehle für die Arbeit mit Projekten und wie du mich (Gemini CLI) am besten beauftragst.

## 1. Projekt neu anlegen (Lokal & GitHub)

**Was du mir sagen kannst:**
* "Erstelle ein neues Projekt 'MeinProjekt' lokal und auf GitHub."
* "Initialisiere ein Git-Repo für den aktuellen Ordner und lade es auf GitHub hoch."

**Manuelle Befehle:**
```bash
mkdir MeinProjekt && cd MeinProjekt
git init
gh repo create MeinProjekt --public --source=. --remote=origin --push
```

## 2. Änderungen übertragen (Commit & Push)

In Git nennt man eine "neue Revision" einen **Commit**. Um diese auf GitHub zu sichern, musst du sie **pushen**.

**Was du mir sagen kannst:**
* "Speichere meine Änderungen und pushe sie zu GitHub mit der Nachricht 'Feature X hinzugefügt'."
* "Erstelle eine neue Revision auf GitHub für das Projekt [Name]."

**Manuelle Befehle:**
```bash
git add .
git commit -m "Deine Beschreibung der Änderungen"
git push origin main
```

## 3. Lokal aktualisieren (Pull)

Wenn GitHub aktueller ist (z. B. nach Änderungen im Webbrowser), holst du den Stand mit **pull**.

**Was du mir sagen kannst:**
* "Aktualisiere mein lokales Projekt [Name] mit dem neuesten Stand von GitHub."
* "Hol die neuesten Änderungen von GitHub ab."

**Manuelle Befehle:**
```bash
git pull origin main
```

## 4. Projekt löschen (Lokal & GitHub)

**Was du mir sagen kannst:**
* "Lösche das Projekt [Name] und das zugehörige Repo auf GitHub." (Wie gerade geschehen).

**Manuelle Befehle:**
```bash
gh repo delete <Username>/<RepoName> --yes
rm -rf /Pfad/zum/Ordner
```

---

### Tipps für die Kommunikation mit mir:
- **Eindeutigkeit:** Nenne am besten den Projektnamen oder den Pfad.
- **Nachricht:** Wenn du einen Commit möchtest, sag mir kurz, was geändert wurde (z.B. "Update README"). Wenn du nichts sagst, verwende ich eine Standardnachricht wie "Update durch Gemini".
- **Authentifizierung:** Da ich Zugriff auf deinen Account habe, nutze ich im Hintergrund meist das `gh` Tool (GitHub CLI) oder Standard-Git-Befehle.
