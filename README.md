# Rowbreak

A brick breaker that runs in the browser. No install and no build step. It is one `index.html` file.

## Play

Open `index.html` in any modern browser, or use the hosted version on GitHub Pages (steps below).

| Control | Action |
| --- | --- |
| `A` `D` or `←` `→` | Move the paddle |
| `Space` | Launch the ball, confirm |
| `P` or `Esc` | Pause (single player) |
| `M` | Level tree |
| Mouse, or drag on a touch screen | Move the paddle |

## What is in it

- Twenty-one levels in a branching unlock tree. Some levels only open once two branches are cleared (double ring), and five bonus levels sit on the branch tips and pay double coins.
- A clock on every level, with your best time saved per level.
- Power-ups: wide paddle, narrow paddle, slow ball, fast ball, extra life, and a very rare golden ball that throws off 50 more balls.
- Hardcore mode: one life, double ball speed, only bad power-ups (narrow paddle, fast ball) and twice as many of them. A death resets the whole tree back to level 1.
- A coin shop with backgrounds, balls, paddles and brick styles to unlock.
- Vs computer: a 1v1 against the computer on Easy, Medium or Hard.

Progress, coins and shop unlocks are saved in each player's own browser (local storage).

## Vs computer

Press **Vs computer** on the menu and pick Easy, Medium or Hard.

- Both sides get one arena with five rows of bricks each. Your bricks are green and the computer's are pink, and you always see yourself at the bottom. The computer's half is squashed into a strip at the top.
- Each side has one ball. Break your own bricks and the other side gets a block added, in the same column.
- Your ball bounces off your own bricks. Once you carve a gap through your own wall, your ball breaks straight through the other wall without bouncing.
- Drop your own ball and you lose a life. You have 3.
- If the computer's ball gets past your paddle, you lose straight away, and the same goes for the computer.
- Balls bounce off both paddles, so you can block a ball that comes at you. They also speed up the longer the match goes on.
- Easy is slow and misses a lot. Hard is fast and rarely makes a mistake.

## Put it on GitHub Pages

1. Create a new public repository on GitHub, for example `rowbreak`.
2. Add the files in this folder (`index.html`, `README.md` and a `LICENSE`) with **Add file → Upload files**, then commit.
3. Open the repository's **Settings**, then **Pages** in the left sidebar.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then save.
5. After a minute or two the page address shows at the top of the Pages settings:

```
https://<your-github-username>.github.io/<repository-name>/
```

Share that link and anyone can play. To update the game later, upload a new `index.html` to the same repository and Pages redeploys on its own.

## Notes

- The fonts (Silkscreen and IBM Plex Mono) load from Google Fonts. Offline, the game falls back to system monospace fonts and still works.
- Saves live in the browser, so clearing site data or switching browsers starts from scratch.
