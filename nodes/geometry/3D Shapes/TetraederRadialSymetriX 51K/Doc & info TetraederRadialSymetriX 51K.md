[English](#-english) | [Deutsch](#-deutsch)
---

# 🔺 TetraederRadialSymetriX 51K Node Documentation

## 🇬🇧 English

### 📋 Overview
The **TetraederRadialSymetriX 51K** node creates sophisticated radial fractal structures based on tetrahedral geometry with advanced symmetry controls. This procedural geometry generator combines tetrahedral folding mathematics with radial distribution patterns, inspired by butadiene's SDF research. The node produces complex geometric patterns that exhibit both fractal detail and radial symmetry, creating structures reminiscent of crystalline formations, architectural rosettes, or complex molecular arrangements.
& It generates stunning radial fractal geometries that can serve as decorative architectural elements, crystalline structures, or complex geometric art installations with precise mathematical symmetry.

**📋 Files Included**

- TetraederRadialSymetriX 51K.clbnode - The main COOLLAB 3D shape node
- TetraederRadialSymetriX 51K.clbnode.presets.json - Preset configurations including "Default/Standart", "Kavalier 69", "MarenkoBlock", "Korlund", "Spir-V Odysse Z", and "Odysse Rings" effects

**🚀 How to Use**

*Import the Node:*

- Download both files from this directory (necessary files to make it run)
- Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
- as well as the associated preset .json file. 

You can place the two files in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*Connect to Scene:*

- Use as a 3D geometry source in your scene
- Combine with materials, lighting, and other 3D nodes
- Works excellently with raymarching renderers and creates intricate light diffraction patterns through geometric details

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Iteration-dependent (higher iterations require more computation)
- Rendering: Compatible with raymarching and mesh generation

**📜 License & Attribution**

*Mathematical Foundation:*

- Inspired by butadiene's SDF research at https://jbaker.graphics/writings/DEC.html
- Credits for the inspirational SDF go to: butadiene
- Based on tetrahedral folding and radial symmetry mathematics

*This COOLLAB Node:*

- Idea and project coordination by bennoH.
- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not a simple geometric primitive. The TetraederRadialSymetriX 51K node combines advanced mathematical concepts:
- 🔺 **Tetrahedral Folding**: Uses iterative tetrahedral folding operations for fractal complexity
- ⚡ **Radial Symmetry**: Creates precise radial distributions around the Y-axis with controllable repetition count
- 🎯 **Multi-Axis Rotation**: Independent rotation controls for XY, XZ, and YZ planes
- 📐 **Geometric Folding**: Multiple folding operations with scalable parameters for structural variation
- 🔄 **Iterative Refinement**: Controllable iteration count for detail vs performance balance

### 🎛️ Parameters

#### 🔧 Core Fractal Controls
- 📏 **Scale** (Float, 0.5-3.0): Controls the fractal scaling factor. Higher values create more expansive structures, lower values create tighter, more compact forms
- 🔢 **Iterations** (Integer, 1-12): Number of fractal iterations. Higher values create more detailed and complex structures but require more computational power
- 🎯 **Offset** (vec3, xyz vector): Fractal offset vector that influences the base structure generation and asymmetry

#### ⚡ Radial Distribution Controls
- 🔄 **Radial Symmetry** (Float, 3-50): Number of radial repetitions around Y-axis. Higher values create more detailed radial patterns (24 = classic, 30+ = high detail)
- 📍 **Distance** (Float, 2-15): Distance from center axis. Controls how far the tetrahedral elements are positioned from the central axis

#### 🎲 Rotation Controls
- 🔄 **XY Rotation** (Float, 0-2π): Rotation around Z-axis. Controls the orientation in the XY plane
- 🔄 **XZ Rotation** (Float, 0-2π): Rotation around Y-axis. Controls the orientation in the XZ plane  
- 🔄 **YZ Rotation** (Float, 0-2π): Rotation around X-axis. Controls the orientation in the YZ plane

#### 📐 Geometric Structure Controls
- 🎛️ **Fold Scale** (vec3, xyz vector): Scaling factors for the folding operations. Controls the intensity and direction of geometric folding transformations

### ⚙️ Technical Implementation
The radial tetrahedral fractal generation works through sophisticated mathematical stages:
1. 🎲 **Initial Transformations**: Applies rotation matrices to the input position
2. ⚡ **Radial Symmetry Calculation**: Uses polar coordinate transformation with modular arithmetic for radial repetition
3. 📍 **Radial Positioning**: Translates elements outward from center using distance parameter
4. 🔄 **Multi-Axis Rotation**: Applies independent rotations for complex orientation control
5. 📐 **Geometric Folding**: Performs multiple absolute value folding operations with scaling
6. 🔺 **Tetrahedral Iteration**: Executes iterative tetrahedral folding with controlled complexity
7. 📏 **Distance Field Output**: Generates final signed distance field with proper scaling

### 🎨 Creative Applications
- 🏛️ **Architectural Decoration**: Create complex ceiling rosettes, window patterns, or facade decorations
- 💎 **Crystal Visualization**: Generate crystalline structures, mineral formations, or geological patterns
- 🔬 **Scientific Modeling**: Visualize molecular arrangements, atomic structures, or chemical compounds
- 🎮 **Game Environment Design**: Build alien artifacts, sci-fi technology, or fantasy magical structures
- 🎨 **Geometric Art**: Create mathematically precise art installations with radial symmetry themes

### 💡 Tips for Best Results
- ✅ Start with **Scale** around 1.5-2.0 for balanced fractal structures
- ✅ Use **Iterations** between 8-12 for detailed results without excessive computation
- ✅ Set **Radial Symmetry** to 24 for classic patterns, 30+ for high-detail arrangements
- ✅ Keep **Distance** around 5-8 for well-distributed radial elements
- ✅ Use **Offset** values around (1,1,1) for symmetric base structures
- ✅ Experiment with **Fold Scale** variations for unique geometric characteristics

### 🎬 Animation Setup Guide
**TetraederRadialSymetriX 51K** is designed for spectacular geometric animations! The preset names indicate different structural characteristics:

**Understanding Preset Structures:**
Each preset demonstrates different geometric approaches and complexity levels:

**Animation Recommendations:**
1. ⚡ **For Radial Animation**: Animate **Radial Symmetry** for evolving radial patterns
2. 🔄 **For Rotation Effects**: Animate rotation parameters for spinning geometric elements
3. 📏 **For Scale Animation**: Vary **Scale** parameter for growing/shrinking fractal effects
4. 🎯 **For Morphing**: Animate **Offset** components for structural transformation
5. 📐 **For Folding Animation**: Modify **Fold Scale** components for geometric evolution

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.1) → **Sine Wave** (Min: 20, Max: 30, Period: 12.0) → **Radial Symmetry**
2. 🕐 **Time Node** (Speed: 0.2) → **Linear** (Min: 0, Max: 2π, Period: 20.0) → **XY Rotation**
3. 🕐 **Time Node** (Speed: 0.15) → **Sine Wave** (Min: 1.2, Max: 2.5, Period: 8.0) → **Scale**
4. 🔄 **Rotate Node** with **Time Node** (Speed: 0.05) → **Y-axis** for slow orbital presentation

