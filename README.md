# Chum Storm

## Run the game

### VS Code
1. Open this folder in VS Code.
2. Install the **Live Server** extension if needed.
3. Right-click `index.html` and choose **Open with Live Server**.

### GitHub Pages
The project now includes the required root `index.html`. Publish the repository root from the `main` branch in GitHub Pages settings.

### Direct browser opening
You can double-click `index.html`, although Live Server is recommended for consistent asset loading.

## Controls
- Move: WASD or arrow keys
- Mobile: touch and drag
- Feeding skills fire automatically

## Important files
- `index.html` — default game entry point
- `chum-storm.html` — matching standalone copy
- `assets/` — player, cat, fish, and grass PNGs

## Player sprite update
The player now uses the supplied buff fisherman artwork as an 8-direction set. The two supplied rotation groups are alternated as a lightweight two-frame walk cycle. Movement and auto-aim both update the facing sprite.

## Fisherman sprite cropping fix
The 8-direction fisherman frames are tightly cropped to their non-transparent pixel bounds. Player rendering now preserves the cropped frame aspect ratio at a consistent visible height, so transparent export canvas padding no longer makes the character appear undersized. The feet remain anchored to the same collision/shadow position.
