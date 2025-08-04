[English](#-english) | [Deutsch](#-deutsch)
---

# 🌀 Gyroid Torus Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Gyroid Torus** node creates sophisticated 3D structures that combine the mathematical elegance of gyroid minimal surfaces with torus topology. A gyroid is an infinitely connected triply periodic minimal surface discovered by Alan Schoen in 1970, known for its complex organic patterns and high surface area. This node maps gyroid structures onto torus geometry, creating intricate lattice-like forms that are perfect for architectural elements, scientific visualization, and abstract art installations.
& It generates mathematically precise structures that exhibit both the flowing continuity of minimal surfaces and the controlled geometry of torus forms, ideal for biomimetic designs and advanced geometric compositions.

**📋 Files Included**

- Gyroid Torus.clbnode - The main COOLLAB 3D shape node
- Gyroid Torus.clbnode.presets.json - Preset configurations with 7 distinct gyroid variations

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
- Works excellently with raymarching renderers and complex material systems

*Adjust Parameters:* see the parameter list below

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field with gyroid topology
- Performance: Complex calculations, suitable for high-quality rendering
- Rendering: Optimized for raymarching, creates intricate surface details
- Based on: Mathematical research and web-based gyroid information

**📜 License & Attribution**

*Original Inspiration:*

- Inspired by various web searches and free information about gyroid structures
- Mathematical foundation based on Alan Schoen's 1970 gyroid discovery
- Idea and project coordination by bennoH.

*This COOLLAB Node:*

- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This node combines advanced mathematical concepts with artistic control:
- 🌀 **Gyroid Mathematics**: Based on triply periodic minimal surfaces with zero mean curvature
- 🍩 **Torus Topology**: Maps complex gyroid patterns onto familiar torus geometry
- 🔬 **Scientific Foundation**: Grounded in crystallography and materials science research
- 🎨 **Artistic Control**: Four intuitive parameters for creative exploration
- 🏗️ **Structural Integrity**: Creates naturally strong, lightweight lattice structures

### 🎛️ Parameters

#### 🔧 Torus Geometry Controls
- 🍩 **Major Radius** (Float, adjustable): Controls the outer radius of the torus. Defines the main ring size of the gyroid torus structure
- 📏 **Minor Radius** (Float, adjustable): Controls the inner thickness of the torus. Defines the tube thickness of the torus before gyroid pattern application

#### 🌀 Gyroid Pattern Controls  
- 📐 **Gyroid Scale** (Float, adjustable): Controls the density and size of the gyroid pattern. Smaller values create finer, more detailed patterns; larger values create broader, more open structures
- 🧱 **Gyroid Thickness** (Float, adjustable): Controls the thickness of the gyroid walls. Affects the solidity vs. openness of the lattice structure

### ⚙️ Technical Implementation
The gyroid torus generation combines several mathematical operations:
1. 🍩 **Torus Transformation**: Position mapping to torus coordinate system using atan2 functions
2. 📐 **Coordinate Scaling**: Gyroid Scale parameter applied to pattern density
3. 🌀 **Gyroid Calculation**: Infinitely connected triply periodic minimal surface mathematics using dot product of sine and cosine functions
4. 🧱 **Thickness Control**: Wall thickness adjustment through Gyroid Thickness parameter
5. 📏 **Height Limitation**: Z-axis constraint to maintain torus topology
6. 🎯 **Final Assembly**: Combined distance field output with mathematical scaling

### 📦 Available Presets
**Gyroid Torus** comes with 7 distinctive preset variations:

#### 🌀 Standard Gyroid Patterns
- **"OPEN Standart-gyroid"** - Classic open gyroid structure
  - Major: 15.0, Minor: 4.0, Scale: 0.3, Thickness: 0.1
  - Perfect introduction to gyroid topology with clear lattice visibility

- **"Tripy & mostly-recommended"** ⭐ - Balanced complexity and visual appeal
  - Major: 15.0, Minor: 4.0, Scale: 0.4, Thickness: 0.31
  - Ideal starting point combining beauty and structural clarity

#### 🔄 Density Variations
- **"Half-open"** - Medium density with partial closure
  - Major: 15.0, Minor: 4.0, Scale: 0.54, Thickness: 0.49
  - Balanced between open lattice and solid form

- **"Convoluted"** - Maximum complexity and density
  - Major: 15.0, Minor: 4.0, Scale: 1.0, Thickness: 1.0
  - Highly intricate patterns for advanced applications

#### 🎨 Artistic Variations  
- **"Aqua-Plasmoied"** - Fluid, organic appearance
  - Major: 15.0, Minor: 4.0, Scale: 0.2, Thickness: -0.05
  - Negative thickness creates inverted, liquid-like structures

- **"MarbeyaBall"** - Marble-like solid form
  - Major: 15.0, Minor: 4.0, Scale: -0.07, Thickness: -0.05
  - Negative parameters create unique solid interpretations

#### 🔮 Special Effects
- **"EschydaGring - it's not a ring and not a Escher thing"** - Unique geometric form
  - Major: 15.0, Minor: 8.79, Scale: 0.2, Thickness: 0.01
  - Modified minor radius creates distinctive proportions with ultra-thin walls

### 🎨 Creative Applications
- 🏗️ **Architectural Elements**: Biomimetic building components, ventilation systems, structural lattices
- 🔬 **Scientific Visualization**: Materials science demonstrations, crystalline structure models
- 🎮 **Game Assets**: Sci-fi environments, alien architectures, futuristic structures  
- 🎨 **Abstract Art**: Complex geometric sculptures, mathematical art installations
- 🏭 **Industrial Design**: Lightweight structural components, filtering systems, heat exchangers
- 📚 **Educational Tools**: Demonstrating minimal surface mathematics and topology

### 💡 Tips for Best Results
- ✅ Start with **"Tripy & mostly-recommended"** preset for balanced results
- ✅ Use **Major Radius** 10-20 for medium-scale structures
- ✅ Set **Minor Radius** 3-6 for standard torus proportions  
- ✅ **Gyroid Scale** 0.2-0.5 creates optimal pattern density
- ✅ **Gyroid Thickness** 0.1-0.3 provides good structural definition
- ✅ Negative **Gyroid Thickness** values create inverted, hollow effects
- ✅ Animate **Gyroid Scale** for morphing complexity transitions

### 🎬 Animation Possibilities
**Gyroid Torus** offers fascinating animation potential:

**Recommended Animation Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.2, Max: 0.8, Period: 6.0) → **Gyroid Scale**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.05, Max: 0.4, Period: 4.0) → **Gyroid Thickness**
3. 🔄 **Rotate Node** with **Time Node** for gyroid pattern rotation
4. 🍩 **Time Node** → **Sine Wave** (Min: 8.0, Max: 20.0, Period: 8.0) → **Major Radius**

