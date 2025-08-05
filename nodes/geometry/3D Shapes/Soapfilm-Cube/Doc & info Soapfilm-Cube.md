[English](#-english) | [Deutsch](#-deutsch)
---

# 🧼 Soapfilm-Cube Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Soapfilm-Cube** node creates elegant minimal surface structures inspired by Ken Brakke's "Soap film cones" research. This procedural geometry generator produces clean, simplified soap film-like structures within a cubic frame, focusing on essential minimal surface mathematics with straightforward controls. The node simulates the natural behavior of soap films connecting edges and surfaces, creating architecturally clean forms perfect for modern design applications and minimal aesthetic projects.
& It generates refined architectural soap film structures that can serve as contemporary building elements, clean exhibition displays, or minimalist geometric installations with pure minimal surface properties.

**📋 Files Included**

- Soapfilm-Cube.clbnode - The main COOLLAB 3D shape node
- Soapfilm-Cube.clbnode.presets.json - Preset configurations including "SoapOpera", "Tje Foam", "SoapShow", "Holy Moly", "SoapTER", and "ElonaNois" effects

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
- Works excellently with raymarching renderers and creates elegant light transmission effects through clean film surfaces

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable with simplified SDF calculations
- Rendering: Compatible with raymarching and mesh generation

**📜 License & Attribution**

*Mathematical Foundation:*

- Inspired by Ken Brakke's "Soap film cones" research
- Based on minimal surface mathematics and soap film physics
- URL reference: https://kenbrakke.com/cones/cones.htm

*This COOLLAB Node:*

- Idea and project coordination by bennoH.
- Coding by claude.ai in the Sonnet-4 model of Anthropic PBC on a "KostenlosPlan" of bennoH.
- Licensed under GNU General Public License v3.0 by bennoH. 2025
- Compatible with COOLLAB's GPL v3.0 license

### ✨ What Makes This Special
This is not a simple geometric primitive. The Soapfilm-Cube node combines mathematical minimal surface theory with clean architectural design:
- 🏗️ **Simplified Cubic Framework**: Creates a clean 12-edge cube frame structure with precise thickness control
- 🧼 **Pure Soap Film Physics**: Simulates essential minimal surface behavior with simplified algorithms
- 🎯 **Central Surface Control**: Adjustable central flat surface with straightforward size controls
- 🔄 **Clean Connecting Films**: Simplified generation of curved connecting surfaces between frame and center
- 🎛️ **Minimalist Flexibility**: Toggle between frame-only and complete soap film structures with clean controls

### 🎛️ Parameters

#### 🔧 Frame Structure Controls
- 📏 **Frame Thickness** (Float, 0.01-0.5): Controls the thickness of the 12 cube frame edges. Higher values create more substantial structural presence
- 🎯 **Edge Rounding** (Float, 0-0.1): Rounding radius applied to frame edges. Creates softer, more refined edge transitions
- 🔲 **Show Frame Only** (Boolean): Toggle to display only the cubic frame without soap film surfaces for structural studies

#### 🧼 Soap Film Controls
- 🌊 **Film Thickness** (Float, 0.1-2.0): Thickness of the soap film surfaces connecting frame elements. Controls the material presence and visual weight of films
- 📐 **Center Size** (Float, 0.1-0.9): Size of the central flat surface within the cube. Larger values create more prominent central design elements
- 🎯 **Center Offset** (vec3, xyz vector): 3D offset of the central surface from cube center. Enables asymmetric and dynamic architectural compositions

#### 🔄 Surface Blending Controls
- 🌀 **Roundness** (Float, 0-1): Smoothness of surface blending between different film elements. Higher values create more organic, flowing transitions

### ⚙️ Technical Implementation
The simplified soap film structure generation works through clean mathematical stages:
1. 🏗️ **Frame Construction**: Creates 12 precise cube edges using optimized capsule SDFs with clean corner connections
2. 🎯 **Central Surface Generation**: Constructs a refined rounded square surface in the XY plane with controllable proportions
3. 🧼 **Film Connection Calculation**: Generates simplified curved connecting surfaces between frame corners and central surface
4. 🌀 **Smooth Blending**: Applies optimized smooth minimum functions for natural surface transitions
5. 📏 **Distance Field Output**: Combines all elements into a single, clean signed distance field

### 🎨 Creative Applications
- 🏛️ **Minimalist Architecture**: Design clean contemporary pavilions, museum installations, or refined exhibition structures
- 🎭 **Clean Stage Design**: Create elegant theatrical backdrops and performance spaces with pure structural elements
- 🏢 **Modern Urban Planning**: Generate refined public art installations, contemporary bus stops, or architectural focal points
- 🎮 **Clean Game Environment Design**: Build elegant futuristic structures, refined sci-fi architecture, or minimalist level geometry
- 🎨 **Architectural Visualization**: Explore essential minimal surface concepts in modern building design and structural engineering

### 💡 Tips for Best Results
- ✅ Start with **Frame Thickness** around 0.25-0.3 for well-balanced structural elements
- ✅ Use **Film Thickness** values between 0.5-0.6 for elegant soap film appearance
- ✅ Set **Center Size** around 0.5-0.6 for harmonious architectural proportions
- ✅ Keep **Roundness** very low (near 0) for sharp, clean architectural edges
- ✅ Animate **Center Size** for dynamic architectural scaling effects
- ✅ Use **Show Frame Only** to study the pure structural framework

### 🎬 Animation Setup Guide
**Soapfilm-Cube** is designed for clean architectural animation! The preset names indicate different structural and aesthetic approaches:

**Understanding Preset Architectures:**
Each preset demonstrates different design philosophies and structural characteristics:

**Animation Recommendations:**
1. 🏗️ **For Clean Structural Animation**: Animate **Frame Thickness** to show refined construction/deconstruction processes
2. 🌊 **For Film Formation**: Gradually change **Film Thickness** to simulate elegant soap film formation
3. 🎯 **For Spatial Dynamics**: Animate **Center Size** for expanding/contracting central elements
4. 🔄 **For Asymmetric Design**: Vary **Center Offset** components for shifting architectural focus

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.15) → **Sine Wave** (Min: 0.2, Max: 0.4, Period: 12.0) → **Frame Thickness**
2. 🕐 **Time Node** (Speed: 0.25) → **Sine Wave** (Min: 0.4, Max: 0.8, Period: 8.0) → **Film Thickness**  
3. 🕐 **Time Node** (Speed: 0.1) → **Sine Wave** (Min: 0.3, Max: 0.7, Period: 15.0) → **Center Size**
4. 🔄 **Rotate Node** with **Time Node** (Speed: 0.03) → **Y-axis** for slow, elegant architectural presentation

