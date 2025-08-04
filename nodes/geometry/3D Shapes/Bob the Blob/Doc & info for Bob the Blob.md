[English](#-english) | [Deutsch](#-deutsch)
---

# 🟡 Bob the Blob Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Bob the Blob** node creates smooth, organic 3D blob shapes with customizable surface details. This procedural geometry generator produces natural, bulbous forms reminiscent of sea creatures, organic cells, or abstract sculptural elements. Inspired by the cool Blob from VisualJockai-SP1, this streamlined version offers essential blob creation capabilities with two key parameters for size and surface texture control.
& It generates beautiful organic 3D shapes that serve as perfect building blocks for artistic scenes, character modeling bases, or abstract compositions.

**📋 Files Included**

- Bob the Blob.clbnode - The main COOLLAB 3D shape node

**🚀 How to Use**

*Import the Node:*

- Download the .clbnode file from this directory
- Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that

You can place the file in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*Connect to Scene:*

- Use as a 3D geometry source in your scene
- Combine with materials, lighting, and other 3D nodes
- Works excellently with raymarching renderers

*Adjust Parameters:* see the parameter list below

**⚙️ Technical Details**

- Node Type: 3D Shape (Signed Distance Function)
- Input: Procedural generation (no input required)
- Output: 3D signed distance field
- Performance: Real-time capable, lightweight
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
This is the essential blob generator with optimized simplicity:
- 🎯 **Streamlined Interface**: Just two intuitive parameters for quick blob creation
- 🌊 **Golden Ratio Integration**: Built-in PHI constant (1.618) for naturally pleasing proportions  
- 🔄 **Coordinate Sorting**: Automatic orientation optimization for consistent shape generation
- ⚡ **High Performance**: Lightweight implementation for real-time rendering

### 🎛️ Parameters

#### 🔧 Core Shape Controls
- 📏 **Size** (Float, adjustable): Controls the overall scale of the blob. Larger values create bigger blobs, smaller values create more compact shapes
- 🌊 **Bumpiness** (Float, range 0.0-1.0): Controls the surface detail intensity. Higher values create more pronounced surface variations and organic texture

### ⚙️ Technical Implementation
The blob generation works through several mathematical stages:
1. 🔄 **Position Scaling**: Input coordinates are scaled by the inverse of the Size parameter
2. 🪞 **Symmetry Application**: Absolute value operations create symmetric base structure
3. 📊 **Coordinate Sorting**: Automatic sorting ensures proper orientation regardless of input
4. 📐 **Golden Ratio Calculation**: Uses PHI constant (1.618) for mathematically pleasing proportions
5. 🎯 **Dot Product Operations**: Complex calculations using normalized direction vectors
6. 🌊 **Surface Modulation**: Cosine-based surface detail application using Bumpiness parameter
7. 📏 **Distance Field Generation**: Final signed distance calculation with size scaling

### 🎨 Creative Applications
- 🧬 **Organic Modeling**: Create cell-like structures, bacteria, or microscopic organisms
- 🌊 **Sea Creature Design**: Generate jellyfish, sea anemones, or abstract marine life
- 🏗️ **Architectural Elements**: Use for organic building components or sculptural elements
- 🎮 **Game Assets**: Perfect for alien creatures, fantasy elements, or environmental objects
- 🎨 **Abstract Art**: Foundation for complex organic compositions
- 🔬 **Scientific Visualization**: Represent molecular structures or biological forms

### 💡 Tips for Best Results
- ✅ Start with **Size** around 1.0 for standard-scale blobs
- ✅ Use **Bumpiness** values between 0.3-0.8 for natural organic texture
- ✅ Set **Bumpiness** to 0.0 for smooth, minimal blob surfaces
- ✅ Set **Bumpiness** to 1.0 for maximum surface detail and texture
- ✅ Animate both parameters for dynamic morphing effects
- ✅ Combine multiple blobs with different sizes for complex compositions

### 🎬 Animation Possibilities
**Bob the Blob** is perfect for animation:

**Recommended Animation Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 3.0) → **Size**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.2, Max: 0.8, Period: 5.0) → **Bumpiness**
3. 🔄 **Rotate Node** with **Time Node** for spinning blob effects
4. 🌊 **3D-Wave Node** for organic deformation animations

**Creative Animation Ideas:**
- **Breathing Effect**: Animate Size with slow sine wave
- **Texture Pulse**: Animate Bumpiness for surface detail changes
- **Growing Organism**: Linear increase of Size over time
- **Morphing Blob**: Combine Size and Bumpiness animations

