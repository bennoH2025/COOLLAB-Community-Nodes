[English](#-english) | [Deutsch](#-deutsch)
---

# 🧊 Menger Sponge EXTENDED Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Menger Sponge EXTENDED** node is an advanced version of the classic Menger Sponge fractal with additional control parameters for creative experimentation. This procedural geometry generator creates complex fractal cross structures based on the mathematical Menger Sponge concept, but with enhanced flexibility for artistic and architectural applications. The node allows for detailed manipulation of fractal iterations, cross thickness, folding transformations, and scale reductions to create unique 3D structures ranging from architectural frameworks to abstract geometric art.

& It generates stunning fractal structures that can serve as modern architectural frameworks, abstract sculptures, mathematical visualizations, or complex geometric installations with controllable detail levels and transformation parameters.

**📋 Files Included**

- Menger Sponge EXTENDED.clbnode - The main COOLLAB 3D shape node
- Menger Sponge EXTENDED.clbnode.presets.json - Preset configurations including "LivingBuilding with Shiftet Apartements", "Default - Standart", "INSIDER-ONE by nearfield details", "Stuco Sleshed BRO", "Friction H2-B", "DeStructUR", and "CompacT 106" effects

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
- Works excellently with raymarching renderers and creates fascinating fractal light interactions through complex geometric structures

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable with optimized SDF calculations (be careful with high Detail values)
- Rendering: Compatible with raymarching and mesh generation
- Based on: Enhanced Menger Sponge fractal algorithm with folding transformations

**📜 License & Attribution**

*Mathematical Foundation:*

- Based on the classic Menger Sponge fractal concept
- Enhanced with folding transformations and scale manipulations
- Original Menger Sponge concept by Karl Menger (1926)

*This COOLLAB Node:*

- Based on the original "Menger Sponge" Coollab node
- Extensions coded by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Through instructions and under the supervision of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not just a simple Menger Sponge implementation. The EXTENDED version provides comprehensive control over fractal generation:
- 🔢 **Advanced Iteration Control**: Detailed control over fractal iterations with starting points and detail levels
- ➕ **Cross Structure Manipulation**: Adjustable cross thickness for varying structural density
- 📐 **Geometric Constraints**: Cube size control to limit and shape the overall structure
- 🔄 **Folding Transformations**: Advanced folding operations with factor, scale, and offset controls
- 📏 **Scale Management**: Precise control over scale reduction between iterations
- 🎛️ **Creative Flexibility**: Extended parameters allow for non-traditional Menger Sponge variations

### 🎛️ Parameters

#### 🔢 Fractal Structure Controls
- 🎯 **Detail** (Integer, 0-12+): Number of fractal iterations. Higher values create more detailed cross structures but increase computational cost. **Warning**: Values above 8 may significantly impact performance
- ➕ **Cross Thickness** (Float, 0.0-2.0+): Controls how thick the cross arms are. Lower values make thinner crosses, creating more open structures
- 📐 **Cube Size** (Float, 0.0-5.0+): Size of the containing cube that limits the cross shape. Affects the overall boundary of the fractal structure

#### 🔧 Scale and Transformation Controls
- 📏 **Base Scale** (Float, 0.1-2.0): Starting scale factor for the fractal. Affects overall size and can create interesting scaling effects
- 🎯 **Iteration Start** (Float, 0.0-5.0): Starting iteration offset. Shifts which fractal level begins, allowing for interior exploration of the fractal
- 🔄 **Scale Reduction** (Float, 1.5-5.0): How much the scale decreases each iteration. Higher values create faster decay and more compact structures

#### 🌀 Advanced Folding Controls
- 🔄 **Fold Factor** (Float, -1.0-1.0): Controls the folding transformation between iterations. Negative values create inverse folding effects
- 📏 **Fold Scale** (Float, 2.0-10.0): Scale factor for the folding operation. Affects the spacing and distribution of fractal elements
- 🎯 **Fold Offset** (Float, 0.0-5.0): Offset applied during the folding transformation. Shifts the folding center and creates asymmetric effects

### ⚙️ Technical Implementation
The enhanced Menger Sponge generation works through sophisticated mathematical stages:
1. 🎯 **Cross SDF Calculation**: Creates the basic cross structure using absolute position coordinates and thickness controls
2. 📐 **Cube Boundary Application**: Applies cubic constraints to limit the cross shape within defined bounds
3. 🔄 **Iterative Fractal Generation**: Performs multiple iterations with scale reduction and position transformations
4. 🌀 **Folding Transformations**: Applies fractional folding operations with custom factors, scales, and offsets
5. 📏 **Distance Field Combination**: Combines all iterations using maximum distance operations for proper fractal structure

### 🎨 Creative Applications
- 🏛️ **Architectural Frameworks**: Design complex structural systems, scaffolding, or building frameworks with fractal properties
- 🎭 **Abstract Sculptures**: Create mathematical art installations and geometric sculptures for galleries or public spaces
- 🏢 **Urban Design**: Generate complex urban structures, lattice systems, or architectural details with fractal characteristics
- 🎮 **Game Environment Design**: Build futuristic structures, alien architectures, or complex level geometry with mathematical precision
- 🔬 **Mathematical Visualization**: Explore and visualize fractal mathematics, self-similarity concepts, and geometric progression
- 🎨 **Procedural Art**: Create complex geometric patterns and structures for digital art and visualization projects

### 💡 Tips for Best Results
- ✅ Start with **Detail** values between 3-6 for good balance of complexity and performance
- ✅ Use **Cross Thickness** around 0.8-1.2 for well-defined structural elements
- ✅ Set **Cube Size** between 3.0-4.5 for good proportional boundaries
- ✅ Keep **Base Scale** around 0.5-1.0 for standard fractal proportions
- ✅ Experiment with **Fold Factor** values between -0.5 and 0.5 for interesting variations
- ✅ Use **Scale Reduction** around 3.0 for traditional Menger Sponge behavior
- ⚠️ **Performance Warning**: Be cautious with **Detail** values above 8, especially when combining with other complex nodes

### 🎬 Animation Setup Guide
**Menger Sponge EXTENDED** is perfect for mathematical and architectural animations! The preset names indicate different structural and artistic approaches:

**Understanding Preset Architectures:**
Each preset demonstrates different fractal approaches:
- **"LivingBuilding with Shiftet Apartements"**: Architectural interpretation with shifted iteration start
- **"Default - Standart"**: Classic Menger Sponge configuration for traditional fractal appearance
- **"INSIDER-ONE by nearfield details"**: High-detail configuration focusing on interior structure exploration
- **"Stuco Sleshed BRO"**: Artistic variation with negative fold factors for unique geometric effects
- **"Friction H2-B"**: High-detail fractal with enhanced cross thickness for dense structures
- **"DeStructUR"**: Deconstructed fractal appearance with thick cross elements
- **"CompacT 106"**: Compact fractal configuration with modified scale reduction

**Animation Recommendations:**
1. 🔢 **For Fractal Growth**: Animate **Detail** from 1 to target value to show fractal construction process
2. ➕ **For Structural Changes**: Vary **Cross Thickness** to show structural density transitions
3. 🎯 **For Interior Exploration**: Animate **Iteration Start** to journey through fractal levels
4. 🔄 **For Geometric Morphing**: Slowly change **Fold Factor** for smooth geometric transformations
5. 📏 **For Scale Dynamics**: Animate **Scale Reduction** to show different fractal decay rates

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.1) → **Ramp** (Min: 1, Max: 6) → **Detail** (for fractal growth)
2. 🕐 **Time Node** (Speed: 0.2) → **Sine Wave** (Min: 0.5, Max: 1.5, Period: 12.0) → **Cross Thickness**
3. 🕐 **Time Node** (Speed: 0.05) → **Sine Wave** (Min: 0, Max: 3, Period: 20.0) → **Iteration Start**
4. 🕐 **Time Node** (Speed: 0.15) → **Sine Wave** (Min: -0.3, Max: 0.3, Period: 15.0) → **Fold Factor**
5. 🔄 **Rotate Node** with **Time Node** (Speed: 0.03) → **Y-axis** for slow mathematical presentation

