[English](#-english) | [Deutsch](#-deutsch)
---

# 🏗️ FrameworkFract Node Documentation

## 🇬🇧 English

### 📋 Overview
The **FrameworkFract** node creates complex fractal framework structures based on Mandelbulber-inspired mathematics developed by bennoH. This procedural geometry generator produces intricate 3D fractal architectures through iterative folding, scaling, and coordinate transformations. The node combines box folding operations with coordinate sorting to create symmetrical yet complex geometric frameworks that can serve as architectural structures, abstract sculptures, or mathematical visualizations. The fractal algorithm generates self-similar patterns at multiple scales, creating frameworks that maintain structural coherence while exhibiting infinite geometric detail.

& It generates stunning fractal framework structures that can serve as futuristic architectural systems, abstract geometric installations, mathematical art pieces, or complex structural frameworks with controllable iteration depth and transformation parameters.

**📋 Files Included**

- FrameworkFract.clbnode - The main COOLLAB 3D shape node
- FrameworkFract.clbnode.presets.json - Preset configurations including "Cyberland of Orux", "TunTun ars", "Pentrax", "Jorno", "JalRoom", "60tis Patern", and "Buntqun" effects

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
- Works excellently with raymarching renderers and creates fascinating geometric complexity through fractal repetition and box folding

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable with optimized SDF calculations (be careful with high iteration values)
- Rendering: Compatible with raymarching and mesh generation
- Mathematical Foundation: Based on Mandelbulber fractal techniques with box folding operations

**📜 License & Attribution**

*Mathematical Foundation:*

- Based on a Mandelbulber-setup by bennoH
- Inspired by fractal mathematics concepts
- Special credits to Benoit Mandelbrot as the father of fractal mathematics and basic formula

*This COOLLAB Node:*

- Idea and project coordination by bennoH.
- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not a simple geometric primitive. The FrameworkFract node combines advanced fractal mathematics with architectural design principles:
- 🔄 **Iterative Fractal Generation**: Multiple iterations create self-similar structures at different scales
- 📐 **Box Folding Operations**: Advanced modulo-based folding techniques create complex geometric patterns
- 🔀 **Coordinate Sorting**: Optional coordinate swapping creates enhanced symmetrical variations
- 📏 **Multi-Scale Control**: Independent control over iteration scaling and final output scaling
- 🎯 **3D Offset Transformations**: Vector offset controls add asymmetry and variation to each iteration
- 🏗️ **Y-Axis Framework Focus**: Specialized distance calculation creates framework-like structural appearance

### 🎛️ Parameters

#### 🔢 Fractal Generation Controls
- 🎯 **Iterations** (Integer, 1-20): Number of fractal iterations. Higher values create more detailed and complex structures but increase computational cost. **Recommended range: 2-8**
- 📏 **Scale** (Float, 0.5-3.0): Scale factor applied each iteration. Values >1.0 create expanding fractals, <1.0 create contracting fractals. **Sweet spot: 1.2-2.8**
- 📐 **Fold Size** (Float, 0.1-1000+): Size of the box folding operation. Controls the scale of geometric folding patterns. Large values (800+) create different structural effects

#### 🔧 Transformation Controls
- 🔀 **Enable Sorting** (Boolean): Enable coordinate sorting/swapping for enhanced symmetry. Creates more regular, symmetrical patterns when enabled
- 📏 **Final Scale** (Float, -1.0-5.0): Final scaling factor applied to the entire result. Negative values can create inverted structures, positive values adjust overall size
- 🎯 **Offset** (vec3, xyz vector): Translation offset added each iteration. Creates asymmetric variations and breaks perfect symmetry for more organic and complex results

### ⚙️ Technical Implementation
The framework fractal generation works through sophisticated mathematical operations:
1. 🔄 **4D Vector Processing**: Utilizes vec4 with homogeneous coordinates for advanced transformations
2. 🔀 **Conditional Coordinate Sorting**: Optional X-Z and Z-Y coordinate swapping for symmetrical properties
3. 📐 **Absolute Value Folding**: Applies absolute value operations to create reflective symmetry
4. 🏗️ **Modulo Box Folding**: Uses modulo operations with adjustable fold size to create repeating box-like patterns
5. 🎯 **Iterative Offset Application**: Adds 3D offset vectors for positional variation between iterations
6. 📏 **Scale Transformation**: Applies scaling factors to control fractal expansion or contraction
7. 🏗️ **Y-Axis Distance Projection**: Final calculation focuses on Y-axis distance for framework-like structural appearance

### 🎨 Creative Applications
- 🏛️ **Futuristic Architecture**: Design complex building frameworks, space station structures, or sci-fi construction systems
- 🎭 **Abstract Sculptures**: Create mathematical art installations with infinite geometric detail and fractal complexity
- 🏢 **Urban Infrastructure**: Generate complex bridge structures, architectural details, or urban planning frameworks
- 🎮 **Game Environment Design**: Build alien architectures, futuristic structures, or complex level geometry with mathematical precision
- 🔬 **Mathematical Visualization**: Explore fractal mathematics, self-similarity concepts, and geometric transformation principles
- 🎨 **Procedural Art**: Create complex geometric patterns for digital art, architectural visualization, and installation projects
- 🏗️ **Engineering Visualization**: Visualize complex structural systems, lattice frameworks, or construction details

### 💡 Tips for Best Results
- ✅ Start with **Iterations** values between 2-5 for good balance of complexity and performance
- ✅ Use **Scale** around 1.2-2.2 for expanding fractal structures
- ✅ Experiment with **Fold Size** values: small (1-10) for fine detail, large (800+) for mega-structures
- ✅ Keep **Enable Sorting** enabled for more symmetrical, architectural results
- ✅ Try negative **Final Scale** values (-0.1 to -0.2) for interesting inverted structures
- ✅ Use **Offset** X and Y values between 7-8 for good structural variation
- ⚠️ **Performance Note**: High **Iterations** (8+) with complex **Fold Size** may impact performance

### 🎬 Animation Setup Guide
**FrameworkFract** is perfect for futuristic and architectural animations! The preset names indicate different structural and stylistic approaches:

**Understanding Preset Architectures:**
Each preset demonstrates different fractal framework approaches:
- **"Cyberland of Orux"**: Low-iteration cyber structure with moderate scale (2 iterations, scale 2.22)
- **"TunTun ars"**: Artistic medium complexity framework (5 iterations, scale 2.22)
- **"Pentrax"**: Precision framework with fine final scaling (5 iterations, final scale 0.1)
- **"Jorno"**: High-scale organic framework (5 iterations, scale 2.79)
- **"JalRoom"**: Complex room-like structure (8 iterations, mega fold size 987)
- **"60tis Patern"**: Retro 60s pattern with contracting scale (8 iterations, scale 0.75, negative final scale)
- **"Buntqun"**: Colorful complex structure (8 iterations, neutral scale 1.07, mega fold size)

**Animation Recommendations:**
1. 🔢 **For Structural Growth**: Animate **Iterations** from 1 to target value to show framework construction
2. 📏 **For Scale Dynamics**: Vary **Scale** to show expanding/contracting fractal behavior
3. 🎯 **For Geometric Morphing**: Animate **Offset** components for dynamic structural transformations
4. 📐 **For Folding Effects**: Slowly change **Fold Size** for dramatic structural transitions
5. 🔀 **For Symmetry Breaks**: Toggle **Enable Sorting** for symmetry/asymmetry transitions

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.1) → **Ramp** (Min: 1, Max: 6) → **Iterations** (for framework growth)
2. 🕐 **Time Node** (Speed: 0.2) → **Sine Wave** (Min: 1.0, Max: 2.5, Period: 12.0) → **Scale**
3. 🕐 **Time Node** (Speed: 0.05) → **Sine Wave** (Min: 5, Max: 10, Period: 20.0) → **Offset X**
4. 🕐 **Time Node** (Speed: 0.15) → **Sine Wave** (Min: 0.5, Max: 4.0, Period: 15.0) → **Offset Y**
5. 🔄 **Rotate Node** with **Time Node** (Speed: 0.03) → **Y-axis** for architectural presentation

