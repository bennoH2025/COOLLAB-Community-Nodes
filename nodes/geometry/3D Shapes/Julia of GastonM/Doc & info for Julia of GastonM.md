[English](#-english) | [Deutsch](#-deutsch)
---

# 🌀 Julia of GastonM Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Julia of GastonM** node creates sophisticated 3D fractal structures based on the mathematical foundations of Gaston Maurice Julia's groundbreaking work from 1918. This procedural geometry generator combines Julia set mathematics with Mandelbox folding techniques to produce complex, organic-looking fractal geometries with crystalline and smooth organic elements. The node merges historical mathematical discoveries with modern 3D rendering capabilities.
& It generates stunning mathematical fractals that can serve as abstract art pieces, architectural decorative elements, or complex geometric foundations for advanced 3D compositions.

**📋 Files Included**

- Julia of GastonM.clbnode - The main COOLLAB 3D shape node
- Julia of GastonM.clbnode.presets.json - Preset configurations including "Julia-1918", "Mandelbox nucleus", "Julia's softshell", "Amondecartouche FengShui", and "Kris La b" effects

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
- Works excellently with raymarching renderers and creates complex light interaction patterns

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Iteration-dependent (1-20 iterations recommended)
- Rendering: Compatible with raymarching and mesh generation

**📜 License & Attribution**

*Mathematical Foundation:*

- Based on Gaston Maurice Julia's theorem from "Mémoire sur l'itération des fonctions rationnelles" (1918)
- Special credits to Pierre Fatou and Benoit Mandelbrot for fractal mathematics contributions
- Based on a Mandelbulber-setup by bennoH

*This COOLLAB Node:*

- Idea and project coordination by bennoH.
- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not a simple geometric primitive. The Julia of GastonM node combines century-old mathematical discoveries with modern 3D techniques:
- 🔬 **Historical Mathematics**: Based on Julia's 1918 mathematical theorem for rational function iteration
- 📦 **Box Folding**: Creates angular, crystalline structural elements
- 🔵 **Sphere Folding**: Adds smooth, organic curved surfaces  
- 🔄 **Iterative Processing**: Builds mathematical complexity through controlled iteration cycles
- 🎯 **Julia Set Offset**: 3D vector control for fractal variation and morphing effects

### 🎛️ Parameters

#### 🔧 Core Fractal Controls
- 🔢 **Iterations** (Integer, 1-20): Controls fractal complexity and computational detail level. Higher values create more intricate structures but require more processing power
- 📏 **Scale** (Float, 0.1-5.0): Main scaling factor affecting overall fractal structure. Values around 2.5-3.0 typically produce well-balanced forms
- 🔵 **Min Radius** (Float, 0.1-1.0): Minimum radius for sphere folding operations. Controls the smoothness of curved surfaces
- 📦 **Box Limit** (Float, 0.5-2.0): Boundary limits for box folding operations. Affects the angularity and sharpness of structural edges

#### 🎯 Advanced Shape Controls
- 🔴 **Fixed Radius** (Float, 0.1-2.0): Fixed radius multiplier for sphere folding operations. Fine-tunes the curvature characteristics
- 🎯 **Julia Offset** (vec3, xyz vector): 3D offset vector for Julia set variation. This is the key parameter for morphing and animation effects
- ✨ **Detail** (Float, 0.01-2.0): Surface detail multiplier for fine structural elements. Higher values enhance surface complexity

### ⚙️ Technical Implementation
The fractal generation works through sophisticated mathematical stages:
1. 🔄 **Initialization**: Position and Julia offset setup with scaling preparation
2. 📦 **Box Folding**: Clamps coordinates within box limits and applies reflection folding
3. 🔵 **Sphere Folding**: Applies radial folding based on distance calculations with controllable radius parameters
4. 📏 **Scaling & Translation**: Applies scale factor and adds Julia offset for variation
5. 🔄 **Iterative Process**: Repeats folding operations for specified iteration count
6. ✨ **Distance Field Output**: Generates final signed distance with detail modulation

### 🎨 Creative Applications
- 🏛️ **Architectural Visualization**: Create complex decorative elements, facades, or structural details
- 🧬 **Scientific Visualization**: Represent molecular structures, crystal formations, or mathematical concepts
- 🎮 **Game Environment Design**: Generate alien landscapes, crystal caves, or fantasy architectural elements
- 🎨 **Abstract Digital Art**: Create mathematically precise yet organically appealing compositions
- 🔬 **Educational Content**: Visualize complex mathematical concepts and fractal theory

### 💡 Tips for Best Results
- ✅ Start with **Iterations** around 5-9 for good detail without excessive computation
- ✅ Use **Scale** values between 2.5-3.1 for well-balanced fractal structures
- ✅ Keep **Min Radius** at 0.25 initially, adjust for surface smoothness control
- ✅ Set **Box Limit** around 1.0-1.1 for balanced angular/curved element ratio
- ✅ Animate **Julia Offset** values gradually for smooth morphing transitions
- ✅ Use **Detail** values below 1.0 for softer surfaces, above 1.0 for sharper definition

### 🎬 Animation Setup Guide
**Julia of GastonM** is designed for stunning fractal animations! The preset names indicate the animation characteristics:

**Understanding Preset Configurations:**
Each preset demonstrates different fractal characteristics and animation potential:

**Animation Recommendations:**
1. 🕐 **For Morphing Effects**: Animate **Julia Offset** components slowly over time
   - X-axis animation: Creates lateral transformation effects
   - Y-axis animation: Produces vertical structural changes  
   - Z-axis animation: Generates depth-based morphing
2. 🔄 **For Detail Animation**: Connect **Detail** parameter to sine waves for pulsing surface effects
3. 📏 **For Scale Animation**: Animate **Scale** parameter for growing/shrinking fractal effects
4. 🔢 **For Complexity Animation**: Gradually change **Iterations** for evolving detail levels

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.3) → **Sine Wave** (Min: -2.0, Max: 2.0, Period: 8.0) → **Julia Offset X**
2. 🕐 **Time Node** (Speed: 0.2) → **Sine Wave** (Min: -1.0, Max: 1.0, Period: 12.0) → **Julia Offset Y**
3. 🕐 **Time Node** (Speed: 0.5) → **Sine Wave** (Min: 0.5, Max: 1.5, Period: 6.0) → **Detail**
4. 🔄 **Rotate Node** with **Time Node** (Speed: 0.1) → **Y-axis** for slow rotation