**Creative Animation Ideas:**
- **Breathing Lattice**: Animate Gyroid Thickness for expanding/contracting walls
- **Pattern Morphing**: Smooth Gyroid Scale transitions from fine to coarse patterns
- **Torus Pulsing**: Major/Minor Radius animation for size changes
- **Complexity Evolution**: Gradual increase of pattern density over time
- **Inversion Effects**: Animate through positive and negative thickness values

### 🔬 Mathematical Background
The gyroid is an infinitely connected periodic minimal surface containing no straight lines and has three-fold rotational symmetry but no embedded straight lines or mirror symmetries. Triply periodic minimal surfaces (TPMS) are three-dimensional cell structures that occur in nature in many forms: for example, in butterfly wings or on the skeletal plate of a sea urchin.

**Key Mathematical Properties:**
- **Zero Mean Curvature**: Creates naturally balanced surface tensions
- **Triply Periodic**: Repeats in all three spatial dimensions  
- **Minimal Surface**: Locally minimizes surface area like soap films
- **High Surface Area**: Maximum surface area for given volume

### 🎯 Professional Applications
- **Biomimetic Design**: Nature-inspired architectural elements
- **Materials Engineering**: Lightweight structural optimization
- **Scientific Research**: Crystallography and surface chemistry
- **Advanced Manufacturing**: 3D printing complex lattice structures
- **Architectural Innovation**: Natural ventilation and structural systems

### 🔧 Advanced Tips
- **Pattern Density**: Lower Gyroid Scale values (0.1-0.3) create finer, more detailed structures
- **Structural Integrity**: Gyroid Thickness 0.1-0.2 provides optimal strength-to-weight ratio
- **Artistic Expression**: Negative thickness values create unique inverted geometries
- **Torus Proportions**: Major:Minor ratios of 3:1 to 5:1 provide pleasing proportions
- **Rendering Optimization**: Complex gyroid patterns benefit from high-quality raymarching settings

