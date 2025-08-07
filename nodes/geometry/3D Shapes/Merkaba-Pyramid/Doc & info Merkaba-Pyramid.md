[English](#-english) | [Deutsch](#-deutsch)
---

# ✨ Merkaba-Pyramid Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Merkaba-Pyramid** node creates the sacred geometric form known as Merkaba - two interlocked tetrahedrons (triangular pyramids) forming the Star Tetrahedron or Stellated Octahedron. This procedural geometry generator produces the wireframe structure of this ancient sacred symbol with precise geometric accuracy and extensive customization options. The node enables both traditional symmetric Merkaba configurations and experimental asymmetric variations through independent pyramid rotation controls.

The Merkaba represents the perfect union of opposing forces, the intersection of the physical and spiritual realms, and the divine chariot described in mystical traditions. In modern applications, it serves as a powerful geometric element for architectural visualization, spiritual art installations, and sophisticated 3D design projects.

**📋 Files Included**

- Merkaba-Pyramid (or the holy sacred dual pyramid).clbnode - The main COOLLAB 3D shape node
- MERKABA or the sacred DualPyramid.clbnode.presets.json - Preset configurations including "Default", "Bold standard", "Swinger King", "Glider", "BumpyBlober", "Knotted one", and "The Interlocked" variations
- Examples for the MERKABA node.coollab - Complete example project demonstrating optimal node connections, camera settings, and preset usage

**🚀 How to Use**

*Import the Node:*

- Download all three files from this directory (necessary files to make it run optimally)
- Copy the .clbnode file into your COOLLAB Nodes directory in your most current Coollab version
- as well as the associated preset .json file and the example project .coollab file 

You can place the two files in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 

`C:\Users\_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes\Merkaba-Pyramid`

The example project file (.coollab) should be placed in your Projects directory:

`C:\Users\_YourUserName_\AppData\Roaming\Coollab Launcher\Projects`


*Connect to Scene:*

- Use as a 3D geometry source in your scene
- Combine with materials, lighting, and other 3D nodes
- Works excellently with raymarching renderers and creates stunning light effects through the wireframe structure
- Perfect for spiritual visualization, architectural elements, and geometric art installations

*Adjust Parameters:* see the detailed parameter list below

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field representing wireframe tetrahedrons
- Performance: Real-time capable with optimized SDF calculations for 12 edges
- Rendering: Compatible with raymarching and mesh generation
- Geometry: Mathematically precise Merkaba with proper vertex interlocking

**📜 License & Attribution**

*Sacred Geometry Foundation:*

- Based on ancient Merkaba sacred geometry - the Star Tetrahedron
- Represents the intersection of two tetrahedrons creating 12 edges total
- Inspired by mystical traditions and Kabbalistic symbolism

*This COOLLAB Node:*

- Idea and project coordination by bennoH.
- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not just a simple geometric shape. The Merkaba-Pyramid node creates the authentic sacred geometry with mathematical precision:
- ⭐ **True Sacred Geometry**: Creates the authentic Merkaba where every face is penetrated by an opposing vertex, just like the sacred symbol
- 🔄 **Dual Rotation System**: Independent control over global rotation and second pyramid rotation for infinite variations
- 🏗️ **Wireframe Precision**: Clean 12-edge wireframe structure with adjustable thickness for architectural applications
- 🎯 **Integration Control**: Fine-tune the interpenetration depth of the two pyramids
- 🎛️ **Animation Ready**: Perfect for spiritual visualizations, meditative animations, and geometric art projects

### 🎛️ Parameters

#### 📏 Basic Geometry Controls
- **Size** (Float, 0.1-2.0): Controls the overall scale of the entire Merkaba structure. Higher values create larger, more prominent geometric presence
- **Thickness** (Float, 0.01-0.5): Thickness of the wireframe edges. Controls how substantial the tubular structure appears
- **Integration** (Float, -1.0-2.0): Controls how deeply the two pyramids interpenetrate. 0 = perfect traditional Merkaba, positive values = more overlap, negative values = separation

#### 🌍 Global Rotation Controls
- **Rotation X** (Angle, 0-360°): Rotates the entire Merkaba structure around the X-axis
- **Rotation Y** (Angle, 0-360°): Rotates the entire Merkaba structure around the Y-axis  
- **Rotation Z** (Angle, 0-360°): Rotates the entire Merkaba structure around the Z-axis

#### 🔺 Second Pyramid Independent Rotation
- **Rotation X** (Angle, 0-360°): Independent rotation of the second pyramid around its X-axis only
- **Rotation Y** (Angle, 0-360°): Independent rotation of the second pyramid around its Y-axis only
- **Rotation Z** (Angle, 0-360°): Independent rotation of the second pyramid around its Z-axis only

### ⚙️ Technical Implementation
The Merkaba geometry generation uses precise mathematical construction:
1. 🔺 **First Tetrahedron**: Creates the base upward-pointing tetrahedron with 4 vertices and 6 edges
2. 🔻 **Second Tetrahedron**: Generates the inverted tetrahedron positioned for proper interlocking
3. 🌀 **Rotation Application**: Applies combined Euler rotations with optimized matrix calculations
4. 📏 **Edge SDF Calculation**: Uses precise line segment distance functions for all 12 edges
5. 🔧 **Thickness Application**: Converts line segments to tubes with adjustable radius
6. ✨ **Final Combination**: Merges both tetrahedrons into a single signed distance field

### 🎨 Creative Applications
- 🏛️ **Sacred Architecture**: Design meditation spaces, spiritual centers, and consciousness-expanding installations
- 🎭 **Mystical Stage Design**: Create powerful stage backdrops for spiritual performances and transformative ceremonies
- 🏢 **Modern Geometric Art**: Generate contemporary art installations exploring sacred geometry principles
- 🎮 **Spiritual Game Environments**: Build transcendent spaces, portals, and consciousness-themed level geometry
- 🎨 **Meditation Visualization**: Create animated sequences for guided meditations and consciousness exploration
- 🔮 **Architectural Focal Points**: Design striking structural elements that embody spiritual principles

### 💡 Tips for Best Results
- ✅ Start with the "Default" preset for traditional balanced Merkaba proportions
- ✅ Use **Dicke** (Thickness) around 0.08 for crisp wireframe definition
- ✅ Keep **Verschränkung** (Integration) at 0.25 for classic sacred geometry proportions
- ✅ Experiment with **Rotation X** = 180° on the second pyramid for traditional Merkaba orientation
- ✅ Try the "Bold standard" preset for more substantial visual presence
- ✅ Use slow rotation animation for meditative, consciousness-expanding effects
- ✅ Combine with emission materials for luminous spiritual visualization

### 🎬 Animation Setup Guide
**Merkaba-Pyramid** is designed for profound spiritual and geometric animation! The preset names indicate different energetic and structural approaches:

**Understanding Preset Energetics:**
Each preset demonstrates different spiritual and geometric philosophies. **Open the included example project** to see the complete node setup with proper connections, materials, and optimized camera positions. The project shows how each preset is meant to be experienced - some work best with specific 2D/3D camera angles and rendering settings.

- **"Default"**: Classic balanced Merkaba with traditional proportions
- **"Bold standard"**: Increased size and thickness for commanding presence with global rotation
- **"Swinger King"**: High integration for dynamic interlocking with thick wireframe
- **"Glider"**: Advanced second pyramid rotation (90°/90°/-90°) creating flight-like asymmetry  
- **"BumpyBlober"**: Partial second pyramid rotation for organic, flowing energy patterns (activate Union node in example project)
- **"Knotted one"**: Subtle Z-rotation (25°) creating gentle geometric twist
- **"The Interlocked"**: Complex multi-axis rotation creating sophisticated geometric dance

**Animation Recommendations:**
1. ⭐ **For Sacred Rotation**: Animate global **Rotation Y** for classic spinning Merkaba meditation
2. 🌀 **For Consciousness Expansion**: Slowly animate second pyramid rotations for awakening effects
3. 📏 **For Breathing Effect**: Animate **Grösse** (Size) with sine wave for pulsing sacred geometry
4. 🔄 **For Integration Dance**: Vary **Verschränkung** (Integration) for dynamic interpenetration
5. ✨ **For Light Vehicle**: Combine rotation with emission materials for luminous chariot effect

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.05) → **Global Rotation Y** for slow meditative spinning
2. 🕐 **Time Node** (Speed: 0.08) → **Sine Wave** (Min: 0.8, Max: 1.2, Period: 10.0) → **Grösse** for breathing effect
3. 🕐 **Time Node** (Speed: 0.03) → **Second Pyramid Rotation X/Y/Z** for consciousness awakening patterns
4. 🌀 **Multiple Time Nodes** with different speeds on different rotation axes for complex sacred dance

