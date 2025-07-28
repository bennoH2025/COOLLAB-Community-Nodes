English | Deutsch
---

# 🌊 3D-Wave Node Documentation

## 🇬🇧 English

### 📋 Overview
The **3D-Wave** node creates sophisticated wave-based deformations for 3D shapes using signed distance field modifications. This node generates smooth sinusoidal wave patterns that travel along a customizable 3D direction vector, creating organic flowing motions perfect for simulating water, fabric, energy fields, and other wave-like phenomena. Based on video VFX techniques but implemented using SDF transformations for precise real-time 3D shape manipulation.

📋 Files Included

    3D-Wave.clbnode - The main COOLLAB node
    3D-Wave.clbnode.presets.json - Preset configurations with 6 wave variations

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
    Perfect for creating flowing, organic wave animations
    ⚠️ IMPORTANT: Connect Time Node to Phase parameter for wave animation

Animation Setup: Connect Time Node to Phase parameter with speeds specified in preset names for optimal wave motion

⚙️ Technical Details

    Node Type: 3D Shape Modifier
    Input: vec3->SignedDistance (3D Shape)
    Output: Modified SignedDistance field
    Performance: Real-time capable
    SDF-based: GPU-accelerated distance field transformation with sinusoidal wave mathematics

📜 License & Attribution

This COOLLAB Node:

    Created for COOLLAB by bennoH. & claude.ai (Sonnet-4 model)
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license
    Based on video VFX techniques adapted for SDF manipulation

### ✨ What Makes This Special
This is not a simple displacement effect. The 3D-Wave node implements several advanced features:
- 🌊 **Directional Wave Propagation**: Waves travel along customizable 3D direction vectors
- 📐 **Perpendicular Displacement**: Smart perpendicular calculation ensures natural wave motion
- 🎯 **Phase Control**: Precise phase parameter enables smooth wave animation and timing
- 🔄 **Mathematical Precision**: Uses normalized direction vectors and cross products for accurate geometry
- 🌊 **Organic Flow**: Creates smooth, continuous deformations that maintain shape integrity
- ⚡ **Real-time Performance**: Optimized SDF implementation for fluid interactive animation

### 🎛️ Parameters

#### 🌊 Wave Core Controls
- 📏 **Amplitude** (0.0-2.0+, default: varies): Controls the height/strength of the wave displacement. Higher values create more dramatic wave effects
- 🔄 **Frequency** (0.1-10.0+, default: varies): Controls the number of wave cycles along the direction. Higher values create more frequent waves
- 📐 **Direction** (vec3, default: varies): 3D vector defining the direction of wave propagation. Waves travel along this axis
- ⏱️ **Phase** (0.0-6.28+, default: varies): Controls the wave timing/offset. Animate this parameter to create traveling wave motion

### ⚙️ Technical Implementation
The effect works through several sophisticated mathematical stages:
1. 📐 **Direction Normalization**: Normalize the direction vector for consistent wave propagation
2. 🎯 **Wave Position Calculation**: Calculate position along wave direction using dot product
3. 🔄 **Perpendicular Vector**: Compute perpendicular displacement direction using cross product
4. 🌊 **Sinusoidal Displacement**: Apply sine wave with frequency, phase, and amplitude
5. 📏 **Position Transform**: Displace original position perpendicular to wave direction
6. ✨ **SDF Sampling**: Sample original shape at transformed coordinates

### 🎨 Creative Applications
- 🌊 **Water Simulation**: Create realistic water surface and fluid motion effects
- 🏃 **Cloth Animation**: Simulate fabric, flags, and flexible material movement
- ⚡ **Energy Fields**: Generate energy waves, force fields, and magical effects
- 🎵 **Audio Visualization**: Create wave patterns that respond to music and sound
- 🌬️ **Wind Effects**: Simulate objects moving in wind or air currents
- 🎬 **Organic Animation**: Add life-like movement to static objects

