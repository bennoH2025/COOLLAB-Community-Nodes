English | Deutsch
---

# 💥 3D-Explode Node Documentation

## 🇬🇧 English

### 📋 Overview
The **3D-Explode** node creates dramatic explosion effects for 3D shapes using signed distance field modifications. This node simulates the visual effect of objects exploding outward from a central point, with customizable strength, timing, and noise patterns for realistic, irregular explosion dynamics. Based on video VFX techniques but implemented using SDF transformations for real-time 3D shape manipulation.

📋 Files Included

    3D-Explode.clbnode - The main COOLLAB node
    3D-Explode.clbnode.presets.json - Preset configurations with 4 explosion variations

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
    Perfect for creating dramatic destruction and explosion sequences
    ⚠️ IMPORTANT: Connect a Time Node to the 'Time' parameter for animation

Animate Parameters: Connect Time Node (not manual keyframes) with appropriate speed settings for realistic explosion timing

⚙️ Technical Details

    Node Type: 3D Shape Modifier
    Input: vec3->SignedDistance (3D Shape)
    Output: Modified SignedDistance field
    Performance: Real-time capable
    SDF-based: GPU-accelerated distance field transformation

📜 License & Attribution

This COOLLAB Node:

    Created for COOLLAB by bennoH. & claude.ai (Sonnet-4 model)
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license
    Based on video VFX techniques adapted for SDF manipulation

### ✨ What Makes This Special
This is not a simple displacement effect. The 3D-Explode node implements several advanced features:
- 💥 **Radial Explosion Physics**: Realistic outward displacement from configurable center point
- 🎯 **Precision Control**: Adjustable explosion center in full 3D space
- ⏱️ **Time-Based Animation**: Smooth temporal progression for realistic explosion timing
- 🌊 **Organic Noise Integration**: 3D noise patterns create irregular, natural-looking fragmentation
- 🔄 **SDF Preservation**: Maintains proper distance field properties throughout transformation
- ⚡ **Trigger Node Behavior**: This is a specialized trigger effect - once the explosion completes, the screen becomes empty. Perfect for dramatic one-time destruction sequences rather than continuous effects

### 🎛️ Parameters

#### 💥 Explosion Core Controls
- 🔥 **Strength** (0.0+, default: varies): Controls the intensity of the explosion effect. Higher values create more dramatic displacement
- 🎯 **Center** (vec3, default: varies): 3D position of the explosion epicenter. Objects explode outward from this point
- ⏱️ **Time** (0.0+, default: varies): Animation time parameter. Controls explosion progression over time

#### 🌊 Variation Controls  
- 🎲 **Noise Scale** (-10.0 to 10.0+, default: varies): Controls the scale of noise patterns that add irregularity to the explosion. Positive values create fine detail, negative values create broader variations

### ⚙️ Technical Implementation
The effect works through several sophisticated stages:
1. 🎯 **Center Calculation**: Calculate relative position from explosion center
2. 📐 **Direction Vector**: Compute normalized direction for radial displacement
3. 🌊 **Noise Generation**: Apply 3D sinusoidal noise for organic variation
4. 💥 **Displacement Calculation**: Combine strength, time, and noise for final displacement
5. 🔄 **SDF Sampling**: Sample original shape at displaced coordinates
6. ✨ **Field Reconstruction**: Maintain proper distance field properties

### 🎨 Creative Applications
- 💥 **Destruction Sequences**: Create realistic object destruction and fragmentation
- 🎬 **Motion Graphics**: Add dramatic explosion effects to logos and text
- 🚀 **Sci-Fi Effects**: Generate energy bursts and force field disruptions
- 🎮 **Game VFX**: Real-time explosion effects for interactive applications
- 🎭 **Abstract Art**: Create dynamic, evolving sculptural forms

### 💡 Tips for Best Results
- ✅ Start with **Strength** around 1.0-2.0 for subtle effects
- ✅ Always connect a **Time Node** to the Time parameter - manual animation won't work properly
- ✅ Set Time Node speed to **3.0** for optimal results with presets
- ✅ Use **Center** positioning to control explosion direction and focus
- ✅ Remember this is a **trigger effect** - objects disappear after explosion
- ✅ Experiment with **Noise Scale** - negative values often create interesting large-scale variations
- ✅ Plan your composition knowing the screen will be empty after the explosion sequence

