[English](#-english) | [Deutsch](#-deutsch)
---

# 🧼 SoapFilm-Akropolis Node Documentation

## 🇬🇧 English

### 📋 Overview
The **SoapFilm-Akropolis** node creates sophisticated minimal surface structures inspired by Ken Brakke's "Soap film cones" research. This procedural geometry generator produces soap film-like structures within a cubic frame, combining architectural elements with natural minimal surface mathematics. The node simulates the organic behavior of soap films connecting edges and surfaces, creating architecturally striking forms reminiscent of modern pavilions or exhibition structures.
& It generates stunning architectural soap film structures that can serve as modern building designs, exhibition pavilions, or abstract geometric installations with natural minimal surface properties.

**📋 Files Included**

- SoapFilm-Akropolis.clbnode - The main COOLLAB 3D shape node
- SoapFilm-Akropolis.clbnode.presets.json - Preset configurations including "Nekropolis", "Tec CubeFrame", "Centre Pombidu style", "SandyTimer", "Laterna", "Psy Cuberframe", "RodrigoRODOS", "Essa Bree", "Ivori Cube", "The Stage", "Moshy Planet", and "Serenyti" effects

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
- Works excellently with raymarching renderers and creates beautiful light transmission effects through film surfaces

*Adjust Parameters:* see the parameter list

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable with optimized SDF calculations
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
This is not a simple geometric primitive. The SoapFilm-Akropolis node combines mathematical minimal surface theory with architectural design:
- 🏗️ **Cubic Framework**: Creates a precise 12-edge cube frame structure with controllable thickness
- 🧼 **Soap Film Physics**: Simulates natural minimal surface behavior of soap films
- 🎯 **Central Surface Control**: Adjustable central flat surface with size and offset controls
- 🔄 **Connecting Films**: Automatic generation of curved connecting surfaces between frame and center
- 🎛️ **Architectural Flexibility**: Toggle between frame-only and complete soap film structures

### 🎛️ Parameters

#### 🔧 Frame Structure Controls
- 📏 **Frame Thickness** (Float, 0.01-0.1): Controls the thickness of the 12 cube frame edges. Higher values create more substantial structural elements
- 🎯 **Edge Rounding** (Float, 0-0.05): Rounding radius applied to frame edges. Creates softer, more organic frame connections
- 🔲 **Show Frame Only** (Boolean): Toggle to display only the cubic frame without soap film surfaces

#### 🧼 Soap Film Controls
- 🌊 **Film Thickness** (Float, 0.005-0.05): Thickness of the soap film surfaces connecting frame elements. Affects the material presence of the films
- 📐 **Center Size** (Float, 0.2-0.8): Size of the central flat surface within the cube. Larger values create more prominent central elements
- 🎯 **Center Offset** (vec3, xyz vector): 3D offset of the central surface from cube center. Allows asymmetric architectural compositions

#### 🔄 Surface Blending Controls
- 🌀 **Roundness** (Float, 0.01-0.2): Smoothness of surface blending between different film elements. Higher values create more organic transitions

### ⚙️ Technical Implementation
The soap film structure generation works through sophisticated mathematical stages:
1. 🏗️ **Frame Construction**: Creates 12 precise cube edges using rounded capsule SDFs with proper corner connections
2. 🎯 **Central Surface Generation**: Constructs a rounded square surface in the XY plane with controllable size and offset
3. 🧼 **Film Connection Calculation**: Generates curved connecting surfaces between frame corners and central surface
4. 🌀 **Smooth Blending**: Applies smooth minimum functions for natural surface transitions
5. 📏 **Distance Field Output**: Combines all elements into a single signed distance field

### 🎨 Creative Applications
- 🏛️ **Modern Architecture**: Design contemporary pavilions, museum installations, or exhibition structures
- 🎭 **Stage Design**: Create theatrical backdrops and performance spaces with organic structural elements
- 🏢 **Urban Planning**: Generate public art installations, bus stops, or architectural focal points
- 🎮 **Game Environment Design**: Build futuristic structures, sci-fi architecture, or abstract level geometry
- 🎨 **Architectural Visualization**: Explore minimal surface concepts in building design and structural engineering

### 💡 Tips for Best Results
- ✅ Start with **Frame Thickness** around 0.05 for well-visible structural elements
- ✅ Use **Film Thickness** values between 0.01-0.03 for realistic soap film appearance
- ✅ Set **Center Size** around 0.4-0.6 for balanced architectural proportions
- ✅ Keep **Roundness** low (0.05-0.1) for sharp architectural edges, higher for organic forms
- ✅ Animate **Center Offset** for dynamic architectural transformations
- ✅ Use **Show Frame Only** to study the underlying structural framework

### 🎬 Animation Setup Guide
**SoapFilm-Akropolis** is designed for architectural animation! The preset names indicate different architectural styles and characteristics:

**Understanding Preset Architectures:**
Each preset demonstrates different architectural approaches:

**Animation Recommendations:**
1. 🏗️ **For Structural Animation**: Animate **Frame Thickness** to show construction/deconstruction processes
2. 🌊 **For Film Formation**: Gradually change **Film Thickness** to simulate soap film formation
3. 🎯 **For Spatial Dynamics**: Animate **Center Offset** components for shifting architectural focus
4. 🔄 **For Surface Morphing**: Vary **Center Size** for expanding/contracting central elements

**Recommended Animation Setup:**
1. 🕐 **Time Node** (Speed: 0.2) → **Sine Wave** (Min: 0.02, Max: 0.08, Period: 10.0) → **Frame Thickness**
2. 🕐 **Time Node** (Speed: 0.3) → **Sine Wave** (Min: 0.01, Max: 0.05, Period: 8.0) → **Film Thickness**  
3. 🕐 **Time Node** (Speed: 0.1) → **Sine Wave** (Min: -0.1, Max: 0.1, Period: 15.0) → **Center Offset Y**
4. 🔄 **Rotate Node** with **Time Node** (Speed: 0.05) → **Y-axis** for slow architectural presentation

**🔗 Links**

- Ken Brakke's Soap Film Cones Research: https://kenbrakke.com/cones/cones.htm
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **SoapFilm-Akropolis** Node erzeugt anspruchsvolle Minimalflächen-Strukturen inspiriert von Ken Brakkes "Soap film cones" Forschung. Dieser prozedurale Geometrie-Generator produziert seifenfilm-ähnliche Strukturen innerhalb eines kubischen Rahmens und kombiniert architektonische Elemente mit natürlicher Minimalflächen-Mathematik. Der Node simuliert das organische Verhalten von Seifenfilmen, die Kanten und Oberflächen verbinden, und erzeugt architektonisch beeindruckende Formen, die an moderne Pavillons oder Ausstellungsstrukturen erinnern.
& generiert beeindruckende architektonische Seifenfilm-Strukturen, die als moderne Gebäudedesigns, Ausstellungspavillons oder abstrakte geometrische Installationen mit natürlichen Minimalflächen-Eigenschaften dienen können.

**📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)**