**🔗 Links**

- Alan Schoen's Original Gyroid Research
- Triply Periodic Minimal Surfaces Documentation
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Gyroid Torus** Node erzeugt anspruchsvolle 3D-Strukturen, die die mathematische Eleganz von Gyroid-Minimalflächen mit Torus-Topologie kombinieren. Ein Gyroid ist eine unendlich verbundene dreifach periodische Minimalfläche, die 1970 von Alan Schoen entdeckt wurde, bekannt für ihre komplexen organischen Muster und hohe Oberflächendichte. Dieser Node bildet Gyroid-Strukturen auf Torus-Geometrie ab und erzeugt komplizierte gitterartige Formen, die perfekt für architektonische Elemente, wissenschaftliche Visualisierung und abstrakte Kunstinstallationen sind.
& generiert mathematisch präzise Strukturen, die sowohl die fließende Kontinuität von Minimalflächen als auch die kontrollierte Geometrie von Torus-Formen aufweisen, ideal für biomimetische Designs und fortgeschrittene geometrische Kompositionen.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- Gyroid Torus.clbnode - Das Haupt-COOLLAB 3D-Form Node
- Gyroid Torus.clbnode.presets.json - Preset-Konfigurationen mit 7 verschiedenen Gyroid-Variationen

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
- Funktioniert hervorragend mit Raymarching-Renderern und komplexen Material-Systemen

*Parameter Anpassen:* siehe Parameterliste weiter unten

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field mit Gyroid-Topologie
- Performance: Komplexe Berechnungen, geeignet für hochwertige Renderingu
- Rendering: Optimiert für Raymarching, erzeugt komplizierte Oberflächendetails
- Basiert auf: Mathematischer Forschung und web-basierten Gyroid-Informationen

**📜 Lizenz & Attribution**

*Original-Inspiration:*

- Inspiriert von verschiedenen Web-Suchen und freien Informationen über Gyroid-Strukturen
- Mathematische Grundlage basiert auf Alan Schoens Gyroid-Entdeckung von 1970
- Idee und Projektkoordination von bennoH.

*Dieses COOLLAB Node:*

- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dieser Node kombiniert fortgeschrittene mathematische Konzepte mit künstlerischer Kontrolle:
- 🌀 **Gyroid-Mathematik**: Basiert auf dreifach periodischen Minimalflächen mit null mittlerer Krümmung
- 🍩 **Torus-Topologie**: Bildet komplexe Gyroid-Muster auf vertraute Torus-Geometrie ab
- 🔬 **Wissenschaftliche Grundlage**: Fundiert in Kristallographie- und Materialwissenschafts-Forschung
- 🎨 **Künstlerische Kontrolle**: Vier intuitive Parameter für kreative Erkundung
- 🏗️ **Strukturelle Integrität**: Erzeugt natürlich starke, leichtgewichtige Gitterstrukturen

### 🎛️ Parameter

#### 🔧 Torus-Geometrie-Kontrollen
- 🍩 **Major Radius** (Float, anpassbar): Kontrolliert den äußeren Radius des Torus. Definiert die Hauptring-Größe der Gyroid-Torus-Struktur
- 📏 **Minor Radius** (Float, anpassbar): Kontrolliert die innere Dicke des Torus. Definiert die Röhren-Dicke des Torus vor Gyroid-Muster-Anwendung

#### 🌀 Gyroid-Muster-Kontrollen  
- 📐 **Gyroid Scale** (Float, anpassbar): Kontrolliert die Dichte und Größe des Gyroid-Musters. Kleinere Werte erzeugen feinere, detailliertere Muster; größere Werte erzeugen breitere, offenere Strukturen
- 🧱 **Gyroid Thickness** (Float, anpassbar): Kontrolliert die Dicke der Gyroid-Wände. Beeinflusst die Solidität vs. Offenheit der Gitterstruktur

