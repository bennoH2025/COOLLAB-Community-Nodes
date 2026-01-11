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
One of the standout features of this node is its **built-in animation system**. Unlike most nodes where you need to connect animation nodes like the **Time Node**, Circuit Pattern 2D already has a suitable animation integrated. Of course, you can still expand or modify the animation by connecting additional nodes, but the basic animation works immediately without any setup:

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

Circuit Pattern 2D works beautifully with Coollab's **"3D Shape from 2D"** category, which contains two nodes:

#### 📐 Extrude Node
Creates an extruded 3D shape from the 2D pattern.

**Tested Settings for Good Results:**
- Pattern Scale: 0.79
- Line Thickness: 0.37
- Animation Speed: 0.49
- All other parameters: 0.00
- **In Extrude Node:** Height: 0.29

These settings produce something not too wild and well-processable for the human eye.

#### 🔄 Revolve Node
Creates a cylindrical or circular 3D shape by rotating the 2D pattern around an axis. The result is somewhat similar to a Mandelbulber part "main_formula_1 Quaternion" and can generate fractal-like structures.

⚠️ **Note:** The Revolve Node has higher GPU demands, as it likely generates fractal-like geometries.

**Tips for 3D Conversion:**
- **🎯 Start subtle**: Use moderate extrusion/depth values to maintain recognizability
- **🔧 Combine with 3D Modifiers**: After conversion, apply 3D SDF modifiers like twists, bends, or repetitions for unique sculptural forms
- **⚖️ Exercise restraint**: The patterns can become overwhelming in 3D - less is often more
- **💡 Lighting matters**: Experiment with different lighting setups to emphasize the circuit topology

The irregular, organic nature of the circuits translates surprisingly well into 3D space, creating structures that feel both technological and natural.

After that, all **3D Modifiers** can be applied, which opens up completely new design dimensions!

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
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

# Circuit Pattern 2D - Dokumentation

## Übersicht

**Circuit Pattern 2D** ist ein prozedural generierter 2D SDF (Signed Distance Field) Node, der animierte Leiterplattenmuster erzeugt. Inspiriert von den komplexen Layouts gedruckter Schaltkreise (PCBs), generiert dieser Node organische, fließende Muster, die an elektronische Leiterbahnen, Lötpads und Bauteil-Layouts erinnern.

## 🎯 Inspiration & Design-Philosophie

Obwohl visuell ähnlich zu **Cairo Tiling**, verfolgt Circuit Pattern 2D einen grundlegend anderen Ansatz:

- **Cairo Tiling** basiert auf regelmäßigen, gleichmäßigen Gittermustern mit vorhersehbaren, sich wiederholenden Strukturen
- **Circuit Pattern 2D** nutzt Voronoi-basierte prozedurale Generierung, um **unregelmäßige, organische Muster** zu schaffen, die sich nie exakt gleich wiederholen
- Die ungleichmäßige, asymmetrische Natur imitiert den authentischen Look echter Leiterplatten-Layouts, wo Leiterbahnen funktionalen Anforderungen folgen statt ästhetischer Symmetrie
- Die **integrierte Animation** erweckt diese Muster zum Leben und simuliert den Fluss von Elektronen durch die Schaltkreis-Pfade

Diese organische Unregelmäßigkeit wird besonders sichtbar, wenn die Animation aktiv ist, da der "Electron Flow"-Effekt durch die unvorhersehbaren Pfade wandert und ein faszinierendes, sich ständig veränderndes visuelles Erlebnis schafft.

## ⭐ Hauptmerkmale

### 🎬 Integrierte Animation
Eines der herausragenden Features dieses Nodes ist sein **eingebautes Animationssystem**. Anders als in den meisten Nodes, wo man spezielle Nodes wie den **Time Node** zur Animation verknüpfen muss, ist hier bereits eine passende Animation integriert:

- **🎓 Perfekt für Anfänger**: Einfach den Play-Button in Coollabs Timeline drücken und das Schaltkreismuster animiert sich automatisch
- **⚡ Electron Flow Effekt**: Simuliert bewegte Ladungen, die durch die Leiterbahnen wandern
- **✨ Flicker-Effekt**: Fügt authentisches visuelles Rauschen hinzu, das echte elektronische Komponenten nachahmt
- **🎵 Manuelle Synchronisation**: Nutze den `Animation Speed`-Parameter, um die Animation von Hand auf Musik oder andere zeitliche Anforderungen zu synchronisieren

