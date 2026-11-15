# Godot Scene Series

Short animations that show how to build each piece of a 2D game in Godot, one scene tree at a time.

## Put it on GitHub Pages (one time)

1. Create a new **public** repo, for example `godot-scene-series`.
2. Copy this whole folder into it (`index.html`, `episodes.json`, `README.md`, `videos/`), then commit and push to `main`.
3. In the repo, open **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick `main` and `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/godot-scene-series/`.
5. Open that link on a student Chromebook once, to make sure the district filter allows `github.io`.

## Add the videos

Export each animation as an MP4 (the **Export** button on its page) and save it in `videos/` with these exact names:

| Episode | File name |
|---|---|
| P1 Platformer player | `videos/p1-platformer-player.mp4` |
| P2 Top-down player | `videos/p2-topdown-player.mp4` |
| P3 Arcade dodger player | `videos/p3-arcade-dodger-player.mp4` |
| P4 Physics player | `videos/p4-physics-player.mp4` |
| P5 Which body should my player be? | `videos/p5-which-body.mp4` |
| K1 A coin that collects itself | `videos/k1-coin.mp4` |
| K2 Hearts and signals | `videos/k2-hearts-and-signals.mp4` |
| K3 Magnet pickups | `videos/k3-magnet.mp4` |
| E1 A patrolling slime | `videos/e1-patrolling-slime.mp4` |
| E2 Danger zones and hurtboxes | `videos/e2-danger-zones.mp4` |
| E3 Chase when close | `videos/e3-chase-when-close.mp4` |

Until a file is there, its card says "Video not uploaded yet."

## Add a new episode later

1. Put the MP4 in `videos/`.
2. In `episodes.json`, find the planned episode (for example `K1`), delete its `"planned": true` line, and add a `"video"` line, like this:
   `"video": "videos/k1-coin.mp4",`
3. Commit and push. The site updates by itself in about a minute.

A brand-new topic only needs one entry in `"topics"` and episodes with that topic's `id`. A new big idea goes in `"bigIdeas"`, and an episode points to it with `"bigIdea": "<its id>"`.

## Try it on your computer first (optional)

The page loads `episodes.json` with `fetch`, which browsers block for files opened straight from disk. Run a tiny local server in this folder instead:

```
python3 -m http.server
```

Then open http://localhost:8000.

## Downloads
Each topic tab has a Downloads area. The files live in `downloads/`:
- `godot-scene-series-starter.zip`: the Players starter project
- `godot-pickups-starter.zip`: the Pickups starter project
- `godot-enemies-starter.zip`: the Enemies starter project
- `godot-scene-series-art.zip`: the 16 x 16 art pack

When a starter changes, upload the new zip into `downloads/` with the same name.
To add a download to a topic, add an entry to that topic's `"downloads"` list in `episodes.json`.
The teacher solutions are not on the site, on purpose: anyone with the link could download them.
