# SWAT Raiders

Single-file browser game. `index.html` is the whole thing — no build step, no
dependencies, nothing to install. PeerJS is vendored inside it.

## Publishing this on GitHub Pages

From this folder:

    git init
    git add .
    git commit -m "SWAT Raiders"
    git branch -M main
    git remote add origin https://github.com/<you>/swat-raiders.git
    git push -u origin main

Then on GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save.**

A minute later the game is live at `https://<you>.github.io/swat-raiders/`.

## Why hosting it here fixes co-op

Co-op needs to introduce the two players to each other. The five-character code
does that through PeerJS's matchmaking server. A normal web host — GitHub Pages
included — allows that connection, so **the code path works and co-op is one
step: your friend types the code.**

The claude.ai artifact sandbox blocks that connection, which is why the game
falls back to "No internet — only same-computer play is available" there. The
direct-link path (two pasted codes, no server) exists for that case.
