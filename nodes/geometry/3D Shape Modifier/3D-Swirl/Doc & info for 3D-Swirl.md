English | Deutsch
---

# 🌪️ 3D-Swirl Node Documentation

## 🇬🇧 English

### 📋 Overview
The **3D-Swirl** node creates sophisticated swirling and twisting effects for 3D shapes using signed distance field modifications. This node generates smooth rotational deformations around a customizable 3D axis with exponential distance falloff, creating natural-looking spiral and vortex effects. Based on video VFX techniques but implemented using SDF transformations with Rodrigues rotation mathematics for precise 3D shape manipulation.

📋 Files Included

    3D-Swirl.clbnode - The main COOLLAB node
    3D-Swirl.clbnode.presets.json - Basic preset configurations with 6 swirl variations

🚀 How to Use

Import the Node:

    Download both files from this directory (necessary files to make it run)
    Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
    as well as the associated preset .json file. 
You can place the two files in the category "3D Shape Modifier", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shape Modifiers: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\07 3D Shape Modifier

Connect Input:

    Connect any 3D shape or geometry as input to the 'Shape' parameter
    Works with primitive shapes, complex geometries, and other shape modifiers
    Perfect for creating organic twisting and flowing animations
    ⚠️ IMPORTANT: Requires additional animation nodes for dynamic effects

Animation Setup: Connect Time Node and/or Sine Wave Node to parameters. Some complex animations may require Input Vec3 Node to control individual axis components

⚙️ Technical Details

    Node Type: 3D Shape Modifier
    Input: vec3->SignedDistance (3D Shape)
    Output: Modified SignedDistance field
    Performance: Real-time capable
    SDF-based: GPU-accelerated distance field transformation using Rodrigues rotation

📜 License & Attribution

This COOLLAB Node:

    Created for COOLLAB by bennoH. & claude.ai (Sonnet-4 model)
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license
    Based on video VFX techniques adapted for SDF manipulation

### ✨ What Makes This Special
This is not a simple rotation effect. The 3D-Swirl node implements several advanced features:
- 🌪️ **Mathematical Precision**: Uses Rodrigues rotation formula for accurate 3D axis rotation
- 📐 **Exponential Falloff**: Distance-based strength decay creates natural-looking swirl patterns
- 🎯 **3D Axis Control**: Full control over rotation axis direction and position in 3D space
- 🔄 **Flexible Animation**: Designed to work with multiple animation node types for complex motion
- 🌊 **Organic Flow**: Creates smooth, continuous deformations that maintain shape integrity
- ⚙️ **Modular Design**: Basic presets allow custom animation setups rather than fixed behaviors

### 🎛️ Parameters

#### 🌪️ Swirl Core Controls
- 🔥 **Strength** (-20.0 to 20.0+, default: varies): Controls the intensity and direction of the swirl effect. Positive values create clockwise rotation, negative values create counter-clockwise rotation
- 🎯 **Center** (vec3, default: varies): 3D position of the swirl center point. Objects rotate around this position
- 📐 **Axis** (vec3, default: varies): Direction vector defining the rotation axis. The swirl rotates around this 3D axis

### ⚙️ Technical Implementation
The effect works through several sophisticated mathematical stages:
1. 🎯 **Position Calculation**: Calculate relative position from swirl center
2. 📐 **Axis Normalization**: Normalize the rotation axis vector for consistent behavior
3. 🔄 **Projection**: Project position onto rotation plane perpendicular to axis
4. 📏 **Distance Calculation**: Calculate distance from rotation axis for falloff
5. 🌪️ **Angle Computation**: Apply exponential falloff to create natural swirl strength
6. 🔄 **Rodrigues Rotation**: Apply mathematical rotation around arbitrary 3D axis
7. ✨ **SDF Sampling**: Sample original shape at transformed coordinates

