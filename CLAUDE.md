# Mellow

Lokaler Desktop-Zeittracker für Aufgaben, Arbeitssessions und Markdown-Notizen.
**Tauri-2-App, kein Client-Server-Projekt.** Alle Daten bleiben auf dem Rechner —
keine Cloud, keine externe API. Diese Entscheidung ist bindend: nichts einbauen,
das einen Serverdienst oder einen API-Key braucht.

## Struktur

- `src/` — Frontend: Vue 3 + TypeScript, Vite
- `src-tauri/` — Rust-Seite: Tauri-Commands, Persistenz, OS-Integration

Es gibt **kein** `backend/` und **kein** `frontend/`. Claude Code lädt die
nächstgelegene `CLAUDE.md`; für Arbeit unter `src/` bzw. `src-tauri/` gelten die
dortigen Regeln.

- Frontend-Konventionen: @src/CLAUDE.md
- Rust-/Tauri-Konventionen: @src-tauri/CLAUDE.md

Berührt eine Änderung beide Seiten, gilt für jede Datei die Konvention ihres
eigenen Bereichs.

## Was hier nicht gilt

Dieses Repo hat **kein NestJS, kein TypeORM, keine DTOs, kein Swagger**. Regeln
aus dem `webdev-rules`-Template, die davon ausgehen, sind hier gegenstandslos.
Die Rust-Seite ersetzt das Backend.