### 💡 Tips for Best Results
- ✅ Start with **Amplitude** around 0.2-0.5 for subtle wave effects
- ✅ Connect **Time Node** to **Phase** parameter for traveling wave animation
- ✅ Use **Direction** vectors like (1,0,0), (0,1,0), or (0,0,1) for clean axis-aligned waves
- ✅ **Frequency** between 2-5 creates natural-looking wave patterns
- ✅ Animate **Amplitude** with Sine Wave Node for breathing/pulsing effects
- ✅ Combine multiple 3D-Wave nodes with different directions for complex wave interactions
- ✅ Use diagonal **Direction** vectors for interesting angular wave propagation

### 🎨 Preset Variations with Time Settings
The node includes 6 carefully crafted presets with specific Time Node speed requirements:

- **soft SwoBle (Time 1.0 at Phase)**: Gentle wave with moderate frequency. Requires Time Node speed 1.0 on Phase parameter
- **mid fish-Blob'l (Time 1.8 at Phase)**: Medium intensity wave perfect for organic blob animations. Requires Time Node speed 1.8 on Phase parameter  
- **full Blob'l (Time 1.7 at Phase)**: Full-strength wave with complex direction vector. Requires Time Node speed 1.7 on Phase parameter
- **Bublegum particle-beaming (Time 1.7 at Phase)**: High amplitude wave for dramatic particle-like effects. Requires Time Node speed 1.7 on Phase parameter
- **S-Curve roller (Time 4.0 at Phase)**: Fast rolling wave with extreme direction vector. Requires Time Node speed 4.0 on Phase parameter
- **for BlobPro (Time on Phase 0.5)**: Subtle wave optimized for blob shapes. Requires Time Node speed 0.5 on Phase parameter

**⚠️ Important Setup Note**: All presets require a **Time Node** connected to the **Phase** parameter. The Time Node must be configured with the specific speed setting indicated in parentheses for each preset. Without this setup, the wave animation will not work properly.

### 🎬 Animation Workflow
1. **Setup**: Connect your 3D shape and select desired preset
2. **Time Connection**: Connect a **Time Node** to the **Phase** parameter (essential for wave motion)
3. **Speed Configuration**: Set the Time Node speed according to preset specifications (e.g., 1.0, 1.8, 4.0, etc.)
4. **Direction Tuning**: Adjust **Direction** vector for desired wave propagation angle
5. **Wave Intensity**: Fine-tune **Amplitude** and **Frequency** for perfect wave characteristics
6. **Advanced Animation**: Optionally animate other parameters with Sine Wave Nodes for complex effects

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025

---

## 🇩🇪 Deutsch

### 📋 Überblick
Der **3D-Wave** Node erzeugt anspruchsvolle wellen-basierte Deformationen für 3D-Formen mittels Signed Distance Field Modifikationen. Dieser Node generiert glatte sinusoidale Wellenmuster die entlang eines anpassbaren 3D-Richtungsvektors wandern, wodurch organische fließende Bewegungen entstehen, perfekt für die Simulation von Wasser, Stoff, Energiefeldern und anderen wellen-ähnlichen Phänomenen. Basiert auf Video-VFX-Techniken, aber implementiert mittels SDF-Transformationen für präzise Echtzeit-3D-Form-Manipulation.

📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)

    3D-Wave.clbnode - Das Haupt-COOLLAB Node
    3D-Wave.clbnode.presets.json - Preset-Konfigurationen mit 6 Wellen-Variationen

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
    Perfekt für fließende, organische Wellen-Animationen
    ⚠️ WICHTIG: Time Node an Phase-Parameter anschließen für Wellen-Animation

Animations-Setup: Time Node an Phase-Parameter anschließen mit Geschwindigkeiten wie in Preset-Namen spezifiziert für optimale Wellen-Bewegung

⚙️ Technische Details

    Node-Typ: 3D Shape Modifier
    Eingabe: vec3->SignedDistance (3D Form)
    Ausgabe: Modifiziertes SignedDistance Feld
    Performance: Echtzeitfähig
    SDF-basiert: GPU-beschleunigte Distance-Field-Transformation mit sinusoidaler Wellen-Mathematik