**🔗 Links**

- Butadiene's SDF Research: https://jbaker.graphics/writings/DEC.html
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **TetraederRadialSymetriX 51K** Node erzeugt anspruchsvolle radiale Fraktalstrukturen basierend auf tetraedrischer Geometrie mit erweiterten Symmetrie-Kontrollen. Dieser prozedurale Geometrie-Generator kombiniert tetraedrische Faltungsmathematik mit radialen Verteilungsmustern, inspiriert von butadienes SDF-Forschung. Der Node produziert komplexe geometrische Muster, die sowohl fraktale Details als auch radiale Symmetrie aufweisen und Strukturen erzeugen, die an kristalline Formationen, architektonische Rosetten oder komplexe molekulare Anordnungen erinnern.
& generiert beeindruckende radiale Fraktal-Geometrien, die als dekorative architektonische Elemente, kristalline Strukturen oder komplexe geometrische Kunstinstallationen mit präziser mathematischer Symmetrie dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- TetraederRadialSymetriX 51K.clbnode - Das Haupt-COOLLAB 3D-Form Node
- TetraederRadialSymetriX 51K.clbnode.presets.json - Preset-Konfigurationen inklusive "Default/Standart", "Kavalier 69", "MarenkoBlock", "Korlund", "Spir-V Odysse Z" und "Odysse Rings" Effekte

**🚀 Verwendung sprich Installationsanleitung**

*Node Importieren:*

- Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
- Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
- wie auch die zugehörige Preset-Datei die .json Datei. 

Sie können die beiden Files in die Kategorie "3D Shapes" respektive den entsprechenden Ordner hinein legen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "3D Shapes" einzuordnen: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*In Szene Verbinden:*

