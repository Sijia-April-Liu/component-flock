# 偏旁 · Component Flock

An interactive, generative animation in which the components of Chinese characters (偏旁部件) behave like a flock. Each piece follows a few simple local rules. Out of those rules come drifting crowds, scattering, ink trails, and complete Chinese characters that form and dissolve.

**Live demo:** `https://<your-username>.github.io/<repo-name>/`
**3D version:** `https://<your-username>.github.io/<repo-name>/hanzi-flock-3d.html`

## How to play

- Every floating piece is one **component** of a Chinese character.
- **Move your mouse** to scatter them. When the mouse leaves, they regroup on their own.
- **Click a component** in the top box. The box groups components by where they usually sit in a character: left, right, top, bottom, or enclosing. Every piece that can combine with the one you clicked is pulled toward its nearest copy. The first to arrive docks and forms a complete character, shown in red.
- You can select several components at once. **Click again to release**: the character splits back into its parts.
- **Hover over a red character** to see its pinyin and English meaning.
- Use **Parameters** to change the number of pieces, their size and speed, and how the ink merges, evaporates and spreads. **Erase · Reset** starts over.
- In the 3D version, **drag** to rotate the paper and **scroll** to zoom.

## The simple rules

Each component only knows what is near it:

1. **Drift**: it wanders slowly, at its own pace.
2. **Separation**: when it is too crowded, it steers away. The more crowded it is, the harder it pushes.
3. **Alignment**: it loosely follows its neighbours' direction. In a crowd, it peels off to the side that has more room.
4. **Mouse repulsion**: it flees the cursor. The closer the cursor, the stronger the push.
5. **Attraction**: when a matching component is selected, it heads for the empty seat next to the nearest free copy and joins it to form a character.
6. **Ink**: every movement leaves ink. The ink spreads (diffusion) and dries (evaporation). Pieces that come close merge like drops of ink, and separate again when they pull apart.

Nobody places the characters or plans the final image. What forms, where, and when emerges from these interactions.

## Built with

- [p5.js](https://p5js.org/) for the simulation loop
- WebGL shaders for the wet, glossy ink rendering
- Google Fonts: Noto Serif SC and Ma Shan Zheng

Each version is a single HTML file. Open `index.html` in a browser; an internet connection is needed to load p5.js and the fonts.

Made with Claude.