📜 Lizenz & Attribution

Dieses COOLLAB Node:

    Für COOLLAB erstellt von bennoH. & claude.ai (Sonnet-4 Modell)
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz
    Basiert auf Video-VFX-Techniken adaptiert für SDF-Manipulation

### ✨ Was macht diesen Node besonders
Dies ist kein einfacher Displacement-Effekt. Der 3D-Wave Node implementiert mehrere erweiterte Features:
- 🌊 **Direktionale Wellen-Ausbreitung**: Wellen wandern entlang anpassbarer 3D-Richtungsvektoren
- 📐 **Senkrechte Verlagerung**: Intelligente senkrechte Berechnung gewährleistet natürliche Wellen-Bewegung
- 🎯 **Phasen-Kontrolle**: Präziser Phasen-Parameter ermöglicht glatte Wellen-Animation und Timing
- 🔄 **Mathematische Präzision**: Verwendet normalisierte Richtungsvektoren und Kreuzprodukte für genaue Geometrie
- 🌊 **Organischer Fluss**: Erzeugt glatte, kontinuierliche Deformationen die Form-Integrität bewahren
- ⚡ **Echtzeit-Performance**: Optimierte SDF-Implementation für flüssige interaktive Animation

### 🎛️ Parameter

#### 🌊 Wellen-Kern-Kontrollen
- 📏 **Amplitude** (0.0-2.0+, Standard: variiert): Kontrolliert die Höhe/Stärke der Wellen-Verlagerung. Höhere Werte erzeugen dramatischere Wellen-Effekte
- 🔄 **Frequency** (0.1-10.0+, Standard: variiert): Kontrolliert die Anzahl der Wellen-Zyklen entlang der Richtung. Höhere Werte erzeugen häufigere Wellen
- 📐 **Direction** (vec3, Standard: variiert): 3D-Vektor der die Richtung der Wellen-Ausbreitung definiert. Wellen wandern entlang dieser Achse
- ⏱️ **Phase** (0.0-6.28+, Standard: variiert): Kontrolliert das Wellen-Timing/Offset. Diesen Parameter animieren um wandernde Wellen-Bewegung zu erzeugen

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere ausgeklügelte mathematische Stufen:
1. 📐 **Richtungs-Normalisierung**: Richtungsvektor für konsistente Wellen-Ausbreitung normalisieren
2. 🎯 **Wellen-Positions-Berechnung**: Position entlang Wellen-Richtung mit Skalarprodukt berechnen
3. 🔄 **Senkrechter Vektor**: Senkrechte Verlagerungs-Richtung mit Kreuzprodukt berechnen
4. 🌊 **Sinusoidale Verlagerung**: Sinuswelle mit Frequenz, Phase und Amplitude anwenden
5. 📏 **Positions-Transformation**: Original-Position senkrecht zur Wellen-Richtung verlagern
6. ✨ **SDF-Sampling**: Original-Form an transformierten Koordinaten sampeln

### 🎨 Kreative Anwendungen
- 🌊 **Wasser-Simulation**: Realistische Wasseroberflächen- und Flüssigkeits-Bewegungseffekte erstellen
- 🏃 **Stoff-Animation**: Stoff, Flaggen und flexible Material-Bewegungen simulieren
- ⚡ **Energiefelder**: Energiewellen, Kraftfelder und magische Effekte generieren
- 🎵 **Audio-Visualisierung**: Wellenmuster erstellen die auf Musik und Klang reagieren
- 🌬️ **Wind-Effekte**: Objekte simulieren die sich in Wind oder Luftströmungen bewegen
- 🎬 **Organische Animation**: Lebensähnliche Bewegung zu statischen Objekten hinzufügen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Amplitude** um 0.2-0.5 für subtile Wellen-Effekte beginnen
- ✅ **Time Node** an **Phase**-Parameter anschließen für wandernde Wellen-Animation
- ✅ **Direction**-Vektoren wie (1,0,0), (0,1,0) oder (0,0,1) für saubere achsen-ausgerichtete Wellen verwenden
- ✅ **Frequency** zwischen 2-5 erzeugt natürlich aussehende Wellen-Muster
- ✅ **Amplitude** mit Sine Wave Node für Atem-/Pulseffekte animieren
- ✅ Mehrere 3D-Wave Nodes mit verschiedenen Richtungen für komplexe Wellen-Interaktionen kombinieren
- ✅ Diagonale **Direction**-Vektoren für interessante winklige Wellen-Ausbreitung verwenden

