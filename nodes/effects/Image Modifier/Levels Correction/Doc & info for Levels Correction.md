[English](#levels-correction---documentation) | [Deutsch](#levels-correction---dokumentation)

---

# Levels Correction - Documentation

## Overview

**Levels Correction** is a classic video levels adjustment tool that provides precise control over the tonal range of your image through three key control points: Base (black point), Mid Point (gamma), and Ratio (white point). This is the same fundamental tool found in professional video editing software, allowing you to remap input tonal ranges and adjust midtone gamma for perfect exposure and contrast control.

## Inspiration & Design Philosophy

Based on the classic levels histogram control found in professional color correction:

- **Three-Point Control**: Industry-standard Base/Mid/Ratio workflow
- **Histogram Remapping**: Redefine what constitutes black and white in your image
- **Gamma Adjustment**: Non-linear midtone control for natural-looking corrections
- **Bidirectional Operation**: All controls work symmetrically around their neutral points
- **Professional Standard**: The same tool used in broadcast and cinema color grading

This node brings professional levels adjustment to Coollab, enabling precise tonal control that forms the foundation of color correction workflows.

## Key Features

### ⚫ Base (Input Black Point)
Control where blacks begin:
- **0.5** = Neutral (no change)
- **<0.5** = Crush blacks (darker shadows, increased contrast)
- **>0.5** = Lift blacks (lighter shadows, reduced contrast)
- Redefines the darkest point in your image

### 🌓 Mid Point (Gamma)
Non-linear midtone adjustment:
- **0.5** = Neutral (no gamma change)
- **<0.5** = Darken midtones (power curve adjustment)
- **>0.5** = Lighten midtones (inverse power curve)
- Affects middle tones without clipping blacks or whites

### ⚪ Ratio (Input White Point)
Control where whites end:
- **0.5** = Neutral (no change)
- **<0.5** = Compress whites (darker highlights)
- **>0.5** = Expand whites (brighter highlights)
- Redefines the brightest point in your image

### 🎯 Mathematical Precision
- Proper histogram remapping mathematics
- Non-destructive tonal adjustments
- Prevents clipping through careful clamping
- Professional-grade algorithms

### ⚡ Real-time Performance
- Optimized power curve calculations
- Fast range remapping
- Suitable for video playback
- Interactive adjustment feedback

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to adjust |
| **Base** | 0.0 - 1.0 | 0.5 | Input black point. 0.5 = neutral, <0.5 = darker blacks, >0.5 = lifted blacks. |
| **Mid Point** | 0.0 - 1.0 | 0.5 | Midpoint gamma adjustment. 0.5 = neutral, <0.5 = darker midtones, >0.5 = lighter midtones. |
| **Ratio** | 0.0 - 1.0 | 0.5 | Input white point. 0.5 = neutral, <0.5 = compressed whites, >0.5 = expanded whites. |

## Creative Usage Tips

### 🎬 Corrective Levels Adjustment

**Basic Exposure Correction:**
1. Import underexposed image
2. Add **Levels Correction**
3. **Base**: Keep at 0.5 (don't lift blacks unless necessary)
4. **Mid Point**: Increase to 0.6-0.7 (lighten midtones)
5. **Ratio**: Keep at 0.5 or slightly increase (0.52-0.55)
6. Result: Brighter image without washing out blacks

**Overexposed Recovery:**
1. Overexposed/washed out image
2. **Base**: Slight increase to 0.52-0.55 (add some black)
3. **Mid Point**: Decrease to 0.4-0.45 (darken midtones)
4. **Ratio**: Decrease to 0.45-0.48 (compress highlights)
5. Result: Recovered tonal range

**Low Contrast / Flat Image:**
1. Image lacks depth (flat histogram)
2. **Base**: Decrease to 0.45-0.48 (crush blacks slightly)
3. **Mid Point**: Keep at 0.5 or adjust slightly
4. **Ratio**: Increase to 0.52-0.55 (expand highlights)
5. Result: Increased contrast, more punch

**High Contrast Reduction:**
1. Harsh, contrasty image
2. **Base**: Increase to 0.52-0.58 (lift shadows)
3. **Mid Point**: Adjust to taste (0.48-0.52)
4. **Ratio**: Decrease to 0.45-0.48 (compress highlights)
5. Result: Softer, more compressed tonal range

### 🎨 Creative Stylization

**Crushed Blacks (Cinema Look):**
1. **Base**: Significantly decrease to 0.35-0.42
2. **Mid Point**: Slight increase to 0.52-0.55 (compensate)
3. **Ratio**: Keep at 0.5
4. Creates deep, rich blacks typical of cinema

**Lifted Blacks (Faded/Vintage):**
1. **Base**: Significantly increase to 0.58-0.65
2. **Mid Point**: Adjust to prevent washout (0.48-0.52)
3. **Ratio**: May need to decrease slightly (0.48-0.5)
4. Creates washed, vintage, faded aesthetic

**Compressed Highlights (Soft/Dreamy):**
1. **Base**: Keep neutral or slightly lift (0.5-0.52)
2. **Mid Point**: Slight increase (0.52-0.55)
3. **Ratio**: Significantly decrease to 0.38-0.45
4. Creates soft, dreamy, high-key look

**Expanded Tonal Range:**
1. **Base**: Slight decrease (0.48-0.5)
2. **Mid Point**: Adjust for exposure (0.48-0.55)
3. **Ratio**: Increase to 0.55-0.6
4. Maximum tonal range utilization

### 🌈 Advanced Techniques

**S-Curve Contrast (Manual):**
1. **Base**: Decrease to 0.47 (darken shadows)
2. **Mid Point**: Keep at 0.5 or slight increase (0.51)
3. **Ratio**: Increase to 0.53 (brighten highlights)
4. Creates classic S-curve contrast boost

**Inverse S-Curve (Flatten):**
1. **Base**: Increase to 0.53 (lift shadows)
2. **Mid Point**: Keep at 0.5 or adjust slightly
3. **Ratio**: Decrease to 0.47 (compress highlights)
4. Reduces contrast, flattens image

**Shadow Detail Recovery:**
1. **Base**: Increase to 0.52-0.6 (lift shadows)
2. **Mid Point**: Decrease slightly to 0.48 (prevent overexposure)
3. **Ratio**: Keep at 0.5
4. Reveals hidden shadow detail

**Highlight Detail Protection:**
1. **Base**: Keep at 0.5
2. **Mid Point**: Increase slightly to 0.52 (maintain exposure)
3. **Ratio**: Decrease to 0.42-0.48 (protect highlights)
4. Prevents highlight clipping

### 🎛️ Working with the Histogram (Conceptual)

Think of Levels Correction as manipulating a histogram:

**Base (Left Point):**
- Moves where "black" starts on the histogram
- Everything darker than this becomes pure black
- Lifting this adds gray to shadows

**Mid Point (Middle Slider):**
- Redistributes tones between black and white
- Doesn't move the endpoints
- Gamma curve adjustment

**Ratio (Right Point):**
- Moves where "white" ends on the histogram
- Everything brighter than this becomes pure white
- Lowering this compresses highlights

**Visualization:**
```
Dark ← Base → Mid Point ← Ratio → Bright
 |              ↕              |
Black     Gamma Adjust      White
```

## Workflow Examples

### Example 1: Underexposed Image Correction
1. Load dark, underexposed image
2. Add **Levels Correction**
3. **Base**: 0.5 (keep blacks)
4. **Mid Point**: 0.65 (significantly lighten midtones)
5. **Ratio**: 0.52 (slight highlight expansion)
6. Result: Properly exposed, natural-looking image

### Example 2: Washed Out / Low Contrast Fix
1. Flat, low contrast image
2. Add **Levels Correction**
3. **Base**: 0.46 (crush blacks slightly)
4. **Mid Point**: 0.5 (keep midtones)
5. **Ratio**: 0.54 (expand highlights)
6. Result: Punchy, contrasty image with depth

### Example 3: Vintage Faded Look
1. Modern digital photo
2. Add **Levels Correction**
3. **Base**: 0.6 (significantly lift blacks - faded)
4. **Mid Point**: 0.48 (slightly darken to compensate)
5. **Ratio**: 0.48 (compress highlights slightly)
6. Result: Vintage, faded, retro aesthetic

### Example 4: Cinema Black Crush
1. Standard video footage
2. Add **Levels Correction**
3. **Base**: 0.4 (aggressive black crush)
4. **Mid Point**: 0.54 (lift midtones to compensate)
5. **Ratio**: 0.5 (keep whites)
6. Result: Deep, rich cinematic blacks

### Example 5: High-Key Bright Aesthetic
1. Portrait or product photo
2. Add **Levels Correction**
3. **Base**: 0.56 (lift shadows significantly)
4. **Mid Point**: 0.55 (brighten midtones)
5. **Ratio**: 0.48 (compress highlights)
6. Result: Bright, airy, high-key look

### Example 6: Shadow Detail Recovery
1. Image with blocked-up shadows
2. Add **Levels Correction**
3. **Base**: 0.58 (aggressively lift shadows)
4. **Mid Point**: 0.46 (darken midtones to prevent wash-out)
5. **Ratio**: 0.5 (keep highlights)
6. Result: Revealed shadow detail without overexposure

### Example 7: HDR-Style Look
1. Standard dynamic range image
2. Add **Levels Correction**
3. **Base**: 0.52 (lift shadows)
4. **Mid Point**: 0.48 (darken midtones slightly)
5. **Ratio**: 0.48 (compress highlights)
6. Result: Pseudo-HDR compressed tonal range

## Technical Details

- **Node Type**: Tonal Adjustment (UV→sRGB_StraightA)
- **Category**: Color Grading / Levels
- **Algorithm**: Range remapping + gamma power curves
- **Precision**: Full floating-point calculations
- **Performance**: Real-time capable, optimized
- **Color Space**: sRGB

## Understanding the Algorithm

### Base (Black Point Adjustment)
```
base_offset = (Base - 0.5) × 2.0
rgb = rgb - base_offset
```
- Shifts entire tonal range up or down
- Negative offset (Base < 0.5) darkens/crushes blacks
- Positive offset (Base > 0.5) lifts blacks

### Ratio (White Point Adjustment)
```
ratio_factor = 0.5 + (Ratio - 0.5) × 2.0
rgb = rgb / ratio_factor
```
- Compresses or expands tonal range
- Factor < 1.0 (Ratio < 0.5) compresses (darker)
- Factor > 1.0 (Ratio > 0.5) expands (brighter)

### Mid Point (Gamma Adjustment)
```
If Mid Point < 0.5:
  gamma = 1.0 + (0.5 - Mid Point) × 4.0  // Range: 1.0 to 3.0
  rgb = pow(rgb, gamma)  // Darkens

If Mid Point > 0.5:
  gamma = 1.0 - (Mid Point - 0.5) × 1.6  // Range: 1.0 to 0.2
  rgb = pow(rgb, gamma)  // Lightens
```
- Power curve adjustment
- Non-linear redistribution of midtones
- Preserves blacks and whites

### Processing Order
1. **Base** (first) - establishes black point
2. **Ratio** (second) - establishes white point  
3. **Mid Point** (last) - redistributes midtones

This order ensures predictable, professional results.

## Best Practices

### 🎯 Adjustment Strategy

**Start with Base & Ratio:**
1. Set **Base** to establish your blacks
2. Set **Ratio** to establish your whites
3. Finally adjust **Mid Point** for exposure

**Work Subtly:**
- Small adjustments (±0.02-0.05) often sufficient
- Extreme values (±0.15+) for creative looks only
- Preview constantly while adjusting

**Check Your Endpoints:**
- Ensure you're not clipping blacks (losing shadow detail)
- Ensure you're not clipping whites (losing highlight detail)
- Use histogram if available

### 💡 Common Adjustments

**Slight Contrast Boost:**
- Base: 0.48
- Mid Point: 0.5
- Ratio: 0.52

**Moderate Contrast Boost:**
- Base: 0.45
- Mid Point: 0.5
- Ratio: 0.55

**Vintage Fade:**
- Base: 0.58-0.65
- Mid Point: 0.48-0.5
- Ratio: 0.48-0.5

**Cinema Blacks:**
- Base: 0.35-0.42
- Mid Point: 0.52-0.55
- Ratio: 0.5

### ⚠️ Common Mistakes to Avoid

- ❌ Moving all three sliders simultaneously (confusing)
- ❌ Extreme Base values causing gray blacks
- ❌ Ignoring Mid Point (most powerful control)
- ❌ Forgetting that 0.5 is neutral for all controls
- ❌ Not checking for clipping in shadows/highlights

## Combining with Other Nodes

**Essential Workflow Companions:**
- **⭐ Color Grading - Basic**: Use after Levels for saturation/hue
- **🎨 Gamma Correction**: Additional gamma control if needed
- **💡 Color Grading - Tonal**: Selective shadow/mid/highlight adjustment
- **🔧 Additional Levels Correction**: Stack for complex curves
- **🌈 Color Replace**: Selective color work after tonal correction

**Recommended Workflows:**

**Professional Color Correction:**
```
Image → Levels Correction (tonal foundation)
      → Color Grading - Basic (saturation/contrast)
      → Color Grading - Tonal (selective adjustments)
      → Output
```

**Vintage Film Emulation:**
```
Image → Levels Correction (lift blacks, compress highlights)
      → Color Grading - Basic (reduce saturation, add warmth)
      → Output
```

**HDR-Style Processing:**
```
Image → Levels Correction (compress tonal range)
      → Color Grading - Tonal (enhance local contrast)
      → Color Grading - Basic (boost saturation)
      → Output
```

## Troubleshooting Guide

### Problem: Image looks washed out / gray
**Solutions**:
- ✅ **Base** is too high - reduce toward 0.5
- ✅ **Ratio** is too low - increase toward 0.5
- ✅ You've compressed the tonal range too much
- ✅ Add contrast with Color Grading - Basic after

### Problem: Lost detail in shadows
**Solutions**:
- ✅ **Base** is too low - crushing blacks
- ✅ Increase Base to 0.48-0.52 to reveal detail
- ✅ Adjust **Mid Point** up slightly (0.52-0.55)
- ✅ May need better source material

### Problem: Lost detail in highlights
**Solutions**:
- ✅ **Ratio** is too high - clipping whites
- ✅ Decrease Ratio to 0.45-0.5 to protect highlights
- ✅ Adjust **Mid Point** down slightly (0.48-0.5)
- ✅ May need better exposed source

### Problem: Midtones too dark after adjusting Base/Ratio
**Solutions**:
- ✅ Increase **Mid Point** to 0.55-0.65
- ✅ Base and Ratio set the range, Mid Point redistributes
- ✅ This is normal - Mid Point is your compensation tool

### Problem: Can't achieve desired contrast
**Solutions**:
- ✅ Use **Color Grading - Basic** for additional contrast
- ✅ Stack multiple **Levels Correction** nodes
- ✅ Combine with **Color Grading - Tonal** for selective contrast
- ✅ Source material may have limitations

### Problem: Colors look strange after adjustment
**Solutions**:
- ✅ Levels affects luminance, which can shift color perception
- ✅ Use **Color Grading - Basic** after to adjust saturation
- ✅ Extreme tonal shifts may require color correction
- ✅ Check on calibrated display

### Problem: Don't understand which control does what
**Solutions**:
- ✅ **Base**: Think "where do my blacks start?"
- ✅ **Ratio**: Think "where do my whites end?"
- ✅ **Mid Point**: Think "are my midtones too dark/bright?"
- ✅ Always return to 0.5 (neutral) to reset

## Performance Tips

- ✅ Very fast, real-time capable
- ✅ Power curve calculations are optimized
- ✅ Works great with video playback
- ✅ Can stack multiple instances without major slowdown
- ✅ Suitable for live performance use

## Advanced Techniques

### Matching Shots
When matching multiple shots in a sequence:

1. **Reference Shot**: Adjust your hero shot first
2. **Note Values**: Write down exact Base/Mid/Ratio values
3. **Apply to Others**: Use same or similar values on other shots
4. **Fine-Tune**: Adjust for lighting differences
5. **Consistency**: Maintain overall look across sequence

### Creating Custom Curves
Stack multiple Levels Correction nodes for complex curves:

**Double S-Curve:**
1. **First Instance**: Base 0.47, Mid 0.5, Ratio 0.53
2. **Second Instance**: Base 0.5, Mid 0.52, Ratio 0.5
3. Result: Complex tonal response

### Film Print Emulation
Recreate film print characteristics:

**Positive Print:**
- Base: 0.52 (lifted blacks characteristic of prints)
- Mid Point: 0.5
- Ratio: 0.5

**Faded Print:**
- Base: 0.6 (significant lift)
- Mid Point: 0.48
- Ratio: 0.48 (compressed highlights)

### Broadcast Safe
Ensure levels stay within broadcast standards:

**Conservative Levels:**
- Base: 0.52 (prevent crushed blacks at 0 IRE)
- Mid Point: Adjust for exposure
- Ratio: 0.48 (prevent clipped whites at 100 IRE)

## Why This Node Was Created

Professional color correction requires precise tonal control. **Levels Correction** provides:

- ✅ **Industry-standard three-point control** (Base/Mid/Ratio)
- ✅ **Proper histogram remapping** mathematics
- ✅ **Bidirectional operation** - all controls work naturally
- ✅ **Foundation for color grading** workflows
- ✅ **Professional results** with intuitive controls
- ✅ **Real-time feedback** for interactive adjustment

This is the same fundamental tool used in professional color grading suites, now available in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#levels-correction---documentation) | [Deutsch](#levels-correction---dokumentation)

---

# Levels Correction - Dokumentation

## Übersicht

**Levels Correction** ist ein klassisches Video-Levels-Anpassungstool, das präzise Kontrolle über den Tonbereich Ihres Bildes durch drei Schlüssel-Kontrollpunkte bietet: Base (Schwarzpunkt), Mid Point (Gamma) und Ratio (Weißpunkt). Dies ist dasselbe fundamentale Tool, das in professioneller Videobearbeitungs-Software zu finden ist, und ermöglicht es Ihnen, Eingangs-Tonbereiche neu zu mappen und Mittelton-Gamma für perfekte Belichtungs- und Kontrast-Kontrolle anzupassen.

## 🎯 Inspiration & Design-Philosophie

Basierend auf der klassischen Levels-Histogramm-Kontrolle aus professioneller Farbkorrektur:

- **Drei-Punkt-Kontrolle**: Industrie-standard Base/Mid/Ratio-Workflow
- **Histogramm-Remapping**: Definieren Sie neu, was Schwarz und Weiß in Ihrem Bild ausmacht
- **Gamma-Anpassung**: Nicht-lineare Mittelton-Kontrolle für natürlich aussehende Korrekturen
- **Bidirektionale Operation**: Alle Kontrollen arbeiten symmetrisch um ihre neutralen Punkte
- **Professioneller Standard**: Dasselbe Tool, das in Broadcast und Kino-Color-Grading genutzt wird

Dieser Node bringt professionelle Levels-Anpassung zu Coollab und ermöglicht präzise Ton-Kontrolle, die die Grundlage von Farbkorrektur-Workflows bildet.

## ⭐ Hauptmerkmale

### ⚫ Base (Eingangs-Schwarzpunkt)
Kontrollieren Sie, wo Schwarz beginnt:
- **0.5** = Neutral (keine Änderung)
- **<0.5** = Crush Blacks (dunklere Schatten, erhöhter Kontrast)
- **>0.5** = Lift Blacks (hellere Schatten, reduzierter Kontrast)
- Definiert den dunkelsten Punkt in Ihrem Bild neu

### 🌓 Mid Point (Gamma)
Nicht-lineare Mittelton-Anpassung:
- **0.5** = Neutral (keine Gamma-Änderung)
- **<0.5** = Verdunkle Mitteltöne (Power-Kurven-Anpassung)
- **>0.5** = Helle Mitteltöne auf (inverse Power-Kurve)
- Betrifft mittlere Töne ohne Clipping von Schwarz oder Weiß

### ⚪ Ratio (Eingangs-Weißpunkt)
Kontrollieren Sie, wo Weiß endet:
- **0.5** = Neutral (keine Änderung)
- **<0.5** = Komprimiere Weißtöne (dunklere Highlights)
- **>0.5** = Erweitere Weißtöne (hellere Highlights)
- Definiert den hellsten Punkt in Ihrem Bild neu

### 🎯 Mathematische Präzision
- Korrekte Histogramm-Remapping-Mathematik
- Non-destructive Ton-Anpassungen
- Verhindert Clipping durch sorgfältiges Clamping
- Professionelle Algorithmen

### ⚡ Echtzeit-Performance
- Optimierte Power-Kurven-Berechnungen
- Schnelles Range-Remapping
- Geeignet für Video-Wiedergabe
- Interaktives Anpassungs-Feedback

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das anzupassende Bild |
| **Base** | 0.0 - 1.0 | 0.5 | Eingangs-Schwarzpunkt. 0.5 = neutral, <0.5 = dunklere Schwarztöne, >0.5 = gehobene Schwarztöne. |
| **Mid Point** | 0.0 - 1.0 | 0.5 | Mittelpunkt-Gamma-Anpassung. 0.5 = neutral, <0.5 = dunklere Mitteltöne, >0.5 = hellere Mitteltöne. |
| **Ratio** | 0.0 - 1.0 | 0.5 | Eingangs-Weißpunkt. 0.5 = neutral, <0.5 = komprimierte Weißtöne, >0.5 = erweiterte Weißtöne. |

## 🎨 Kreative Nutzungstipps

### 🎬 Korrigierende Levels-Anpassung

**Basis-Belichtungskorrektur:**
1. Importieren Sie unterbelichtetes Bild
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: Bei 0.5 halten (nicht Schwarztöne heben außer notwendig)
4. **Mid Point**: Erhöhen auf 0.6-0.7 (Mitteltöne aufhellen)
5. **Ratio**: Bei 0.5 halten oder leicht erhöhen (0.52-0.55)
6. Ergebnis: Helleres Bild ohne Auswaschen der Schwarztöne

**Überbelichtungs-Wiederherstellung:**
1. Überbelichtetes/ausgewaschenes Bild
2. **Base**: Leichte Erhöhung auf 0.52-0.55 (etwas Schwarz hinzufügen)
3. **Mid Point**: Verringern auf 0.4-0.45 (Mitteltöne verdunkeln)
4. **Ratio**: Verringern auf 0.45-0.48 (Highlights komprimieren)
5. Ergebnis: Wiederhergestellter Tonbereich

**Niedriger Kontrast / Flaches Bild:**
1. Bild fehlt Tiefe (flaches Histogramm)
2. **Base**: Verringern auf 0.45-0.48 (Schwarztöne leicht crushen)
3. **Mid Point**: Bei 0.5 halten oder leicht anpassen
4. **Ratio**: Erhöhen auf 0.52-0.55 (Highlights erweitern)
5. Ergebnis: Erhöhter Kontrast, mehr Punch

**Hohe Kontrast-Reduktion:**
1. Hartes, kontrastiges Bild
2. **Base**: Erhöhen auf 0.52-0.58 (Schatten heben)
3. **Mid Point**: Nach Geschmack anpassen (0.48-0.52)
4. **Ratio**: Verringern auf 0.45-0.48 (Highlights komprimieren)
5. Ergebnis: Weicherer, komprimierterer Tonbereich

### 🎨 Kreative Stilisierung

**Gecrushtе Schwarztöne (Kino-Look):**
1. **Base**: Signifikant verringern auf 0.35-0.42
2. **Mid Point**: Leichte Erhöhung auf 0.52-0.55 (kompensieren)
3. **Ratio**: Bei 0.5 halten
4. Erzeugt tiefe, satte Schwarztöne typisch für Kino

**Gehobene Schwarztöne (Faded/Vintage):**
1. **Base**: Signifikant erhöhen auf 0.58-0.65
2. **Mid Point**: Anpassen zur Vermeidung von Auswaschen (0.48-0.52)
3. **Ratio**: Könnte leichte Verringerung brauchen (0.48-0.5)
4. Erzeugt ausgewaschene, Vintage, verblasste Ästhetik

**Komprimierte Highlights (Weich/Verträumt):**
1. **Base**: Neutral halten oder leicht heben (0.5-0.52)
2. **Mid Point**: Leichte Erhöhung (0.52-0.55)
3. **Ratio**: Signifikant verringern auf 0.38-0.45
4. Erzeugt weichen, verträumten, High-Key-Look

**Erweiterten Tonbereich:**
1. **Base**: Leichte Verringerung (0.48-0.5)
2. **Mid Point**: Für Belichtung anpassen (0.48-0.55)
3. **Ratio**: Erhöhen auf 0.55-0.6
4. Maximale Tonbereich-Nutzung

### 🌈 Fortgeschrittene Techniken

**S-Kurven-Kontrast (Manuell):**
1. **Base**: Verringern auf 0.47 (Schatten verdunkeln)
2. **Mid Point**: Bei 0.5 halten oder leicht erhöhen (0.51)
3. **Ratio**: Erhöhen auf 0.53 (Highlights aufhellen)
4. Erzeugt klassischen S-Kurven-Kontrast-Boost

**Inverse S-Kurve (Abflachen):**
1. **Base**: Erhöhen auf 0.53 (Schatten heben)
2. **Mid Point**: Bei 0.5 halten oder leicht anpassen
3. **Ratio**: Verringern auf 0.47 (Highlights komprimieren)
4. Reduziert Kontrast, flacht Bild ab

**Schatten-Detail-Wiederherstellung:**
1. **Base**: Erhöhen auf 0.52-0.6 (Schatten heben)
2. **Mid Point**: Leicht verringern auf 0.48 (Überbelichtung verhindern)
3. **Ratio**: Bei 0.5 halten
4. Enthüllt verstecktes Schatten-Detail

**Highlight-Detail-Schutz:**
1. **Base**: Bei 0.5 halten
2. **Mid Point**: Leicht erhöhen auf 0.52 (Belichtung erhalten)
3. **Ratio**: Verringern auf 0.42-0.48 (Highlights schützen)
4. Verhindert Highlight-Clipping

### 🎛️ Mit dem Histogramm arbeiten (Konzeptuell)

Denken Sie an Levels Correction als Manipulation eines Histogramms:

**Base (Linker Punkt):**
- Bewegt, wo "Schwarz" auf dem Histogramm beginnt
- Alles dunkler als dies wird reines Schwarz
- Dies heben fügt Grau zu Schatten hinzu

**Mid Point (Mittlerer Slider):**
- Verteilt Töne zwischen Schwarz und Weiß neu
- Bewegt die Endpunkte nicht
- Gamma-Kurven-Anpassung

**Ratio (Rechter Punkt):**
- Bewegt, wo "Weiß" auf dem Histogramm endet
- Alles heller als dies wird reines Weiß
- Dies senken komprimiert Highlights

**Visualisierung:**
```
Dunkel ← Base → Mid Point ← Ratio → Hell
   |                ↕               |
Schwarz      Gamma Anpassung     Weiß
```

## 💡 Workflow-Beispiele

### Beispiel 1: Unterbelichtete Bild-Korrektur
1. Laden Sie dunkles, unterbelichtetes Bild
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.5 (Schwarztöne behalten)
4. **Mid Point**: 0.65 (signifikant Mitteltöne aufhellen)
5. **Ratio**: 0.52 (leichte Highlight-Erweiterung)
6. Ergebnis: Korrekt belichtetes, natürlich aussehendes Bild

### Beispiel 2: Ausgewaschen / Niedriger Kontrast Fix
1. Flaches, niedriger-Kontrast-Bild
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.46 (Schwarztöne leicht crushen)
4. **Mid Point**: 0.5 (Mitteltöne behalten)
5. **Ratio**: 0.54 (Highlights erweitern)
6. Ergebnis: Knackiges, kontrastiges Bild mit Tiefe

### Beispiel 3: Vintage-Verblasster-Look
1. Modernes Digital-Foto
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.6 (signifikant Schwarztöne heben - verbliched)
4. **Mid Point**: 0.48 (leicht verdunkeln zur Kompensation)
5. **Ratio**: 0.48 (Highlights leicht komprimieren)
6. Ergebnis: Vintage, verblasste, Retro-Ästhetik

### Beispiel 4: Kino-Schwarz-Crush
1. Standard-Video-Footage
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.4 (aggressiver Schwarz-Crush)
4. **Mid Point**: 0.54 (Mitteltöne heben zur Kompensation)
5. **Ratio**: 0.5 (Weißtöne behalten)
6. Ergebnis: Tiefe, satte kinematische Schwarztöne

### Beispiel 5: High-Key-Helle-Ästhetik
1. Portrait oder Produkt-Foto
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.56 (Schatten signifikant heben)
4. **Mid Point**: 0.55 (Mitteltöne aufhellen)
5. **Ratio**: 0.48 (Highlights komprimieren)
6. Ergebnis: Heller, luftiger, High-Key-Look

### Beispiel 6: Schatten-Detail-Wiederherstellung
1. Bild mit zugemachten Schatten
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.58 (aggressiv Schatten heben)
4. **Mid Point**: 0.46 (Mitteltöne verdunkeln zur Vermeidung von Auswaschen)
5. **Ratio**: 0.5 (Highlights behalten)
6. Ergebnis: Enthülltes Schatten-Detail ohne Überbelichtung

### Beispiel 7: HDR-Stil-Look
1. Standard-Dynamikbereich-Bild
2. Fügen Sie **Levels Correction** hinzu
3. **Base**: 0.52 (Schatten heben)
4. **Mid Point**: 0.48 (Mitteltöne leicht verdunkeln)
5. **Ratio**: 0.48 (Highlights komprimieren)
6. Ergebnis: Pseudo-HDR komprimierter Tonbereich

## 🔧 Technische Details

- **Node-Typ**: Tonal Adjustment (UV→sRGB_StraightA)
- **Kategorie**: Color Grading / Levels
- **Algorithmus**: Range-Remapping + Gamma-Power-Kurven
- **Präzision**: Vollständige Fließkomma-Berechnungen
- **Performance**: Echtzeit-fähig, optimiert
- **Farbraum**: sRGB

## 🧮 Verständnis des Algorithmus

### Base (Schwarzpunkt-Anpassung)
```
base_offset = (Base - 0.5) × 2.0
rgb = rgb - base_offset
```
- Verschiebt gesamten Tonbereich auf oder ab
- Negativer Offset (Base < 0.5) verdunkelt/crusht Schwarztöne
- Positiver Offset (Base > 0.5) hebt Schwarztöne

### Ratio (Weißpunkt-Anpassung)
```
ratio_factor = 0.5 + (Ratio - 0.5) × 2.0
rgb = rgb / ratio_factor
```
- Komprimiert oder erweitert Tonbereich
- Faktor < 1.0 (Ratio < 0.5) komprimiert (dunkler)
- Faktor > 1.0 (Ratio > 0.5) erweitert (heller)

### Mid Point (Gamma-Anpassung)
```
Falls Mid Point < 0.5:
  gamma = 1.0 + (0.5 - Mid Point) × 4.0  // Bereich: 1.0 bis 3.0
  rgb = pow(rgb, gamma)  // Verdunkelt

Falls Mid Point > 0.5:
  gamma = 1.0 - (Mid Point - 0.5) × 1.6  // Bereich: 1.0 bis 0.2
  rgb = pow(rgb, gamma)  // Hellt auf
```
- Power-Kurven-Anpassung
- Nicht-lineare Neuverteilung von Mitteltönen
- Erhält Schwarztöne und Weißtöne

### Verarbeitungs-Reihenfolge
1. **Base** (zuerst) - etabliert Schwarzpunkt
2. **Ratio** (zweite) - etabliert Weißpunkt
3. **Mid Point** (zuletzt) - verteilt Mitteltöne neu

Diese Reihenfolge gewährleistet vorhersagbare, professionelle Ergebnisse.

## 🎬 Best Practices

### 🎯 Anpassungs-Strategie

**Starten Sie mit Base & Ratio:**
1. Setzen Sie **Base**, um Ihre Schwarztöne zu etablieren
2. Setzen Sie **Ratio**, um Ihre Weißtöne zu etablieren
3. Passen Sie schließlich **Mid Point** für Belichtung an

**Arbeiten Sie subtil:**
- Kleine Anpassungen (±0.02-0.05) oft ausreichend
- Extreme Werte (±0.15+) nur für kreative Looks
- Vorschau konstant während Anpassung

**Prüfen Sie Ihre Endpunkte:**
- Stellen Sie sicher, dass Sie Schwarztöne nicht clippen (Schatten-Detail verlieren)
- Stellen Sie sicher, dass Sie Weißtöne nicht clippen (Highlight-Detail verlieren)
- Nutzen Sie Histogramm falls verfügbar

### 💡 Häufige Anpassungen

**Leichter Kontrast-Boost:**
- Base: 0.48
- Mid Point: 0.5
- Ratio: 0.52

**Moderater Kontrast-Boost:**
- Base: 0.45
- Mid Point: 0.5
- Ratio: 0.55

**Vintage-Verblassen:**
- Base: 0.58-0.65
- Mid Point: 0.48-0.5
- Ratio: 0.48-0.5

**Kino-Schwarztöne:**
- Base: 0.35-0.42
- Mid Point: 0.52-0.55
- Ratio: 0.5

### ⚠️ Häufige Fehler vermeiden

- ❌ Alle drei Slider gleichzeitig bewegen (verwirrend)
- ❌ Extreme Base-Werte, die graue Schwarztöne verursachen
- ❌ Mid Point ignorieren (mächtigste Kontrolle)
- ❌ Vergessen, dass 0.5 für alle Kontrollen neutral ist
- ❌ Nicht auf Clipping in Schatten/Highlights prüfen

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **⭐ Color Grading - Basic**: Nach Levels für Sättigung/Hue nutzen
- **🎨 Gamma Correction**: Zusätzliche Gamma-Kontrolle falls nötig
- **💡 Color Grading - Tonal**: Selektive Schatten/Mid/Highlight-Anpassung
- **🔧 Zusätzliche Levels Correction**: Stapeln für komplexe Kurven
- **🌈 Color Replace**: Selektive Farbarbeit nach Ton-Korrektur

**Empfohlene Workflows:**

**Professionelle Farbkorrektur:**
```
Image → Levels Correction (tonale Grundlage)
      → Color Grading - Basic (Sättigung/Kontrast)
      → Color Grading - Tonal (selektive Anpassungen)
      → Output
```

**Vintage-Film-Emulation:**
```
Image → Levels Correction (Schwarztöne heben, Highlights komprimieren)
      → Color Grading - Basic (Sättigung reduzieren, Wärme hinzufügen)
      → Output
```

**HDR-Stil-Verarbeitung:**
```
Image → Levels Correction (Tonbereich komprimieren)
      → Color Grading - Tonal (lokalen Kontrast verstärken)
      → Color Grading - Basic (Sättigung steigern)
      → Output
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Bild sieht ausgewaschen / grau aus
**Lösungen**:
- ✅ **Base** ist zu hoch - reduzieren Richtung 0.5
- ✅ **Ratio** ist zu niedrig - erhöhen Richtung 0.5
- ✅ Sie haben den Tonbereich zu sehr komprimiert
- ✅ Kontrast mit Color Grading - Basic danach hinzufügen

### Problem: Verlust von Detail in Schatten
**Lösungen**:
- ✅ **Base** ist zu niedrig - crusht Schwarztöne
- ✅ Base auf 0.48-0.52 erhöhen, um Detail zu enthüllen
- ✅ **Mid Point** leicht nach oben anpassen (0.52-0.55)
- ✅ Könnte besseres Quellmaterial brauchen

### Problem: Verlust von Detail in Highlights
**Lösungen**:
- ✅ **Ratio** ist zu hoch - clippt Weißtöne
- ✅ Ratio auf 0.45-0.5 verringern, um Highlights zu schützen
- ✅ **Mid Point** leicht nach unten anpassen (0.48-0.5)
- ✅ Könnte besser belichtete Quelle brauchen

### Problem: Mitteltöne zu dunkel nach Anpassung Base/Ratio
**Lösungen**:
- ✅ **Mid Point** auf 0.55-0.65 erhöhen
- ✅ Base und Ratio setzen den Bereich, Mid Point verteilt neu
- ✅ Dies ist normal - Mid Point ist Ihr Kompensations-Tool

### Problem: Kann gewünschten Kontrast nicht erreichen
**Lösungen**:
- ✅ Nutzen Sie **Color Grading - Basic** für zusätzlichen Kontrast
- ✅ Stapeln Sie mehrere **Levels Correction** Nodes
- ✅ Kombinieren Sie mit **Color Grading - Tonal** für selektiven Kontrast
- ✅ Quellmaterial könnte Limitationen haben

### Problem: Farben sehen seltsam aus nach Anpassung
**Lösungen**:
- ✅ Levels betrifft Luminanz, was Farbwahrnehmung verschieben kann
- ✅ Nutzen Sie **Color Grading - Basic** danach zur Sättigungs-Anpassung
- ✅ Extreme Ton-Verschiebungen könnten Farbkorrektur benötigen
- ✅ Prüfen Sie auf kalibriertem Display

### Problem: Verstehe nicht, welche Kontrolle was macht
**Lösungen**:
- ✅ **Base**: Denken Sie "wo beginnen meine Schwarztöne?"
- ✅ **Ratio**: Denken Sie "wo enden meine Weißtöne?"
- ✅ **Mid Point**: Denken Sie "sind meine Mitteltöne zu dunkel/hell?"
- ✅ Immer zu 0.5 (neutral) zurückkehren zum Zurücksetzen

## ⚡ Performance-Tipps

- ✅ Sehr schnell, echtzeit-fähig
- ✅ Power-Kurven-Berechnungen sind optimiert
- ✅ Funktioniert großartig mit Video-Wiedergabe
- ✅ Kann mehrere Instanzen stapeln ohne große Verlangsamung
- ✅ Geeignet für Live-Performance-Nutzung

## 🎓 Fortgeschrittene Techniken

### Shots angleichen
Beim Angleichen mehrerer Shots in einer Sequenz:

1. **Referenz-Shot**: Passen Sie Ihren Hero-Shot zuerst an
2. **Werte notieren**: Schreiben Sie exakte Base/Mid/Ratio-Werte auf
3. **Auf andere anwenden**: Nutzen Sie gleiche oder ähnliche Werte auf anderen Shots
4. **Feinabstimmung**: Passen Sie für Beleuchtungs-Unterschiede an
5. **Konsistenz**: Erhalten Sie Gesamtlook über Sequenz

### Custom-Kurven erstellen
Stapeln Sie mehrere Levels-Correction-Nodes für komplexe Kurven:

**Doppel-S-Kurve:**
1. **Erste Instanz**: Base 0.47, Mid 0.5, Ratio 0.53
2. **Zweite Instanz**: Base 0.5, Mid 0.52, Ratio 0.5
3. Ergebnis: Komplexe tonale Reaktion

### Film-Print-Emulation
Bilden Sie Film-Print-Charakteristika nach:

**Positiv-Print:**
- Base: 0.52 (gehobene Schwarztöne charakteristisch für Prints)
- Mid Point: 0.5
- Ratio: 0.5

**Verblasster Print:**
- Base: 0.6 (signifikantes Heben)
- Mid Point: 0.48
- Ratio: 0.48 (komprimierte Highlights)

### Broadcast Safe
Stellen Sie sicher, dass Levels innerhalb Broadcast-Standards bleiben:

**Konservative Levels:**
- Base: 0.52 (verhindert gecrushtе Schwarztöne bei 0 IRE)
- Mid Point: Für Belichtung anpassen
- Ratio: 0.48 (verhindert geclippte Weißtöne bei 100 IRE)

## 💡 Warum dieser Node erstellt wurde

Professionelle Farbkorrektur erfordert präzise Ton-Kontrolle. **Levels Correction** bietet:

- ✅ **Industrie-standard Drei-Punkt-Kontrolle** (Base/Mid/Ratio)
- ✅ **Korrekte Histogramm-Remapping**-Mathematik
- ✅ **Bidirektionale Operation** - alle Kontrollen arbeiten natürlich
- ✅ **Grundlage für Color-Grading**-Workflows
- ✅ **Professionelle Ergebnisse** mit intuitiven Kontrollen
- ✅ **Echtzeit-Feedback** für interaktive Anpassung

Dies ist dasselbe fundamentale Tool, das in professionellen Color-Grading-Suites genutzt wird, jetzt verfügbar in Coollab!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
