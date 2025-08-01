English | Deutsch
---

# 🔸 Kaleidoscope Tiles Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Kaleidoscope Tiles** node creates a sophisticated kaleidoscope effect that combines traditional kaleidoscope mirroring with advanced tiling capabilities. Unlike a simple kaleidoscope, this effect creates repeating tile patterns with individual sliding animations and complex geometric transformations.
& It creates stunning symmetrical, mirrored patterns from any input image or imagelike 2Dsurces. This effect transforms ordinary images or imagelike 2Dsurce into mesmerizing kaleidoscope-like visuals with repeating geometric patterns.


📋 Files Included

    Kaleidoscope Tiles.clbnode - The main COOLLAB node
    Kaleidoscope Tiles - Default.json - Default preset configuration

🚀 How to Use

Import the Node:

    Download both files from this directory (necessary files to make it run)
    Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the moast actual Collab-Version you find in that
    as well as the associated default .json file. 
You can place the two files in the categorie "Image Modifier", means in that named folders in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the Image Modifiers: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\11 Image Modifier (Post Process)

Connect Input:

    Connect any image or a 2D-source, video, or generator as input
    The effect works best with images ansd sources that have interesting details

Adjust Parameters: see the paremeterlist


⚙️ Technical Details

    Node Type: Effect
    Input: Single image/texture input
    Output: Processed image with kaleidoscope effect
    Performance: Real-time capable
    Shader-based: GPU-accelerated processing

📜 License & Attribution

Original Source:

    Based on ISF shader from VIDVOX/ISF-Files
    Original shader licensed under MIT License
    Original authors: VIDVOX team

This COOLLAB Node:

    Adapted for COOLLAB by bennoH. & claude.ai
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license



### ✨ What Makes This Special
This is not a standard kaleidoscope effect. The "Tiles" component adds several unique features:
- 🔲 **Tiling System**: The image is divided into repeating tiles that can be manipulated independently
- 🎭 **Slide Effects**: Two separate slide parameters allow different parts of the tiles to move independently
- ⚙️ **Advanced Pattern Generation**: Combines rotation, scaling, shifting, and kaleidoscope mirroring in a sophisticated pipeline



### 🎛️ Parameters

#### 🔧 Core Transform Controls
- 📏 **Size** (0.0 - 2.0, default: 0.5): Controls the scale of the tile pattern. Smaller values create larger tiles, larger values create smaller, more detailed tiles
- 🔄 **Rotation** (0.0 - 1.0, default: 0.125): Rotates the entire pattern before tiling operations
- 📐 **Shift** (Point2D, default: [0,0]): Translates the pattern in 2D space before tiling

#### 🪞 Kaleidoscope Controls
- 🔺 **Sides** (1 - 32, default: 6): Number of kaleidoscope segments. Creates the characteristic mirrored sections
- 🎯 **Angle** (0.0 - 1.0, default: 0.0): Rotates the kaleidoscope effect within each segment

#### 🎬 Tile Animation Controls
- ➡️ **Slide 1** (Point2D, default: [0,0]): Controls sliding animation for the first set of tiles (when point.x < 0.5 or point.y < 0.5)
- ⬅️ **Slide 2** (Point2D, default: [0,0]): Controls sliding animation for the second set of tiles (when point.x >= 0.5 or point.y >= 0.5)

### ⚙️ Technical Implementation
The effect works through several stages:
1. 🔄 **Initial Transform**: Apply rotation and scaling to input coordinates
2. 🔲 **Pattern Tiling**: Create repeating tiles using modulo operations
3. 🎭 **Selective Sliding**: Apply different slide effects based on tile position
4. 🪞 **Reflection Generation**: Create mirrored patterns within each tile
5. 🔺 **Kaleidoscope Mapping**: Convert to polar coordinates and apply kaleidoscope segmentation
6. 🎨 **Final Sampling**: Sample the original image using the transformed coordinates