### 🎨 Creative Applications
- 🌪️ **Tornado Effects**: Create realistic tornado and vortex simulations
- 🍥 **Organic Animation**: Generate flowing, liquid-like deformations
- 🎭 **Logo Animation**: Add sophisticated twisting motion to text and graphics
- 🌊 **Fluid Dynamics**: Simulate swirling fluid and gas movements
- 🎨 **Abstract Art**: Create complex sculptural forms with flowing geometry
- 🎬 **Transition Effects**: Smooth morphing between different states

### 💡 Tips for Best Results
- ✅ Start with **Strength** around 3-5 for moderate swirl effects
- ✅ Use **Time Node** connected to Strength for continuous spinning animation
- ✅ Connect **Sine Wave Node** to Strength for oscillating swirl effects
- ✅ Use **Input Vec3 Node** to animate Center or Axis components independently
- ✅ Experiment with **Axis** directions - diagonal axes create interesting tilted swirls
- ✅ Combine multiple 3D-Swirl nodes for complex multi-axis rotations
- ✅ Negative **Strength** values reverse rotation direction

### 🎨 Basic Preset Variations
The node includes 6 basic presets as starting points for custom animations:
- **Ruber**: Moderate strength swirl with diagonal axis orientation
- **Splisch**: High-intensity swirl with dynamic axis positioning  
- **Snailing**: Consistent high-strength swirl with balanced center/axis alignment
- **GumBuble**: High-strength swirl with offset center for bubble-like deformation
- **small s**: Medium strength swirl with precise positioning for subtle effects
- **Krumpl**: Reverse rotation (negative strength) for counter-clockwise motion effects

**⚠️ Important Animation Note**: These are basic static presets. For dynamic swirl animations, you must connect additional nodes:
- **Time Node**: For continuous rotation animation
- **Sine Wave Node**: For oscillating/pulsing swirl effects  
- **Input Vec3 Node**: For complex multi-axis or multi-parameter animations

### 🎬 Animation Workflow Options
**Option 1 - Continuous Spin:**
1. Connect **Time Node** to **Strength** parameter
2. Adjust Time Node speed for rotation velocity
3. Use preset as base configuration

**Option 2 - Oscillating Swirl:**
1. Connect **Sine Wave Node** to **Strength** parameter
2. Adjust frequency and amplitude for desired oscillation
3. Fine-tune **Center** and **Axis** positions

**Option 3 - Complex Multi-Axis Animation:**
1. Add **Input Vec3 Node** for **Center** or **Axis**
2. Connect different animation sources to X, Y, Z components
3. Combine **Time Node** on Strength with **Input Vec3** on position/axis

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025

---

## 🇩🇪 Deutsch

### 📋 Überblick
Der **3D-Swirl** Node erzeugt anspruchsvolle Wirbel- und Verdrehungseffekte für 3D-Formen mittels Signed Distance Field Modifikationen. Dieser Node generiert glatte Rotations-Deformationen um eine anpassbare 3D-Achse mit exponentieller Distanz-Abnahme, wodurch natürlich aussehende Spiral- und Vortex-Effekte entstehen. Basiert auf Video-VFX-Techniken, aber implementiert mittels SDF-Transformationen mit Rodrigues-Rotations-Mathematik für präzise 3D-Form-Manipulation.

📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)

    3D-Swirl.clbnode - Das Haupt-COOLLAB Node
    3D-Swirl.clbnode.presets.json - Basis-Preset-Konfigurationen mit 6 Wirbel-Variationen

🚀 Verwendung sprich Installationsanleitung

Node Importieren:

    Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
    Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
    wie auch die zugehörige Preset-Datei die .json Datei. 
Sie können die beiden Files in die Kategorie "3D Shape Modifier" respektive den entsprechenden Ordner hineinlegen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "3D Shape Modifiers" einzuordnen: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\07 3D Shape Modifier

Eingabe Verbinden:

    Beliebige 3D-Form oder Geometrie als Eingabe zum 'Shape' Parameter verbinden
    Funktioniert mit primitiven Formen, komplexen Geometrien und anderen Form-Modifikatoren
    Perfekt für organische Verdrehungs- und Fließ-Animationen
    ⚠️ WICHTIG: Benötigt zusätzliche Animations-Nodes für dynamische Effekte