**🔗 Links**

- Based on Mandelbulber-setup by bennoH
- Special credits to Benoit Mandelbrot for fractal mathematics foundation
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - August 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **FrameworkFract** Node erzeugt komplexe fraktale Framework-Strukturen basierend auf Mandelbulber-inspirierter Mathematik, entwickelt von bennoH. Dieser prozedurale Geometrie-Generator produziert komplizierte 3D-Fraktal-Architekturen durch iterative Faltung, Skalierung und Koordinatentransformationen. Der Node kombiniert Box-Faltungsoperationen mit Koordinatensortierung, um symmetrische aber komplexe geometrische Frameworks zu erstellen, die als architektonische Strukturen, abstrakte Skulpturen oder mathematische Visualisierungen dienen können. Der Fraktal-Algorithmus generiert selbstähnliche Muster in mehreren Maßstäben und erzeugt Frameworks, die strukturelle Kohärenz beibehalten, während sie unendliche geometrische Details aufweisen.

& generiert beeindruckende fraktale Framework-Strukturen, die als futuristische architektonische Systeme, abstrakte geometrische Installationen, mathematische Kunstwerke oder komplexe strukturelle Frameworks mit kontrollierbarer Iterationstiefe und Transformationsparametern dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- FrameworkFract.clbnode - Das Haupt-COOLLAB 3D-Form Node
- FrameworkFract.clbnode.presets.json - Preset-Konfigurationen inklusive "Cyberland of Orux", "TunTun ars", "Pentrax", "Jorno", "JalRoom", "60tis Patern" und "Buntqun" Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt faszinierende geometrische Komplexität durch Fraktal-Wiederholung und Box-Faltung

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig mit optimierten SDF-Berechnungen (Vorsicht bei hohen Iterationswerten)
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung
- Mathematische Grundlage: Basierend auf Mandelbulber-Fraktal-Techniken mit Box-Faltungsoperationen