### 🎨 Creative Applications
- 🕉️ **Animated Mandalas**: Use slide parameters to create flowing, organic movements
- 🏛️ **Architectural Patterns**: Create complex geometric tile patterns
- 🎵 **VJ Performances**: Combine with audio reactivity for dynamic visual effects
- 🎭 **Texture Generation**: Create seamless, complex patterns for 3D materials

### 💡 Tips for Best Results
- ✅ Start with **Sides** set to 6 or 8 for classic kaleidoscope looks
- ✅ Use small **Size** values (0.1-0.3) for large, dramatic patterns
- ✅ Animate **Slide 1** and **Slide 2** with different speeds for complex motion
- ✅ Combine **Rotation** and **Angle** animation for spinning kaleidoscope effects



🔗 Links

    Original ISF Shader Repository
    COOLLAB Official Website
    Community Node Collection

First community node contributed to the COOLLAB Community Nodes collection - July 19, 2025

---



## 🇩🇪 Deutsch

### 📋 Überblick
Der **Kaleidoscope Tiles** Node erzeugt einen anspruchsvollen Kaleidoskop-Effekt, der traditionelle Kaleidoskop-Spiegelung mit erweiterten Kachel-Funktionen kombiniert. Im Gegensatz zu einem einfachen Kaleidoskop erzeugt dieser Effekt sich wiederholende Kachelmuster mit individuellen Gleitanimationen und komplexen geometrischen Transformationen.
& erstellt grunsätzlich beeindruckende symmetrische, gespiegelte Muster aus beliebigen Eingabebildern oder 2D-Eingabequellen. Dieser Effekt verwandelt gewöhnliche Bilder und 2D-Eingabequellen in faszinierende kaleidoskop-ähnliche Visualisierungen mit sich wiederholenden geometrischen Mustern.


📋 Enthaltene Dateien (notwendige Datein damit es lauffähig ist)

    Kaleidoscope Tiles.clbnode - Das Haupt-COOLLAB Node
    Kaleidoscope Tiles - Default.json - Standard-Preset-Konfiguration

🚀 Verwendung sprich Insatllationsanleitung

Node Importieren:

    Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
    Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
    wie auch die zugehörige Standard-Preset-Datei die .json Datei. 
Sie können die beiden Files in die Kategorie "Image Modifier" respektive den entsprechenden Ordner hinenin legen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwnde im Beispilelspfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernahme (Windows Konto), hier der Beispilspfad um es unter den "Image Modifier's" ein zu ordnen: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\11 Image Modifier (Post Process)

Eingabe Verbinden:

    Beliebiges Bild, 2D-Quellen, Videos oder Generatoren als Eingabe verbinden
    Der Effekt funktioniert am besten mit Bildern und Quellen mit interessanten Details

Parameter Anpassen: sehe Parameterliste die weiter unten folgt

         

⚙️ Technische Details

    Node-Typ: Effekt
    Eingabe: Einzelne Bild-/Textur-Eingabe
    Ausgabe: Verarbeitetes Bild mit Kaleidoskop-Effekt
    Performance: Echtzeitfähig
    Shader-basiert: GPU-beschleunigte Verarbeitung

📜 Lizenz & Attribution

Original-Quelle:

    Basiert auf ISF-Shader aus VIDVOX/ISF-Files
    Original-Shader unter MIT-Lizenz
    Original-Autoren: VIDVOX-Team

Dieses COOLLAB Node:

    Für COOLLAB angepasst von bennoH. & claude.ai
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz




### ✨ Was macht diesen Node besonders
Dies ist kein Standard-Kaleidoskop-Effekt. Die "Tiles"-Komponente fügt mehrere einzigartige Features hinzu:
- 🔲 **Kachelsystem**: Das Bild wird in sich wiederholende Kacheln unterteilt, die unabhängig manipuliert werden können
- 🎭 **Gleit-Effekte**: Zwei separate Gleit-Parameter ermöglichen es verschiedenen Teilen der Kacheln, sich unabhängig zu bewegen
- ⚙️ **Erweiterte Mustererzeugung**: Kombiniert Rotation, Skalierung, Verschiebung und Kaleidoskop-Spiegelung in einer ausgeklügelten Pipeline



