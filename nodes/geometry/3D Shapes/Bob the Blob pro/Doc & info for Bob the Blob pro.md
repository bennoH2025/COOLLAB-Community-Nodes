[English](#-english) | [Deutsch](#-deutsch)
---

# 🟡 Bob the Blob pro Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Bob the Blob pro** node creates sophisticated organic 3D blob shapes with advanced surface detail control. This procedural geometry generator produces smooth, bulbous forms reminiscent of sea creatures, organic cells, or abstract sculptural elements. Inspired by the cool Blob from VisualJockai-SP1, this professional version offers extensive customization through multiple direction vectors and surface modulation parameters.
& It generates stunning organic 3D shapes that can serve as building blocks for complex scenes, character modeling bases, or abstract art installations.


**📋 Files Included**

- Bob the Blob pro.clbnode - The main COOLLAB 3D shape node
- Bob the Blob pro.clbnode.presets.json - Preset configurations including "SeaMine" effects

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
- Works excellently with raymarching renderers

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable
- Rendering: Compatible with raymarching and mesh generation

**📜 License & Attribution**

*Original Inspiration:*

- Inspired by the cool Blob from VisualJockai-SP1
- Idea and project coordination by bennoH.

*This COOLLAB Node:*

- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license



### ✨ What Makes This Special
This is not a simple primitive shape. The "pro" version adds several advanced features:
- 🎯 **Multi-Directional Control**: Three independent direction vectors for complex asymmetric shapes
- 🌊 **Surface Detail Modulation**: Advanced bumpiness control with cosine-based surface variations  
- 📐 **Golden Ratio Integration**: Built-in PHI parameter for naturally pleasing proportions
- 🔄 **Coordinate Sorting**: Automatic orientation optimization for consistent shape generation



### 🎛️ Parameters

#### 🔧 Core Shape Controls
- 📏 **Size** (Float, adjustable): Controls the overall scale of the blob. Larger values create bigger blobs, smaller values create more compact shapes
- 🌊 **Bumpiness** (0.0 - higher values, suggested range 0.0-3.0): Controls the surface detail intensity. Higher values create more pronounced surface variations and organic texture
- ⚱️ **PHI** (Float, typically around 0.5-1.6): Golden ratio constant that influences the mathematical proportions of the blob shape

#### 🎯 Direction Vector Controls
- ➡️ **Direction 1** (vec3, default: variable): Primary directional influence vector that shapes the main blob orientation
- ⬇️ **Direction 2** (vec3, default: [0,0,0]): Secondary directional vector for additional asymmetric deformation
- ↗️ **Direction 3** (vec3, default: [0,0,0]): Tertiary directional vector for fine-tuned shape control

### ⚙️ Technical Implementation
The blob generation works through several sophisticated stages:
1. 🔄 **Position Scaling**: Input coordinates are scaled by the inverse of the Size parameter
2. 🪞 **Symmetry Application**: Absolute value operations create symmetric base structure
3. 📊 **Coordinate Sorting**: Automatic sorting ensures proper orientation regardless of input
4. 🎯 **Multi-Vector Calculation**: Complex dot product calculations using all three direction vectors
5. 🌊 **Surface Modulation**: Cosine-based surface detail application using Bumpiness parameter
6. 📏 **Distance Field Generation**: Final signed distance calculation with size scaling

### 🎨 Creative Applications
- 🧬 **Organic Modeling**: Create cell-like structures, bacteria, or microscopic organisms
- 🌊 **Sea Creature Design**: Generate jellyfish, sea anemones, or abstract marine life
- 🏗️ **Architectural Elements**: Use for organic building components or sculptural elements
- 🎮 **Game Assets**: Perfect for alien creatures, fantasy elements, or environmental objects
- 🎨 **Abstract Art**: Combine multiple blobs for complex organic compositions

### 💡 Tips for Best Results
- ✅ Start with **Size** around 0.5-1.0 for medium-scale blobs
- ✅ Use **Bumpiness** values between 1.0-2.5 for natural organic texture
- ✅ Set **PHI** to 1.618 (golden ratio) for mathematically pleasing proportions
- ✅ Experiment with **Direction 1** values around [-1 to 1, -1 to 1, -1 to 1] for primary shaping
- ✅ Leave **Direction 2** and **Direction 3** at [0,0,0] initially, then add subtle variations
- ✅ Animate direction vectors for morphing blob effects

### 🎬 Animation Setup Guide
**Bob the Blob pro** is designed for animation! The preset names contain detailed node chain instructions:

**Understanding Preset Names:**
The text in parentheses describes the complete animation setup. For example:
`"SeaMine Anima (all Time's 0.5 SinWav0.86 2.42 4.0 Bumpin & 0.01 0.53 10.0 PHI / 3D-Wave for BlobPro / Rotate)"`

**Decoding the Animation Chain:**
- **Time's 0.5** = Time Node with speed 0.5
- **SinWav0.86 2.42 4.0 Bumpin** = Sine Wave Node (Min: 0.86, Max: 2.42, Period: 4.0) → connected to Bumpiness parameter
- **0.01 0.53 10.0 PHI** = Another Sine Wave (Min: 0.01, Max: 0.53, Period: 10.0) → connected to PHI parameter  
- **3D-Wave for BlobPro** = 3D-Wave Node applied to the blob (often with "SoftSwoBle" preset)
- **Rotate** = Rotation Node for final transformation

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.5) → **Sine Wave** (Min: 0.86, Max: 2.42, Period: 4.0) → **Bumpiness**
2. 🕐 **Time Node** (Speed: 0.5) → **Sine Wave** (Min: 0.01, Max: 0.53, Period: 10.0) → **PHI**
3. 🌊 **3D-Wave Node** with "SoftSwoBle" preset + **Time Node** (Speed: 1.0) → **Phase**
4. 🔄 **Rotate Node** with **Time Nodes** (Speed: 0.1) → **X and Z axes**
   - Optional: Add **Sine Wave** to Z-axis for non-repetitive motion



