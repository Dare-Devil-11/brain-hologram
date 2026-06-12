# AI-OS Brain Hologram

> A Three.js neural cortex — 240 neurons, WebGL signal pulses, built with empathy, compassion, and vigor.

**Live:** https://dare-devil-11.github.io/brain-hologram/

---

## What This Is

A real-time 3D visualization of an AI operating system's neural activity. 240 nodes connected by live signal pulses — built with Three.js, WebGL shader materials, and a force-directed spatial layout.

No dependencies to install. No build step. Open and it runs.

Built as part of the AI-OS project: one person building tools that make AI genuinely useful for organizations that can't afford enterprise software.

---

## Why It's Open Source

Because the best tools don't stay locked. Because visualization techniques should be shareable. Because someone else might use this as the base for something even more useful.

Use it. Fork it. Adapt it. If you build something with it that helps people, that's the point.

---

## Principles

**Empathy.** Built to communicate clearly — not to impress engineers, but to help non-technical people understand how an AI system thinks.

**Compassion.** This visualization is one part of a system designed to serve an elder care nonprofit. The people on the other end of these tools are families in hard circumstances. Every layer of this project is built with that in mind.

**Vigor.** Ships as a single HTML file. No framework overhead. No setup friction. It works the first time you open it.

**Faith as guardrail.** This system will not be adapted to surveil, manipulate, or exploit. The aesthetic power of a neural visualization should never be used to make deception look impressive. That line doesn't move.

---

## Stack

- **Three.js r158** — WebGL renderer, shader materials
- **OrbitControls** — drag/zoom/pan
- **Custom GLSL** — pulsing signal shader, glow effect
- **D3-force-3D** — spatial node layout
- **Vanilla JS** — no framework overhead

---

## Run It

```bash
# No build step needed
open index.html

# Or serve it
python3 -m http.server 8080
# → http://localhost:8080
```

---

## Customize It

The neuron data is embedded in the JS at the bottom of `index.html`. Find the `NODES` array and replace with your own structure:

```javascript
const NODES = [
  { id: 'core', label: 'Core System', color: '#6366f1', size: 8 },
  { id: 'memory', label: 'Memory', color: '#10b981', size: 5 },
  // ...
]

const EDGES = [
  { source: 'core', target: 'memory', strength: 0.8 },
  // ...
]
```

Colors, pulse speed, and glow intensity are all controlled by CSS variables at the top of the script block.

---

## License

MIT — free forever. Attribution appreciated, not required.

---

## The Bigger Picture

This hologram is the visual layer of a larger AI-OS project. The system it represents:

- Serves UMAS, an elder care nonprofit in Chicagoland
- Helps one-person teams do the work of five
- Is being built to be deployed for any organization doing good work

The goal isn't to build the flashiest AI demo. The goal is dignity — for the people being served and for the people doing the work.

> *"Do justice, love mercy, walk humbly."*
