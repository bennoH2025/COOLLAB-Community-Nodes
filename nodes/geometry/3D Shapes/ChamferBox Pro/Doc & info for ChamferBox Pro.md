[English](#-english) | [Deutsch](#-deutsch)
---

# 📦 ChamferBox Pro Node Documentation

## 🇬🇧 English

### 📋 Overview
The **ChamferBox Pro** node creates sophisticated 3D box shapes with rounded edges (chamfers) and optional surface segmentation. This procedural geometry generator produces professional-quality chamfered boxes reminiscent of those found in traditional 3D modeling software like 3ds Max and Strata 3D CX. The node combines precise geometric control with advanced surface detailing capabilities, making it perfect for architectural elements, product design, and technical visualizations.
& It generates clean, professional 3D box geometries with smooth rounded edges that can serve as building blocks for complex mechanical designs, architectural elements, or stylized geometric compositions.

**📋 Files Included**

- ChamferBox Pro.clbnode - The main COOLLAB 3D shape node
- ChamferBox Pro.clbnode.presets.json - Preset configurations with 13 different variations

**🚀 How to Use**

*Import the Node:*

- Download both files from this directory (necessary files to make it run)
- Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
- as well as the associated preset .json file.

You can place the file in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*Connect to Scene:*

- Use as a 3D geometry source in your scene
- Combine with materials, lighting, and other 3D nodes
- Works excellently with raymarching renderers and mesh generation

*Adjust Parameters:* see the parameter list below

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable, optimized
- Rendering: Compatible with raymarching and mesh generation
- Based on: 3D primitives from 3ds Max, Strata 3D CX and similar professional software

**📜 License & Attribution**

*Original Inspiration:*

- Based on the 3D-primitives of 3ds Max, Strata 3D CX and similar professional 3D software
- Idea and project coordination by bennoH.

*This COOLLAB Node:*

- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is a professional-grade chamfered box generator with advanced features:
- 📐 **Precise Dimensional Control**: Independent width, height, and depth parameters
- 🔄 **Smooth Chamfer System**: Professional-quality rounded edge generation
- 📊 **Surface Segmentation**: Optional grid-based surface detail system
- ⚙️ **Professional Standard**: Based on industry-standard 3D modeling software
- 🎯 **Centered Geometry**: Automatic center-based positioning for consistent placement

### 🎛️ Parameters

#### 🔧 Core Geometry Controls
- 📏 **Width** (Float, adjustable): Controls the X-axis dimension of the box. Defines the horizontal width of the chamfered box
- 📐 **Height** (Float, adjustable): Controls the Y-axis dimension of the box. Defines the vertical height of the chamfered box
- 📦 **Depth** (Float, adjustable): Controls the Z-axis dimension of the box. Defines the front-to-back depth of the chamfered box

#### 🔄 Chamfer Controls
- ✨ **Chamfer Size** (Float, adjustable): Controls the radius of the rounded edges. Larger values create more pronounced rounded corners, smaller values create sharper edges

#### 📊 Surface Detail Controls
- 🔘 **Segment Mode** (Boolean, default: false): Enables/disables surface segmentation display. When enabled, shows grid-based surface divisions
- 📏 **Segment Size** (Float, adjustable): Controls the size of surface segments when Segment Mode is enabled. Affects the spacing and prominence of the grid pattern

### ⚙️ Technical Implementation
The chamfered box generation works through several sophisticated stages:
1. 📐 **Dimension Processing**: Input dimensions are halved for center-based box calculation
2. 📦 **Base Box Generation**: Standard box shape creation using absolute position values
3. 🔄 **Chamfer Application**: Rounded edge generation using distance field mathematics
4. 📊 **Segmentation Processing**: Optional grid-based surface detail application using fractional coordinates
5. 🎯 **Surface Modulation**: Smooth interpolation for seamless segment integration
6. 📏 **Final Distance Calculation**: Combined geometry and surface detail output

### 🎨 Creative Applications
- 🏗️ **Architectural Elements**: Create building blocks, structural components, or decorative elements
- 🔧 **Product Design**: Generate consumer products, electronic housings, or packaging designs
- 🎮 **Game Assets**: Perfect for sci-fi environments, industrial settings, or geometric structures
- 🏭 **Industrial Design**: Mechanical components, housings, or technical equipment
- 🎨 **Abstract Geometry**: Foundation for geometric art installations or minimalist compositions
- 📐 **Technical Visualization**: Engineering diagrams, CAD-style presentations, or educational models

### 📦 Available Presets
**ChamferBox Pro** comes with 13 carefully crafted presets:

#### 🔲 Cube Variations (1.0 × 1.0 × 1.0)
- **"Cube broken edges MINIMAL"** - Sharp cube with tiny chamfer (0.012)
- **"Cube soft roundet edges NORMAL"** - Subtle rounded edges (0.06)
- **"Cube roundet edges MEDIUM"** - Medium rounded edges (0.18)
- **"Cube wide roundet edges HIGH"** - Heavily rounded edges (0.33)
- **"Cube roundet edges MEDIUM & SEGMENTET"** - Medium chamfer with surface segments enabled

#### 📐 Quader/Cuboid Variations (1.66 × 1.0 × 1.0)
- **"Quader broken edges MINIMAL"** - Sharp rectangular box with minimal chamfer (0.012)
- **"Quader soft roundet edges NORMAL"** - Subtle rounded rectangular box (0.06)
- **"Quader roundet edges MEDIUM"** - Medium rounded rectangular box (0.18)
- **"Quader wide roundet edges HIGH"** - Heavily rounded rectangular box (0.33)
- **"Quader roundet edges MEDIUM & SEGMENTET"** - Medium chamfer with surface segments

#### 🚁 Special Shape Variations
- **"Zepelin out of a Quader"** - Elongated airship-like form (1.86 × 1.0 × 1.0, Chamfer: 0.63)
- **"Segmentelynio out of a Cuboid"** - Wide segmented form (2.0 × 1.0 × 1.0, Chamfer: 0.63, Segments enabled)

**Preset Usage Tips:**
- 🔲 Use **Cube** presets for perfect cubic shapes
- 📐 Use **Quader** presets for rectangular building blocks
- 🚁 Try **Zepelin** for organic, capsule-like forms
- 📊 Use **SEGMENTET** variants for technical/industrial aesthetics

### 💡 Tips for Best Results
- ✅ Start with **Width**, **Height**, **Depth** around 1.0-2.0 for standard proportions
- ✅ Use **Chamfer Size** between 0.05-0.3 for subtle to moderate rounding
- ✅ Set **Chamfer Size** to 0.0 for sharp, cubic boxes
- ✅ Enable **Segment Mode** for technical or industrial aesthetics
- ✅ Use **Segment Size** around 0.1-0.4 when segmentation is enabled
- ✅ Animate **Chamfer Size** for morphing between sharp and rounded forms
- ✅ Combine multiple boxes with different proportions for complex structures

### 🎬 Animation Possibilities
**ChamferBox Pro** offers excellent animation capabilities:

**Recommended Animation Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 4.0) → **Width/Height/Depth**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.0, Max: 0.3, Period: 6.0) → **Chamfer Size**
3. 🔄 **Rotate Node** with **Time Node** for rotating geometric displays
4. 📊 **Time Node** → **Sine Wave** (Min: 0.1, Max: 0.5, Period: 8.0) → **Segment Size**