**🔗 Links**

- VisualJockai-SP1 Original Inspiration
- COOLLAB Official Website
- Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - January 2025

---



## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Bob the Blob pro** Node erzeugt anspruchsvolle organische 3D-Blob-Formen mit erweiteter Oberflächendetail-Kontrolle. Dieser prozedurale Geometrie-Generator produziert glatte, bauchige Formen, die an Meerestiere, organische Zellen oder abstrakte skulpturale Elemente erinnern. Inspiriert vom coolen Blob aus VisualJockai-SP1 bietet diese professionelle Version extensive Anpassungsmöglichkeiten durch mehrere Richtungsvektoren und Oberflächenmodulations-Parameter.
& generiert beeindruckende organische 3D-Formen, die als Bausteine für komplexe Szenen, Charakter-Modeling-Basen oder abstrakte Kunstinstallationen dienen können.


**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- Bob the Blob pro.clbnode - Das Haupt-COOLLAB 3D-Form Node
- Bob the Blob pro.clbnode.presets.json - Preset-Konfigurationen inklusive "SeaMine"-Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung

**📜 Lizenz & Attribution**

*Original-Inspiration:*

- Inspiriert vom coolen Blob aus VisualJockai-SP1
- Idee und Projektkoordination von bennoH.

*Dieses COOLLAB Node:*

- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz




### ✨ Was macht diesen Node besonders
Dies ist keine einfache primitive Form. Die "pro"-Version fügt mehrere erweiterte Features hinzu:
- 🎯 **Multi-Direktionale Kontrolle**: Drei unabhängige Richtungsvektoren für komplexe asymmetrische Formen
- 🌊 **Oberflächendetail-Modulation**: Erweiterte Bumpiness-Kontrolle mit Kosinus-basierten Oberflächenvariationen  
- 📐 **Goldener Schnitt Integration**: Eingebauter PHI-Parameter für natürlich ansprechende Proportionen
- 🔄 **Koordinaten-Sortierung**: Automatische Orientierungs-Optimierung für konsistente Formgenerierung



### 🎛️ Parameter

#### 🔧 Kern-Form-Kontrollen
- 📏 **Size** (Float, anpassbar): Kontrolliert die Gesamtgröße des Blobs. Größere Werte erzeugen größere Blobs, kleinere Werte erzeugen kompaktere Formen
- 🌊 **Bumpiness** (0.0 - höhere Werte, empfohlener Bereich 0.0-3.0): Kontrolliert die Oberflächendetail-Intensität. Höhere Werte erzeugen ausgeprägtere Oberflächenvariationen und organische Textur
- ⚱️ **PHI** (Float, typisch um 0.5-1.6): Goldener Schnitt Konstante, die die mathematischen Proportionen der Blob-Form beeinflusst

#### 🎯 Richtungsvektor-Kontrollen
- ➡️ **Direction 1** (vec3, Standard: variabel): Primärer Richtungseinfluss-Vektor, der die Haupt-Blob-Orientierung formt
- ⬇️ **Direction 2** (vec3, Standard: [0,0,0]): Sekundärer Richtungsvektor für zusätzliche asymmetrische Verformung
- ↗️ **Direction 3** (vec3, Standard: [0,0,0]): Tertiärer Richtungsvektor für feinabgestimmte Formkontrolle

### ⚙️ Technische Implementation
Die Blob-Generierung funktioniert durch mehrere ausgeklügelte Stufen:
1. 🔄 **Positions-Skalierung**: Eingabekoordinaten werden durch den Kehrwert des Size-Parameters skaliert
2. 🪞 **Symmetrie-Anwendung**: Absolutwert-Operationen erzeugen symmetrische Grundstruktur
3. 📊 **Koordinaten-Sortierung**: Automatische Sortierung gewährleistet korrekte Orientierung unabhängig von der Eingabe
4. 🎯 **Multi-Vektor-Berechnung**: Komplexe Skalarprodukt-Berechnungen unter Verwendung aller drei Richtungsvektoren
5. 🌊 **Oberflächenmodulation**: Kosinus-basierte Oberflächendetail-Anwendung mit Bumpiness-Parameter
6. 📏 **Distance Field Generierung**: Finale Signed Distance Berechnung mit Größenskalierung

