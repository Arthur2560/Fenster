# Fenster-Haus-Karte

Seitenansicht des Hauses fürs Home-Assistant-Dashboard. Jeder Raum wird rot (pulsierend), sobald eine der ihm zugeordneten Entitäten offen ist (`on` oder `open`). Kein Helfer nötig: pro Raum werden im visuellen Editor beliebig viele Entitäten gewählt (z. B. bis zu 3 Fensterkontakte). Tippen auf einen Raum öffnet die More-Info-Ansicht des offenen Fensters.

Das Dachgeschoss ist geteilt: **rechts = Erker**, **links = Dachfenster**. Darüber liegt die **Spitze (Gaube)**.

## Installation (HACS)
1. HACS → Dashboard → ⋮ → Benutzerdefinierte Repositories → Repository-URL, Typ **Dashboard**.
2. Installieren, Browser neu laden.
3. Dashboard bearbeiten → Karte hinzufügen → **Fenster-Haus**.

## YAML
```yaml
type: custom:fenster-haus-card
title: Fenster        # optional
zones:
  spitze: [binary_sensor.fenster_gaube]
  dach_links: [binary_sensor.dachfenster_1, binary_sensor.dachfenster_2]
  dach_rechts: [binary_sensor.erker_links, binary_sensor.erker_rechts]
  oben_bad: [binary_sensor.fenster_bad_oben]
```
Zonen: `spitze, dach_links, dach_rechts, oben_links, oben_bad, oben_arthur, mitte_flur, mitte_arthur, mitte_bett, mitte_bad, unten_flur, unten_bad, unten_links`
