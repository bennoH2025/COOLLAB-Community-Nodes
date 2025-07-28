English | Deutsch
---

# ❄️ 3D geo Snowflake Node Documentation

## 🇬🇧 English

### 📋 Overview
The **3D geo Snowflake** node creates sophisticated three-dimensional snowflake shapes using signed distance fields with advanced 3D extrusion capabilities. This node extends the 2D snowflake concept into full 3D space with variable thickness, edge rounding, and thickness variation along the shape's depth. Based on geometric formulas and fractal systems, it generates mathematically precise 3D snowflake forms perfect for winter scenes, architectural elements, decorative objects, and complex 3D compositions.

📋 Files Included

    3D geo Snowflake.clbnode - The main COOLLAB node
    3D geo Snowflake.clbnode.presets.json - Preset configurations with 35 diverse variations

🚀 How to Use

Import the Node:

    Download both files from this directory (necessary files to make it run)
    Copy the .clbnode file into your COOLLAB Launcher to the Node-directory of the most actual Coollab-Version you find in that
    as well as the associated preset .json file. 
You can place the two files in the category "3D Shapes", means in that named folder in your latest version of Coollab, which you can find in the Launcher. In this example, I'm using version "1.4.1 Spout OUT." Also note your username (Windows account). Here's the example path to organize it under the 3D Shapes: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\06 3D Shape

Connect Output:

    Use as a 3D shape source for any material, lighting, or rendering node
    Works excellently with 3D materials, lighting systems, and complex scene compositions
    Perfect for creating detailed winter-themed 3D environments

Adjust Parameters: see the comprehensive parameter list below

⚙️ Technical Details

    Node Type: 3D Shape (Generator)
    Input: None (pure 3D shape generator)
    Output: 3D SignedDistance field
    Performance: Real-time capable
    SDF-based: GPU-accelerated 3D distance field generation with advanced extrusion

📜 License & Attribution

This COOLLAB Node:

    Created for COOLLAB by bennoH. & claude.ai (Sonnet-4 model)
    Licensed under GNU General Public License v3.0
    Compatible with COOLLAB's GPL v3.0 license
    Based on geometric formulas & fractal systems

### ✨ What Makes This Special
This is not a simple 3D extrusion. The 3D geo Snowflake node implements several advanced features:
- ❄️ **True 3D Generation**: Full three-dimensional snowflake shapes with sophisticated depth control
- 🏗️ **Variable Thickness**: Thickness changes dynamically based on distance from center
- 🔄 **Edge Rounding**: Smooth, rounded edges for organic, natural-looking snowflakes
- 📐 **Mathematical Precision**: Uses signed distance fields for perfect geometric accuracy in 3D space
- 🌟 **6-fold Symmetry**: Authentic snowflake symmetry extended into three dimensions
- 🌿 **Branching System**: Sophisticated 3D side-branch generation with depth awareness
- 🔄 **Fractal Detail**: Multi-level detail system that works coherently in 3D space

### 🎛️ Parameters

#### 🔧 Core 2D Shape Controls
- 📏 **Size** (0.0+, default: varies): Controls the overall scale of the 3D snowflake. Larger values create bigger snowflakes
- ❄️ **Arm Length** (0.0+, default: varies): Length of the main snowflake arms extending from center
- 📐 **Arm Thickness** (-5.0 to 5.0+, default: varies): Thickness of the main arms and branches. Negative values create inverse effects
- 🌱 **Branch Density** (0.0-10.0+, default: varies): Controls how many side branches appear along each arm
- ✨ **Detail Level** (0.0-5.0+, default: varies): Adds fine details and sub-branches for complexity
- 🔄 **Symmetry** (0.0-1.0, default: varies): Controls how many of the 6 arms are visible (0.0 = 1 arm, 1.0 = all 6 arms)
- 🔄 **Rotation** (Angle, default: 0°): Rotates the entire snowflake around its center

