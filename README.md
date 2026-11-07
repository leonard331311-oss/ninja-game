# Ninja Head Survival

A small, fast survival game that runs directly in your browser. Play as a ninja, throw shuriken at the approaching zombies, and see how long you can survive.

## Play

Open [the game on GitHub Pages](https://leonard331311-oss.github.io/ninja-game/) or open `index.html` in a modern browser. The game starts when you press **Space** or tap the arena.

### Controls

- **Computer:** Move with **W A S D** or the **arrow keys**. Click in the arena to throw a shuriken toward that point.
- **Touchscreen:** Drag the joystick in the lower-left corner to move. Tap **ATTACK** to throw a shuriken at the nearest zombie. You can also tap in the arena to aim and throw toward that point.

Avoid the zombies. They follow you, drain your health when they touch you, and arrive more frequently as time passes. Your run ends when your health reaches zero. The game reports how many zombies you defeated and how long you survived.

## Best score

Your personal best is the largest number of zombies you have defeated in one run. It is saved in this browser on this device using local storage, and is shown on the start screen the next time you play. It does not sync between browsers or devices. Clearing this site's browser data removes the saved score.

## Install on a phone or tablet

The game is a Progressive Web App and is served over HTTPS by GitHub Pages. After opening it once, you can install it from your browser:

- **iPhone/iPad:** In Safari, tap **Share**, then **Add to Home Screen**.
- **Android:** Open the browser menu and choose **Install app** or **Add to Home screen**.

After the first load, the game files are cached for offline play. Installing it adds a home screen shortcut that opens the game in an app-like window.

## Developer notes

This is a static project: the game, styles, and JavaScript are in `index.html`. GitHub Actions deploys the repository to GitHub Pages when changes are pushed to `main`.

- Set `APP_VERSION` near the top of the script in `index.html` for each release. It follows **MAJOR.MINOR.PATCH** (for example, `1.0.0` to `1.0.1` for a fix, `1.1.0` for a compatible feature, or `2.0.0` for a breaking change). The version is displayed on the start screen.
- `manifest.webmanifest` and `icon.svg` provide the installable app details and home screen artwork.
- `sw.js` caches the app shell and uses the network when available, with a cached page as an offline fallback.
- The high score key is `ninja-head-survival-high-score` in the browser's local storage.

## License

See [LICENSE](LICENSE).
