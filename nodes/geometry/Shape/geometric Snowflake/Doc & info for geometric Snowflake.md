English | Deutsch
---

# ❄️ Geometric Snowflake Node Documentation

## 🇬🇧 English

### 📋 Overview
The **Geometric Snowflake** node creates sophisticated 2D snowflake shapes using signed distance fields (SDF). This node generates mathematically precise snowflake patterns with customizable branching structures, inspired by natural snowflake formations and fractal geometry. It produces detailed, symmetrical snowflake shapes perfect for winter-themed graphics, decorative elements, and procedural pattern generation.

📋 Files Included

    geometric Snowflake.clbnode - The main COOLLAB node
    geometric Snowflake.clbnode.presets.json - Preset configurations with 8 variations

🚀 How to Use

Import the Node:

    Download both files from this directory (necessary files to make it run)
    Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
    as well as the associated preset .json file. 
You can place the two files in the category "Shape", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the Shapes: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\05 Shape

Connect Output:

    Use as a shape source for any material or effect node
    Works excellently with lighting, texturing, and color effects
    Perfect for creating complex winter-themed compositions

Adjust Parameters: see the parameter list below

⚙️ Technical Details

    Node Type: Shape (2D Signed Distance Field)
    Input: None (pure shape generator)
    Output: SignedDistance field
    Performance: Real-time capable
    SDF-based: GPU-accelerated distance field generation

📜 License & Attribution

This COOLLAB Node:

    Created for COOLLAB by bennoH. & claude.ai (Sonnet-4 model)
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license
    Based on geometric formulas & fractal systems

### ✨ What Makes This Special
This is not a simple snowflake shape. The node implements several advanced features:
- ❄️ **Mathematical Precision**: Uses signed distance fields for perfect geometric accuracy
- 🌟 **6-fold Symmetry**: Authentic snowflake symmetry with customizable arm count
- 🌿 **Branching System**: Sophisticated side-branch generation with density control
- 🔄 **Fractal Detail**: Multi-level detail system for realistic snowflake complexity
- ⚡ **Real-time Performance**: Optimized SDF implementation for smooth interaction

### 🎛️ Parameters

#### 🔧 Core Shape Controls
- 📏 **Size** (0.0+, default: 1.0): Controls the overall scale of the snowflake. Larger values create bigger snowflakes
- ❄️ **Arm Length** (0.0-1.0+, default: 0.5): Length of the main snowflake arms extending from center
- 📐 **Arm Thickness** (0.001-0.1, default: ~0.02): Thickness of the main arms and branches

#### 🌿 Branching Controls
- 🌱 **Branch Density** (0.0-5.0+, default: 0.82): Controls how many side branches appear along each arm
- ✨ **Detail Level** (0.0-2.0+, default: varies): Adds fine details and sub-branches for complexity
- 🔄 **Symmetry** (0.0-1.0, default: 1.0): Controls how many of the 6 arms are visible (0.0 = 1 arm, 1.0 = all 6 arms)

#### 🎯 Transform Controls
- 🔄 **Rotation** (Angle, default: 0°): Rotates the entire snowflake around its center

### ⚙️ Technical Implementation
The effect works through several sophisticated stages:
1. 🎯 **Coordinate Setup**: Transform UV coordinates and apply rotation
2. 📐 **Symmetry Generation**: Create 6-fold radial symmetry using rotation matrices  
3. ❄️ **Main Arms**: Generate primary snowflake arms with controlled thickness
4. 🌿 **Branch Generation**: Add side branches at calculated intervals along arms
5. ✨ **Detail Addition**: Apply sub-branches and fine details based on detail level
6. 🔍 **SDF Combination**: Combine all elements using optimized distance field operations

### 🎨 Creative Applications
- ❄️ **Winter Graphics**: Create authentic snowflake decorations and patterns
- 🎄 **Holiday Content**: Perfect for Christmas and winter-themed visuals
- 🔄 **Pattern Generation**: Use as base for complex tiling and repetition effects
- 🎭 **Logo Design**: Create unique, geometric brand elements
- 🌟 **Procedural Art**: Combine with other nodes for complex generative art

