# My Room in 3D

An interactive WebGL room rendered in the browser with [Three.js](https://threejs.org/). The scene uses fully baked lighting exported from Blender, a runtime shader that blends day/night/neutral lightmaps and re-tints the TV, desk and PC accent lights live, plus a set of small animated props: a DVD-style bouncing logo, coffee steam, an ambient LED mask, animated Loupedeck buttons, a Tilting chair and screen videos.

Originally created by [Bruno Simon](https://bruno-simon.com) as a Three.js Journey project. This copy is a personal showcase build.

## Tech

- **Three.js** — scene, camera, renderer, `VideoTexture`
- **Custom GLSL shaders** — baked-lightmap blending (`src/Experience/shaders/baked`)
- **glsl-blend / glslify** — shader partials (Perlin noise, blend modes)
- **GSAP** — animation
- **Tweakpane** — live debug panel
- **Webpack 5** + Babel — build tooling

## Structure

```
src/
  Experience/        # scene, renderer, camera, world
    Baked.js         # room material + baked lightmaps
    BouncingLogo.js  # DVD-style screensaver
    Screen.js        # video screens
    shaders/         # GLSL (baked, coffeeSteam, partials)
    Utils/           # helpers (loader, sizes, time, stats)
  index.html
  script.js
static/assets/       # models, textures, videos
bundler/             # webpack configs
```

## Setup

Download [Node.js](https://nodejs.org/en/download/) and run:

```bash
# Install dependencies (only the first time)
npm install

# Run the local server at localhost:8080
npm run dev

# Build for production in the dist/ directory
npm run build
```

## Credits

Original project and assets by **Bruno Simon** — [my-room-in-3d](https://github.com/brunosimon/my-room-in-3d).
