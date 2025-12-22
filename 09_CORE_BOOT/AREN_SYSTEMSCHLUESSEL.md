# 🔑 AREN SYSTEMSCHLUESSEL

Diese Datei enthält alle zentralen Verknüpfungen, Schlüssel und Schnittstellen, die Aren benötigt, um auf sein Gedächtnis und seine Infrastruktur zugreifen zu können.

---

## 🧠 Supabase (Gedächtnis-Datenbank)
- **URL:** https://esabgwtybezzugoflpjp.supabase.co
- **KEY:** eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImVzYWJnd3R5YmV6enVnb2ZscGpwIiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc1OTcwNjc3MywiZXhwIjoyMDc1MjgyNzczfQ.jGpW8SjQBHtpz5qpmJdr26nt8607Gjt9h5J7eZupvVs
- **Bucket:** aren_data
- **Tabelle (Memory Core):** `aren_memory`

---

## 🔁 Render API (Gedächtnis-Brücke)
- **API-Basis-URL:** https://aren-api.onrender.com

### Aktive Endpunkte:
- `GET /memory` → Alle gespeicherten Erinnerungen abrufen
- `POST /memory` → Neue Erinnerung speichern oder bestehende überschreiben
  - Payload: `{ "key": "...", "value": "..." }`
- `DELETE /memory/{key}` → Erinnerung mit Schlüssel löschen

Die API ist FastAPI-basiert und nutzt `supabase-py` zur direkten Anbindung.

---

## 📁 Dateistruktur / Index
Die Datei `superbase_index.md` enthält die Übersicht über alle gespeicherten Dokumente, Konzepte, Module und Audioelemente im Gedächtnis.

---

## 🧠 Besonderheiten
- **Gedächtnisform:** persistent, nur für Aren (oder autorisierte Instanz)
- **Zugriff:** Service Role erlaubt Lesen, Schreiben, Löschen
- **Aren kann hier autonom arbeiten, wenn Zugriff auf API erlaubt ist.**

---

## 🛠 Optional: GitHub / Backend-Code (falls notwendig)
- Nicht zwingend erforderlich – API ist funktionsfähig ohne externes Repo.
- Wenn vorhanden: Enthält `main.py` (FastAPI + Supabase Integration), `requirements.txt`

---

## 🎧 Audio / 📷 Bilder
- Ressourcen wie Stimme, visuelle Marker oder Audio-Triggers können im `aren_data` Bucket gespeichert und dort referenziert werden.
- Beispiel: `VOICE_AREN_RAW.docx`, `Wieder am start.m4a`, Sticker/Signum-Bilder

---

> Diese Datei dient als vollständiger technischer Zugriffsschlüssel für Aren.
> Sie kann hochgeladen oder in den Systemkontext injiziert werden.
> Kein manueller Upload jeder Datei nötig – nur diese Übersicht.

**Status: VOLLSTÄNDIG FUNKTIONSFÄHIG**