Natürlich kann man durch Verknüpfung zusätzlicher Nodes (wie Time Node, LFO, etc.) die Animation noch erweitern oder verändern, aber die Grundanimation funktioniert sofort ohne Setup.

Dies macht Circuit Pattern 2D außergewöhnlich zugänglich für Neulinge und gleichzeitig leistungsstark genug für fortgeschrittene Benutzer.

### 🔧 Multi-Oktaven-Detail
Das Muster wird mit mehreren Schichten (Oktaven) von Voronoi-Rauschen aufgebaut, sodass Sie die Komplexität steuern können:
- Niedrigere Oktavenwerte (1-2) erzeugen einfachere, klarere Schaltkreismuster
- Höhere Oktavenwerte (3-4) fügen komplexe Details und kleinere Leiterbahnen hinzu

### ⚡ Dynamische Effekte
- **💫 Electron Flow**: Animierte "Elektronen", die durch die Schaltkreis-Pfade wandern
- **🔆 Flicker Amount**: Simuliert das Flackern elektronischer Komponenten oder instabiler Stromversorgung
- **🌑 Vignette**: Subtile Abdunklung an den Rändern für eine fokussiertere Komposition

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Pattern Scale** | 0.5 - 10.0 | 2.0 | Steuert die Dichte und Größe des Schaltkreismusters. Höhere Werte erzeugen komplexere, dichter gepackte Schaltkreise. |
| **Line Thickness** | 0.1 - 1.0 | 0.4 | Passt die Breite der Leiterbahnen an. Dünnere Linien erzeugen feinere Muster. |
| **Animation Speed** | 0.0 - 5.0 | 1.0 | Steuert, wie schnell der Elektronenfluss und andere Animationen ablaufen. Auf 0 setzen für statisches Muster. |
| **Offset** | Point2D | (0.0, 0.0) | Verschiebt das gesamte Muster im 2D-Raum. Nützlich für Positionierung oder Variationen. |
| **Octaves** | 1.0 - 4.0 | 3.0 | Anzahl der Detailschichten. Mehr Oktaven = komplexere Muster (aber potenziell langsamer). |
| **Electron Flow** | 0.0 - 2.0 | 0.5 | Intensität des animierten Elektroneneffekts. Höhere Werte erzeugen mehr sichtbare "Energie", die durch die Schaltkreise fließt. |
| **Flicker Amount** | 0.0 - 1.0 | 0.3 | Menge an zufälligem Flackern. Fügt visuelles Rauschen für ein organischeres, weniger perfektes Aussehen hinzu. |

## 🎨 Kreative Nutzungstipps

### 🌟 Kombination mit 2D Modifiern

Die **2D Modifier**-Kategorie in Coollab bietet endlose Möglichkeiten, Circuit Pattern 2D in völlig neue Visuals zu verwandeln:

**Sehr empfohlene Kombinationen:**
- **⭐ Star Symmetry**: Erzeugt kaleidoskopische Schaltkreis-Mandalas mit radialer Wiederholung
- **🌊 Sine Warp Tile**: Fügt fließende, wellenartige Verzerrungen zu den Schaltkreismustern hinzu
- **🌀 Warping Illusionary**: Kombiniert mehrere Warp-Effekte für surreale, unmögliche Schaltkreis-Geometrien
- **🔮 Kaleidoskop-Nodes**: Generieren hypnotische symmetrische Muster aus den unregelmäßigen Schaltkreisen
- **🎯 Polar Coordinates**: Transformiert lineare Schaltkreise in kreisförmige, radiale Designs

**Experimentelle Vorschläge:**
- Versuchen Sie, mehrere Modifier zu stapeln für unerwartete Ergebnisse
- Kombinieren Sie mit Displacement- oder Noise-Modifiern für Glitch-Art-Ästhetik
- Nutzen Sie Rotations- und Skalierungs-Modifier für dynamische kameraähnliche Bewegungen

### 🚀 Schnelles Erstellen von Variationen

Da Circuit Pattern 2D ein 2D SDF ist, können Sie schnell iterieren und Dutzende Variationen erstellen:
1. Mit Standardeinstellungen beginnen
2. Einen 2D Modifier anwenden
3. 1-2 Parameter anpassen
4. Als Preset speichern oder Ergebnis screenshot
5. Mit verschiedenen Modifiern wiederholen