**🔗 Links**

- Gaston Maurice Julia - Mathematical Foundation (1918)
- COOLLAB Official Website
- Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - January 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Julia of GastonM** Node erzeugt anspruchsvolle 3D-Fraktalstrukturen basierend auf den mathematischen Grundlagen von Gaston Maurice Julias bahnbrechender Arbeit von 1918. Dieser prozedurale Geometrie-Generator kombiniert Julia-Mengen-Mathematik mit Mandelbox-Faltungstechniken, um komplexe, organisch wirkende Fraktalgeometrien mit kristallinen und glatten organischen Elementen zu produzieren. Der Node vereint historische mathematische Entdeckungen mit modernen 3D-Rendering-Fähigkeiten.
& generiert beeindruckende mathematische Fraktale, die als abstrakte Kunstwerke, architektonische Dekorelemente oder komplexe geometrische Grundlagen für fortgeschrittene 3D-Kompositionen dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- Julia of GastonM.clbnode - Das Haupt-COOLLAB 3D-Form Node
- Julia of GastonM.clbnode.presets.json - Preset-Konfigurationen inklusive "Julia-1918", "Mandelbox nucleus", "Julia's softshell", "Amondecartouche FengShui" und "Kris La b" Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt komplexe Lichtinteraktionsmuster

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Iterationsabhängig (1-20 Iterationen empfohlen)
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung

**📜 Lizenz & Attribution**

*Mathematische Grundlage:*

- Basierend auf Gaston Maurice Julias Theorem aus "Mémoire sur l'itération des fonctions rationnelles" (1918)
- Besondere Würdigung für Pierre Fatou und Benoit Mandelbrot für Beiträge zur Fraktalmathematik
- Basierend auf einem Mandelbulber-Setup von bennoH