**📜 Lizenz & Attribution**

*Mathematische Grundlage:*

- Basierend auf einem Mandelbulber-Setup von bennoH
- Inspiriert von Fraktalmathematik-Konzepten
- Besondere Anerkennung an Benoit Mandelbrot als Vater der Fraktalmathematik und Grundformel

*Dieses COOLLAB Node:*

- Idee und Projektkoordination von bennoH.
- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC auf einem "KostenlosPlan" von bennoH.
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist keine einfache geometrische Primitive. Der FrameworkFract Node kombiniert erweiterte Fraktalmathematik mit architektonischen Designprinzipien:
- 🔄 **Iterative Fraktalgenerierung**: Mehrere Iterationen erzeugen selbstähnliche Strukturen in verschiedenen Maßstäben
- 📐 **Box-Faltungsoperationen**: Erweiterte Modulo-basierte Faltungstechniken erzeugen komplexe geometrische Muster
- 🔀 **Koordinatensortierung**: Optionales Koordinatentauschen erzeugt verstärkte symmetrische Variationen
- 📏 **Multi-Skalierungs-Kontrolle**: Unabhängige Kontrolle über Iterations-Skalierung und finale Ausgabe-Skalierung
- 🎯 **3D-Versatz-Transformationen**: Vektor-Versatz-Kontrollen fügen Asymmetrie und Variation zu jeder Iteration hinzu
- 🏗️ **Y-Achsen-Framework-Fokus**: Spezialisierte Distanzberechnung erzeugt framework-ähnliche strukturelle Erscheinung

### 🎛️ Parameter

#### 🔢 Fraktalgenerierungs-Kontrollen
- 🎯 **Iterations** (Integer, 1-20): Anzahl der Fraktaliterationen. Höhere Werte erzeugen detailliertere und komplexere Strukturen, erhöhen aber die Rechenkosten. **Empfohlener Bereich: 2-8**
- 📏 **Scale** (Float, 0.5-3.0): Skalierungsfaktor, der bei jeder Iteration angewendet wird. Werte >1.0 erzeugen expandierende Fraktale, <1.0 erzeugen kontrahierende Fraktale. **Sweet Spot: 1.2-2.8**
- 📐 **Fold Size** (Float, 0.1-1000+): Größe der Box-Faltungsoperation. Kontrolliert den Maßstab geometrischer Faltungsmuster. Große Werte (800+) erzeugen verschiedene strukturelle Effekte

#### 🔧 Transformations-Kontrollen
- 🔀 **Enable Sorting** (Boolean): Koordinatensortierung/-tausch für verstärkte Symmetrie aktivieren. Erzeugt regelmäßigere, symmetrischere Muster wenn aktiviert
- 📏 **Final Scale** (Float, -1.0-5.0): Finaler Skalierungsfaktor, der auf das gesamte Ergebnis angewendet wird. Negative Werte können invertierte Strukturen erzeugen, positive Werte passen die Gesamtgröße an
- 🎯 **Offset** (vec3, xyz-Vektor): Translationsversatz, der bei jeder Iteration hinzugefügt wird. Erzeugt asymmetrische Variationen und bricht perfekte Symmetrie für organischere und komplexere Ergebnisse

