# DRT Orbital Solver — Supernova 3D

> This is an amateur engineering project. We are not HPC professionals and make no competitive claims. Errors likely.

A 3D browser demo that runs a three-step solver on a small problem, framed in orbital / celestial-mechanics language. Observers sit on orbital paths, partial views are gathered, and a reconstruction snaps together at the convergence points — visualised as a "supernova" event in the centre of the scene.

**[Live demo →](https://norayr-m.github.io/drt-orbital-solver/)**

## What it does

Three steps play out on the canvas:

1. **Propose problem.** A small problem is laid out in 3D. Observers (the "satellites") are positioned on orbital paths around it. Each observer sees a different view of the central object.
2. **Snap lock (eigenvectors).** The observers' partial views are aligned by an eigenvector lock — the geometry settles into a consistent reference frame.
3. **Back ribosome pass (×27).** Twenty-seven backward passes refine the reconstruction at the centre. The visual "supernova" is the moment the reconstruction stabilises.

The orbital framing is partly aesthetic — it makes the geometry visible — and partly structural: orbits give a natural way to put observers at distinct, geometrically related positions around the same object.

## Why it matters (DRT angle)

This is the **3D geometric instantiation** of the framework. Where the cellular and grid demos use abstract graphs, this one uses an actual physical-flavoured 3D scene. Two structural points are visible:

1. **Observers on orbits = observers with geometric structure.** Each observer sees the same central object from a different angle, with optical / projective structure determined by its orbit. That's a concrete instance of the family of partial projections in the framework.
2. **Convergence as snap.** The "snap lock" step is a visual analogue of an eigenvector alignment between observer frames — the moment a consistent global reconstruction becomes possible from the partial views.

The honest current claim from the v0.1 draft is conditional: under four hypotheses and a bounded computational budget, the aggregate exposes structural features not accessible from the original signal alone within the same budget. The earlier "norm-growth" prose has been retracted. The supernova flash in the demo is a visual cue, not a claim.

The companion piece on celestial mechanics is the gravitational-lensing intuition: each observer sees a refraction of the central scene determined by intervening mass; the aggregate aligns those refractions. The current demo treats this geometrically rather than physically — actual lensing is a separate problem.

## How to run

Single HTML, open in a browser:

```
git clone https://github.com/norayr-m/drt-orbital-solver.git
open drt-orbital-solver/index.html
```

No build step. No server. No external dependencies beyond a modern browser. WebGL is required.

## Companion work

- **DRT_Interstellar_Harmony** — the encode/process/decode shape on a flat ranked grid.
- **DRT_Cell_Simulator** — same family of ideas in a cellular / biological framing.

## References

- Distributed Reconstruction work — v0.1 in preparation, N. Matevosyan and A. Petrosyan.

Visualization co-authored with Claude (Anthropic).

## Author

Norayr Matevosyan

## License

GPLv3