*Dieses COOLLAB Node:*

- Idee und Projektkoordination von bennoH.
- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC auf einem "KostenlosPlan" von bennoH.
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist keine einfache geometrische Primitive. Der Julia of GastonM Node kombiniert jahrhundertealte mathematische Entdeckungen mit modernen 3D-Techniken:
- 🔬 **Historische Mathematik**: Basierend auf Julias mathematischem Theorem von 1918 für rationale Funktionsiteration
- 📦 **Box-Faltung**: Erzeugt kantige, kristalline Strukturelemente
- 🔵 **Kugel-Faltung**: Fügt glatte, organische gekrümmte Oberflächen hinzu  
- 🔄 **Iterative Verarbeitung**: Baut mathematische Komplexität durch kontrollierte Iterationszyklen auf
- 🎯 **Julia-Mengen-Versatz**: 3D-Vektor-Kontrolle für Fraktalvariation und Morphing-Effekte

### 🎛️ Parameter

#### 🔧 Kern-Fraktal-Kontrollen
- 🔢 **Iterations** (Integer, 1-20): Kontrolliert Fraktalkomplexität und rechnerischen Detailgrad. Höhere Werte erzeugen komplexere Strukturen, benötigen aber mehr Rechenleistung
- 📏 **Scale** (Float, 0.1-5.0): Hauptskalierungsfaktor, der die gesamte Fraktalstruktur beeinflusst. Werte um 2.5-3.0 produzieren typischerweise gut ausbalancierte Formen
- 🔵 **Min Radius** (Float, 0.1-1.0): Mindestradius für Kugelfaltungsoperationen. Kontrolliert die Glätte gekrümmter Oberflächen
- 📦 **Box Limit** (Float, 0.5-2.0): Grenzwerte für Boxfaltungsoperationen. Beeinflusst die Winkligkeit und Schärfe struktureller Kanten

#### 🎯 Erweiterte Form-Kontrollen
- 🔴 **Fixed Radius** (Float, 0.1-2.0): Fester Radius-Multiplikator für Kugelfaltungsoperationen. Feinabstimmung der Krümmungscharakteristiken
- 🎯 **Julia Offset** (vec3, xyz-Vektor): 3D-Versatzvektor für Julia-Mengen-Variation. Dies ist der Schlüsselparameter für Morphing- und Animationseffekte
- ✨ **Detail** (Float, 0.01-2.0): Oberflächendetail-Multiplikator für feine Strukturelemente. Höhere Werte verstärken die Oberflächenkomplexität

### ⚙️ Technische Implementation
Die Fraktalgenerierung funktioniert durch ausgeklügelte mathematische Stufen:
1. 🔄 **Initialisierung**: Positions- und Julia-Versatz-Setup mit Skalierungsvorbereitung
2. 📦 **Box-Faltung**: Begrenzt Koordinaten innerhalb der Box-Limits und wendet Reflexionsfaltung an
3. 🔵 **Kugel-Faltung**: Wendet radiale Faltung basierend auf Entfernungsberechnungen mit kontrollierbaren Radiusparametern an
4. 📏 **Skalierung & Translation**: Wendet Skalierungsfaktor an und fügt Julia-Versatz für Variation hinzu
5. 🔄 **Iterativer Prozess**: Wiederholt Faltungsoperationen für die angegebene Iterationsanzahl
6. ✨ **Distance Field Ausgabe**: Generiert finale Signed Distance mit Detailmodulation

