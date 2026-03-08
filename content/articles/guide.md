---
title: "How DMLS Works: Laser Parameters, Build Strategy, and Process Physics"
date: 2026-03-08
summary: "DMLS is often described as 'laser sintering metal powder' but the physics is full melting, not sintering. Understanding the process at the parameter level is essential for design and quality."
tags: ["DMLS process", "laser parameters", "energy density", "powder bed fusion"]
---

Direct Metal Laser Sintering — invented by EOS GmbH in 1987, commercialized in the
1990s — fully melts pre-alloyed metal powder with a focused laser beam. The "sintering"
in the name is a historical artifact. The physics is fusion.

## Core Process Parameters

**Laser power (P):** 200–400W for most materials. Higher power increases melt pool
size and build rate; lower power improves feature resolution.

**Scan speed (v):** 800–1,600 mm/s typical. Higher speed reduces energy per unit length.

**Hatch spacing (h):** 0.05–0.15 mm. Overlap between adjacent laser tracks determines
melt pool connectivity.

**Layer thickness (t):** 20–100 µm. Thinner layers: better resolution, slower build.
50 µm is the most common production setting.

## Energy Density

The combined effect of these parameters is expressed as volumetric energy density:

**E = P / (v × h × t)** [J/mm³]

Target: 50–100 J/mm³ for most alloys. Below this range: lack-of-fusion porosity.
Above: keyhole porosity from excessive melt pool vaporization.

## Build Strategy

**Scan pattern:** Island scanning (5×5 mm or 7×7 mm squares, rotated 67° per layer)
distributes thermal stress and prevents systematic directionality in mechanical properties.

**Support structures:** Required for geometry below 45° from horizontal. Supports
conduct heat and prevent warping. Lattice supports preferred over solid for easier removal.

**Part orientation:** XY orientation (flat on build plate) maximizes accuracy and
surface finish. Z orientation (tall, vertical) maximizes build productivity but reduces
XY-plane resolution.