**Creative Animation Ideas:**
- **Morphing Box**: Animate all dimensions independently for shape changes
- **Chamfer Transition**: Smooth transition from sharp cube to rounded box
- **Segmentation Pulse**: Animate Segment Size for dynamic surface details
- **Growing Structure**: Linear increase of dimensions over time
- **Technical Display**: Toggle Segment Mode with time-based switching

### 🎯 Professional Applications
- **CAD Visualization**: Rapid prototyping of geometric forms
- **Architectural Previsualization**: Building component mockups
- **Product Development**: Early-stage design visualization
- **Educational Tools**: Geometry and engineering education
- **Technical Documentation**: Clear, professional geometric illustrations

### 🔧 Advanced Tips
- **Precision Modeling**: Use small Chamfer Size values (0.01-0.05) for subtle professional edges
- **Industrial Aesthetic**: Enable Segment Mode with small Segment Size (0.1-0.2) for technical looks
- **Organic Integration**: Combine with other 3D shapes using boolean operations
- **Material Optimization**: Chamfered edges catch light beautifully with metallic materials
- **Scale Considerations**: Adjust Chamfer Size proportionally when scaling the entire box

**🔗 Links**

- 3ds Max Official Website
- Strata 3D CX Reference
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **ChamferBox Pro** Node erzeugt anspruchsvolle 3D-Box-Formen mit abgerundeten Kanten (Chamfers) und optionaler Oberflächensegmentierung. Dieser prozedurale Geometrie-Generator produziert professionelle Qualitäts-Chamfer-Boxen, die an jene aus traditioneller 3D-Modeling-Software wie 3ds Max und Strata 3D CX erinnern. Der Node kombiniert präzise geometrische Kontrolle mit erweiterten Oberflächendetail-Fähigkeiten und macht ihn perfekt für architektonische Elemente, Produktdesign und technische Visualisierungen.
& generiert saubere, professionelle 3D-Box-Geometrien mit glatten abgerundeten Kanten, die als Bausteine für komplexe mechanische Designs, architektonische Elemente oder stilisierte geometrische Kompositionen dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- ChamferBox Pro.clbnode - Das Haupt-COOLLAB 3D-Form Node
- ChamferBox Pro.clbnode.presets.json - Preset-Konfigurationen mit 13 verschiedenen Variationen

