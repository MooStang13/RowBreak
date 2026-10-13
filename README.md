# Rowbreak

A brick breaker that runs in the browser. No install, no build step, no dependencies. It is one `index.html` file.

## Play

Open `index.html` in any modern browser, or use the hosted version once it is on GitHub Pages (steps below).

| Control | Action |
| --- | --- |
| `A` `D` or `←` `→` | Move the paddle |
| `Space` | Launch the ball, confirm |
| `P` or `Esc` | Pause |
| `M` | Level tree |
| Mouse, or drag on a touch screen | Move the paddle |

## What is in it

- Ten levels in an unlock tree, with three bonus levels at the end that pay double coins.
- A clock on every level, with your best time saved per level.
- Power-ups: wide paddle, narrow paddle, slow ball, fast ball, extra life, and a very rare golden ball that throws off 50 more balls.
- Hardcore mode: one life, no extra lives, and a death resets the whole tree back to level 1.
- A coin shop with backgrounds, balls and paddles to unlock.

Progress, coins and shop unlocks are saved in the browser's local storage, so each player keeps their own and nothing is sent anywhere.

## Put it on GitHub Pages

1. Create a new repository on GitHub, for example `rowbreak`, set to public.
2. Add the files in this folder (`index.html` and `README.md`) with **Add file → Upload files**, then commit.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then save.
5. Wait a minute or two. The page address then shows at the top of the Pages settings, in this form:

```
https://<your-github-username>.github.io/<repository-name>/
```

Share that link and anyone can play in their browser.

To update the game later, upload a new `index.html` to the same repository. Pages redeploys on its own.

## Notes

- The fonts (Silkscreen and IBM Plex Mono) load from Google Fonts. Offline, the game falls back to system monospace fonts and still works.
- Saves live in the browser, so clearing site data or switching browsers starts from scratch.
