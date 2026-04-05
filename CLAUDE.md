# Milas Abenteuer

## Purpose

Interactive branching story for young children (age 3+). Teaches German reading/listening comprehension through a guided adventure where Mila explores a forest, meets a frog, and discovers an old house full of stories.

Goals:
- Listening comprehension via story narration
- Simple decision-making via interactive assessments
- Positive first experience with interactive learning content
- Works for children who can't yet read or write (audio + help button)

## Target Audience

- **Age**: 3–8 years
- **Language**: Native or learning German
- **Prior knowledge**: None — the story is the content
- **Reading skill**: Not required (audio-first, visual options)

## Structure

- **3 lessons** forming a branching story (~10–15 min total)
- **Language**: Deutsch only (currently)
- **Special features**:
  - Story mode (full-screen, audio-driven)
  - Branching assessments with `goto` navigation
  - Character voices (narrator, grandma Oma, Fridolin the frog)
  - Custom SVG illustrations per scene
  - Help button for kids who can't answer (ages 3+)

### Lessons

1. **Der geheimnisvolle Wald** — Mila hört ein Geräusch im Wald und muss sich entscheiden: Zum Fluss oder zum alten Haus?
2. **Am Fluss** — Mila trifft Fridolin den Frosch und muss ein kleines Rätsel lösen
3. **Das alte Haus** — Mila entdeckt die alte Frau mit dem magischen Buch

## Voice Mapping

Audio is generated with Microsoft Edge TTS (Neural voices) via `generate-audio.sh`.

| Role | Character | Voice |
|------|-----------|-------|
| `narrator` | Erzähler | `de-DE-KillianNeural` (male, calm) |
| `grandma` | Die alte Frau | `de-DE-KatjaNeural` (female, warm) |
| `fridolin` | Fridolin der Frosch | `de-DE-ConradNeural` (male, different) |
| default | Titles, questions | `de-DE-AmalaNeural` (female, friendly) |

Set per example in `content.yaml`:

```yaml
examples:
  - q: "Komm herein, mein Kind."
    voice: grandma
```

## Conventions

- **All text in German** (Interface-Sprache: Deutsch)
- **Images**: one SVG per scene in `lesson/images/`
- **Branching**: every assessment has `goto_correct` and `goto_wrong` (or per-option `goto`)
- **No written answers required** — all assessments are select/multiple-choice with images
- **Help button**: assessments should have a clear "correct" path so the help button can advance the story
- **Lessons are self-contained**: no cross-lesson vocabulary tracking (this is a story, not a language course)

## Development

```bash
# Generate audio (requires uv and yq)
bash generate-audio.sh deutsch/milas-abenteuer

# Local preview in Open Learn platform
# 1. Clone platform: git clone git@github.com:openlearnapp/openlearnapp.github.io.git
# 2. Place this repo as sibling: ../workshop-milas-abenteuer
# 3. cd openlearnapp.github.io && pnpm dev
# 4. The workshop is auto-detected and shown with 🔧 local-dev label
```

## See Also

- [Open Learn Platform](https://github.com/openlearnapp/openlearnapp.github.io)
- [Workshop Guide](https://github.com/openlearnapp/openlearnapp.github.io/blob/main/docs/workshop-guide.md) — how to create workshops
- [Lesson Schema](https://github.com/openlearnapp/openlearnapp.github.io/blob/main/docs/lesson-schema.md) — content.yaml fields reference
- [YAML Schemas](https://github.com/openlearnapp/openlearnapp.github.io/blob/main/docs/yaml-schemas.md) — index.yaml, workshops.yaml, lessons.yaml
- [Audio System](https://github.com/openlearnapp/openlearnapp.github.io/blob/main/docs/audio-system.md) — audio generation and playback
- [Workshop Creator Plugin](https://github.com/openlearnapp/plugin-workshop-creator) — Claude Code plugin for generating workshops