**🔗 Links**

- Ken Brakke's Soap Film Cones Research: https://kenbrakke.com/cones/cones.htm
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Soapfilm-Cube** Node erzeugt elegante Minimalflächen-Strukturen inspiriert von Ken Brakkes "Soap film cones" Forschung. Dieser prozedurale Geometrie-Generator produziert saubere, vereinfachte seifenfilm-ähnliche Strukturen innerhalb eines kubischen Rahmens und konzentriert sich auf wesentliche Minimalflächen-Mathematik mit unkomplizierten Kontrollen. Der Node simuliert das natürliche Verhalten von Seifenfilmen, die Kanten und Oberflächen verbinden, und erzeugt architektonisch saubere Formen, die perfekt für moderne Designanwendungen und minimalistische Ästhetik-Projekte geeignet sind.
& generiert verfeinerte architektonische Seifenfilm-Strukturen, die als zeitgenössische Gebäudeelemente, saubere Ausstellungsdisplays oder minimalistische geometrische Installationen mit reinen Minimalflächen-Eigenschaften dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- Soapfilm-Cube.clbnode - Das Haupt-COOLLAB 3D-Form Node
- Soapfilm-Cube.clbnode.presets.json - Preset-Konfigurationen inklusive "SoapOpera", "Tje Foam", "SoapShow", "Holy Moly", "SoapTER" und "ElonaNois" Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt elegante Lichttransmissionseffekte durch saubere Film-Oberflächen

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig mit vereinfachten SDF-Berechnungen
- Rendering: Kompatibel mit Raymarching und Mesh-Generierung

**📜 Lizenz & Attribution**

*Mathematische Grundlage:*

- Inspiriert von Ken Brakkes "Soap film cones" Forschung
- Basierend auf Minimalflächen-Mathematik und Seifenfilm-Physik
- URL-Referenz: https://kenbrakke.com/cones/cones.htm

*Dieses COOLLAB Node:*

- Idee und Projektkoordination von bennoH.
- Programmierung von claude.ai im Sonnet-4 Modell von Anthropic PBC auf einem "KostenlosPlan" von bennoH.
- Lizenziert unter GNU General Public License v3.0 von bennoH. 2025
- Kompatibel mit COOLLABs GPL v3.0 Lizenz

