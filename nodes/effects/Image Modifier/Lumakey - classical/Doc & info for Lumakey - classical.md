[English](#lumakey---classical---documentation) | [Deutsch](#lumakey---classical---dokumentation)

---

# Lumakey - classical - Documentation

## Overview

**Lumakey - classical** is a professional luminance-based keying tool that makes brightness ranges transparent. Instead of keying out a color (like greenscreen), this node keys out specific brightness levels - perfect for removing shadows, isolating highlights, creating glows, or building dramatic silhouettes.

## Inspiration & Design Philosophy

Based on professional video production techniques:

- **Luminance-Based Keying**: Keys by brightness, not color
- **Flexible Range Control**: Tolerance and softness for precise keying
- **Invert Capability**: Key dark OR bright areas
- **Professional Tools**: Edge control, black/white point adjustment
- **Visual Feedback**: Show Matte for precise adjustment

This node brings broadcast-quality luma keying to Coollab, enabling creative and technical workflows that color-based keying can't achieve.

## Key Features

### 🔆 Luminance Keying
Remove brightness ranges:
- **Key Luminance**: Target brightness level (0 = black, 1 = white)
- **Tolerance**: How wide the brightness range is
- **Softness**: Smooth edge transitions
- **Precision**: Rec. 709 luminance calculation

### 🔄 Invert Capability
Flexible keying direction:
- **Normal**: Remove the target brightness
- **Inverted**: Keep ONLY the target brightness
- **One Click**: Toggle between modes
- **Creative Freedom**: Isolate lights OR shadows

### 🎨 Refinement Tools
Professional controls:
- **Edge Erode**: Shrink or grow the matte
- **Black Point**: Lift shadows in the result
- **White Point**: Compress highlights
- **Show Matte**: Visualize the alpha mask

### ⚡ Real-time Performance
- Fast luminance calculation
- Optimized smoothstep blending
- Suitable for video playback
- Interactive adjustment

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to key |
| **Key Luminance** | 0.0 - 1.0 | 0.5 | The brightness level to make transparent. 0 = black, 0.5 = mid-gray, 1 = white |
| **Tolerance** | 0.0 - 1.0 | 0.1 | How wide the brightness range is. 0 = exact match, higher = wider range |
| **Softness** | 0.0 - 1.0 | 0.1 | Edge softness. 0 = hard edge, 1 = very soft/feathered |
| **Show Matte** | Boolean | False | Display the alpha matte (white = opaque, black = transparent) |
| **Invert Key** | Boolean | False | Invert the key (keep the brightness range instead of removing it) |
| **Edge Erode** | -1.0 - 1.0 | 0.0 | Shrink matte edges (positive) or grow (negative). 0 = no change |
| **Black Point** | 0.0 - 1.0 | 0.0 | Lift the darkest values in the result. 0 = no change, higher = brighter shadows |
| **White Point** | 0.0 - 1.0 | 1.0 | Compress the brightest values. 1 = no change, lower = darker highlights |

## Creative Usage Tips

### 🌑 Remove Shadows

**Dark Shadow Removal:**
1. Import image with dark shadows
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.1 to 0.3 (dark range)
4. **Tolerance**: 0.2 (adjust to cover shadow range)
5. **Softness**: 0.2 (smooth edges)
6. **Invert Key**: False (remove darks)
7. **Show Matte**: True (to preview)
8. Result: Shadows become transparent

**Fine-tune with Edge Erode:**
1. After basic shadow key
2. **Edge Erode**: 0.1 to 0.3 (shrink edges)
3. Cleans up partial transparency
4. Creates cleaner cutout

### ✨ Isolate Highlights/Glows

**Extract Bright Lights:**
1. Image with lights, glows, or bright elements
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.7 to 0.9 (bright range)
4. **Tolerance**: 0.2
5. **Softness**: 0.1
6. **Invert Key**: True (KEEP the brights!)
7. Result: Only bright areas visible, rest transparent

**Glow Effect Isolation:**
1. Video with practical lights or VFX
2. **Key Luminance**: 0.8
3. **Tolerance**: 0.15
4. **Softness**: 0.3 (soft glow edges)
5. **Invert Key**: True
6. Composite over dark background
7. Result: Isolated glowing elements

### 🎭 Silhouettes & Graphics

**High Contrast Silhouette:**
1. Image with good contrast
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.5 (midtones)
4. **Tolerance**: 0.3
5. **Softness**: 0.05 (sharp)
6. **Invert Key**: False
7. Result: Removes midtones, keeps darks and brights

**Clean Background Removal:**
1. Subject on white/bright background
2. **Key Luminance**: 0.9 (near white)
3. **Tolerance**: 0.15
4. **Softness**: 0.1
5. **Invert Key**: False (remove bright)
6. Result: White background transparent

### 🌈 Creative Effects

**Partial Transparency Gradient:**
1. Any image
2. **Key Luminance**: 0.5
3. **Tolerance**: 0.8 (very wide!)
4. **Softness**: 0.5
5. Creates gradient transparency based on brightness
6. Artistic fade effect

**Double Key Composite:**
1. **First Lumakey**: Remove darks (Key Luma 0.2, Invert False)
2. **Second Lumakey**: Remove brights (Key Luma 0.8, Invert False)
3. Result: Only midtones visible
4. Great for isolating specific tonal ranges

**Vignette Effect:**
1. Image with darker edges
2. **Key Luminance**: 0.2
3. **Tolerance**: 0.3
4. **Softness**: 0.4 (very soft)
5. **Invert Key**: False
6. Result: Edges fade to transparent

### 🎬 Professional Workflows

**Matte Painting Integration:**
1. Extract sky (bright area)
2. **Key Luminance**: 0.75
3. **Tolerance**: 0.2
4. **Invert Key**: True (keep only sky)
5. Replace with new sky background
6. Composite with foreground

**Light Wrap Effect:**
1. Isolate bright edges with Lumakey
2. **Key Luminance**: 0.7
3. **Tolerance**: 0.15
4. **Softness**: 0.3
5. **Invert Key**: True
6. Blur and composite back
7. Creates natural light wrap

**Shadow Enhancement:**
1. Isolate shadows
2. **Key Luminance**: 0.2
3. **Tolerance**: 0.2
4. **Invert Key**: True (keep shadows)
5. Apply color grading to shadows only
6. Composite back
7. Selective shadow adjustment

## Workflow Examples

### Example 1: Remove White Background
1. Product photo on white background
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.95
4. **Tolerance**: 0.15
5. **Softness**: 0.05
6. **Invert Key**: False
7. **Show Matte**: True (check coverage)
8. **Edge Erode**: 0.05 (clean edges)
9. Result: Clean product cutout

### Example 2: Extract Glowing Lights
1. Night scene with lights
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.85
4. **Tolerance**: 0.2
5. **Softness**: 0.25
6. **Invert Key**: True (keep lights!)
7. Result: Only glowing elements visible

### Example 3: Shadow Removal
1. Portrait with harsh shadows
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.15
4. **Tolerance**: 0.25
5. **Softness**: 0.2
6. **Invert Key**: False
7. **Black Point**: 0.1 (lift remaining darks)
8. Result: Shadows transparent, lifted blacks

### Example 4: Midtone Isolation
1. Any image
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.5
4. **Tolerance**: 0.15
5. **Softness**: 0.1
6. **Invert Key**: True (keep mids)
7. Result: Only midtones visible

### Example 5: Dramatic Silhouette
1. Backlit subject
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.3
4. **Tolerance**: 0.4
5. **Softness**: 0.05
6. **Invert Key**: True
7. Result: Dark silhouette, bright bg transparent

### Example 6: Soft Vignette
1. Image to vignette
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.25
4. **Tolerance**: 0.3
5. **Softness**: 0.6 (very soft)
6. **Invert Key**: False
7. **Edge Erode**: -0.2 (grow matte)
8. Result: Soft edge fade

### Example 7: Highlight Recovery
1. Overexposed image
2. Add **Lumakey - classical**
3. **Key Luminance**: 0.9
4. **Tolerance**: 0.12
5. **Softness**: 0.15
6. **Invert Key**: True
7. **White Point**: 0.7 (compress)
8. Apply darker background
9. Result: Recovered highlight detail

## Technical Details

- **Node Type**: Color Modifier with Alpha (UV→sRGB_StraightA)
- **Category**: Keying / Alpha Effects
- **Algorithm**: Luminance-based distance keying
- **Luminance**: Rec. 709 standard (0.2126R + 0.7152G + 0.0722B)
- **Blending**: Smoothstep for soft edges
- **Performance**: Real-time capable

## Understanding the Algorithm

### Luminance Calculation
```
luma = 0.2126 × R + 0.7152 × G + 0.0722 × B
```
- Standard Rec. 709 coefficients
- Perceptually accurate brightness
- Matches human vision weighting

### Distance & Keying
```
distance = |luminance - Key_Luminance|
matte = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
alpha = 1.0 - matte
```

**How it works:**
- Calculate how far pixel brightness is from target
- If within Tolerance range → transparent
- Softness creates smooth transition
- Invert Key flips the logic

### Edge Erode
```
matte = clamp(matte + Edge_Erode, 0.0, 1.0)
```
- Positive: Shrinks matte (tighter key)
- Negative: Grows matte (looser key)
- Useful for cleanup

### Invert Logic
```
if (Invert_Key):
    alpha = 1.0 - alpha
```
- Normal: Remove the keyed range
- Inverted: Keep ONLY the keyed range
- Powerful for isolation

## Best Practices

### 🎯 Keying Strategy

**Start with Show Matte:**
1. Enable **Show Matte** first
2. Adjust **Key Luminance** to target brightness
3. Increase **Tolerance** until range covered
4. Add **Softness** for smooth edges
5. Disable Show Matte to see result

**Iterative Refinement:**
1. Rough key first (approximate values)
2. Fine-tune Tolerance
3. Adjust Softness for edge quality
4. Use Edge Erode for cleanup
5. Black/White Point for final polish

**Check Edges Carefully:**
- Zoom in on edge detail
- Show Matte to check coverage
- Edge Erode can save time
- Softness prevents harsh lines

### 💡 Parameter Guidelines

**Key Luminance:**
- **0.0 - 0.3**: Dark/shadow range
- **0.3 - 0.7**: Midtone range
- **0.7 - 1.0**: Bright/highlight range

**Tolerance:**
- **0.05 - 0.15**: Tight, specific range
- **0.15 - 0.3**: Medium range (most common)
- **0.3 - 0.6**: Wide range (gradient effects)
- **0.6+**: Very wide (artistic effects)

**Softness:**
- **0.0 - 0.1**: Sharp, clean edges
- **0.1 - 0.3**: Natural soft edges
- **0.3 - 0.6**: Very soft, feathered
- **0.6+**: Extreme gradient

**Edge Erode:**
- **-0.3 to -0.1**: Grow matte (more coverage)
- **0.0**: No change
- **0.1 to 0.3**: Shrink matte (tighter key)

### ⚠️ Common Mistakes to Avoid

- ❌ Tolerance too low (patchy key)
- ❌ Tolerance too high (loses too much)
- ❌ No Softness (harsh edges)
- ❌ Forgetting to use Show Matte
- ❌ Not checking Invert Key setting
- ❌ Extreme Edge Erode (artifacts)

## Combining with Other Nodes

**Essential Workflow Companions:**
- **🎨 Color Grading nodes**: Grade before keying for better results
- **🔑 Chroma Key**: Combine luma and chroma keying
- **✨ Alpha Composite**: Composite keyed elements
- **💡 Blur**: Soften edges after keying
- **🌈 Color Replace**: Fix color issues before keying

**Recommended Workflows:**

**Professional Keying:**
```
Image → Color Grading (prep)
      → Lumakey - classical
      → Edge refinement
      → Alpha Composite (with background)
      → Output
```

**Glow Extraction:**
```
Image → Lumakey (isolate brights, inverted)
      → Blur
      → Color Grading (enhance glow)
      → Alpha Composite (add mode)
      → Output
```

**Shadow Removal:**
```
Image → Lumakey (remove darks)
      → Black Point adjustment
      → Alpha Composite
      → Output
```

**Double Key Isolation:**
```
Image → Lumakey #1 (remove darks)
      → Lumakey #2 (remove brights)
      → Result: Only midtones
```

## Troubleshooting Guide

### Problem: Patchy, incomplete key
**Solutions**:
- ✅ Increase **Tolerance** (wider range)
- ✅ Add **Softness** for smoother transitions
- ✅ Use **Show Matte** to see coverage
- ✅ Adjust **Key Luminance** to better target

### Problem: Losing too much of the image
**Solutions**:
- ✅ Reduce **Tolerance** (narrower range)
- ✅ Check **Invert Key** setting (might be wrong)
- ✅ Adjust **Key Luminance** to precise target
- ✅ Use **Edge Erode** positive to shrink

### Problem: Harsh, ugly edges
**Solutions**:
- ✅ Increase **Softness** (0.2-0.4)
- ✅ Slight negative **Edge Erode** (-0.05 to -0.1)
- ✅ Check source image quality
- ✅ May need additional blur after keying

### Problem: Can't isolate highlights/glows
**Solutions**:
- ✅ Enable **Invert Key** (keep instead of remove)
- ✅ Set **Key Luminance** high (0.7-0.9)
- ✅ Adjust **Tolerance** to capture glow range
- ✅ High **Softness** for glow feathering

### Problem: Dark halo around edges
**Solutions**:
- ✅ Increase **Black Point** (lifts shadows)
- ✅ Positive **Edge Erode** (shrinks matte)
- ✅ Check if original has dark edges
- ✅ May need spill suppression (color grading)

### Problem: Show Matte doesn't help
**Solutions**:
- ✅ Make sure it's enabled (checkbox)
- ✅ White = kept, Black = removed
- ✅ Gray = partial transparency
- ✅ Use it to dial in Tolerance/Softness

### Problem: Result too dark/bright
**Solutions**:
- ✅ Adjust **Black Point** (lift darks)
- ✅ Adjust **White Point** (compress brights)
- ✅ Use Color Grading after keying
- ✅ Check composite blend mode

## Advanced Techniques

### Gradient Transparency Effects

**Luminance-Based Fade:**
1. Wide Tolerance (0.6+)
2. High Softness (0.4+)
3. Creates smooth gradient
4. Artistic fade effects

### Multi-Pass Keying

**Remove Multiple Ranges:**
1. First Lumakey: Remove darks
2. Second Lumakey: Remove brights
3. Third Lumakey: Refine edges
4. Build complex keys step-by-step

### Isolate & Enhance

**Selective Grading:**
1. Lumakey to isolate range (Invert True)
2. Apply color grading
3. Composite back
4. Affects only that brightness range

### Light Wrap Technique

**Natural Integration:**
1. Extract bright edges (high Key Luma, Inverted)
2. Blur heavily
3. Color tint to match scene
4. Composite in Add mode
5. Creates natural light wrap

### Matte Painting

**Sky Replacement:**
1. Isolate sky (usually bright)
2. Lumakey with Invert True
3. Replace with new sky
4. Edge refinement
5. Professional compositing

## Why This Node Was Created

Luminance keying is essential for professional compositing. **Lumakey - classical** provides:

- ✅ **Brightness-based keying** (not just color)
- ✅ **Invert capability** for isolation
- ✅ **Professional refinement** tools
- ✅ **Visual feedback** with Show Matte
- ✅ **Real-time performance** for interactive work
- ✅ **Flexible applications** from technical to creative

Making professional luma keying accessible in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#lumakey---classical---documentation) | [Deutsch](#lumakey---classical---dokumentation)

---

# Lumakey - classical - Dokumentation

## Übersicht

**Lumakey - classical** ist ein professionelles luminanz-basiertes Keying-Tool, das Helligkeitsbereiche transparent macht. Statt eine Farbe auszukeyen (wie Greenscreen), keyt dieser Node spezifische Helligkeitslevel aus - perfekt zum Entfernen von Schatten, Isolieren von Highlights, Erstellen von Glows oder Bauen dramatischer Silhouetten.

## 🎯 Inspiration & Design-Philosophie

Basierend auf professionellen Videoproduktions-Techniken:

- **Luminanz-basiertes Keying**: Keyt nach Helligkeit, nicht Farbe
- **Flexible Bereichs-Kontrolle**: Tolerance und Softness für präzises Keying
- **Invert-Fähigkeit**: Key dunkle ODER helle Bereiche
- **Professionelle Tools**: Kanten-Kontrolle, Schwarz/Weiß-Punkt-Anpassung
- **Visuelles Feedback**: Show Matte für präzise Anpassung

Dieser Node bringt Broadcast-Qualität Luma-Keying zu Coollab und ermöglicht kreative und technische Workflows, die farb-basiertes Keying nicht erreichen kann.

## ⭐ Hauptmerkmale

### 🔆 Luminanz-Keying
Entfernen Sie Helligkeitsbereiche:
- **Key Luminance**: Ziel-Helligkeitslevel (0 = schwarz, 1 = weiß)
- **Tolerance**: Wie breit der Helligkeitsbereich ist
- **Softness**: Weiche Kanten-Übergänge
- **Präzision**: Rec. 709 Luminanz-Berechnung

### 🔄 Invert-Fähigkeit
Flexible Keying-Richtung:
- **Normal**: Entferne die Ziel-Helligkeit
- **Invertiert**: Behalte NUR die Ziel-Helligkeit
- **Ein Klick**: Umschalten zwischen Modi
- **Kreative Freiheit**: Isoliere Lichter ODER Schatten

### 🎨 Verfeinerungs-Tools
Professionelle Kontrollen:
- **Edge Erode**: Schrumpfe oder erweitere die Maske
- **Black Point**: Hebe Schatten im Ergebnis an
- **White Point**: Komprimiere Highlights
- **Show Matte**: Visualisiere die Alpha-Maske

### ⚡ Echtzeit-Performance
- Schnelle Luminanz-Berechnung
- Optimiertes Smoothstep-Blending
- Geeignet für Video-Wiedergabe
- Interaktive Anpassung

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu keyende Bild |
| **Key Luminance** | 0.0 - 1.0 | 0.5 | Das transparent zu machende Helligkeitslevel. 0 = schwarz, 0.5 = mittelgrau, 1 = weiß |
| **Tolerance** | 0.0 - 1.0 | 0.1 | Wie breit der Helligkeitsbereich ist. 0 = exakte Übereinstimmung, höher = breiterer Bereich |
| **Softness** | 0.0 - 1.0 | 0.1 | Kanten-Weichheit. 0 = harte Kante, 1 = sehr weich/gefedert |
| **Show Matte** | Boolean | False | Zeigt die Alpha-Maske (weiß = undurchsichtig, schwarz = transparent) |
| **Invert Key** | Boolean | False | Invertiert den Key (behalte den Helligkeitsbereich statt ihn zu entfernen) |
| **Edge Erode** | -1.0 - 1.0 | 0.0 | Schrumpfe Masken-Kanten (positiv) oder erweitere (negativ). 0 = keine Änderung |
| **Black Point** | 0.0 - 1.0 | 0.0 | Hebe die dunkelsten Werte im Ergebnis an. 0 = keine Änderung, höher = hellere Schatten |
| **White Point** | 0.0 - 1.0 | 1.0 | Komprimiere die hellsten Werte. 1 = keine Änderung, niedriger = dunklere Highlights |

## 🎨 Kreative Nutzungstipps

### 🌑 Schatten Entfernen

**Dunkle Schatten-Entfernung:**
1. Importieren Sie Bild mit dunklen Schatten
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.1 bis 0.3 (dunkler Bereich)
4. **Tolerance**: 0.2 (anpassen für Schatten-Bereich)
5. **Softness**: 0.2 (glatte Kanten)
6. **Invert Key**: False (entferne Dunkles)
7. **Show Matte**: True (zur Vorschau)
8. Ergebnis: Schatten werden transparent

**Feinabstimmung mit Edge Erode:**
1. Nach Basis-Schatten-Key
2. **Edge Erode**: 0.1 bis 0.3 (schrumpfe Kanten)
3. Bereinigt partielle Transparenz
4. Erzeugt saubereren Ausschnitt

### ✨ Highlights/Glows Isolieren

**Helle Lichter Extrahieren:**
1. Bild mit Lichtern, Glows oder hellen Elementen
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.7 bis 0.9 (heller Bereich)
4. **Tolerance**: 0.2
5. **Softness**: 0.1
6. **Invert Key**: True (BEHALTE die Hellen!)
7. Ergebnis: Nur helle Bereiche sichtbar, Rest transparent

**Glow-Effekt-Isolierung:**
1. Video mit praktischen Lichtern oder VFX
2. **Key Luminance**: 0.8
3. **Tolerance**: 0.15
4. **Softness**: 0.3 (weiche Glow-Kanten)
5. **Invert Key**: True
6. Composite über dunklem Hintergrund
7. Ergebnis: Isolierte leuchtende Elemente

### 🎭 Silhouetten & Grafiken

**Hochkontrast-Silhouette:**
1. Bild mit gutem Kontrast
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.5 (Mitteltöne)
4. **Tolerance**: 0.3
5. **Softness**: 0.05 (scharf)
6. **Invert Key**: False
7. Ergebnis: Entfernt Mitteltöne, behält Dunkles und Helles

**Saubere Hintergrund-Entfernung:**
1. Subjekt auf weißem/hellem Hintergrund
2. **Key Luminance**: 0.9 (nahe weiß)
3. **Tolerance**: 0.15
4. **Softness**: 0.1
5. **Invert Key**: False (entferne hell)
6. Ergebnis: Weißer Hintergrund transparent

### 🌈 Kreative Effekte

**Partielle Transparenz-Gradient:**
1. Beliebiges Bild
2. **Key Luminance**: 0.5
3. **Tolerance**: 0.8 (sehr breit!)
4. **Softness**: 0.5
5. Erzeugt Gradient-Transparenz basierend auf Helligkeit
6. Künstlerischer Fade-Effekt

**Doppel-Key-Composite:**
1. **Erster Lumakey**: Entferne Dunkles (Key Luma 0.2, Invert False)
2. **Zweiter Lumakey**: Entferne Helles (Key Luma 0.8, Invert False)
3. Ergebnis: Nur Mitteltöne sichtbar
4. Großartig für Isolierung spezifischer Tonbereiche

**Vignetten-Effekt:**
1. Bild mit dunkleren Kanten
2. **Key Luminance**: 0.2
3. **Tolerance**: 0.3
4. **Softness**: 0.4 (sehr weich)
5. **Invert Key**: False
6. Ergebnis: Kanten verblassen zu transparent

### 🎬 Professionelle Workflows

**Matte-Painting-Integration:**
1. Extrahiere Himmel (heller Bereich)
2. **Key Luminance**: 0.75
3. **Tolerance**: 0.2
4. **Invert Key**: True (behalte nur Himmel)
5. Ersetze mit neuem Himmel-Hintergrund
6. Composite mit Vordergrund

**Light-Wrap-Effekt:**
1. Isoliere helle Kanten mit Lumakey
2. **Key Luminance**: 0.7
3. **Tolerance**: 0.15
4. **Softness**: 0.3
5. **Invert Key**: True
6. Weichzeichnen und zurück compositen
7. Erzeugt natürlichen Light Wrap

**Schatten-Verbesserung:**
1. Isoliere Schatten
2. **Key Luminance**: 0.2
3. **Tolerance**: 0.2
4. **Invert Key**: True (behalte Schatten)
5. Wende Color Grading nur auf Schatten an
6. Composite zurück
7. Selektive Schatten-Anpassung

## 💡 Workflow-Beispiele

### Beispiel 1: Weißen Hintergrund Entfernen
1. Produkt-Foto auf weißem Hintergrund
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.95
4. **Tolerance**: 0.15
5. **Softness**: 0.05
6. **Invert Key**: False
7. **Show Matte**: True (Abdeckung prüfen)
8. **Edge Erode**: 0.05 (Kanten säubern)
9. Ergebnis: Sauberer Produkt-Ausschnitt

### Beispiel 2: Leuchtende Lichter Extrahieren
1. Nachtszene mit Lichtern
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.85
4. **Tolerance**: 0.2
5. **Softness**: 0.25
6. **Invert Key**: True (behalte Lichter!)
7. Ergebnis: Nur leuchtende Elemente sichtbar

### Beispiel 3: Schatten-Entfernung
1. Portrait mit harten Schatten
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.15
4. **Tolerance**: 0.25
5. **Softness**: 0.2
6. **Invert Key**: False
7. **Black Point**: 0.1 (verbleibende Dunkeltöne heben)
8. Ergebnis: Schatten transparent, gehobene Schwarztöne

### Beispiel 4: Mittelton-Isolierung
1. Beliebiges Bild
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.5
4. **Tolerance**: 0.15
5. **Softness**: 0.1
6. **Invert Key**: True (behalte Mids)
7. Ergebnis: Nur Mitteltöne sichtbar

### Beispiel 5: Dramatische Silhouette
1. Gegenlicht-Subjekt
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.3
4. **Tolerance**: 0.4
5. **Softness**: 0.05
6. **Invert Key**: True
7. Ergebnis: Dunkle Silhouette, heller Hintergrund transparent

### Beispiel 6: Weiche Vignette
1. Zu vignettirendes Bild
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.25
4. **Tolerance**: 0.3
5. **Softness**: 0.6 (sehr weich)
6. **Invert Key**: False
7. **Edge Erode**: -0.2 (Maske erweitern)
8. Ergebnis: Weicher Kanten-Fade

### Beispiel 7: Highlight-Wiederherstellung
1. Überbelichtetes Bild
2. Fügen Sie **Lumakey - classical** hinzu
3. **Key Luminance**: 0.9
4. **Tolerance**: 0.12
5. **Softness**: 0.15
6. **Invert Key**: True
7. **White Point**: 0.7 (komprimieren)
8. Dunklen Hintergrund anwenden
9. Ergebnis: Wiederhergestelltes Highlight-Detail

## 🔧 Technische Details

- **Node-Typ**: Color Modifier with Alpha (UV→sRGB_StraightA)
- **Kategorie**: Keying / Alpha Effects
- **Algorithmus**: Luminanz-basiertes Distanz-Keying
- **Luminanz**: Rec. 709 Standard (0.2126R + 0.7152G + 0.0722B)
- **Blending**: Smoothstep für weiche Kanten
- **Performance**: Echtzeit-fähig

## 🧮 Verständnis des Algorithmus

### Luminanz-Berechnung
```
luma = 0.2126 × R + 0.7152 × G + 0.0722 × B
```
- Standard Rec. 709 Koeffizienten
- Perzeptuell genaue Helligkeit
- Passt menschliche Seh-Gewichtung

### Distanz & Keying
```
distance = |luminance - Key_Luminance|
matte = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
alpha = 1.0 - matte
```

**Wie es funktioniert:**
- Berechnet, wie weit Pixel-Helligkeit vom Ziel ist
- Falls innerhalb Tolerance-Bereich → transparent
- Softness erzeugt weichen Übergang
- Invert Key dreht die Logik um

### Edge Erode
```
matte = clamp(matte + Edge_Erode, 0.0, 1.0)
```
- Positiv: Schrumpft Maske (engerer Key)
- Negativ: Erweitert Maske (loserer Key)
- Nützlich für Bereinigung

### Invert-Logik
```
if (Invert_Key):
    alpha = 1.0 - alpha
```
- Normal: Entferne den gekeyten Bereich
- Invertiert: Behalte NUR den gekeyten Bereich
- Kraftvoll für Isolierung

## 🎬 Best Practices

### 🎯 Keying-Strategie

**Starten Sie mit Show Matte:**
1. Aktivieren Sie **Show Matte** zuerst
2. Passen Sie **Key Luminance** auf Ziel-Helligkeit an
3. Erhöhen Sie **Tolerance** bis Bereich abgedeckt
4. Fügen Sie **Softness** für glatte Kanten hinzu
5. Deaktivieren Sie Show Matte für Ergebnis

**Iterative Verfeinerung:**
1. Grober Key zuerst (ungefähre Werte)
2. Tolerance feinabstimmen
3. Softness für Kanten-Qualität anpassen
4. Edge Erode für Bereinigung nutzen
5. Black/White Point für finalen Polish

**Prüfen Sie Kanten Sorgfältig:**
- Zoomen Sie auf Kanten-Detail
- Show Matte zur Abdeckungs-Prüfung
- Edge Erode kann Zeit sparen
- Softness verhindert harte Linien

### 💡 Parameter-Richtlinien

**Key Luminance:**
- **0.0 - 0.3**: Dunkel/Schatten-Bereich
- **0.3 - 0.7**: Mittelton-Bereich
- **0.7 - 1.0**: Hell/Highlight-Bereich

**Tolerance:**
- **0.05 - 0.15**: Eng, spezifischer Bereich
- **0.15 - 0.3**: Mittlerer Bereich (am häufigsten)
- **0.3 - 0.6**: Breiter Bereich (Gradient-Effekte)
- **0.6+**: Sehr breit (künstlerische Effekte)

**Softness:**
- **0.0 - 0.1**: Scharfe, saubere Kanten
- **0.1 - 0.3**: Natürlich weiche Kanten
- **0.3 - 0.6**: Sehr weich, gefedert
- **0.6+**: Extremer Gradient

**Edge Erode:**
- **-0.3 bis -0.1**: Maske erweitern (mehr Abdeckung)
- **0.0**: Keine Änderung
- **0.1 bis 0.3**: Maske schrumpfen (engerer Key)

### ⚠️ Häufige Fehler vermeiden

- ❌ Tolerance zu niedrig (fleckiger Key)
- ❌ Tolerance zu hoch (verliert zu viel)
- ❌ Keine Softness (harte Kanten)
- ❌ Vergessen Show Matte zu nutzen
- ❌ Invert Key Einstellung nicht prüfen
- ❌ Extremes Edge Erode (Artefakte)

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **🎨 Color Grading Nodes**: Grade vor Keying für bessere Ergebnisse
- **🔑 Chroma Key**: Kombiniere Luma und Chroma Keying
- **✨ Alpha Composite**: Composite gekeyte Elemente
- **💡 Blur**: Weiche Kanten nach Keying
- **🌈 Color Replace**: Farb-Probleme vor Keying beheben

**Empfohlene Workflows:**

**Professionelles Keying:**
```
Image → Color Grading (Vorbereitung)
      → Lumakey - classical
      → Kanten-Verfeinerung
      → Alpha Composite (mit Hintergrund)
      → Output
```

**Glow-Extraktion:**
```
Image → Lumakey (isoliere Helles, invertiert)
      → Blur
      → Color Grading (Glow verstärken)
      → Alpha Composite (Add-Modus)
      → Output
```

**Schatten-Entfernung:**
```
Image → Lumakey (entferne Dunkles)
      → Black Point Anpassung
      → Alpha Composite
      → Output
```

**Doppel-Key-Isolierung:**
```
Image → Lumakey #1 (entferne Dunkles)
      → Lumakey #2 (entferne Helles)
      → Ergebnis: Nur Mitteltöne
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Fleckiger, unvollständiger Key
**Lösungen**:
- ✅ Erhöhen Sie **Tolerance** (breiterer Bereich)
- ✅ Fügen Sie **Softness** für glattere Übergänge hinzu
- ✅ Nutzen Sie **Show Matte** zur Abdeckungs-Ansicht
- ✅ Passen Sie **Key Luminance** für besseres Ziel an

### Problem: Verliere zu viel vom Bild
**Lösungen**:
- ✅ Reduzieren Sie **Tolerance** (engerer Bereich)
- ✅ Prüfen Sie **Invert Key** Einstellung (könnte falsch sein)
- ✅ Passen Sie **Key Luminance** auf präzises Ziel an
- ✅ Nutzen Sie **Edge Erode** positiv zum Schrumpfen

### Problem: Harte, hässliche Kanten
**Lösungen**:
- ✅ Erhöhen Sie **Softness** (0.2-0.4)
- ✅ Leicht negatives **Edge Erode** (-0.05 bis -0.1)
- ✅ Prüfen Sie Quellbild-Qualität
- ✅ Könnte zusätzlichen Blur nach Keying brauchen

### Problem: Kann Highlights/Glows nicht isolieren
**Lösungen**:
- ✅ Aktivieren Sie **Invert Key** (behalten statt entfernen)
- ✅ Setzen Sie **Key Luminance** hoch (0.7-0.9)
- ✅ Passen Sie **Tolerance** für Glow-Bereich-Erfassung an
- ✅ Hohe **Softness** für Glow-Federung

### Problem: Dunkler Halo um Kanten
**Lösungen**:
- ✅ Erhöhen Sie **Black Point** (hebt Schatten)
- ✅ Positives **Edge Erode** (schrumpft Maske)
- ✅ Prüfen Sie ob Original dunkle Kanten hat
- ✅ Könnte Spill Suppression brauchen (Color Grading)

### Problem: Show Matte hilft nicht
**Lösungen**:
- ✅ Stellen Sie sicher, dass es aktiviert ist (Checkbox)
- ✅ Weiß = behalten, Schwarz = entfernt
- ✅ Grau = partielle Transparenz
- ✅ Nutzen Sie es für Tolerance/Softness-Einstellung

### Problem: Ergebnis zu dunkel/hell
**Lösungen**:
- ✅ Passen Sie **Black Point** an (Dunkeltöne heben)
- ✅ Passen Sie **White Point** an (Helles komprimieren)
- ✅ Nutzen Sie Color Grading nach Keying
- ✅ Prüfen Sie Composite-Blend-Modus

## 🎓 Fortgeschrittene Techniken

### Gradient-Transparenz-Effekte

**Luminanz-basierter Fade:**
1. Breite Tolerance (0.6+)
2. Hohe Softness (0.4+)
3. Erzeugt glatten Gradient
4. Künstlerische Fade-Effekte

### Multi-Pass-Keying

**Mehrere Bereiche Entfernen:**
1. Erster Lumakey: Entferne Dunkles
2. Zweiter Lumakey: Entferne Helles
3. Dritter Lumakey: Verfeinere Kanten
4. Baue komplexe Keys Schritt-für-Schritt

### Isolieren & Verstärken

**Selektives Grading:**
1. Lumakey zur Bereichs-Isolierung (Invert True)
2. Wende Color Grading an
3. Composite zurück
4. Betrifft nur diesen Helligkeitsbereich

### Light-Wrap-Technik

**Natürliche Integration:**
1. Extrahiere helle Kanten (hohe Key Luma, Invertiert)
2. Stark weichzeichnen
3. Farbtönung passend zur Szene
4. Composite in Add-Modus
5. Erzeugt natürlichen Light Wrap

### Matte Painting

**Himmel-Ersetzung:**
1. Isoliere Himmel (normalerweise hell)
2. Lumakey mit Invert True
3. Ersetze mit neuem Himmel
4. Kanten-Verfeinerung
5. Professionelles Compositing

## 💡 Warum dieser Node erstellt wurde

Luminanz-Keying ist essentiell für professionelles Compositing. **Lumakey - classical** bietet:

- ✅ **Helligkeits-basiertes Keying** (nicht nur Farbe)
- ✅ **Invert-Fähigkeit** für Isolierung
- ✅ **Professionelle Verfeinerungs**-Tools
- ✅ **Visuelles Feedback** mit Show Matte
- ✅ **Echtzeit-Performance** für interaktive Arbeit
- ✅ **Flexible Anwendungen** von technisch bis kreativ

Macht professionelles Luma-Keying in Coollab zugänglich!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
