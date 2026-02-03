[English](#make-bg-color---documentation) | [Deutsch](#make-bg-color---dokumentation)

---

# Make BG Color - Documentation

## Overview

**Make BG Color** is a simple color replacement tool originally intended for backgrounds but useful for various solid color applications. It replaces input colors completely while preserving alpha/transparency.

⚠️ **Note**: This node ignores the input's color completely - it only uses the alpha channel. Perfect for solid colors, but not for color grading!

## What It Does

🎨 **Replaces all colors** with your chosen RGBA  
🔲 **Keeps alpha/shape** from the input  
⚡ **Simple & direct** - no blending, just replacement

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | Provides alpha/transparency mask |
| **R** | 0.0 - 1.0 | - | Red channel (0 = none, 1 = full) |
| **G** | 0.0 - 1.0 | - | Green channel |
| **B** | 0.0 - 1.0 | - | Blue channel |
| **A** | 0.0 - 1.0 | - | Alpha/transparency (0 = invisible, 1 = opaque) |

## 💡 Use Cases

### ✅ Works Great For:

**🖼️ Solid Color Backgrounds:**
- R: 0.2, G: 0.3, B: 0.5, A: 1.0
- Creates uniform colored backdrop
- Perfect for simple backgrounds

**🔵 Flat 3D Shape Colors:**
- Input: 3D SDF shape (sphere, cube, etc.)
- R: 1.0, G: 0.0, B: 0.0, A: 1.0
- Result: Solid red 3D object (no shading!)
- Note: No lighting/edges - pure flat color

**🎨 Color Overlays:**
- Semi-transparent colors
- A: 0.5 for 50% transparency
- Layering effects

**🌈 Simple Colored Shapes:**
- Geometric generators
- Flat color fills
- Minimalist graphics

### ❌ Doesn't Work For:

**2D Shapes/Generators:**
- Input: 2D shape/pattern
- Result: Screen-filling solid color (shape lost!)
- Use Colorize Easy instead

**Color Grading:**
- Doesn't preserve original colors
- Completely replaces them
- Use Color Grading nodes instead

**Textured/Detailed Images:**
- All detail lost, only alpha preserved
- Not suitable for photos/complex images

## Quick Examples

### Example 1: Blue Background
```
Input: Empty/white screen
R: 0.0, G: 0.2, B: 0.8, A: 1.0
Result: Solid blue screen
```

### Example 2: Red 3D Sphere
```
Input: Sphere (3D SDF)
R: 1.0, G: 0.0, B: 0.0, A: 1.0
Result: Flat red sphere (no shading)
```

### Example 3: Semi-Transparent Green
```
Input: Any shape
R: 0.0, G: 0.8, B: 0.2, A: 0.5
Result: 50% transparent green
```

### Example 4: Purple Overlay
```
Input: Video/image
R: 0.6, G: 0.0, B: 0.8, A: 0.3
Result: Purple tinted overlay
```

## 🎨 Color Recipes

**Primary Colors:**
- 🔴 Red: R:1.0, G:0.0, B:0.0
- 🟢 Green: R:0.0, G:1.0, B:0.0
- 🔵 Blue: R:0.0, G:0.0, B:1.0

**Common Backgrounds:**
- ⬜ White: R:1.0, G:1.0, B:1.0
- ⬛ Black: R:0.0, G:0.0, B:0.0
- 🟦 Sky Blue: R:0.4, G:0.7, B:1.0
- 🟫 Warm Gray: R:0.5, G:0.48, B:0.46

**Creative Colors:**
- 🟣 Purple: R:0.6, G:0.2, B:0.8
- 🟠 Orange: R:1.0, G:0.5, B:0.0
- 🩷 Pink: R:1.0, G:0.4, B:0.7
- 🟡 Yellow: R:1.0, G:0.9, B:0.0

## How It Works
```
Output RGB = Target RGB (input color ignored!)
Output Alpha = Input Alpha × Target Alpha
```

Simple: Takes your RGBA values, applies them everywhere the input has alpha.

## When to Use

**✅ Use Make BG Color for:**
- Simple solid backgrounds
- Flat 3D object colors
- Color overlays
- Minimalist graphics

**❌ Use other nodes for:**
- 2D shapes → **Colorize Easy**
- Color grading → **Color Grading** nodes
- Textured objects → **Materials/Shading**

## Tips

💡 **For 3D shapes:** Creates flat colors without shading  
💡 **For backgrounds:** Perfect for simple solid colors  
💡 **For 2D shapes:** Won't work as expected - use Colorize Easy  
💡 **Alpha control:** Adjust A parameter for transparency

## Troubleshooting

**Problem: 2D shape disappeared, just see solid color**
- This is normal behavior for this node
- Use **Colorize Easy** instead

**Problem: 3D shape has no depth/shading**
- This node removes all lighting/shading
- Intentional for flat color look
- Use materials if you want shading

**Problem: Color not visible**
- Check **A** (Alpha) - might be 0.0
- Set A to 1.0 for fully opaque

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#make-bg-color---documentation) | [Deutsch](#make-bg-color---dokumentation)

---

# Make BG Color - Dokumentation

## Übersicht

**Make BG Color** ist ein einfaches Farbersetzungs-Tool, ursprünglich für Hintergründe gedacht, aber nützlich für verschiedene Vollfarb-Anwendungen. Es ersetzt Input-Farben komplett während es Alpha/Transparenz bewahrt.

⚠️ **Hinweis**: Dieser Node ignoriert die Input-Farbe komplett - er nutzt nur den Alpha-Kanal. Perfekt für Vollfarben, aber nicht für Color Grading!

## Was es macht

🎨 **Ersetzt alle Farben** mit Ihrer gewählten RGBA  
🔲 **Behält Alpha/Form** vom Input  
⚡ **Einfach & direkt** - kein Blending, nur Ersetzung

## Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Liefert Alpha/Transparenz-Maske |
| **R** | 0.0 - 1.0 | - | Rotkanal (0 = keiner, 1 = voll) |
| **G** | 0.0 - 1.0 | - | Grünkanal |
| **B** | 0.0 - 1.0 | - | Blaukanal |
| **A** | 0.0 - 1.0 | - | Alpha/Transparenz (0 = unsichtbar, 1 = undurchsichtig) |

## 💡 Anwendungsfälle

### ✅ Funktioniert Großartig Für:

**🖼️ Vollfarb-Hintergründe:**
- R: 0.2, G: 0.3, B: 0.5, A: 1.0
- Erzeugt einheitliche farbige Kulisse
- Perfekt für einfache Hintergründe

**🔵 Flache 3D-Form-Farben:**
- Input: 3D SDF-Form (Kugel, Würfel, etc.)
- R: 1.0, G: 0.0, B: 0.0, A: 1.0
- Ergebnis: Solid rotes 3D-Objekt (keine Schattierung!)
- Hinweis: Keine Beleuchtung/Kanten - pure flache Farbe

**🎨 Farb-Overlays:**
- Halbtransparente Farben
- A: 0.5 für 50% Transparenz
- Schichtungs-Effekte

**🌈 Einfache Gefärbte Formen:**
- Geometrische Generatoren
- Flache Farb-Füllungen
- Minimalistische Grafiken

### ❌ Funktioniert Nicht Für:

**2D-Formen/Generatoren:**
- Input: 2D-Form/Muster
- Ergebnis: Bildschirmfüllende Vollfarbe (Form verloren!)
- Nutzen Sie Colorize Easy stattdessen

**Color Grading:**
- Bewahrt Original-Farben nicht
- Ersetzt sie komplett
- Nutzen Sie Color Grading Nodes stattdessen

**Texturierte/Detaillierte Bilder:**
- Alle Details verloren, nur Alpha bewahrt
- Nicht geeignet für Fotos/komplexe Bilder

## Schnelle Beispiele

### Beispiel 1: Blauer Hintergrund
```
Input: Leerer/weißer Screen
R: 0.0, G: 0.2, B: 0.8, A: 1.0
Ergebnis: Solider blauer Screen
```

### Beispiel 2: Rote 3D-Kugel
```
Input: Kugel (3D SDF)
R: 1.0, G: 0.0, B: 0.0, A: 1.0
Ergebnis: Flache rote Kugel (keine Schattierung)
```

### Beispiel 3: Halbtransparentes Grün
```
Input: Beliebige Form
R: 0.0, G: 0.8, B: 0.2, A: 0.5
Ergebnis: 50% transparentes Grün
```

### Beispiel 4: Lila Overlay
```
Input: Video/Bild
R: 0.6, G: 0.0, B: 0.8, A: 0.3
Ergebnis: Lila getöntes Overlay
```

## 🎨 Farb-Rezepte

**Primärfarben:**
- 🔴 Rot: R:1.0, G:0.0, B:0.0
- 🟢 Grün: R:0.0, G:1.0, B:0.0
- 🔵 Blau: R:0.0, G:0.0, B:1.0

**Häufige Hintergründe:**
- ⬜ Weiß: R:1.0, G:1.0, B:1.0
- ⬛ Schwarz: R:0.0, G:0.0, B:0.0
- 🟦 Himmelblau: R:0.4, G:0.7, B:1.0
- 🟫 Warmes Grau: R:0.5, G:0.48, B:0.46

**Kreative Farben:**
- 🟣 Lila: R:0.6, G:0.2, B:0.8
- 🟠 Orange: R:1.0, G:0.5, B:0.0
- 🩷 Pink: R:1.0, G:0.4, B:0.7
- 🟡 Gelb: R:1.0, G:0.9, B:0.0

## Wie es funktioniert
```
Output RGB = Target RGB (Input-Farbe ignoriert!)
Output Alpha = Input Alpha × Target Alpha
```

Einfach: Nimmt Ihre RGBA-Werte, wendet sie überall an wo Input Alpha hat.

## Wann nutzen

**✅ Nutzen Sie Make BG Color für:**
- Einfache Vollfarb-Hintergründe
- Flache 3D-Objekt-Farben
- Farb-Overlays
- Minimalistische Grafiken

**❌ Nutzen Sie andere Nodes für:**
- 2D-Formen → **Colorize Easy**
- Color Grading → **Color Grading** Nodes
- Texturierte Objekte → **Materials/Shading**

## Tipps

💡 **Für 3D-Formen:** Erzeugt flache Farben ohne Schattierung  
💡 **Für Hintergründe:** Perfekt für einfache Vollfarben  
💡 **Für 2D-Formen:** Funktioniert nicht wie erwartet - nutzen Sie Colorize Easy  
💡 **Alpha-Kontrolle:** Passen Sie A-Parameter für Transparenz an

## Fehlerbehebung

**Problem: 2D-Form verschwunden, sehe nur Vollfarbe**
- Das ist normales Verhalten für diesen Node
- Nutzen Sie **Colorize Easy** stattdessen

**Problem: 3D-Form hat keine Tiefe/Schattierung**
- Dieser Node entfernt alle Beleuchtung/Schattierung
- Beabsichtigt für flachen Farb-Look
- Nutzen Sie Materialien wenn Sie Schattierung wollen

**Problem: Farbe nicht sichtbar**
- Prüfen Sie **A** (Alpha) - könnte 0.0 sein
- Setzen Sie A auf 1.0 für vollständig undurchsichtig

## Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
