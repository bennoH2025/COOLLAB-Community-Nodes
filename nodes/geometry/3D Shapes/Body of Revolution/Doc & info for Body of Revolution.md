[English](#body-of-revolution---documentation) | [Deutsch](#body-of-revolution---dokumentation)

---

# Body of Revolution - Documentation

## Overview

**Body of Revolution** creates 3D shapes by rotating a 2D profile curve around a vertical axis. This powerful node lets you create everything from simple cylinders to complex vases, bottles, bowls, and abstract sculptural forms with precise control over the profile shape and asymmetric distortions.

## Inspiration & Design Philosophy

Based on the mathematical concept of surfaces of revolution:

- **Rotational Symmetry**: 2D profile rotated 360° around Y-axis
- **9 Control Points**: Precise profile shaping with 9 radius points
- **7 Profile Types**: From basic shapes to organic forms
- **Dual Eccentricity**: Two independent off-center displacement points
- **Professional Control**: Create pottery, architecture, abstract art

This node brings the classic mathematical surface of revolution to Coollab with artistic flexibility and technical precision.

## Key Features

### 🔄 Rotational Construction
Classic body of revolution:
- **Y-Axis Rotation**: Profile spins around vertical axis
- **Continuous Surface**: Smooth 360° rotation
- **Signed Distance Field**: Professional SDF rendering
- **Real-time**: Interactive parameter adjustment

### 📐 9 Radius Control Points
Precise profile control:
- **Base Radius** (0/8): Bottom
- **Radius 1-7**: Intermediate points at 1/8 through 7/8 height
- **Top Radius** (8/8): Top
- **Linear Interpolation**: Smooth transitions between points
- **Full Control**: Shape any profile curve

### 🎨 7 Profile Types
Preset profile modifications:
- **0 - Cylinder**: Straight sides, uses radius points as-is
- **1 - Cone**: Linear taper, uses radius points directly
- **2 - Sphere**: Circular profile (spherical shape)
- **3 - Vase**: Smooth bulge in middle
- **4 - Hourglass**: Pinch/constriction in middle
- **5 - Bulb**: Bulge at bottom, narrow at top
- **6 - Bowl**: Smooth curve, wide at top

### ↗️ Dual Eccentricity
Two independent off-center points:
- **Eccentric Point**: First displacement (0.0-8.0 range)
- **Decentric Point**: Second independent displacement (0.0-8.0 range)
- **Amount Control**: How far off-center each displaces
- **Angle Control**: Direction of displacement (0-TAU)
- **Smooth Falloff**: Gradual influence around each point
- **Asymmetric Forms**: Create tilted, warped, organic shapes

### 🎯 Flat Caps
Clean top and bottom closure:
- **Top Cap**: Flat circular lid at top radius
- **Bottom Cap**: Flat circular lid at base radius
- **No Artifacts**: Clean SDF mathematics
- **Eccentric Compatible**: Caps follow eccentricity

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Profile Type** | 0 - 6 | 0 | Shape modification: 0=Cylinder, 1=Cone, 2=Sphere, 3=Vase, 4=Hourglass, 5=Bulb, 6=Bowl |
| **Height** | 0.1+ | 2.0 | Total height of the object |
| **Base Radius** | 0.01+ | 0.5 | Radius at bottom (0/8 height) |
| **Radius 1** | 0.01+ | 0.5 | Radius at 1/8 height |
| **Radius 2** | 0.01+ | 0.5 | Radius at 2/8 height |
| **Radius 3** | 0.01+ | 0.5 | Radius at 3/8 height |
| **Radius 4** | 0.01+ | 0.5 | Radius at 4/8 height (middle) |
| **Radius 5** | 0.01+ | 0.5 | Radius at 5/8 height |
| **Radius 6** | 0.01+ | 0.5 | Radius at 6/8 height |
| **Radius 7** | 0.01+ | 0.5 | Radius at 7/8 height |
| **Top Radius** | 0.01+ | 0.5 | Radius at top (8/8 height) |
| **Bulge** | 0.0 - 2.0 | 0.0 | Bulge amount for Vase/Hourglass/Bulb/Bowl profiles |
| **Smoothness** | 0.01 - 0.99 | 0.5 | Curve smoothness (currently for Bowl profile) |
| **Eccentric Point** | 0.0 - 8.0 | 0.0 | Height position for first eccentricity (0=bottom, 8=top) |
| **Eccentricity Amount** | 0.0+ | 0.0 | How far off-center to displace first point (0=none) |
| **Eccentricity Angle** | 0.0 - TAU | 0.0 | Angle/direction of first displacement |
| **Decentric Point** | 0.0 - 8.0 | 0.0 | Height position for second eccentricity (0=bottom, 8=top) |
| **Decentricity Amount** | 0.0+ | 0.0 | How far off-center to displace second point (0=none) |
| **Decentricity Angle** | 0.0 - TAU | 0.0 | Angle/direction of second displacement |
| **Position** | Any | (0,0,0) | XYZ position offset |

## Creative Usage Tips

### 🏺 Classic Pottery Shapes

**Simple Vase:**
1. **Profile Type**: 3 (Vase)
2. **Height**: 3.0
3. **Base Radius**: 0.4
4. **Radius 4** (middle): 0.7
5. **Top Radius**: 0.3
6. **Bulge**: 0.3
7. Result: Classic vase shape

**Wide Bowl:**
1. **Profile Type**: 6 (Bowl)
2. **Height**: 1.5
3. **Base Radius**: 0.2
4. **Top Radius**: 1.0
5. **Bulge**: 0.2
6. Result: Wide, shallow bowl

**Elegant Bottle:**
1. **Profile Type**: 1 (Cone)
2. **Height**: 4.0
3. **Base Radius**: 0.6
4. **Radius 1-3**: 0.6
5. **Radius 4-6**: 0.4
6. **Radius 7**: 0.2
7. **Top Radius**: 0.15
8. Result: Bottle with narrow neck

### 📐 Geometric Forms

**Perfect Cylinder:**
1. **Profile Type**: 0 (Cylinder)
2. **All radii**: 0.5 (same value)
3. **Height**: 2.0
4. Result: Perfect cylinder

**Cone:**
1. **Profile Type**: 1 (Cone)
2. **Base Radius**: 1.0
3. **Top Radius**: 0.0
4. **All middle radii**: Linear taper
5. Result: Perfect cone

**Sphere:**
1. **Profile Type**: 2 (Sphere)
2. **Base/Top Radius**: 1.0
3. **Height**: 2.0
4. Result: Perfect sphere

### 🌀 Complex Profile Control

**Hourglass Figure:**
1. **Profile Type**: 4 (Hourglass)
2. **Base Radius**: 0.6
3. **Top Radius**: 0.6
4. **Radius 4** (middle): 0.3
5. **Bulge**: 0.5
6. Result: Constricted middle

**Bulbous Form:**
1. **Profile Type**: 5 (Bulb)
2. **Base Radius**: 0.8
3. **Radius 1-2**: 0.9
4. **Radius 3-7**: Gradual taper to 0.3
5. **Top Radius**: 0.3
6. **Bulge**: 0.4
7. Result: Bulb/onion shape

**Custom Curved Profile:**
1. **Profile Type**: 0 (Cylinder - raw control)
2. Manually set each radius:
   - Base: 0.3
   - R1: 0.4
   - R2: 0.6
   - R3: 0.8
   - R4: 0.9
   - R5: 0.8
   - R6: 0.6
   - R7: 0.4
   - Top: 0.3
3. Result: Custom wave/curve profile

### ↗️ Eccentric/Asymmetric Forms

**Tilted Vase:**
1. Create basic vase (Profile Type 3)
2. **Eccentric Point**: 4.0 (middle)
3. **Eccentricity Amount**: 0.3
4. **Eccentricity Angle**: 0.0 (tilt in +X direction)
5. Result: Vase tilted to one side

**S-Curved Form:**
1. **Profile Type**: 0 (Cylinder)
2. **Eccentric Point**: 2.0 (lower third)
3. **Eccentricity Amount**: 0.2
4. **Eccentricity Angle**: 0.0
5. **Decentric Point**: 6.0 (upper third)
6. **Decentricity Amount**: 0.2
7. **Decentricity Angle**: 3.14 (opposite direction)
8. Result: S-curve snake form

**Warped Bowl:**
1. **Profile Type**: 6 (Bowl)
2. **Eccentric Point**: 8.0 (top)
3. **Eccentricity Amount**: 0.5
4. **Eccentricity Angle**: 0.785 (45°)
5. Result: Bowl tilted/warped at rim

**Organic Sculpture:**
1. Custom radius profile (varied radii)
2. **Eccentric Point**: 3.0
3. **Eccentricity Amount**: 0.4
4. **Eccentricity Angle**: 1.57
5. **Decentric Point**: 5.5
6. **Decentricity Amount**: 0.3
7. **Decentricity Angle**: 4.71
8. Result: Complex organic asymmetric form

### 🎨 Artistic Applications

**Architectural Column:**
1. **Profile Type**: 0 (Cylinder)
2. **Height**: 6.0
3. **Base Radius**: 0.5
4. **Radius 1-7**: Slight variations (0.48-0.52)
5. **Top Radius**: 0.5
6. Result: Column with subtle entasis

**Abstract Sculpture:**
1. **Profile Type**: 3 (Vase)
2. Extreme radius variations
3. **Bulge**: 1.0
4. **Eccentric Point**: 6.0
5. **Eccentricity Amount**: 0.8
6. Result: Dramatic twisted form

**Glassware:**
1. **Profile Type**: 1 (Cone)
2. **Height**: 2.5
3. **Base Radius**: 0.3
4. **Radius 1-4**: 0.5
5. **Radius 5-7**: Taper to 0.4
6. **Top Radius**: 0.4
7. Result: Wine glass stem and bowl

## Workflow Examples

### Example 1: Simple Clay Pot
1. Add **Body of Revolution**
2. **Profile Type**: 3 (Vase)
3. **Height**: 2.0
4. **Base Radius**: 0.3
5. **Radius 4**: 0.6
6. **Top Radius**: 0.5
7. **Bulge**: 0.2
8. Result: Traditional clay pot

### Example 2: Elegant Bottle
1. Add **Body of Revolution**
2. **Profile Type**: 0 (Cylinder - manual control)
3. **Height**: 4.0
4. **Base Radius**: 0.5
5. **Radius 1-3**: 0.5 (wide body)
6. **Radius 4-5**: 0.3 (shoulder)
7. **Radius 6-7**: 0.15 (neck)
8. **Top Radius**: 0.15
9. Result: Bottle with distinct sections

### Example 3: Perfect Sphere
1. Add **Body of Revolution**
2. **Profile Type**: 2 (Sphere)
3. **Height**: 2.0
4. **Base Radius**: 1.0
5. **Top Radius**: 1.0
6. Result: Perfect sphere (radius 1.0)

### Example 4: Hourglass
1. Add **Body of Revolution**
2. **Profile Type**: 4 (Hourglass)
3. **Height**: 3.0
4. **Base Radius**: 0.6
5. **Radius 4**: 0.2
6. **Top Radius**: 0.6
7. **Bulge**: 0.6
8. Result: Dramatic hourglass constriction

### Example 5: Tilted Vase
1. Add **Body of Revolution**
2. **Profile Type**: 3 (Vase)
3. **Base Radius**: 0.4
4. **Radius 4**: 0.7
5. **Top Radius**: 0.4
6. **Eccentric Point**: 5.0 (upper portion)
7. **Eccentricity Amount**: 0.4
8. **Eccentricity Angle**: 0.0
9. Result: Vase leaning to one side

### Example 6: Complex Organic Form
1. Add **Body of Revolution**
2. **Profile Type**: 0 (Cylinder)
3. Manually vary all 9 radii (wave pattern)
4. **Eccentric Point**: 2.5
5. **Eccentricity Amount**: 0.3
6. **Eccentricity Angle**: 1.0
7. **Decentric Point**: 6.0
8. **Decentricity Amount**: 0.25
9. **Decentricity Angle**: 4.0
10. Result: Complex twisted organic sculpture

### Example 7: Architectural Column Base
1. Add **Body of Revolution**
2. **Profile Type**: 0 (Cylinder)
3. **Height**: 1.5
4. **Base Radius**: 0.8
5. **Radius 1**: 0.7
6. **Radius 2-6**: 0.6
7. **Radius 7**: 0.65
8. **Top Radius**: 0.6
9. Result: Classical column base with torus

## Technical Details

- **Node Type**: 3D SDF Shape (vec3 → SignedDistance)
- **Category**: 3D Shapes / Surfaces of Revolution
- **Algorithm**: Parametric profile + rotational distance field
- **Control Points**: 9 radius points (0-8)
- **Profile Types**: 7 preset modifications
- **Eccentricity**: Dual independent off-center displacement
- **Caps**: Flat circular top and bottom
- **Rendering**: Signed Distance Field

## Understanding the Mathematics

### Surface of Revolution

**Basic Concept:**
```
For a 2D profile curve r(y):
- Rotate around Y-axis
- At any point (x, y, z):
  - Distance from Y-axis: d = sqrt(x² + z²)
  - Profile radius at height y: r(y)
  - SDF: distance = d - r(y)
```

### 9-Point Profile Interpolation

**Radius Control:**
```
9 points at heights: 0/8, 1/8, 2/8, ..., 8/8
Normalized height t ∈ [0, 1]
Segment = floor(t × 8)
Local t = fract(t × 8)
Radius = mix(radius[segment], radius[segment+1], local_t)
```

**Example:**
- At t=0.5 (middle): Segment 4, blends Radius 4 and Radius 5
- At t=0.25: Segment 2, blends Radius 2 and Radius 3

### Eccentricity Algorithm

**Dual Offset Calculation:**
```
For each point (Eccentric and Decentric):
1. Target height: point / 8.0 (maps 0-8 to 0-1)
2. Falloff: 1.0 - |current_height - target| × 8.0
3. Smooth falloff: smoothstep(0, 1, falloff)
4. Offset X: cos(angle) × amount × falloff
5. Offset Z: sin(angle) × amount × falloff
6. Combine: total_offset = offset1 + offset2
```

**Effect:**
- Maximum displacement at the eccentric point
- Gradual falloff ±1/8 height around point
- Smooth transitions via smoothstep
- Two independent offsets combine additively

### Profile Type Modifications

**Type 0 (Cylinder):**
```
radius = control_points(t)  // Raw interpolation
```

**Type 3 (Vase):**
```
base = control_points(t)
bulge_factor = sin(t × π) × bulge × base_radius
radius = base + bulge_factor
```

**Type 4 (Hourglass):**
```
base = control_points(t)
pinch = sin(t × π) × bulge × base_radius
radius = base - pinch
```

### Flat Caps

**Cap SDF:**
```
Top cap:
- Plane: y = height/2
- Circle: length(xz - offset) - top_radius
- Combined: max(circle_dist, y_dist)

Bottom cap:
- Plane: y = -height/2
- Circle: length(xz - offset) - base_radius
- Combined: max(circle_dist, -y_dist)
```

## Best Practices

### 🎯 Profile Design

**Start Simple:**
1. Begin with **Profile Type 0** (Cylinder)
2. Set all radii equal for basic shape
3. Gradually vary radii for desired profile
4. Switch to preset types for specific effects

**Smooth Profiles:**
- Avoid extreme jumps between adjacent radii
- Gradual changes create smooth surfaces
- Large jumps = visible ridges/steps

**Bulge Parameter:**
- Only affects types 3-6
- Start small (0.1-0.3)
- Extreme values (>1.0) can create unusual forms

### 💡 Radius Guidelines

**Proportions:**
- Base/Top radii: 0.3-1.0 for typical objects
- Middle radii: Vary smoothly
- Avoid zero radius (minimum 0.01 enforced)

**Common Patterns:**
- **Cylinder**: All radii equal
- **Cone**: Linear decrease from base to top
- **Vase**: Wider in middle
- **Bottle**: Wide base, narrow neck
- **Bowl**: Narrow base, wide top

### ↗️ Eccentricity Tips

**Subtle Asymmetry:**
- Amount: 0.1-0.3 for gentle tilt
- Single eccentric point for simple lean

**Dramatic Warping:**
- Amount: 0.5-1.0+ for extreme distortion
- Use both Eccentric and Decentric for S-curves

**Point Placement:**
- 0.0-2.0: Bottom third
- 3.0-5.0: Middle third
- 6.0-8.0: Top third
- Smooth slider control (0.000-8.000)

**Angle Control:**
- 0.0: +X direction
- 1.57 (π/2): +Z direction
- 3.14 (π): -X direction
- 4.71 (3π/2): -Z direction
- Full rotation: 0 to 6.28 (TAU)

### ⚠️ Common Mistakes

- ❌ All radii at 0.0 (no visible shape)
- ❌ Extreme radius variations (visible ridges)
- ❌ Eccentricity Amount too high (weird distortions)
- ❌ Height too small relative to radii (squashed)
- ❌ Forgetting flat caps are at radius endpoints

## Combining with Other Nodes

**Creative Combinations:**
- **🔄 Multiple Bodies of Revolution**: Different sizes, nested
- **📐 Boolean Operations**: Union, subtract, intersect
- **🎨 Materials**: Pottery glazes, glass, metal
- **💡 Deformers**: Further twist, bend
- **✨ Array/Duplicate**: Patterns of vessels

**Composition Ideas:**
- Stack multiple vases vertically
- Boolean subtract to create hollow vessels
- Array around circle for mandala patterns
- Combine with other primitives for hybrid forms

## Troubleshooting Guide

### Problem: Shape not visible
**Solutions**:
- ✅ Check all radii > 0.0
- ✅ Increase **Height** parameter
- ✅ Check **Position** offset
- ✅ Verify camera position

### Problem: Visible ridges/steps
**Solutions**:
- ✅ Smooth radius transitions between points
- ✅ Avoid large jumps between adjacent radii
- ✅ Use more gradual changes
- ✅ Check **Profile Type** - some add bulges

### Problem: Weird artifacts at top/bottom
**Solutions**:
- ✅ Caps are flat circles at Base/Top radius
- ✅ Ensure those radii are reasonable
- ✅ If caps look wrong, check extreme eccentricity
- ✅ Caps follow eccentricity offset

### Problem: Eccentricity too extreme
**Solutions**:
- ✅ Reduce **Amount** (try 0.2-0.5)
- ✅ Check **Point** placement (0.0-8.0 range)
- ✅ Angle might be unexpected direction
- ✅ Two eccentricities can combine unexpectedly

### Problem: Can't control eccentricity smoothly
**Solutions**:
- ✅ **Eccentric Point** is float (0.000-8.000)
- ✅ Slow slider movement for precision
- ✅ Values between integers work (e.g., 3.5)
- ✅ Full range allows smooth positioning

### Problem: Shape too tall/short
**Solutions**:
- ✅ Adjust **Height** parameter
- ✅ Height is independent of radii
- ✅ Aspect ratio = Height / (2 × Average Radius)
- ✅ Typical: Height 1.5-3× max radius

### Problem: Want rounded caps instead of flat
**Solutions**:
- ✅ Flat caps are by design (simpler, no artifacts)
- ✅ For rounded, use **Profile Type 2** (Sphere)
- ✅ Or manually taper radii near ends
- ✅ Combine with sphere primitive via boolean

## Advanced Techniques

### Multi-Point Eccentricity Patterns

**Spiral Form:**
1. **Eccentric Point**: 2.0
2. **Eccentricity Amount**: 0.3
3. **Eccentricity Angle**: 1.0
4. **Decentric Point**: 6.0
5. **Decentricity Amount**: 0.3
6. **Decentricity Angle**: 4.0 (opposite side)
7. Creates helical twist effect

### Complex Profile Sculpting

**Wave Pattern:**
1. Set radii in wave: 0.3, 0.5, 0.7, 0.9, 0.7, 0.5, 0.3, 0.5, 0.7
2. Creates undulating surface
3. Combine with eccentricity for organic forms

### Architectural Details

**Classical Column:**
1. **Base section**: Wider radii (0-2)
2. **Shaft**: Uniform radii (2-6) with subtle entasis
3. **Capital**: Wider radii (6-8)
4. Subtle **Eccentric Point** at 1.0, Amount 0.05 for imperfection

### Pottery Techniques

**Thrown Pottery Look:**
1. Slight random variations in radii
2. Very subtle eccentricity (Amount 0.05-0.1)
3. Creates handmade feel
4. Combine with material roughness

## Real-World Applications

### Product Design
- Bottles, vases, containers
- Glassware, ceramics
- Architectural elements

### Game Assets
- Pottery props
- Columns, pillars
- Abstract environment pieces

### Art & Sculpture
- Organic abstract forms
- Twisted sculptures
- Installation pieces

### Architecture Visualization
- Column capitals and bases
- Decorative elements
- Structural forms

## Why This Node Was Created

Bodies of revolution are fundamental 3D forms used across art, design, and engineering. **Body of Revolution** provides:

- ✅ **9 radius control points** for precise profile shaping
- ✅ **7 preset profile types** for quick results
- ✅ **Dual eccentricity** for asymmetric organic forms
- ✅ **Professional SDF rendering** for clean geometry
- ✅ **Real-time performance** for interactive design
- ✅ **Artistic freedom** from pottery to abstract sculpture

From classical pottery to futuristic abstract forms - all from rotating a curve!

## Credits

- Mathematical concept: Surfaces of revolution (classical geometry)
- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#body-of-revolution---documentation) | [Deutsch](#body-of-revolution---dokumentation)

---

# Body of Revolution - Dokumentation

## Übersicht

**Body of Revolution** (Rotationskörper) erstellt 3D-Formen durch Rotation einer 2D-Profilkurve um eine vertikale Achse. Dieser kraftvolle Node ermöglicht es Ihnen, alles von einfachen Zylindern bis zu komplexen Vasen, Flaschen, Schalen und abstrakten skulpturalen Formen mit präziser Kontrolle über die Profilform und asymmetrische Verzerrungen zu erstellen.

## 🎯 Inspiration & Design-Philosophie

Basierend auf dem mathematischen Konzept der Rotationsflächen:

- **Rotationssymmetrie**: 2D-Profil um 360° um Y-Achse rotiert
- **9 Kontrollpunkte**: Präzise Profil-Formung mit 9 Radiuspunkten
- **7 Profiltypen**: Von Basisformen bis organischen Formen
- **Duale Exzentrizität**: Zwei unabhängige Off-Center-Verschiebungspunkte
- **Professionelle Kontrolle**: Erstelle Töpferei, Architektur, abstrakte Kunst

Dieser Node bringt die klassische mathematische Rotationsfläche zu Coollab mit künstlerischer Flexibilität und technischer Präzision.

## ⭐ Hauptmerkmale

### 🔄 Rotationskonstruktion
Klassischer Rotationskörper:
- **Y-Achsen-Rotation**: Profil dreht sich um vertikale Achse
- **Kontinuierliche Oberfläche**: Glatte 360° Rotation
- **Signed Distance Field**: Professionelles SDF-Rendering
- **Echtzeit**: Interaktive Parameter-Anpassung

### 📐 9 Radius-Kontrollpunkte
Präzise Profil-Kontrolle:
- **Base Radius** (0/8): Unten
- **Radius 1-7**: Zwischenpunkte bei 1/8 bis 7/8 Höhe
- **Top Radius** (8/8): Oben
- **Lineare Interpolation**: Glatte Übergänge zwischen Punkten
- **Volle Kontrolle**: Forme jede Profilkurve

### 🎨 7 Profiltypen
Voreingestellte Profil-Modifikationen:
- **0 - Cylinder**: Gerade Seiten, nutzt Radiuspunkte wie sie sind
- **1 - Cone**: Lineares Verjüngen, nutzt Radiuspunkte direkt
- **2 - Sphere**: Kreisförmiges Profil (sphärische Form)
- **3 - Vase**: Glatte Wölbung in der Mitte
- **4 - Hourglass**: Einschnürung in der Mitte
- **5 - Bulb**: Wölbung unten, schmal oben
- **6 - Bowl**: Glatte Kurve, weit oben

### ↗️ Duale Exzentrizität
Zwei unabhängige Off-Center-Punkte:
- **Eccentric Point**: Erste Verschiebung (0.0-8.0 Bereich)
- **Decentric Point**: Zweite unabhängige Verschiebung (0.0-8.0 Bereich)
- **Amount-Kontrolle**: Wie weit off-center jede verschiebt
- **Winkel-Kontrolle**: Richtung der Verschiebung (0-TAU)
- **Glatter Abfall**: Gradueller Einfluss um jeden Punkt
- **Asymmetrische Formen**: Erstelle gekippte, verworfene, organische Formen

### 🎯 Flache Abschlüsse
Sauberer oberer und unterer Abschluss:
- **Top Cap**: Flacher kreisförmiger Deckel bei Top Radius
- **Bottom Cap**: Flacher kreisförmiger Deckel bei Base Radius
- **Keine Artefakte**: Saubere SDF-Mathematik
- **Exzentrizitäts-kompatibel**: Deckel folgen Exzentrizität

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Profile Type** | 0 - 6 | 0 | Formmodifikation: 0=Zylinder, 1=Kegel, 2=Kugel, 3=Vase, 4=Sanduhr, 5=Birne, 6=Schale |
| **Height** | 0.1+ | 2.0 | Gesamthöhe des Objekts |
| **Base Radius** | 0.01+ | 0.5 | Radius unten (0/8 Höhe) |
| **Radius 1** | 0.01+ | 0.5 | Radius bei 1/8 Höhe |
| **Radius 2** | 0.01+ | 0.5 | Radius bei 2/8 Höhe |
| **Radius 3** | 0.01+ | 0.5 | Radius bei 3/8 Höhe |
| **Radius 4** | 0.01+ | 0.5 | Radius bei 4/8 Höhe (Mitte) |
| **Radius 5** | 0.01+ | 0.5 | Radius bei 5/8 Höhe |
| **Radius 6** | 0.01+ | 0.5 | Radius bei 6/8 Höhe |
| **Radius 7** | 0.01+ | 0.5 | Radius bei 7/8 Höhe |
| **Top Radius** | 0.01+ | 0.5 | Radius oben (8/8 Höhe) |
| **Bulge** | 0.0 - 2.0 | 0.0 | Wölbungsstärke für Vase/Sanduhr/Birne/Schale-Profile |
| **Smoothness** | 0.01 - 0.99 | 0.5 | Kurven-Glätte (aktuell für Schalen-Profil) |
| **Eccentric Point** | 0.0 - 8.0 | 0.0 | Höhenposition für erste Exzentrizität (0=unten, 8=oben) |
| **Eccentricity Amount** | 0.0+ | 0.0 | Wie weit off-center erster Punkt verschoben wird (0=keine) |
| **Eccentricity Angle** | 0.0 - TAU | 0.0 | Winkel/Richtung der ersten Verschiebung |
| **Decentric Point** | 0.0 - 8.0 | 0.0 | Höhenposition für zweite Exzentrizität (0=unten, 8=oben) |
| **Decentricity Amount** | 0.0+ | 0.0 | Wie weit off-center zweiter Punkt verschoben wird (0=keine) |
| **Decentricity Angle** | 0.0 - TAU | 0.0 | Winkel/Richtung der zweiten Verschiebung |
| **Position** | Beliebig | (0,0,0) | XYZ-Positions-Verschiebung |

## 🎨 Kreative Nutzungstipps

### 🏺 Klassische Töpferformen

**Einfache Vase:**
1. **Profile Type**: 3 (Vase)
2. **Height**: 3.0
3. **Base Radius**: 0.4
4. **Radius 4** (Mitte): 0.7
5. **Top Radius**: 0.3
6. **Bulge**: 0.3
7. Ergebnis: Klassische Vasenform

**Breite Schale:**
1. **Profile Type**: 6 (Bowl)
2. **Height**: 1.5
3. **Base Radius**: 0.2
4. **Top Radius**: 1.0
5. **Bulge**: 0.2
6. Ergebnis: Breite, flache Schale

**Elegante Flasche:**
1. **Profile Type**: 0 (Cylinder - manuelle Kontrolle)
2. **Height**: 4.0
3. **Base Radius**: 0.6
4. **Radius 1-3**: 0.6 (breiter Körper)
5. **Radius 4-5**: 0.3 (Schulter)
6. **Radius 6-7**: 0.15 (Hals)
7. **Top Radius**: 0.15
8. Ergebnis: Flasche mit distinkten Sektionen

### 📐 Geometrische Formen

**Perfekter Zylinder:**
1. **Profile Type**: 0 (Cylinder)
2. **Alle Radien**: 0.5 (gleicher Wert)
3. **Height**: 2.0
4. Ergebnis: Perfekter Zylinder

**Kegel:**
1. **Profile Type**: 1 (Cone)
2. **Base Radius**: 1.0
3. **Top Radius**: 0.0
4. **Alle mittleren Radien**: Lineares Verjüngen
5. Ergebnis: Perfekter Kegel

**Kugel:**
1. **Profile Type**: 2 (Sphere)
2. **Base/Top Radius**: 1.0
3. **Height**: 2.0
4. Ergebnis: Perfekte Kugel

### 🌀 Komplexe Profil-Kontrolle

**Sanduhr-Figur:**
1. **Profile Type**: 4 (Hourglass)
2. **Base Radius**: 0.6
3. **Top Radius**: 0.6
4. **Radius 4** (Mitte): 0.3
5. **Bulge**: 0.5
6. Ergebnis: Eingeschnürte Mitte

**Birnenform:**
1. **Profile Type**: 5 (Bulb)
2. **Base Radius**: 0.8
3. **Radius 1-2**: 0.9
4. **Radius 3-7**: Graduelles Verjüngen zu 0.3
5. **Top Radius**: 0.3
6. **Bulge**: 0.4
7. Ergebnis: Birnen-/Zwiebelform

**Benutzerdefiniertes Gekurvtes Profil:**
1. **Profile Type**: 0 (Cylinder - rohe Kontrolle)
2. Manuell jeden Radius setzen:
   - Base: 0.3, R1: 0.4, R2: 0.6, R3: 0.8
   - R4: 0.9, R5: 0.8, R6: 0.6, R7: 0.4
   - Top: 0.3
3. Ergebnis: Benutzerdefiniertes Wellen-/Kurvenprofil

### ↗️ Exzentrische/Asymmetrische Formen

**Gekippte Vase:**
1. Erstellen Sie Basis-Vase (Profile Type 3)
2. **Eccentric Point**: 4.0 (Mitte)
3. **Eccentricity Amount**: 0.3
4. **Eccentricity Angle**: 0.0 (Kippen in +X Richtung)
5. Ergebnis: Vase zu einer Seite gekippt

**S-Kurven-Form:**
1. **Profile Type**: 0 (Cylinder)
2. **Eccentric Point**: 2.0 (unteres Drittel)
3. **Eccentricity Amount**: 0.2
4. **Eccentricity Angle**: 0.0
5. **Decentric Point**: 6.0 (oberes Drittel)
6. **Decentricity Amount**: 0.2
7. **Decentricity Angle**: 3.14 (entgegengesetzte Richtung)
8. Ergebnis: S-Kurven-Schlangenform

**Verworfene Schale:**
1. **Profile Type**: 6 (Bowl)
2. **Eccentric Point**: 8.0 (oben)
3. **Eccentricity Amount**: 0.5
4. **Eccentricity Angle**: 0.785 (45°)
5. Ergebnis: Schale gekippt/verworfen am Rand

**Organische Skulptur:**
1. Benutzerdefiniertes Radiusprofil (variierte Radien)
2. **Eccentric Point**: 3.0
3. **Eccentricity Amount**: 0.4
4. **Eccentricity Angle**: 1.57
5. **Decentric Point**: 5.5
6. **Decentricity Amount**: 0.3
7. **Decentricity Angle**: 4.71
8. Ergebnis: Komplexe organische asymmetrische Form

### 🎨 Künstlerische Anwendungen

**Architektonische Säule:**
1. **Profile Type**: 0 (Cylinder)
2. **Height**: 6.0
3. **Base Radius**: 0.5
4. **Radius 1-7**: Leichte Variationen (0.48-0.52)
5. **Top Radius**: 0.5
6. Ergebnis: Säule mit subtilem Entasis

**Abstrakte Skulptur:**
1. **Profile Type**: 3 (Vase)
2. Extreme Radius-Variationen
3. **Bulge**: 1.0
4. **Eccentric Point**: 6.0
5. **Eccentricity Amount**: 0.8
6. Ergebnis: Dramatische verdrehte Form

**Glaswaren:**
1. **Profile Type**: 1 (Cone)
2. **Height**: 2.5
3. **Base Radius**: 0.3
4. **Radius 1-4**: 0.5
5. **Radius 5-7**: Verjüngen zu 0.4
6. **Top Radius**: 0.4
7. Ergebnis: Weinglas-Stiel und Schale

## 💡 Workflow-Beispiele

### Beispiel 1: Einfacher Tontopf
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 3 (Vase)
3. **Height**: 2.0
4. **Base Radius**: 0.3
5. **Radius 4**: 0.6
6. **Top Radius**: 0.5
7. **Bulge**: 0.2
8. Ergebnis: Traditioneller Tontopf

### Beispiel 2: Elegante Flasche
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 0 (Cylinder - manuelle Kontrolle)
3. **Height**: 4.0
4. **Base Radius**: 0.5
5. **Radius 1-3**: 0.5 (breiter Körper)
6. **Radius 4-5**: 0.3 (Schulter)
7. **Radius 6-7**: 0.15 (Hals)
8. **Top Radius**: 0.15
9. Ergebnis: Flasche mit distinkten Sektionen

### Beispiel 3: Perfekte Kugel
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 2 (Sphere)
3. **Height**: 2.0
4. **Base Radius**: 1.0
5. **Top Radius**: 1.0
6. Ergebnis: Perfekte Kugel (Radius 1.0)

### Beispiel 4: Sanduhr
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 4 (Hourglass)
3. **Height**: 3.0
4. **Base Radius**: 0.6
5. **Radius 4**: 0.2
6. **Top Radius**: 0.6
7. **Bulge**: 0.6
8. Ergebnis: Dramatische Sanduhr-Einschnürung

### Beispiel 5: Gekippte Vase
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 3 (Vase)
3. **Base Radius**: 0.4
4. **Radius 4**: 0.7
5. **Top Radius**: 0.4
6. **Eccentric Point**: 5.0 (oberer Teil)
7. **Eccentricity Amount**: 0.4
8. **Eccentricity Angle**: 0.0
9. Ergebnis: Vase zu einer Seite geneigt

### Beispiel 6: Komplexe Organische Form
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 0 (Cylinder)
3. Manuell alle 9 Radien variieren (Wellenmuster)
4. **Eccentric Point**: 2.5
5. **Eccentricity Amount**: 0.3
6. **Eccentricity Angle**: 1.0
7. **Decentric Point**: 6.0
8. **Decentricity Amount**: 0.25
9. **Decentricity Angle**: 4.0
10. Ergebnis: Komplexe verdrehte organische Skulptur

### Beispiel 7: Architektonische Säulenbasis
1. Fügen Sie **Body of Revolution** hinzu
2. **Profile Type**: 0 (Cylinder)
3. **Height**: 1.5
4. **Base Radius**: 0.8
5. **Radius 1**: 0.7
6. **Radius 2-6**: 0.6
7. **Radius 7**: 0.65
8. **Top Radius**: 0.6
9. Ergebnis: Klassische Säulenbasis mit Torus

## 🔧 Technische Details

- **Node-Typ**: 3D SDF Shape (vec3 → SignedDistance)
- **Kategorie**: 3D Shapes / Rotationsflächen
- **Algorithmus**: Parametrisches Profil + Rotations-Distanzfeld
- **Kontrollpunkte**: 9 Radiuspunkte (0-8)
- **Profiltypen**: 7 voreingestellte Modifikationen
- **Exzentrizität**: Duale unabhängige Off-Center-Verschiebung
- **Abschlüsse**: Flache kreisförmige Ober- und Unterseite
- **Rendering**: Signed Distance Field

## 🧮 Verständnis der Mathematik

### Rotationsfläche

**Grundkonzept:**
```
Für eine 2D-Profilkurve r(y):
- Rotation um Y-Achse
- Bei jedem Punkt (x, y, z):
  - Distanz von Y-Achse: d = sqrt(x² + z²)
  - Profil-Radius bei Höhe y: r(y)
  - SDF: distance = d - r(y)
```

### 9-Punkt-Profil-Interpolation

**Radius-Kontrolle:**
```
9 Punkte bei Höhen: 0/8, 1/8, 2/8, ..., 8/8
Normalisierte Höhe t ∈ [0, 1]
Segment = floor(t × 8)
Lokales t = fract(t × 8)
Radius = mix(radius[segment], radius[segment+1], local_t)
```

**Beispiel:**
- Bei t=0.5 (Mitte): Segment 4, blendet Radius 4 und Radius 5
- Bei t=0.25: Segment 2, blendet Radius 2 und Radius 3

### Exzentrizitäts-Algorithmus

**Duale Offset-Berechnung:**
```
Für jeden Punkt (Eccentric und Decentric):
1. Ziel-Höhe: punkt / 8.0 (mappt 0-8 zu 0-1)
2. Abfall: 1.0 - |aktuelle_höhe - ziel| × 8.0
3. Glatter Abfall: smoothstep(0, 1, abfall)
4. Offset X: cos(winkel) × stärke × abfall
5. Offset Z: sin(winkel) × stärke × abfall
6. Kombinieren: total_offset = offset1 + offset2
```

**Effekt:**
- Maximale Verschiebung am exzentrischen Punkt
- Gradueller Abfall ±1/8 Höhe um Punkt
- Glatte Übergänge via smoothstep
- Zwei unabhängige Offsets kombinieren additiv

### Profiltyp-Modifikationen

**Typ 0 (Cylinder):**
```
radius = kontrollpunkte(t)  // Rohe Interpolation
```

**Typ 3 (Vase):**
```
basis = kontrollpunkte(t)
wölbungs_faktor = sin(t × π) × wölbung × basis_radius
radius = basis + wölbungs_faktor
```

**Typ 4 (Hourglass):**
```
basis = kontrollpunkte(t)
einschnürung = sin(t × π) × wölbung × basis_radius
radius = basis - einschnürung
```

### Flache Abschlüsse

**Abschluss-SDF:**
```
Oberer Abschluss:
- Ebene: y = höhe/2
- Kreis: length(xz - offset) - top_radius
- Kombiniert: max(kreis_dist, y_dist)

Unterer Abschluss:
- Ebene: y = -höhe/2
- Kreis: length(xz - offset) - base_radius
- Kombiniert: max(kreis_dist, -y_dist)
```

## 🎬 Best Practices

### 🎯 Profil-Design

**Einfach starten:**
1. Beginnen Sie mit **Profile Type 0** (Cylinder)
2. Setzen Sie alle Radien gleich für Basisform
3. Variieren Sie Radien graduell für gewünschtes Profil
4. Wechseln Sie zu Voreinstellungs-Typen für spezifische Effekte

**Glatte Profile:**
- Vermeiden Sie extreme Sprünge zwischen benachbarten Radien
- Graduelle Änderungen erzeugen glatte Oberflächen
- Große Sprünge = sichtbare Grate/Stufen

**Bulge-Parameter:**
- Betrifft nur Typen 3-6
- Klein starten (0.1-0.3)
- Extreme Werte (>1.0) können ungewöhnliche Formen erzeugen

### 💡 Radius-Richtlinien

**Proportionen:**
- Base/Top-Radien: 0.3-1.0 für typische Objekte
- Mittlere Radien: Glatt variieren
- Null-Radius vermeiden (Minimum 0.01 erzwungen)

**Häufige Muster:**
- **Zylinder**: Alle Radien gleich
- **Kegel**: Linearer Rückgang von Basis zu Spitze
- **Vase**: Breiter in der Mitte
- **Flasche**: Breite Basis, schmaler Hals
- **Schale**: Schmale Basis, breite Spitze

### ↗️ Exzentrizitäts-Tipps

**Subtile Asymmetrie:**
- Amount: 0.1-0.3 für sanfte Neigung
- Einzelner exzentrischer Punkt für einfache Schräge

**Dramatische Verwerfung:**
- Amount: 0.5-1.0+ für extreme Verzerrung
- Nutzen Sie beide Eccentric und Decentric für S-Kurven

**Punkt-Platzierung:**
- 0.0-2.0: Unteres Drittel
- 3.0-5.0: Mittleres Drittel
- 6.0-8.0: Oberes Drittel
- Glatte Slider-Kontrolle (0.000-8.000)

**Winkel-Kontrolle:**
- 0.0: +X Richtung
- 1.57 (π/2): +Z Richtung
- 3.14 (π): -X Richtung
- 4.71 (3π/2): -Z Richtung
- Volle Rotation: 0 bis 6.28 (TAU)

### ⚠️ Häufige Fehler

- ❌ Alle Radien bei 0.0 (keine sichtbare Form)
- ❌ Extreme Radius-Variationen (sichtbare Grate)
- ❌ Eccentricity Amount zu hoch (seltsame Verzerrungen)
- ❌ Height zu klein relativ zu Radien (gequetscht)
- ❌ Vergessen, dass flache Abschlüsse bei Radius-Endpunkten sind

## 🔗 Kombination mit anderen Nodes

**Kreative Kombinationen:**
- **🔄 Mehrere Bodies of Revolution**: Verschiedene Größen, verschachtelt
- **📐 Boolean-Operationen**: Union, Subtraktion, Schnittmenge
- **🎨 Materialien**: Töpferei-Glasuren, Glas, Metall
- **💡 Deformer**: Weitere Verdrehung, Biegung
- **✨ Array/Duplicate**: Muster von Gefäßen

**Kompositions-Ideen:**
- Mehrere Vasen vertikal stapeln
- Boolean-Subtraktion für hohle Gefäße
- Array um Kreis für Mandala-Muster
- Mit anderen Primitiven für Hybridformen kombinieren

## 🔧 Fehlerbehebungs-Guide

### Problem: Form nicht sichtbar
**Lösungen**:
- ✅ Prüfen Sie alle Radien > 0.0
- ✅ Erhöhen Sie **Height**-Parameter
- ✅ Prüfen Sie **Position**-Offset
- ✅ Verifizieren Sie Kamera-Position

### Problem: Sichtbare Grate/Stufen
**Lösungen**:
- ✅ Glätten Sie Radius-Übergänge zwischen Punkten
- ✅ Vermeiden Sie große Sprünge zwischen benachbarten Radien
- ✅ Nutzen Sie graduellere Änderungen
- ✅ Prüfen Sie **Profile Type** - einige fügen Wölbungen hinzu

### Problem: Seltsame Artefakte oben/unten
**Lösungen**:
- ✅ Abschlüsse sind flache Kreise bei Base/Top Radius
- ✅ Stellen Sie sicher, dass diese Radien vernünftig sind
- ✅ Falls Abschlüsse falsch aussehen, prüfen Sie extreme Exzentrizität
- ✅ Abschlüsse folgen Exzentrizitäts-Offset

### Problem: Exzentrizität zu extrem
**Lösungen**:
- ✅ Reduzieren Sie **Amount** (versuchen Sie 0.2-0.5)
- ✅ Prüfen Sie **Point**-Platzierung (0.0-8.0 Bereich)
- ✅ Winkel könnte unerwartete Richtung sein
- ✅ Zwei Exzentrizitäten können unerwartet kombinieren

### Problem: Kann Exzentrizität nicht glatt kontrollieren
**Lösungen**:
- ✅ **Eccentric Point** ist float (0.000-8.000)
- ✅ Langsame Slider-Bewegung für Präzision
- ✅ Werte zwischen Ganzzahlen funktionieren (z.B. 3.5)
- ✅ Voller Bereich erlaubt glatte Positionierung

### Problem: Form zu groß/klein
**Lösungen**:
- ✅ Passen Sie **Height**-Parameter an
- ✅ Height ist unabhängig von Radien
- ✅ Seitenverhältnis = Height / (2 × Durchschnittlicher Radius)
- ✅ Typisch: Height 1.5-3× maximaler Radius

### Problem: Möchte gerundete Abschlüsse statt flachen
**Lösungen**:
- ✅ Flache Abschlüsse sind by Design (einfacher, keine Artefakte)
- ✅ Für gerundet, nutzen Sie **Profile Type 2** (Sphere)
- ✅ Oder manuell Radien nahe Enden verjüngen
- ✅ Mit Kugel-Primitiv via Boolean kombinieren

## 🎓 Fortgeschrittene Techniken

### Multi-Punkt-Exzentrizitäts-Muster

**Spiralform:**
1. **Eccentric Point**: 2.0
2. **Eccentricity Amount**: 0.3
3. **Eccentricity Angle**: 1.0
4. **Decentric Point**: 6.0
5. **Decentricity Amount**: 0.3
6. **Decentricity Angle**: 4.0 (entgegengesetzte Seite)
7. Erzeugt helischen Verdrehungs-Effekt

### Komplexe Profil-Skulptur

**Wellenmuster:**
1. Setzen Sie Radien in Welle: 0.3, 0.5, 0.7, 0.9, 0.7, 0.5, 0.3, 0.5, 0.7
2. Erzeugt undulierende Oberfläche
3. Mit Exzentrizität für organische Formen kombinieren

### Architektonische Details

**Klassische Säule:**
1. **Basis-Sektion**: Breitere Radien (0-2)
2. **Schaft**: Einheitliche Radien (2-6) mit subtilem Entasis
3. **Kapitell**: Breitere Radien (6-8)
4. Subtiler **Eccentric Point** bei 1.0, Amount 0.05 für Unvollkommenheit

### Töpferei-Techniken

**Gedrehter Töpferei-Look:**
1. Leichte zufällige Variationen in Radien
2. Sehr subtile Exzentrizität (Amount 0.05-0.1)
3. Erzeugt handgemachtes Gefühl
4. Mit Material-Rauheit kombinieren

## 📚 Reale Anwendungen

### Produkt-Design
- Flaschen, Vasen, Behälter
- Glaswaren, Keramik
- Architektonische Elemente

### Game-Assets
- Töpferei-Requisiten
- Säulen, Pfeiler
- Abstrakte Umgebungs-Teile

### Kunst & Skulptur
- Organische abstrakte Formen
- Verdrehte Skulpturen
- Installations-Stücke

### Architektur-Visualisierung
- Säulen-Kapitelle und -Basen
- Dekorative Elemente
- Strukturelle Formen

## 💡 Warum dieser Node erstellt wurde

Rotationskörper sind fundamentale 3D-Formen, die in Kunst, Design und Ingenieurwesen genutzt werden. **Body of Revolution** bietet:

- ✅ **9 Radius-Kontrollpunkte** für präzise Profil-Formung
- ✅ **7 Voreinstellungs-Profiltypen** für schnelle Ergebnisse
- ✅ **Duale Exzentrizität** für asymmetrische organische Formen
- ✅ **Professionelles SDF-Rendering** für saubere Geometrie
- ✅ **Echtzeit-Performance** für interaktives Design
- ✅ **Künstlerische Freiheit** von Töpferei bis abstrakte Skulptur

Von klassischer Töpferei bis futuristischen abstrakten Formen - alles durch Rotation einer Kurve!

## 📜 Credits

- Mathematisches Konzept: Rotationsflächen (klassische Geometrie)
- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
