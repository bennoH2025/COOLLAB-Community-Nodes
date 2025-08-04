[English](#-english) | [Deutsch](#-deutsch)
---

# 📦 ChamferBox Node Documentation

## 🇬🇧 English

### 📋 Overview
The **ChamferBox** node creates clean 3D box shapes with smooth rounded edges (chamfers). This streamlined procedural geometry generator produces professional-quality chamfered boxes based on industry-standard 3D modeling software like 3ds Max and Strata 3D CX. The node focuses on essential geometric control with four key parameters, making it perfect for architectural elements, product design, and technical visualizations where simplicity and performance are priorities.
& It generates precise, professional 3D box geometries with smooth rounded edges that serve as fundamental building blocks for clean geometric designs, architectural elements, or minimalist compositions.

**📋 Files Included**

- ChamferBox.clbnode - The main COOLLAB 3D shape node
- ChamferBox.clbnode.presets.json - Preset configurations with 4 chamfer intensity levels

**🚀 How to Use**

*Import the Node:*

- Download both files from this directory (necessary files to make it run)
- Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
- as well as the associated preset .json file.

You can place the files in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 

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
- Performance: Real-time capable, lightweight, optimized
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
This is the essential chamfered box generator with streamlined efficiency:
- 📐 **Precise Dimensional Control**: Independent width, height, and depth parameters
- 🔄 **Clean Chamfer System**: Professional-quality rounded edge generation
- ⚡ **Optimized Performance**: Lightweight implementation for maximum speed
- 🎯 **Essential Parameters**: Only 4 parameters for quick, intuitive control
- 🎨 **Professional Standard**: Based on industry-standard 3D modeling software

### 🎛️ Parameters

#### 🔧 Core Geometry Controls
- 📏 **Width** (Float, adjustable): Controls the X-axis dimension of the box. Defines the horizontal width of the chamfered box
- 📐 **Height** (Float, adjustable): Controls the Y-axis dimension of the box. Defines the vertical height of the chamfered box
- 📦 **Depth** (Float, adjustable): Controls the Z-axis dimension of the box. Defines the front-to-back depth of the chamfered box
- ✨ **Chamfer Radius** (Float, adjustable): Controls the radius of the rounded edges. Larger values create more pronounced rounded corners, smaller values create sharper edges

### ⚙️ Technical Implementation
The chamfered box generation works through clean mathematical operations:
1. 📐 **Dimension Processing**: Input dimensions are halved for center-based box calculation
2. 📦 **Distance Calculation**: Standard box distance field computation using absolute position values
3. 🔄 **Chamfer Application**: Rounded edge generation using optimized distance field mathematics
4. 📏 **Final Output**: Clean signed distance field with precise chamfer radius control

### 📦 Available Presets
**ChamferBox** comes with 4 essential chamfer intensity presets:

#### 🔲 Chamfer Intensity Levels (All 1.0 × 1.0 × 1.0 cubes)
- **"Minimal"** - Sharp cube with tiny chamfer (Radius: 0.012)
  - Perfect for subtle edge softening and realistic hard-surface modeling
  
- **"Normal"** - Balanced chamfer for general use (Radius: 0.06)
  - Ideal for architectural elements and product visualization
  
- **"Medium"** - Pronounced rounded edges (Radius: 0.18)
  - Great for consumer products and comfortable geometric forms
  
- **"High"** - Heavily rounded, capsule-like form (Radius: 0.33)
  - Perfect for soft, organic-geometric hybrid shapes

**Preset Usage Guide:**
- 🔹 **Minimal**: Technical drawings, CAD visualization, precision modeling
- 🔹 **Normal**: General architectural elements, building blocks, furniture
- 🔹 **Medium**: Consumer products, electronic housings, decorative elements
- 🔹 **High**: Soft geometric forms, artistic installations, organic transitions

### 🎨 Creative Applications
- 🏗️ **Architectural Elements**: Create building blocks, structural components, or clean geometric forms
- 🔧 **Product Design**: Generate consumer products, electronic housings, or minimalist designs
- 🎮 **Game Assets**: Perfect for clean environments, modern interiors, or geometric structures
- 🏭 **Industrial Design**: Mechanical components, housings, or technical equipment
- 🎨 **Minimalist Art**: Foundation for clean geometric art installations or modern compositions
- 📐 **Technical Visualization**: Engineering diagrams, CAD presentations, or educational models

### 💡 Tips for Best Results
- ✅ Start with **Width**, **Height**, **Depth** around 1.0 for standard cube proportions
- ✅ Use **Chamfer Radius** between 0.01-0.06 for subtle professional edges
- ✅ Set **Chamfer Radius** between 0.1-0.2 for moderate rounding
- ✅ Use **Chamfer Radius** above 0.3 for soft, organic-like forms
- ✅ Set **Chamfer Radius** to 0.0 for perfectly sharp cubic edges
- ✅ Animate **Chamfer Radius** for morphing between sharp and rounded forms
- ✅ Combine multiple boxes with different dimensions for complex structures

### 🎬 Animation Possibilities
**ChamferBox** offers excellent animation capabilities:

**Recommended Animation Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 4.0) → **Width/Height/Depth**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.0, Max: 0.3, Period: 6.0) → **Chamfer Radius**
3. 🔄 **Rotate Node** with **Time Node** for rotating geometric displays
4. 📐 **Scale Node** with **Time Node** for uniform scaling effects

