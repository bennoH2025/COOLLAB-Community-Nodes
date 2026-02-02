[English](#toroidal-polyhedron---documentation) | [Deutsch](#toroidal-polyhedron---dokumentation)

---

# Toroidal Polyhedron - Documentation

## Overview

**Toroidal Polyhedron** creates a fascinating hybrid 3D shape that combines the organic ring form of a torus with the geometric faceted surface of a polyhedron. Unlike a smooth torus, this shape is built from flat quadrilateral faces arranged in a grid pattern around the donut form, creating a unique geometric sculpture that bridges mathematical precision and artistic beauty.

## Inspiration & Design Philosophy

Inspired by geometric art and mathematical visualization:

- **Hybrid Form**: Torus topology + polyhedron geometry
- **Faceted Surface**: Flat quad faces instead of smooth curves
- **Parametric Grid**: Controllable tessellation density
- **Geometric Art**: Perfect for low-poly aesthetic
- **Mathematical Play**: Exploring different ways to build a torus

This node demonstrates that even familiar forms like the torus can be reimagined through different geometric approaches, creating playful and visually interesting results.

## Key Features

### 🍩 Toroidal Topology
The familiar donut shape:
- **Ring Form**: Classic torus structure
- **Major Circle**: Large circle around the center
- **Minor Circle**: Tube cross-section
- **Continuous Surface**: Wraps around completely

### 📐 Polyhedral Construction
Built from flat faces:
- **Quad Faces**: Flat four-sided polygons
- **Grid Structure**: Organized in rows and columns
- **Faceted Look**: Low-poly geometric aesthetic
- **Adjustable Density**: Control face count

### 🎛️ Parametric Control
Full control over shape:
- **Major Radius**: Size of the main ring
- **Minor Radius**: Thickness of the tube
- **Major Divisions**: Faces around the ring
- **Minor Divisions**: Faces around the tube
- **Position**: Place anywhere in 3D space

### ✨ Creative Flexibility
Versatile applications:
- **Low-Poly Art**: Geometric aesthetic
- **Architectural Forms**: Faceted structures
- **Abstract Sculptures**: Geometric art pieces
- **Game Assets**: Retro/stylized 3D objects

### ⚡ True SDF Implementation
Professional rendering:
- Signed Distance Field mathematics
- Precise quad distance calculations
- Proper ray marching
- Clean edges and corners

## Parameters

| Parameter | Range | Recommended | Description |
|-----------|-------|-------------|-------------|
| **Major Radius** | 0.1+ | 1.0 - 3.0 | Distance from center to the tube center (size of main ring) |
| **Minor Radius** | 0.01+ | 0.3 - 0.8 | Radius of the tube cross-section (thickness) |
| **Major Divisions** | 3 - 32 | 8 - 16 | Number of quad faces around the major circumference |
| **Minor Divisions** | 3 - 32 | 6 - 12 | Number of quad faces around the tube |
| **Position** | Any | (0,0,0) | XYZ position of the polyhedron center |

## Creative Usage Tips

### 🎨 Classic Toroidal Polyhedron

**Balanced Geometric Torus:**
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 12
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Result: Clean, balanced geometric donut

**High-Resolution Faceted:**
1. **Major Radius**: 2.5
2. **Minor Radius**: 0.6
3. **Major Divisions**: 20 (more faces)
4. **Minor Divisions**: 12
5. **Position**: (0, 0, 0)
6. Result: Smoother appearance, still geometric

**Low-Poly Aesthetic:**
1. **Major Radius**: 2.0
2. **Minor Radius**: 0.5
3. **Major Divisions**: 6 (few faces)
4. **Minor Divisions**: 4
5. **Position**: (0, 0, 0)
6. Result: Bold, chunky low-poly look

### 📐 Proportion Variations

**Thick Ring (Fat Donut):**
1. **Major Radius**: 1.5
2. **Minor Radius**: 0.8 (large tube)
3. **Major Divisions**: 12
4. **Minor Divisions**: 8
5. Result: Chunky, thick ring

**Thin Ring (Elegant):**
1. **Major Radius**: 3.0
2. **Minor Radius**: 0.3 (small tube)
3. **Major Divisions**: 16
4. **Minor Divisions**: 6
5. Result: Elegant, delicate ring

**Large Scale:**
1. **Major Radius**: 5.0 (very large)
2. **Minor Radius**: 1.0
3. **Major Divisions**: 20
4. **Minor Divisions**: 12
5. Result: Architectural scale structure

**Compact Form:**
1. **Major Radius**: 0.8 (small)
2. **Minor Radius**: 0.3
3. **Major Divisions**: 8
4. **Minor Divisions**: 6
5. Result: Small, compact geometric ring

### 🌀 Division Experiments

**Minimal Polygons:**
1. **Major Divisions**: 3 (minimum)
2. **Minor Divisions**: 3 (minimum)
3. Result: Extreme low-poly, triangulated appearance

**Asymmetric Grid:**
1. **Major Divisions**: 16 (many)
2. **Minor Divisions**: 4 (few)
3. Result: Long rectangular faces around ring

**Square Grid:**
1. **Major Divisions**: 12
2. **Minor Divisions**: 12 (same as major)
3. Result: More uniform quad shapes

**High Density:**
1. **Major Divisions**: 24
2. **Minor Divisions**: 16
3. Result: Approaching smooth torus appearance

### 🎨 Artistic Applications

**Retro Game Asset:**
1. **Major Radius**: 1.5
2. **Minor Radius**: 0.4
3. **Major Divisions**: 8
4. **Minor Divisions**: 6
5. Apply solid color material
6. Result: PS1/N64-era game object

**Geometric Sculpture:**
1. **Major Radius**: 3.0
2. **Minor Radius**: 0.7
3. **Major Divisions**: 14
4. **Minor Divisions**: 10
5. Metallic material with sharp reflections
6. Result: Modern art sculpture

**Architectural Element:**
1. **Major Radius**: 4.0
2. **Minor Radius**: 0.9
3. **Major Divisions**: 18
4. **Minor Divisions**: 12
5. Concrete or stone material
6. Result: Architectural ring structure

**Abstract Pattern:**
1. Create multiple instances at different positions
2. Vary division counts
3. Apply different colors
4. Result: Complex geometric composition

### 🌈 Material & Rendering

**Flat Shading:**
1. Use materials that emphasize flat faces
2. Each quad face clearly visible
3. Highlights geometric structure
4. Clean, graphic look

**Smooth vs Faceted:**
1. Low divisions: Clearly faceted
2. High divisions: Approaches smooth
3. Choice affects aesthetic
4. Experiment to find sweet spot

**Wireframe Mode:**
1. Render as wireframe
2. Shows grid structure clearly
3. Educational and artistic
4. Beautiful geometric pattern

**Gradient Mapping:**
1. Apply gradient based on height or angle
2. Colors flow across facets
3. Emphasizes form
4. Creates visual interest

### 📐 Positioning & Composition

**Floating Rings:**
1. Create multiple instances
2. Vary **Position** parameter:
   - Ring 1: (0, 0, 0)
   - Ring 2: (3, 1, 0)
   - Ring 3: (-2, -1, 1)
3. Different sizes/divisions
4. Result: Floating geometric composition

**Stacked Rings:**
1. Same X and Z position
2. Different Y positions:
   - Ring 1: Y = 0
   - Ring 2: Y = 1
   - Ring 3: Y = 2
3. Result: Vertical stack

**Interlocked Rings:**
1. Position rings to intersect
2. Different orientations (rotate in scene)
3. Creates complex interplay
4. Interesting boolean intersections

## Workflow Examples

### Example 1: Classic Geometric Torus
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 12
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Apply simple material
8. Result: Clean geometric ring

### Example 2: Low-Poly Game Asset
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 1.5
3. **Minor Radius**: 0.4
4. **Major Divisions**: 6
5. **Minor Divisions**: 4
6. **Position**: (0, 0, 0)
7. Apply solid color (no smooth shading)
8. Result: Retro game collectible ring

### Example 3: Elegant Thin Ring
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 3.5
3. **Minor Radius**: 0.25
4. **Major Divisions**: 20
5. **Minor Divisions**: 6
6. **Position**: (0, 0, 0)
7. Metallic gold material
8. Result: Elegant jewelry-like ring

### Example 4: Chunky Sculpture
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.9
4. **Major Divisions**: 10
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Matte material with strong lighting
8. Result: Bold geometric sculpture

### Example 5: High-Resolution Faceted
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 2.5
3. **Minor Radius**: 0.6
4. **Major Divisions**: 24
5. **Minor Divisions**: 16
6. **Position**: (0, 0, 0)
7. Result: Nearly smooth but still geometric

### Example 6: Minimal Triangle Grid
1. Add **Toroidal Polyhedron**
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 3
5. **Minor Divisions**: 3
6. **Position**: (0, 0, 0)
7. Result: Extreme low-poly triangulated form

### Example 7: Multiple Ring Composition
1. Create 3 instances:
   - Small: Major=1.0, Minor=0.3, Pos=(0,0,0)
   - Medium: Major=2.0, Minor=0.5, Pos=(0,1,0)
   - Large: Major=3.0, Minor=0.7, Pos=(0,2,0)
2. Same divisions: 12 major, 8 minor
3. Different colors
4. Result: Nested/stacked rings

## Technical Details

- **Node Type**: 3D SDF Shape (vec3 → SignedDistance)
- **Category**: 3D Shapes / Polyhedra
- **Construction**: Grid of quad faces on torus surface
- **Algorithm**: Parametric torus + quad distance field
- **Rendering**: Signed Distance Field
- **Face Count**: Major Divisions × Minor Divisions quads

## Understanding the Mathematics

### Torus Parametric Equations

The underlying torus surface:
```
For parameters u, v ∈ [0, 1]:

majorAngle = u × 2π (angle around main ring)
minorAngle = v × 2π (angle around tube)

centerCircle = (cos(majorAngle) × R, 0, sin(majorAngle) × R)
tubeOffset = (cos(minorAngle), sin(minorAngle)) × r

point = centerCircle + tubeOffset (in local frame)
```

**Where:**
- R = Major Radius (main ring)
- r = Minor Radius (tube thickness)
- u = position around major circle (0-1)
- v = position around tube (0-1)

### Grid Generation

**Quad face creation:**
1. Divide major circumference into Major Divisions segments
2. Divide tube circumference into Minor Divisions segments
3. Each grid cell becomes a quad face
4. Total quads = Major Divisions × Minor Divisions

**Example with 12 major, 8 minor:**
- 12 segments around main ring
- 8 segments around tube
- 12 × 8 = 96 quad faces total

### Quad Distance Calculation

For each quad face:
1. **Calculate plane**: From 4 vertices
2. **Project point**: Onto quad's plane
3. **Check bounds**: Is projection inside quad?
4. **If inside**: Distance = perpendicular distance to plane
5. **If outside**: Distance = to nearest edge/corner
6. **Return minimum**: Across all quads

### SDF Properties

**Signed Distance:**
- Positive: Outside the shape
- Zero: On the surface
- Negative: Inside (hollow)

**Advantages:**
- Smooth ray marching
- Exact surface representation
- Clean edges and corners
- Efficient rendering

## Best Practices

### 🎯 Division Guidelines

**For Smooth Appearance:**
- Major Divisions: 16-24
- Minor Divisions: 12-16
- Approaches smooth torus
- Still maintains geometric structure

**For Low-Poly Look:**
- Major Divisions: 6-10
- Minor Divisions: 4-8
- Bold, faceted appearance
- Clear geometric aesthetic

**For Minimal Polygons:**
- Major Divisions: 3-5
- Minor Divisions: 3-4
- Extreme low-poly
- Abstract geometric form

**Performance Considerations:**
- Higher divisions = more quads to calculate
- Keep total quads (major × minor) reasonable
- 32×32 = 1024 quads is maximum
- 12×8 = 96 quads is good balance

### 💡 Proportion Tips

**Aspect Ratio:**
- Major Radius / Minor Radius ratio affects shape
- **Ratio 2:1**: Thin ring (2.0 / 1.0)
- **Ratio 4:1**: Classic torus (2.0 / 0.5)
- **Ratio 8:1**: Very thin ring (3.2 / 0.4)

**Scale:**
- Large Major Radius (3+): Architectural scale
- Medium (1-3): Object scale
- Small (<1): Detail/jewelry scale

**Thickness:**
- Thick tube (minor ≈ 0.6-1.0): Chunky, solid
- Medium (0.3-0.6): Balanced
- Thin (0.1-0.3): Delicate, elegant

### ⚠️ Common Mistakes to Avoid

- ❌ Too few divisions (2 or less) - won't form properly
- ❌ Extreme division mismatch (30 vs 3) - uneven tessellation
- ❌ Minor radius > Major radius - inverted/weird topology
- ❌ Too many divisions (32×32) - performance issues
- ❌ Forgetting to set position when composing multiple

## Combining with Other Nodes

**Creative Combinations:**
- **🔄 Möbius Strip**: Compare topologies
- **✨ Array/Duplicate**: Patterns of rings
- **🎨 Materials**: Flat shading emphasizes geometry
- **💡 Boolean Operations**: Intersect, subtract
- **🌈 Gradient Mapping**: Color across facets
- **📐 Other Polyhedra**: Compose geometric scenes

**Composition Ideas:**
- Multiple rings at different scales
- Interlocked/intersecting rings
- Rings as architectural elements
- Abstract geometric sculptures

## Troubleshooting Guide

### Problem: Shape doesn't appear
**Solutions**:
- ✅ Check divisions: Must be ≥ 3
- ✅ Check radii: Major > Minor usually
- ✅ Check position: Might be off-camera
- ✅ Check SDF rendering settings

### Problem: Too faceted/chunky
**Solutions**:
- ✅ Increase **Major Divisions** (16-20)
- ✅ Increase **Minor Divisions** (10-14)
- ✅ Higher divisions = smoother appearance
- ✅ Balance between smooth and performance

### Problem: Looks too smooth, want more geometry
**Solutions**:
- ✅ Reduce **Major Divisions** (6-8)
- ✅ Reduce **Minor Divisions** (4-6)
- ✅ Lower divisions = more faceted
- ✅ Use flat shading material

### Problem: Weird proportions
**Solutions**:
- ✅ Adjust **Major Radius** to **Minor Radius** ratio
- ✅ Try ratio 4:1 for classic torus (e.g., 2.0 / 0.5)
- ✅ Minor shouldn't be larger than major
- ✅ Experiment with different ratios

### Problem: Performance issues
**Solutions**:
- ✅ Reduce total quads (major × minor)
- ✅ Try 12×8 = 96 instead of 24×16 = 384
- ✅ Lower divisions still looks good
- ✅ Maximum is 32×32 = 1024

### Problem: Faces appear distorted
**Solutions**:
- ✅ This is normal for toroidal geometry
- ✅ Inner ring quads are smaller than outer
- ✅ Use more divisions for more uniform quads
- ✅ Asymmetry is part of the geometric nature

## Fun Facts & Applications

### Why "Toroidal Polyhedron"?

- **Toroidal**: Has torus topology (genus-1 surface with hole)
- **Polyhedron**: Built from flat polygonal faces
- **Hybrid**: Combines two mathematical concepts
- **Result**: Geometric interpretation of organic form

### Real-World Inspirations

- **Architecture**: Faceted ring structures in buildings
- **Game Design**: Low-poly collectibles and power-ups
- **Jewelry**: Geometric ring designs
- **Art**: Geometric sculptures and installations
- **Product Design**: Stylized toroidal forms

### Mathematical Interest

- **Tessellation**: How to tile a torus surface
- **Discrete Geometry**: Polygonal approximation of curves
- **Topology**: Maintains torus properties (genus-1)
- **Parametric Surfaces**: Grid-based surface generation

### Creative Variations

Try experimenting with:
- Different division ratios (e.g., 16×4 vs 4×16)
- Extreme proportions (very thick or very thin)
- Minimal polygons (3×3 triangle grid)
- High resolution (approaching smooth)

## Why This Node Was Created

Sometimes the most interesting forms come from playful experimentation. **Toroidal Polyhedron** provides:

- ✅ **Geometric play** with familiar forms
- ✅ **Low-poly aesthetic** for retro/stylized work
- ✅ **Parametric control** over tessellation
- ✅ **Educational value** in discrete geometry
- ✅ **Artistic flexibility** for sculptures
- ✅ **Fun exploration** of torus variations

A "lustiges Ding" that bridges mathematics, art, and play!

## Credits

- Inspired by: Geometric art and toroidal polyhedra research
- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2025

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#toroidal-polyhedron---documentation) | [Deutsch](#toroidal-polyhedron---dokumentation)

---

# Toroidal Polyhedron - Dokumentation

## Übersicht

**Toroidal Polyhedron** erstellt eine faszinierende hybride 3D-Form, die die organische Ringform eines Torus mit der geometrischen facettierten Oberfläche eines Polyeders kombiniert. Im Gegensatz zu einem glatten Torus ist diese Form aus flachen viereckigen Flächen aufgebaut, die in einem Gittermuster um die Donut-Form angeordnet sind, und erzeugt eine einzigartige geometrische Skulptur, die mathematische Präzision und künstlerische Schönheit verbindet.

## 🎯 Inspiration & Design-Philosophie

Inspiriert von geometrischer Kunst und mathematischer Visualisierung:

- **Hybrid-Form**: Torus-Topologie + Polyeder-Geometrie
- **Facettierte Oberfläche**: Flache Quad-Flächen statt glatter Kurven
- **Parametrisches Gitter**: Kontrollierbare Tessellierungs-Dichte
- **Geometrische Kunst**: Perfekt für Low-Poly-Ästhetik
- **Mathematisches Spiel**: Erkundung verschiedener Wege, einen Torus zu bauen

Dieser Node demonstriert, dass selbst vertraute Formen wie der Torus durch verschiedene geometrische Ansätze neu vorgestellt werden können, was spielerische und visuell interessante Ergebnisse erzeugt.

## ⭐ Hauptmerkmale

### 🍩 Toroidale Topologie
Die vertraute Donut-Form:
- **Ringform**: Klassische Torus-Struktur
- **Hauptkreis**: Großer Kreis um das Zentrum
- **Nebenkreis**: Röhren-Querschnitt
- **Kontinuierliche Oberfläche**: Wickelt vollständig herum

### 📐 Polyedrische Konstruktion
Gebaut aus flachen Flächen:
- **Quad-Flächen**: Flache vierseitige Polygone
- **Gitter-Struktur**: Organisiert in Reihen und Spalten
- **Facettierter Look**: Low-Poly geometrische Ästhetik
- **Anpassbare Dichte**: Kontrolle über Flächenanzahl

### 🎛️ Parametrische Kontrolle
Volle Kontrolle über Form:
- **Major Radius**: Größe des Hauptrings
- **Minor Radius**: Dicke der Röhre
- **Major Divisions**: Flächen um den Ring
- **Minor Divisions**: Flächen um die Röhre
- **Position**: Platzierung irgendwo im 3D-Raum

### ✨ Kreative Flexibilität
Vielseitige Anwendungen:
- **Low-Poly-Kunst**: Geometrische Ästhetik
- **Architektonische Formen**: Facettierte Strukturen
- **Abstrakte Skulpturen**: Geometrische Kunstwerke
- **Game-Assets**: Retro/stilisierte 3D-Objekte

### ⚡ Echte SDF-Implementation
Professionelles Rendering:
- Signed Distance Field Mathematik
- Präzise Quad-Distanz-Berechnungen
- Korrektes Ray Marching
- Saubere Kanten und Ecken

## 📊 Parameter

| Parameter | Bereich | Empfohlen | Beschreibung |
|-----------|---------|-----------|--------------|
| **Major Radius** | 0.1+ | 1.0 - 3.0 | Distanz vom Zentrum zur Röhren-Mitte (Größe des Hauptrings) |
| **Minor Radius** | 0.01+ | 0.3 - 0.8 | Radius des Röhren-Querschnitts (Dicke) |
| **Major Divisions** | 3 - 32 | 8 - 16 | Anzahl der Quad-Flächen um den Hauptumfang |
| **Minor Divisions** | 3 - 32 | 6 - 12 | Anzahl der Quad-Flächen um die Röhre |
| **Position** | Beliebig | (0,0,0) | XYZ-Position des Polyeder-Zentrums |

## 🎨 Kreative Nutzungstipps

### 🎓 Klassisches Toroidal Polyhedron

**Balancierter Geometrischer Torus:**
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 12
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Ergebnis: Sauberer, balancierter geometrischer Donut

**Hoch-Auflösend Facettiert:**
1. **Major Radius**: 2.5
2. **Minor Radius**: 0.6
3. **Major Divisions**: 20 (mehr Flächen)
4. **Minor Divisions**: 12
5. **Position**: (0, 0, 0)
6. Ergebnis: Glatteres Erscheinungsbild, noch geometrisch

**Low-Poly-Ästhetik:**
1. **Major Radius**: 2.0
2. **Minor Radius**: 0.5
3. **Major Divisions**: 6 (wenige Flächen)
4. **Minor Divisions**: 4
5. **Position**: (0, 0, 0)
6. Ergebnis: Kühner, klobiger Low-Poly-Look

### 📐 Proportions-Variationen

**Dicker Ring (Fetter Donut):**
1. **Major Radius**: 1.5
2. **Minor Radius**: 0.8 (große Röhre)
3. **Major Divisions**: 12
4. **Minor Divisions**: 8
5. Ergebnis: Klobiger, dicker Ring

**Dünner Ring (Elegant):**
1. **Major Radius**: 3.0
2. **Minor Radius**: 0.3 (kleine Röhre)
3. **Major Divisions**: 16
4. **Minor Divisions**: 6
5. Ergebnis: Eleganter, delikater Ring

**Großer Maßstab:**
1. **Major Radius**: 5.0 (sehr groß)
2. **Minor Radius**: 1.0
3. **Major Divisions**: 20
4. **Minor Divisions**: 12
5. Ergebnis: Architektonische Maßstabs-Struktur

**Kompakte Form:**
1. **Major Radius**: 0.8 (klein)
2. **Minor Radius**: 0.3
3. **Major Divisions**: 8
4. **Minor Divisions**: 6
5. Ergebnis: Kleiner, kompakter geometrischer Ring

### 🌀 Divisions-Experimente

**Minimale Polygone:**
1. **Major Divisions**: 3 (Minimum)
2. **Minor Divisions**: 3 (Minimum)
3. Ergebnis: Extrem Low-Poly, trianguliertes Erscheinungsbild

**Asymmetrisches Gitter:**
1. **Major Divisions**: 16 (viele)
2. **Minor Divisions**: 4 (wenige)
3. Ergebnis: Lange rechteckige Flächen um Ring

**Quadratisches Gitter:**
1. **Major Divisions**: 12
2. **Minor Divisions**: 12 (gleich wie major)
3. Ergebnis: Gleichförmigere Quad-Formen

**Hohe Dichte:**
1. **Major Divisions**: 24
2. **Minor Divisions**: 16
3. Ergebnis: Annäherung an glattes Torus-Erscheinungsbild

### 🎨 Künstlerische Anwendungen

**Retro-Game-Asset:**
1. **Major Radius**: 1.5
2. **Minor Radius**: 0.4
3. **Major Divisions**: 8
4. **Minor Divisions**: 6
5. Wenden Sie Solidfarben-Material an
6. Ergebnis: PS1/N64-Ära Game-Objekt

**Geometrische Skulptur:**
1. **Major Radius**: 3.0
2. **Minor Radius**: 0.7
3. **Major Divisions**: 14
4. **Minor Divisions**: 10
5. Metallisches Material mit scharfen Reflexionen
6. Ergebnis: Moderne Kunst-Skulptur

**Architektonisches Element:**
1. **Major Radius**: 4.0
2. **Minor Radius**: 0.9
3. **Major Divisions**: 18
4. **Minor Divisions**: 12
5. Beton- oder Stein-Material
6. Ergebnis: Architektonische Ring-Struktur

**Abstraktes Muster:**
1. Erstellen Sie mehrere Instanzen an verschiedenen Positionen
2. Variieren Sie Division-Anzahlen
3. Wenden Sie verschiedene Farben an
4. Ergebnis: Komplexe geometrische Komposition

### 🌈 Material & Rendering

**Flat Shading:**
1. Nutzen Sie Materialien, die flache Flächen betonen
2. Jede Quad-Fläche klar sichtbar
3. Hebt geometrische Struktur hervor
4. Sauberer, grafischer Look

**Glatt vs Facettiert:**
1. Niedrige Divisions: Klar facettiert
2. Hohe Divisions: Nähert sich glatt an
3. Wahl beeinflusst Ästhetik
4. Experimentieren für Sweet Spot

**Wireframe-Modus:**
1. Als Wireframe rendern
2. Zeigt Gitter-Struktur klar
3. Bildend und künstlerisch
4. Wunderschönes geometrisches Muster

**Gradient-Mapping:**
1. Wenden Sie Gradient basierend auf Höhe oder Winkel an
2. Farben fließen über Facetten
3. Betont Form
4. Erzeugt visuelles Interesse

### 📐 Positionierung & Komposition

**Schwebende Ringe:**
1. Erstellen Sie mehrere Instanzen
2. Variieren Sie **Position**-Parameter:
   - Ring 1: (0, 0, 0)
   - Ring 2: (3, 1, 0)
   - Ring 3: (-2, -1, 1)
3. Verschiedene Größen/Divisions
4. Ergebnis: Schwebende geometrische Komposition

**Gestapelte Ringe:**
1. Gleiche X und Z Position
2. Verschiedene Y Positionen:
   - Ring 1: Y = 0
   - Ring 2: Y = 1
   - Ring 3: Y = 2
3. Ergebnis: Vertikaler Stapel

**Ineinandergreifende Ringe:**
1. Positionieren Sie Ringe zum Schnitt
2. Verschiedene Orientierungen (in Szene rotieren)
3. Erzeugt komplexes Zusammenspiel
4. Interessante Boolean-Schnittmengen

## 💡 Workflow-Beispiele

### Beispiel 1: Klassischer Geometrischer Torus
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 12
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Wenden Sie einfaches Material an
8. Ergebnis: Sauberer geometrischer Ring

### Beispiel 2: Low-Poly-Game-Asset
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 1.5
3. **Minor Radius**: 0.4
4. **Major Divisions**: 6
5. **Minor Divisions**: 4
6. **Position**: (0, 0, 0)
7. Wenden Sie Solidfarbe an (kein Smooth Shading)
8. Ergebnis: Retro-Game sammelbarer Ring

### Beispiel 3: Eleganter Dünner Ring
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 3.5
3. **Minor Radius**: 0.25
4. **Major Divisions**: 20
5. **Minor Divisions**: 6
6. **Position**: (0, 0, 0)
7. Metallisches Gold-Material
8. Ergebnis: Eleganter schmuck-artiger Ring

### Beispiel 4: Klobige Skulptur
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.9
4. **Major Divisions**: 10
5. **Minor Divisions**: 8
6. **Position**: (0, 0, 0)
7. Mattes Material mit starker Beleuchtung
8. Ergebnis: Kühne geometrische Skulptur

### Beispiel 5: Hoch-Auflösend Facettiert
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 2.5
3. **Minor Radius**: 0.6
4. **Major Divisions**: 24
5. **Minor Divisions**: 16
6. **Position**: (0, 0, 0)
7. Ergebnis: Nahezu glatt aber noch geometrisch

### Beispiel 6: Minimales Dreieck-Gitter
1. Fügen Sie **Toroidal Polyhedron** hinzu
2. **Major Radius**: 2.0
3. **Minor Radius**: 0.5
4. **Major Divisions**: 3
5. **Minor Divisions**: 3
6. **Position**: (0, 0, 0)
7. Ergebnis: Extrem Low-Poly triangulierte Form

### Beispiel 7: Mehrfach-Ring-Komposition
1. Erstellen Sie 3 Instanzen:
   - Klein: Major=1.0, Minor=0.3, Pos=(0,0,0)
   - Mittel: Major=2.0, Minor=0.5, Pos=(0,1,0)
   - Groß: Major=3.0, Minor=0.7, Pos=(0,2,0)
2. Gleiche Divisions: 12 major, 8 minor
3. Verschiedene Farben
4. Ergebnis: Verschachtelte/gestapelte Ringe

## 🔧 Technische Details

- **Node-Typ**: 3D SDF Shape (vec3 → SignedDistance)
- **Kategorie**: 3D Shapes / Polyhedra
- **Konstruktion**: Gitter von Quad-Flächen auf Torus-Oberfläche
- **Algorithmus**: Parametrischer Torus + Quad-Distanz-Feld
- **Rendering**: Signed Distance Field
- **Flächen-Anzahl**: Major Divisions × Minor Divisions Quads

## 🧮 Verständnis der Mathematik

### Torus Parametrische Gleichungen

Die zugrunde liegende Torus-Oberfläche:
```
Für Parameter u, v ∈ [0, 1]:

majorAngle = u × 2π (Winkel um Hauptring)
minorAngle = v × 2π (Winkel um Röhre)

centerCircle = (cos(majorAngle) × R, 0, sin(majorAngle) × R)
tubeOffset = (cos(minorAngle), sin(minorAngle)) × r

point = centerCircle + tubeOffset (in lokalem Frame)
```

**Wobei:**
- R = Major Radius (Hauptring)
- r = Minor Radius (Röhrendicke)
- u = Position um Hauptkreis (0-1)
- v = Position um Röhre (0-1)

### Gitter-Generierung

**Quad-Flächen-Erstellung:**
1. Teilen Sie Hauptumfang in Major Divisions Segmente
2. Teilen Sie Röhrenumfang in Minor Divisions Segmente
3. Jede Gitterzelle wird eine Quad-Fläche
4. Gesamt-Quads = Major Divisions × Minor Divisions

**Beispiel mit 12 major, 8 minor:**
- 12 Segmente um Hauptring
- 8 Segmente um Röhre
- 12 × 8 = 96 Quad-Flächen gesamt

### Quad-Distanz-Berechnung

Für jede Quad-Fläche:
1. **Ebene berechnen**: Von 4 Vertices
2. **Punkt projizieren**: Auf Quad-Ebene
3. **Grenzen prüfen**: Ist Projektion innerhalb Quad?
4. **Falls innerhalb**: Distanz = senkrechte Distanz zur Ebene
5. **Falls außerhalb**: Distanz = zur nächsten Kante/Ecke
6. **Minimum zurückgeben**: Über alle Quads

### SDF-Eigenschaften

**Signed Distance:**
- Positiv: Außerhalb der Form
- Null: Auf der Oberfläche
- Negativ: Innerhalb (hohl)

**Vorteile:**
- Glattes Ray Marching
- Exakte Oberflächen-Darstellung
- Saubere Kanten und Ecken
- Effizientes Rendering

## 🎬 Best Practices

### 🎯 Divisions-Richtlinien

**Für Glattes Erscheinungsbild:**
- Major Divisions: 16-24
- Minor Divisions: 12-16
- Nähert sich glattem Torus an
- Erhält noch geometrische Struktur

**Für Low-Poly-Look:**
- Major Divisions: 6-10
- Minor Divisions: 4-8
- Kühnes, facettiertes Erscheinungsbild
- Klare geometrische Ästhetik

**Für Minimale Polygone:**
- Major Divisions: 3-5
- Minor Divisions: 3-4
- Extrem Low-Poly
- Abstrakte geometrische Form

**Performance-Überlegungen:**
- Höhere Divisions = mehr Quads zu berechnen
- Halten Sie Gesamt-Quads (major × minor) vernünftig
- 32×32 = 1024 Quads ist Maximum
- 12×8 = 96 Quads ist gute Balance

### 💡 Proportions-Tipps

**Seitenverhältnis:**
- Major Radius / Minor Radius Verhältnis beeinflusst Form
- **Verhältnis 2:1**: Dünner Ring (2.0 / 1.0)
- **Verhältnis 4:1**: Klassischer Torus (2.0 / 0.5)
- **Verhältnis 8:1**: Sehr dünner Ring (3.2 / 0.4)

**Maßstab:**
- Großer Major Radius (3+): Architektonischer Maßstab
- Mittel (1-3): Objekt-Maßstab
- Klein (<1): Detail-/Schmuck-Maßstab

**Dicke:**
- Dicke Röhre (minor ≈ 0.6-1.0): Klobig, solide
- Mittel (0.3-0.6): Balanciert
- Dünn (0.1-0.3): Delikat, elegant

### ⚠️ Häufige Fehler vermeiden

- ❌ Zu wenige Divisions (2 oder weniger) - formt sich nicht richtig
- ❌ Extreme Division-Fehlanpassung (30 vs 3) - ungleichmäßige Tessellierung
- ❌ Minor Radius > Major Radius - invertierte/seltsame Topologie
- ❌ Zu viele Divisions (32×32) - Performance-Probleme
- ❌ Vergessen, Position zu setzen beim Komponieren mehrerer

## 🔗 Kombination mit anderen Nodes

**Kreative Kombinationen:**
- **🔄 Möbius Strip**: Topologien vergleichen
- **✨ Array/Duplicate**: Muster von Ringen
- **🎨 Materialien**: Flat Shading betont Geometrie
- **💡 Boolean-Operationen**: Schnitt, Subtraktion
- **🌈 Gradient-Mapping**: Farbe über Facetten
- **📐 Andere Polyeder**: Geometrische Szenen komponieren

**Kompositions-Ideen:**
- Mehrere Ringe in verschiedenen Skalen
- Ineinandergreifende/sich schneidende Ringe
- Ringe als architektonische Elemente
- Abstrakte geometrische Skulpturen

## 🔧 Fehlerbehebungs-Guide

### Problem: Form erscheint nicht
**Lösungen**:
- ✅ Prüfen Sie Divisions: Muss ≥ 3 sein
- ✅ Prüfen Sie Radien: Major > Minor normalerweise
- ✅ Prüfen Sie Position: Könnte außerhalb Kamera sein
- ✅ Prüfen Sie SDF-Rendering-Einstellungen

### Problem: Zu facettiert/klobig
**Lösungen**:
- ✅ Erhöhen Sie **Major Divisions** (16-20)
- ✅ Erhöhen Sie **Minor Divisions** (10-14)
- ✅ Höhere Divisions = glatteres Erscheinungsbild
- ✅ Balance zwischen glatt und Performance

### Problem: Sieht zu glatt aus, möchte mehr Geometrie
**Lösungen**:
- ✅ Reduzieren Sie **Major Divisions** (6-8)
- ✅ Reduzieren Sie **Minor Divisions** (4-6)
- ✅ Niedrigere Divisions = facettierter
- ✅ Nutzen Sie Flat-Shading-Material

### Problem: Seltsame Proportionen
**Lösungen**:
- ✅ Passen Sie **Major Radius** zu **Minor Radius** Verhältnis an
- ✅ Versuchen Sie Verhältnis 4:1 für klassischen Torus (z.B. 2.0 / 0.5)
- ✅ Minor sollte nicht größer als Major sein
- ✅ Experimentieren Sie mit verschiedenen Verhältnissen

### Problem: Performance-Probleme
**Lösungen**:
- ✅ Reduzieren Sie Gesamt-Quads (major × minor)
- ✅ Versuchen Sie 12×8 = 96 statt 24×16 = 384
- ✅ Niedrigere Divisions sehen noch gut aus
- ✅ Maximum ist 32×32 = 1024

### Problem: Flächen erscheinen verzerrt
**Lösungen**:
- ✅ Das ist normal für toroidale Geometrie
- ✅ Innere Ring-Quads sind kleiner als äußere
- ✅ Nutzen Sie mehr Divisions für gleichförmigere Quads
- ✅ Asymmetrie ist Teil der geometrischen Natur

## 📚 Spaß-Fakten & Anwendungen

### Warum "Toroidal Polyhedron"?

- **Toroidal**: Hat Torus-Topologie (Genus-1-Oberfläche mit Loch)
- **Polyhedron**: Gebaut aus flachen polygonalen Flächen
- **Hybrid**: Kombiniert zwei mathematische Konzepte
- **Ergebnis**: Geometrische Interpretation organischer Form

### Reale Inspirationen

- **Architektur**: Facettierte Ring-Strukturen in Gebäuden
- **Game-Design**: Low-Poly-Sammelobjekte und Power-Ups
- **Schmuck**: Geometrische Ring-Designs
- **Kunst**: Geometrische Skulpturen und Installationen
- **Produkt-Design**: Stilisierte toroidale Formen

### Mathematisches Interesse

- **Tessellierung**: Wie man eine Torus-Oberfläche kachelt
- **Diskrete Geometrie**: Polygonale Approximation von Kurven
- **Topologie**: Erhält Torus-Eigenschaften (Genus-1)
- **Parametrische Oberflächen**: Gitter-basierte Oberflächen-Generierung

### Kreative Variationen

Versuchen Sie zu experimentieren mit:
- Verschiedenen Division-Verhältnissen (z.B. 16×4 vs 4×16)
- Extremen Proportionen (sehr dick oder sehr dünn)
- Minimalen Polygonen (3×3 Dreieck-Gitter)
- Hoher Auflösung (Annäherung an glatt)

## 💡 Warum dieser Node erstellt wurde

Manchmal kommen die interessantesten Formen aus spielerischem Experimentieren. **Toroidal Polyhedron** bietet:

- ✅ **Geometrisches Spiel** mit vertrauten Formen
- ✅ **Low-Poly-Ästhetik** für Retro/stilisierte Arbeit
- ✅ **Parametrische Kontrolle** über Tessellierung
- ✅ **Bildender Wert** in diskreter Geometrie
- ✅ **Künstlerische Flexibilität** für Skulpturen
- ✅ **Spaß-Erkundung** von Torus-Variationen

Ein "lustiges Ding", das Mathematik, Kunst und Spiel verbindet!

## 📜 Credits

- Inspiriert von: Geometrischer Kunst und Toroidal-Polyeder-Forschung
- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2025

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