### 🎛️ Parameter

#### 🔧 Kern-Transform-Kontrollen
- 📏 **Size** (0.0 - 2.0, Standard: 0.5): Kontrolliert die Skalierung des Kachelmusters. Kleinere Werte erzeugen größere Kacheln, größere Werte erzeugen kleinere, detailliertere Kacheln
- 🔄 **Rotation** (0.0 - 1.0, Standard: 0.125): Rotiert das gesamte Muster vor den Kachel-Operationen
- 📐 **Shift** (Point2D, Standard: [0,0]): Verschiebt das Muster im 2D-Raum vor der Kachelung

#### 🪞 Kaleidoskop-Kontrollen
- 🔺 **Sides** (1 - 32, Standard: 6): Anzahl der Kaleidoskop-Segmente. Erzeugt die charakteristischen gespiegelten Bereiche
- 🎯 **Angle** (0.0 - 1.0, Standard: 0.0): Rotiert den Kaleidoskop-Effekt innerhalb jedes Segments

#### 🎬 Kachel-Animations-Kontrollen
- ➡️ **Slide 1** (Point2D, Standard: [0,0]): Kontrolliert Gleitanimation für den ersten Satz von Kacheln (wenn point.x < 0.5 oder point.y < 0.5)
- ⬅️ **Slide 2** (Point2D, Standard: [0,0]): Kontrolliert Gleitanimation für den zweiten Satz von Kacheln (wenn point.x >= 0.5 oder point.y >= 0.5)

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere Stufen:
1. 🔄 **Initiale Transformation**: Rotation und Skalierung auf Eingabekoordinaten anwenden
2. 🔲 **Muster-Kachelung**: Sich wiederholende Kacheln mit Modulo-Operationen erstellen
3. 🎭 **Selektives Gleiten**: Verschiedene Gleit-Effekte basierend auf Kachelposition anwenden
4. 🪞 **Spiegelungs-Generierung**: Gespiegelte Muster innerhalb jeder Kachel erstellen
5. 🔺 **Kaleidoskop-Mapping**: In Polarkoordinaten umwandeln und Kaleidoskop-Segmentierung anwenden
6. 🎨 **Finales Sampling**: Originalbild mit den transformierten Koordinaten sampeln

### 🎨 Kreative Anwendungen
- 🕉️ **Animierte Mandalas**: Gleit-Parameter für fließende, organische Bewegungen verwenden
- 🏛️ **Architektonische Muster**: Komplexe geometrische Kachelmuster erstellen
- 🎵 **VJ-Performances**: Mit Audio-Reaktivität für dynamische visuelle Effekte kombinieren
- 🎭 **Textur-Generierung**: Nahtlose, komplexe Muster für 3D-Materialien erstellen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Sides** auf 6 oder 8 für klassische Kaleidoskop-Looks beginnen
- ✅ Kleine **Size**-Werte (0.1-0.3) für große, dramatische Muster verwenden
- ✅ **Slide 1** und **Slide 2** mit verschiedenen Geschwindigkeiten für komplexe Bewegung animieren
- ✅ **Rotation** und **Angle**-Animation für drehende Kaleidoskop-Effekte kombinieren

---

## 🔧 Expandet-Technical Notes / Erweiterete Technische Hinweise

**Based on**: ISF shader by VIDVOX 🎨  
**Basiert auf**: ISF Shader von VIDVOX 🎨

**Category**: Effects > Kaleidoscope 🔸  
**Kategorie**: Effekte > Kaleidoskop 🔸

**Input**: UV->sRGB_StraightA (Image) 🖼️  
**Eingabe**: UV->sRGB_StraightA (Bild) 🖼️

**Output**: sRGB_StraightA ✨  
**Ausgabe**: sRGB_StraightA ✨


🔗 Links

    Original ISF Shader Repository
    COOLLAB Official Website
    Community Node Collection

First community node contributed to the COOLLAB Community Nodes collection - July 19, 2025
