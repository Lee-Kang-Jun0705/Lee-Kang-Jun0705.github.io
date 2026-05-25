# Asset Manifest

## Runtime Asset Policy
- Runtime visuals must resolve to PNG sprite, icon, field, and effect files.
- SVG prototype assets were removed from runtime paths to avoid visual drift.
- `motion-hq/final/*.png` owns actor sprites and 4x8 frame animation.
- `image2/**/*.png` owns field, icon, and effect presentation.
- `audio/*.wav`: local combat, loot, operation, portal, skill, and UI effects.
- `music/*.mp3`: user-provided BGM tracks copied with browser-safe filenames.

## Legacy Motion Sprite Sheets
- `motion/hero.png`: 4x4 player sheet, 128px frames, idle/walk/attack/skill rows.
- `motion/merc-*.png`: guard and mage companion sheets using the same row contract.
- `motion/monster-*.png`: imp, brute, and shaman sheets for varied monster packs.
- `motion/npc-*.png`: merchant, smith, and guild NPC sheets for town population.
- These files are retained as old prototypes; runtime uses `motion-hq/final`.

## High Quality Motion Sprite Sheets
- `motion-hq/raw/*-source.png`: built-in image2 source sheets on chroma-key green.
- `motion-hq/raw/*-alpha.png`: locally de-keyed transparent source sheets.
- `motion-hq/final/*.png`: normalized 512x1024 4x8 runtime sheets, 128px per frame.
- Runtime now prefers `motion-hq/final` over the previous simple motion sheets.
- Actor variety is now 88 runtime sheets: 3 hero, 3 mercenary, 66 monster, 10 boss, and 6 NPC variants.
- Standard actors keep idle/walk/run/attack1~3/dodge/spell rows.
- Boss sheets use the same contract at larger render scale.
- `attack.wav`, `hit.wav`, and `hurt.wav` were regenerated with softer tones and longer playback throttles.

## Image2 Runtime Assets
- `image2/fields/*.png`: 10 generated field backgrounds.
- `image2/turnarounds/*.png`: 4-direction green chroma reference sheets.
- `image2/motion-chroma/*.png`: 4x8 green chroma motion source sheets.
- `image2/sprites/*-sheet.png`: 16-frame sheets, 128x128 frames.
- `image2/icons/*.png`: generated item and building icons.
- `image2/fx/*.png`: generated portal, skill, and hit effects.
- `image2/fx/death-smoke.png`: 4-frame smoke sheet tinted/scaled per player, mercenary, monster, and boss.
- Keep raw built-in image2 atlases in `image2/raw/` for traceability.

## BGM Assignment
- `hearth.mp3`: early village-adjacent fields, calm exploration.
- `starlight.mp3`: mid exploration fields with lighter adventure tone.
- `fallen-sky-duel.mp3`: chapel/pass combat fields.
- `dragon-threshold.mp3`: siege and watch fields.
- `starfire-maw.mp3`: royal bastion and final gate fields.