**Advanced Spiritual Animation:**
For deep meditative experiences, use the example project which demonstrates:
- Multi-layered Merkaba structures
- Union node combinations for complex geometries  
- Emission and transparency effects for light body visualization
- Camera movement synchronized with sacred rotation patterns

### 🔗 Links

- Sacred Geometry Research and Merkaba Symbolism
- COOLLAB Official Website
- Community Node Collection
- Example Project: "Examples for the MERKABA node.coollab"

Coollab-node contributed to the Coollab-Community Nodes collection - August 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Merkaba-Pyramid** Node erzeugt die heilige geometrische Form bekannt als Merkaba - zwei ineinander verschränkte Tetraeder (dreiseitige Pyramiden), die den Stern-Tetraeder oder Stellated Octahedron bilden. Dieser prozedurale Geometrie-Generator produziert die Wireframe-Struktur dieses uralten heiligen Symbols mit präziser geometrischer Genauigkeit und umfangreichen Anpassungsoptionen. Der Node ermöglicht sowohl traditionelle symmetrische Merkaba-Konfigurationen als auch experimentelle asymmetrische Variationen durch unabhängige Pyramiden-Rotationskontrollen.

Die Merkaba repräsentiert die perfekte Vereinigung gegensätzlicher Kräfte, die Schnittstelle zwischen physischem und spirituellem Bereich und den göttlichen Wagen, der in mystischen Traditionen beschrieben wird. In modernen Anwendungen dient sie als mächtiges geometrisches Element für Architekturvisualisierung, spirituelle Kunstinstallationen und raffinierte 3D-Design-Projekte.

