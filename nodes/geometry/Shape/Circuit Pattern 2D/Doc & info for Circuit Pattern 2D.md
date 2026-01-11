# Circuit Pattern 2D - Documentation

## Overview

**Circuit Pattern 2D** is a procedurally generated 2D SDF (Signed Distance Field) node that creates animated electronic circuit board patterns. Inspired by the intricate layouts of printed circuit boards (PCBs), this node generates organic, flowing patterns that resemble electronic traces, solder pads, and component layouts.

## Inspiration & Design Philosophy

While visually similar to **Cairo Tiling** in its geometric nature, Circuit Pattern 2D takes a fundamentally different approach:

- **Cairo Tiling** is based on regular, uniform grid patterns with predictable, repeating structures
- **Circuit Pattern 2D** uses Voronoi-based procedural generation to create **irregular, organic patterns** that never repeat exactly the same way
- The uneven, asymmetric nature mimics the authentic look of real circuit board layouts, where traces follow functional requirements rather than aesthetic symmetry
- The **built-in animation** brings these patterns to life, simulating the flow of electrons through the circuit pathways

This organic irregularity becomes especially apparent when the animation is active, as the "electron flow" effect travels through the unpredictable pathways, creating a mesmerizing, ever-changing visual experience.

## Key Features

### 🎬 Integrated Animation
One of the standout features of this node is its **built-in animation system**. Unlike many procedural patterns that require external animation setups, Circuit Pattern 2D comes alive with just one click:

- **Perfect for beginners**: Simply press the Play button in Coollab's timeline and watch the circuit patterns animate automatically
- **Electron Flow effect**: Simulates moving charges traveling through the circuit traces
- **Flicker effect**: Adds authentic visual noise resembling real electronic components
- **Manual synchronization**: Use the `Animation Speed` parameter to sync the animation to music or other timing requirements by hand

This makes Circuit Pattern 2D exceptionally accessible for newcomers while remaining powerful enough for advanced users.

### 🔧 Multi-Octave Detail
The pattern is built using multiple layers (octaves) of Voronoi noise, allowing you to control the complexity:
- Lower octave values (1-2) create simpler, cleaner circuit patterns
- Higher octave values (3-4) add intricate detail and smaller circuit traces

### ⚡ Dynamic Effects
- **Electron Flow**: Animated "electrons" that travel through the circuit pathways
- **Flicker Amount**: Simulates the flickering of electronic components or unstable power
- **Vignette**: Subtle darkening at the edges for a more focused composition

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Pattern Scale** | 0.5 - 10.0 | 2.0 | Controls the density and size of the circuit pattern. Higher values create more intricate, tightly-packed circuits. |
| **Line Thickness** | 0.1 - 1.0 | 0.4 | Adjusts the width of the circuit traces. Thinner lines create more delicate patterns. |
| **Animation Speed** | 0.0 - 5.0 | 1.0 | Controls how fast the electron flow and other animations play. Set to 0 for a static pattern. |
| **Offset** | Point2D | (0.0, 0.0) | Shifts the entire pattern in 2D space. Useful for positioning or creating variations. |
| **Octaves** | 1.0 - 4.0 | 3.0 | Number of detail layers. More octaves = more complex patterns (but potentially slower). |
| **Electron Flow** | 0.0 - 2.0 | 0.5 | Intensity of the animated electron effect. Higher values create more visible "energy" flowing through the circuits. |
| **Flicker Amount** | 0.0 - 1.0 | 0.3 | Amount of random flickering. Adds visual noise for a more organic, less perfect appearance. |

## Creative Usage Tips

### 🌟 Combining with 2D Modifiers

The **2D Modifier** category in Coollab offers endless possibilities for transforming Circuit Pattern 2D into completely new visuals:

**Highly Recommended Combinations:**
- **Star Symmetry**: Creates kaleidoscopic circuit mandalas with radial repetition
- **Sine Warp Tile**: Adds flowing, wave-like distortions to the circuit patterns
- **Warping Illusionary**: Combines multiple warping effects for surreal, impossible circuit geometries
- **Kaleidoscope nodes**: Generate mesmerizing symmetric patterns from the irregular circuits
- **Polar Coordinates**: Transform linear circuits into circular, radial designs

**Experimental Suggestions:**
- Try stacking multiple modifiers for unexpected results
- Combine with displacement or noise modifiers for glitch-art aesthetics
- Use rotation and scaling modifiers for dynamic camera-like movements

### 🎨 Creating Variations Quickly

Because Circuit Pattern 2D is a 2D SDF, you can rapidly iterate and create dozens of variations:
1. Start with default settings
2. Apply a 2D Modifier
3. Adjust 1-2 parameters
4. Save as a preset or screenshot the result
5. Repeat with different modifiers

This workflow allows for fast exploration and is perfect for creative experimentation.

### 🔮 Converting to 3D

Circuit Pattern 2D works beautifully with Coollab's **2D to 3D shape converters**:

**Tips for 3D Conversion:**
- **Start subtle**: Use moderate extrusion/depth values to maintain recognizability
- **Combine with 3D Modifiers**: After conversion, apply 3D SDF modifiers like twists, bends, or repetitions for unique sculptural forms
- **Exercise restraint**: The patterns can become overwhelming in 3D - less is often more
- **Lighting matters**: Experiment with different lighting setups to emphasize the circuit topology

The irregular, organic nature of the circuits translates surprisingly well into 3D space, creating structures that feel both technological and natural.

## Technical Details

- **Node Type**: 2D SDF (UV → SignedDistance)
- **Category**: 2D SDF
- **Animation**: Built-in via `_time` variable
- **Algorithm**: Multi-octave Voronoi noise with Chebyshev distance
- **Performance**: Moderate (scales with octave count)

## Workflow Examples

### Example 1: Animated Circuit Background
1. Add Circuit Pattern 2D to your composition
2. Press Play in the timeline
3. Adjust `Animation Speed` to match your project tempo
4. Use as a background layer or mask

### Example 2: Glitch Art
1. Start with Circuit Pattern 2D
2. Set `Flicker Amount` to 0.7-1.0
3. Add a **Displacement** modifier
4. Combine with color effects for cyberpunk aesthetics

### Example 3: 3D Circuit Sculpture
1. Create Circuit Pattern 2D
2. Convert to 3D using an extrusion node
3. Apply a **Twist** or **Bend** 3D modifier
4. Render with metallic materials for a tech-art look

## Creative Freedom

The beauty of Circuit Pattern 2D lies in its versatility and the unexpected results that emerge from experimentation. Don't be afraid to:
- Push parameters to extreme values
- Combine seemingly incompatible modifiers
- Break the "rules" and see what happens
- Layer multiple instances with blend modes

**Let your creativity flow freely** - just like the electrons flowing through these digital circuits! ⚡✨

## Credits

- Inspired by electronic circuit board patterns and procedural generation techniques
- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2025

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