### ⚙️ Technische Implementation
Die Framework-Fraktalgenerierung funktioniert durch ausgeklügelte mathematische Operationen:
1. 🔄 **4D-Vektor-Verarbeitung**: Verwendet vec4 mit homogenen Koordinaten für erweiterte Transformationen
2. 🔀 **Bedingte Koordinatensortierung**: Optionales X-Z- und Z-Y-Koordinatentauschen für symmetrische Eigenschaften
3. 📐 **Absolut-Wert-Faltung**: Wendet Absolut-Wert-Operationen an, um reflektive Symmetrie zu erzeugen
4. 🏗️ **Modulo-Box-Faltung**: Verwendet Modulo-Operationen mit anpassbarer Faltgröße für sich wiederholende box-ähnliche Muster
5. 🎯 **Iterative Versatz-Anwendung**: Fügt 3D-Versatz-Vektoren für Positionsvariation zwischen Iterationen hinzu
6. 📏 **Skalierungs-Transformation**: Wendet Skalierungsfaktoren an, um Fraktal-Expansion oder -Kontraktion zu kontrollieren
7. 🏗️ **Y-Achsen-Distanz-Projektion**: Finale Berechnung fokussiert auf Y-Achsen-Distanz für framework-ähnliche strukturelle Erscheinung

### 🎨 Kreative Anwendungen
- 🏛️ **Futuristische Architektur**: Komplexe Gebäude-Frameworks, Raumstations-Strukturen oder Sci-Fi-Konstruktionssysteme entwerfen
- 🎭 **Abstrakte Skulpturen**: Mathematische Kunstinstallationen mit unendlichen geometrischen Details und Fraktal-Komplexität erstellen
- 🏢 **Urbane Infrastruktur**: Komplexe Brückenstrukturen, architektonische Details oder Stadtplanungs-Frameworks generieren
- 🎮 **Spielumgebungs-Design**: Alien-Architekturen, futuristische Strukturen oder komplexe Level-Geometrie mit mathematischer Präzision bauen
- 🔬 **Mathematische Visualisierung**: Fraktalmathematik, Selbstähnlichkeitskonzepte und geometrische Transformationsprinzipien erkunden
- 🎨 **Prozedurale Kunst**: Komplexe geometrische Muster für digitale Kunst, architektonische Visualisierung und Installationsprojekte erstellen
- 🏗️ **Ingenieur-Visualisierung**: Komplexe Struktursysteme, Gitter-Frameworks oder Konstruktionsdetails visualisieren

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Iterations**-Werten zwischen 2-5 für gute Balance zwischen Komplexität und Performance beginnen
- ✅ **Scale** um 1.2-2.2 für expandierende Fraktalstrukturen verwenden
- ✅ Mit **Fold Size**-Werten experimentieren: klein (1-10) für feine Details, groß (800+) für Mega-Strukturen
- ✅ **Enable Sorting** aktiviert lassen für symmetrischere, architektonische Ergebnisse
- ✅ Negative **Final Scale**-Werte (-0.1 bis -0.2) für interessante invertierte Strukturen ausprobieren
- ✅ **Offset** X- und Y-Werte zwischen 7-8 für gute strukturelle Variation verwenden
- ⚠️ **Performance-Hinweis**: Hohe **Iterations** (8+) mit komplexer **Fold Size** können Performance beeinträchtigen

### 🎬 Animations-Setup Anleitung
**FrameworkFract** ist perfekt für futuristische und architektonische Animationen! Die Preset-Namen zeigen verschiedene strukturelle und stilistische Ansätze an:

**Preset-Architekturen verstehen:**
Jedes Preset demonstriert verschiedene fraktale Framework-Ansätze:
- **"Cyberland of Orux"**: Niedrig-Iterations-Cyber-Struktur mit moderater Skalierung (2 Iterationen, Skalierung 2.22)
- **"TunTun ars"**: Künstlerisches mittlere Komplexitäts-Framework (5 Iterationen, Skalierung 2.22)
- **"Pentrax"**: Präzisions-Framework mit feiner finaler Skalierung (5 Iterationen, finale Skalierung 0.1)
- **"Jorno"**: Hoch-Skalierungs organisches Framework (5 Iterationen, Skalierung 2.79)
- **"JalRoom"**: Komplexe raum-ähnliche Struktur (8 Iterationen, Mega-Faltgröße 987)
- **"60tis Patern"**: Retro-60er-Muster mit kontrahierender Skalierung (8 Iterationen, Skalierung 0.75, negative finale Skalierung)
- **"Buntqun"**: Farbenfrohe komplexe Struktur (8 Iterationen, neutrale Skalierung 1.07, Mega-Faltgröße)