**🔗 Links**

- Original Menger Sponge concept by Karl Menger (1926)
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - August 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Menger Sponge EXTENDED** Node ist eine erweiterte Version des klassischen Menger-Schwamm-Fraktals mit zusätzlichen Kontrollparametern für kreative Experimente. Dieser prozedurale Geometrie-Generator erzeugt komplexe fraktale Kreuzstrukturen basierend auf dem mathematischen Menger-Schwamm-Konzept, jedoch mit erhöhter Flexibilität für künstlerische und architektonische Anwendungen. Der Node ermöglicht detaillierte Manipulation von Fraktaliterationen, Kreuzdicke, Faltungstransformationen und Skalierungsreduktionen, um einzigartige 3D-Strukturen zu erstellen, die von architektonischen Frameworks bis zu abstrakten geometrischen Kunstwerken reichen.

& generiert beeindruckende Fraktalstrukturen, die als moderne architektonische Frameworks, abstrakte Skulpturen, mathematische Visualisierungen oder komplexe geometrische Installationen mit kontrollierbaren Detaillevels und Transformationsparametern dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- Menger Sponge EXTENDED.clbnode - Das Haupt-COOLLAB 3D-Form Node
- Menger Sponge EXTENDED.clbnode.presets.json - Preset-Konfigurationen inklusive "LivingBuilding with Shiftet Apartements", "Default - Standart", "INSIDER-ONE by nearfield details", "Stuco Sleshed BRO", "Friction H2-B", "DeStructUR" und "CompacT 106" Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt faszinierende fraktale Lichtinteraktionen durch komplexe geometrische Strukturen

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig mit optimierten SDF-Berechnungen (Vorsicht bei hohen Detail-Werten)
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung
- Basierend auf: Erweitertem Menger-Schwamm-Fraktal-Algorithmus mit Faltungstransformationen

