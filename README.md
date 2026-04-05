# Milas Abenteuer

Eine interaktive Geschichte zum Entdecken — wohin wird Mila gehen?

> **[🌐 Landing Page](https://open-learn.app/workshop-milas-abenteuer/)** · **[➕ Add to Open Learn](https://open-learn.app/#/add?source=https://open-learn.app/workshop-milas-abenteuer/index.yaml&lang=deutsch)**

## 3 Lessons

1. **Der geheimnisvolle Wald** — Mila entdeckt einen Wald und muss sich entscheiden
2. **Am Fluss** — Mila folgt dem Geräusch zum Fluss und trifft einen besonderen Freund
3. **Das alte Haus** — Mila entdeckt ein geheimnisvolles Haus voller Geschichten

## Features

- Interaktive Story mit Entscheidungen (wohin soll Mila gehen?)
- Verschiedene Stimmen: Erzähler, Oma, Fridolin der Frosch
- Audio generiert mit Edge TTS (Neural Voices)
- Story Mode mit Bildern und Animationen
- Hilfe-Button für kleine Kinder (ab 3 Jahre)

## Voice Mapping

| Rolle | Charakter | Stimme |
|-------|-----------|--------|
| `narrator` | Erzähler | de-DE-KillianNeural |
| `grandma` | Oma | de-DE-KatjaNeural |
| `fridolin` | Frosch Fridolin | de-DE-ConradNeural |
| default | Titel, Fragen | de-DE-AmalaNeural |

## Audio generieren

```bash
bash generate-audio.sh deutsch/milas-abenteuer
```

Benötigt: `uv` (für `uvx edge-tts`) und `yq` (`brew install yq`).

## Links

- [Open Learn Platform](https://open-learn.app)
- [Open Learn GitHub](https://github.com/openlearnapp)