**Creative Animation Ideas:**
- **Morphing Box**: Animate all dimensions independently for shape changes
- **Chamfer Transition**: Smooth transition from sharp cube to rounded box
- **Growing Structure**: Linear increase of dimensions over time
- **Geometric Dance**: Synchronized animation of multiple boxes with different scales
- **Edge Softening**: Gradual increase of chamfer radius over time

### 🆚 Comparison with ChamferBox Pro
This streamlined version focuses on essential functionality:
- ✅ **Faster Performance**: Simplified calculations for maximum speed
- ✅ **Easier Workflow**: Only 4 parameters for quick setup
- ✅ **Clean Results**: Professional chamfering without extra features
- ✅ **Essential Control**: Core dimensional and chamfer parameters
- ❌ **No Surface Segmentation**: No grid-based surface details
- ❌ **No Advanced Features**: Focus on pure chamfered box generation

**Choose ChamferBox when you want:**
- Maximum performance and speed
- Simple, clean chamfered boxes
- Quick prototyping and iteration
- Essential geometric building blocks

**Choose ChamferBox Pro when you need:**
- Surface segmentation effects
- Advanced technical aesthetics
- Complex surface detailing

### 🎯 Professional Applications
- **Rapid Prototyping**: Quick geometric form generation
- **Architectural Previsualization**: Clean building component mockups
- **Product Development**: Essential form studies and iteration
- **Educational Tools**: Basic geometry and 3D modeling education
- **Clean Design**: Minimalist and modern geometric applications

### 🔧 Advanced Tips
- **Precision Modeling**: Use tiny Chamfer Radius values (0.005-0.015) for ultra-subtle edges
- **Organic Transitions**: Large Chamfer Radius values (0.4+) create capsule-like forms
- **Boolean Operations**: Combine with other 3D shapes for complex geometries
- **Material Optimization**: Chamfered edges enhance lighting and material definition
- **Scale Proportions**: Adjust Chamfer Radius proportionally when scaling dimensions

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
Der **ChamferBox** Node erzeugt saubere 3D-Box-Formen mit glatten abgerundeten Kanten (Chamfers). Dieser optimierte prozedurale Geometrie-Generator produziert professionelle Qualitäts-Chamfer-Boxen basierend auf branchenüblicher 3D-Modeling-Software wie 3ds Max und Strata 3D CX. Der Node fokussiert auf essentielle geometrische Kontrolle mit vier Hauptparametern und macht ihn perfekt für architektonische Elemente, Produktdesign und technische Visualisierungen, wo Einfachheit und Performance Priorität haben.
& generiert präzise, professionelle 3D-Box-Geometrien mit glatten abgerundeten Kanten, die als fundamentale Bausteine für saubere geometrische Designs, architektonische Elemente oder minimalistische Kompositionen dienen.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- ChamferBox.clbnode - Das Haupt-COOLLAB 3D-Form Node
- ChamferBox.clbnode.presets.json - Preset-Konfigurationen mit 4 Chamfer-Intensitätsstufen

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
- Funktioniert hervorragend mit Raymarching-Renderern und Mesh-Generierung