### 💡 Tips for Best Results
- ✅ Start with **Size** = 1.0 and **Symmetry** = 1.0 for classic snowflakes
- ✅ Use **Branch Density** between 0.5-1.5 for realistic branch distribution
- ✅ Increase **Detail Level** gradually to add complexity without performance loss
- ✅ Animate **Rotation** for spinning snowflake effects
- ✅ Lower **Symmetry** values create partial snowflakes for artistic effects

### 🎨 Preset Variations
The node includes 8 carefully crafted presets:
- **Ice Cristal**: Classic, delicate snowflake with fine details
- **Winter Symbol (2D)**: Bold, symbolic snowflake design
- **CristalStar**: Star-like snowflake with enhanced branching
- **Symetrico**: Highly detailed, symmetrical pattern
- **Krypticol**: Complex, cryptic snowflake structure
- **Wing Thing**: Asymmetrical, wing-like variation
- **Tribut of a Tribun**: Tribute pattern with unique characteristics
- **Asymeter**: Partially asymmetrical design for artistic variation

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025

---

## 🇩🇪 Deutsch

### 📋 Überblick
Der **Geometric Snowflake** Node erzeugt anspruchsvolle 2D-Schneeflocken-Formen mit Signed Distance Fields (SDF). Dieser Node generiert mathematisch präzise Schneeflocken-Muster mit anpassbaren Verzweigungsstrukturen, inspiriert von natürlichen Schneeflocken-Formationen und Fraktal-Geometrie. Er produziert detaillierte, symmetrische Schneeflocken-Formen, perfekt für winter-thematische Grafiken, dekorative Elemente und prozedurale Muster-Generierung.

📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)

    geometric Snowflake.clbnode - Das Haupt-COOLLAB Node
    geometric Snowflake.clbnode.presets.json - Preset-Konfigurationen mit 8 Variationen

🚀 Verwendung sprich Installationsanleitung

Node Importieren:

    Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
    Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
    wie auch die zugehörige Preset-Datei die .json Datei. 
Sie können die beiden Files in die Kategorie "Shape" respektive den entsprechenden Ordner hineinlegen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "Shapes" einzuordnen: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\05 Shape

Ausgabe Verbinden:

    Als Shape-Quelle für beliebige Material- oder Effekt-Nodes verwenden
    Funktioniert hervorragend mit Beleuchtung, Texturierung und Farbeffekten
    Perfekt für komplexe winter-thematische Kompositionen

Parameter Anpassen: siehe Parameterliste die weiter unten folgt

⚙️ Technische Details

    Node-Typ: Shape (2D Signed Distance Field)
    Eingabe: Keine (reiner Shape-Generator)
    Ausgabe: SignedDistance Feld
    Performance: Echtzeitfähig
    SDF-basiert: GPU-beschleunigte Distance-Field-Generierung

📜 Lizenz & Attribution

Dieses COOLLAB Node:

    Für COOLLAB erstellt von bennoH. & claude.ai (Sonnet-4 Modell)
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz
    Basiert auf geometrischen Formeln & Fraktalsystemen

### ✨ Was macht diesen Node besonders
Dies ist keine einfache Schneeflocken-Form. Der Node implementiert mehrere erweiterte Features:
- ❄️ **Mathematische Präzision**: Verwendet Signed Distance Fields für perfekte geometrische Genauigkeit
- 🌟 **6-fache Symmetrie**: Authentische Schneeflocken-Symmetrie mit anpassbarer Armanzahl
- 🌿 **Verzweigungssystem**: Ausgeklügeltes Seitenzweig-System mit Dichte-Kontrolle
- 🔄 **Fraktale Details**: Multi-Level-Detail-System für realistische Schneeflocken-Komplexität
- ⚡ **Echtzeit-Performance**: Optimierte SDF-Implementation für flüssige Interaktion

### 🎛️ Parameter

#### 🔧 Kern-Form-Kontrollen
- 📏 **Size** (0.0+, Standard: 1.0): Kontrolliert die Gesamtgröße der Schneeflocke. Größere Werte erzeugen größere Schneeflocken
- ❄️ **Arm Length** (0.0-1.0+, Standard: 0.5): Länge der Haupt-Schneeflocken-Arme die vom Zentrum ausgehen
- 📐 **Arm Thickness** (0.001-0.1, Standard: ~0.02): Dicke der Hauptarme und Verzweigungen