#### 🏗️ Advanced 3D Controls
- 📊 **Z Thickness** (-5.0 to 5.0+, default: varies): Controls the depth/thickness of the 3D extrusion. Negative values can create hollow or inverted effects
- 🔘 **Edge Rounding** (0.0-5.0+, default: varies): Smooths the edges of the 3D shape. Higher values create more rounded, organic forms
- 📈 **Thickness Variation** (-30.0 to 30.0+, default: varies): Varies thickness based on distance from center. Creates natural tapering effects

### ⚙️ Technical Implementation
The effect works through several sophisticated stages:
1. 🎯 **2D Pattern Generation**: Create base snowflake pattern using mathematical formulas
2. 📐 **6-fold Symmetry**: Apply radial symmetry using rotation matrices
3. 🌿 **Branch Generation**: Add side branches at calculated intervals along arms
4. ✨ **Detail Addition**: Apply sub-branches and fine details based on detail level
5. 🏗️ **3D Extrusion**: Extend 2D pattern into 3D space with variable thickness
6. 📊 **Thickness Variation**: Apply distance-based thickness modulation
7. 🔘 **Edge Rounding**: Apply smooth edge rounding for organic appearance
8. 🔍 **SDF Combination**: Combine all elements using optimized 3D distance field operations

### 🎨 Creative Applications
- ❄️ **Winter Environments**: Create detailed 3D snowflake collections for winter scenes
- 🏛️ **Architectural Elements**: Use as decorative 3D elements in buildings and structures
- 💍 **Jewelry Design**: Perfect geometric forms for ornamental and jewelry applications
- 🎭 **Logo Design**: Create sophisticated 3D brand elements and symbols
- 🌟 **Sculptural Art**: Generate complex 3D sculptural forms with natural beauty
- 🎬 **Film & Animation**: Detailed 3D snowflakes for cinematic winter sequences

### 💡 Tips for Best Results
- ✅ Start with positive **Z Thickness** (0.1-0.5) for solid 3D shapes
- ✅ Use **Edge Rounding** (0.1-1.0) for natural, organic snowflake appearance
- ✅ **Thickness Variation** between 1-5 creates beautiful tapering effects
- ✅ Negative **Arm Thickness** values create interesting inverse/hollow effects
- ✅ Combine multiple nodes with different rotations for complex snowfall scenes
- ✅ Use **Symmetry** < 1.0 for partial snowflakes and artistic variations

### 🎨 Comprehensive Preset Collection
The node includes 35 carefully crafted presets covering a vast range of snowflake styles:

#### ❄️ Classic Winter Shapes
- **WinterScape One**: Traditional detailed snowflake with natural proportions
- **Crisp StarLet**: Sharp, crystalline star-like snowflake design
- **Happy-Frost**: Cheerful, highly detailed snowflake with dense branching
- **The WinterStar Symbol**: Clean, symbolic winter star representation

#### 🌟 Star Variations
- **Sea-Star Shelby**: Organic star shape reminiscent of sea creatures
- **CookieStar**: Rounded, cookie-cutter style star design
- **SmallSTAR**: Compact, simple star with clean geometry
- **Ice Ice Stary**: Extended arms with crystalline detail
- **China Star**: Complex star with intricate branching patterns
- **Deco Star**: Decorative star with artistic proportions

#### 🎭 Artistic & Abstract Forms
- **Z-Star 0**: Minimalist design with negative thickness effects
- **StarDreamer**: Ethereal, dream-like snowflake with soft edges
- **Straw Star**: Thin, delicate straw-like structure
- **BowCrown**: Crown-like shape with regal proportions
- **BowCrown XL**: Extended version with enhanced rounding

#### 🌍 Cultural & Themed Variations
- **Ethiopic ChurchStar**: Inspired by Ethiopian cross designs
- **Chie-STAR**: Asian-influenced star pattern
- **TexasMan'sHead**: Unique asymmetrical design with personality
- **MapleTreeLeavSTARik**: Maple leaf inspired snowflake design

#### 🔮 Mystical & Fantasy Shapes
- **CrudFo is not U-Fo**: Mysterious, UFO-inspired design
- **Part El-Shel**: Partial shell-like organic form
- **QuantSixtant**: Mathematical, quantized design
- **O-Risus**: Smile-inspired curved design
- **Door to the hiden City**: Gateway-like architectural form