### ✨ Was macht diesen Node besonders
Dies ist keine einfache geometrische Primitive. Der Soapfilm-Cube Node kombiniert mathematische Minimalflächen-Theorie mit sauberem architektonischem Design:
- 🏗️ **Vereinfachtes Kubisches Framework**: Erzeugt eine saubere 12-Kanten-Würfelrahmen-Struktur mit präziser Dickenkontrolle
- 🧼 **Reine Seifenfilm-Physik**: Simuliert wesentliches Minimalflächen-Verhalten mit vereinfachten Algorithmen
- 🎯 **Zentrale Oberflächenkontrolle**: Anpassbare zentrale flache Oberfläche mit unkomplizierten Größenkontrollen
- 🔄 **Saubere Verbindungsfilme**: Vereinfachte Generierung gekrümmter Verbindungsoberflächen zwischen Rahmen und Zentrum
- 🎛️ **Minimalistische Flexibilität**: Umschaltung zwischen reinem Rahmen und vollständigen Seifenfilm-Strukturen mit sauberen Kontrollen

### 🎛️ Parameter

#### 🔧 Rahmenstruktur-Kontrollen
- 📏 **Frame Thickness** (Float, 0.01-0.5): Kontrolliert die Dicke der 12 Würfelrahmen-Kanten. Höhere Werte erzeugen substanziellere strukturelle Präsenz
- 🎯 **Edge Rounding** (Float, 0-0.1): Rundungsradius für Rahmenkanten. Erzeugt weichere, verfeinerte Kantenübergänge
- 🔲 **Show Frame Only** (Boolean): Umschalter zur Anzeige nur des kubischen Rahmens ohne Seifenfilm-Oberflächen für Strukturstudien

#### 🧼 Seifenfilm-Kontrollen
- 🌊 **Film Thickness** (Float, 0.1-2.0): Dicke der Seifenfilm-Oberflächen, die Rahmenelemente verbinden. Kontrolliert die materielle Präsenz und visuelle Gewichtung der Filme
- 📐 **Center Size** (Float, 0.1-0.9): Größe der zentralen flachen Oberfläche innerhalb des Würfels. Größere Werte erzeugen prominentere zentrale Designelemente
- 🎯 **Center Offset** (vec3, xyz-Vektor): 3D-Versatz der zentralen Oberfläche vom Würfelzentrum. Ermöglicht asymmetrische und dynamische architektonische Kompositionen

#### 🔄 Oberflächenmischungs-Kontrollen
- 🌀 **Roundness** (Float, 0-1): Glätte der Oberflächenmischung zwischen verschiedenen Film-Elementen. Höhere Werte erzeugen organischere, fließendere Übergänge

### ⚙️ Technische Implementation
Die vereinfachte Seifenfilm-Struktur-Generierung funktioniert durch saubere mathematische Stufen:
1. 🏗️ **Rahmen-Konstruktion**: Erzeugt 12 präzise Würfelkanten mit optimierten Kapsel-SDFs und sauberen Eckverbindungen
2. 🎯 **Zentrale Oberflächengenerierung**: Konstruiert eine verfeinerte gerundete quadratische Oberfläche in der XY-Ebene mit kontrollierbaren Proportionen
3. 🧼 **Film-Verbindungsberechnung**: Generiert vereinfachte gekrümmte Verbindungsoberflächen zwischen Rahmenecken und zentraler Oberfläche
4. 🌀 **Glatte Mischung**: Wendet optimierte glatte Minimum-Funktionen für natürliche Oberflächenübergänge an
5. 📏 **Distance Field Ausgabe**: Kombiniert alle Elemente in ein einziges, sauberes Signed Distance Field