**🚀 Verwendung sprich Installationsanleitung**

*Node Importieren:*

- Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
- Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
- wie auch die zugehörige Preset-Datei die .json Datei.

Sie können die Datei in die Kategorie "3D Shapes" respektive den entsprechenden Ordner hinein legen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "3D Shapes" einzuordnen: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*In Szene Verbinden:*

- Als 3D-Geometrie-Quelle in Ihrer Szene verwenden
- Mit Materialien, Beleuchtung und anderen 3D-Nodes kombinieren
- Funktioniert hervorragend mit Raymarching-Renderern und Mesh-Generierung

*Parameter Anpassen:* siehe Parameterliste weiter unten

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig, optimiert
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung
- Basiert auf: 3D-Primitiven von 3ds Max, Strata 3D CX und ähnlicher professioneller Software

**📜 Lizenz & Attribution**

*Original-Inspiration:*

- Basiert auf den 3D-Primitiven von 3ds Max, Strata 3D CX und ähnlicher professioneller 3D-Software
- Idee und Projektkoordination von bennoH.

*Dieses COOLLAB Node:*

- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist ein professioneller Chamfer-Box-Generator mit erweiterten Features:
- 📐 **Präzise Dimensions-Kontrolle**: Unabhängige Breite-, Höhe- und Tiefe-Parameter
- 🔄 **Glattes Chamfer-System**: Professionelle abgerundete Kanten-Generierung
- 📊 **Oberflächensegmentierung**: Optionales raster-basiertes Oberflächendetail-System
- ⚙️ **Professioneller Standard**: Basiert auf branchenüblicher 3D-Modeling-Software
- 🎯 **Zentrierte Geometrie**: Automatische zentrum-basierte Positionierung für konsistente Platzierung

### 🎛️ Parameter

#### 🔧 Kern-Geometrie-Kontrollen
- 📏 **Width** (Float, anpassbar): Kontrolliert die X-Achsen-Dimension der Box. Definiert die horizontale Breite der Chamfer-Box
- 📐 **Height** (Float, anpassbar): Kontrolliert die Y-Achsen-Dimension der Box. Definiert die vertikale Höhe der Chamfer-Box
- 📦 **Depth** (Float, anpassbar): Kontrolliert die Z-Achsen-Dimension der Box. Definiert die Vorne-nach-Hinten-Tiefe der Chamfer-Box