**📋 Enthaltene Dateien**

- Merkaba-Pyramid (or the holy sacred dual pyramid).clbnode - Das Haupt-COOLLAB 3D-Form Node
- MERKABA or the sacred DualPyramid.clbnode.presets.json - Preset-Konfigurationen inklusive "Default", "Bold standard", "Swinger King", "Glider", "BumpyBlober", "Knotted one" und "The Interlocked" Variationen
- Examples for the MERKABA node.coollab - Vollständiges Beispielprojekt mit optimalen Node-Verbindungen, Kameraeinstellungen und Preset-Nutzung

**🚀 Verwendung**

*Node Importieren:*

- Alle drei Dateien aus diesem Verzeichnis herunterladen (notwendige Dateien für optimale Funktion)
- Die .clbnode Datei in Ihr COOLLAB Nodes-Verzeichnis in Ihrer aktuellsten Coollab-Version kopieren
- sowie die zugehörige Preset .json Datei und die Beispielprojekt .coollab Datei

Sie können die Node-Dateien in die Kategorie "3D Shapes" platzieren, also in den entsprechend benannten Ordner Ihrer neuesten Coollab-Version, die Sie im Launcher finden. In diesem Beispiel verwende ich Version "1.4.1 Spout OUT". Beachten Sie auch Ihren Benutzernamen (Windows-Konto). Hier der Beispielpfad zur Organisation unter den 3D Shapes:

`C:\Users\_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes\Merkaba-Pyramid`

Die Beispielprojekt-Datei (.coollab) sollte in Ihr Projects-Verzeichnis gelegt werden:

`C:\Users\_YourUserName_\AppData\Roaming\Coollab Launcher\Projects`

*In Szene Verbinden:*

- Als 3D-Geometrie-Quelle in Ihrer Szene verwenden
- Mit Materialien, Beleuchtung und anderen 3D-Nodes kombinieren
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt atemberaubende Lichteffekte durch die Wireframe-Struktur
- Perfekt für spirituelle Visualisierung, architektonische Elemente und geometrische Kunstinstallationen

*Parameter Anpassen:* siehe detaillierte Parameterliste unten

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field repräsentiert Wireframe-Tetraeder
- Performance: Echtzeitfähig mit optimierten SDF-Berechnungen für 12 Kanten
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung
- Geometrie: Mathematisch präzise Merkaba mit korrekter Vertex-Verschränkung

