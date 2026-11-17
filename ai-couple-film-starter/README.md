# AI Couple Stories — Production Repository

Reusable workflow: **ChatGPT (script + direction) → ChatGPT Images (characters + keyframes) → Google Veo (animation) → CapCut (edit)**.

## Quick start
1. Read `docs/production-workflow.md` and complete `docs/style-bible.md` and `docs/characters.md`.
2. Complete `episodes/ep001/brief.md`; create the script using `prompts/templates/01-script.md`.
3. Write a shot list in `episodes/ep001/shot-list.csv` (one row per shot).
4. Generate a **master character sheet**; select one approved image and preserve it unchanged.
5. Generate one keyframe per shot. Use the approved character images as references in every prompt.
6. Animate approved frames with Veo, usually one short clip per shot; save the exact prompt and tool settings for every attempt.
7. Edit in CapCut, export 9:16 video, run QA, and write lessons learned.

## Reproducibility rule
**Before each generation:** save its prompt in `episodes/ep001/prompts/` with a unique attempt number.
**After generation:** log tool, model/version as shown by the UI, timestamp, input asset filenames, aspect ratio, duration, settings, result filename, cost/credits, feedback, and approved/rejected decision in `episodes/ep001/metadata/generations.csv`.

A prompt alone cannot guarantee the identical output. Keep approved source images/frames and metadata. UI models may change, and generation can be stochastic.

## Git setup
```bash
git init
git add .
git commit -m "chore: initialize reusable AI filmmaking pipeline"
```
Use a **private** repository if you include photos of you and your wife or personal story details. Large renders are ignored by default; track those in private cloud storage or Git LFS. Do not commit API keys.

## Episode naming
`ep001_sh03_keyframe_v01.png`, `ep001_sh03_veo_v02.mp4`, `ep001_sh03_image_v01.md`, `ep001_sh03_video_v02.md`.

## Definition of done
See `docs/quality-checklist.md`.
