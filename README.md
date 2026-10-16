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
- Hardcore mode: one life, no extra lives, and a death resets the whole tree back to level 1.
- A coin shop with backgrounds, balls and paddles to unlock.
- Online 1v1 against a friend, with a four character game code.

Progress, coins and shop unlocks are saved in each player's own browser (local storage).

## Online 1v1

Press **Online 1v1** on the menu. One player picks **Create game** and gets a four character code, plus a **Copy invite link** button. The other player picks **Join with code** and types it, or just opens the invite link.

The rules:

- Both players share one arena with five rows of bricks each. Your bricks are green and your opponent's are pink, and you always see yourself at the bottom. Your opponent's half is squashed into a strip at the top.
- Each player has one ball. Break your own bricks and your opponent gets a block added to their wall, in the same column.
- Your ball bounces off your own bricks. Once you carve a gap through your own wall, your ball breaks straight through your opponent's bricks without bouncing.
- Drop your own ball and you lose a life. You have 3.
- If your opponent's ball gets past your paddle, you lose straight away.
- Balls bounce off both paddles, so you can block a ball that comes at you. They also speed up the longer the match goes on.

How the connection works: the two browsers talk directly to each other (WebRTC, using [PeerJS](https://peerjs.com), which is bundled inside `index.html`). A free public PeerJS relay is used only for the first handshake, to turn the code into a connection. It is not part of this repository and nothing about the match goes through it. If that relay is down, online play shows an error and the rest of the game still works. A few strict networks (some mobile carriers and company Wi-Fi) can block direct connections.

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
- Online 1v1 needs both players on the same version of the game, so refresh the page after an update.
- PeerJS is MIT licensed. Copyright (c) 2013 Michelle Bu and Eric Zhang.