- SoapFilm-Akropolis.clbnode - Das Haupt-COOLLAB 3D-Form Node
- SoapFilm-Akropolis.clbnode.presets.json - Preset-Konfigurationen inklusive "Nekropolis", "Tec CubeFrame", "Centre Pombidu style", "SandyTimer", "Laterna", "Psy Cuberframe", "RodrigoRODOS", "Essa Bree", "Ivori Cube", "The Stage", "Moshy Planet" und "Serenyti" Effekte

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
- Funktioniert hervorragend mit Raymarching-Renderern und erzeugt wunderschöne Lichttransmissionseffekte durch Film-Oberflächen

*Parameter Anpassen:* siehe Parameterliste die weiter unten folgt

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig mit optimierten SDF-Berechnungen
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
Dies ist keine einfache geometrische Primitive. Der SoapFilm-Akropolis Node kombiniert mathematische Minimalflächen-Theorie mit architektonischem Design:
- 🏗️ **Kubisches Framework**: Erzeugt eine präzise 12-Kanten-Würfelrahmen-Struktur mit kontrollierbarer Dicke
- 🧼 **Seifenfilm-Physik**: Simuliert natürliches Minimalflächen-Verhalten von Seifenfilmen
- 🎯 **Zentrale Oberflächenkontrolle**: Anpassbare zentrale flache Oberfläche mit Größen- und Versatz-Kontrollen
- 🔄 **Verbindungsfilme**: Automatische Generierung gekrümmter Verbindungsoberflächen zwischen Rahmen und Zentrum
- 🎛️ **Architektonische Flexibilität**: Umschaltung zwischen reinem Rahmen und vollständigen Seifenfilm-Strukturen