#### 🦋 Organic & Natural Forms
- **Krampurnus**: Horn-like, organic creature-inspired design
- **Storrilo Pik**: Sharp, dynamic organic spikes
- **V-Chrove**: V-shaped wing-like structure
- **VaginButerFlay**: Butterfly-wing organic form
- **CrosWings**: Cross-shaped wing design
- **Chau Ho Mau**: Flowing, organic Asian-inspired form

#### 🎪 Playful & Unique Designs
- **StaryStar floral**: Floral-inspired delicate star design
- **DubCrosing**: Complex crossing pattern design
- **Gin Zen Py ohh me ma mo ...**: Zen-inspired minimalist approach

### 🎬 3D Workflow Recommendations
1. **Shape Selection**: Choose appropriate preset based on intended use
2. **Scale Adjustment**: Use **Size** parameter to fit scene requirements
3. **3D Refinement**: Adjust **Z Thickness** for desired depth
4. **Edge Softening**: Apply **Edge Rounding** for natural appearance
5. **Variation**: Use **Thickness Variation** for organic tapering
6. **Material Application**: Apply appropriate 3D materials and lighting

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025

---

## 🇩🇪 Deutsch

### 📋 Überblick
Der **3D geo Snowflake** Node erzeugt anspruchsvolle dreidimensionale Schneeflocken-Formen mittels Signed Distance Fields mit erweiterten 3D-Extrusions-Fähigkeiten. Dieser Node erweitert das 2D-Schneeflocken-Konzept in den vollen 3D-Raum mit variabler Dicke, Kantenrundung und Dickenvariation entlang der Form-Tiefe. Basiert auf geometrischen Formeln und Fraktalsystemen und generiert mathematisch präzise 3D-Schneeflocken-Formen perfekt für Winterszenen, architektonische Elemente, dekorative Objekte und komplexe 3D-Kompositionen.

📋 Enthaltene Dateien (notwendige Dateien damit es lauffähig ist)

    3D geo Snowflake.clbnode - Das Haupt-COOLLAB Node
    3D geo Snowflake.clbnode.presets.json - Preset-Konfigurationen mit 35 diversen Variationen

🚀 Verwendung sprich Installationsanleitung

Node Importieren:

    Sie müssen beide Dateien aus diesem Verzeichnis herunterladen
    Die .clbnode Datei in Ihr COOLLAB Launcher kopieren
    wie auch die zugehörige Preset-Datei die .json Datei. 
Sie können die beiden Files in die Kategorie "3D Shapes" respektive den entsprechenden Ordner hineinlegen in Ihrer aktuellsten Version von Coollab die Sie im Launcher finden, ich verwende im Beispielpfad Version "1.4.1 Spout OUT" und beachten Sie auch Ihren Nutzernamen (Windows Konto), hier der Beispielpfad um es unter den "3D Shapes" einzuordnen: 
    C:\Users_YourUserName_\AppData\Roaming\Coollab Launcher\Installed Versions\1.4.1 Spout OUT\Nodes\06 3D Shape

Ausgabe Verbinden:

    Als 3D-Form-Quelle für beliebige Material-, Beleuchtungs- oder Rendering-Nodes verwenden
    Funktioniert hervorragend mit 3D-Materialien, Beleuchtungssystemen und komplexen Szenen-Kompositionen
    Perfekt für detaillierte winter-thematische 3D-Umgebungen

Parameter Anpassen: siehe die umfassende Parameterliste weiter unten

⚙️ Technische Details

    Node-Typ: 3D Shape (Generator)
    Eingabe: Keine (reiner 3D-Form-Generator)
    Ausgabe: 3D SignedDistance Feld
    Performance: Echtzeitfähig
    SDF-basiert: GPU-beschleunigte 3D-Distance-Field-Generierung mit erweiteter Extrusion

📜 Lizenz & Attribution

