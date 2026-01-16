[English](#sine-warp-tile---documentation) | [Deutsch](#sine-warp-tile---dokumentation)

---

# Sine Warp Tile - Documentation

## Overview

**Sine Warp Tile** is a powerful 2D UV modifier that creates mesmerizing warping and tiling effects through sine wave distortions. Originally based on the VIDVOX ISF shader, this node transforms any image or pattern through mathematical warping, creating kaleidoscopic and psychedelic visual effects.

## Inspiration & Design Philosophy

This node demonstrates the beautiful intersection of mathematics and visual art:

- **Sine Wave Mathematics**: Uses trigonometric functions to create smooth, flowing distortions
- **Dual Rotation System**: Two separate rotation parameters (Rotation and Angle) allow for complex layered effects
- **Tiling Through Warping**: The sine distortion creates natural repetition and symmetry
- **Real-time Manipulation**: All parameters can be animated for dynamic, evolving visuals

The combination of these elements creates effects that range from subtle wave-like distortions to mind-bending kaleidoscopic transformations.

## Key Features

### 🌊 Sine Wave Distortion
The core of this node is its sine-based coordinate transformation:
- Creates smooth, organic warping patterns
- Natural tiling effect emerges from the mathematical periodicity
- Adjustable scale controls the frequency of waves

### 🔄 Dual Rotation System
Two independent rotation controls offer unprecedented creative flexibility:
- **Rotation**: Rotates the pattern before the sine distortion is applied
- **Angle**: Rotates the final warped result
- Combined, these create spiraling, twisting effects impossible with single rotation

### 📍 Shift Control
The Shift parameter (Point2D) allows you to:
- Reposition the center point of the effect
- Create asymmetric variations
- Animate the origin for flowing movements

### ⚙️ Precise Size Control
Ultra-fine size adjustment (0.001 - 0.5 range) enables:
- From subtle waves to intense warping
- Precise control over tiling density
- Fine-tuning for perfect visual balance

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Size** | 0.001 - 0.5 | 0.25 | Controls the scale/frequency of the sine wave distortion. Smaller values create tighter, more frequent waves. |
| **Rotation** | 0.0 - 1.0 | 0.0 | Rotates the pattern before applying the sine warp. Value of 1.0 = 360° rotation. |
| **Angle** | 0.0 - 1.0 | 0.0 | Rotates the warped result. Creates spiral and twisted effects when combined with Rotation. |
| **Shift** | Point2D | (0.5, 0.5) | Moves the center point of the effect. Use for asymmetric variations or animated flows. |

## Creative Usage Tips

### 🌟 Combining with 2D Modifiers

Sine Warp Tile becomes exponentially more powerful when combined with other **2D Modifier** nodes:

**Highly Recommended Combinations:**
- **⭐ Star Symmetry**: Creates mandala-like patterns with radial symmetry
- **🌀 Warping Illusionary**: Stack multiple warp effects for impossible geometries
- **🔮 Kaleidoscope nodes**: Generate hypnotic symmetric patterns from the warped base
- **🎨 Color Modifiers**: Apply after warping to color the distorted patterns
- **📐 Polar Coordinates**: Transform linear waves into circular, radial designs

**Experimental Suggestions:**
- Try multiple Sine Warp Tile nodes in sequence for fractal-like complexity
- Combine with displacement maps for textured distortions
- Use with feedback loops for evolving, organic animations

### 🎬 Animation Ideas

All parameters are perfect for animation:

1. **Flowing Waves**: Animate Size smoothly for breathing, pulsing effects
2. **Spinning Vortex**: Slowly increase Rotation or Angle over time
3. **Drifting Center**: Animate Shift in circular or figure-8 patterns
4. **Combined Motion**: Animate all parameters simultaneously for chaotic beauty

### 🖼️ Image Processing

When applied to images:
- **Portraits**: Create surreal, dreamlike distortions
- **Landscapes**: Transform into abstract art
- **Textures**: Generate unique tileable patterns
- **Video**: Apply for psychedelic music video effects

### 🔮 Converting to 3D

While primarily a 2D effect, you can use it creatively with **"3D Shape from 2D"**:

#### 📐 With Extrude Node
1. Create a pattern or gradient as base
2. Apply Sine Warp Tile
3. Convert to 3D with Extrude
4. Result: Sculptural, wave-like 3D forms

**Tips for 3D:**
- Keep Size moderate (0.2-0.3) to avoid too much chaos
- Use subtle Rotation values for recognizable forms
- Combine with 3D Modifiers like Twist or Bend for organic sculptures

## Technical Details

- **Node Type**: 2D Modifier (UV → UV)
- **Category**: 2D Modifier
- **Algorithm**: Sine wave coordinate transformation with dual rotation
- **Performance**: Very fast, suitable for real-time use
- **Based on**: VIDVOX ISF "Sine Warp Tile" shader

## Workflow Examples

### Example 1: Simple Wave Pattern
1. Start with a "Color Ramp"node or any gradient and link that to the Saturation on a "Color HSL" node
2. Add Sine Warp Tile
3. Set Size to 0.2
4. Adjust Rotation slowly to find interesting angles
5. Add color effects to enhance the pattern
6. You can then animate the "Angel" and "Rotate" options using a Time node, and additionally also the X and/or Y shift of the "Sine Warp Tile".

### Example 2: Kaleidoscope Effect
1. Create or import an image
2. Apply Sine Warp Tile with Size: 0.15
3. Add Star Symmetry node (8 or 12 segments)
4. Fine-tune Angle for perfect alignment
5. Result: Mesmerizing mandala patterns

### Example 3: Animated Vortex
1. Start with a textured image
2. Add Sine Warp Tile
3. Set Size: 0.25, Rotation: 0.25
4. Animate Angle from 0 to 1 over time
5. Add color grading for dramatic effect

### Example 4: Dual Warp Complexity
1. Apply Sine Warp Tile (Size: 0.3, Rotation: 0.0)
2. Add a second Sine Warp Tile (Size: 0.15, Rotation: 0.5)
3. Adjust both Angle parameters independently
4. Creates intricate, fractal-like patterns

## Parameter Interaction

Understanding how parameters interact is key to mastering this node:

- **Size + Rotation**: Small Size with high Rotation creates tight spirals
- **Rotation + Angle**: Different values create asymmetric, flowing patterns
- **Size + Shift**: Moving Shift with small Size reveals hidden symmetries
- **All Four**: Maximum creative freedom, can produce infinite variations

## Creative Freedom

Sine Warp Tile is a playground for experimentation:
- 🎲 Try extreme Size values (0.001 or 0.5) for surprising results
- 🔄 Rotate both parameters in opposite directions
- 🎯 Use Shift to break symmetry intentionally
- 🌈 Layer multiple instances with different blend modes
- ⚡ Animate everything for constantly evolving visuals

**Let your creativity flow like sine waves!** 🌊✨

## Credits

- Inspired by VIDVOX-ISFs from the MIT-Repository
- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#sine-warp-tile---documentation) | [Deutsch](#sine-warp-tile---dokumentation)

---

# Sine Warp Tile - Dokumentation

## Übersicht

**Sine Warp Tile** ist ein leistungsstarker 2D UV-Modifier, der faszinierende Verzerrungs- und Kacheleffekte durch Sinuswellen-Distortion erzeugt. Ursprünglich basierend auf dem VIDVOX ISF-Shader, transformiert dieser Node jedes Bild oder Muster durch mathematische Verzerrung und erschafft kaleidoskopische und psychedelische visuelle Effekte.

## 🎯 Inspiration & Design-Philosophie

Dieser Node demonstriert die schöne Verbindung von Mathematik und visueller Kunst:

- **Sinuswellen-Mathematik**: Nutzt trigonometrische Funktionen für glatte, fließende Verzerrungen
- **Duales Rotationssystem**: Zwei separate Rotationsparameter (Rotation und Angle) ermöglichen komplexe, geschichtete Effekte
- **Kachelung durch Verzerrung**: Die Sinus-Distortion erzeugt natürliche Wiederholung und Symmetrie
- **Echtzeit-Manipulation**: Alle Parameter können für dynamische, sich entwickelnde Visuals animiert werden

Die Kombination dieser Elemente erzeugt Effekte, die von subtilen wellenartigen Verzerrungen bis zu bewusstseinserweiternden kaleidoskopischen Transformationen reichen.

## ⭐ Hauptmerkmale

### 🌊 Sinuswellen-Verzerrung
Der Kern dieses Nodes ist seine sinus-basierte Koordinatentransformation:
- Erzeugt glatte, organische Verzerrungsmuster
- Natürlicher Kacheleffekt entsteht aus der mathematischen Periodizität
- Anpassbare Skalierung steuert die Frequenz der Wellen

### 🔄 Duales Rotationssystem
Zwei unabhängige Rotationssteuerungen bieten beispiellose kreative Flexibilität:
- **Rotation**: Rotiert das Muster, bevor die Sinus-Verzerrung angewendet wird
- **Angle**: Rotiert das finale verzerrte Ergebnis
- Kombiniert erzeugen diese spiralförmige, verdrehte Effekte, die mit einfacher Rotation unmöglich wären

### 📍 Shift-Steuerung
Der Shift-Parameter (Point2D) ermöglicht es:
- Den Mittelpunkt des Effekts neu zu positionieren
- Asymmetrische Variationen zu erstellen
- Den Ursprung für fließende Bewegungen zu animieren

### ⚙️ Präzise Größensteuerung
Ultra-feine Größenanpassung (0.001 - 0.5 Bereich) ermöglicht:
- Von subtilen Wellen bis zu intensiver Verzerrung
- Präzise Kontrolle über Kacheldichte
- Feinabstimmung für perfekte visuelle Balance

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Size** | 0.001 - 0.5 | 0.25 | Steuert die Skalierung/Frequenz der Sinuswellen-Verzerrung. Kleinere Werte erzeugen engere, häufigere Wellen. |
| **Rotation** | 0.0 - 1.0 | 0.0 | Rotiert das Muster vor Anwendung der Sinus-Verzerrung. Wert von 1.0 = 360° Rotation. |
| **Angle** | 0.0 - 1.0 | 0.0 | Rotiert das verzerrte Ergebnis. Erzeugt Spiral- und Verdrehungseffekte in Kombination mit Rotation. |
| **Shift** | Point2D | (0.5, 0.5) | Verschiebt den Mittelpunkt des Effekts. Nutzen für asymmetrische Variationen oder animierte Flows. |

## 🎨 Kreative Nutzungstipps

### 🌟 Kombination mit 2D Modifiern

Sine Warp Tile wird exponentiell mächtiger in Kombination mit anderen **2D Modifier**-Nodes:

**Sehr empfohlene Kombinationen:**
- **⭐ Star Symmetry**: Erzeugt mandala-artige Muster mit radialer Symmetrie
- **🌀 Warping Illusionary**: Stapelt mehrere Warp-Effekte für unmögliche Geometrien
- **🔮 Kaleidoskop-Nodes**: Generieren hypnotische symmetrische Muster aus der verzerrten Basis
- **🎨 Farbmodifier**: Nach der Verzerrung anwenden, um die verzerrten Muster einzufärben
- **📐 Polar Coordinates**: Transformiert lineare Wellen in kreisförmige, radiale Designs

**Experimentelle Vorschläge:**
- Versuchen Sie mehrere Sine Warp Tile Nodes nacheinander für fraktalartige Komplexität
- Kombinieren Sie mit Displacement Maps für texturierte Verzerrungen
- Nutzen Sie Feedback-Schleifen für sich entwickelnde, organische Animationen

### 🎬 Animations-Ideen

Alle Parameter sind perfekt für Animation:

1. **🌊 Fließende Wellen**: Animieren Sie Size sanft für atmende, pulsierende Effekte
2. **🌀 Wirbelnder Vortex**: Erhöhen Sie Rotation oder Angle langsam über Zeit
3. **📍 Driftender Mittelpunkt**: Animieren Sie Shift in kreisförmigen oder Achter-Mustern
4. **🎭 Kombinierte Bewegung**: Animieren Sie alle Parameter gleichzeitig für chaotische Schönheit

### 🖼️ Bildverarbeitung

Bei Anwendung auf Bilder:
- **👤 Portraits**: Erzeugen Sie surreale, traumartige Verzerrungen
- **🏞️ Landschaften**: Verwandeln Sie in abstrakte Kunst
- **🎨 Texturen**: Generieren Sie einzigartige kachelbare Muster
- **🎬 Video**: Anwenden für psychedelische Musikvideo-Effekte

### 🔮 Umwandlung in 3D

Obwohl primär ein 2D-Effekt, können Sie ihn kreativ mit **"3D Shape from 2D"** nutzen:

#### 📐 Mit Extrude Node
1. Erstellen Sie ein Muster oder Gradient als Basis
2. Wenden Sie Sine Warp Tile an
3. Konvertieren Sie mit Extrude zu 3D
4. Ergebnis: Skulpturale, wellenartige 3D-Formen

**Tipps für 3D:**
- Halten Sie Size moderat (0.2-0.3), um zu viel Chaos zu vermeiden
- Nutzen Sie subtile Rotation-Werte für erkennbare Formen
- Kombinieren Sie mit 3D Modifiern wie Twist oder Bend für organische Skulpturen

## 🔧 Technische Details

- **Node-Typ**: 2D Modifier (UV → UV)
- **Kategorie**: 2D Modifier
- **Algorithmus**: Sinuswellen-Koordinatentransformation mit dualer Rotation
- **Performance**: Sehr schnell, geeignet für Echtzeit-Nutzung
- **Basiert auf**: VIDVOX ISF "Sine Warp Tile" Shader

## 💡 Workflow-Beispiele

### Beispiel 1: Einfaches Wellenmuster
1. Beginnen Sie mit einem Gradient oder Volltonfarbe
2. Fügen Sie Sine Warp Tile hinzu
3. Setzen Sie Size auf 0.2
4. Passen Sie Rotation langsam an, um interessante Winkel zu finden
5. Fügen Sie Farbeffekte hinzu, um das Muster zu verstärken

### Beispiel 2: Kaleidoskop-Effekt
1. Erstellen oder importieren Sie ein Bild
2. Wenden Sie Sine Warp Tile mit Size: 0.15 an
3. Fügen Sie Star Symmetry Node hinzu (8 oder 12 Segmente)
4. Feinabstimmung von Angle für perfekte Ausrichtung
5. Ergebnis: Hypnotische Mandala-Muster

### Beispiel 3: Animierter Vortex
1. Beginnen Sie mit einem texturierten Bild
2. Fügen Sie Sine Warp Tile hinzu
3. Setzen Sie Size: 0.25, Rotation: 0.25
4. Animieren Sie Angle von 0 bis 1 über Zeit
5. Fügen Sie Color Grading für dramatischen Effekt hinzu

### Beispiel 4: Doppelte Warp-Komplexität
1. Wenden Sie Sine Warp Tile an (Size: 0.3, Rotation: 0.0)
2. Fügen Sie einen zweiten Sine Warp Tile hinzu (Size: 0.15, Rotation: 0.5)
3. Passen Sie beide Angle-Parameter unabhängig an
4. Erzeugt komplexe, fraktalartige Muster

## 🔄 Parameter-Interaktion

Das Verstehen der Parameter-Interaktionen ist der Schlüssel zur Beherrschung dieses Nodes:

- **Size + Rotation**: Kleine Size mit hoher Rotation erzeugt enge Spiralen
- **Rotation + Angle**: Unterschiedliche Werte erzeugen asymmetrische, fließende Muster
- **Size + Shift**: Verschieben von Shift mit kleiner Size enthüllt versteckte Symmetrien
- **Alle Vier**: Maximale kreative Freiheit, kann unendliche Variationen produzieren

## 🎭 Kreative Freiheit

Sine Warp Tile ist ein Spielplatz für Experimente:
- 🎲 Probieren Sie extreme Size-Werte (0.001 oder 0.5) für überraschende Ergebnisse
- 🔄 Rotieren Sie beide Parameter in entgegengesetzte Richtungen
- 🎯 Nutzen Sie Shift, um Symmetrie absichtlich zu brechen
- 🌈 Schichten Sie mehrere Instanzen mit verschiedenen Blend-Modi
- ⚡ Animieren Sie alles für sich ständig entwickelnde Visuals

**Lassen Sie Ihrer Kreativität freien Lauf wie Sinuswellen!** 🌊✨

## 📜 Credits

- Inspiriert von VIDVOX-ISFs aus dem MIT-Repository
- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
