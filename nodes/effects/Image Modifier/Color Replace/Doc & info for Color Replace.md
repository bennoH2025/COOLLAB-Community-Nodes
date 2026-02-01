[English](#color-replace---documentation) | [Deutsch](#color-replace---dokumentation)

---

# Color Replace - Documentation

## Overview

**Color Replace** is a precision color manipulation node that targets specific color ranges in your image and transforms them with surgical accuracy. Unlike global color adjustments, this node allows you to select a specific color and modify only that color range - changing its hue, saturation, and brightness while leaving the rest of your image untouched.

## Inspiration & Design Philosophy

Designed for targeted, selective color work:

- **Precision Targeting**: Select and modify specific colors without affecting the entire image
- **Visual Feedback**: "Show Selection" mode displays exactly what will be affected
- **Smooth Blending**: Adjustable tolerance and softness create natural-looking transitions
- **Triple Control**: Modify hue, saturation, and brightness independently
- **Non-Destructive**: Original colors outside the target range remain completely unchanged

This node brings professional color grading capabilities to Coollab, enabling the kind of selective color work seen in high-end photo and video editing.

## Key Features

### 🎯 Precise Color Selection
Target specific colors with mathematical precision:
- RGB-based color distance calculation
- Pick any color as your target
- Adjustable tolerance for similar shades
- Soft edge blending for natural results

### 🌈 Triple Transformation Control
Three independent adjustment parameters:
- **Hue Shift**: Rotate the color wheel (red → orange → yellow, etc.)
- **Saturation**: Make colors more vivid or more muted
- **Brightness**: Lighten or darken the selected range

### 👁️ Visual Selection Preview
See exactly what you're affecting:
- **Show Selection** mode displays mask in bright green
- Black areas = not selected
- Bright green = fully selected
- Gradient = partial selection (edges)
- Perfect for dialing in precise selections

### 🎨 Creative Flexibility
Endless possibilities:
- Change specific object colors without masking
- Fix color casts in specific areas
- Create stylized color looks
- Selective color grading
- Color correction without manual masking

### ⚡ Real-time Performance
- Fast color distance calculations
- Smooth HSV transformations
- Suitable for live performance and video

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to process |
| **Target Color** | sRGB | - | The color to select and replace. Use color picker to select from image. |
| **Tolerance** | 0.0 - 1.0 | 0.2 | How similar colors must be to be affected. 0 = exact match only, 1 = all colors. |
| **Softness** | 0.0 - 1.0 | 0.1 | Edge softness of the selection. 0 = hard edge, 1 = very soft transition. |
| **Show Selection** | Boolean | false | Display the selection mask in bright green for adjustment. |
| **Hue Shift** | 0.0 - 1.0 | 0.0 | Shift the hue of selected area (0 to 1 = 0° to 360°). Example: 0.33 shifts red to green. |
| **Saturation** | 0.0 - 2.0 | 1.0 | Adjust saturation: 0 = grayscale, 1 = original, 2 = hyper-saturated. |
| **Brightness** | -1.0 - 1.0 | 0.0 | Adjust brightness: negative = darker, 0 = no change, positive = lighter. |

## Creative Usage Tips

### 🎨 Color Correction Workflows

**Fix Color Casts:**
1. Load image with unwanted color cast
2. Use **color picker** on the problematic color
3. Set as **Target Color**
4. Enable **Show Selection** to verify you're targeting the right areas
5. Reduce **Saturation** to 0.3-0.7 to remove the cast
6. Or use **Hue Shift** to correct the color direction
7. Adjust **Tolerance** and **Softness** for natural blending

**Selective White Balance:**
1. Target overly warm/cool areas
2. Use **Hue Shift** to correct color temperature
3. Adjust **Saturation** if colors became too vivid
4. Keep **Tolerance** moderate (0.2-0.3) for natural results

**Remove Color Spill (from Chroma Key):**
1. After chroma keying, green/blue spill may remain
2. Set **Target Color** to the spill color (green/blue)
3. Increase **Tolerance** to catch all variations
4. Reduce **Saturation** to 0.2-0.5 to desaturate spill
5. Fine-tune with **Softness** for smooth transitions

### 🎭 Creative Color Transformations

**Change Object Colors:**
1. Pick the color of the object you want to change
2. Enable **Show Selection** - verify selection
3. Adjust **Tolerance** until object is fully selected
4. Use **Hue Shift** to change to desired color
   - Shift by ~0.16 (60°) for adjacent colors
   - Shift by ~0.33 (120°) for complementary colors
   - Shift by ~0.5 (180°) for opposite colors
5. Adjust **Saturation** to match original intensity
6. Fine-tune **Brightness** if needed

**Stylized Color Grading:**
1. Target specific color ranges (e.g., all reds)
2. Shift them dramatically with **Hue Shift**
3. Boost **Saturation** to 1.5-2.0 for intense looks
4. Create unique, stylized color palettes
5. Repeat for multiple colors to build complex grades

**Selective Desaturation:**
1. Target a specific color range
2. Set **Saturation** to 0.0-0.3
3. Creates "pop of color" effect (one color saturated, others muted)
4. Or remove distracting colors from composition

**Color Isolation Effect:**
1. Pick the color you want to keep vibrant
2. Set **very tight Tolerance** (0.1-0.15)
3. Slightly boost **Saturation** (1.2-1.5)
4. Use with global desaturation on other colors
5. Classic "single color in black & white" look

### 🌈 Advanced Techniques

**Gradual Color Transitions:**
1. Select starting color with moderate **Tolerance**
2. Use small **Hue Shift** (0.05-0.1)
3. High **Softness** (0.3-0.5)
4. Creates smooth color gradients
5. Repeat with multiple nodes for complex transitions

**Multi-Pass Color Replacement:**
1. **First pass**: Broad selection, major hue change
2. **Second pass**: Tighter selection, saturation adjustment
3. **Third pass**: Very tight, brightness fine-tuning
4. Stacking multiple Color Replace nodes allows complex transformations

**Skin Tone Correction:**
1. Carefully select skin tone with **color picker**
2. Use moderate **Tolerance** (0.15-0.25)
3. High **Softness** (0.2-0.3) for natural blending
4. Subtle **Hue Shift** (±0.02-0.05) to correct color cast
5. Slight **Saturation** adjustment (0.9-1.1)
6. Very subtle **Brightness** (±0.05-0.1)

**Environmental Color Grading:**
1. Target sky colors specifically
2. Shift hue for different times of day
3. Boost saturation for dramatic skies
4. Target foliage separately for seasonal changes
5. Target shadows/highlights with different instances

### 🔧 Using Show Selection Effectively

**The Power of Visual Feedback:**
- **Always enable** when first setting up selection
- Bright green shows exactly what will be affected
- Black shows what remains unchanged
- Gray/dim green shows partial selection (edges)

**Adjustment Workflow:**
1. Enable **Show Selection**
2. Adjust **Target Color** (pick from image)
3. Adjust **Tolerance** until desired area is bright green
4. Adjust **Softness** for smooth edges (check gray transitions)
5. Disable **Show Selection**
6. Apply your **Hue/Saturation/Brightness** changes
7. Re-enable to verify if needed

**Common Selection Patterns:**
- **Sharp object edges**: Low Softness (0.05-0.1)
- **Natural blending**: Medium Softness (0.15-0.25)
- **Artistic effects**: High Softness (0.3-0.5)
- **Precise selection**: Low Tolerance (0.1-0.2)
- **Broad selection**: High Tolerance (0.3-0.5)

## Workflow Examples

### Example 1: Change Red Car to Blue
1. Load image with red car
2. Add **Color Replace**
3. Use **color picker** on red car paint
4. Enable **Show Selection**
5. Adjust **Tolerance** to 0.25 (car should be bright green)
6. Adjust **Softness** to 0.15 (smooth edges)
7. Disable **Show Selection**
8. Set **Hue Shift** to 0.6 (shifts red to blue)
9. Adjust **Saturation** to 1.1 (maintain vibrancy)
10. Fine-tune **Brightness** to match lighting

### Example 2: Remove Green Spill from Keying
1. After chroma keying, green fringe remains on subject
2. Add **Color Replace**
3. Set **Target Color** to green using picker
4. Set **Tolerance** to 0.3 (catch all green variations)
5. Enable **Show Selection** - edges should be green
6. Set **Saturation** to 0.2 (heavily desaturate)
7. Optionally use small **Hue Shift** toward subject colors
8. Disable **Show Selection** and check result

### Example 3: Autumn Color Grading
1. Load landscape with green foliage
2. Add **Color Replace**
3. Pick green from leaves
4. Set **Tolerance** to 0.3, **Softness** to 0.2
5. **Hue Shift** to 0.08 (shift green toward yellow/orange)
6. **Saturation** to 1.3 (boost autumn colors)
7. **Brightness** to 0.1 (slightly lighten)
8. Optionally add second instance for additional colors

### Example 4: Selective Pop of Color
1. Import any colorful image
2. Add global desaturation (using Color Grading - Basic, Saturation = 0.2)
3. Add **Color Replace**
4. Pick the color you want to "pop"
5. **Tolerance**: 0.2, **Softness**: 0.15
6. **Saturation**: 1.5 (boost only this color)
7. Result: mostly desaturated image with one vibrant color

### Example 5: Sky Enhancement
1. Load landscape photo
2. Add **Color Replace**
3. Pick sky blue with **color picker**
4. **Tolerance**: 0.25, **Softness**: 0.2
5. Enable **Show Selection** - sky should be bright green
6. **Hue Shift**: -0.05 (slightly more cyan/dramatic)
7. **Saturation**: 1.4 (more vivid sky)
8. **Brightness**: -0.1 (slightly darker for drama)
9. Disable **Show Selection**

### Example 6: Fix Skin Tone Color Cast
1. Portrait with greenish/yellowish skin tones
2. Add **Color Replace**
3. Carefully pick skin tone
4. **Tolerance**: 0.2, **Softness**: 0.3 (very soft for skin)
5. Enable **Show Selection** - skin should be selected
6. **Hue Shift**: -0.03 to 0.03 (subtle correction)
7. **Saturation**: 0.95 (slightly less saturated)
8. **Brightness**: 0.02 (tiny lift)
9. Very subtle adjustments for natural results

### Example 7: Product Photography Color Change
1. Photo of product in one color
2. Add **Color Replace**
3. Pick product color
4. **Tolerance**: 0.15-0.2 (tight for product only)
5. **Softness**: 0.1 (clean edges)
6. **Hue Shift**: Adjust to desired color
   - 0.33 = shift 120° (dramatic change)
   - 0.16 = shift 60° (adjacent color)
7. Match **Saturation** and **Brightness** to original
8. Create product variations without re-shooting

## Technical Details

- **Node Type**: Color Modifier (UV→sRGB_StraightA)
- **Category**: Color Correction / Color Grading
- **Algorithm**: RGB color distance with HSV transformation
- **Color Space**: sRGB input/output, HSV for modifications
- **Selection Method**: Euclidean distance in RGB space
- **Performance**: Real-time capable, optimized

## Understanding the Algorithm

### Color Selection (Mask Creation)
```
distance = length(pixel.RGB - TargetColor.RGB)
mask = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
```

- Calculates 3D distance in RGB color cube
- Closer to target = higher mask value (more affected)
- Smoothstep creates soft edges based on Softness parameter

### Color Transformation
```
1. Convert pixel RGB to HSV
2. Apply transformations weighted by mask:
   - Hue: hsv.x = fract(hsv.x + HueShift × mask)
   - Saturation: hsv.y = hsv.y × mix(1.0, Saturation, mask)
   - Brightness: hsv.z = hsv.z + Brightness × mask
3. Convert back to RGB
```

- Transformations are **masked** - only affect selected areas
- Gradual falloff at edges due to mask values
- Preserves colors outside selection completely

### Show Selection Visualization
```
if (ShowSelection) {
    green = vec3(0.0, 1.0, 0.0)
    output = mix(black, green, mask)
}
```

- Bright green (toxic green) = high mask value
- Black = zero mask value
- Shades of green = partial mask (edges)

## Best Practices

### 🎯 Selection Accuracy
- **Use Show Selection** liberally - don't work blind
- **Start with low Tolerance**, increase until you get desired coverage
- **Adjust Softness** after Tolerance is set
- **Re-check** selection after any adjustment

### 🎨 Color Transformation
- **Start subtle** - you can always add more
- **Hue Shift**: Small changes (0.05) often better than large (0.5)
- **Saturation**: Stay in 0.8-1.2 range for natural results
- **Brightness**: ±0.1 is usually sufficient

### 🔄 Multi-Pass Strategy
- **Complex changes**: Use multiple Color Replace nodes
- **First pass**: Broad strokes
- **Second pass**: Refinement
- **Third pass**: Final details

### ⚠️ Common Mistakes to Avoid
- ❌ Tolerance too high (affects unintended colors)
- ❌ Forgetting to check Show Selection
- ❌ Extreme Hue Shifts without saturation adjustment
- ❌ Zero Softness on organic subjects (too harsh)
- ❌ Not accounting for lighting variations in target color

## Combining with Other Nodes

**Perfect Companions:**
- **⭐ Chroma Key**: Remove green spill after keying
- **🎨 Color Grading nodes**: Global adjustments + selective = perfect
- **🎭 Multiple Color Replace instances**: Complex multi-color transformations
- **🔄 2D Modifiers**: Apply effects then selectively adjust colors
- **💡 Alpha Composite**: Composite after color correction

**Advanced Workflows:**
- **Chroma Key → Color Replace**: Fix spill
- **Color Grading → Color Replace**: Global grade + selective touches
- **Color Replace × 3**: Multi-pass for complex changes
- **Masks → Color Replace**: Combine with spatial and color selection

## Troubleshooting Guide

### Problem: Selection too broad/affecting wrong areas
**Solutions**:
- ✅ Decrease **Tolerance** (make selection more strict)
- ✅ Re-pick **Target Color** more precisely
- ✅ Check **Show Selection** to see what's selected
- ✅ Consider using multiple passes with different target colors

### Problem: Hard, unnatural edges
**Solutions**:
- ✅ Increase **Softness** (0.15-0.3 for most cases)
- ✅ Check if Tolerance is too tight
- ✅ Slight increase in Tolerance + Softness = smoother

### Problem: Can't select desired color fully
**Solutions**:
- ✅ Increase **Tolerance** gradually
- ✅ Target color may have lighting variations - pick mid-tone
- ✅ May need multiple passes with different Target Colors
- ✅ Use Show Selection to identify coverage gaps

### Problem: Color change looks artificial
**Solutions**:
- ✅ Reduce **Hue Shift** amount (be more subtle)
- ✅ Adjust **Saturation** to match original intensity
- ✅ Match **Brightness** to original lighting
- ✅ Increase **Softness** for more natural blending

### Problem: Selection includes skin tones unintentionally
**Solutions**:
- ✅ Decrease **Tolerance** (skin tones are specific range)
- ✅ Re-pick Target Color more carefully
- ✅ Use low Softness (0.05-0.1) for precise selection
- ✅ May need to isolate areas with masks first

### Problem: Show Selection shows nothing
**Solutions**:
- ✅ Increase **Tolerance** (selection may be too strict)
- ✅ Verify **Target Color** is actually in the image
- ✅ Check if color picker selected correct color
- ✅ Some colors may be too dark/bright to see green overlay

## Performance Tips

- ✅ **Show Selection** has minimal performance impact
- ✅ HSV conversion is optimized
- ✅ Works well with video playback
- ✅ Can stack multiple instances without major slowdown
- ✅ Real-time capable for live performance

## Why This Node Was Created

Color correction often requires changing specific colors without affecting the entire image. Traditional global adjustments lack precision, while manual masking is time-consuming. **Color Replace** solves this by:

- ✅ **Automatic selection** based on color (no manual masking)
- ✅ **Visual feedback** with Show Selection
- ✅ **Smooth blending** with tolerance and softness
- ✅ **Triple control** over hue, saturation, brightness
- ✅ **Non-destructive** to unselected colors

This enables professional-grade selective color work that would otherwise require complex masking workflows!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#color-replace---documentation) | [Deutsch](#color-replace---dokumentation)

---

# Color Replace - Dokumentation

## Übersicht

**Color Replace** ist ein präziser Farbmanipulations-Node, der spezifische Farbbereiche in Ihrem Bild zielt und sie mit chirurgischer Genauigkeit transformiert. Im Gegensatz zu globalen Farbanpassungen ermöglicht dieser Node, eine spezifische Farbe auszuwählen und nur diesen Farbbereich zu modifizieren - Änderung von Farbton, Sättigung und Helligkeit, während der Rest Ihres Bildes unberührt bleibt.

## 🎯 Inspiration & Design-Philosophie

Entwickelt für gezielte, selektive Farbarbeit:

- **Präzisions-Targeting**: Wählen und modifizieren Sie spezifische Farben ohne das gesamte Bild zu beeinflussen
- **Visuelles Feedback**: "Show Selection"-Modus zeigt genau, was betroffen sein wird
- **Weiches Blending**: Anpassbare Toleranz und Softness erzeugen natürlich aussehende Übergänge
- **Dreifach-Kontrolle**: Modifizieren Sie Farbton, Sättigung und Helligkeit unabhängig
- **Non-Destructive**: Original-Farben außerhalb des Zielbereichs bleiben vollständig unverändert

Dieser Node bringt professionelle Color-Grading-Fähigkeiten zu Coollab und ermöglicht die Art von selektiver Farbarbeit, die in High-End-Foto- und Videobearbeitung zu sehen ist.

## ⭐ Hauptmerkmale

### 🎯 Präzise Farbauswahl
Zielen Sie spezifische Farben mit mathematischer Präzision:
- RGB-basierte Farbdistanz-Berechnung
- Wählen Sie jede Farbe als Ihr Ziel
- Anpassbare Toleranz für ähnliche Schattierungen
- Weiches Kanten-Blending für natürliche Ergebnisse

### 🌈 Dreifach-Transformations-Kontrolle
Drei unabhängige Anpassungsparameter:
- **Hue Shift**: Rotieren Sie das Farbrad (rot → orange → gelb, etc.)
- **Saturation**: Machen Sie Farben lebendiger oder gedämpfter
- **Brightness**: Hellen oder dunkeln Sie den ausgewählten Bereich

### 👁️ Visuelle Auswahl-Vorschau
Sehen Sie genau, was Sie beeinflussen:
- **Show Selection**-Modus zeigt Maske in hellem Grün
- Schwarze Bereiche = nicht ausgewählt
- Helles Grün = vollständig ausgewählt
- Gradient = teilweise Auswahl (Kanten)
- Perfekt zum Einstellen präziser Auswahlen

### 🎨 Kreative Flexibilität
Endlose Möglichkeiten:
- Ändern Sie spezifische Objektfarben ohne Maskierung
- Korrigieren Sie Farbstiche in spezifischen Bereichen
- Erstellen Sie stilisierte Farblooks
- Selektives Color Grading
- Farbkorrektur ohne manuelle Maskierung

### ⚡ Echtzeit-Performance
- Schnelle Farbdistanz-Berechnungen
- Weiche HSV-Transformationen
- Geeignet für Live-Performance und Video

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu verarbeitende Bild |
| **Target Color** | sRGB | - | Die auszuwählende und zu ersetzende Farbe. Farbwähler nutzen zur Auswahl aus Bild. |
| **Tolerance** | 0.0 - 1.0 | 0.2 | Wie ähnlich Farben sein müssen, um betroffen zu werden. 0 = nur exakte Übereinstimmung, 1 = alle Farben. |
| **Softness** | 0.0 - 1.0 | 0.1 | Kanten-Weichheit der Auswahl. 0 = harte Kante, 1 = sehr weicher Übergang. |
| **Show Selection** | Boolean | false | Zeigt die Auswahl-Maske in hellem Grün zur Anpassung an. |
| **Hue Shift** | 0.0 - 1.0 | 0.0 | Verschiebt den Farbton des ausgewählten Bereichs (0 bis 1 = 0° bis 360°). Beispiel: 0.33 verschiebt rot zu grün. |
| **Saturation** | 0.0 - 2.0 | 1.0 | Passt Sättigung an: 0 = Graustufen, 1 = Original, 2 = hyper-gesättigt. |
| **Brightness** | -1.0 - 1.0 | 0.0 | Passt Helligkeit an: negativ = dunkler, 0 = keine Änderung, positiv = heller. |

## 🎨 Kreative Nutzungstipps

### 🎨 Farbkorrektur-Workflows

**Farbstiche beheben:**
1. Laden Sie Bild mit unerwünschtem Farbstich
2. Nutzen Sie **Farbwähler** auf der problematischen Farbe
3. Setzen Sie als **Target Color**
4. Aktivieren Sie **Show Selection** zur Verifizierung der richtigen Bereiche
5. Reduzieren Sie **Saturation** auf 0.3-0.7, um Stich zu entfernen
6. Oder nutzen Sie **Hue Shift** zur Korrektur der Farbrichtung
7. Passen Sie **Tolerance** und **Softness** für natürliches Blending an

**Selektiver Weißabgleich:**
1. Zielen Sie übermäßig warme/kühle Bereiche
2. Nutzen Sie **Hue Shift** zur Korrektur der Farbtemperatur
3. Passen Sie **Saturation** an, falls Farben zu lebendig wurden
4. Halten Sie **Tolerance** moderat (0.2-0.3) für natürliche Ergebnisse

**Color Spill entfernen (von Chroma Key):**
1. Nach Chroma-Keying kann grüner/blauer Spill verbleiben
2. Setzen Sie **Target Color** auf die Spill-Farbe (grün/blau)
3. Erhöhen Sie **Tolerance**, um alle Variationen zu erfassen
4. Reduzieren Sie **Saturation** auf 0.2-0.5, um Spill zu entsättigen
5. Feinabstimmung mit **Softness** für weiche Übergänge

### 🎭 Kreative Farb-Transformationen

**Objektfarben ändern:**
1. Wählen Sie die Farbe des Objekts, das Sie ändern möchten
2. Aktivieren Sie **Show Selection** - verifizieren Sie Auswahl
3. Passen Sie **Tolerance** an, bis Objekt vollständig ausgewählt ist
4. Nutzen Sie **Hue Shift** zum Ändern zur gewünschten Farbe
   - Verschieben um ~0.16 (60°) für benachbarte Farben
   - Verschieben um ~0.33 (120°) für komplementäre Farben
   - Verschieben um ~0.5 (180°) für entgegengesetzte Farben
5. Passen Sie **Saturation** an, um Original-Intensität zu matchen
6. Feinabstimmung **Brightness** falls nötig

**Stilisiertes Color Grading:**
1. Zielen Sie spezifische Farbbereiche (z.B. alle Rottöne)
2. Verschieben Sie dramatisch mit **Hue Shift**
3. Steigern Sie **Saturation** auf 1.5-2.0 für intensive Looks
4. Erstellen Sie einzigartige, stilisierte Farbpaletten
5. Wiederholen Sie für mehrere Farben zum Aufbau komplexer Grades

**Selektive Entsättigung:**
1. Zielen Sie einen spezifischen Farbbereich
2. Setzen Sie **Saturation** auf 0.0-0.3
3. Erzeugt "Pop of Color"-Effekt (eine Farbe gesättigt, andere gedämpft)
4. Oder entfernen Sie ablenkende Farben aus Komposition

**Farbisolations-Effekt:**
1. Wählen Sie die Farbe, die Sie lebendig halten möchten
2. Setzen Sie **sehr enge Tolerance** (0.1-0.15)
3. Steigern Sie **Saturation** leicht (1.2-1.5)
4. Nutzen Sie mit globaler Entsättigung auf anderen Farben
5. Klassischer "Einzelfarbe in Schwarzweiß"-Look

### 🌈 Fortgeschrittene Techniken

**Graduelle Farbübergänge:**
1. Wählen Sie Startfarbe mit moderater **Tolerance**
2. Nutzen Sie kleinen **Hue Shift** (0.05-0.1)
3. Hohe **Softness** (0.3-0.5)
4. Erzeugt weiche Farbgradienten
5. Wiederholen Sie mit mehreren Nodes für komplexe Übergänge

**Multi-Pass-Farbersetzung:**
1. **Erster Pass**: Breite Auswahl, große Hue-Änderung
2. **Zweiter Pass**: Engere Auswahl, Sättigungs-Anpassung
3. **Dritter Pass**: Sehr eng, Helligkeits-Feinabstimmung
4. Stapeln mehrerer Color-Replace-Nodes erlaubt komplexe Transformationen

**Hauttöne-Korrektur:**
1. Wählen Sie sorgfältig Hautton mit **Farbwähler**
2. Nutzen Sie moderate **Tolerance** (0.15-0.25)
3. Hohe **Softness** (0.2-0.3) für natürliches Blending
4. Subtiler **Hue Shift** (±0.02-0.05) zur Korrektur von Farbstich
5. Leichte **Saturation**-Anpassung (0.9-1.1)
6. Sehr subtile **Brightness** (±0.05-0.1)

**Umgebungs-Color-Grading:**
1. Zielen Sie Himmelfarben speziell
2. Verschieben Sie Hue für verschiedene Tageszeiten
3. Steigern Sie Sättigung für dramatische Himmel
4. Zielen Sie Laub separat für saisonale Änderungen
5. Zielen Sie Schatten/Highlights mit verschiedenen Instanzen

### 🔧 Show Selection effektiv nutzen

**Die Kraft von visuellem Feedback:**
- **Immer aktivieren** beim ersten Einrichten der Auswahl
- Helles Grün zeigt genau, was betroffen sein wird
- Schwarz zeigt, was unverändert bleibt
- Grau/schwaches Grün zeigt teilweise Auswahl (Kanten)

**Anpassungs-Workflow:**
1. Aktivieren Sie **Show Selection**
2. Passen Sie **Target Color** an (aus Bild wählen)
3. Passen Sie **Tolerance** an, bis gewünschter Bereich hell grün ist
4. Passen Sie **Softness** für weiche Kanten an (prüfen Sie graue Übergänge)
5. Deaktivieren Sie **Show Selection**
6. Wenden Sie Ihre **Hue/Saturation/Brightness**-Änderungen an
7. Re-aktivieren zur Verifizierung falls nötig

**Häufige Auswahl-Muster:**
- **Scharfe Objektkanten**: Niedrige Softness (0.05-0.1)
- **Natürliches Blending**: Mittlere Softness (0.15-0.25)
- **Künstlerische Effekte**: Hohe Softness (0.3-0.5)
- **Präzise Auswahl**: Niedrige Tolerance (0.1-0.2)
- **Breite Auswahl**: Hohe Tolerance (0.3-0.5)

## 💡 Workflow-Beispiele

### Beispiel 1: Rotes Auto zu Blau ändern
1. Laden Sie Bild mit rotem Auto
2. Fügen Sie **Color Replace** hinzu
3. Nutzen Sie **Farbwähler** auf rotem Auto-Lack
4. Aktivieren Sie **Show Selection**
5. Passen Sie **Tolerance** auf 0.25 an (Auto sollte hell grün sein)
6. Passen Sie **Softness** auf 0.15 an (weiche Kanten)
7. Deaktivieren Sie **Show Selection**
8. Setzen Sie **Hue Shift** auf 0.6 (verschiebt rot zu blau)
9. Passen Sie **Saturation** auf 1.1 an (erhalten Sie Lebendigkeit)
10. Feinabstimmung **Brightness** zum Matchen der Beleuchtung

### Beispiel 2: Grünen Spill von Keying entfernen
1. Nach Chroma-Keying verbleibt grüner Rand am Motiv
2. Fügen Sie **Color Replace** hinzu
3. Setzen Sie **Target Color** auf Grün mit Picker
4. Setzen Sie **Tolerance** auf 0.3 (erfasse alle Grün-Variationen)
5. Aktivieren Sie **Show Selection** - Kanten sollten grün sein
6. Setzen Sie **Saturation** auf 0.2 (stark entsättigen)
7. Optional nutzen Sie kleinen **Hue Shift** Richtung Motiv-Farben
8. Deaktivieren Sie **Show Selection** und prüfen Sie Ergebnis

### Beispiel 3: Herbst-Color-Grading
1. Laden Sie Landschaft mit grünem Laub
2. Fügen Sie **Color Replace** hinzu
3. Wählen Sie Grün von Blättern
4. Setzen Sie **Tolerance** auf 0.3, **Softness** auf 0.2
5. **Hue Shift** auf 0.08 (verschiebe Grün Richtung Gelb/Orange)
6. **Saturation** auf 1.3 (steigere Herbstfarben)
7. **Brightness** auf 0.1 (leicht aufhellen)
8. Optional fügen Sie zweite Instanz für zusätzliche Farben hinzu

### Beispiel 4: Selektiver Pop of Color
1. Importieren Sie beliebiges farbenfrohes Bild
2. Fügen Sie globale Entsättigung hinzu (mit Color Grading - Basic, Saturation = 0.2)
3. Fügen Sie **Color Replace** hinzu
4. Wählen Sie die Farbe, die "poppen" soll
5. **Tolerance**: 0.2, **Softness**: 0.15
6. **Saturation**: 1.5 (steigern Sie nur diese Farbe)
7. Ergebnis: größtenteils entsättigtes Bild mit einer lebendigen Farbe

### Beispiel 5: Himmel-Verbesserung
1. Laden Sie Landschaftsfoto
2. Fügen Sie **Color Replace** hinzu
3. Wählen Sie Himmelblau mit **Farbwähler**
4. **Tolerance**: 0.25, **Softness**: 0.2
5. Aktivieren Sie **Show Selection** - Himmel sollte hell grün sein
6. **Hue Shift**: -0.05 (leicht mehr cyan/dramatisch)
7. **Saturation**: 1.4 (lebendigerer Himmel)
8. **Brightness**: -0.1 (leicht dunkler für Drama)
9. Deaktivieren Sie **Show Selection**

### Beispiel 6: Hautton-Farbstich korrigieren
1. Portrait mit grünlichen/gelblichen Hauttönen
2. Fügen Sie **Color Replace** hinzu
3. Wählen Sie sorgfältig Hautton
4. **Tolerance**: 0.2, **Softness**: 0.3 (sehr weich für Haut)
5. Aktivieren Sie **Show Selection** - Haut sollte ausgewählt sein
6. **Hue Shift**: -0.03 bis 0.03 (subtile Korrektur)
7. **Saturation**: 0.95 (leicht weniger gesättigt)
8. **Brightness**: 0.02 (winziges Anheben)
9. Sehr subtile Anpassungen für natürliche Ergebnisse

### Beispiel 7: Produktfotografie-Farbänderung
1. Foto von Produkt in einer Farbe
2. Fügen Sie **Color Replace** hinzu
3. Wählen Sie Produktfarbe
4. **Tolerance**: 0.15-0.2 (eng nur für Produkt)
5. **Softness**: 0.1 (saubere Kanten)
6. **Hue Shift**: Anpassen zur gewünschten Farbe
   - 0.33 = Verschiebung 120° (dramatische Änderung)
   - 0.16 = Verschiebung 60° (benachbarte Farbe)
7. Matchen Sie **Saturation** und **Brightness** zum Original
8. Erstellen Sie Produkt-Variationen ohne Neuaufnahme

## 🔧 Technische Details

- **Node-Typ**: Color Modifier (UV→sRGB_StraightA)
- **Kategorie**: Color Correction / Color Grading
- **Algorithmus**: RGB-Farbdistanz mit HSV-Transformation
- **Farbraum**: sRGB Input/Output, HSV für Modifikationen
- **Auswahl-Methode**: Euklidische Distanz im RGB-Raum
- **Performance**: Echtzeit-fähig, optimiert

## 🧮 Verständnis des Algorithmus

### Farbauswahl (Masken-Erstellung)
```
distance = length(pixel.RGB - TargetColor.RGB)
mask = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
```

- Berechnet 3D-Distanz im RGB-Farbwürfel
- Näher am Ziel = höherer Maskenwert (mehr betroffen)
- Smoothstep erzeugt weiche Kanten basierend auf Softness-Parameter

### Farb-Transformation
```
1. Konvertiere Pixel RGB zu HSV
2. Wende Transformationen gewichtet nach Maske an:
   - Hue: hsv.x = fract(hsv.x + HueShift × mask)
   - Saturation: hsv.y = hsv.y × mix(1.0, Saturation, mask)
   - Brightness: hsv.z = hsv.z + Brightness × mask
3. Konvertiere zurück zu RGB
```

- Transformationen sind **maskiert** - betreffen nur ausgewählte Bereiche
- Gradueller Abfall an Kanten durch Maskenwerte
- Erhält Farben außerhalb Auswahl vollständig

### Show Selection Visualisierung
```
if (ShowSelection) {
    green = vec3(0.0, 1.0, 0.0)
    output = mix(black, green, mask)
}
```

- Helles Grün (Giftgrün) = hoher Maskenwert
- Schwarz = null Maskenwert
- Grün-Schattierungen = partielle Maske (Kanten)

## 🎬 Best Practices

### 🎯 Auswahl-Genauigkeit
- **Nutzen Sie Show Selection** großzügig - arbeiten Sie nicht blind
- **Starten Sie mit niedriger Tolerance**, erhöhen Sie bis gewünschte Abdeckung
- **Passen Sie Softness an**, nachdem Tolerance gesetzt ist
- **Re-prüfen** Sie Auswahl nach jeder Anpassung

### 🎨 Farb-Transformation
- **Starten Sie subtil** - Sie können immer mehr hinzufügen
- **Hue Shift**: Kleine Änderungen (0.05) oft besser als große (0.5)
- **Saturation**: Bleiben Sie im 0.8-1.2 Bereich für natürliche Ergebnisse
- **Brightness**: ±0.1 ist normalerweise ausreichend

### 🔄 Multi-Pass-Strategie
- **Komplexe Änderungen**: Nutzen Sie mehrere Color-Replace-Nodes
- **Erster Pass**: Grobe Striche
- **Zweiter Pass**: Verfeinerung
- **Dritter Pass**: Finale Details

### ⚠️ Häufige Fehler vermeiden
- ❌ Tolerance zu hoch (betrifft unbeabsichtigte Farben)
- ❌ Vergessen, Show Selection zu prüfen
- ❌ Extreme Hue Shifts ohne Sättigungs-Anpassung
- ❌ Null Softness auf organischen Motiven (zu hart)
- ❌ Nicht berücksichtigen von Beleuchtungs-Variationen in Zielfarbe

## 🔗 Kombination mit anderen Nodes

**Perfekte Begleiter:**
- **⭐ Chroma Key**: Entfernen Sie grünen Spill nach Keying
- **🎨 Color Grading Nodes**: Globale Anpassungen + selektiv = perfekt
- **🎭 Mehrere Color Replace Instanzen**: Komplexe Multi-Farb-Transformationen
- **🔄 2D Modifier**: Wenden Sie Effekte an, dann passen Sie Farben selektiv an
- **💡 Alpha Composite**: Compositen Sie nach Farbkorrektur

**Fortgeschrittene Workflows:**
- **Chroma Key → Color Replace**: Spill beheben
- **Color Grading → Color Replace**: Globales Grade + selektive Touches
- **Color Replace × 3**: Multi-Pass für komplexe Änderungen
- **Masken → Color Replace**: Kombinieren Sie mit räumlicher und Farbauswahl

## 🔧 Fehlerbehebungs-Guide

### Problem: Auswahl zu breit/betrifft falsche Bereiche
**Lösungen**:
- ✅ Verringern Sie **Tolerance** (machen Sie Auswahl strenger)
- ✅ Wählen Sie **Target Color** präziser neu
- ✅ Prüfen Sie **Show Selection**, um zu sehen, was ausgewählt ist
- ✅ Erwägen Sie mehrere Passes mit verschiedenen Target Colors

### Problem: Harte, unnatürliche Kanten
**Lösungen**:
- ✅ Erhöhen Sie **Softness** (0.15-0.3 für die meisten Fälle)
- ✅ Prüfen Sie, ob Tolerance zu eng ist
- ✅ Leichte Erhöhung in Tolerance + Softness = weicher

### Problem: Kann gewünschte Farbe nicht vollständig auswählen
**Lösungen**:
- ✅ Erhöhen Sie **Tolerance** graduell
- ✅ Zielfarbe könnte Beleuchtungs-Variationen haben - wählen Sie Mittelton
- ✅ Könnte mehrere Passes mit verschiedenen Target Colors benötigen
- ✅ Nutzen Sie Show Selection zur Identifizierung von Abdeckungslücken

### Problem: Farbänderung sieht künstlich aus
**Lösungen**:
- ✅ Reduzieren Sie **Hue Shift**-Menge (seien Sie subtiler)
- ✅ Passen Sie **Saturation** an, um Original-Intensität zu matchen
- ✅ Matchen Sie **Brightness** zur Original-Beleuchtung
- ✅ Erhöhen Sie **Softness** für natürlicheres Blending

### Problem: Auswahl enthält unbeabsichtigt Hauttöne
**Lösungen**:
- ✅ Verringern Sie **Tolerance** (Hauttöne sind spezifischer Bereich)
- ✅ Wählen Sie Target Color sorgfältiger neu
- ✅ Nutzen Sie niedrige Softness (0.05-0.1) für präzise Auswahl
- ✅ Könnte zuerst Isolation von Bereichen mit Masken benötigen

### Problem: Show Selection zeigt nichts
**Lösungen**:
- ✅ Erhöhen Sie **Tolerance** (Auswahl könnte zu streng sein)
- ✅ Verifizieren Sie, dass **Target Color** tatsächlich im Bild ist
- ✅ Prüfen Sie, ob Farbwähler korrekte Farbe ausgewählt hat
- ✅ Einige Farben könnten zu dunkel/hell sein, um grünes Overlay zu sehen

## ⚡ Performance-Tipps

- ✅ **Show Selection** hat minimale Performance-Auswirkung
- ✅ HSV-Konversion ist optimiert
- ✅ Funktioniert gut mit Video-Wiedergabe
- ✅ Kann mehrere Instanzen stapeln ohne große Verlangsamung
- ✅ Echtzeit-fähig für Live-Performance

## 💡 Warum dieser Node erstellt wurde

Farbkorrektur erfordert oft Änderung spezifischer Farben ohne das gesamte Bild zu beeinflussen. Traditionelle globale Anpassungen fehlt Präzision, während manuelle Maskierung zeitaufwändig ist. **Color Replace** löst dies durch:

- ✅ **Automatische Auswahl** basierend auf Farbe (keine manuelle Maskierung)
- ✅ **Visuelles Feedback** mit Show Selection
- ✅ **Weiches Blending** mit Toleranz und Softness
- ✅ **Dreifach-Kontrolle** über Hue, Saturation, Brightness
- ✅ **Non-destructive** zu nicht ausgewählten Farben

Dies ermöglicht professionelle selektive Farbarbeit, die ansonsten komplexe Maskierungs-Workflows erfordern würde!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