- Als 3D-Geometrie-Quelle in Ihrer Szene verwenden
- Mit Materialien, Beleuchtung und anderen 3D-Nodes kombinieren
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt komplexe Lichtbeugungsmuster durch geometrische Details

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Iterationsabhängig (höhere Iterationen benötigen mehr Berechnung)
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung

**📜 Lizenz & Attribution**

*Mathematische Grundlage:*

- Inspiriert von butadienes SDF-Forschung auf https://jbaker.graphics/writings/DEC.html
- Credits für das inspirierende SDF gehen an: butadiene
- Basierend auf tetraedrischer Faltung und radialer Symmetrie-Mathematik

*Dieses COOLLAB Node:*

- Idee und Projektkoordination von bennoH.
- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC auf einem "KostenlosPlan" von bennoH.
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist keine einfache geometrische Primitive. Der TetraederRadialSymetriX 51K Node kombiniert fortgeschrittene mathematische Konzepte:
- 🔺 **Tetraedrische Faltung**: Verwendet iterative tetraedrische Faltungsoperationen für fraktale Komplexität
- ⚡ **Radiale Symmetrie**: Erzeugt präzise radiale Verteilungen um die Y-Achse mit kontrollierbarer Wiederholungsanzahl
- 🎯 **Multi-Achsen-Rotation**: Unabhängige Rotationskontrollen für XY-, XZ- und YZ-Ebenen
- 📐 **Geometrische Faltung**: Multiple Faltungsoperationen mit skalierbaren Parametern für strukturelle Variation
- 🔄 **Iterative Verfeinerung**: Kontrollierbare Iterationsanzahl für Detail-vs-Performance-Balance

### 🎛️ Parameter

#### 🔧 Kern-Fraktal-Kontrollen
- 📏 **Scale** (Float, 0.5-3.0): Kontrolliert den Fraktal-Skalierungsfaktor. Höhere Werte erzeugen expansivere Strukturen, niedrigere Werte erzeugen engere, kompaktere Formen
- 🔢 **Iterations** (Integer, 1-12): Anzahl der Fraktal-Iterationen. Höhere Werte erzeugen detailliertere und komplexere Strukturen, benötigen aber mehr Rechenleistung
- 🎯 **Offset** (vec3, xyz-Vektor): Fraktal-Versatzvektor, der die Basis-Strukturgenerierung und Asymmetrie beeinflusst

#### ⚡ Radiale Verteilungs-Kontrollen
- 🔄 **Radial Symmetry** (Float, 3-50): Anzahl radialer Wiederholungen um die Y-Achse. Höhere Werte erzeugen detailliertere radiale Muster (24 = klassisch, 30+ = hohe Details)
- 📍 **Distance** (Float, 2-15): Entfernung von der Mittelachse. Kontrolliert, wie weit die tetraedrischen Elemente von der zentralen Achse positioniert sind

#### 🎲 Rotations-Kontrollen
- 🔄 **XY Rotation** (Float, 0-2π): Rotation um die Z-Achse. Kontrolliert die Orientierung in der XY-Ebene
- 🔄 **XZ Rotation** (Float, 0-2π): Rotation um die Y-Achse. Kontrolliert die Orientierung in der XZ-Ebene  
- 🔄 **YZ Rotation** (Float, 0-2π): Rotation um die X-Achse. Kontrolliert die Orientierung in der YZ-Ebene

#### 📐 Geometrische Struktur-Kontrollen
- 🎛️ **Fold Scale** (vec3, xyz-Vektor): Skalierungsfaktoren für die Faltungsoperationen. Kontrolliert die Intensität und Richtung geometrischer Faltungstransformationen

### ⚙️ Technische Implementation
Die radiale tetraedrische Fraktal-Generierung funktioniert durch ausgeklügelte mathematische Stufen:
1. 🎲 **Initiale Transformationen**: Wendet Rotationsmatrizen auf die Eingabeposition an
2. ⚡ **Radiale Symmetrie-Berechnung**: Verwendet polare Koordinatentransformation mit modularer Arithmetik für radiale Wiederholung
3. 📍 **Radiale Positionierung**: Verschiebt Elemente vom Zentrum nach außen mittels Entfernungsparameter
4. 🔄 **Multi-Achsen-Rotation**: Wendet unabhängige Rotationen für komplexe Orientierungskontrolle an
5. 📐 **Geometrische Faltung**: Führt multiple Absolutwert-Faltungsoperationen mit Skalierung durch
6. 🔺 **Tetraedrische Iteration**: Führt iterative tetraedrische Faltung mit kontrollierter Komplexität aus
7. 📏 **Distance Field Ausgabe**: Generiert finales Signed Distance Field mit korrekter Skalierung