### 🆚 Comparison with Bob the Blob Pro
This streamlined version focuses on simplicity and performance:
- ✅ **Faster Rendering**: Fewer calculations for real-time performance
- ✅ **Easier Setup**: Only 2 parameters vs 6 in the Pro version
- ✅ **Golden Ratio Built-in**: Automatic PHI integration (1.618)
- ❌ **Limited Directional Control**: No custom direction vectors
- ❌ **Fixed Proportions**: Cannot adjust PHI parameter manually

**Choose Bob the Blob when you want:**
- Quick, simple blob generation
- Maximum performance
- Consistent, reliable results

**Choose Bob the Blob Pro when you need:**
- Advanced directional control
- Custom PHI adjustments
- Complex asymmetric shapes

**🔗 Links**

- VisualJockai-SP1 Original Inspiration
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025

---

## 🇩🇪 Deutsch

[English](#-english) | [Deutsch](#-deutsch)

### 📋 Überblick
Der **Bob the Blob** Node erzeugt glatte, organische 3D-Blob-Formen mit anpassbaren Oberflächendetails. Dieser prozedurale Geometrie-Generator produziert natürliche, bauchige Formen, die an Meerestiere, organische Zellen oder abstrakte skulpturale Elemente erinnern. Inspiriert vom coolen Blob aus VisualJockai-SP1 bietet diese optimierte Version essentielle Blob-Erstellungs-Fähigkeiten mit zwei Hauptparametern für Größen- und Oberflächentextur-Kontrolle.
& generiert wunderschöne organische 3D-Formen, die als perfekte Bausteine für künstlerische Szenen, Charakter-Modeling-Basen oder abstrakte Kompositionen dienen.

**📋 Enthaltene Dateien**

- Bob the Blob.clbnode - Das Haupt-COOLLAB 3D-Form Node

**🚀 Verwendung sprich Installationsanleitung**

*Node Importieren:*

- Die .clbnode Datei aus diesem Verzeichnis herunterladen
- Die .clbnode Datei in Ihr COOLLAB Launcher in das Node-Verzeichnis der aktuellsten Coollab-Version kopieren

Sie können die Datei in die Kategorie "3D Shapes" respektive den entsprechenden Ordner hinein legen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "3D Shapes" einzuordnen: 

`C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\08 3D Shapes`

*In Szene Verbinden:*

- Als 3D-Geometrie-Quelle in Ihrer Szene verwenden
- Mit Materialien, Beleuchtung und anderen 3D-Nodes kombinieren
- Funktioniert hervorragend mit Raymarching-Renderern

*Parameter Anpassen:* siehe Parameterliste weiter unten

**⚙️ Technische Details**

- Node-Typ: 3D-Form (Signed Distance Function)
- Eingabe: Prozedurale Generierung (keine Eingabe erforderlich)
- Ausgabe: 3D Signed Distance Field
- Performance: Echtzeitfähig, leichtgewichtig
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
Dies ist der essentielle Blob-Generator mit optimierter Einfachheit:
- 🎯 **Optimierte Benutzeroberfläche**: Nur zwei intuitive Parameter für schnelle Blob-Erstellung
- 🌊 **Goldener Schnitt Integration**: Eingebaute PHI-Konstante (1.618) für natürlich ansprechende Proportionen  
- 🔄 **Koordinaten-Sortierung**: Automatische Orientierungs-Optimierung für konsistente Formgenerierung
- ⚡ **Hohe Performance**: Leichtgewichtige Implementation für Echtzeit-Rendering

### 🎛️ Parameter

#### 🔧 Kern-Form-Kontrollen
- 📏 **Size** (Float, anpassbar): Kontrolliert die Gesamtgröße des Blobs. Größere Werte erzeugen größere Blobs, kleinere Werte erzeugen kompaktere Formen
- 🌊 **Bumpiness** (Float, Bereich 0.0-1.0): Kontrolliert die Oberflächendetail-Intensität. Höhere Werte erzeugen ausgeprägtere Oberflächenvariationen und organische Textur

### ⚙️ Technische Implementation
Die Blob-Generierung funktioniert durch mehrere mathematische Stufen:
1. 🔄 **Positions-Skalierung**: Eingabekoordinaten werden durch den Kehrwert des Size-Parameters skaliert
2. 🪞 **Symmetrie-Anwendung**: Absolutwert-Operationen erzeugen symmetrische Grundstruktur
3. 📊 **Koordinaten-Sortierung**: Automatische Sortierung gewährleistet korrekte Orientierung unabhängig von der Eingabe
4. 📐 **Goldener Schnitt Berechnung**: Verwendet PHI-Konstante (1.618) für mathematisch ansprechende Proportionen
5. 🎯 **Skalarprodukt-Operationen**: Komplexe Berechnungen mit normalisierten Richtungsvektoren
6. 🌊 **Oberflächenmodulation**: Kosinus-basierte Oberflächendetail-Anwendung mit Bumpiness-Parameter
7. 📏 **Distance Field Generierung**: Finale Signed Distance Berechnung mit Größenskalierung

### 🎨 Kreative Anwendungen
- 🧬 **Organisches Modeling**: Zell-ähnliche Strukturen, Bakterien oder mikroskopische Organismen erstellen
- 🌊 **Meerestier-Design**: Quallen, Seeanemonen oder abstrakte Meereslebewesen generieren
- 🏗️ **Architektonische Elemente**: Für organische Gebäudekomponenten oder skulpturale Elemente verwenden
- 🎮 **Spiel-Assets**: Perfekt für Alien-Kreaturen, Fantasy-Elemente oder Umgebungsobjekte
- 🎨 **Abstrakte Kunst**: Grundlage für komplexe organische Kompositionen
- 🔬 **Wissenschaftliche Visualisierung**: Darstellung von Molekülstrukturen oder biologischen Formen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Size** um 1.0 für standard-große Blobs beginnen
- ✅ **Bumpiness**-Werte zwischen 0.3-0.8 für natürliche organische Textur verwenden
- ✅ **Bumpiness** auf 0.0 für glatte, minimale Blob-Oberflächen setzen
- ✅ **Bumpiness** auf 1.0 für maximale Oberflächendetails und Textur setzen
- ✅ Beide Parameter für dynamische Morphing-Effekte animieren
- ✅ Mehrere Blobs mit verschiedenen Größen für komplexe Kompositionen kombinieren

### 🎬 Animations-Möglichkeiten
**Bob the Blob** ist perfekt für Animation:

**Empfohlene Animations-Setups:**
1. 🕐 **Time Node** → **Sine Wave** (Min: 0.5, Max: 2.0, Period: 3.0) → **Size**
2. 🕐 **Time Node** → **Sine Wave** (Min: 0.2, Max: 0.8, Period: 5.0) → **Bumpiness**
3. 🔄 **Rotate Node** mit **Time Node** für drehende Blob-Effekte
4. 🌊 **3D-Wave Node** für organische Verformungs-Animationen

**Kreative Animations-Ideen:**
- **Atem-Effekt**: Size mit langsamer Sinuswelle animieren
- **Textur-Puls**: Bumpiness für Oberflächendetail-Änderungen animieren
- **Wachsender Organismus**: Lineare Vergrößerung der Size über Zeit
- **Morphender Blob**: Size- und Bumpiness-Animationen kombinieren

### 🆚 Vergleich mit Bob the Blob Pro
Diese optimierte Version fokussiert auf Einfachheit und Performance:
- ✅ **Schnelleres Rendering**: Weniger Berechnungen für Echtzeit-Performance
- ✅ **Einfacheres Setup**: Nur 2 Parameter vs 6 in der Pro-Version
- ✅ **Goldener Schnitt Eingebaut**: Automatische PHI-Integration (1.618)
- ❌ **Begrenzte Richtungskontrolle**: Keine benutzerdefinierten Richtungsvektoren
- ❌ **Feste Proportionen**: PHI-Parameter kann nicht manuell angepasst werden

**Wählen Sie Bob the Blob wenn Sie wollen:**
- Schnelle, einfache Blob-Generierung
- Maximale Performance
- Konsistente, zuverlässige Ergebnisse

**Wählen Sie Bob the Blob Pro wenn Sie benötigen:**
- Erweiterte Richtungskontrolle
- Benutzerdefinierte PHI-Anpassungen
- Komplexe asymmetrische Formen

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

**Built-in PHI**: 1.618033988749895 (Golden Ratio) 📐  
**Eingebautes PHI**: 1.618033988749895 (Goldener Schnitt) 📐

**Performance**: Optimized for real-time rendering ⚡  
**Performance**: Optimiert für Echtzeit-Rendering ⚡

**🔗 Links**

- VisualJockai-SP1 Original Inspiration
- COOLLAB Official Website
- Community Node Collection

Coollab-node contributed to the Coolab-Community Nodes collection - June 2025