### 🎨 Kreative Anwendungen
- 🏛️ **Minimalistische Architektur**: Saubere zeitgenössische Pavillons, Museumsinstallationen oder verfeinerte Ausstellungsstrukturen entwerfen
- 🎭 **Sauberes Bühnendesign**: Elegante theatrale Hintergründe und Aufführungsräume mit reinen Strukturelementen erstellen
- 🏢 **Moderne Stadtplanung**: Verfeinerte öffentliche Kunstinstallationen, zeitgenössische Bushaltestellen oder architektonische Brennpunkte generieren
- 🎮 **Sauberes Spielumgebungs-Design**: Elegante futuristische Strukturen, verfeinerte Sci-Fi-Architektur oder minimalistische Level-Geometrie bauen
- 🎨 **Architektur-Visualisierung**: Wesentliche Minimalflächen-Konzepte im modernen Gebäudedesign und Strukturingenieurwesen erkunden

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Frame Thickness** um 0.25-0.3 für gut ausbalancierte Strukturelemente beginnen
- ✅ **Film Thickness**-Werte zwischen 0.5-0.6 für elegante Seifenfilm-Erscheinung verwenden
- ✅ **Center Size** um 0.5-0.6 für harmonische architektonische Proportionen setzen
- ✅ **Roundness** sehr niedrig (nahe 0) für scharfe, saubere architektonische Kanten halten
- ✅ **Center Size** für dynamische architektonische Skalierungseffekte animieren
- ✅ **Show Frame Only** verwenden, um das reine Strukturframework zu studieren

### 🎬 Animations-Setup Anleitung
**Soapfilm-Cube** ist für saubere architektonische Animation konzipiert! Die Preset-Namen zeigen verschiedene strukturelle und ästhetische Ansätze an:

**Preset-Architekturen verstehen:**
Jedes Preset demonstriert verschiedene Designphilosophien und strukturelle Charakteristiken:

**Animations-Empfehlungen:**
1. 🏗️ **Für saubere Struktur-Animation**: **Frame Thickness** animieren, um verfeinerte Konstruktions-/Dekonstruktionsprozesse zu zeigen
2. 🌊 **Für Film-Formation**: **Film Thickness** allmählich ändern, um elegante Seifenfilm-Formation zu simulieren
3. 🎯 **Für räumliche Dynamik**: **Center Size** für expandierende/kontrahierende zentrale Elemente animieren
4. 🔄 **Für asymmetrisches Design**: **Center Offset**-Komponenten für sich verändernden architektonischen Fokus variieren

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.15) → **Sine Wave** (Min: 0.2, Max: 0.4, Period: 12.0) → **Frame Thickness**
2. 🕐 **Time Node** (Geschwindigkeit: 0.25) → **Sine Wave** (Min: 0.4, Max: 0.8, Period: 8.0) → **Film Thickness**  
3. 🕐 **Time Node** (Geschwindigkeit: 0.1) → **Sine Wave** (Min: 0.3, Max: 0.7, Period: 15.0) → **Center Size**
4. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.03) → **Y-Achse** für langsame, elegante architektonische Präsentation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Inspired by**: Ken Brakke's Soap Film Cones Research 🧼  
**Inspiriert von**: Ken Brakkes Seifenfilm-Kegel-Forschung 🧼

**Category**: 3D Shapes > Minimal Surfaces 🏗️  
**Kategorie**: 3D-Formen > Minimalflächen 🏗️

**Input**: Procedural (no input required) 🔧  
**Eingabe**: Prozedural (keine Eingabe erforderlich) 🔧

**Output**: Signed Distance Function ✨  
**Ausgabe**: Signed Distance Function ✨

**Presets Available**: 
- "SoapOpera" - Dramatic thick frame with substantial film thickness (0.29/0.61)
- "Tje Foam" - Balanced foam-like structure with moderate proportions (0.4/0.5)
- "SoapShow" - Clean presentation structure with refined frame (0.26/0.5)
- "Holy Moly" - Frame-only structure for pure architectural studies (0.19 frame only)
- "SoapTER" - Thick central element with full-size center (0.26/1.0/1.0)
- "ElonaNois" - Complex structure with thick films and negative roundness (0.31/1.64/0.68)

**Verfügbare Presets**: 
- "SoapOpera" - Dramatischer dicker Rahmen mit substantieller Filmdicke (0.29/0.61)
- "Tje Foam" - Ausgewogene schaumartige Struktur mit moderaten Proportionen (0.4/0.5)
- "SoapShow" - Saubere Präsentationsstruktur mit verfeinertem Rahmen (0.26/0.5)
- "Holy Moly" - Nur-Rahmen-Struktur für reine architektonische Studien (0.19 nur Rahmen)
- "SoapTER" - Dickes zentrales Element mit vollgroßem Zentrum (0.26/1.0/1.0)
- "ElonaNois" - Komplexe Struktur mit dicken Filmen und negativer Rundung (0.31/1.64/0.68)

**🔗 Links**

- Ken Brakke's Soap Film Cones Research: https://kenbrakke.com/cones/cones.htm
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025