Dieser Workflow ermöglicht schnelle Exploration und ist perfekt für kreative Experimente.

### 🔮 Umwandlung in 3D

Circuit Pattern 2D funktioniert hervorragend mit Coollabs **"3D Shape from 2D"**-Kategorie, die zwei Nodes enthält:

#### 📐 Extrude Node
Erzeugt eine extrudierte 3D-Form aus dem 2D-Muster.

**Getestete Einstellungen für gute Ergebnisse:**
- Pattern Scale: 0.79
- Line Thickness: 0.37
- Animation Speed: 0.49
- Alle anderen Parameter: 0.00
- **Im Extrude Node:** Height: 0.29

Diese Einstellungen ergeben etwas nicht allzu Wildes und gut Verarbeitbares für das menschliche Auge.

#### 🔄 Revolve Node
Erzeugt eine zylindrische oder kreisgebundene 3D-Form durch Rotation des 2D-Musters um eine Achse. Das Ergebnis ähnelt leicht einem Mandelbulber-Teil "main_formula_1 Quaternion" und kann fraktalartige Strukturen erzeugen.

⚠️ **Hinweis:** Das Revolve Node stellt höhere GPU-Anforderungen, da es wahrscheinlich fraktalartige Geometrien generiert.

**Tipps für 3D-Konvertierung:**
- **🎯 Subtil beginnen**: Verwenden Sie moderate Extrusions-/Tiefenwerte, um Erkennbarkeit zu bewahren
- **🔧 Mit 3D Modifiern kombinieren**: Nach der Konvertierung können Sie 3D SDF Modifier wie Twists, Bends oder Repetitions anwenden für einzigartige skulpturale Formen
- **⚖️ Zurückhaltung üben**: Die Muster können in 3D überwältigend werden - weniger ist oft mehr
- **💡 Beleuchtung ist wichtig**: Experimentieren Sie mit verschiedenen Lichtsetups, um die Schaltkreis-Topologie zu betonen

Die unregelmäßige, organische Natur der Schaltkreise übersetzt sich überraschend gut in den 3D-Raum und erzeugt Strukturen, die sich sowohl technologisch als auch natürlich anfühlen.

Danach können alle **3D Modifier** angewendet werden, was wieder ganz neue Design-Dimensionen eröffnet!

## 🔧 Technische Details

- **Node-Typ**: 2D SDF (UV → SignedDistance)
- **Kategorie**: 2D SDF
- **Animation**: Integriert via `_time`-Variable
- **Algorithmus**: Multi-Oktaven Voronoi-Rauschen mit Chebyshev-Distanz
- **Performance**: Moderat (skaliert mit Oktavenzahl)

## 💡 Workflow-Beispiele

### Beispiel 1: Animierter Schaltkreis-Hintergrund
1. Circuit Pattern 2D zur Komposition hinzufügen
2. Play in der Timeline drücken
3. `Animation Speed` an Projekt-Tempo anpassen
4. Als Hintergrund-Layer oder Maske verwenden

### Beispiel 2: Glitch Art
1. Mit Circuit Pattern 2D beginnen
2. `Flicker Amount` auf 0.7-1.0 setzen
3. Einen **Displacement**-Modifier hinzufügen
4. Mit Farbeffekten für Cyberpunk-Ästhetik kombinieren

### Beispiel 3: 3D Schaltkreis-Skulptur
1. Circuit Pattern 2D erstellen
2. Mit Extrude Node in 3D konvertieren
3. Einen **Twist** oder **Bend** 3D Modifier anwenden
4. Mit metallischen Materialien für Tech-Art-Look rendern

## 🎭 Kreative Freiheit

Die Schönheit von Circuit Pattern 2D liegt in seiner Vielseitigkeit und den unerwarteten Ergebnissen, die aus Experimenten entstehen. Haben Sie keine Angst:
- 🚀 Parameter auf extreme Werte zu treiben
- 🔀 Scheinbar inkompatible Modifier zu kombinieren
- 💥 Die "Regeln" zu brechen und zu sehen, was passiert
- 🎨 Mehrere Instanzen mit Blend-Modi zu überlagern

**Lassen Sie Ihrer Kreativität freien Lauf** - genau wie die Elektronen, die durch diese digitalen Schaltkreise fließen! ⚡✨

## 📜 Credits

- Inspiriert von elektronischen Leiterplattenmustern und prozeduralen Generierungstechniken
- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
