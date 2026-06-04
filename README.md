# The Lazy Dungeon Master's Tome

A session prep tool following Sly Flourish's *Return of the Lazy Dungeon Master* eight-step framework.

## Setup on GitHub Pages

1. Fork or upload this repo to GitHub
2. Go to **Settings → Pages → Source: main branch / root folder**
3. Your tool will be live at `https://yourusername.github.io/repo-name/`

## File Structure

```
/
├── index.html                  ← Main DM prep app
├── README.md
└── characters/
    ├── example-character.json  ← Template for player sheets
    └── example-character2.json ← Second example
```

## How to Load Player Character Sheets

1. Each player (or you) creates a JSON file in the `characters/` folder using the format in `example-character.json`
2. Push the file to GitHub
3. In the app's **① Characters** tab, click the **Raw** button on the file in GitHub to get a URL like:
   ```
   https://raw.githubusercontent.com/USERNAME/REPO/main/characters/playername.json
   ```
4. Paste that URL into the loader and click **Load Sheet**
5. The sheet will render inline with stats, traits, goals, and a session hook field

## Player Workflow

Players can update their own character sheet between sessions:
- Edit their JSON file on GitHub (or via a PR)
- The DM loads the updated sheet each session

## Character JSON Format

See `characters/example-character.json` for the full schema. Key fields:

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Character name |
| `player` | string | Player's name |
| `class` / `race` / `level` | string/number | Core info |
| `stats` | object | `{STR, DEX, CON, INT, WIS, CHA}` |
| `hp_max` / `hp_current` | number | Hit points |
| `goals` | array | What the character wants |
| `equipment` / `spells` / `features` | arrays | Lists |
| `personality` / `ideals` / `bonds` / `flaws` | string | Character traits |
| `notes` | string | DM-only notes |

## Attribution

Built on the eight-step framework from *Return of the Lazy Dungeon Master* by Michael E. Shea (Sly Flourish). For personal/non-commercial use.
