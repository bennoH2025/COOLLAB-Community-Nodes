[English](#color-grading---basic---documentation) | [Deutsch](#color-grading---basic---dokumentation)

---

# Color Grading - Basic - Documentation

## Overview

**Color Grading - Basic** is your essential toolkit for fundamental color correction and creative color grading. With four core controls - Brightness, Contrast, Saturation, and Hue Rotation - this node provides the foundation for both corrective color work and creative stylization. Simple yet powerful, it's the perfect starting point for any color grading workflow.

## Inspiration & Design Philosophy

Designed as the cornerstone of color grading in Coollab:

- **Essential Controls**: The four fundamental adjustments every colorist needs
- **Intuitive Interface**: Simple, straightforward parameters anyone can understand
- **Professional Results**: Industry-standard adjustments used in film and video
- **Creative Foundation**: Build complex looks by stacking multiple instances
- **Real-time Feedback**: Instant visual response for interactive grading

This node embodies the principle that powerful tools don't need to be complex. Master these four controls, and you have the foundation for professional color work.

## Key Features

### 💡 Brightness Control
Global luminance adjustment:
- Lift or lower overall brightness
- Symmetric control: -1.0 to +1.0
- Affects all tones equally
- Perfect for exposure correction

### ⚫⚪ Contrast Control
Tonal range expansion/compression:
- Increase contrast: darker darks, brighter brights
- Decrease contrast: compressed, flat look
- Pivots around midpoint (0.5)
- Creates depth and dimension

### 🌈 Saturation Control
Color intensity adjustment:
- 0.0 = Complete desaturation (grayscale)
- 1.0 = Original color intensity
- 2.0 = Maximum saturation (hyper-vivid)
- Affects all colors uniformly

### 🎨 Hue Rotation
Color wheel rotation:
- Shift all colors along the spectrum
- 0.0 to 1.0 = 0° to 360° rotation
- Creative color transformations
- Stylized looks and color effects

### ⚡ Real-time Performance
- Optimized shader calculations
- Instant visual feedback
- Suitable for video playback
- Stackable for complex grades

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to grade |
| **Brightness** | -1.0 - 1.0 | 0.0 | Brightness adjustment. Negative = darker, 0 = no change, positive = brighter. |
| **Contrast** | -1.0 - 1.0 | 0.0 | Contrast adjustment. Negative = flat/low contrast, 0 = no change, positive = high contrast. |
| **Saturation** | 0.0 - 2.0 | 1.0 | Color saturation. 0 = grayscale, 1 = original, 2 = hyper-saturated. |
| **Hue Rotation** | 0.0 - 1.0 | 0.0 | Rotate colors on the color wheel. 0 to 1 = 0° to 360° rotation. |

## Creative Usage Tips

### 🎬 Corrective Color Grading

**Basic Exposure Correction:**
1. Import underexposed/overexposed image
2. Add **Color Grading - Basic**
3. Adjust **Brightness**:
   - Underexposed: +0.1 to +0.3
   - Overexposed: -0.1 to -0.3
4. Adjust **Contrast** if image looks flat:
   - Usually +0.1 to +0.3 to restore depth
5. Check if **Saturation** needs adjustment:
   - Brightness changes can affect perceived saturation

**Flat/Washed Out Image:**
1. Image lacks depth and punch
2. Increase **Contrast**: +0.2 to +0.5
3. Boost **Saturation**: 1.2 to 1.4
4. Slightly adjust **Brightness** if needed: ±0.05
5. Creates vibrant, punchy look

**Oversaturated/Vivid Correction:**
1. Colors too intense or unrealistic
2. Reduce **Saturation**: 0.6 to 0.8
3. May need slight **Contrast** reduction: -0.1 to -0.2
4. Adjust **Brightness** for balance

### 🎨 Creative Color Grading

**Cinematic Look:**
1. Slightly reduce **Saturation**: 0.85 to 0.95
2. Increase **Contrast**: +0.15 to +0.25
3. Subtle **Brightness** adjustment: -0.05 to 0.0
4. Creates filmic, less "digital" appearance

**Vintage/Retro Style:**
1. Reduce **Saturation**: 0.7 to 0.85
2. Lower **Contrast**: -0.1 to -0.2 (slightly flat)
3. Add warmth with **Hue Rotation**: 0.02 to 0.05 (subtle shift to orange/yellow)
4. Optional: Slight **Brightness** lift: +0.05

**High-Key Bright:**
1. Increase **Brightness**: +0.2 to +0.4
2. Reduce **Contrast**: -0.1 to -0.3 (flatten shadows)
3. Slightly boost **Saturation**: 1.1 to 1.3
4. Creates airy, dreamy, bright aesthetic

**Low-Key Dark/Moody:**
1. Decrease **Brightness**: -0.2 to -0.4
2. Increase **Contrast**: +0.3 to +0.5 (deepen shadows)
3. Reduce **Saturation**: 0.7 to 0.9 (muted colors)
4. Creates dramatic, moody atmosphere

**Black & White Conversion:**
1. Set **Saturation** to 0.0 (complete desaturation)
2. Adjust **Contrast** for desired tonal range: 0.0 to +0.4
3. Adjust **Brightness** for proper exposure
4. Clean, classic black & white

**Hyper-Vivid/Pop Art:**
1. Maximize **Saturation**: 1.5 to 2.0
2. Increase **Contrast**: +0.2 to +0.4
3. May need **Brightness** adjustment to compensate
4. Bold, graphic, pop art aesthetic

### 🌈 Hue Rotation Creative Uses

**Understanding Hue Shift:**
- **0.08 (~30°)**: Subtle warm shift (more yellow/orange)
- **0.16 (~60°)**: Noticeable color change
- **0.33 (~120°)**: Complementary shift (red↔green, blue↔orange)
- **0.5 (~180°)**: Opposite colors (red↔cyan, yellow↔blue)

**Stylized Color Palettes:**
1. Shift **Hue Rotation** to 0.1-0.2
2. Creates surreal, stylized color schemes
3. All colors shift uniformly
4. Useful for music videos, artistic work

**Day to Night Effect:**
1. Reduce **Brightness**: -0.3 to -0.5
2. Increase **Contrast**: +0.2 to +0.3
3. **Hue Rotation**: 0.5 to 0.6 (shift toward blues/purples)
4. Reduce **Saturation**: 0.6 to 0.8
5. Creates night-time aesthetic from day footage

**Seasons Change:**
- **Spring**: Saturation 1.2, Hue Rotation 0.9-1.0 (toward fresh greens)
- **Summer**: Saturation 1.3, Brightness +0.1, high contrast
- **Autumn**: Hue Rotation 0.05-0.08 (shift to warm oranges), Saturation 1.1
- **Winter**: Saturation 0.7, Brightness +0.05, Contrast +0.1

### 🎛️ Layering Multiple Instances

**Two-Pass Grading:**
1. **First Pass**: Global correction
   - Fix brightness and contrast
   - Basic saturation adjustment
2. **Second Pass**: Creative look
   - Artistic saturation boost
   - Hue rotation for style
   - Final contrast enhancement

**Three-Stage Workflow:**
1. **Correction Stage**: Fix technical issues (exposure, contrast)
2. **Primary Grade**: Establish overall look and feel
3. **Creative Polish**: Final artistic touches (saturation, hue shifts)

**Extreme Transformations:**
- Stack 3-4 instances with subtle changes each
- Gradual shifts prevent harsh jumps
- Each instance adds refinement
- Build complex looks incrementally

## Workflow Examples

### Example 1: Basic Exposure & Contrast Correction
1. Import slightly dark, flat image
2. Add **Color Grading - Basic**
3. **Brightness**: +0.15 (lighten overall)
4. **Contrast**: +0.25 (add depth)
5. **Saturation**: 1.1 (slight boost)
6. **Hue Rotation**: 0.0 (no color shift)
7. Result: Well-exposed, punchy image

### Example 2: Cinematic Film Look
1. Start with digital video footage
2. Add **Color Grading - Basic**
3. **Saturation**: 0.88 (slightly muted)
4. **Contrast**: +0.18 (more dramatic)
5. **Brightness**: -0.03 (subtle darkening)
6. **Hue Rotation**: 0.0
7. Result: Filmic, less "video-like" appearance

### Example 3: Vintage Photograph Style
1. Modern digital photo
2. Add **Color Grading - Basic**
3. **Saturation**: 0.75 (faded colors)
4. **Contrast**: -0.15 (flatter, softer)
5. **Brightness**: +0.08 (slightly washed out)
6. **Hue Rotation**: 0.03 (warm shift)
7. Result: Vintage, aged photo aesthetic

### Example 4: High-Contrast Black & White
1. Color image
2. Add **Color Grading - Basic**
3. **Saturation**: 0.0 (remove all color)
4. **Contrast**: +0.35 (dramatic tones)
5. **Brightness**: +0.05 (slight lift)
6. **Hue Rotation**: 0.0 (irrelevant in B&W)
7. Result: Classic, high-contrast B&W

### Example 5: Surreal Color Transformation
1. Normal landscape photo
2. Add **Color Grading - Basic**
3. **Hue Rotation**: 0.33 (120° shift - greens become magentas)
4. **Saturation**: 1.5 (boost shifted colors)
5. **Contrast**: +0.2 (add punch)
6. **Brightness**: 0.0
7. Result: Surreal, alien landscape

### Example 6: Summer Blockbuster Look
1. Outdoor scene
2. Add **Color Grading - Basic**
3. **Saturation**: 1.25 (vivid colors)
4. **Contrast**: +0.3 (deep shadows, bright highlights)
5. **Brightness**: +0.05 (slightly lifted)
6. **Hue Rotation**: 0.02 (subtle warm shift)
7. Result: Bold, commercial look

### Example 7: Dreamy Soft Aesthetic
1. Portrait or soft scene
2. Add **Color Grading - Basic**
3. **Brightness**: +0.15 (lifted)
4. **Contrast**: -0.2 (soft, low contrast)
5. **Saturation**: 1.15 (enhanced but not harsh)
6. **Hue Rotation**: 0.0
7. Result: Soft, ethereal, dreamy look

## Technical Details

- **Node Type**: Color Modifier (UV→sRGB_StraightA)
- **Category**: Color Grading / Color Correction
- **Algorithm**: RGB brightness/contrast + HSV saturation/hue
- **Color Space**: sRGB for input/output, HSV for hue/saturation
- **Performance**: Highly optimized, real-time capable
- **Precision**: Full floating-point calculations

## Understanding the Algorithm

### Brightness
```
rgb = rgb + Brightness
```
- Simple additive adjustment
- Affects all channels equally
- Range clipped to [0.0, 1.0]

### Contrast
```
contrast_factor = 1.0 + Contrast
rgb = (rgb - 0.5) × contrast_factor + 0.5
```
- Pivots around midpoint (0.5)
- Expands or compresses tonal range
- Preserves middle gray when Contrast = 0

### Saturation & Hue (HSV)
```
1. Convert RGB to HSV
2. hsv.saturation = hsv.saturation × Saturation
3. hsv.hue = fract(hsv.hue + HueRotation)
4. Convert back to RGB
```
- Saturation: Multiplier on color intensity
- Hue Rotation: Additive shift on color wheel
- Fract() wraps hue around (0.0-1.0 range)

## Best Practices

### 🎯 Adjustment Order Matters
The internal processing order is:
1. **Brightness** (first)
2. **Contrast** (second)
3. **Saturation & Hue** (last)

**Tip**: Order affects results. Brightness before contrast means contrast pivots around the brightened midpoint.

### 💡 Start Subtle
- Begin with small adjustments (±0.1)
- Build up gradually
- Easier to add more than to undo excessive changes
- Subtle often looks more professional than extreme

### 🎨 Saturation Sweet Spots
- **Corrective**: 0.8 to 1.2
- **Creative**: 0.6 to 1.5
- **Extreme**: <0.5 or >1.5
- Most natural looks stay within 0.9-1.3

### 🌓 Contrast Guidelines
- **Subtle enhancement**: +0.1 to +0.2
- **Strong look**: +0.3 to +0.5
- **Flat/vintage**: -0.1 to -0.3
- Extreme contrast (±0.5+) usually needs brightness compensation

### 🔄 Iterative Grading
1. Start with correction (fix technical issues)
2. Add creative grade (establish look)
3. Fine-tune (refine details)
4. Review and adjust
5. Repeat if necessary

### ⚠️ Common Mistakes to Avoid
- ❌ Cranking all sliders to maximum
- ❌ Ignoring clipping (pure black/white loss)
- ❌ Oversaturation (unrealistic colors)
- ❌ Not checking result on different displays
- ❌ Forgetting to stack multiple instances for complex grades

## Combining with Other Nodes

**Essential Workflow Companions:**
- **⭐ Color Grading - Tonal**: Add after Basic for shadows/mids/highlights control
- **🎨 Color Replace**: Selective color work after global grade
- **🔑 Chroma Key + Alpha Composite**: Grade foreground/background separately
- **💡 Gamma Correction**: Fine-tune overall gamma after basic grade
- **🌈 Additional Color Grading - Basic**: Stack for complex looks

**Recommended Workflows:**

**Simple Correction:**
```
Image → Color Grading - Basic → Output
```

**Professional Grade:**
```
Image → Color Grading - Basic (correction)
      → Color Grading - Tonal (shadows/highlights)
      → Color Grading - Basic (creative look)
      → Output
```

**Selective Grading:**
```
Image → Color Grading - Basic (global)
      → Color Replace (specific colors)
      → Color Grading - Basic (final polish)
      → Output
```

**Composite Grading:**
```
Foreground → Color Grading - Basic → \
Background → Color Grading - Basic → Alpha Composite → Output
```

## Troubleshooting Guide

### Problem: Image looks washed out after adjustment
**Solutions**:
- ✅ Increase **Contrast** (+0.1 to +0.3)
- ✅ Check if **Brightness** is too high
- ✅ Boost **Saturation** (1.1 to 1.3)
- ✅ May need to reduce excessive brightness

### Problem: Colors look unnatural/fake
**Solutions**:
- ✅ Reduce **Saturation** (closer to 1.0)
- ✅ Check **Hue Rotation** - subtle shifts (0.02-0.05) usually better
- ✅ May have too much contrast - try reducing
- ✅ Review on calibrated display

### Problem: Image too dark or too bright
**Solutions**:
- ✅ Adjust **Brightness** in small increments (±0.05)
- ✅ Check if **Contrast** is compounding the issue
- ✅ If very dark: Brightness +0.2, Contrast -0.1
- ✅ If very bright: Brightness -0.2, Contrast +0.1

### Problem: Loss of detail in shadows or highlights
**Solutions**:
- ✅ Reduce **Contrast** (you've pushed too far)
- ✅ Adjust **Brightness** to compensate
- ✅ Consider using **Color Grading - Tonal** for targeted control
- ✅ May need to work with original better-exposed footage

### Problem: Black & white conversion looks flat
**Solutions**:
- ✅ Set **Saturation** to 0.0
- ✅ Increase **Contrast** significantly (+0.3 to +0.5)
- ✅ Adjust **Brightness** for proper exposure
- ✅ May need multiple passes for dramatic B&W

### Problem: Hue rotation creates weird colors
**Solutions**:
- ✅ Use smaller **Hue Rotation** values (<0.1)
- ✅ Understand you're shifting ALL colors uniformly
- ✅ For selective hue changes, use **Color Replace** instead
- ✅ Some hue values create more natural results than others

### Problem: Adjustments look different on different screens
**Solutions**:
- ✅ Work on calibrated display when possible
- ✅ Preview on target display (phone, TV, etc.)
- ✅ Avoid extreme saturation/contrast
- ✅ Test on multiple devices before finalizing

## Performance Tips

- ✅ Single instance is extremely fast
- ✅ Stacking 5+ instances may impact performance slightly
- ✅ HSV conversion is optimized
- ✅ Works great with video playback
- ✅ Real-time capable for live visuals

## Advanced Techniques

### Recreating Film Stocks
Different film stocks have characteristic looks:

**Kodak Vision3 500T (Warm, Saturated):**
- Saturation: 1.15
- Contrast: +0.12
- Hue Rotation: 0.015 (slight warm shift)
- Brightness: 0.0

**Fuji Eterna (Muted, Cinematic):**
- Saturation: 0.85
- Contrast: +0.08
- Brightness: -0.05
- Hue Rotation: 0.0

**Ilford HP5 B&W:**
- Saturation: 0.0
- Contrast: +0.25
- Brightness: +0.03
- Hue Rotation: 0.0

### Matching Scenes
When compositing or editing multiple shots:

1. **Reference Shot**: Grade your hero/reference shot first
2. **Matching**: Note exact parameter values
3. **Apply**: Use same or similar values on other shots
4. **Fine-tune**: Adjust for lighting differences
5. **Consistency**: Maintain overall look across all shots

### Color Harmony Techniques

**Complementary Colors (High Drama):**
- Hue Rotation: 0.5 (180° - opposite colors)
- High Saturation: 1.4-1.6
- Strong Contrast: +0.3

**Analogous Colors (Harmonious):**
- Hue Rotation: 0.08-0.16 (30-60° shift)
- Moderate Saturation: 1.1-1.3
- Moderate Contrast: +0.15

**Monochromatic (Unified):**
- Low Saturation: 0.7-0.9
- Any Hue Rotation
- Contrast for interest: +0.2

## Why This Node Was Created

Every colorist needs fundamental controls. **Color Grading - Basic** provides:

- ✅ **Essential four controls** every image needs
- ✅ **Simple interface** for quick adjustments
- ✅ **Professional results** with minimal complexity
- ✅ **Stackable design** for complex workflows
- ✅ **Real-time feedback** for interactive grading
- ✅ **Foundation** for all color work in Coollab

Master these basics, and you're equipped for 80% of color grading tasks!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#color-grading---basic---documentation) | [Deutsch](#color-grading---basic---dokumentation)

---

# Color Grading - Basic - Dokumentation

## Übersicht

**Color Grading - Basic** ist Ihr essentielles Toolkit für fundamentale Farbkorrektur und kreatives Color Grading. Mit vier Kernkontrollen - Brightness, Contrast, Saturation und Hue Rotation - bietet dieser Node die Grundlage für sowohl korrigierende Farbarbeit als auch kreative Stilisierung. Einfach aber kraftvoll, ist er der perfekte Startpunkt für jeden Color-Grading-Workflow.

## 🎯 Inspiration & Design-Philosophie

Entwickelt als Eckpfeiler des Color Gradings in Coollab:

- **Essentielle Kontrollen**: Die vier fundamentalen Anpassungen, die jeder Colorist braucht
- **Intuitive Oberfläche**: Einfache, straightforward Parameter, die jeder verstehen kann
- **Professionelle Ergebnisse**: Industriestandard-Anpassungen aus Film und Video
- **Kreative Grundlage**: Bauen Sie komplexe Looks durch Stapeln mehrerer Instanzen
- **Echtzeit-Feedback**: Sofortige visuelle Reaktion für interaktives Grading

Dieser Node verkörpert das Prinzip, dass kraftvolle Werkzeuge nicht komplex sein müssen. Meistern Sie diese vier Kontrollen, und Sie haben die Grundlage für professionelle Farbarbeit.

## ⭐ Hauptmerkmale

### 💡 Brightness-Kontrolle
Globale Luminanz-Anpassung:
- Heben oder senken Sie die Gesamthelligkeit
- Symmetrische Kontrolle: -1.0 bis +1.0
- Betrifft alle Töne gleichmäßig
- Perfekt für Belichtungskorrektur

### ⚫⚪ Contrast-Kontrolle
Tonbereich-Expansion/Kompression:
- Kontrast erhöhen: dunklere Dunkeltöne, hellere Helltöne
- Kontrast verringern: komprimierter, flacher Look
- Dreht um Mittelpunkt (0.5)
- Erzeugt Tiefe und Dimension

### 🌈 Saturation-Kontrolle
Farbintensitäts-Anpassung:
- 0.0 = Vollständige Entsättigung (Graustufen)
- 1.0 = Original-Farbintensität
- 2.0 = Maximale Sättigung (hyper-lebendig)
- Betrifft alle Farben gleichmäßig

### 🎨 Hue Rotation
Farbrad-Rotation:
- Verschieben Sie alle Farben entlang des Spektrums
- 0.0 bis 1.0 = 0° bis 360° Rotation
- Kreative Farb-Transformationen
- Stilisierte Looks und Farbeffekte

### ⚡ Echtzeit-Performance
- Optimierte Shader-Berechnungen
- Sofortiges visuelles Feedback
- Geeignet für Video-Wiedergabe
- Stapelbar für komplexe Grades

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu gradende Bild |
| **Brightness** | -1.0 - 1.0 | 0.0 | Helligkeits-Anpassung. Negativ = dunkler, 0 = keine Änderung, positiv = heller. |
| **Contrast** | -1.0 - 1.0 | 0.0 | Kontrast-Anpassung. Negativ = flach/niedriger Kontrast, 0 = keine Änderung, positiv = hoher Kontrast. |
| **Saturation** | 0.0 - 2.0 | 1.0 | Farbsättigung. 0 = Graustufen, 1 = Original, 2 = hyper-gesättigt. |
| **Hue Rotation** | 0.0 - 1.0 | 0.0 | Farben auf Farbrad rotieren. 0 bis 1 = 0° bis 360° Rotation. |

## 🎨 Kreative Nutzungstipps

### 🎬 Korrigierendes Color Grading

**Basis-Belichtungskorrektur:**
1. Importieren Sie unter-/überbelichtetes Bild
2. Fügen Sie **Color Grading - Basic** hinzu
3. Passen Sie **Brightness** an:
   - Unterbelichtet: +0.1 bis +0.3
   - Überbelichtet: -0.1 bis -0.3
4. Passen Sie **Contrast** an, falls Bild flach aussieht:
   - Normalerweise +0.1 bis +0.3 zur Wiederherstellung von Tiefe
5. Prüfen Sie, ob **Saturation** Anpassung braucht:
   - Helligkeitsänderungen können wahrgenommene Sättigung beeinflussen

**Flaches/Ausgewaschenes Bild:**
1. Bild fehlt Tiefe und Punch
2. Erhöhen Sie **Contrast**: +0.2 bis +0.5
3. Steigern Sie **Saturation**: 1.2 bis 1.4
4. Passen Sie **Brightness** leicht an falls nötig: ±0.05
5. Erzeugt lebendigen, knackigen Look

**Übersättigte/Lebendige Korrektur:**
1. Farben zu intensiv oder unrealistisch
2. Reduzieren Sie **Saturation**: 0.6 bis 0.8
3. Könnte leichte **Contrast**-Reduktion brauchen: -0.1 bis -0.2
4. Passen Sie **Brightness** für Balance an

### 🎨 Kreatives Color Grading

**Kinematischer Look:**
1. Reduzieren Sie **Saturation** leicht: 0.85 bis 0.95
2. Erhöhen Sie **Contrast**: +0.15 bis +0.25
3. Subtile **Brightness**-Anpassung: -0.05 bis 0.0
4. Erzeugt filmisches, weniger "digitales" Erscheinungsbild

**Vintage/Retro-Stil:**
1. Reduzieren Sie **Saturation**: 0.7 bis 0.85
2. Senken Sie **Contrast**: -0.1 bis -0.2 (leicht flach)
3. Fügen Sie Wärme mit **Hue Rotation** hinzu: 0.02 bis 0.05 (subtile Verschiebung zu Orange/Gelb)
4. Optional: Leichtes **Brightness**-Anheben: +0.05

**High-Key Hell:**
1. Erhöhen Sie **Brightness**: +0.2 bis +0.4
2. Reduzieren Sie **Contrast**: -0.1 bis -0.3 (flachere Schatten)
3. Steigern Sie **Saturation** leicht: 1.1 bis 1.3
4. Erzeugt luftige, verträumte, helle Ästhetik

**Low-Key Dunkel/Moody:**
1. Verringern Sie **Brightness**: -0.2 bis -0.4
2. Erhöhen Sie **Contrast**: +0.3 bis +0.5 (vertiefen Sie Schatten)
3. Reduzieren Sie **Saturation**: 0.7 bis 0.9 (gedämpfte Farben)
4. Erzeugt dramatische, stimmungsvolle Atmosphäre

**Schwarzweiß-Konversion:**
1. Setzen Sie **Saturation** auf 0.0 (vollständige Entsättigung)
2. Passen Sie **Contrast** für gewünschten Tonbereich an: 0.0 bis +0.4
3. Passen Sie **Brightness** für korrekte Belichtung an
4. Sauberes, klassisches Schwarzweiß

**Hyper-Lebendig/Pop-Art:**
1. Maximieren Sie **Saturation**: 1.5 bis 2.0
2. Erhöhen Sie **Contrast**: +0.2 bis +0.4
3. Könnte **Brightness**-Anpassung zur Kompensation brauchen
4. Kühne, grafische, Pop-Art-Ästhetik

### 🌈 Hue Rotation Kreative Nutzung

**Hue-Shift verstehen:**
- **0.08 (~30°)**: Subtile warme Verschiebung (mehr Gelb/Orange)
- **0.16 (~60°)**: Merkliche Farbänderung
- **0.33 (~120°)**: Komplementäre Verschiebung (Rot↔Grün, Blau↔Orange)
- **0.5 (~180°)**: Entgegengesetzte Farben (Rot↔Cyan, Gelb↔Blau)

**Stilisierte Farbpaletten:**
1. Verschieben Sie **Hue Rotation** auf 0.1-0.2
2. Erzeugt surreale, stilisierte Farbschemata
3. Alle Farben verschieben gleichmäßig
4. Nützlich für Musikvideos, künstlerische Arbeit

**Tag-zu-Nacht-Effekt:**
1. Reduzieren Sie **Brightness**: -0.3 bis -0.5
2. Erhöhen Sie **Contrast**: +0.2 bis +0.3
3. **Hue Rotation**: 0.5 bis 0.6 (Verschiebung zu Blau/Lila)
4. Reduzieren Sie **Saturation**: 0.6 bis 0.8
5. Erzeugt nächtliche Ästhetik aus Tag-Footage

**Jahreszeiten-Wechsel:**
- **Frühling**: Saturation 1.2, Hue Rotation 0.9-1.0 (zu frischen Grüntönen)
- **Sommer**: Saturation 1.3, Brightness +0.1, hoher Kontrast
- **Herbst**: Hue Rotation 0.05-0.08 (Verschiebung zu warmen Orangetönen), Saturation 1.1
- **Winter**: Saturation 0.7, Brightness +0.05, Contrast +0.1

### 🎛️ Mehrere Instanzen schichten

**Zwei-Pass-Grading:**
1. **Erster Pass**: Globale Korrektur
   - Beheben Sie Helligkeit und Kontrast
   - Basis-Sättigungs-Anpassung
2. **Zweiter Pass**: Kreativer Look
   - Künstlerische Sättigungs-Steigerung
   - Hue-Rotation für Stil
   - Finale Kontrast-Verbesserung

**Dreistufen-Workflow:**
1. **Korrektur-Stufe**: Technische Probleme beheben (Belichtung, Kontrast)
2. **Primäres Grade**: Gesamtlook etablieren
3. **Kreativer Polish**: Finale künstlerische Touches (Sättigung, Hue-Shifts)

**Extreme Transformationen:**
- Stapeln Sie 3-4 Instanzen mit jeweils subtilen Änderungen
- Graduelle Verschiebungen verhindern harte Sprünge
- Jede Instanz fügt Verfeinerung hinzu
- Bauen Sie komplexe Looks inkrementell auf

## 💡 Workflow-Beispiele

### Beispiel 1: Basis-Belichtungs- & Kontrast-Korrektur
1. Importieren Sie leicht dunkles, flaches Bild
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Brightness**: +0.15 (aufhellen insgesamt)
4. **Contrast**: +0.25 (Tiefe hinzufügen)
5. **Saturation**: 1.1 (leichte Steigerung)
6. **Hue Rotation**: 0.0 (keine Farbverschiebung)
7. Ergebnis: Gut belichtetes, knackiges Bild

### Beispiel 2: Kinematischer Film-Look
1. Starten Sie mit digitaler Video-Footage
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Saturation**: 0.88 (leicht gedämpft)
4. **Contrast**: +0.18 (dramatischer)
5. **Brightness**: -0.03 (subtiles Abdunkeln)
6. **Hue Rotation**: 0.0
7. Ergebnis: Filmisches, weniger "video-artiges" Erscheinungsbild

### Beispiel 3: Vintage-Foto-Stil
1. Modernes Digital-Foto
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Saturation**: 0.75 (verblasste Farben)
4. **Contrast**: -0.15 (flacher, weicher)
5. **Brightness**: +0.08 (leicht ausgewaschen)
6. **Hue Rotation**: 0.03 (warme Verschiebung)
7. Ergebnis: Vintage, gealterte Foto-Ästhetik

### Beispiel 4: Hochkontrast-Schwarzweiß
1. Farbbild
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Saturation**: 0.0 (alle Farbe entfernen)
4. **Contrast**: +0.35 (dramatische Töne)
5. **Brightness**: +0.05 (leichtes Anheben)
6. **Hue Rotation**: 0.0 (irrelevant in S/W)
7. Ergebnis: Klassisches, hochkontrast S/W

### Beispiel 5: Surreale Farb-Transformation
1. Normale Landschafts-Foto
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Hue Rotation**: 0.33 (120° Verschiebung - Grüntöne werden Magentas)
4. **Saturation**: 1.5 (steigern Sie verschobene Farben)
5. **Contrast**: +0.2 (Punch hinzufügen)
6. **Brightness**: 0.0
7. Ergebnis: Surreale, außerirdische Landschaft

### Beispiel 6: Sommer-Blockbuster-Look
1. Außenszene
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Saturation**: 1.25 (lebendige Farben)
4. **Contrast**: +0.3 (tiefe Schatten, helle Highlights)
5. **Brightness**: +0.05 (leicht angehoben)
6. **Hue Rotation**: 0.02 (subtile warme Verschiebung)
7. Ergebnis: Kühner, kommerzieller Look

### Beispiel 7: Verträumte Weiche Ästhetik
1. Portrait oder weiche Szene
2. Fügen Sie **Color Grading - Basic** hinzu
3. **Brightness**: +0.15 (angehoben)
4. **Contrast**: -0.2 (weich, niedriger Kontrast)
5. **Saturation**: 1.15 (verstärkt aber nicht hart)
6. **Hue Rotation**: 0.0
7. Ergebnis: Weicher, ätherischer, verträumter Look

## 🔧 Technische Details

- **Node-Typ**: Color Modifier (UV→sRGB_StraightA)
- **Kategorie**: Color Grading / Color Correction
- **Algorithmus**: RGB Brightness/Contrast + HSV Saturation/Hue
- **Farbraum**: sRGB für Input/Output, HSV für Hue/Saturation
- **Performance**: Hoch optimiert, echtzeit-fähig
- **Präzision**: Vollständige Fließkomma-Berechnungen

## 🧮 Verständnis des Algorithmus

### Brightness
```
rgb = rgb + Brightness
```
- Einfache additive Anpassung
- Betrifft alle Kanäle gleichmäßig
- Bereich beschnitten auf [0.0, 1.0]

### Contrast
```
contrast_factor = 1.0 + Contrast
rgb = (rgb - 0.5) × contrast_factor + 0.5
```
- Dreht um Mittelpunkt (0.5)
- Expandiert oder komprimiert Tonbereich
- Erhält mittleres Grau wenn Contrast = 0

### Saturation & Hue (HSV)
```
1. Konvertiere RGB zu HSV
2. hsv.saturation = hsv.saturation × Saturation
3. hsv.hue = fract(hsv.hue + HueRotation)
4. Konvertiere zurück zu RGB
```
- Saturation: Multiplikator auf Farbintensität
- Hue Rotation: Additive Verschiebung auf Farbrad
- Fract() wickelt Hue um (0.0-1.0 Bereich)

## 🎬 Best Practices

### 🎯 Anpassungs-Reihenfolge zählt
Die interne Verarbeitungs-Reihenfolge ist:
1. **Brightness** (zuerst)
2. **Contrast** (zweite)
3. **Saturation & Hue** (zuletzt)

**Tipp**: Reihenfolge beeinflusst Ergebnisse. Brightness vor Contrast bedeutet, Kontrast dreht um den aufgehellten Mittelpunkt.

### 💡 Starten Sie subtil
- Beginnen Sie mit kleinen Anpassungen (±0.1)
- Bauen Sie graduell auf
- Einfacher mehr hinzuzufügen als exzessive Änderungen rückgängig zu machen
- Subtil sieht oft professioneller aus als extrem

### 🎨 Saturation Sweet Spots
- **Korrigierend**: 0.8 bis 1.2
- **Kreativ**: 0.6 bis 1.5
- **Extrem**: <0.5 oder >1.5
- Natürlichste Looks bleiben innerhalb 0.9-1.3

### 🌓 Contrast-Richtlinien
- **Subtile Verbesserung**: +0.1 bis +0.2
- **Starker Look**: +0.3 bis +0.5
- **Flach/Vintage**: -0.1 bis -0.3
- Extremer Kontrast (±0.5+) braucht normalerweise Brightness-Kompensation

### 🔄 Iteratives Grading
1. Starten Sie mit Korrektur (technische Probleme beheben)
2. Fügen Sie kreatives Grade hinzu (Look etablieren)
3. Feinabstimmung (Details verfeinern)
4. Überprüfen und anpassen
5. Wiederholen falls nötig

### ⚠️ Häufige Fehler vermeiden
- ❌ Alle Slider auf Maximum drehen
- ❌ Clipping ignorieren (Verlust von reinem Schwarz/Weiß)
- ❌ Übersättigung (unrealistische Farben)
- ❌ Ergebnis nicht auf verschiedenen Displays prüfen
- ❌ Vergessen, mehrere Instanzen für komplexe Grades zu stapeln

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **⭐ Color Grading - Tonal**: Nach Basic hinzufügen für Schatten/Mids/Highlights-Kontrolle
- **🎨 Color Replace**: Selektive Farbarbeit nach globalem Grade
- **🔑 Chroma Key + Alpha Composite**: Vordergrund/Hintergrund separat graden
- **💡 Gamma Correction**: Gesamtes Gamma nach Basis-Grade feinabstimmen
- **🌈 Zusätzliche Color Grading - Basic**: Stapeln für komplexe Looks

**Empfohlene Workflows:**

**Einfache Korrektur:**
```
Image → Color Grading - Basic → Output
```

**Professionelles Grade:**
```
Image → Color Grading - Basic (Korrektur)
      → Color Grading - Tonal (Schatten/Highlights)
      → Color Grading - Basic (kreativer Look)
      → Output
```

**Selektives Grading:**
```
Image → Color Grading - Basic (global)
      → Color Replace (spezifische Farben)
      → Color Grading - Basic (finaler Polish)
      → Output
```

**Composite-Grading:**
```
Foreground → Color Grading - Basic → \
Background → Color Grading - Basic → Alpha Composite → Output
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Bild sieht nach Anpassung ausgewaschen aus
**Lösungen**:
- ✅ Erhöhen Sie **Contrast** (+0.1 bis +0.3)
- ✅ Prüfen Sie, ob **Brightness** zu hoch ist
- ✅ Steigern Sie **Saturation** (1.1 bis 1.3)
- ✅ Könnte exzessive Helligkeit reduzieren müssen

### Problem: Farben sehen unnatürlich/fake aus
**Lösungen**:
- ✅ Reduzieren Sie **Saturation** (näher zu 1.0)
- ✅ Prüfen Sie **Hue Rotation** - subtile Verschiebungen (0.02-0.05) normalerweise besser
- ✅ Könnte zu viel Kontrast haben - versuchen Sie zu reduzieren
- ✅ Überprüfen Sie auf kalibriertem Display

### Problem: Bild zu dunkel oder zu hell
**Lösungen**:
- ✅ Passen Sie **Brightness** in kleinen Schritten an (±0.05)
- ✅ Prüfen Sie, ob **Contrast** das Problem verstärkt
- ✅ Falls sehr dunkel: Brightness +0.2, Contrast -0.1
- ✅ Falls sehr hell: Brightness -0.2, Contrast +0.1

### Problem: Verlust von Details in Schatten oder Highlights
**Lösungen**:
- ✅ Reduzieren Sie **Contrast** (Sie haben zu weit gedrückt)
- ✅ Passen Sie **Brightness** zur Kompensation an
- ✅ Erwägen Sie **Color Grading - Tonal** für gezielte Kontrolle
- ✅ Könnte mit Original besser-belichteter Footage arbeiten müssen

### Problem: Schwarzweiß-Konversion sieht flach aus
**Lösungen**:
- ✅ Setzen Sie **Saturation** auf 0.0
- ✅ Erhöhen Sie **Contrast** signifikant (+0.3 bis +0.5)
- ✅ Passen Sie **Brightness** für korrekte Belichtung an
- ✅ Könnte mehrere Passes für dramatisches S/W brauchen

### Problem: Hue-Rotation erzeugt seltsame Farben
**Lösungen**:
- ✅ Nutzen Sie kleinere **Hue Rotation**-Werte (<0.1)
- ✅ Verstehen Sie, dass Sie ALLE Farben gleichmäßig verschieben
- ✅ Für selektive Hue-Änderungen nutzen Sie **Color Replace** stattdessen
- ✅ Einige Hue-Werte erzeugen natürlichere Ergebnisse als andere

### Problem: Anpassungen sehen auf verschiedenen Bildschirmen unterschiedlich aus
**Lösungen**:
- ✅ Arbeiten Sie auf kalibriertem Display wenn möglich
- ✅ Vorschau auf Ziel-Display (Telefon, TV, etc.)
- ✅ Vermeiden Sie extreme Sättigung/Kontrast
- ✅ Testen Sie auf mehreren Geräten vor Finalisierung

## ⚡ Performance-Tipps

- ✅ Einzelne Instanz ist extrem schnell
- ✅ Stapeln von 5+ Instanzen könnte Performance leicht beeinflussen
- ✅ HSV-Konversion ist optimiert
- ✅ Funktioniert großartig mit Video-Wiedergabe
- ✅ Echtzeit-fähig für Live-Visuals

## 🎓 Fortgeschrittene Techniken

### Nachbildung von Filmstocks
Verschiedene Filmstocks haben charakteristische Looks:

**Kodak Vision3 500T (Warm, Gesättigt):**
- Saturation: 1.15
- Contrast: +0.12
- Hue Rotation: 0.015 (leichte warme Verschiebung)
- Brightness: 0.0

**Fuji Eterna (Gedämpft, Kinematisch):**
- Saturation: 0.85
- Contrast: +0.08
- Brightness: -0.05
- Hue Rotation: 0.0

**Ilford HP5 S/W:**
- Saturation: 0.0
- Contrast: +0.25
- Brightness: +0.03
- Hue Rotation: 0.0

### Szenen angleichen
Beim Compositing oder Editieren mehrerer Shots:

1. **Referenz-Shot**: Graden Sie Ihren Hero-/Referenz-Shot zuerst
2. **Angleichen**: Notieren Sie exakte Parameter-Werte
3. **Anwenden**: Nutzen Sie gleiche oder ähnliche Werte auf anderen Shots
4. **Feinabstimmung**: Passen Sie für Beleuchtungs-Unterschiede an
5. **Konsistenz**: Erhalten Sie Gesamtlook über alle Shots

### Farbharmonie-Techniken

**Komplementärfarben (Hohes Drama):**
- Hue Rotation: 0.5 (180° - entgegengesetzte Farben)
- Hohe Sättigung: 1.4-1.6
- Starker Kontrast: +0.3

**Analoge Farben (Harmonisch):**
- Hue Rotation: 0.08-0.16 (30-60° Verschiebung)
- Moderate Sättigung: 1.1-1.3
- Moderater Kontrast: +0.15

**Monochromatisch (Vereinheitlicht):**
- Niedrige Sättigung: 0.7-0.9
- Beliebige Hue Rotation
- Kontrast für Interesse: +0.2

## 💡 Warum dieser Node erstellt wurde

Jeder Colorist braucht fundamentale Kontrollen. **Color Grading - Basic** bietet:

- ✅ **Essentielle vier Kontrollen**, die jedes Bild braucht
- ✅ **Einfache Oberfläche** für schnelle Anpassungen
- ✅ **Professionelle Ergebnisse** mit minimaler Komplexität
- ✅ **Stapelbares Design** für komplexe Workflows
- ✅ **Echtzeit-Feedback** für interaktives Grading
- ✅ **Grundlage** für alle Farbarbeit in Coollab

Meistern Sie diese Basics, und Sie sind für 80% der Color-Grading-Aufgaben ausgerüstet!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