Animations-Setup: Time Node und/oder Sine Wave Node an Parameter anschließen. Manche komplexe Animationen benötigen Input Vec3 Node um einzelne Achsen-Komponenten zu kontrollieren

⚙️ Technische Details

    Node-Typ: 3D Shape Modifier
    Eingabe: vec3->SignedDistance (3D Form)
    Ausgabe: Modifiziertes SignedDistance Feld
    Performance: Echtzeitfähig
    SDF-basiert: GPU-beschleunigte Distance-Field-Transformation mit Rodrigues-Rotation

📜 Lizenz & Attribution

Dieses COOLLAB Node:

    Für COOLLAB erstellt von bennoH. & claude.ai (Sonnet-4 Modell)
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz
    Basiert auf Video-VFX-Techniken adaptiert für SDF-Manipulation

### ✨ Was macht diesen Node besonders
Dies ist kein einfacher Rotations-Effekt. Der 3D-Swirl Node implementiert mehrere erweiterte Features:
- 🌪️ **Mathematische Präzision**: Verwendet Rodrigues-Rotations-Formel für genaue 3D-Achsen-Rotation
- 📐 **Exponentielle Abnahme**: Distanz-basierte Stärke-Abnahme erzeugt natürlich aussehende Wirbel-Muster
- 🎯 **3D-Achsen-Kontrolle**: Volle Kontrolle über Rotations-Achsen-Richtung und Position im 3D-Raum
- 🔄 **Flexible Animation**: Entwickelt um mit mehreren Animations-Node-Typen für komplexe Bewegung zu arbeiten
- 🌊 **Organischer Fluss**: Erzeugt glatte, kontinuierliche Deformationen die Form-Integrität bewahren
- ⚙️ **Modulares Design**: Basis-Presets erlauben benutzerdefinierte Animations-Setups anstatt fixer Verhaltensweisen

### 🎛️ Parameter

#### 🌪️ Wirbel-Kern-Kontrollen
- 🔥 **Strength** (-20.0 bis 20.0+, Standard: variiert): Kontrolliert die Intensität und Richtung des Wirbel-Effekts. Positive Werte erzeugen Uhrzeigersinn-Rotation, negative Werte erzeugen Gegen-Uhrzeigersinn-Rotation
- 🎯 **Center** (vec3, Standard: variiert): 3D-Position des Wirbel-Zentrums. Objekte rotieren um diese Position
- 📐 **Axis** (vec3, Standard: variiert): Richtungs-Vektor der die Rotations-Achse definiert. Der Wirbel rotiert um diese 3D-Achse

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere ausgeklügelte mathematische Stufen:
1. 🎯 **Positions-Berechnung**: Relative Position vom Wirbel-Zentrum berechnen
2. 📐 **Achsen-Normalisierung**: Rotations-Achsen-Vektor für konsistentes Verhalten normalisieren
3. 🔄 **Projektion**: Position auf Rotations-Ebene senkrecht zur Achse projizieren
4. 📏 **Distanz-Berechnung**: Distanz von Rotations-Achse für Abnahme berechnen
5. 🌪️ **Winkel-Berechnung**: Exponentielle Abnahme für natürliche Wirbel-Stärke anwenden
6. 🔄 **Rodrigues-Rotation**: Mathematische Rotation um beliebige 3D-Achse anwenden
7. ✨ **SDF-Sampling**: Original-Form an transformierten Koordinaten sampeln