**Animations-Empfehlungen:**
1. 🔢 **Für Struktur-Wachstum**: **Iterations** von 1 zum Zielwert animieren, um Framework-Konstruktion zu zeigen
2. 📏 **Für Skalierungs-Dynamik**: **Scale** variieren, um expandierendes/kontrahierendes Fraktal-Verhalten zu zeigen
3. 🎯 **Für geometrisches Morphing**: **Offset**-Komponenten für dynamische strukturelle Transformationen animieren
4. 📐 **Für Faltungseffekte**: **Fold Size** langsam ändern für dramatische strukturelle Übergänge
5. 🔀 **Für Symmetrie-Brüche**: **Enable Sorting** für Symmetrie/Asymmetrie-Übergänge umschalten

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.1) → **Ramp** (Min: 1, Max: 6) → **Iterations** (für Framework-Wachstum)
2. 🕐 **Time Node** (Geschwindigkeit: 0.2) → **Sine Wave** (Min: 1.0, Max: 2.5, Period: 12.0) → **Scale**
3. 🕐 **Time Node** (Geschwindigkeit: 0.05) → **Sine Wave** (Min: 5, Max: 10, Period: 20.0) → **Offset X**
4. 🕐 **Time Node** (Geschwindigkeit: 0.15) → **Sine Wave** (Min: 0.5, Max: 4.0, Period: 15.0) → **Offset Y**
5. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.03) → **Y-Achse** für architektonische Präsentation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Mandelbulber-setup by bennoH 🏗️  
**Basierend auf**: Mandelbulber-Setup von bennoH 🏗️

**Category**: 3D Shapes > Fractals 🔢  
**Kategorie**: 3D-Formen > Fraktale 🔢

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "Cyberland of Orux" - Low-iteration cyber structure with moderate scaling (2 iterations, scale 2.22, large offset X)
- "TunTun ars" - Artistic medium complexity framework (5 iterations, scale 2.22, same offset pattern)
- "Pentrax" - Precision framework with fine final scaling (5 iterations, final scale 0.1, higher Y offset)
- "Jorno" - High-scale organic framework (5 iterations, scale 2.79, maximum Y offset variation)
- "JalRoom" - Complex room-like structure (8 iterations, mega fold size 987, negative final scale)
- "60tis Patern" - Retro 60s pattern with contracting scale (8 iterations, scale 0.75, mega fold 944)
- "Buntqun" - Colorful complex structure (8 iterations, neutral scale 1.07, mega fold 946)

**Verfügbare Presets**: 
- "Cyberland of Orux" - Niedrig-Iterations-Cyber-Struktur mit moderater Skalierung (2 Iterationen, Skalierung 2.22, großer X-Versatz)
- "TunTun ars" - Künstlerisches mittlere Komplexitäts-Framework (5 Iterationen, Skalierung 2.22, gleiches Versatz-Muster)
- "Pentrax" - Präzisions-Framework mit feiner finaler Skalierung (5 Iterationen, finale Skalierung 0.1, höherer Y-Versatz)
- "Jorno" - Hoch-Skalierungs organisches Framework (5 Iterationen, Skalierung 2.79, maximale Y-Versatz-Variation)
- "JalRoom" - Komplexe raum-ähnliche Struktur (8 Iterationen, Mega-Faltgröße 987, negative finale Skalierung)
- "60tis Patern" - Retro-60er-Muster mit kontrahierender Skalierung (8 Iterationen, Skalierung 0.75, Mega-Falt 944)
- "Buntqun" - Farbenfrohe komplexe Struktur (8 Iterationen, neutrale Skalierung 1.07, Mega-Falt 946)

**Mathematical Credits**: Special thanks to Benoit Mandelbrot for fractal mathematics foundation  
**Mathematische Anerkennung**: Besonderer Dank an Benoit Mandelbrot für die Fraktalmathematik-Grundlage

**🔗 Links**

- Based on Mandelbulber-setup by bennoH
- Special credits to Benoit Mandelbrot for fractal mathematics foundation
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025