### ✨ Was macht diesen Node besonders
Dies ist nicht nur eine einfache geometrische Form. Der Merkaba-Pyramid Node erstellt die authentische heilige Geometrie mit mathematischer Präzision:
- ⭐ **Wahre Heilige Geometrie**: Erstellt die authentische Merkaba, wo jede Fläche von einem gegenüberliegenden Vertex durchdrungen wird, genau wie das heilige Symbol
- 🔄 **Duales Rotationssystem**: Unabhängige Kontrolle über globale Rotation und zweite Pyramiden-Rotation für unendliche Variationen
- 🏗️ **Wireframe-Präzision**: Saubere 12-Kanten-Wireframe-Struktur mit anpassbarer Dicke für architektonische Anwendungen
- 🎯 **Integrationskontrolle**: Feinabstimmung der Durchdringungstiefe der beiden Pyramiden
- 🎛️ **Animations-bereit**: Perfekt für spirituelle Visualisierungen, meditative Animationen und geometrische Kunstprojekte

### 🎛️ Parameter

#### 📏 Basis-Geometrie-Kontrollen
- **Grösse** (Float, 0.1-2.0): Kontrolliert die Gesamtgröße der kompletten Merkaba-Struktur. Höhere Werte erzeugen größere, prominentere geometrische Präsenz
- **Dicke** (Float, 0.01-0.5): Dicke der Wireframe-Kanten. Kontrolliert wie substanziell die röhrenförmige Struktur erscheint
- **Verschränkung** (Float, -1.0-2.0): Kontrolliert wie tief sich die beiden Pyramiden durchdringen. 0 = perfekte traditionelle Merkaba, positive Werte = mehr Überlappung, negative Werte = Trennung

#### 🌍 Globale Rotationskontrollen
- **Rotation X** (Winkel, 0-360°): Rotiert die gesamte Merkaba-Struktur um die X-Achse
- **Rotation Y** (Winkel, 0-360°): Rotiert die gesamte Merkaba-Struktur um die Y-Achse
- **Rotation Z** (Winkel, 0-360°): Rotiert die gesamte Merkaba-Struktur um die Z-Achse

#### 🔺 Zweite Pyramide Unabhängige Rotation
- **Rotation X** (Winkel, 0-360°): Unabhängige Rotation der zweiten Pyramide nur um ihre X-Achse
- **Rotation Y** (Winkel, 0-360°): Unabhängige Rotation der zweiten Pyramide nur um ihre Y-Achse
- **Rotation Z** (Winkel, 0-360°): Unabhängige Rotation der zweiten Pyramide nur um ihre Z-Achse

### 🎨 Kreative Anwendungen
- 🏛️ **Heilige Architektur**: Meditationsräume, spirituelle Zentren und bewusstseinserweiternde Installationen entwerfen
- 🎭 **Mystisches Bühnendesign**: Kraftvolle Bühnenhintergründe für spirituelle Aufführungen und transformative Zeremonien erstellen
- 🏢 **Moderne Geometrische Kunst**: Zeitgenössische Kunstinstallationen generieren, die heilige Geometrie-Prinzipien erforschen
- 🎮 **Spirituelle Spielumgebungen**: Transzendente Räume, Portale und bewusstseins-thematische Level-Geometrie bauen
- 🎨 **Meditations-Visualisierung**: Animierte Sequenzen für geführte Meditationen und Bewusstseinserforschung erstellen
- 🔮 **Architektonische Brennpunkte**: Auffallende Strukturelemente entwerfen, die spirituelle Prinzipien verkörpern

### 💡 Tipps für beste Ergebnisse
- ✅ Mit dem "Default" Preset für traditionelle ausgewogene Merkaba-Proportionen beginnen
- ✅ **Dicke** um 0.08 für scharfe Wireframe-Definition verwenden
- ✅ **Verschränkung** bei 0.25 für klassische heilige Geometrie-Proportionen halten
- ✅ Mit **Rotation X** = 180° auf der zweiten Pyramide für traditionelle Merkaba-Orientierung experimentieren
- ✅ Das "Bold standard" Preset für substanziellere visuelle Präsenz ausprobieren
- ✅ Langsame Rotationsanimation für meditative, bewusstseinserweiternde Effekte verwenden
- ✅ Mit Emissionsmaterialien für leuchtende spirituelle Visualisierung kombinieren