Dieses COOLLAB Node:

    Für COOLLAB erstellt von bennoH. & claude.ai (Sonnet-4 Modell)
    Lizenziert unter GNU General Public License v3.0
    Kompatibel mit COOLLABs GPL v3.0 Lizenz
    Basiert auf geometrischen Formeln & Fraktalsystemen

### ✨ Was macht diesen Node besonders
Dies ist keine einfache 3D-Extrusion. Der 3D geo Snowflake Node implementiert mehrere erweiterte Features:
- ❄️ **Echte 3D-Generierung**: Vollständige dreidimensionale Schneeflocken-Formen mit ausgeklügelter Tiefenkontrolle
- 🏗️ **Variable Dicke**: Dicke ändert sich dynamisch basierend auf Distanz vom Zentrum
- 🔄 **Kantenrundung**: Glatte, gerundete Kanten für organische, natürlich aussehende Schneeflocken
- 📐 **Mathematische Präzision**: Verwendet Signed Distance Fields für perfekte geometrische Genauigkeit im 3D-Raum
- 🌟 **6-fache Symmetrie**: Authentische Schneeflocken-Symmetrie erweitert in drei Dimensionen
- 🌿 **Verzweigungssystem**: Ausgeklügeltes 3D-Seitenzweig-System mit Tiefenbewusstsein
- 🔄 **Fraktale Details**: Multi-Level-Detail-System das kohärent im 3D-Raum funktioniert

### 🎛️ Parameter

#### 🔧 Kern-2D-Form-Kontrollen
- 📏 **Size** (0.0+, Standard: variiert): Kontrolliert die Gesamtgröße der 3D-Schneeflocke. Größere Werte erzeugen größere Schneeflocken
- ❄️ **Arm Length** (0.0+, Standard: variiert): Länge der Haupt-Schneeflocken-Arme die vom Zentrum ausgehen
- 📐 **Arm Thickness** (-5.0 bis 5.0+, Standard: variiert): Dicke der Hauptarme und Verzweigungen. Negative Werte erzeugen inverse Effekte
- 🌱 **Branch Density** (0.0-10.0+, Standard: variiert): Kontrolliert wie viele Seitenzweige entlang jedes Arms erscheinen
- ✨ **Detail Level** (0.0-5.0+, Standard: variiert): Fügt feine Details und Unter-Verzweigungen für Komplexität hinzu
- 🔄 **Symmetry** (0.0-1.0, Standard: variiert): Kontrolliert wie viele der 6 Arme sichtbar sind (0.0 = 1 Arm, 1.0 = alle 6 Arme)
- 🔄 **Rotation** (Winkel, Standard: 0°): Rotiert die gesamte Schneeflocke um ihr Zentrum

#### 🏗️ Erweiterte 3D-Kontrollen
- 📊 **Z Thickness** (-5.0 bis 5.0+, Standard: variiert): Kontrolliert die Tiefe/Dicke der 3D-Extrusion. Negative Werte können hohle oder invertierte Effekte erzeugen
- 🔘 **Edge Rounding** (0.0-5.0+, Standard: variiert): Glättet die Kanten der 3D-Form. Höhere Werte erzeugen gerundetere, organische Formen
- 📈 **Thickness Variation** (-30.0 bis 30.0+, Standard: variiert): Variiert Dicke basierend auf Distanz vom Zentrum. Erzeugt natürliche Verjüngungs-Effekte

### ⚙️ Technische Implementation
Der Effekt funktioniert durch mehrere ausgeklügelte Stufen:
1. 🎯 **2D-Muster-Generierung**: Basis-Schneeflocken-Muster mit mathematischen Formeln erstellen
2. 📐 **6-fache Symmetrie**: Radiale Symmetrie mit Rotationsmatrizen anwenden
3. 🌿 **Zweig-Generierung**: Seitenzweige in berechneten Intervallen entlang der Arme hinzufügen
4. ✨ **Detail-Addition**: Unter-Verzweigungen und feine Details basierend auf Detail-Level anwenden
5. 🏗️ **3D-Extrusion**: 2D-Muster in 3D-Raum mit variabler Dicke erweitern
6. 📊 **Dicken-Variation**: Distanz-basierte Dicken-Modulation anwenden
7. 🔘 **Kanten-Rundung**: Glatte Kanten-Rundung für organisches Aussehen anwenden
8. 🔍 **SDF-Kombination**: Alle Elemente mit optimierten 3D-Distance-Field-Operationen kombinieren