**📜 Lizenz & Attribution**

*Mathematische Grundlage:*

- Basierend auf dem klassischen Menger-Schwamm-Fraktal-Konzept
- Erweitert mit Faltungstransformationen und Skalierungsmanipulationen
- Ursprüngliches Menger-Schwamm-Konzept von Karl Menger (1926)

*Dieses COOLLAB Node:*

- Basierend auf dem ursprünglichen "Menger Sponge" Coollab Node
- Erweiterungen programmiert von claude.ai im Sonnet-4 Modell von Anthropic PBC auf einem "KostenlosPlan" von bennoH.
- Durch Anweisungen und unter der Aufsicht von bennoH.
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist keine einfache Menger-Schwamm-Implementation. Die EXTENDED Version bietet umfassende Kontrolle über Fraktalgenerierung:
- 🔢 **Erweiterte Iterationskontrolle**: Detaillierte Kontrolle über Fraktaliterationen mit Startpunkten und Detaillevels
- ➕ **Kreuzstruktur-Manipulation**: Anpassbare Kreuzdicke für variierende strukturelle Dichte
- 📐 **Geometrische Beschränkungen**: Würfelgrößen-Kontrolle zur Begrenzung und Formung der Gesamtstruktur
- 🔄 **Faltungstransformationen**: Erweiterte Faltungsoperationen mit Faktor-, Skalierungs- und Versatz-Kontrollen
- 📏 **Skalierungs-Management**: Präzise Kontrolle über Skalierungsreduktion zwischen Iterationen
- 🎛️ **Kreative Flexibilität**: Erweiterte Parameter ermöglichen nicht-traditionelle Menger-Schwamm-Variationen

### 🎛️ Parameter

#### 🔢 Fraktalstruktur-Kontrollen
- 🎯 **Detail** (Integer, 0-12+): Anzahl der Fraktaliterationen. Höhere Werte erzeugen detailliertere Kreuzstrukturen, erhöhen aber die Rechenkosten. **Warnung**: Werte über 8 können die Performance erheblich beeinträchtigen
- ➕ **Cross Thickness** (Float, 0.0-2.0+): Kontrolliert die Dicke der Kreuzarme. Niedrigere Werte erzeugen dünnere Kreuze und offenere Strukturen
- 📐 **Cube Size** (Float, 0.0-5.0+): Größe des begrenzenden Würfels, der die Kreuzform begrenzt. Beeinflusst die Gesamtgrenze der Fraktalstruktur

#### 🔧 Skalierungs- und Transformations-Kontrollen
- 📏 **Base Scale** (Float, 0.1-2.0): Startskalierungsfaktor für das Fraktal. Beeinflusst die Gesamtgröße und kann interessante Skalierungseffekte erzeugen
- 🎯 **Iteration Start** (Float, 0.0-5.0): Startiterations-Versatz. Verschiebt, welches Fraktallevel beginnt, ermöglicht Erkundung des Fraktalinneren
- 🔄 **Scale Reduction** (Float, 1.5-5.0): Wie stark die Skalierung bei jeder Iteration abnimmt. Höhere Werte erzeugen schnelleren Zerfall und kompaktere Strukturen