#### 🔄 Chamfer-Kontrollen
- ✨ **Chamfer Size** (Float, anpassbar): Kontrolliert den Radius der abgerundeten Kanten. Größere Werte erzeugen ausgeprägtere abgerundete Ecken, kleinere Werte erzeugen schärfere Kanten

#### 📊 Oberflächendetail-Kontrollen
- 🔘 **Segment Mode** (Boolean, Standard: false): Aktiviert/deaktiviert die Oberflächensegmentierungs-Anzeige. Wenn aktiviert, zeigt raster-basierte Oberflächenaufteilungen
- 📏 **Segment Size** (Float, anpassbar): Kontrolliert die Größe der Oberflächensegmente wenn Segment Mode aktiviert ist. Beeinflusst den Abstand und die Sichtbarkeit des Rastermusters

### ⚙️ Technische Implementation
Die Chamfer-Box-Generierung funktioniert durch mehrere ausgeklügelte Stufen:
1. 📐 **Dimensions-Verarbeitung**: Eingabe-Dimensionen werden halbiert für zentrum-basierte Box-Berechnung
2. 📦 **Basis-Box-Generierung**: Standard Box-Form-Erstellung unter Verwendung absoluter Positionswerte
3. 🔄 **Chamfer-Anwendung**: Abgerundete Kanten-Generierung mit Distance Field Mathematik
4. 📊 **Segmentierungs-Verarbeitung**: Optionale raster-basierte Oberflächendetail-Anwendung mit fraktionalen Koordinaten
5. 🎯 **Oberflächenmodulation**: Glatte Interpolation für nahtlose Segment-Integration
6. 📏 **Finale Distance-Berechnung**: Kombinierte Geometrie- und Oberflächendetail-Ausgabe

### 🎨 Kreative Anwendungen
- 🏗️ **Architektonische Elemente**: Bausteine, Strukturkomponenten oder dekorative Elemente erstellen
- 🔧 **Produktdesign**: Konsumprodukte, Elektronikgehäuse oder Verpackungsdesigns generieren
- 🎮 **Spiel-Assets**: Perfekt für Sci-Fi-Umgebungen, industrielle Settings oder geometrische Strukturen
- 🏭 **Industriedesign**: Mechanische Komponenten, Gehäuse oder technische Ausrüstung
- 🎨 **Abstrakte Geometrie**: Grundlage für geometrische Kunstinstallationen oder minimalistische Kompositionen
- 📐 **Technische Visualisierung**: Ingenieurdiagramme, CAD-ähnliche Präsentationen oder Bildungsmodelle

### 📦 Verfügbare Presets
**ChamferBox Pro** kommt mit 13 sorgfältig gestalteten Presets:

#### 🔲 Würfel-Variationen (1.0 × 1.0 × 1.0)
- **"Cube broken edges MINIMAL"** - Scharfer Würfel mit winzigem Chamfer (0.012)
- **"Cube soft roundet edges NORMAL"** - Subtil abgerundete Kanten (0.06)
- **"Cube roundet edges MEDIUM"** - Mittlere abgerundete Kanten (0.18)
- **"Cube wide roundet edges HIGH"** - Stark abgerundete Kanten (0.33)
- **"Cube roundet edges MEDIUM & SEGMENTET"** - Mittlerer Chamfer mit aktivierten Oberflächensegmenten

#### 📐 Quader-Variationen (1.66 × 1.0 × 1.0)
- **"Quader broken edges MINIMAL"** - Scharfe rechteckige Box mit minimalem Chamfer (0.012)
- **"Quader soft roundet edges NORMAL"** - Subtil abgerundete rechteckige Box (0.06)
- **"Quader roundet edges MEDIUM"** - Mittlere abgerundete rechteckige Box (0.18)
- **"Quader wide roundet edges HIGH"** - Stark abgerundete rechteckige Box (0.33)
- **"Quader roundet edges MEDIUM & SEGMENTET"** - Mittlerer Chamfer mit Oberflächensegmenten