### 🎨 Kreative Anwendungen
- 🌪️ **Tornado-Effekte**: Realistische Tornado- und Vortex-Simulationen erstellen
- 🍥 **Organische Animation**: Fließende, flüssigkeits-ähnliche Deformationen generieren
- 🎭 **Logo-Animation**: Anspruchsvolle Verdrehungs-Bewegung zu Text und Grafiken hinzufügen
- 🌊 **Fluid-Dynamik**: Wirbelnde Flüssigkeits- und Gas-Bewegungen simulieren
- 🎨 **Abstrakte Kunst**: Komplexe skulpturale Formen mit fließender Geometrie erstellen
- 🎬 **Übergangs-Effekte**: Glatte Morphing zwischen verschiedenen Zuständen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Strength** um 3-5 für moderate Wirbel-Effekte beginnen
- ✅ **Time Node** an Strength anschließen für kontinuierliche Spin-Animation
- ✅ **Sine Wave Node** an Strength anschließen für oszillierende Wirbel-Effekte
- ✅ **Input Vec3 Node** verwenden um Center- oder Axis-Komponenten unabhängig zu animieren
- ✅ Mit **Axis**-Richtungen experimentieren - diagonale Achsen erzeugen interessante geneigte Wirbel
- ✅ Mehrere 3D-Swirl Nodes für komplexe Multi-Achsen-Rotationen kombinieren
- ✅ Negative **Strength**-Werte kehren Rotations-Richtung um

### 🎨 Basis-Preset-Variationen
Der Node enthält 6 Basis-Presets als Ausgangspunkte für benutzerdefinierte Animationen:
- **Ruber**: Moderate Stärke Wirbel mit diagonaler Achsen-Orientierung
- **Splisch**: Hoch-Intensitäts-Wirbel mit dynamischer Achsen-Positionierung
- **Snailing**: Konsistenter hoch-Stärke-Wirbel mit ausgewogener Center/Axis-Ausrichtung
- **GumBuble**: Hoch-Stärke-Wirbel mit versetztem Center für blasen-ähnliche Deformation
- **small s**: Mittlere Stärke Wirbel mit präziser Positionierung für subtile Effekte
- **Krumpl**: Rückwärts-Rotation (negative Stärke) für Gegen-Uhrzeigersinn-Bewegungs-Effekte

**⚠️ Wichtiger Animations-Hinweis**: Dies sind statische Basis-Presets. Für dynamische Wirbel-Animationen müssen Sie zusätzliche Nodes anschließen:
- **Time Node**: Für kontinuierliche Rotations-Animation
- **Sine Wave Node**: Für oszillierende/pulsierende Wirbel-Effekte
- **Input Vec3 Node**: Für komplexe Multi-Achsen- oder Multi-Parameter-Animationen

### 🎬 Animations-Workflow-Optionen
**Option 1 - Kontinuierlicher Spin:**
1. **Time Node** an **Strength**-Parameter anschließen
2. Time Node Geschwindigkeit für Rotations-Geschwindigkeit anpassen
3. Preset als Basis-Konfiguration verwenden

**Option 2 - Oszillierender Wirbel:**
1. **Sine Wave Node** an **Strength**-Parameter anschließen
2. Frequenz und Amplitude für gewünschte Oszillation anpassen
3. **Center** und **Axis** Positionen feinabstimmen

**Option 3 - Komplexe Multi-Achsen-Animation:**
1. **Input Vec3 Node** für **Center** oder **Axis** hinzufügen
2. Verschiedene Animations-Quellen an X, Y, Z Komponenten anschließen
3. **Time Node** auf Strength mit **Input Vec3** auf Position/Achse kombinieren

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Video VFX techniques with Rodrigues rotation mathematics 🎬  
**Basiert auf**: Video-VFX-Techniken mit Rodrigues-Rotations-Mathematik 🎬

**Category**: 3D Shape Modifier > Deformation 🌪️  
**Kategorie**: 3D Shape Modifier > Deformation 🌪️

**Input**: vec3->SignedDistance (3D Shape) 🎯  
**Eingabe**: vec3->SignedDistance (3D Form) 🎯

**Output**: SignedDistance ✨  
**Ausgabe**: SignedDistance ✨

**Animation Requirements**: Time Node, Sine Wave Node, Input Vec3 Node 🔄  
**Animations-Anforderungen**: Time Node, Sine Wave Node, Input Vec3 Node 🔄

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025
