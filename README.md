# NEIZVESNY Menu

Experimental Mindustry menu-logo replacement project for iPhone.

## Goal
Replace only the original `MINDUSTRY` logo with a Dungeon Synth styled `NEIZVESNY` logo. Leave menu buttons, background, and the game's automatically rendered build label unchanged.

## Technical investigation
Mindustry's `MenuFragment.build` draws the menu logo using `Core.atlas.find("logo")`, and renders the version label separately. Mindustry's `Mods` sprite packer processes PNG images in `sprites-override/` without adding a mod prefix. Thus the candidate override path is **`sprites-override/logo.png`**. A previous attempt at this path did not visibly work on iOS; its exact PNG contents and loading diagnostics have not yet been verified.

## Next steps
1. Upload the approved transparent logo PNG as `sprites-override/logo.png` (not `sprites-override/ui/logo.png`).
2. Check the PNG dimensions and alpha channel.
3. Import from GitHub into Mindustry and restart fully.
4. If unchanged, inspect startup logs / atlas behavior before attempting another fix.

**Status:** project scaffold only; no verified working iOS logo replacement yet.