### 🎨 Kreative Anwendungen
- 🏛️ **Architektur-Visualisierung**: Komplexe Dekorelemente, Fassaden oder Strukturdetails erstellen
- 🧬 **Wissenschaftliche Visualisierung**: Molekularstrukturen, Kristallformationen oder mathematische Konzepte darstellen
- 🎮 **Spielumgebungs-Design**: Alien-Landschaften, Kristallhöhlen oder Fantasy-Architekturelemente generieren
- 🎨 **Abstrakte Digitale Kunst**: Mathematisch präzise und dennoch organisch ansprechende Kompositionen erstellen
- 🔬 **Bildungsinhalte**: Komplexe mathematische Konzepte und Fraktaltheorie visualisieren

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Iterations** um 5-9 für gute Details ohne übermäßige Berechnung beginnen
- ✅ **Scale**-Werte zwischen 2.5-3.1 für gut ausbalancierte Fraktalstrukturen verwenden
- ✅ **Min Radius** zunächst bei 0.25 belassen, für Oberflächenglätte-Kontrolle anpassen
- ✅ **Box Limit** um 1.0-1.1 für ausgewogenes Verhältnis kantiger/gekrümmter Elemente setzen
- ✅ **Julia Offset**-Werte allmählich für sanfte Morphing-Übergänge animieren
- ✅ **Detail**-Werte unter 1.0 für weichere Oberflächen, über 1.0 für schärfere Definition verwenden

### 🎬 Animations-Setup Anleitung
**Julia of GastonM** ist für beeindruckende Fraktal-Animationen konzipiert! Die Preset-Namen zeigen die Animationscharakteristiken an:

**Preset-Konfigurationen verstehen:**
Jedes Preset demonstriert verschiedene Fraktalcharakteristiken und Animationspotential:

**Animations-Empfehlungen:**
1. 🕐 **Für Morphing-Effekte**: **Julia Offset**-Komponenten langsam über die Zeit animieren
   - X-Achsen-Animation: Erzeugt laterale Transformationseffekte
   - Y-Achsen-Animation: Produziert vertikale Strukturveränderungen  
   - Z-Achsen-Animation: Generiert tiefenbasiertes Morphing
2. 🔄 **Für Detail-Animation**: **Detail**-Parameter mit Sinuswellen für pulsierende Oberflächeneffekte verbinden
3. 📏 **Für Skalierungs-Animation**: **Scale**-Parameter für wachsende/schrumpfende Fraktaleffekte animieren
4. 🔢 **Für Komplexitäts-Animation**: **Iterations** allmählich ändern für sich entwickelnde Detailgrade

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.3) → **Sine Wave** (Min: -2.0, Max: 2.0, Period: 8.0) → **Julia Offset X**
2. 🕐 **Time Node** (Geschwindigkeit: 0.2) → **Sine Wave** (Min: -1.0, Max: 1.0, Period: 12.0) → **Julia Offset Y**
3. 🕐 **Time Node** (Geschwindigkeit: 0.5) → **Sine Wave** (Min: 0.5, Max: 1.5, Period: 6.0) → **Detail**
4. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.1) → **Y-Achse** für langsame Rotation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Gaston Maurice Julia's mathematical theorem (1918) 🔬  
**Basierend auf**: Gaston Maurice Julias mathematischem Theorem (1918) 🔬

**Category**: 3D Shapes > Fractals 🌀  
**Kategorie**: 3D-Formen > Fraktale 🌀

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "Julia-1918 in the Mandelbox-2025" - Classic Julia fractal with modern Mandelbox enhancement
- "Mandelbox nucleus" - Core structure with organic center formation
- "Julia's softshell" - Soft, shell-like surface with subtle detail variations
- "Amondecartouche FengShui" - Harmonious balanced structure with minimal surface detail
- "Kris La b" - Crystalline formation with X-axis offset creating asymmetric beauty

**Verfügbare Presets**: 
- "Julia-1918 in the Mandelbox-2025" - Klassisches Julia-Fraktal mit moderner Mandelbox-Verbesserung
- "Mandelbox nucleus" - Kernstruktur mit organischer Zentrumsbildung
- "Julia's softshell" - Weiche, muschelartige Oberfläche mit subtilen Detailvariationen
- "Amondecartouche FengShui" - Harmonisch ausgewogene Struktur mit minimalen Oberflächendetails
- "Kris La b" - Kristalline Formation mit X-Achsen-Versatz für asymmetrische Schönheit

**🔗 Links**

- Gaston Maurice Julia - Mathematical Foundation (1918)
- COOLLAB Official Website
- Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - January 2025