### 🎛️ Parameter

#### 🔧 Rahmenstruktur-Kontrollen
- 📏 **Frame Thickness** (Float, 0.01-0.1): Kontrolliert die Dicke der 12 Würfelrahmen-Kanten. Höhere Werte erzeugen substanziellere Strukturelemente
- 🎯 **Edge Rounding** (Float, 0-0.05): Rundungsradius für Rahmenkanten. Erzeugt weichere, organischere Rahmenverbindungen
- 🔲 **Show Frame Only** (Boolean): Umschalter zur Anzeige nur des kubischen Rahmens ohne Seifenfilm-Oberflächen

#### 🧼 Seifenfilm-Kontrollen
- 🌊 **Film Thickness** (Float, 0.005-0.05): Dicke der Seifenfilm-Oberflächen, die Rahmenelemente verbinden. Beeinflusst die materielle Präsenz der Filme
- 📐 **Center Size** (Float, 0.2-0.8): Größe der zentralen flachen Oberfläche innerhalb des Würfels. Größere Werte erzeugen prominentere zentrale Elemente
- 🎯 **Center Offset** (vec3, xyz-Vektor): 3D-Versatz der zentralen Oberfläche vom Würfelzentrum. Ermöglicht asymmetrische architektonische Kompositionen

#### 🔄 Oberflächenmischungs-Kontrollen
- 🌀 **Roundness** (Float, 0.01-0.2): Glätte der Oberflächenmischung zwischen verschiedenen Film-Elementen. Höhere Werte erzeugen organischere Übergänge

### ⚙️ Technische Implementation
Die Seifenfilm-Struktur-Generierung funktioniert durch ausgeklügelte mathematische Stufen:
1. 🏗️ **Rahmen-Konstruktion**: Erzeugt 12 präzise Würfelkanten mit gerundeten Kapsel-SDFs und korrekten Eckverbindungen
2. 🎯 **Zentrale Oberflächengenerierung**: Konstruiert eine gerundete quadratische Oberfläche in der XY-Ebene mit kontrollierbarer Größe und Versatz
3. 🧼 **Film-Verbindungsberechnung**: Generiert gekrümmte Verbindungsoberflächen zwischen Rahmenecken und zentraler Oberfläche
4. 🌀 **Glatte Mischung**: Wendet glatte Minimum-Funktionen für natürliche Oberflächenübergänge an
5. 📏 **Distance Field Ausgabe**: Kombiniert alle Elemente in ein einziges Signed Distance Field

### 🎨 Kreative Anwendungen
- 🏛️ **Moderne Architektur**: Zeitgenössische Pavillons, Museumsinstallationen oder Ausstellungsstrukturen entwerfen
- 🎭 **Bühnendesign**: Theatrale Hintergründe und Aufführungsräume mit organischen Strukturelementen erstellen
- 🏢 **Stadtplanung**: Öffentliche Kunstinstallationen, Bushaltestellen oder architektonische Brennpunkte generieren
- 🎮 **Spielumgebungs-Design**: Futuristische Strukturen, Sci-Fi-Architektur oder abstrakte Level-Geometrie bauen
- 🎨 **Architektur-Visualisierung**: Minimalflächen-Konzepte im Gebäudedesign und Strukturingenieurwesen erkunden

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Frame Thickness** um 0.05 für gut sichtbare Strukturelemente beginnen
- ✅ **Film Thickness**-Werte zwischen 0.01-0.03 für realistische Seifenfilm-Erscheinung verwenden
- ✅ **Center Size** um 0.4-0.6 für ausgewogene architektonische Proportionen setzen
- ✅ **Roundness** niedrig (0.05-0.1) für scharfe architektonische Kanten, höher für organische Formen halten
- ✅ **Center Offset** für dynamische architektonische Transformationen animieren
- ✅ **Show Frame Only** verwenden, um das zugrundeliegende Strukturframework zu studieren