#### 🌀 Erweiterte Faltungs-Kontrollen
- 🔄 **Fold Factor** (Float, -1.0-1.0): Kontrolliert die Faltungstransformation zwischen Iterationen. Negative Werte erzeugen inverse Faltungseffekte
- 📏 **Fold Scale** (Float, 2.0-10.0): Skalierungsfaktor für die Faltungsoperation. Beeinflusst Abstand und Verteilung der Fraktalelemente
- 🎯 **Fold Offset** (Float, 0.0-5.0): Versatz, der während der Faltungstransformation angewendet wird. Verschiebt das Faltungszentrum und erzeugt asymmetrische Effekte

### ⚙️ Technische Implementation
Die erweiterte Menger-Schwamm-Generierung funktioniert durch ausgeklügelte mathematische Stufen:
1. 🎯 **Kreuz-SDF-Berechnung**: Erzeugt die grundlegende Kreuzstruktur mit absoluten Positionskoordinaten und Dickenkontrolle
2. 📐 **Würfelgrenze-Anwendung**: Wendet kubische Beschränkungen an, um die Kreuzform innerhalb definierter Grenzen zu begrenzen
3. 🔄 **Iterative Fraktalgenerierung**: Führt mehrere Iterationen mit Skalierungsreduktion und Positionstransformationen durch
4. 🌀 **Faltungstransformationen**: Wendet fraktionale Faltungsoperationen mit benutzerdefinierten Faktoren, Skalierungen und Versätzen an
5. 📏 **Distance Field Kombination**: Kombiniert alle Iterationen mit maximalen Distanzoperationen für korrekte Fraktalstruktur

### 🎨 Kreative Anwendungen
- 🏛️ **Architektonische Frameworks**: Komplexe Struktursysteme, Gerüste oder Gebäude-Frameworks mit Fraktaleigenschaften entwerfen
- 🎭 **Abstrakte Skulpturen**: Mathematische Kunstinstallationen und geometrische Skulpturen für Galerien oder öffentliche Räume erstellen
- 🏢 **Stadtplanung**: Komplexe urbane Strukturen, Gittersysteme oder architektonische Details mit Fraktalcharakteristiken generieren
- 🎮 **Spielumgebungs-Design**: Futuristische Strukturen, Alien-Architekturen oder komplexe Level-Geometrie mit mathematischer Präzision bauen
- 🔬 **Mathematische Visualisierung**: Fraktalmathematik, Selbstähnlichkeitskonzepte und geometrische Progression erkunden und visualisieren
- 🎨 **Prozedurale Kunst**: Komplexe geometrische Muster und Strukturen für digitale Kunst und Visualisierungsprojekte erstellen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Detail**-Werten zwischen 3-6 für gute Balance zwischen Komplexität und Performance beginnen
- ✅ **Cross Thickness** um 0.8-1.2 für gut definierte Strukturelemente verwenden
- ✅ **Cube Size** zwischen 3.0-4.5 für gute proportionale Grenzen setzen
- ✅ **Base Scale** um 0.5-1.0 für Standard-Fraktalproportionen halten
- ✅ Mit **Fold Factor**-Werten zwischen -0.5 und 0.5 für interessante Variationen experimentieren
- ✅ **Scale Reduction** um 3.0 für traditionelles Menger-Schwamm-Verhalten verwenden
- ⚠️ **Performance-Warnung**: Vorsicht bei **Detail**-Werten über 8, besonders in Kombination mit anderen komplexen Nodes

### 🎬 Animations-Setup Anleitung
**Menger Sponge EXTENDED** ist perfekt für mathematische und architektonische Animationen! Die Preset-Namen zeigen verschiedene strukturelle und künstlerische Ansätze an:

**Preset-Architekturen verstehen:**
Jedes Preset demonstriert verschiedene Fraktalansätze:
- **"LivingBuilding with Shiftet Apartements"**: Architektonische Interpretation mit verschobenem Iterationsstart
- **"Default - Standart"**: Klassische Menger-Schwamm-Konfiguration für traditionelle Fraktalerscheinung
- **"INSIDER-ONE by nearfield details"**: Hochdetail-Konfiguration fokussiert auf Innenstruktur-Erkundung
- **"Stuco Sleshed BRO"**: Künstlerische Variation mit negativen Fold-Faktoren für einzigartige geometrische Effekte
- **"Friction H2-B"**: Hochdetail-Fraktal mit erhöhter Kreuzdicke für dichte Strukturen
- **"DeStructUR"**: Dekonstruierte Fraktal-Erscheinung mit dicken Kreuzelementen
- **"CompacT 106"**: Kompakte Fraktal-Konfiguration mit modifizierter Skalierungsreduktion