### 🎬 Animations-Setup Anleitung
**Merkaba-Pyramid** ist für tiefgreifende spirituelle und geometrische Animation konzipiert! Die Preset-Namen zeigen verschiedene energetische und strukturelle Ansätze an:

**Preset-Energetik verstehen:**
Jedes Preset demonstriert verschiedene spirituelle und geometrische Philosophien. **Öffnen Sie das beiliegende Beispielprojekt**, um den vollständigen Node-Aufbau mit korrekten Verbindungen, Materialien und optimierten Kamerapositionen zu sehen. Das Projekt zeigt, wie jedes Preset erlebt werden soll - manche funktionieren am besten mit spezifischen 2D/3D-Kamerawinkeln und Rendering-Einstellungen.

- **"Default"**: Klassische ausgewogene Merkaba mit traditionellen Proportionen
- **"Bold standard"**: Erhöhte Größe und Dicke für kommandierendes Erscheinungsbild mit globaler Rotation
- **"Swinger King"**: Hohe Integration für dynamische Verschränkung mit dickem Wireframe
- **"Glider"**: Fortgeschrittene zweite Pyramiden-Rotation (90°/90°/-90°) erzeugt flug-ähnliche Asymmetrie
- **"BumpyBlober"**: Partielle zweite Pyramiden-Rotation für organische, fließende Energiemuster (Union Node im Beispielprojekt aktivieren)
- **"Knotted one"**: Subtile Z-Rotation (25°) erzeugt sanfte geometrische Drehung
- **"The Interlocked"**: Komplexe Multi-Achsen-Rotation erzeugt raffinierte geometrische Tanzfigur

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.05) → **Globale Rotation Y** für langsame meditative Drehung
2. 🕐 **Time Node** (Geschwindigkeit: 0.08) → **Sine Wave** (Min: 0.8, Max: 1.2, Period: 10.0) → **Grösse** für Atmungseffekt
3. 🕐 **Time Node** (Geschwindigkeit: 0.03) → **Zweite Pyramiden-Rotation X/Y/Z** für Bewusstseins-Erweckungsmuster
4. 🌀 **Mehrere Time Nodes** mit verschiedenen Geschwindigkeiten auf verschiedenen Rotationsachsen für komplexen heiligen Tanz

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Sacred Geometry Foundation**: Ancient Merkaba - Star Tetrahedron ⭐  
**Heilige Geometrie-Grundlage**: Uralte Merkaba - Stern-Tetraeder ⭐

**Category**: 3D Shapes > Sacred Geometry 🏗️  
**Kategorie**: 3D-Formen > Heilige Geometrie 🏗️

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function (12-edge wireframe) ✨  
**Ausgabe**: Signed Distance Function (12-Kanten Wireframe) ✨

**Presets Available / Verfügbare Presets**: 
- **"Default"**: Classic balanced Merkaba (Size: 1.0, Thickness: 0.08, Integration: 0.0) - Traditional proportions
- **"Bold standard"**: Commanding presence (Size: 1.16, Thickness: 0.16, Global rotation) - Substantial visual impact
- **"Swinger King"**: Dynamic interlocking (Size: 0.76, Thickness: 0.26, Integration: 1.49) - High interpenetration
- **"Glider"**: Flight asymmetry (X/Y/Z Rotar-P2: 90°/90°/-90°) - Advanced pyramid rotation for dynamic effects
- **"BumpyBlober"**: Organic patterns (Y/Z Rotar-P2: 90°/-90°) - Partial rotation for flowing energy
- **"Knotted one"**: Gentle twist (Z Rotar-P2: 25°, Thickness: 0.47) - Subtle geometric transformation
- **"The Interlocked"**: Complex dance (Multi-axis rotations, Integration: 0.92) - Sophisticated geometric choreography

**🔗 Links**

Sacred Geometry Research and Merkaba Symbolism
COOLLAB Official Website
COOLLAB Community Node Collection
Example Project: "Examples for the MERKABA node.coollab"
Coollab-node contributed to the Coollab-Community Nodes collection - August 2025