### 🎨 Kreative Anwendungen
- 🧬 **Organisches Modeling**: Zell-ähnliche Strukturen, Bakterien oder mikroskopische Organismen erstellen
- 🌊 **Meerestier-Design**: Quallen, Seeanemonen oder abstrakte Meereslebewesen generieren
- 🏗️ **Architektonische Elemente**: Für organische Gebäudekomponenten oder skulpturale Elemente verwenden
- 🎮 **Spiel-Assets**: Perfekt für Alien-Kreaturen, Fantasy-Elemente oder Umgebungsobjekte
- 🎨 **Abstrakte Kunst**: Mehrere Blobs für komplexe organische Kompositionen kombinieren

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Size** um 0.5-1.0 für mittelgroße Blobs beginnen
- ✅ **Bumpiness**-Werte zwischen 1.0-2.5 für natürliche organische Textur verwenden
- ✅ **PHI** auf 1.618 (Goldener Schnitt) für mathematisch ansprechende Proportionen setzen
- ✅ Mit **Direction 1**-Werten um [-1 bis 1, -1 bis 1, -1 bis 1] für primäre Formgebung experimentieren
- ✅ **Direction 2** und **Direction 3** zunächst bei [0,0,0] belassen, dann subtile Variationen hinzufügen
- ✅ Richtungsvektoren für morphende Blob-Effekte animieren

### 🎬 Animations-Setup Anleitung
**Bob the Blob pro** ist für Animation konzipiert! Die Preset-Namen enthalten detaillierte Node-Chain-Anweisungen:

**Preset-Namen verstehen:**
Der Text in Klammern beschreibt das komplette Animations-Setup. Zum Beispiel:
`"SeaMine Anima (all Time's 0.5 SinWav0.86 2.42 4.0 Bumpin & 0.01 0.53 10.0 PHI / 3D-Wave for BlobPro / Rotate)"`

**Animations-Chain entschlüsseln:**
- **Time's 0.5** = Time Node mit Geschwindigkeit 0.5
- **SinWav0.86 2.42 4.0 Bumpin** = Sine Wave Node (Min: 0.86, Max: 2.42, Period: 4.0) → verbunden mit Bumpiness-Parameter
- **0.01 0.53 10.0 PHI** = Weitere Sine Wave (Min: 0.01, Max: 0.53, Period: 10.0) → verbunden mit PHI-Parameter  
- **3D-Wave for BlobPro** = 3D-Wave Node auf den Blob angewendet (oft mit "SoftSwoBle" Preset)
- **Rotate** = Rotation Node für finale Transformation

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.5) → **Sine Wave** (Min: 0.86, Max: 2.42, Period: 4.0) → **Bumpiness**
2. 🕐 **Time Node** (Geschwindigkeit: 0.5) → **Sine Wave** (Min: 0.01, Max: 0.53, Period: 10.0) → **PHI**
3. 🌊 **3D-Wave Node** mit "SoftSwoBle" Preset + **Time Node** (Geschwindigkeit: 1.0) → **Phase**
4. 🔄 **Rotate Node** mit **Time Nodes** (Geschwindigkeit: 0.1) → **X und Z Achsen**
   - Optional: **Sine Wave** zur Z-Achse für nicht-repetitive Bewegung hinzufügen

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Inspired by**: VisualJockai-SP1 Blob 🎨  
**Inspiriert von**: VisualJockai-SP1 Blob 🎨

**Category**: 3D Shapes > Organic 🟡  
**Kategorie**: 3D-Formen > Organisch 🟡

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "SeaMine" - Static sea mine/underwater mine aesthetic with specific direction vectors
- "SeaMine Anima (all Time's 0.5 SinWav0.86 2.42 4.0 Bumpin & 0.01 0.53 10.0 PHI / 3D-Wave for BlobPro / Rotate)" - Complete animated setup with detailed node chain instructions

**Verfügbare Presets**: 
- "SeaMine" - Statische Seeminen/Unterwasserminen-Ästhetik mit spezifischen Richtungsvektoren
- "SeaMine Anima (all Time's 0.5 SinWav0.86 2.42 4.0 Bumpin & 0.01 0.53 10.0 PHI / 3D-Wave for BlobPro / Rotate)" - Komplettes animiertes Setup mit detaillierten Node-Chain-Anweisungen


**🔗 Links**

- VisualJockai-SP1 Original Inspiration
- COOLLAB Official Website
- Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - January 2025