### ⚙️ Technische Implementation
Die Gyroid-Torus-Generierung kombiniert mehrere mathematische Operationen:
1. 🍩 **Torus-Transformation**: Positions-Mapping zum Torus-Koordinatensystem mit atan2-Funktionen
2. 📐 **Koordinaten-Skalierung**: Gyroid Scale-Parameter angewendet auf Muster-Dichte
3. 🌀 **Gyroid-Berechnung**: Unendlich verbundene dreifach periodische Minimalflächen-Mathematik mit Skalarprodukt von Sinus- und Kosinus-Funktionen
4. 🧱 **Dicken-Kontrolle**: Wand-Dicken-Anpassung durch Gyroid Thickness-Parameter
5. 📏 **Höhen-Begrenzung**: Z-Achsen-Beschränkung zur Erhaltung der Torus-Topologie
6. 🎯 **Finale Zusammenstellung**: Kombinierte Distance Field-Ausgabe mit mathematischer Skalierung

### 📦 Verfügbare Presets
**Gyroid Torus** kommt mit 7 charakteristischen Preset-Variationen:

#### 🌀 Standard-Gyroid-Muster
- **"OPEN Standart-gyroid"** - Klassische offene Gyroid-Struktur
  - Major: 15.0, Minor: 4.0, Scale: 0.3, Thickness: 0.1
  - Perfekte Einführung in Gyroid-Topologie mit klarer Gitter-Sichtbarkeit

- **"Tripy & mostly-recommended"** ⭐ - Ausgewogene Komplexität und visuelle Anziehungskraft
  - Major: 15.0, Minor: 4.0, Scale: 0.4, Thickness: 0.31
  - Idealer Ausgangspunkt, der Schönheit und strukturelle Klarheit kombiniert

#### 🔄 Dichte-Variationen
- **"Half-open"** - Mittlere Dichte mit teilweisem Verschluss
  - Major: 15.0, Minor: 4.0, Scale: 0.54, Thickness: 0.49
  - Ausgewogen zwischen offenem Gitter und fester Form

- **"Convoluted"** - Maximale Komplexität und Dichte
  - Major: 15.0, Minor: 4.0, Scale: 1.0, Thickness: 1.0
  - Hochkomplizierte Muster für fortgeschrittene Anwendungen

#### 🎨 Künstlerische Variationen  
- **"Aqua-Plasmoied"** - Flüssige, organische Erscheinung
  - Major: 15.0, Minor: 4.0, Scale: 0.2, Thickness: -0.05
  - Negative Dicke erzeugt invertierte, flüssigkeits-ähnliche Strukturen

- **"MarbeyaBall"** - Marmor-ähnliche feste Form
  - Major: 15.0, Minor: 4.0, Scale: -0.07, Thickness: -0.05
  - Negative Parameter erzeugen einzigartige feste Interpretationen

#### 🔮 Spezialeffekte
- **"EschydaGring - it's not a ring and not a Escher thing"** - Einzigartige geometrische Form
  - Major: 15.0, Minor: 8.79, Scale: 0.2, Thickness: 0.01
  - Modifizierter Minor Radius erzeugt charakteristische Proportionen mit ultra-dünnen Wänden

### 🎨 Kreative Anwendungen
- 🏗️ **Architektonische Elemente**: Biomimetische Gebäudekomponenten, Belüftungssysteme, Strukturgitter
- 🔬 **Wissenschaftliche Visualisierung**: Materialwissenschafts-Demonstrationen, Kristallstruktur-Modelle
- 🎮 **Spiel-Assets**: Sci-Fi-Umgebungen, Alien-Architekturen, futuristische Strukturen  
- 🎨 **Abstrakte Kunst**: Komplexe geometrische Skulpturen, mathematische Kunstinstallationen
- 🏭 **Industriedesign**: Leichtgewichtige Strukturkomponenten, Filtersysteme, Wärmetauscher
- 📚 **Bildungstools**: Demonstration von Minimalflächen-Mathematik und Topologie

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **"Tripy & mostly-recommended"** Preset für ausgewogene Ergebnisse beginnen
- ✅ **Major Radius** 10-20 für mittelgroße Strukturen verwenden
- ✅ **Minor Radius** 3-6 für Standard-Torus-Proportionen setzen  
- ✅ **Gyroid Scale** 0.2-0.5 erzeugt optimale Muster-Dichte
- ✅ **Gyroid Thickness** 0.1-0.3 bietet gute strukturelle Definition
- ✅ Negative **Gyroid Thickness**-Werte erzeugen invertierte, hohle Effekte
- ✅ **Gyroid Scale** für morphende Komplexitäts-Übergänge animieren