*Parameter Anpassen:* siehe Parameterliste weiter unten

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig, leichtgewichtig, optimiert
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
Dies ist der essentielle Chamfer-Box-Generator mit optimierter Effizienz:
- 📐 **Präzise Dimensions-Kontrolle**: Unabhängige Breite-, Höhe- und Tiefe-Parameter
- 🔄 **Sauberes Chamfer-System**: Professionelle abgerundete Kanten-Generierung
- ⚡ **Optimierte Performance**: Leichtgewichtige Implementation für maximale Geschwindigkeit
- 🎯 **Essentielle Parameter**: Nur 4 Parameter für schnelle, intuitive Kontrolle
- 🎨 **Professioneller Standard**: Basiert auf branchenüblicher 3D-Modeling-Software

### 🎛️ Parameter

#### 🔧 Kern-Geometrie-Kontrollen
- 📏 **Width** (Float, anpassbar): Kontrolliert die X-Achsen-Dimension der Box. Definiert die horizontale Breite der Chamfer-Box
- 📐 **Height** (Float, anpassbar): Kontrolliert die Y-Achsen-Dimension der Box. Definiert die vertikale Höhe der Chamfer-Box
- 📦 **Depth** (Float, anpassbar): Kontrolliert die Z-Achsen-Dimension der Box. Definiert die Vorne-nach-Hinten-Tiefe der Chamfer-Box
- ✨ **Chamfer Radius** (Float, anpassbar): Kontrolliert den Radius der abgerundeten Kanten. Größere Werte erzeugen ausgeprägtere abgerundete Ecken, kleinere Werte erzeugen schärfere Kanten

### ⚙️ Technische Implementation
Die Chamfer-Box-Generierung funktioniert durch saubere mathematische Operationen:
1. 📐 **Dimensions-Verarbeitung**: Eingabe-Dimensionen werden halbiert für zentrum-basierte Box-Berechnung
2. 📦 **Distance-Berechnung**: Standard Box Distance Field Berechnung mit absoluten Positionswerten
3. 🔄 **Chamfer-Anwendung**: Abgerundete Kanten-Generierung mit optimierter Distance Field Mathematik
4. 📏 **Finale Ausgabe**: Sauberes Signed Distance Field mit präziser Chamfer Radius Kontrolle

### 📦 Verfügbare Presets
**ChamferBox** kommt mit 4 essentiellen Chamfer-Intensitäts-Presets:

#### 🔲 Chamfer-Intensitätsstufen (Alle 1.0 × 1.0 × 1.0 Würfel)
- **"Minimal"** - Scharfer Würfel mit winzigem Chamfer (Radius: 0.012)
  - Perfekt für subtile Kanten-Weichzeichnung und realistisches Hard-Surface-Modeling
  
- **"Normal"** - Ausgewogener Chamfer für allgemeine Verwendung (Radius: 0.06)
  - Ideal für architektonische Elemente und Produktvisualisierung
  
- **"Medium"** - Ausgeprägte abgerundete Kanten (Radius: 0.18)
  - Großartig für Konsumprodukte und komfortable geometrische Formen
  
- **"High"** - Stark abgerundet, kapsel-ähnliche Form (Radius: 0.33)
  - Perfekt für weiche, organisch-geometrische Hybrid-Formen

**Preset-Verwendungsleitfaden:**
- 🔹 **Minimal**: Technische Zeichnungen, CAD-Visualisierung, Präzisions-Modeling
- 🔹 **Normal**: Allgemeine architektonische Elemente, Bausteine, Möbel
- 🔹 **Medium**: Konsumprodukte, Elektronikgehäuse, dekorative Elemente
- 🔹 **High**: Weiche geometrische Formen, Kunstinstallationen, organische Übergänge

### 🎨 Kreative Anwendungen
- 🏗️ **Architektonische Elemente**: Bausteine, Strukturkomponenten oder saubere geometrische Formen erstellen
- 🔧 **Produktdesign**: Konsumprodukte, Elektronikgehäuse oder minimalistische Designs generieren
- 🎮 **Spiel-Assets**: Perfekt für saubere Umgebungen, moderne Innenräume oder geometrische Strukturen
- 🏭 **Industriedesign**: Mechanische Komponenten, Gehäuse oder technische Ausrüstung
- 🎨 **Minimalistische Kunst**: Grundlage für saubere geometrische Kunstinstallationen oder moderne Kompositionen
- 📐 **Technische Visualisierung**: Ingenieurdiagramme, CAD-Präsentationen oder Bildungsmodelle

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Width**, **Height**, **Depth** um 1.0 für Standard-Würfel-Proportionen beginnen
- ✅ **Chamfer Radius** zwischen 0.01-0.06 für subtile professionelle Kanten verwenden
- ✅ **Chamfer Radius** zwischen 0.1-0.2 für moderate Rundung setzen
- ✅ **Chamfer Radius** über 0.3 für weiche, organik-ähnliche Formen verwenden
- ✅ **Chamfer Radius** auf 0.0 für perfekt scharfe kubische Kanten setzen
- ✅ **Chamfer Radius** für Morphing zwischen scharfen und abgerundeten Formen animieren
- ✅ Mehrere Boxen mit verschiedenen Dimensionen für komplexe Strukturen kombinieren