### 🎨 Preset Variations
The node includes 4 carefully crafted presets:
- **Splash out right down (Time x 3.0)**: Directional explosion with moderate strength and fine noise details. Requires Time Node connected with speed setting 3.0
- **Explod DRASTIC (Time x 3.0)**: Maximum intensity explosion with high noise variation for chaotic effects. Requires Time Node connected with speed setting 3.0
- **Explode FLASHY (Time x 3.0)**: Balanced explosion with high-frequency noise for detailed fragmentation. Requires Time Node connected with speed setting 3.0
- **Explod STEROIDE-SLOPY (Time x 3.0)**: Controlled explosion with medium noise for organic, flowing displacement. Requires Time Node connected with speed setting 3.0

**⚠️ Important Setup Note**: All presets require a separate **Time Node** to be connected to the **Time** parameter. The Time Node must be configured with a **speed setting of 3.0** as indicated in the preset names. Without this setup, the explosion animation will not work properly.

### 🎬 Animation Workflow
1. **Setup**: Connect your 3D shape and set explosion **Center**
2. **Time Connection**: Connect a **Time Node** to the **Time** parameter (essential for animation)
3. **Time Node Configuration**: Set the Time Node speed to **3.0** (as indicated in presets)
4. **Intensity**: Adjust **Strength** for desired explosion power
5. **Variation**: Fine-tune **Noise Scale** for organic randomness
6. **Trigger Usage**: Remember this is a trigger effect - plan for screen to be empty after explosion completes

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025

---

## 🇩🇪 Deutsch

### 📋 Überblick
Der **3D-Explode** Node erzeugt dramatische Explosions-Effekte für 3D-Formen mittels Signed Distance Field Modifikationen. Dieser Node simuliert die visuelle Wirkung von Objekten, die von einem zentralen Punkt nach außen explodieren, mit anpassbarer Stärke, Timing und Noise-Mustern für realistische, unregelmäßige Explosions-Dynamik. Basiert auf Video-VFX-Techniken, aber implementiert mittels SDF-Transformationen für Echtzeit-3D-Form-Manipulation.

📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)

    3D-Explode.clbnode - Das Haupt-COOLLAB Node
    3D-Explode.clbnode.presets.json - Preset-Konfigurationen mit 4 Explosions-Variationen

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
    Perfekt für dramatische Zerstörungs- und Explosions-Sequenzen

Parameter Animieren: Time-Parameter mit Keyframes verwenden oder an Zeitquelle für Animation anschließen

⚙️ Technische Details

    Node-Typ: 3D Shape Modifier
    Eingabe: vec3->SignedDistance (3D Form)
    Ausgabe: Modifiziertes SignedDistance Feld
    Performance: Echtzeitfähig
    SDF-basiert: GPU-beschleunigte Distance-Field-Transformation

📜 Lizenz & Attribution

Dieses COOLLAB Node:

    Für COOLLAB erstellt von bennoH. & claude.ai (Sonnet-4 Modell)
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz
    Basiert auf Video-VFX-Techniken adaptiert für SDF-Manipulation

### ✨ Was macht diesen Node besonders
Dies ist kein einfacher Displacement-Effekt. Der 3D-Explode Node implementiert mehrere erweiterte Features:
- 💥 **Radiale Explosions-Physik**: Realistische Außen-Verlagerung von konfigurierbarem Zentrum
- 🎯 **Präzisions-Kontrolle**: Anpassbares Explosions-Zentrum im vollen 3D-Raum
- ⏱️ **Zeit-basierte Animation**: Glatte zeitliche Progression für realistische Explosions-Timing
- 🌊 **Organische Noise-Integration**: 3D-Noise-Muster erzeugen unregelmäßige, natürlich aussehende Fragmentierung
- 🔄 **SDF-Erhaltung**: Erhält ordnungsgemäße Distance-Field-Eigenschaften während der Transformation
- ⚡ **Trigger-Node-Verhalten**: Dies ist ein spezialisierter Trigger-Effekt - sobald die Explosion abgeschlossen ist, wird der Bildschirm leer. Perfekt für dramatische einmalige Zerstörungs-Sequenzen anstatt kontinuierliche Effekte

### 🎛️ Parameter

#### 💥 Explosions-Kern-Kontrollen
- 🔥 **Strength** (0.0+, Standard: variiert): Kontrolliert die Intensität des Explosions-Effekts. Höhere Werte erzeugen dramatischere Verlagerung
- 🎯 **Center** (vec3, Standard: variiert): 3D-Position des Explosions-Epizentrums. Objekte explodieren von diesem Punkt nach außen
- ⏱️ **Time** (0.0+, Standard: variiert): Animations-Zeit-Parameter. Kontrolliert Explosions-Progression über die Zeit