### 🎬 Animations-Möglichkeiten
**Gyroid Torus** bietet faszinierende Animations-Möglichkeiten:

**Empfohlene Animations-Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.2, Max: 0.8, Period: 6.0) → **Gyroid Scale**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.05, Max: 0.4, Period: 4.0) → **Gyroid Thickness**
3. 🔄 **Rotate Node** mit **Time Node** für Gyroid-Muster-Rotation
4. 🍩 **Time Node** → **Sine Wave** (Min: 8.0, Max: 20.0, Period: 8.0) → **Major Radius**

**Kreative Animations-Ideen:**
- **Atmendes Gitter**: Gyroid Thickness für expandierende/kontrahierende Wände animieren
- **Muster-Morphing**: Glatte Gyroid Scale-Übergänge von feinen zu groben Mustern
- **Torus-Pulsieren**: Major/Minor Radius-Animation für Größenänderungen
- **Komplexitäts-Evolution**: Graduelle Erhöhung der Muster-Dichte über Zeit
- **Inversions-Effekte**: Zwischen positiven und negativen Dicken-Werten animieren

### 🔬 Mathematischer Hintergrund
Der Gyroid ist eine unendlich verbundene periodische Minimalfläche ohne gerade Linien und hat dreifache Rotationssymmetrie aber keine eingebetteten geraden Linien oder Spiegelsymmetrien. Dreifach periodische Minimalflächen (TPMS) sind dreidimensionale Zellstrukturen, die in der Natur in vielen Formen auftreten: zum Beispiel in Schmetterlingsflügeln oder auf der Skelettplatte eines Seeigels.

**Wichtige mathematische Eigenschaften:**
- **Null mittlere Krümmung**: Erzeugt natürlich ausgewogene Oberflächenspannungen
- **Dreifach periodisch**: Wiederholt sich in allen drei räumlichen Dimensionen  
- **Minimalfläche**: Minimiert lokal die Oberflächenfläche wie Seifenfilme
- **Hohe Oberflächendichte**: Maximale Oberflächenfläche für gegebenes Volumen

### 🎯 Professionelle Anwendungen
- **Biomimetisches Design**: Natur-inspirierte architektonische Elemente
- **Material-Engineering**: Leichtgewichtige Struktur-Optimierung
- **Wissenschaftliche Forschung**: Kristallographie und Oberflächenchemie
- **Fortgeschrittene Fertigung**: 3D-Druck komplexer Gitterstrukturen
- **Architektonische Innovation**: Natürliche Belüftung und Struktursysteme

### 🔧 Erweiterte Tipps
- **Muster-Dichte**: Niedrigere Gyroid Scale-Werte (0.1-0.3) erzeugen feinere, detailliertere Strukturen
- **Strukturelle Integrität**: Gyroid Thickness 0.1-0.2 bietet optimales Stärke-zu-Gewicht-Verhältnis
- **Künstlerischer Ausdruck**: Negative Dicken-Werte erzeugen einzigartige invertierte Geometrien
- **Torus-Proportionen**: Major:Minor-Verhältnisse von 3:1 bis 5:1 bieten ansprechende Proportionen
- **Rendering-Optimierung**: Komplexe Gyroid-Muster profitieren von hochwertigen Raymarching-Einstellungen

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Mathematical Foundation**: Alan Schoen's 1970 Gyroid Discovery 🔬  
**Mathematische Grundlage**: Alan Schoens Gyroid-Entdeckung von 1970 🔬

**Category**: 3D Shapes > Mathematical Surfaces 🌀  
**Kategorie**: 3D-Formen > Mathematische Oberflächen 🌀

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Complex Signed Distance Function ✨  
**Ausgabe**: Komplexe Signed Distance Function ✨

**Special Properties**: Triply Periodic, Zero Mean Curvature 📐  
**Besondere Eigenschaften**: Dreifach periodisch, null mittlere Krümmung 📐

**Applications**: Architecture, Materials Science, Art 🏗️  
**Anwendungen**: Architektur, Materialwissenschaft, Kunst 🏗️

**Presets Available**: 7 distinct variations from open to complex 📦  
**Verfügbare Presets**: 7 charakteristische Variationen von offen bis komplex 📦

**🔗 Links**

- Alan Schoen's Original Gyroid Research
- Triply Periodic Minimal Surfaces Documentation
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025