#### 🌿 Verzweigungs-Kontrollen
- 🌱 **Branch Density** (0.0-5.0+, Standard: 0.82): Kontrolliert wie viele Seitenzweige entlang jedes Arms erscheinen
- ✨ **Detail Level** (0.0-2.0+, Standard: variiert): Fügt feine Details und Unter-Verzweigungen für Komplexität hinzu
- 🔄 **Symmetry** (0.0-1.0, Standard: 1.0): Kontrolliert wie viele der 6 Arme sichtbar sind (0.0 = 1 Arm, 1.0 = alle 6 Arme)

#### 🎯 Transform-Kontrollen
- 🔄 **Rotation** (Winkel, Standard: 0°): Rotiert die gesamte Schneeflocke um ihr Zentrum

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere ausgeklügelte Stufen:
1. 🎯 **Koordinaten-Setup**: UV-Koordinaten transformieren und Rotation anwenden
2. 📐 **Symmetrie-Generierung**: 6-fache radiale Symmetrie mit Rotationsmatrizen erstellen
3. ❄️ **Hauptarme**: Primäre Schneeflocken-Arme mit kontrollierter Dicke generieren
4. 🌿 **Zweig-Generierung**: Seitenzweige in berechneten Intervallen entlang der Arme hinzufügen
5. ✨ **Detail-Addition**: Unter-Verzweigungen und feine Details basierend auf Detail-Level anwenden
6. 🔍 **SDF-Kombination**: Alle Elemente mit optimierten Distance-Field-Operationen kombinieren

### 🎨 Kreative Anwendungen
- ❄️ **Winter-Grafiken**: Authentische Schneeflocken-Dekorationen und Muster erstellen
- 🎄 **Feiertagsinhalte**: Perfekt für Weihnachts- und winter-thematische Visualisierungen
- 🔄 **Muster-Generierung**: Als Basis für komplexe Kachel- und Wiederholungseffekte verwenden
- 🎭 **Logo-Design**: Einzigartige, geometrische Markenelemente erstellen
- 🌟 **Prozedurale Kunst**: Mit anderen Nodes für komplexe generative Kunst kombinieren

### 💡 Tipps für beste Ergebnisse
- ✅ Mit **Size** = 1.0 und **Symmetry** = 1.0 für klassische Schneeflocken beginnen
- ✅ **Branch Density** zwischen 0.5-1.5 für realistische Zweig-Verteilung verwenden
- ✅ **Detail Level** graduell erhöhen um Komplexität ohne Performance-Verlust hinzuzufügen
- ✅ **Rotation** für drehende Schneeflocken-Effekte animieren
- ✅ Niedrigere **Symmetry**-Werte erzeugen partielle Schneeflocken für künstlerische Effekte

### 🎨 Preset-Variationen
Der Node enthält 8 sorgfältig gestaltete Presets:
- **Ice Cristal**: Klassische, zarte Schneeflocke mit feinen Details
- **Winter Symbol (2D)**: Kühnes, symbolisches Schneeflocken-Design
- **CristalStar**: Stern-ähnliche Schneeflocke mit verstärkter Verzweigung
- **Symetrico**: Hochdetailliertes, symmetrisches Muster
- **Krypticol**: Komplexe, kryptische Schneeflocken-Struktur
- **Wing Thing**: Asymmetrische, flügel-ähnliche Variation
- **Tribut of a Tribun**: Tribut-Muster mit einzigartigen Charakteristiken
- **Asymeter**: Teilweise asymmetrisches Design für künstlerische Variation

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Geometric formulas & fractal systems 🔬  
**Basiert auf**: Geometrischen Formeln & Fraktalsystemen 🔬

**Category**: Shape > Generators ❄️  
**Kategorie**: Shape > Generatoren ❄️

**Input**: None (Pure Generator) 🎯  
**Eingabe**: Keine (Reiner Generator) 🎯

**Output**: SignedDistance ✨  
**Ausgabe**: SignedDistance ✨

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025