### 🎬 Animations-Möglichkeiten
**ChamferBox** bietet ausgezeichnete Animations-Fähigkeiten:

**Empfohlene Animations-Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 4.0) → **Width/Height/Depth**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.0, Max: 0.3, Period: 6.0) → **Chamfer Radius**
3. 🔄 **Rotate Node** mit **Time Node** für rotierende geometrische Displays
4. 📐 **Scale Node** mit **Time Node** für einheitliche Skalierungs-Effekte

**Kreative Animations-Ideen:**
- **Morphende Box**: Alle Dimensionen unabhängig für Formänderungen animieren
- **Chamfer-Übergang**: Glatter Übergang von scharfem Würfel zu abgerundeter Box
- **Wachsende Struktur**: Lineare Vergrößerung der Dimensionen über Zeit
- **Geometrischer Tanz**: Synchronisierte Animation mehrerer Boxen mit verschiedenen Skalen
- **Kanten-Weichzeichnung**: Graduelle Vergrößerung des Chamfer Radius über Zeit

### 🆚 Vergleich mit ChamferBox Pro
Diese optimierte Version fokussiert auf essentielle Funktionalität:
- ✅ **Schnellere Performance**: Vereinfachte Berechnungen für maximale Geschwindigkeit
- ✅ **Einfacherer Workflow**: Nur 4 Parameter für schnelles Setup
- ✅ **Saubere Ergebnisse**: Professionelles Chamfering ohne Extra-Features
- ✅ **Essentielle Kontrolle**: Kern-Dimensions- und Chamfer-Parameter
- ❌ **Keine Oberflächensegmentierung**: Keine raster-basierten Oberflächendetails
- ❌ **Keine erweiterten Features**: Fokus auf reine Chamfer-Box-Generierung

**Wählen Sie ChamferBox wenn Sie wollen:**
- Maximale Performance und Geschwindigkeit
- Einfache, saubere Chamfer-Boxen
- Schnelles Prototyping und Iteration
- Essentielle geometrische Bausteine

**Wählen Sie ChamferBox Pro wenn Sie benötigen:**
- Oberflächensegmentierungs-Effekte
- Erweiterte technische Ästhetik
- Komplexe Oberflächendetaillierung

### 🎯 Professionelle Anwendungen
- **Schnelles Prototyping**: Schnelle geometrische Form-Generierung
- **Architektonische Vorvisualisierung**: Saubere Gebäudekomponenten-Mockups
- **Produktentwicklung**: Essentielle Form-Studien und Iteration
- **Bildungstools**: Basis-Geometrie und 3D-Modeling-Bildung
- **Sauberes Design**: Minimalistische und moderne geometrische Anwendungen

### 🔧 Erweiterte Tipps
- **Präzisions-Modeling**: Winzige Chamfer Radius-Werte (0.005-0.015) für ultra-subtile Kanten verwenden
- **Organische Übergänge**: Große Chamfer Radius-Werte (0.4+) erzeugen kapsel-ähnliche Formen
- **Boolesche Operationen**: Mit anderen 3D-Formen für komplexe Geometrien kombinieren
- **Material-Optimierung**: Chamfer-Kanten verbessern Beleuchtung und Material-Definition
- **Skalierungs-Proportionen**: Chamfer Radius proportional anpassen beim Skalieren der Dimensionen

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

**Core Features**: Clean Chamfering, Essential Controls 🔄  
**Kern-Features**: Sauberes Chamfering, Essentielle Kontrollen 🔄

**Performance**: Optimized for maximum speed ⚡  
**Performance**: Optimiert für maximale Geschwindigkeit ⚡

**Presets Available**: 4 Chamfer intensity levels 📦  
**Verfügbare Presets**: 4 Chamfer-Intensitätsstufen 📦

**🔗 Links**

- 3ds Max Official Website
- Strata 3D CX Reference
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025