#### 🌊 Variations-Kontrollen
- 🎲 **Noise Scale** (-10.0 bis 10.0+, Standard: variiert): Kontrolliert die Skalierung von Noise-Mustern die Unregelmäßigkeit zur Explosion hinzufügen. Positive Werte erzeugen feine Details, negative Werte erzeugen breitere Variationen

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere ausgeklügelte Stufen:
1. 🎯 **Zentrum-Berechnung**: Relative Position vom Explosions-Zentrum berechnen
2. 📐 **Richtungs-Vektor**: Normalisierte Richtung für radiale Verlagerung berechnen
3. 🌊 **Noise-Generierung**: 3D-sinusoidales Noise für organische Variation anwenden
4. 💥 **Verlagerungs-Berechnung**: Stärke, Zeit und Noise für finale Verlagerung kombinieren
5. 🔄 **SDF-Sampling**: Original-Form an verlagerten Koordinaten sampeln
6. ✨ **Feld-Rekonstruktion**: Ordnungsgemäße Distance-Field-Eigenschaften beibehalten

### 🎨 Kreative Anwendungen
- 💥 **Zerstörungs-Sequenzen**: Realistische Objekt-Zerstörung und Fragmentierung erstellen
- 🎬 **Motion Graphics**: Dramatische Explosions-Effekte zu Logos und Text hinzufügen
- 🚀 **Sci-Fi-Effekte**: Energie-Ausbrüche und Kraftfeld-Störungen generieren
- 🎮 **Game-VFX**: Echtzeit-Explosions-Effekte für interaktive Anwendungen
- 🎭 **Abstrakte Kunst**: Dynamische, sich entwickelnde skulpturale Formen erstellen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Strength** um 1.0-2.0 für subtile Effekte beginnen
- ✅ **Time** von 0 animieren um Explosions-Progression zu erstellen
- ✅ **Center**-Positionierung verwenden um Explosions-Richtung und Fokus zu kontrollieren
- ✅ Mit **Noise Scale** experimentieren - negative Werte erzeugen oft interessante großflächige Variationen
- ✅ Mit anderen Modifikatoren für komplexe Zerstörungs-Sequenzen kombinieren

### 🎨 Preset-Variationen
Der Node enthält 4 sorgfältig gestaltete Presets:
- **Splash out right down (Time x 3.0)**: Richtungs-Explosion mit moderater Stärke und feinen Noise-Details. Benötigt Time Node mit Geschwindigkeits-Einstellung 3.0
- **Explod DRASTIC (Time x 3.0)**: Maximum-Intensitäts-Explosion mit hoher Noise-Variation für chaotische Effekte. Benötigt Time Node mit Geschwindigkeits-Einstellung 3.0
- **Explode FLASHY (Time x 3.0)**: Ausgewogene Explosion mit hochfrequentem Noise für detaillierte Fragmentierung. Benötigt Time Node mit Geschwindigkeits-Einstellung 3.0
- **Explod STEROIDE-SLOPY (Time x 3.0)**: Kontrollierte Explosion mit mittlerem Noise für organische, fließende Verlagerung. Benötigt Time Node mit Geschwindigkeits-Einstellung 3.0

**⚠️ Wichtiger Setup-Hinweis**: Alle Presets benötigen einen separaten **Time Node**, der mit dem **Time**-Parameter verbunden werden muss. Der Time Node muss mit einer **Geschwindigkeits-Einstellung von 3.0** konfiguriert werden, wie in den Preset-Namen angegeben. Ohne dieses Setup funktioniert die Explosions-Animation nicht ordnungsgemäß.

### 🎬 Animations-Workflow
1. **Setup**: 3D-Form verbinden und Explosions-**Center** setzen
2. **Timing**: Keyframes für **Time**-Parameter erstellen (0 → gewünschter Endwert)
3. **Intensität**: **Strength** für gewünschte Explosions-Kraft anpassen
4. **Variation**: **Noise Scale** für organische Zufälligkeit feinabstimmen
5. **Verfeinerung**: Vorschau und Parameter für perfektes Timing anpassen

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Video VFX techniques adapted for SDF 🎬  
**Basiert auf**: Video-VFX-Techniken adaptiert für SDF 🎬

**Category**: 3D Shape Modifier > Deformation 💥  
**Kategorie**: 3D Shape Modifier > Deformation 💥

**Input**: vec3->SignedDistance (3D Shape) 🎯  
**Eingabe**: vec3->SignedDistance (3D Form) 🎯

**Output**: SignedDistance ✨  
**Ausgabe**: SignedDistance ✨

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025