**Animations-Empfehlungen:**
1. 🔢 **Für Fraktal-Wachstum**: **Detail** von 1 zum Zielwert animieren, um Fraktal-Konstruktionsprozess zu zeigen
2. ➕ **Für Strukturänderungen**: **Cross Thickness** variieren, um strukturelle Dichteübergänge zu zeigen
3. 🎯 **Für Innen-Erkundung**: **Iteration Start** animieren, um durch Fraktalebenen zu reisen
4. 🔄 **Für geometrisches Morphing**: **Fold Factor** langsam ändern für glatte geometrische Transformationen
5. 📏 **Für Skalierungs-Dynamik**: **Scale Reduction** animieren, um verschiedene Fraktal-Zerfallsraten zu zeigen

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.1) → **Ramp** (Min: 1, Max: 6) → **Detail** (für Fraktal-Wachstum)
2. 🕐 **Time Node** (Geschwindigkeit: 0.2) → **Sine Wave** (Min: 0.5, Max: 1.5, Period: 12.0) → **Cross Thickness**
3. 🕐 **Time Node** (Geschwindigkeit: 0.05) → **Sine Wave** (Min: 0, Max: 3, Period: 20.0) → **Iteration Start**
4. 🕐 **Time Node** (Geschwindigkeit: 0.15) → **Sine Wave** (Min: -0.3, Max: 0.3, Period: 15.0) → **Fold Factor**
5. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.03) → **Y-Achse** für langsame mathematische Präsentation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Enhanced Menger Sponge fractal algorithm 🧊  
**Basierend auf**: Erweitertem Menger-Schwamm-Fraktal-Algorithmus 🧊

**Category**: 3D Shapes > Fractals 🔢  
**Kategorie**: 3D-Formen > Fraktale 🔢

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "LivingBuilding with Shiftet Apartements" - Architectural interpretation with shifted iteration parameters
- "Default - Standart" - Classic Menger Sponge configuration for traditional fractal behavior
- "INSIDER-ONE by nearfield details" - High-detail exploration focused on interior fractal structures
- "Stuco Sleshed BRO" - Artistic variation with negative fold factors for unique geometric effects
- "Friction H2-B" - High-detail fractal with enhanced cross thickness for dense structural elements
- "DeStructUR" - Deconstructed fractal appearance with thick cross elements and high detail
- "CompacT 106" - Compact fractal configuration with modified scale reduction for tighter structures

**Verfügbare Presets**: 
- "LivingBuilding with Shiftet Apartements" - Architektonische Interpretation mit verschobenen Iterations-Parametern
- "Default - Standart" - Klassische Menger-Schwamm-Konfiguration für traditionelles Fraktal-Verhalten
- "INSIDER-ONE by nearfield details" - Hochdetail-Erkundung fokussiert auf innere Fraktalstrukturen
- "Stuco Sleshed BRO" - Künstlerische Variation mit negativen Fold-Faktoren für einzigartige geometrische Effekte
- "Friction H2-B" - Hochdetail-Fraktal mit erhöhter Kreuzdicke für dichte Strukturelemente
- "DeStructUR" - Dekonstruierte Fraktal-Erscheinung mit dicken Kreuzelementen und hohem Detail
- "CompacT 106" - Kompakte Fraktal-Konfiguration mit modifizierter Skalierungsreduktion für dichtere Strukturen

**Performance Notes / Performance-Hinweise**:
- ⚠️ **Detail values above 8**: May cause significant performance impact / Werte über 8 können erhebliche Performance-Auswirkungen haben
- ✅ **Recommended range**: Detail 3-6 for real-time applications / Empfohlener Bereich: Detail 3-6 für Echtzeitanwendungen
- 🔧 **Optimization tip**: Lower Cross Thickness values render faster / Optimierungs-Tipp: Niedrigere Cross Thickness-Werte rendern schneller

**🔗 Links**

- Original Menger Sponge concept by Karl Menger (1926)
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - August 2025
