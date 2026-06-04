# The Lazy Dungeon Master's Tome

Session prep tool following Sly Flourish's *Return of the Lazy Dungeon Master* — all eight steps, initiative tracker, character sheet viewer, and session archive.

## GitHub Pages Setup

1. Upload all files to a GitHub repo keeping the folder structure
2. **Settings → Pages → Source: main branch / root**
3. Live at `https://yourusername.github.io/repo-name/`

## Folder Structure

```
/
├── index.html                        ← Main app
├── README.md
├── characters/
│   ├── stuart-warryn.json            ← Warryn's sheet
│   ├── example-character.json        ← Template
│   └── example-character2.json
└── sessions/                         ← Export sessions here
    └── session-01-campaign.json
```

## Loading Character Sheets

**Two ways to load a character sheet:**

### 1. From GitHub (JSON)
- Put the character JSON in `/characters/` folder
- Click **Raw** on GitHub to get the direct URL
- Paste into the loader in the **① Characters** tab

### 2. Paste directly (any format)
- Click **Paste / Type Character Sheet**
- Paste YAML-style stat blocks (like the ones in your campaign notes), plain text, or JSON
- The parser will extract name, stats, HP, AC, features, spells, backstory, and more

### Character JSON format
See `characters/stuart-warryn.json` for a full example. Key fields:

| Field | Description |
|-------|-------------|
| `name`, `player` | Character and player names |
| `race`, `class`, `level` | Core info |
| `stats` | Array: [STR, DEX, CON, INT, WIS, CHA] |
| `hp_max`, `ac`, `speed` | Combat stats |
| `goals` | Array of character goals |
| `backstory` | Full backstory text |
| `class_features`, `traits`, `spellcasting`, `actions` | Feature blocks |
| `equipment`, `spells`, `skills`, `languages` | Tag lists |

## Initiative Tracker

- **Add combatants** manually or click **Import PCs from Sheets** to pull in loaded characters
- **Roll All Initiative** auto-rolls d20 + DEX mod for everyone
- **Next Turn** advances the active combatant, auto-increments round
- **Quick Damage/Heal** — select a target and apply in one click
- **Add Condition** — all standard 5e conditions with click-to-remove pips

## Session Archive

Export sessions as JSON after each game, upload to the `sessions/` folder on GitHub. Load them back in the **📚 History** tab or drag-and-drop the JSON file directly. Sessions expand to show strong start, what happened, loose threads, and next prep notes.

## Attribution

Built on the eight-step framework from *Return of the Lazy Dungeon Master* by Michael E. Shea (Sly Flourish). Non-commercial personal use.
