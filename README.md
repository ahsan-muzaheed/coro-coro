# Coro Coro

A 2D platformer built in Godot 4, with an infinite procedurally generated side-scrolling level.

**Play it here:** https://ahsan-muzaheed.github.io/coro-coro/

## Controls

| Action | Key |
|---|---|
| Move | A / D or Left / Right arrows |
| Jump | Space |

## About

Coro Coro follows an explorer who stumbles into a buried subterranean city.
The floor is generated on the fly as you run: terrain height steps up and down,
gaps open that have to be jumped, and floating platforms appear overhead.
Columns behind the player are discarded as new ones are built ahead, so the
level is endless without memory growing.

Fall off the bottom of the screen and you respawn further back along the track.

## This repository

Pre-built HTML5 export, served directly by GitHub Pages:

- `index.html` – page shell and loader
- `index.js` / `index.wasm` – Godot 4 web runtime (Compatibility renderer)
- `index.pck` – packed game data
- `index.audio.worklet.js`, `index.audio.position.worklet.js` – audio worklets

Source project lives at
https://github.com/ahsan-muzaheed/dgd-game-jam-1-group-4

## Running it locally

Opening `index.html` straight from disk will not work — browsers block
`file://` requests for the `.wasm` and `.pck`. Serve the folder over HTTP:

```
python -m http.server 8000
```

Then open http://localhost:8000
