[English](#colorize-easy---documentation) | [Deutsch](#colorize-easy---dokumentation)

---

# Colorize Easy - Documentation

## Overview

**Colorize Easy** is a simple yet powerful colorization tool that allows you to apply color to images or shapes while preserving their structure and detail. With two distinct modes - Tint Mode and Blend Mode - this node gives you flexible control over how color is applied, making it perfect for everything from simple tinting to complex creative color effects.

## Inspiration & Design Philosophy

Designed for accessible, intuitive colorization:

- **Two Modes, One Node**: Switch between tinting and blending approaches
- **Preserve Structure**: Maintains the detail and form of your input
- **Simple Controls**: Direct RGBA color input for easy adjustment
- **Flexible Application**: Works with images, shapes, generators, and effects
- **Creative Freedom**: From subtle tints to bold color overlays

This node makes colorization accessible to everyone while providing professional-quality results for both corrective and creative work.

## Key Features

### 🎨 Dual Mode Operation
Two distinct colorization approaches:
- **Tint Mode**: Luminance-based tinting (grayscale → colored)
- **Blend Mode**: Multiply blending (colored overlay)
- Switch modes with a single checkbox

### 🖌️ Tint Mode (Luminance-Based)
Convert to grayscale, then colorize:
- Converts input to luminance values
- Applies target color based on brightness
- Perfect for black & white images
- Complete color control

### 🎭 Blend Mode (Multiply)
Colored overlay multiplication:
- Multiplies input colors with target color
- Preserves some original color information
- Like a colored gel or filter
- Natural color blending

### 🎯 Direct RGBA Control
Simple, intuitive color input:
- **R, G, B**: Red, Green, Blue channels (0-1)
- **A**: Alpha/transparency (0-1)
- Direct numeric control
- Easy to automate or animate

### ⚡ Real-time Performance
- Fast luminance calculation
- Optimized color multiplication
- Suitable for video and animation
- Interactive color adjustment

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image/shape to colorize |
| **R** | 0.0 - 1.0 | - | Red channel of target color |
| **G** | 0.0 - 1.0 | - | Green channel of target color |
| **B** | 0.0 - 1.0 | - | Blue channel of target color |
| **A** | 0.0 - 1.0 | - | Alpha channel (transparency) of target color |
| **Use Tint Mode** | Boolean | - | True = Tint Mode (luminance), False = Blend Mode (multiply) |

## Creative Usage Tips

### 🎬 Tint Mode Applications

**Colorize Black & White Photos:**
1. Import black & white photograph
2. Add **Colorize Easy**
3. **Use Tint Mode**: True (enable)
4. Set **RGB** to desired color (e.g., R: 0.9, G: 0.7, B: 0.5 for sepia)
5. **A**: 1.0 (fully opaque)
6. Result: Beautifully tinted vintage photo

**Monochrome Color Looks:**
1. Any color image
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. Set **RGB** to single-color tone (e.g., R: 0.2, G: 0.5, B: 0.8 for blue)
5. **A**: 1.0
6. Result: Monochromatic color scheme

**Duotone Effects:**
1. First instance: **Colorize Easy** in Tint Mode with dark color (shadows)
2. Blend/composite with second version
3. Second instance: **Colorize Easy** in Tint Mode with light color (highlights)
4. Creates classic duotone print effect

**Infrared Photography Simulation:**
1. Landscape or foliage image
2. **Use Tint Mode**: True
3. Set **RGB** to infrared colors (R: 1.0, G: 0.8, B: 0.8 - pinkish)
4. **A**: 1.0
5. Result: Surreal infrared look

### 🎨 Blend Mode Applications

**Colored Gel/Filter Effect:**
1. Standard color image
2. Add **Colorize Easy**
3. **Use Tint Mode**: False (Blend Mode)
4. Set **RGB** to filter color (e.g., R: 1.0, G: 0.5, B: 0.2 for warm orange)
5. **A**: 1.0
6. Result: Image through colored filter

**Sunset/Golden Hour Tint:**
1. Daytime outdoor scene
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 1.0, G: 0.8, B: 0.6 (warm golden)
4. **A**: 1.0
5. Result: Warm, golden-hour atmosphere

**Cool Night Tone:**
1. Any scene
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 0.7, G: 0.8, B: 1.0 (cool blue)
4. **A**: 1.0
5. Result: Cool, nighttime feel

**Selective Darkening:**
1. Image to darken
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 0.5, G: 0.5, B: 0.5 (gray - darkens)
4. **A**: 1.0
5. Result: Overall darkening while preserving color ratios

### 🌈 Advanced Techniques

**Gradient Colorization:**
1. Create gradient shape/generator
2. Add **Colorize Easy**
3. Choose mode based on desired effect
4. Animate **RGB** values over time
5. Creates flowing color transitions

**Shape Colorization:**
1. Geometric shapes or SDF generators
2. Add **Colorize Easy**
3. **Use Tint Mode**: True (for solid colors)
4. Set **RGB** to desired shape color
5. **A**: Adjust for transparency
6. Perfect for motion graphics

**Layer Tinting:**
1. Multiple layers in composition
2. Apply different **Colorize Easy** to each
3. Use **Tint Mode** for complete recoloring
4. Or **Blend Mode** for overlay tints
5. Creates complex color palettes

**Alpha Transparency Control:**
1. Any input
2. Add **Colorize Easy**
3. Set **RGB** as desired
4. **A**: 0.5 (semi-transparent)
5. Colorizes while adding transparency
6. Useful for overlays and compositing

### 🎛️ Mode Comparison

**When to Use Tint Mode:**
- ✅ Black & white images
- ✅ Grayscale content
- ✅ Complete color replacement
- ✅ Monochromatic looks
- ✅ When you want total color control

**When to Use Blend Mode:**
- ✅ Color images
- ✅ Subtle color shifts
- ✅ Warm/cool toning
- ✅ Filter/gel effects
- ✅ When you want to preserve some original color

**Visual Comparison:**
```
Original: Full color image

Tint Mode (Blue):
- Converts to B&W luminance
- Applies blue tint
- Result: Blue monochrome

Blend Mode (Blue):
- Keeps color info
- Multiplies with blue
- Result: Blue-tinted but color preserved
```

### 🎨 Color Recipes

**Sepia Tone (Tint Mode):**
- R: 0.9, G: 0.7, B: 0.5, A: 1.0

**Warm Sunset (Blend Mode):**
- R: 1.0, G: 0.8, B: 0.6, A: 1.0

**Cool Moonlight (Blend Mode):**
- R: 0.7, G: 0.8, B: 1.0, A: 1.0

**Vintage Cyan (Tint Mode):**
- R: 0.3, G: 0.7, B: 0.8, A: 1.0

**Magenta Gel (Blend Mode):**
- R: 1.0, G: 0.5, B: 0.8, A: 1.0

**Forest Green (Tint Mode):**
- R: 0.2, G: 0.6, B: 0.3, A: 1.0

## Workflow Examples

### Example 1: Classic Sepia Tone
1. Import black & white photograph
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. **R**: 0.9
5. **G**: 0.7
6. **B**: 0.5
7. **A**: 1.0
8. Result: Classic sepia-toned photograph

### Example 2: Warm Film Look
1. Modern digital image
2. Add **Colorize Easy**
3. **Use Tint Mode**: False (Blend Mode)
4. **R**: 1.0
5. **G**: 0.85
6. **B**: 0.7
7. **A**: 1.0
8. Result: Warm, film-like color cast

### Example 3: Monochrome Blue
1. Color portrait
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. **R**: 0.2
5. **G**: 0.4
6. **B**: 0.8
7. **A**: 1.0
8. Result: Dramatic blue monochrome

### Example 4: Night Vision Effect
1. Daytime scene
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. **R**: 0.2
5. **G**: 0.8
6. **B**: 0.2
7. **A**: 1.0
8. Combine with **Color Grading - Basic** (Brightness -0.2)
9. Result: Night vision aesthetic

### Example 5: Colored Shape
1. Circle or geometric shape generator
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. **R**: 1.0
5. **G**: 0.0
6. **B**: 0.0
7. **A**: 1.0
8. Result: Solid red shape

### Example 6: Semi-Transparent Overlay
1. Pattern or texture
2. Add **Colorize Easy**
3. **Use Tint Mode**: False (Blend Mode)
4. **R**: 0.8
5. **G**: 0.5
6. **B**: 1.0
7. **A**: 0.5 (semi-transparent)
8. Result: Purple semi-transparent overlay

### Example 7: Gradient Rainbow
1. Create horizontal gradient (black to white)
2. Add **Colorize Easy**
3. **Use Tint Mode**: True
4. Animate **RGB** values:
   - Time 0s: R:1, G:0, B:0 (red)
   - Time 1s: R:0, G:1, B:0 (green)
   - Time 2s: R:0, G:0, B:1 (blue)
5. Result: Animated rainbow gradient

## Technical Details

- **Node Type**: Color Modifier (UV→sRGB_StraightA)
- **Category**: Color Effects / Colorization
- **Modes**: Dual-mode (Tint / Blend)
- **Algorithm**: Luminance calculation + color multiplication
- **Color Space**: sRGB
- **Performance**: Real-time capable, optimized

## Understanding the Algorithm

### Tint Mode (Luminance-Based)
```
1. Calculate luminance:
   luma = input.r × 0.2126 + input.g × 0.7152 + input.b × 0.0722

2. Apply color:
   colorized = vec3(luma, luma, luma) × target_color.rgb
```

**How it works:**
- Converts input to grayscale (luminance)
- Multiplies grayscale by target color
- Brightness preserved, color completely replaced
- Perfect for B&W → Color

**Example:**
```
Input pixel: R:0.8, G:0.4, B:0.6
Luminance: 0.8×0.2126 + 0.4×0.7152 + 0.6×0.0722 = 0.599

Target color: R:1.0, G:0.5, B:0.0 (orange)
Result: (0.599, 0.599, 0.599) × (1.0, 0.5, 0.0)
      = R:0.599, G:0.299, B:0.0 (orange at that brightness)
```

### Blend Mode (Multiply)
```
colorized = input.rgb × target_color.rgb
```

**How it works:**
- Multiplies each color channel
- Preserves color relationships
- Darkens based on target color
- Like a colored filter/gel

**Example:**
```
Input pixel: R:0.8, G:0.4, B:0.6
Target color: R:1.0, G:0.5, B:0.0 (orange)

Result: (0.8, 0.4, 0.6) × (1.0, 0.5, 0.0)
      = R:0.8, G:0.2, B:0.0 (warm, shifted toward orange)
```

### Alpha Handling
```
result.alpha = input.alpha × target_alpha
```

- Multiplies input alpha with target alpha
- Allows transparency control
- Preserves original transparency relationships

## Best Practices

### 🎯 Mode Selection

**Use Tint Mode When:**
- ✅ Working with black & white images
- ✅ Want complete color control
- ✅ Creating monochromatic looks
- ✅ Colorizing shapes or generators
- ✅ Need uniform color application

**Use Blend Mode When:**
- ✅ Working with color images
- ✅ Want subtle color shifts
- ✅ Creating warm/cool tones
- ✅ Simulating colored filters
- ✅ Preserving some original color

### 💡 Color Selection Tips

**Subtle Tinting:**
- Use colors close to white (R:0.9, G:0.9, B:0.8)
- Creates gentle warmth/coolness
- Good for fine-tuning

**Bold Colorization:**
- Use saturated colors (R:1.0, G:0.0, B:0.0)
- Creates dramatic effects
- Good for creative looks

**Neutral Tones:**
- Sepia: R:0.9, G:0.7, B:0.5
- Cool gray: R:0.8, G:0.8, B:0.9
- Warm gray: R:0.9, G:0.9, B:0.8

### ⚠️ Common Mistakes to Avoid

- ❌ Using Tint Mode on color images expecting subtle change (creates monochrome)
- ❌ Setting **A** to 0.0 accidentally (makes everything transparent)
- ❌ Using very dark colors in Blend Mode (can make image too dark)
- ❌ Forgetting which mode you're in
- ❌ Not previewing before committing to values

## Combining with Other Nodes

**Essential Workflow Companions:**
- **⭐ Color Grading - Basic**: Fine-tune after colorization
- **🎨 Chroma Key**: Colorize keyed elements differently
- **💡 Color Replace**: Selective color work after colorization
- **🔧 Levels Correction**: Adjust brightness before/after
- **🌈 Multiple Colorize Easy**: Stack for complex effects

**Recommended Workflows:**

**Black & White to Sepia:**
```
B&W Image → Colorize Easy (Tint Mode, sepia color)
          → Color Grading - Basic (contrast boost)
          → Output
```

**Warm Film Look:**
```
Image → Colorize Easy (Blend Mode, warm orange)
      → Color Grading - Basic (saturation 0.9)
      → Levels Correction (lift blacks slightly)
      → Output
```

**Duotone Effect:**
```
Image → Colorize Easy #1 (Tint, dark blue)
      → Colorize Easy #2 (Tint, light yellow)
      → Blend/Composite based on luminance
      → Output
```

**Colored Shapes:**
```
Shape Generator → Colorize Easy (Tint Mode, target color)
                → Output
```

## Troubleshooting Guide

### Problem: Image became monochrome when I didn't want it
**Solutions**:
- ✅ Switch to **Blend Mode** (disable Tint Mode)
- ✅ Tint Mode converts to grayscale first - this is intentional
- ✅ Use Blend Mode for colored inputs

### Problem: Color too intense/dark
**Solutions**:
- ✅ Increase **RGB** values (closer to 1.0)
- ✅ In Blend Mode, low RGB values darken significantly
- ✅ Try lighter colors or adjust brightness after

### Problem: Everything is transparent
**Solutions**:
- ✅ Check **A** (Alpha) value - should be 1.0 for opaque
- ✅ Alpha multiplies, so 0.0 makes everything transparent
- ✅ Set **A**: 1.0

### Problem: Can't get the color I want
**Solutions**:
- ✅ Use color picker to get RGB values from reference
- ✅ Try both Tint and Blend modes - different results
- ✅ Adjust **Color Grading - Basic** after for fine-tuning
- ✅ May need multiple passes

### Problem: Blend Mode has no visible effect
**Solutions**:
- ✅ Check if **RGB** is close to 1.0, 1.0, 1.0 (white = no change)
- ✅ Use more saturated colors for visible effect
- ✅ Input image may already be close to target color

### Problem: Different results than expected between modes
**Solutions**:
- ✅ This is normal - modes work very differently
- ✅ Tint Mode: Luminance → Color (monochrome)
- ✅ Blend Mode: Color × Color (overlay)
- ✅ Experiment with both to find what works

## Performance Tips

- ✅ Very fast - simple calculations
- ✅ Real-time capable for video
- ✅ Can stack multiple instances
- ✅ Negligible performance impact
- ✅ Perfect for live visuals

## Advanced Techniques

### Animated Color Transitions
1. Use **Time** node or keyframes
2. Animate **RGB** values
3. Create flowing color changes
4. Works in both modes

### Multi-Layer Colorization
1. Duplicate image to layers
2. Apply different colors to each
3. Composite with blend modes
4. Creates complex color palettes

### Conditional Colorization
1. Use with **Select** node or conditionals
2. Apply different colors based on conditions
3. Example: Daytime vs nighttime colors
4. Switch between color schemes

### Procedural Color Generation
1. Connect to random/noise generators
2. Drive **RGB** values procedurally
3. Creates evolving color schemes
4. Great for generative art

## Why This Node Was Created

Colorization should be simple and accessible. **Colorize Easy** provides:

- ✅ **Dual modes** for flexibility (Tint vs Blend)
- ✅ **Simple RGBA controls** anyone can understand
- ✅ **Preserves structure** while changing color
- ✅ **Works with any input** (images, shapes, effects)
- ✅ **Professional results** with minimal effort
- ✅ **Real-time feedback** for interactive work

Making professional colorization accessible to everyone in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#colorize-easy---documentation) | [Deutsch](#colorize-easy---dokumentation)

---

# Colorize Easy - Dokumentation

## Übersicht

**Colorize Easy** ist ein einfaches aber wertvolles Einfärbungs-Tool, das es Ihnen ermöglicht, Farbe auf Bilder oder Formen anzuwenden während Struktur und Detail erhalten bleiben. Mit zwei unterschiedlichen Modi - Tint Mode und Blend Mode - gibt Ihnen dieser Node flexible Kontrolle darüber, wie Farbe angewendet wird, und macht ihn perfekt für alles von einfachem Tinting bis zu komplexen kreativen Farbeffekten.

## 🎯 Inspiration & Design-Philosophie

Entwickelt für rasches und einfaches wie auch intuitives Einfärben/Colorieren:

- **Zwei Modi, ein Node**: Wechseln zwischen Tinting- und Blending-Ansätzen
- **Struktur erhalten**: Erhält Detail und Form Ihres Inputs
- **Einfache Kontrollen**: Direkte RGBA-Farb-Eingabe für einfache Anpassung
- **Flexible Anwendung**: Funktioniert mit Bildern, Formen, Generatoren und Effekten
- **Kreative Freiheit**: Von subtilen Tönungen bis zu kühnen Farbüberlagerungen

Dieser Node macht Colorieren für jeden zugänglich während er professionelle Qualität für sowohl korrigierende als auch kreative Arbeit bietet.

## ⭐ Hauptmerkmale

### 🎨 Dual-Modus-Operation
Zwei unterschiedliche Färbungsansätze:
- **Tint Mode**: Luminanz-basiertes Tinting (Graustufen → gefärbt)
- **Blend Mode**: Multiply-Blending (farbiges Overlay)
- Modi wechseln mit einzelner Checkbox

### 🖌️ Tint Mode (Luminanz-basiert)
Konvertiert zu Graustufen, dann kolorisiert:
- Konvertiert Input zu Luminanzwerten
- Wendet Zielfarbe basierend auf Helligkeit an
- Perfekt für Schwarzweiß-Bilder
- Komplette Farbkontrolle

### 🎭 Blend Mode (Multiply)
Farbige Overlay-Multiplikation:
- Multipliziert Input-Farben mit Zielfarbe
- Erhält einige Original-Farbinformationen
- Wie ein farbiges Gel oder Filter
- Natürliches Farb-Blending

### 🎯 Direkte RGBA-Kontrolle
Einfache, intuitive Farb-Eingabe:
- **R, G, B**: Rot, Grün, Blau Kanäle (0-1)
- **A**: Alpha/Transparenz (0-1)
- Direkte numerische Kontrolle
- Einfach zu automatisieren oder animieren

### ⚡ Echtzeit-Performance
- Schnelle Luminanz-Berechnung
- Optimierte Farb-Multiplikation
- Geeignet für Video und Animation
- Interaktive Farb-Anpassung

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu kolorisierende Bild/Form |
| **R** | 0.0 - 1.0 | - | Rotkanal der Zielfarbe |
| **G** | 0.0 - 1.0 | - | Grünkanal der Zielfarbe |
| **B** | 0.0 - 1.0 | - | Blaukanal der Zielfarbe |
| **A** | 0.0 - 1.0 | - | Alphakanal (Transparenz) der Zielfarbe |
| **Use Tint Mode** | Boolean | - | True = Tint Mode (Luminanz), False = Blend Mode (multiply) |

## 🎨 Kreative Nutzungstipps

### 🎬 Tint Mode Anwendungen

**Schwarzweiß-Fotos kolorisieren:**
1. Importieren Sie Schwarzweiß-Fotografie
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True (aktivieren)
4. Setzen Sie **RGB** auf gewünschte Farbe (z.B. R: 0.9, G: 0.7, B: 0.5 für Sepia)
5. **A**: 1.0 (vollständig undurchsichtig)
6. Ergebnis: Wunderschön getöntes Vintage-Foto

**Monochrome Farb-Looks:**
1. Beliebiges Farbbild
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. Setzen Sie **RGB** auf Einzelfarb-Ton (z.B. R: 0.2, G: 0.5, B: 0.8 für Blau)
5. **A**: 1.0
6. Ergebnis: Monochromatisches Farbschema

**Duotone-Effekte:**
1. Erste Instanz: **Colorize Easy** in Tint Mode mit dunkler Farbe (Schatten)
2. Blend/Composite mit zweiter Version
3. Zweite Instanz: **Colorize Easy** in Tint Mode mit heller Farbe (Highlights)
4. Erzeugt klassischen Duotone-Druck-Effekt

**Infrarot-Fotografie-Simulation:**
1. Landschafts- oder Laubbild
2. **Use Tint Mode**: True
3. Setzen Sie **RGB** auf Infrarot-Farben (R: 1.0, G: 0.8, B: 0.8 - rötlich)
4. **A**: 1.0
5. Ergebnis: Surrealer Infrarot-Look

### 🎨 Blend Mode Anwendungen

**Farbiges Gel/Filter-Effekt:**
1. Standard-Farbbild
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: False (Blend Mode)
4. Setzen Sie **RGB** auf Filterfarbe (z.B. R: 1.0, G: 0.5, B: 0.2 für warm orange)
5. **A**: 1.0
6. Ergebnis: Bild durch farbiges Filter

**Sonnenuntergangs-/Golden-Hour-Tönung:**
1. Tagsüber-Außenszene
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 1.0, G: 0.8, B: 0.6 (warm golden)
4. **A**: 1.0
5. Ergebnis: Warme, Golden-Hour-Atmosphäre

**Kühler Nacht-Ton:**
1. Beliebige Szene
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 0.7, G: 0.8, B: 1.0 (kühl blau)
4. **A**: 1.0
5. Ergebnis: Kühles, nächtliches Gefühl

**Selektives Abdunkeln:**
1. Abzudunkelndes Bild
2. **Use Tint Mode**: False (Blend Mode)
3. **RGB**: R: 0.5, G: 0.5, B: 0.5 (grau - verdunkelt)
4. **A**: 1.0
5. Ergebnis: Gesamtes Abdunkeln während Farbverhältnisse erhalten bleiben

### 🌈 Fortgeschrittene Techniken

**Gradient-Kolorisierung:**
1. Erstellen Sie Gradient-Form/Generator
2. Fügen Sie **Colorize Easy** hinzu
3. Wählen Sie Modus basierend auf gewünschtem Effekt
4. Animieren Sie **RGB**-Werte über Zeit
5. Erzeugt fließende Farbübergänge

**Form-Kolorisierung:**
1. Geometrische Formen oder SDF-Generatoren
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True (für solide Farben)
4. Setzen Sie **RGB** auf gewünschte Formfarbe
5. **A**: Anpassen für Transparenz
6. Perfekt für Motion Graphics

**Layer-Tinting:**
1. Mehrere Layer in Komposition
2. Wenden Sie verschiedene **Colorize Easy** auf jeden an
3. Nutzen Sie **Tint Mode** für komplettes Umfärben
4. Oder **Blend Mode** für Overlay-Tönungen
5. Erzeugt komplexe Farbpaletten

**Alpha-Transparenz-Kontrolle:**
1. Beliebiger Input
2. Fügen Sie **Colorize Easy** hinzu
3. Setzen Sie **RGB** wie gewünscht
4. **A**: 0.5 (halbtransparent)
5. Kolorisiert während Transparenz hinzugefügt wird
6. Nützlich für Overlays und Compositing

### 🎛️ Modus-Vergleich

**Wann Tint Mode nutzen:**
- ✅ Schwarzweiß-Bilder
- ✅ Graustufen-Inhalt
- ✅ Kompletter Farbersatz
- ✅ Monochromatische Looks
- ✅ Wenn Sie totale Farbkontrolle wollen

**Wann Blend Mode nutzen:**
- ✅ Farbbilder
- ✅ Subtile Farbverschiebungen
- ✅ Warm/Kühl-Tönung
- ✅ Filter/Gel-Effekte
- ✅ Wenn Sie einige Original-Farben erhalten wollen

**Visueller Vergleich:**
```
Original: Vollfarbiges Bild

Tint Mode (Blau):
- Konvertiert zu S/W Luminanz
- Wendet blaue Tönung an
- Ergebnis: Blau monochrom

Blend Mode (Blau):
- Behält Farbinfo
- Multipliziert mit Blau
- Ergebnis: Blau-getönt aber Farbe erhalten
```

### 🎨 Farb-Rezepte

**Sepia-Ton (Tint Mode):**
- R: 0.9, G: 0.7, B: 0.5, A: 1.0

**Warmer Sonnenuntergang (Blend Mode):**
- R: 1.0, G: 0.8, B: 0.6, A: 1.0

**Kühles Mondlicht (Blend Mode):**
- R: 0.7, G: 0.8, B: 1.0, A: 1.0

**Vintage Cyan (Tint Mode):**
- R: 0.3, G: 0.7, B: 0.8, A: 1.0

**Magenta Gel (Blend Mode):**
- R: 1.0, G: 0.5, B: 0.8, A: 1.0

**Waldgrün (Tint Mode):**
- R: 0.2, G: 0.6, B: 0.3, A: 1.0

## 💡 Workflow-Beispiele

### Beispiel 1: Klassischer Sepia-Ton
1. Importieren Sie Schwarzweiß-Fotografie
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. **R**: 0.9
5. **G**: 0.7
6. **B**: 0.5
7. **A**: 1.0
8. Ergebnis: Klassisch Sepia-getöntes Foto

### Beispiel 2: Warmer Film-Look
1. Modernes Digital-Bild
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: False (Blend Mode)
4. **R**: 1.0
5. **G**: 0.85
6. **B**: 0.7
7. **A**: 1.0
8. Ergebnis: Warmer, film-artiger Farbstich

### Beispiel 3: Monochromes Blau
1. Farb-Portrait
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. **R**: 0.2
5. **G**: 0.4
6. **B**: 0.8
7. **A**: 1.0
8. Ergebnis: Dramatisches blaues Monochrom

### Beispiel 4: Nachtsicht-Effekt
1. Tagsüber-Szene
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. **R**: 0.2
5. **G**: 0.8
6. **B**: 0.2
7. **A**: 1.0
8. Kombinieren mit **Color Grading - Basic** (Brightness -0.2)
9. Ergebnis: Nachtsicht-Ästhetik

### Beispiel 5: Farbige Form
1. Kreis oder geometrischer Form-Generator
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. **R**: 1.0
5. **G**: 0.0
6. **B**: 0.0
7. **A**: 1.0
8. Ergebnis: Solide rote Form

### Beispiel 6: Halbtransparentes Overlay
1. Muster oder Textur
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: False (Blend Mode)
4. **R**: 0.8
5. **G**: 0.5
6. **B**: 1.0
7. **A**: 0.5 (halbtransparent)
8. Ergebnis: Lila halbtransparentes Overlay

### Beispiel 7: Gradient-Regenbogen
1. Erstellen Sie horizontalen Gradient (schwarz zu weiß)
2. Fügen Sie **Colorize Easy** hinzu
3. **Use Tint Mode**: True
4. Animieren Sie **RGB**-Werte:
   - Zeit 0s: R:1, G:0, B:0 (rot)
   - Zeit 1s: R:0, G:1, B:0 (grün)
   - Zeit 2s: R:0, G:0, B:1 (blau)
5. Ergebnis: Animierter Regenbogen-Gradient

## 🔧 Technische Details

- **Node-Typ**: Color Modifier (UV→sRGB_StraightA)
- **Kategorie**: Color Effects / Colorization
- **Modi**: Dual-Modus (Tint / Blend)
- **Algorithmus**: Luminanz-Berechnung + Farb-Multiplikation
- **Farbraum**: sRGB
- **Performance**: Echtzeit-fähig, optimiert

## 🧮 Verständnis des Algorithmus

### Tint Mode (Luminanz-basiert)
```
1. Berechne Luminanz:
   luma = input.r × 0.2126 + input.g × 0.7152 + input.b × 0.0722

2. Wende Farbe an:
   colorized = vec3(luma, luma, luma) × target_color.rgb
```

**Wie es funktioniert:**
- Konvertiert Input zu Graustufen (Luminanz)
- Multipliziert Graustufen mit Zielfarbe
- Helligkeit erhalten, Farbe komplett ersetzt
- Perfekt für S/W → Farbe

**Beispiel:**
```
Input-Pixel: R:0.8, G:0.4, B:0.6
Luminanz: 0.8×0.2126 + 0.4×0.7152 + 0.6×0.0722 = 0.599

Zielfarbe: R:1.0, G:0.5, B:0.0 (orange)
Ergebnis: (0.599, 0.599, 0.599) × (1.0, 0.5, 0.0)
        = R:0.599, G:0.299, B:0.0 (orange bei dieser Helligkeit)
```

### Blend Mode (Multiply)
```
colorized = input.rgb × target_color.rgb
```

**Wie es funktioniert:**
- Multipliziert jeden Farbkanal
- Erhält Farbbeziehungen
- Verdunkelt basierend auf Zielfarbe
- Wie ein farbiges Filter/Gel

**Beispiel:**
```
Input-Pixel: R:0.8, G:0.4, B:0.6
Zielfarbe: R:1.0, G:0.5, B:0.0 (orange)

Ergebnis: (0.8, 0.4, 0.6) × (1.0, 0.5, 0.0)
        = R:0.8, G:0.2, B:0.0 (warm, verschoben zu Orange)
```

### Alpha-Handhabung
```
result.alpha = input.alpha × target_alpha
```

- Multipliziert Input-Alpha mit Ziel-Alpha
- Ermöglicht Transparenz-Kontrolle
- Erhält Original-Transparenz-Beziehungen

## 🎬 Best Practices

### 🎯 Modus-Auswahl

**Nutzen Sie Tint Mode wenn:**
- ✅ Mit Schwarzweiß-Bildern arbeiten
- ✅ Komplette Farbkontrolle wollen
- ✅ Monochromatische Looks erstellen
- ✅ Formen oder Generatoren kolorisieren
- ✅ Einheitliche Farbanwendung brauchen

**Nutzen Sie Blend Mode wenn:**
- ✅ Mit Farbbildern arbeiten
- ✅ Subtile Farbverschiebungen wollen
- ✅ Warm/Kühl-Töne erstellen
- ✅ Farbige Filter simulieren
- ✅ Einige Original-Farbe erhalten wollen

### 💡 Farbauswahl-Tipps

**Subtiles Tinting:**
- Nutzen Sie Farben nah an Weiß (R:0.9, G:0.9, B:0.8)
- Erzeugt sanfte Wärme/Kühle
- Gut für Feinabstimmung

**Kühne Kolorisierung:**
- Nutzen Sie gesättigte Farben (R:1.0, G:0.0, B:0.0)
- Erzeugt dramatische Effekte
- Gut für kreative Looks

**Neutrale Töne:**
- Sepia: R:0.9, G:0.7, B:0.5
- Kühles Grau: R:0.8, G:0.8, B:0.9
- Warmes Grau: R:0.9, G:0.9, B:0.8

### ⚠️ Häufige Fehler vermeiden

- ❌ Tint Mode auf Farbbildern nutzen und subtile Änderung erwarten (erzeugt Monochrom)
- ❌ **A** versehentlich auf 0.0 setzen (macht alles transparent)
- ❌ Sehr dunkle Farben in Blend Mode nutzen (kann Bild zu dunkel machen)
- ❌ Vergessen, in welchem Modus Sie sind
- ❌ Nicht Vorschau vor Festlegung auf Werte

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **⭐ Color Grading - Basic**: Feinabstimmung nach Kolorisierung
- **🎨 Chroma Key**: Gekeyte Elemente unterschiedlich kolorisieren
- **💡 Color Replace**: Selektive Farbarbeit nach Kolorisierung
- **🔧 Levels Correction**: Helligkeit vor/nach anpassen
- **🌈 Mehrere Colorize Easy**: Stapeln für komplexe Effekte

**Empfohlene Workflows:**

**Schwarzweiß zu Sepia:**
```
S/W Bild → Colorize Easy (Tint Mode, Sepia-Farbe)
         → Color Grading - Basic (Kontrast-Boost)
         → Output
```

**Warmer Film-Look:**
```
Image → Colorize Easy (Blend Mode, warm orange)
      → Color Grading - Basic (Sättigung 0.9)
      → Levels Correction (Schwarztöne leicht heben)
      → Output
```

**Duotone-Effekt:**
```
Image → Colorize Easy #1 (Tint, dunkelblau)
      → Colorize Easy #2 (Tint, hellgelb)
      → Blend/Composite basierend auf Luminanz
      → Output
```

**Farbige Formen:**
```
Form-Generator → Colorize Easy (Tint Mode, Zielfarbe)
               → Output
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Bild wurde monochrom, obwohl ich das nicht wollte
**Lösungen**:
- ✅ Wechseln zu **Blend Mode** (Tint Mode deaktivieren)
- ✅ Tint Mode konvertiert zuerst zu Graustufen - das ist beabsichtigt
- ✅ Nutzen Sie Blend Mode für farbige Inputs

### Problem: Farbe zu intensiv/dunkel
**Lösungen**:
- ✅ **RGB**-Werte erhöhen (näher zu 1.0)
- ✅ In Blend Mode verdunkeln niedrige RGB-Werte signifikant
- ✅ Versuchen Sie hellere Farben oder passen Sie Helligkeit danach an

### Problem: Alles ist transparent
**Lösungen**:
- ✅ Prüfen Sie **A** (Alpha) Wert - sollte 1.0 für undurchsichtig sein
- ✅ Alpha multipliziert, also macht 0.0 alles transparent
- ✅ Setzen Sie **A**: 1.0

### Problem: Kann gewünschte Farbe nicht erzielen
**Lösungen**:
- ✅ Nutzen Sie Farbwähler, um RGB-Werte von Referenz zu erhalten
- ✅ Versuchen Sie beide Tint und Blend Modi - unterschiedliche Ergebnisse
- ✅ Passen Sie **Color Grading - Basic** danach für Feinabstimmung an
- ✅ Könnte mehrere Passes brauchen

### Problem: Blend Mode hat keinen sichtbaren Effekt
**Lösungen**:
- ✅ Prüfen Sie, ob **RGB** nah an 1.0, 1.0, 1.0 ist (weiß = keine Änderung)
- ✅ Nutzen Sie gesättigtere Farben für sichtbaren Effekt
- ✅ Input-Bild könnte bereits nah an Zielfarbe sein

### Problem: Unterschiedliche Ergebnisse als erwartet zwischen Modi
**Lösungen**:
- ✅ Das ist normal - Modi funktionieren sehr unterschiedlich
- ✅ Tint Mode: Luminanz → Farbe (Monochrom)
- ✅ Blend Mode: Farbe × Farbe (Overlay)
- ✅ Experimentieren Sie mit beiden, um zu finden, was funktioniert

## ⚡ Performance-Tipps

- ✅ Sehr schnell - einfache Berechnungen
- ✅ Echtzeit-fähig für Video
- ✅ Kann mehrere Instanzen stapeln
- ✅ Vernachlässigbare Performance-Auswirkung
- ✅ Perfekt für Live-Visuals

## 🎓 Fortgeschrittene Techniken

### Animierte Farbübergänge
1. Nutzen Sie **Time** Node oder Keyframes
2. Animieren Sie **RGB**-Werte
3. Erstellen Sie fließende Farbänderungen
4. Funktioniert in beiden Modi

### Multi-Layer-Kolorisierung
1. Duplizieren Sie Bild zu Layern
2. Wenden Sie verschiedene Farben auf jeden an
3. Composite mit Blend-Modi
4. Erzeugt komplexe Farbpaletten

### Konditionale Kolorisierung
1. Nutzen Sie mit **Select** Node oder Conditionals
2. Wenden Sie verschiedene Farben basierend auf Bedingungen an
3. Beispiel: Tagsüber vs Nachtzeit-Farben
4. Wechseln zwischen Farbschemata

### Prozedurale Farb-Generierung
1. Verbinden zu Random/Noise-Generatoren
2. Steuern Sie **RGB**-Werte prozedural
3. Erzeugt sich entwickelnde Farbschemata
4. Großartig für generative Kunst

## 💡 Warum dieser Node erstellt wurde

Kolorisierung sollte einfach und zugänglich sein. **Colorize Easy** bietet:

- ✅ **Dual-Modi** für Flexibilität (Tint vs Blend)
- ✅ **Einfache RGBA-Kontrollen**, die jeder verstehen kann
- ✅ **Erhält Struktur** während Farbe geändert wird
- ✅ **Funktioniert mit jedem Input** (Bilder, Formen, Effekte)
- ✅ **Professionelle Ergebnisse** mit minimalem Aufwand
- ✅ **Echtzeit-Feedback** für interaktive Arbeit

Macht professionelle Kolorisierung für jeden in Coollab zugänglich!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