#### 🚁 Spezielle Form-Variationen
- **"Zepelin out of a Quader"** - Längliche luftschiff-ähnliche Form (1.86 × 1.0 × 1.0, Chamfer: 0.63)
- **"Segmentelynio out of a Cuboid"** - Breite segmentierte Form (2.0 × 1.0 × 1.0, Chamfer: 0.63, Segmente aktiviert)

**Preset-Verwendungstipps:**
- 🔲 **Cube**-Presets für perfekte kubische Formen verwenden
- 📐 **Quader**-Presets für rechteckige Bausteine verwenden
- 🚁 **Zepelin** für organische, kapsel-ähnliche Formen ausprobieren
- 📊 **SEGMENTET**-Varianten für technische/industrielle Ästhetik verwenden

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Width**, **Height**, **Depth** um 1.0-2.0 für Standard-Proportionen beginnen
- ✅ **Chamfer Size** zwischen 0.05-0.3 für subtile bis moderate Rundung verwenden
- ✅ **Chamfer Size** auf 0.0 für scharfe, kubische Boxen setzen
- ✅ **Segment Mode** für technische oder industrielle Ästhetik aktivieren
- ✅ **Segment Size** um 0.1-0.4 verwenden wenn Segmentierung aktiviert ist
- ✅ **Chamfer Size** für Morphing zwischen scharfen und abgerundeten Formen animieren
- ✅ Mehrere Boxen mit verschiedenen Proportionen für komplexe Strukturen kombinieren

### 🎬 Animations-Möglichkeiten
**ChamferBox Pro** bietet ausgezeichnete Animations-Fähigkeiten:

**Empfohlene Animations-Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 4.0) → **Width/Height/Depth**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.0, Max: 0.3, Period: 6.0) → **Chamfer Size**
3. 🔄 **Rotate Node** mit **Time Node** für rotierende geometrische Displays
4. 📊 **Time Node** → **Sine Wave** (Min: 0.1, Max: 0.5, Period: 8.0) → **Segment Size**

**Kreative Animations-Ideen:**
- **Morphende Box**: Alle Dimensionen unabhängig für Formänderungen animieren
- **Chamfer-Übergang**: Glatter Übergang von scharfem Würfel zu abgerundeter Box
- **Segmentierungs-Puls**: Segment Size für dynamische Oberflächendetails animieren
- **Wachsende Struktur**: Lineare Vergrößerung der Dimensionen über Zeit
- **Technische Anzeige**: Segment Mode mit zeit-basiertem Umschalten

### 🎯 Professionelle Anwendungen
- **CAD-Visualisierung**: Schnelles Prototyping geometrischer Formen
- **Architektonische Vorvisualisierung**: Gebäudekomponenten-Mockups
- **Produktentwicklung**: Frühe Design-Visualisierung
- **Bildungstools**: Geometrie- und Ingenieurswesen-Bildung
- **Technische Dokumentation**: Klare, professionelle geometrische Illustrationen

### 🔧 Erweiterte Tipps
- **Präzisions-Modeling**: Kleine Chamfer Size-Werte (0.01-0.05) für subtile professionelle Kanten verwenden
- **Industrielle Ästhetik**: Segment Mode mit kleiner Segment Size (0.1-0.2) für technische Looks aktivieren
- **Organische Integration**: Mit anderen 3D-Formen mittels boolescher Operationen kombinieren
- **Material-Optimierung**: Chamfer-Kanten fangen Licht wunderschön mit metallischen Materialien
- **Skalierungs-Überlegungen**: Chamfer Size proportional anpassen beim Skalieren der gesamten Box

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: 3ds Max, Strata 3D CX 3D primitives 🏗️  
**Basiert auf**: 3ds Max, Strata 3D CX 3D-Primitiven 🏗️

**Category**: 3D Shapes > Geometric 📦  
**Kategorie**: 3D-Formen > Geometrisch 📦

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Special Features**: Chamfering, Surface Segmentation 🔄  
**Besondere Features**: Chamfering, Oberflächensegmentierung 🔄

**Performance**: Optimized for real-time rendering ⚡  
**Performance**: Optimiert für Echtzeit-Rendering ⚡

**🔗 Links**

- 3ds Max Official Website
- Strata 3D CX Reference
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025