### 🎨 Preset-Variationen mit Zeit-Einstellungen
Der Node enthält 6 sorgfältig gestaltete Presets mit spezifischen Time Node Geschwindigkeits-Anforderungen:

- **soft SwoBle (Time 1.0 at Phase)**: Sanfte Welle mit moderater Frequenz. Benötigt Time Node Geschwindigkeit 1.0 am Phase-Parameter
- **mid fish-Blob'l (Time 1.8 at Phase)**: Mittlere Intensitäts-Welle perfekt für organische Blob-Animationen. Benötigt Time Node Geschwindigkeit 1.8 am Phase-Parameter
- **full Blob'l (Time 1.7 at Phase)**: Vollstärke-Welle mit komplexem Richtungsvektor. Benötigt Time Node Geschwindigkeit 1.7 am Phase-Parameter  
- **Bublegum particle-beaming (Time 1.7 at Phase)**: Hohe Amplitude Welle für dramatische partikel-ähnliche Effekte. Benötigt Time Node Geschwindigkeit 1.7 am Phase-Parameter
- **S-Curve roller (Time 4.0 at Phase)**: Schnelle rollende Welle mit extremem Richtungsvektor. Benötigt Time Node Geschwindigkeit 4.0 am Phase-Parameter
- **for BlobPro (Time on Phase 0.5)**: Subtile Welle optimiert für Blob-Formen. Benötigt Time Node Geschwindigkeit 0.5 am Phase-Parameter

**⚠️ Wichtiger Setup-Hinweis**: Alle Presets benötigen einen **Time Node** der mit dem **Phase**-Parameter verbunden ist. Der Time Node muss mit der spezifischen Geschwindigkeits-Einstellung konfiguriert werden, die in Klammern für jedes Preset angegeben ist. Ohne dieses Setup funktioniert die Wellen-Animation nicht ordnungsgemäß.

### 🎬 Animations-Workflow
1. **Setup**: 3D-Form verbinden und gewünschtes Preset wählen
2. **Zeit-Verbindung**: **Time Node** an **Phase**-Parameter anschließen (essentiell für Wellen-Bewegung)
3. **Geschwindigkeits-Konfiguration**: Time Node Geschwindigkeit entsprechend Preset-Spezifikationen setzen (z.B. 1.0, 1.8, 4.0, etc.)
4. **Richtungs-Abstimmung**: **Direction**-Vektor für gewünschten Wellen-Ausbreitungswinkel anpassen
5. **Wellen-Intensität**: **Amplitude** und **Frequency** für perfekte Wellen-Eigenschaften feinabstimmen
6. **Erweiterte Animation**: Optional andere Parameter mit Sine Wave Nodes für komplexe Effekte animieren

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Video VFX techniques with sinusoidal wave mathematics 🎬  
**Basiert auf**: Video-VFX-Techniken mit sinusoidaler Wellen-Mathematik 🎬

**Category**: 3D Shape Modifier > Deformation 🌊  
**Kategorie**: 3D Shape Modifier > Deformation 🌊

**Input**: vec3->SignedDistance (3D Shape) 🎯  
**Eingabe**: vec3->SignedDistance (3D Form) 🎯

**Output**: SignedDistance ✨  
**Ausgabe**: SignedDistance ✨

**Animation Requirements**: Time Node (essential for Phase parameter) ⏱️  
**Animations-Anforderungen**: Time Node (essentiell für Phase-Parameter) ⏱️

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025