### 🎬 Animations-Setup Anleitung
**SoapFilm-Akropolis** ist für architektonische Animation konzipiert! Die Preset-Namen zeigen verschiedene architektonische Stile und Charakteristiken an:

**Preset-Architekturen verstehen:**
Jedes Preset demonstriert verschiedene architektonische Ansätze:

**Animations-Empfehlungen:**
1. 🏗️ **Für Struktur-Animation**: **Frame Thickness** animieren, um Konstruktions-/Dekonstruktionsprozesse zu zeigen
2. 🌊 **Für Film-Formation**: **Film Thickness** allmählich ändern, um Seifenfilm-Formation zu simulieren
3. 🎯 **Für räumliche Dynamik**: **Center Offset**-Komponenten für sich verändernden architektonischen Fokus animieren
4. 🔄 **Für Oberflächenmorphing**: **Center Size** für expandierende/kontrahierende zentrale Elemente variieren

**Empfohlenes Animations-Setup:**
1. 🕐 **Time Node** (Geschwindigkeit: 0.2) → **Sine Wave** (Min: 0.02, Max: 0.08, Period: 10.0) → **Frame Thickness**
2. 🕐 **Time Node** (Geschwindigkeit: 0.3) → **Sine Wave** (Min: 0.01, Max: 0.05, Period: 8.0) → **Film Thickness**  
3. 🕐 **Time Node** (Geschwindigkeit: 0.1) → **Sine Wave** (Min: -0.1, Max: 0.1, Period: 15.0) → **Center Offset Y**
4. 🔄 **Rotate Node** mit **Time Node** (Geschwindigkeit: 0.05) → **Y-Achse** für langsame architektonische Präsentation

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
- "Nekropolis" - Frame-focused structure with minimal films
- "Tec CubeFrame" - Technical cubic framework with film variations
- "Centre Pombidu style" - Modern architectural pavilion approach
- "SandyTimer" - Organic timer-like form with thick films
- "Laterna" - Lantern-inspired structure with balanced proportions
- "Psy Cuberframe" - Psychedelic cube frame with medium films
- "RodrigoRODOS" - Architectural installation with thick soap films
- "Essa Bree" - Minimalist structure with thin frame elements
- "Ivori Cube" - Clean cubic form with centered surface
- "The Stage" - Performance platform with flat central surface
- "Moshy Planet" - Planetary sphere-like form with large center
- "Serenyti" - Serene architectural form with thick frames

**Verfügbare Presets**: 
- "Nekropolis" - Rahmen-fokussierte Struktur mit minimalen Filmen
- "Tec CubeFrame" - Technisches kubisches Framework mit Film-Variationen
- "Centre Pombidu style" - Moderner architektonischer Pavillon-Ansatz
- "SandyTimer" - Organische sanduhr-ähnliche Form mit dicken Filmen
- "Laterna" - Laternen-inspirierte Struktur mit ausgewogenen Proportionen
- "Psy Cuberframe" - Psychedelischer Würfelrahmen mit mittleren Filmen
- "RodrigoRODOS" - Architektonische Installation mit dicken Seifenfilmen
- "Essa Bree" - Minimalistische Struktur mit dünnen Rahmenelementen
- "Ivori Cube" - Saubere kubische Form mit zentrierter Oberfläche
- "The Stage" - Aufführungsplattform mit flacher zentraler Oberfläche
- "Moshy Planet" - Planetare kugel-ähnliche Form mit großem Zentrum
- "Serenyti" - Ruhige architektonische Form mit dicken Rahmen

**🔗 Links**

- Ken Brakke's Soap Film Cones Research: https://kenbrakke.com/cones/cones.htm
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coollab-Community Nodes collection - June 2025
