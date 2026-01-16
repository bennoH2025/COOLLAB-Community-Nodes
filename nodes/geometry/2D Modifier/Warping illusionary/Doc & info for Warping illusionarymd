[English](#warping-illusionary---documentation) | [Deutsch](#warping-illusionary---dokumentation)

---

# Warping Illusionary - Documentation

## Overview

**Warping Illusionary** is a sophisticated 2D UV modifier that combines two powerful warping techniques into one creative powerhouse. By layering **Power Curve distortions** with **Sine Wave warping**, this node creates impossible geometries and mind-bending visual illusions that push the boundaries of what seems physically possible.

## Inspiration & Design Philosophy

This node was born from the fusion of two distinct VIDVOX ISF shaders:

- **Power Warp**: Exponential distortions that compress and stretch space
- **Sine Warp Tile**: Trigonometric transformations that create flowing patterns

The genius lies in the **layered approach**: first, space is bent through power curves, then the already-warped coordinates are subjected to sine wave distortions. This creates effects that neither technique could achieve alone—truly illusionary warping that defies expectations.

### Why "Illusionary"?

The name reflects the node's ability to create visuals that seem impossible:
- Spaces that fold in on themselves
- Surfaces that appear to ripple in multiple dimensions
- Patterns that simultaneously expand and contract
- Geometries that shouldn't exist in Euclidean space

## Key Features

### 🔮 Dual-Layer Warping System
The node applies effects in sequence:
1. **Power Warp** reshapes the coordinate space exponentially
2. **Sine Warp** flows through the already-distorted space
3. Result: Complex, unpredictable, beautiful chaos

### ⚡ Power Curve Distortion
Exponential transformations on X and Y axes independently:
- **Linear Mode**: Simple exponential curve from origin
- **Symmetric Mode**: Mirror the distortion from the center
- Creates compression, expansion, and barrel/pincushion effects

### 🌊 Sine Wave Integration
Multi-parameter sine distortion with:
- Adjustable scale (frequency)
- Variable strength (amplitude)
- Rotation before and after warping
- Shift with automatic wrapping

### 🎯 Unprecedented Control
Nine parameters working in concert:
- 2 Power parameters (X, Y)
- 2 Symmetry toggles
- 2 Sine parameters (Scale, Strength)
- 2 Rotation parameters
- 1 Shift control (Point2D)

## Parameters

| Parameter | Type | Range/Default | Description |
|-----------|------|---------------|-------------|
| **Sine Scale** | float | 0.001 - 1.0 (default: 0.25) | Controls the frequency of the sine wave distortion. Lower values = tighter waves. |
| **Sine Strength** | float | 0.0 - 2.0 (default: 0.5) | Controls the amplitude/intensity of the sine warp effect. |
| **Power X** | float | 0.25 - 4.0 (default: 1.0) | Exponential distortion strength on X axis. Values < 1 expand, > 1 compress. |
| **Power Y** | float | 0.25 - 4.0 (default: 1.0) | Exponential distortion strength on Y axis. Independent from X. |
| **Symmetric X** | bool | false | If true, mirrors the power curve from center on X axis. |
| **Symmetric Y** | bool | false | If true, mirrors the power curve from center on Y axis. |
| **Rotation** | float | 0.0 - 1.0 (default: 0.0) | Rotates the pattern before sine distortion. 1.0 = 360°. |
| **Angle** | float | 0.0 - 1.0 (default: 0.0) | Rotates the final warped result. Creates spiral effects. |
| **Shift** | Point2D | (0.0, 0.0) | Shifts the pattern with automatic wrapping. Useful for animation. |

## Creative Usage Tips

### 🌟 Understanding Parameter Interactions

The power of this node comes from parameter combinations:

**Power + Sine Synergy:**
- High Power X + Low Sine Scale = Compressed wavy patterns
- Symmetric mode + High Sine Strength = Radial wave explosions
- Asymmetric Power + Rotation = Spiral compression tunnels

**Rotation Layering:**
- Different Rotation + Angle values create complex spirals
- Same values = simple rotation (less interesting)
- Opposite directions (0.25 vs 0.75) = counter-rotating effects

**Shift Magic:**
- Animate Shift in circles for orbiting patterns
- Combine with high Sine Strength for liquid flows
- Use with Symmetric mode for kaleidoscopic shifts

### 🎨 Combining with Other 2D Modifiers

**Warping Illusionary** becomes exponentially more powerful when stacked:

**Highly Recommended Combinations:**
- **⭐ Star Symmetry**: Apply after warping for psychedelic mandalas
- **🔮 Another Warping Illusionary**: Stack two instances with different settings for fractal complexity
- **🌀 Sine Warp Tile**: Yes, even more sine warping! Creates multi-frequency patterns
- **📐 Polar Coordinates**: Transform the warped cartesian space into circular
- **🎨 Color Gradient Maps**: Map colors to the distorted space for painterly effects

**For Extreme Results:**
- Try 3+ Warping Illusionary nodes in sequence
- Alternate symmetric and asymmetric modes
- Vary Power values dramatically between instances
- Use feedback loops for evolving, organic chaos

### 🎬 Animation Strategies

Every parameter is animation-ready:

**Subtle Animations:**
- Slowly vary Sine Scale (0.2 - 0.3) for breathing effect
- Gentle Shift circular motion for flowing movement
- Gradual Power changes (0.8 - 1.2) for pulsing

**Dramatic Animations:**
- Spin Rotation continuously (0 to 1 loop)
- Ramp Sine Strength (0 to 2) for intensity builds
- Toggle Symmetric modes for sudden transformations

**Synchronized Animations:**
- Link Rotation and Angle to music beats
- Tie Sine Strength to audio amplitude
- Modulate Power with LFOs for rhythmic warping

### 🖼️ Application Examples

**For Abstract Art:**
- Start with gradients
- Use extreme Power values (0.25 or 4.0)
- High Sine Strength (1.5+)
- Animate slowly for meditative motion

**For Psychedelic Effects:**
- Apply to photos or video
- Moderate Power (1.2 - 1.8)
- High Sine Scale (0.8+) for fine detail
- Add Star Symmetry afterward

**For Glitch Art:**
- Rapid Shift animations
- Toggle Symmetric modes rapidly
- Extreme parameter combinations
- Layer with feedback and color effects

**For Music Videos:**
- Link all parameters to audio features
- Use as transition effect between scenes
- Apply to text and graphics
- Combine with color modulation

### 🔮 Converting to 3D

While primarily 2D, creative 3D workflows exist:

#### 📐 With Extrude Node
1. Create a base pattern or import texture
2. Apply Warping Illusionary (moderate settings)
3. Convert to 3D with Extrude (Height: 0.2 - 0.5)
4. Result: Sculptural forms with flowing topology

**Recommended Settings for 3D:**
- Sine Scale: 0.3 - 0.5 (not too chaotic)
- Power X/Y: 1.0 - 1.5 (subtle distortion)
- Sine Strength: 0.3 - 0.7 (enough detail, not overwhelming)
- Use Symmetric modes for recognizable forms

#### 🔄 With Revolve Node
- Creates cylindrical warped forms
- Best with asymmetric Power curves
- Can produce vase-like or organic structures
- Combine with 3D Bend/Twist for extra complexity

**After 3D Conversion:**
- Apply 3D Modifiers (Twist, Bend, Repetition)
- Experiment with different lighting angles
- Use metallic or glass materials for stunning results

## Technical Details

- **Node Type**: 2D Modifier (UV → UV)
- **Category**: 2D Modifier
- **Algorithm**: Sequential power curve and sine wave coordinate transformations
- **Performance**: Moderate (two-pass processing)
- **Based on**: Fusion of VIDVOX ISF "Power Warp" and "Sine Warp Tile"

## Workflow Examples

### Example 1: Impossible Architecture
1. Start with a grid pattern or photograph of building
2. Apply Warping Illusionary
3. Set Power X: 1.5, Power Y: 0.7, Symmetric both: true
4. Sine Scale: 0.4, Sine Strength: 0.6
5. Adjust Rotation and Angle to taste
6. Result: M.C. Escher-like impossible structures

### Example 2: Liquid Metal
1. Begin with metallic gradient or texture
2. Warping Illusionary with Power X/Y: 1.2
3. Sine Strength: 1.0, Sine Scale: 0.25
4. Animate Shift in circular pattern
5. Animate Rotation slowly
6. Result: Flowing liquid metal effect

### Example 3: Portal Effect
1. Create radial gradient or spiral
2. Warping Illusionary: Symmetric X/Y: true
3. Power X/Y: 2.0, Sine Scale: 0.15
4. Animate Angle continuously (0 to 1 loop)
5. Add color effects and glow
6. Result: Swirling vortex portal

### Example 4: Fractal Complexity
1. Apply first Warping Illusionary: Power X: 1.5, Sine: 0.3
2. Add second Warping Illusionary: Power Y: 1.5, Sine: 0.2
3. Add third with Symmetric modes: Power: 2.0, Sine: 0.15
4. Fine-tune Shift and Rotation on each
5. Result: Mind-bending fractal-like patterns

### Example 5: Glitch Transition
1. Start with video or image sequence
2. Warping Illusionary at keyframe A: All defaults (Power: 1.0)
3. At keyframe B: Power X/Y: 3.0, Sine Strength: 2.0
4. Animate between A and B quickly (0.5 seconds)
5. Result: Explosive glitch transition

## Understanding the Illusion

The "illusionary" quality comes from perceptual contradictions:

- **Spatial Impossibility**: Power curves compress one area while sine waves expand it—the eye can't reconcile this
- **Directional Ambiguity**: Multiple rotation parameters create surfaces that seem to twist in contradictory directions
- **Scale Confusion**: The combination makes it impossible to judge the "true" size or distance of elements
- **Symmetry Breaking**: Symmetric power with asymmetric sine creates patterns that are almost—but not quite—regular

This cognitive dissonance is what makes the warping truly "illusionary."

## Tips for Mastery

**Start Simple:**
1. Begin with Power parameters only (Sine Scale: 0, Sine Strength: 0)
2. Understand power curves first
3. Then add sine warping gradually
4. Build complexity layer by layer

**Experimentation Protocol:**
1. Try extreme values first to understand parameter range
2. Find interesting "accidents"
3. Refine toward your vision
4. Save presets of discoveries

**Performance Optimization:**
- Lower Sine Scale = fewer calculations = better performance
- Moderate Sine Strength < 1.0 for real-time use
- Extreme Power values (< 0.5 or > 3.0) can cause edge artifacts

## Creative Freedom

Warping Illusionary is limitless:
- 🎲 Randomize all parameters for happy accidents
- 🔄 Stack 5+ instances for absolute chaos
- 🎯 Animate everything simultaneously for maximum dynamics
- 🌈 Combine with every other modifier in Coollab
- ⚡ Push parameters to extremes—break the illusion!

**Let impossibility become your canvas!** 🔮✨

## Credits

- Inspired by VIDVOX-ISFs from the MIT-Repository
- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#warping-illusionary---documentation) | [Deutsch](#warping-illusionary---dokumentation)

---

# Warping Illusionary - Dokumentation

## Übersicht

**Warping Illusionary** ist ein ausgeklügelter 2D UV-Modifier, der zwei mächtige Verzerrungs-Techniken zu einem kreativen Kraftpaket kombiniert. Durch die Schichtung von **Power-Curve-Verzerrungen** mit **Sinuswellen-Warping** erzeugt dieser Node unmögliche Geometrien und bewusstseinsverändernde visuelle Illusionen, die die Grenzen des physikalisch Möglichen sprengen.

## 🎯 Inspiration & Design-Philosophie

Dieser Node entstand aus der Fusion zweier verschiedener VIDVOX ISF-Shader:

- **Power Warp**: Exponentielle Verzerrungen, die den Raum komprimieren und dehnen
- **Sine Warp Tile**: Trigonometrische Transformationen, die fließende Muster erzeugen

Das Geniale liegt im **geschichteten Ansatz**: Zuerst wird der Raum durch Power Curves gebogen, dann werden die bereits verzerrten Koordinaten Sinuswellen-Verzerrungen unterworfen. Dies erzeugt Effekte, die keine der beiden Techniken allein erreichen könnte—wahrhaft illusionäres Warping, das Erwartungen trotzt.

### Warum "Illusionary"?

Der Name spiegelt die Fähigkeit des Nodes wider, Visuals zu erzeugen, die unmöglich erscheinen:
- Räume, die sich in sich selbst falten
- Oberflächen, die in mehreren Dimensionen zu wellen scheinen
- Muster, die sich gleichzeitig ausdehnen und zusammenziehen
- Geometrien, die im euklidischen Raum nicht existieren sollten

## ⭐ Hauptmerkmale

### 🔮 Dual-Layer Warping-System
Der Node wendet Effekte sequenziell an:
1. **Power Warp** formt den Koordinatenraum exponentiell um
2. **Sine Warp** fließt durch den bereits verzerrten Raum
3. Ergebnis: Komplexes, unvorhersehbares, wunderschönes Chaos

### ⚡ Power-Curve-Verzerrung
Exponentielle Transformationen auf X- und Y-Achse unabhängig:
- **Linear-Modus**: Einfache exponentielle Kurve vom Ursprung
- **Symmetric-Modus**: Spiegelt die Verzerrung vom Zentrum
- Erzeugt Kompression, Expansion und Tonnen-/Nadelkissen-Effekte

### 🌊 Sinuswellen-Integration
Multi-Parameter Sinus-Verzerrung mit:
- Anpassbarer Skalierung (Frequenz)
- Variabler Stärke (Amplitude)
- Rotation vor und nach dem Warping
- Shift mit automatischem Wrapping

### 🎯 Beispiellose Kontrolle
Neun Parameter arbeiten im Konzert:
- 2 Power-Parameter (X, Y)
- 2 Symmetrie-Schalter
- 2 Sinus-Parameter (Scale, Strength)
- 2 Rotations-Parameter
- 1 Shift-Steuerung (Point2D)

## 📊 Parameter

| Parameter | Typ | Bereich/Standard | Beschreibung |
|-----------|-----|------------------|--------------|
| **Sine Scale** | float | 0.001 - 1.0 (Standard: 0.25) | Steuert die Frequenz der Sinuswellen-Verzerrung. Niedrigere Werte = engere Wellen. |
| **Sine Strength** | float | 0.0 - 2.0 (Standard: 0.5) | Steuert die Amplitude/Intensität des Sinus-Warp-Effekts. |
| **Power X** | float | 0.25 - 4.0 (Standard: 1.0) | Exponentielle Verzerrungsstärke auf X-Achse. Werte < 1 dehnen, > 1 komprimieren. |
| **Power Y** | float | 0.25 - 4.0 (Standard: 1.0) | Exponentielle Verzerrungsstärke auf Y-Achse. Unabhängig von X. |
| **Symmetric X** | bool | false | Wenn true, spiegelt die Power-Kurve vom Zentrum auf X-Achse. |
| **Symmetric Y** | bool | false | Wenn true, spiegelt die Power-Kurve vom Zentrum auf Y-Achse. |
| **Rotation** | float | 0.0 - 1.0 (Standard: 0.0) | Rotiert das Muster vor Sinus-Verzerrung. 1.0 = 360°. |
| **Angle** | float | 0.0 - 1.0 (Standard: 0.0) | Rotiert das finale verzerrte Ergebnis. Erzeugt Spiral-Effekte. |
| **Shift** | Point2D | (0.0, 0.0) | Verschiebt das Muster mit automatischem Wrapping. Nützlich für Animation. |

## 🎨 Kreative Nutzungstipps

### 🌟 Parameter-Interaktionen verstehen

Die Kraft dieses Nodes kommt aus Parameter-Kombinationen:

**Power + Sinus Synergie:**
- Hohe Power X + Niedrige Sine Scale = Komprimierte wellige Muster
- Symmetric-Modus + Hohe Sine Strength = Radiale Wellen-Explosionen
- Asymmetrische Power + Rotation = Spiral-Kompressions-Tunnel

**Rotations-Schichtung:**
- Unterschiedliche Rotation + Angle-Werte erzeugen komplexe Spiralen
- Gleiche Werte = einfache Rotation (weniger interessant)
- Entgegengesetzte Richtungen (0.25 vs 0.75) = gegenläufige Effekte

**Shift-Magie:**
- Animieren Sie Shift in Kreisen für orbitale Muster
- Kombinieren mit hoher Sine Strength für flüssige Flows
- Nutzen mit Symmetric-Modus für kaleidoskopische Verschiebungen

### 🎨 Kombination mit anderen 2D Modifiern

**Warping Illusionary** wird exponentiell mächtiger beim Stapeln:

**Sehr empfohlene Kombinationen:**
- **⭐ Star Symmetry**: Nach dem Warping anwenden für psychedelische Mandalas
- **🔮 Weiteres Warping Illusionary**: Stapeln Sie zwei Instanzen mit verschiedenen Einstellungen für fraktale Komplexität
- **🌀 Sine Warp Tile**: Ja, noch mehr Sinus-Warping! Erzeugt Multi-Frequenz-Muster
- **📐 Polar Coordinates**: Transformiert den verzerrten kartesischen Raum in kreisförmig
- **🎨 Color Gradient Maps**: Mappen Sie Farben auf den verzerrten Raum für malerische Effekte

**Für extreme Ergebnisse:**
- Versuchen Sie 3+ Warping Illusionary Nodes nacheinander
- Wechseln Sie zwischen symmetrischen und asymmetrischen Modi
- Variieren Sie Power-Werte dramatisch zwischen Instanzen
- Nutzen Sie Feedback-Schleifen für sich entwickelndes, organisches Chaos

### 🎬 Animations-Strategien

Jeder Parameter ist animations-bereit:

**Subtile Animationen:**
- Variieren Sie Sine Scale langsam (0.2 - 0.3) für Atem-Effekt
- Sanfte kreisförmige Shift-Bewegung für fließende Bewegung
- Graduelle Power-Änderungen (0.8 - 1.2) für Pulsieren

**Dramatische Animationen:**
- Drehen Sie Rotation kontinuierlich (0 bis 1 Loop)
- Rampen Sie Sine Strength (0 bis 2) für Intensitäts-Aufbau
- Schalten Sie Symmetric-Modi für plötzliche Transformationen

**Synchronisierte Animationen:**
- Verknüpfen Sie Rotation und Angle mit Musik-Beats
- Binden Sie Sine Strength an Audio-Amplitude
- Modulieren Sie Power mit LFOs für rhythmisches Warping

### 🖼️ Anwendungsbeispiele

**Für abstrakte Kunst:**
- Beginnen Sie mit Gradienten
- Nutzen Sie extreme Power-Werte (0.25 oder 4.0)
- Hohe Sine Strength (1.5+)
- Animieren Sie langsam für meditative Bewegung

**Für psychedelische Effekte:**
- Auf Fotos oder Video anwenden
- Moderate Power (1.2 - 1.8)
- Hohe Sine Scale (0.8+) für feine Details
- Star Symmetry danach hinzufügen

**Für Glitch-Art:**
- Schnelle Shift-Animationen
- Schnelles Umschalten der Symmetric-Modi
- Extreme Parameter-Kombinationen
- Schichten mit Feedback und Farbeffekten

**Für Musikvideos:**
- Verknüpfen Sie alle Parameter mit Audio-Features
- Als Übergangseffekt zwischen Szenen nutzen
- Auf Text und Grafiken anwenden
- Mit Farbmodulation kombinieren

### 🔮 Umwandlung in 3D

Obwohl primär 2D, existieren kreative 3D-Workflows:

#### 📐 Mit Extrude Node
1. Erstellen Sie ein Basis-Muster oder importieren Sie Textur
2. Wenden Sie Warping Illusionary an (moderate Einstellungen)
3. Konvertieren Sie mit Extrude zu 3D (Height: 0.2 - 0.5)
4. Ergebnis: Skulpturale Formen mit fließender Topologie

**Empfohlene Einstellungen für 3D:**
- Sine Scale: 0.3 - 0.5 (nicht zu chaotisch)
- Power X/Y: 1.0 - 1.5 (subtile Verzerrung)
- Sine Strength: 0.3 - 0.7 (genug Detail, nicht überwältigend)
- Nutzen Sie Symmetric-Modi für erkennbare Formen

#### 🔄 Mit Revolve Node
- Erzeugt zylindrische verzerrte Formen
- Am besten mit asymmetrischen Power-Kurven
- Kann vasenähnliche oder organische Strukturen produzieren
- Kombinieren mit 3D Bend/Twist für extra Komplexität

**Nach 3D-Konvertierung:**
- Wenden Sie 3D Modifier an (Twist, Bend, Repetition)
- Experimentieren Sie mit verschiedenen Beleuchtungswinkeln
- Nutzen Sie metallische oder Glas-Materialien für atemberaubende Ergebnisse

## 🔧 Technische Details

- **Node-Typ**: 2D Modifier (UV → UV)
- **Kategorie**: 2D Modifier
- **Algorithmus**: Sequenzielle Power-Curve- und Sinuswellen-Koordinaten-Transformationen
- **Performance**: Moderat (Zwei-Pass-Verarbeitung)
- **Basiert auf**: Fusion von VIDVOX ISF "Power Warp" und "Sine Warp Tile"

## 💡 Workflow-Beispiele

### Beispiel 1: Unmögliche Architektur
1. Beginnen Sie mit Gittermuster oder Foto von Gebäude
2. Wenden Sie Warping Illusionary an
3. Setzen Sie Power X: 1.5, Power Y: 0.7, beide Symmetric: true
4. Sine Scale: 0.4, Sine Strength: 0.6
5. Passen Sie Rotation und Angle nach Geschmack an
6. Ergebnis: M.C. Escher-artige unmögliche Strukturen

### Beispiel 2: Flüssiges Metall
1. Beginnen Sie mit metallischem Gradient oder Textur
2. Warping Illusionary mit Power X/Y: 1.2
3. Sine Strength: 1.0, Sine Scale: 0.25
4. Animieren Sie Shift in kreisförmigem Muster
5. Animieren Sie Rotation langsam
6. Ergebnis: Fließender Flüssigmetall-Effekt

### Beispiel 3: Portal-Effekt
1. Erstellen Sie radialen Gradient oder Spirale
2. Warping Illusionary: Symmetric X/Y: true
3. Power X/Y: 2.0, Sine Scale: 0.15
4. Animieren Sie Angle kontinuierlich (0 bis 1 Loop)
5. Fügen Sie Farbeffekte und Glow hinzu
6. Ergebnis: Wirbelndes Vortex-Portal

### Beispiel 4: Fraktale Komplexität
1. Wenden Sie erstes Warping Illusionary an: Power X: 1.5, Sine: 0.3
2. Fügen Sie zweites Warping Illusionary hinzu: Power Y: 1.5, Sine: 0.2
3. Fügen Sie drittes mit Symmetric-Modi hinzu: Power: 2.0, Sine: 0.15
4. Feinabstimmung von Shift und Rotation bei jedem
5. Ergebnis: Bewusstseinserweiternde fraktalartige Muster

### Beispiel 5: Glitch-Übergang
1. Beginnen Sie mit Video oder Bildsequenz
2. Warping Illusionary bei Keyframe A: Alle Standardwerte (Power: 1.0)
3. Bei Keyframe B: Power X/Y: 3.0, Sine Strength: 2.0
4. Animieren zwischen A und B schnell (0.5 Sekunden)
5. Ergebnis: Explosiver Glitch-Übergang

## 🔮 Die Illusion verstehen

Die "illusionäre" Qualität kommt von perzeptuellen Widersprüchen:

- **Räumliche Unmöglichkeit**: Power-Kurven komprimieren einen Bereich, während Sinuswellen ihn ausdehnen—das Auge kann dies nicht vereinen
- **Richtungs-Ambiguität**: Multiple Rotations-Parameter erzeugen Oberflächen, die sich in widersprüchliche Richtungen zu drehen scheinen
- **Skalierungs-Verwirrung**: Die Kombination macht es unmöglich, die "wahre" Größe oder Distanz von Elementen zu beurteilen
- **Symmetrie-Bruch**: Symmetrische Power mit asymmetrischem Sinus erzeugt Muster, die fast—aber nicht ganz—regelmäßig sind

Diese kognitive Dissonanz ist es, was das Warping wahrhaft "illusionär" macht.

## 💡 Tipps zur Meisterschaft

**Einfach beginnen:**
1. Beginnen Sie nur mit Power-Parametern (Sine Scale: 0, Sine Strength: 0)
2. Verstehen Sie Power-Kurven zuerst
3. Dann fügen Sie Sinus-Warping graduell hinzu
4. Bauen Sie Komplexität Schicht für Schicht auf

**Experimentier-Protokoll:**
1. Probieren Sie zuerst extreme Werte, um Parameter-Bereich zu verstehen
2. Finden Sie interessante "Unfälle"
3. Verfeinern Sie in Richtung Ihrer Vision
4. Speichern Sie Presets von Entdeckungen

**Performance-Optimierung:**
- Niedrigere Sine Scale = weniger Berechnungen = bessere Performance
- Moderate Sine Strength < 1.0 für Echtzeit-Nutzung
- Extreme Power-Werte (< 0.5 oder > 3.0) können Rand-Artefakte verursachen

## 🎭 Kreative Freiheit

Warping Illusionary ist grenzenlos:
- 🎲 Randomisieren Sie alle Parameter für glückliche Unfälle
- 🔄 Stapeln Sie 5+ Instanzen für absolutes Chaos
- 🎯 Animieren Sie alles gleichzeitig für maximale Dynamik
- 🌈 Kombinieren Sie mit jedem anderen Modifier in Coollab
- ⚡ Treiben Sie Parameter an Extreme—brechen Sie die Illusion!

**Lassen Sie Unmöglichkeit Ihre Leinwand werden!** 🔮✨

## 📜 Credits

- Inspiriert von VIDVOX-ISFs aus dem MIT-Repository
- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