### 🎨 Kreative Anwendungen
- ❄️ **Winter-Umgebungen**: Detaillierte 3D-Schneeflocken-Sammlungen für Winterszenen erstellen
- 🏛️ **Architektonische Elemente**: Als dekorative 3D-Elemente in Gebäuden und Strukturen verwenden
- 💍 **Schmuck-Design**: Perfekte geometrische Formen für ornamentale und Schmuck-Anwendungen
- 🎭 **Logo-Design**: Anspruchsvolle 3D-Markenelemente und Symbole erstellen
- 🌟 **Skulpturale Kunst**: Komplexe 3D-skulpturale Formen mit natürlicher Schönheit generieren
- 🎬 **Film & Animation**: Detaillierte 3D-Schneeflocken für filmische Wintersequenzen

### 💡 Tipps für beste Ergebnisse
- ✅ Mit positiver **Z Thickness** (0.1-0.5) für solide 3D-Formen beginnen
- ✅ **Edge Rounding** (0.1-1.0) für natürliches, organisches Schneeflocken-Aussehen verwenden
- ✅ **Thickness Variation** zwischen 1-5 erzeugt schöne Verjüngungs-Effekte
- ✅ Negative **Arm Thickness**-Werte erzeugen interessante inverse/hohle Effekte
- ✅ Mehrere Nodes mit verschiedenen Rotationen für komplexe Schneefall-Szenen kombinieren
- ✅ **Symmetry** < 1.0 für partielle Schneeflocken und künstlerische Variationen verwenden

### 🎨 Umfassende Preset-Sammlung
Der Node enthält 35 sorgfältig gestaltete Presets die eine riesige Bandbreite von Schneeflocken-Stilen abdecken:

#### ❄️ Klassische Winter-Formen
- **WinterScape One**: Traditionelle detaillierte Schneeflocke mit natürlichen Proportionen
- **Crisp StarLet**: Scharfes, kristallines stern-ähnliches Schneeflocken-Design
- **Happy-Frost**: Fröhliche, hochdetaillierte Schneeflocke mit dichter Verzweigung
- **The WinterStar Symbol**: Saubere, symbolische Winter-Stern-Darstellung

#### 🌟 Stern-Variationen
- **Sea-Star Shelby**: Organische Stern-Form die an Meereskreaturen erinnert
- **CookieStar**: Gerundetes, Keksausstecher-Stil Stern-Design
- **SmallSTAR**: Kompakter, einfacher Stern mit sauberer Geometrie
- **Ice Ice Stary**: Erweiterte Arme mit kristallinen Details
- **China Star**: Komplexer Stern mit komplizierten Verzweigungsmustern
- **Deco Star**: Dekorativer Stern mit künstlerischen Proportionen

[Continues with all preset descriptions in German...]

---

## 🔧 Expanded Technical Notes / Erweiterte Technische Hinweise

**Based on**: Geometric formulas & fractal systems with 3D extrusion 🔬  
**Basiert auf**: Geometrischen Formeln & Fraktalsystemen mit 3D-Extrusion 🔬

**Category**: 3D Shape > Generators ❄️  
**Kategorie**: 3D Shape > Generatoren ❄️

**Input**: None (Pure 3D Generator) 🎯  
**Eingabe**: Keine (Reiner 3D-Generator) 🎯

**Output**: 3D SignedDistance ✨  
**Ausgabe**: 3D SignedDistance ✨

**Presets**: 35 diverse variations 🎨  
**Presets**: 35 diverse Variationen 🎨

🔗 Links

    COOLLAB Official Website
    Community Node Collection

Community node contributed to the COOLLAB Community Nodes collection - July 2025