### 🎨 Kreative Anwendungen
- 🏛️ **Architektonische Dekoration**: Komplexe Deckenrosetten, Fenstermuster oder Fassadendekorationen erstellen
- 💎 **Kristall-Visualisierung**: Kristalline Strukturen, Mineralformationen oder geologische Muster generieren
- 🔬 **Wissenschaftliche Modellierung**: Molekulare Anordnungen, atomare Strukturen oder chemische Verbindungen visualisieren
- 🎮 **Spielumgebungs-Design**: Alien-Artefakte, Sci-Fi-Technologie oder Fantasy-Magiestrukturen bauen
- 🎨 **Geometrische Kunst**: Mathematisch präzise Kunstinstallationen mit radialen Symmetrie-Themen erstellen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Scale** um 1.5-2.0 für ausgewogene Fraktalstrukturen beginnen
- ✅ **Iterations** zwischen 8-12 für detaillierte Ergebnisse ohne übermäßige Berechnung verwenden
- ✅ **Radial Symmetry** auf 24 für klassische Muster, 30+ für hochdetaillierte Anordnungen setzen
- ✅ **Distance** um 5-8 für gut verteilte radiale Elemente halten
- ✅ **Offset**-Werte um (1,1,1) für symmetrische Basisstrukturen verwenden
- ✅ Mit **Fold Scale**-Variationen für einzigartige geometrische Charakteristiken experimentieren

### 🎬 Animations-Setup Anleitung
**TetraederRadialSymetriX 51K** ist für spektakuläre geometrische Animationen konzipiert! Die Preset-Namen zeigen verschiedene strukturelle Charakteristiken an:

**Preset-Strukturen verstehen:**
Jedes Preset demonstriert verschiedene geometrische Ansätze und Komplexitätsgrade:

**Animations-Empfehlungen:**
1. ⚡ **Für radiale Animation**: **Radial Symmetry** für sich entwickelnde radiale Muster animieren
2. 🔄 **Für Rotations-Effekte**: Rotationsparameter für rotierende geometrische Elemente animieren
3. 📏 **Für Skalierungs-Animation**: **Scale**-Parameter für wachsende/schrumpfende Fraktaleffekte variieren
4. 🎯 **Für Morphing**: **Offset**-Komponenten für strukturelle Transformation animieren
5. 📐 **Für Faltungs-Animation**: **Fold Scale**-Komponenten für geometrische Evolution modifizieren

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.1) → **Sine Wave** (Min: 20, Max: 30, Period: 12.0) → **Radial Symmetry**
2. 🕐 **Time Node** (Geschwindigkeit: 0.2) → **Linear** (Min: 0, Max: 2π, Period: 20.0) → **XY Rotation**
3. 🕐 **Time Node** (Geschwindigkeit: 0.15) → **Sine Wave** (Min: 1.2, Max: 2.5, Period: 8.0) → **Scale**
4. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.05) → **Y-Achse** für langsame orbitale Präsentation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Inspired by**: Butadiene's SDF Research 🔺  
**Inspiriert von**: Butadienes SDF-Forschung 🔺

**Category**: 3D Shapes > Radial Fractals ⚡  
**Kategorie**: 3D-Formen > Radiale Fraktale ⚡

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "Default/Standart" - Balanced tetrahedral structure with 24-fold radial symmetry
- "Kavalier 69" - Refined structure with reduced scale for delicate patterns
- "MarenkoBlock" - Block-like formation with reduced radial symmetry (5.88)
- "Korlund" - Extended structure with modified offset and fold parameters
- "Spir-V Odysse Z" - Spiral-like formation with 30-fold symmetry and complex offset
- "Odysse Rings" - Ring-like structures with 25.36-fold symmetry and extreme fold scaling

**Verfügbare Presets**: 
- "Default/Standart" - Ausgewogene tetraedrische Struktur mit 24-facher radialer Symmetrie
- "Kavalier 69" - Verfeinerte Struktur mit reduzierter Skalierung für zarte Muster
- "MarenkoBlock" - Block-ähnliche Formation mit reduzierter radialer Symmetrie (5.88)
- "Korlund" - Erweiterte Struktur mit modifiziertem Offset und Faltungsparametern
- "Spir-V Odysse Z" - Spiral-ähnliche Formation mit 30-facher Symmetrie und komplexem Offset
- "Odysse Rings" - Ring-ähnliche Strukturen mit 25.36-facher Symmetrie und extremer Faltungsskalierung

**🔗 Links**

- Butadiene's SDF Research: https://jbaker.graphics/writings/DEC.html
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025
