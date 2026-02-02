[English](#gamma-correction---documentation) | [Deutsch](#gamma-correction---dokumentation)

---

# Gamma Correction - Documentation

## Overview

**Gamma Correction** is a fundamental tool for adjusting the overall brightness curve of your image using gamma values. This single-parameter node provides professional gamma control based on the EBU/TV standard (gamma 2.2), allowing you to lighten or darken your image with a mathematically correct power curve that affects midtones more than shadows or highlights.

## Inspiration & Design Philosophy

Based on the broadcast and display standard gamma correction:

- **Single Parameter Simplicity**: One control, powerful results
- **EBU/TV Standard**: Based on gamma 2.2 reference (standard for video displays)
- **Non-Linear Adjustment**: Power curve affects midtones primarily
- **Professional Standard**: The same gamma correction used in broadcast workflows
- **Mathematical Precision**: Proper gamma mathematics for accurate results

This node brings broadcast-standard gamma correction to Coollab, providing the fundamental brightness adjustment tool used throughout the video production industry.

## Key Features

### 📐 Standard Gamma Correction
Professional gamma power curve:
- **Gamma 2.2** = Neutral (EBU/TV standard, no change)
- **Higher values** (>2.2) = Lighter image
- **Lower values** (<2.2) = Darker image
- Non-linear curve preserves shadow and highlight detail

### 🎯 Midtone-Focused Adjustment
Unlike linear brightness:
- Affects midtones more than extremes
- Preserves black and white points
- Natural-looking brightness changes
- Prevents clipping at endpoints

### ⚡ Mathematical Precision
- Proper gamma power curve calculation
- Based on industry standards (EBU, Rec. 709)
- Zero-division protection
- Accurate color space handling

### 🎬 Broadcast Standard
- **Gamma 2.2**: Standard for SDR video displays
- **Rec. 709**: HD video standard uses gamma 2.2
- **sRGB**: Computer displays approximate gamma 2.2
- Industry-standard reference point

### ⚡ Real-time Performance
- Fast power curve calculation
- Optimized shader code
- Suitable for video playback
- Interactive adjustment

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to apply gamma correction |
| **Gamma** | 0.01 - ∞ | 2.2 | Gamma value. 2.2 = neutral (EBU standard), higher = lighter, lower = darker. |

## Creative Usage Tips

### 🎬 Corrective Gamma Adjustment

**Darken Overly Bright Image:**
1. Image appears too bright/washed out
2. Add **Gamma Correction**
3. **Gamma**: 1.8 to 2.0 (lower than 2.2)
4. Result: Darker, more contained brightness

**Lighten Dark Image:**
1. Image appears too dark
2. Add **Gamma Correction**
3. **Gamma**: 2.6 to 3.0 (higher than 2.2)
4. Result: Lifted midtones, revealed detail

**Fine-Tune After Other Adjustments:**
1. After levels, contrast, color grading
2. Add **Gamma Correction**
3. **Gamma**: 2.1 to 2.3 (subtle adjustment)
4. Final brightness fine-tuning

**Compensate for Display Differences:**
1. Content looks different on different displays
2. Add **Gamma Correction**
3. **Gamma**: Adjust to match target display
4. Example: For bright projector, use lower gamma (1.9-2.0)

### 🎨 Creative Stylization

**High-Gamma Bright Look:**
1. **Gamma**: 2.8 to 3.5
2. Creates airy, bright aesthetic
3. Popular for beauty, fashion photography
4. Combine with slight desaturation for dreamy look

**Low-Gamma Moody Look:**
1. **Gamma**: 1.5 to 1.8
2. Creates dark, moody atmosphere
3. Popular for thriller, horror, dramatic scenes
4. Combine with reduced saturation for gritty feel

**Film Print Emulation:**
1. **Gamma**: 2.4 to 2.6
2. Simulates film print characteristics
3. Slightly brighter than video standard
4. Classic cinema look

**Monitor Calibration Simulation:**
1. **Gamma**: Adjust to simulate different displays
2. Mac displays: ~2.2
3. PC displays (older): ~2.4
4. Preview how content looks on different systems

### 🌈 Advanced Techniques

**Gamma Before vs After:**
- **Before other adjustments**: Sets overall brightness foundation
- **After other adjustments**: Fine-tunes final result
- Different placement creates different results

**Stacking Multiple Gamma Nodes:**
1. **First pass**: Major gamma correction (1.8 or 2.6)
2. **Second pass**: Fine-tuning (2.15 or 2.25)
3. Allows precise, incremental adjustment

**Gamma + Contrast Combo:**
1. **Gamma Correction**: Adjust overall brightness
2. **Color Grading - Basic (Contrast)**: Add punch
3. Order matters: Usually gamma first, then contrast

**Gamma for Different Content Types:**
- **CGI/3D Renders**: Often need gamma 2.4-2.6 (renders are darker)
- **Live Video**: Usually gamma 2.0-2.2 (already corrected)
- **Log Footage**: Needs significant gamma boost (2.6-3.2)
- **Scanned Film**: Depends on scanner, often 2.2-2.4

### 🎛️ Understanding Gamma Values

**Common Gamma Settings:**
- **1.0**: Linear (no gamma correction) - very dark
- **1.8**: Significantly darker than standard
- **2.0**: Moderately darker
- **2.2**: **Neutral/Standard** (EBU, Rec. 709, sRGB)
- **2.4**: Moderately lighter
- **2.6**: Significantly lighter
- **3.0+**: Very bright, high-key

**Gamma Adjustment Guidelines:**
- **Small adjustments**: ±0.1 to ±0.2 from 2.2
- **Moderate adjustments**: ±0.3 to ±0.5
- **Large adjustments**: ±0.6 to ±1.0
- **Extreme**: <1.5 or >3.0

**Visual Effects of Gamma:**
```
Gamma 1.8: ■■■□□□□□□□ (darker)
Gamma 2.2: ■■■■■□□□□□ (neutral)
Gamma 2.6: ■■■■■■■□□□ (lighter)
```

## Workflow Examples

### Example 1: Lighten Dark Image
1. Import dark, underexposed image
2. Add **Gamma Correction**
3. **Gamma**: 2.8
4. Result: Significantly lighter, midtones lifted
5. Fine-tune: Adjust to 2.6 or 3.0 as needed

### Example 2: Darken Bright Image
1. Import bright, overexposed image
2. Add **Gamma Correction**
3. **Gamma**: 1.9
4. Result: Darker overall, more controlled brightness
5. Fine-tune: Adjust to 1.8 or 2.0 as needed

### Example 3: Film Print Look
1. Modern digital video
2. Add **Gamma Correction**
3. **Gamma**: 2.5
4. Combine with:
   - **Color Grading - Basic**: Saturation 0.9, Contrast +0.1
   - **Levels Correction**: Base 0.52 (lifted blacks)
5. Result: Classic film print aesthetic

### Example 4: Log Footage Conversion
1. Import flat log footage (very dark)
2. Add **Gamma Correction**
3. **Gamma**: 3.0 to 3.5 (aggressive lift)
4. Then add other color grading
5. Result: Proper brightness for viewing

### Example 5: Display Calibration
1. Content for specific display (e.g., bright projector)
2. Add **Gamma Correction**
3. **Gamma**: 1.9 (compensate for bright projector)
4. Content now looks correct on that display

### Example 6: Subtle Fine-Tuning
1. After full color grade
2. Image slightly too dark
3. Add **Gamma Correction**
4. **Gamma**: 2.3 (subtle lift)
5. Final polish without re-doing entire grade

### Example 7: Extreme Moody Dark
1. Horror/thriller scene
2. Add **Gamma Correction**
3. **Gamma**: 1.5 (very dark)
4. Combine with:
   - **Color Grading - Basic**: Saturation 0.7, Contrast +0.2
   - **Color Grading - Tonal**: Cool blue tint in shadows
5. Result: Intense, dark, moody atmosphere

## Technical Details

- **Node Type**: Gamma Adjustment (UV→sRGB_StraightA)
- **Category**: Color Grading / Color Correction
- **Algorithm**: Power curve (gamma correction)
- **Standard**: Based on EBU/Rec. 709 gamma 2.2
- **Precision**: Full floating-point calculations
- **Performance**: Highly optimized, real-time capable

## Understanding the Algorithm

### Gamma Correction Formula
```
gamma_factor = 2.2 / Gamma
rgb = pow(rgb, gamma_factor)
```

**How it works:**
- When **Gamma = 2.2**: `gamma_factor = 2.2 / 2.2 = 1.0` → `pow(rgb, 1.0) = rgb` (no change)
- When **Gamma > 2.2**: `gamma_factor < 1.0` → Power curve less than 1 → **Lighter**
- When **Gamma < 2.2**: `gamma_factor > 1.0` → Power curve greater than 1 → **Darker**

**Examples:**
```
Gamma 2.8: factor = 2.2/2.8 = 0.786 → pow(rgb, 0.786) = lighter
Gamma 1.8: factor = 2.2/1.8 = 1.222 → pow(rgb, 1.222) = darker
```

### Why Gamma 2.2 is Neutral

**Historical Background:**
- **CRT Displays**: Had inherent gamma of ~2.5
- **Compensation**: Signals pre-corrected with gamma ~0.45 (1/2.2)
- **Combined**: 0.45 × 2.5 ≈ 1.1 (approximately linear)
- **Modern Standard**: Gamma 2.2 became the reference

**Standards:**
- **Rec. 709** (HDTV): Gamma 2.2 (approximately)
- **sRGB** (Computer): Gamma 2.2 (approximately)
- **EBU**: Gamma 2.2 reference

### Gamma vs Linear Brightness

**Linear Brightness:**
```
rgb = rgb + adjustment
```
- Adds same amount to all pixels
- Can cause clipping
- Less natural-looking

**Gamma Correction:**
```
rgb = pow(rgb, factor)
```
- Non-linear power curve
- Affects midtones more than extremes
- More natural, preserves detail

**Comparison:**
```
        Linear  Gamma
Black:  0.0     0.0    (unchanged)
Dark:   0.2     0.3    (gamma lifts more)
Mid:    0.5     0.7    (significant lift)
Bright: 0.8     0.9    (slight lift)
White:  1.0     1.0    (unchanged)
```

## Best Practices

### 🎯 When to Use Gamma Correction

**Use Gamma When:**
- ✅ Need overall brightness adjustment
- ✅ Working with log or flat footage
- ✅ Compensating for display differences
- ✅ Fine-tuning after other color grading
- ✅ Emulating film/broadcast standards

**Use Other Tools When:**
- ❌ Need selective tonal control → Use **Levels Correction**
- ❌ Need shadow/mid/highlight separation → Use **Color Grading - Tonal**
- ❌ Need contrast adjustment → Use **Color Grading - Basic**

### 💡 Adjustment Guidelines

**Subtle Correction:**
- Gamma: 2.1 to 2.3
- Barely noticeable, fine-tuning
- Final polish adjustments

**Moderate Correction:**
- Gamma: 1.8 to 2.0 (darker) or 2.4 to 2.8 (lighter)
- Visible but natural change
- Most common adjustments

**Strong Correction:**
- Gamma: 1.5 to 1.7 (very dark) or 2.9 to 3.5 (very light)
- Dramatic change
- Log footage, extreme stylization

**Extreme:**
- Gamma: <1.5 or >3.5
- Extreme looks, special cases
- May require additional adjustments

### ⚠️ Common Mistakes to Avoid

- ❌ Using gamma when levels would be better (for black/white point adjustment)
- ❌ Extreme gamma values without checking result
- ❌ Forgetting gamma 2.2 is neutral (not 1.0!)
- ❌ Not compensating for other adjustments
- ❌ Using linear brightness thinking instead of gamma thinking

## Combining with Other Nodes

**Essential Workflow Companions:**
- **⭐ Levels Correction**: Set black/white points, then gamma
- **🎨 Color Grading - Basic**: Contrast, saturation after gamma
- **💡 Color Grading - Tonal**: Selective adjustments after gamma
- **🔧 Additional Gamma Correction**: Fine-tune with second instance

**Recommended Workflows:**

**Standard Color Correction:**
```
Image → Levels Correction (set tonal range)
      → Gamma Correction (overall brightness)
      → Color Grading - Basic (contrast, saturation)
      → Output
```

**Log Footage Workflow:**
```
Log Footage → Gamma Correction (initial lift, 2.8-3.2)
            → Levels Correction (set blacks/whites)
            → Color Grading - Tonal (selective work)
            → Gamma Correction (final fine-tune, 2.1-2.3)
            → Output
```

**Display Compensation:**
```
Graded Image → Gamma Correction (adjust for target display)
             → Output to specific display
```

**Film Emulation:**
```
Image → Levels Correction (lift blacks slightly)
      → Gamma Correction (2.4-2.6)
      → Color Grading - Basic (reduce saturation, add contrast)
      → Output
```

## Troubleshooting Guide

### Problem: Image too bright after gamma adjustment
**Solutions**:
- ✅ Reduce **Gamma** value (try 2.0 or less)
- ✅ Check if you need Levels Correction instead
- ✅ Combine with contrast reduction
- ✅ May need to darken shadows specifically (use Tonal grading)

### Problem: Image too dark after gamma adjustment
**Solutions**:
- ✅ Increase **Gamma** value (try 2.4 or higher)
- ✅ Check if source material is extremely underexposed
- ✅ May need Levels Correction first
- ✅ For log footage, may need very high gamma (3.0+)

### Problem: Midtones look washed out
**Solutions**:
- ✅ Reduce **Gamma** slightly
- ✅ Add contrast with **Color Grading - Basic**
- ✅ Use **Color Grading - Tonal** for selective midtone adjustment
- ✅ Check if saturation also needs adjustment

### Problem: Lost detail in shadows or highlights
**Solutions**:
- ✅ Gamma preserves endpoints, so check source material
- ✅ Use **Levels Correction** to establish proper black/white points first
- ✅ May need selective adjustment with **Color Grading - Tonal**
- ✅ Source may be clipped already

### Problem: Gamma adjustment looks unnatural
**Solutions**:
- ✅ You may be using too extreme a value
- ✅ Try smaller increments (±0.2 from 2.2)
- ✅ Check if other adjustments (contrast, saturation) are needed
- ✅ May need Levels or Tonal grading instead

### Problem: Don't know what gamma value to use
**Solutions**:
- ✅ Start at **2.2** (neutral)
- ✅ Increase in 0.2 increments if too dark
- ✅ Decrease in 0.2 increments if too bright
- ✅ Fine-tune in 0.1 increments
- ✅ Trust your eyes, preview on target display

## Performance Tips

- ✅ Extremely fast (power curve calculation)
- ✅ Real-time capable even with video
- ✅ Can stack multiple instances without issue
- ✅ Negligible performance impact
- ✅ Perfect for live grading

## Advanced Techniques

### Gamma for Different Source Types

**Digital Camera (Standard):**
- Usually needs minimal gamma: 2.1 to 2.3

**Log/Flat Profile:**
- Needs significant gamma: 2.6 to 3.5

**Film Scan:**
- Depends on scanner: 2.2 to 2.6

**CGI Render (Linear):**
- Needs inverse gamma: 2.2 to convert to sRGB

**Screen Capture:**
- Usually already gamma-corrected: 2.2

### Display-Specific Gamma

**Computer Monitor (sRGB):**
- Target gamma: 2.2

**Old PC Monitors:**
- Had gamma ~2.4
- Content for these: Use gamma 2.0

**Mac Displays (Older):**
- Had gamma ~1.8
- Content for these: Use gamma 2.4-2.5

**Projectors (Bright):**
- Often appear brighter
- Content for projector: Use gamma 1.9-2.0

**HDR Displays:**
- Use PQ or HLG gamma curves (not simple gamma 2.2)
- This node is for SDR workflow

### Gamma in Color Spaces

**Linear RGB:**
- Gamma 1.0 (linear, no curve)

**sRGB:**
- Gamma ~2.2 (actually more complex curve)

**Adobe RGB:**
- Gamma 2.2 (exactly)

**ProPhoto RGB:**
- Gamma 1.8

**Rec. 709 (HD Video):**
- Gamma ~2.2 (transfer function)

### Two-Pass Gamma Technique

**First Pass (Major Correction):**
```
Gamma Correction: 2.8 (if too dark)
```

**Second Pass (Fine-Tuning):**
```
Gamma Correction: 2.15 (subtle adjustment)
```

**Why?** 
- Easier to dial in precise result
- Less chance of overshooting
- More control over final look

## Why This Node Was Created

Gamma correction is fundamental to video production. **Gamma Correction** provides:

- ✅ **Industry-standard gamma adjustment** (EBU 2.2 reference)
- ✅ **Simple single-parameter control**
- ✅ **Professional power curve** mathematics
- ✅ **Essential for display compensation**
- ✅ **Foundation of brightness workflows**
- ✅ **Real-time interactive adjustment**

This is the same fundamental gamma tool used in professional video production, now in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#gamma-correction---documentation) | [Deutsch](#gamma-correction---dokumentation)

---

# Gamma Correction - Dokumentation

## Übersicht

**Gamma Correction** ist ein fundamentales Tool zur Anpassung der gesamten Helligkeitskurve Ihres Bildes mittels Gammawerten. Dieser Ein-Parameter-Node bietet professionelle Gamma-Kontrolle basierend auf dem EBU/TV-Standard (Gamma 2.2) und ermöglicht es Ihnen, Ihr Bild mit einer mathematisch korrekten Power-Kurve aufzuhellen oder abzudunkeln, die Mitteltöne mehr als Schatten oder Highlights betrifft.

## 🎯 Inspiration & Design-Philosophie

Basierend auf der Broadcast- und Display-Standard-Gammakorrektur:

- **Ein-Parameter-Einfachheit**: Eine Kontrolle, kraftvolle Ergebnisse
- **EBU/TV-Standard**: Basierend auf Gamma-2.2-Referenz (Standard für Video-Displays)
- **Nicht-lineare Anpassung**: Power-Kurve betrifft primär Mitteltöne
- **Professioneller Standard**: Dieselbe Gammakorrektur, die in Broadcast-Workflows genutzt wird
- **Mathematische Präzision**: Korrekte Gamma-Mathematik für genaue Ergebnisse

Dieser Node bringt Broadcast-Standard-Gammakorrektur zu Coollab und bietet das fundamentale Helligkeits-Anpassungstool, das in der gesamten Videoproduktions-Industrie genutzt wird.

## ⭐ Hauptmerkmale

### 📐 Standard-Gammakorrektur
Professionelle Gamma-Power-Kurve:
- **Gamma 2.2** = Neutral (EBU/TV-Standard, keine Änderung)
- **Höhere Werte** (>2.2) = Helleres Bild
- **Niedrigere Werte** (<2.2) = Dunkleres Bild
- Nicht-lineare Kurve erhält Schatten- und Highlight-Detail

### 🎯 Mittelton-fokussierte Anpassung
Im Gegensatz zu linearer Helligkeit:
- Betrifft Mitteltöne mehr als Extreme
- Erhält Schwarz- und Weißpunkte
- Natürlich aussehende Helligkeitsänderungen
- Verhindert Clipping an Endpunkten

### ⚡ Mathematische Präzision
- Korrekte Gamma-Power-Kurven-Berechnung
- Basierend auf Industrie-Standards (EBU, Rec. 709)
- Null-Divisions-Schutz
- Genaue Farbraum-Handhabung

### 🎬 Broadcast-Standard
- **Gamma 2.2**: Standard für SDR-Video-Displays
- **Rec. 709**: HD-Video-Standard nutzt Gamma 2.2
- **sRGB**: Computer-Displays approximieren Gamma 2.2
- Industrie-Standard-Referenzpunkt

### ⚡ Echtzeit-Performance
- Schnelle Power-Kurven-Berechnung
- Optimierter Shader-Code
- Geeignet für Video-Wiedergabe
- Interaktive Anpassung

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das Bild für Gammakorrektur |
| **Gamma** | 0.01 - ∞ | 2.2 | Gammawert. 2.2 = neutral (EBU-Standard), höher = heller, niedriger = dunkler. |

## 🎨 Kreative Nutzungstipps

### 🎬 Korrigierende Gamma-Anpassung

**Zu helles Bild abdunkeln:**
1. Bild erscheint zu hell/ausgewaschen
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 1.8 bis 2.0 (niedriger als 2.2)
4. Ergebnis: Dunkler, kontrollierte Helligkeit

**Dunkles Bild aufhellen:**
1. Bild erscheint zu dunkel
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 2.6 bis 3.0 (höher als 2.2)
4. Ergebnis: Gehobene Mitteltöne, enthülltes Detail

**Feinabstimmung nach anderen Anpassungen:**
1. Nach Levels, Kontrast, Color Grading
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 2.1 bis 2.3 (subtile Anpassung)
4. Finale Helligkeits-Feinabstimmung

**Kompensation für Display-Unterschiede:**
1. Inhalt sieht auf verschiedenen Displays unterschiedlich aus
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: Anpassen zum Angleichen an Ziel-Display
4. Beispiel: Für hellen Projektor, nutzen Sie niedrigeres Gamma (1.9-2.0)

### 🎨 Kreative Stilisierung

**High-Gamma-Heller-Look:**
1. **Gamma**: 2.8 bis 3.5
2. Erzeugt luftige, helle Ästhetik
3. Beliebt für Beauty-, Mode-Fotografie
4. Mit leichter Entsättigung für verträumten Look kombinieren

**Low-Gamma-Stimmungsvoller-Look:**
1. **Gamma**: 1.5 bis 1.8
2. Erzeugt dunkle, stimmungsvolle Atmosphäre
3. Beliebt für Thriller, Horror, dramatische Szenen
4. Mit reduzierter Sättigung für körniges Gefühl kombinieren

**Film-Print-Emulation:**
1. **Gamma**: 2.4 bis 2.6
2. Simuliert Film-Print-Charakteristika
3. Leicht heller als Video-Standard
4. Klassischer Kino-Look

**Monitor-Kalibrierungs-Simulation:**
1. **Gamma**: Anpassen zur Simulation verschiedener Displays
2. Mac-Displays: ~2.2
3. PC-Displays (älter): ~2.4
4. Vorschau, wie Inhalt auf verschiedenen Systemen aussieht

### 🌈 Fortgeschrittene Techniken

**Gamma Vorher vs Nachher:**
- **Vor anderen Anpassungen**: Setzt gesamte Helligkeits-Grundlage
- **Nach anderen Anpassungen**: Feinabstimmung finales Ergebnis
- Unterschiedliche Platzierung erzeugt unterschiedliche Ergebnisse

**Mehrere Gamma-Nodes stapeln:**
1. **Erster Pass**: Große Gammakorrektur (1.8 oder 2.6)
2. **Zweiter Pass**: Feinabstimmung (2.15 oder 2.25)
3. Ermöglicht präzise, inkrementelle Anpassung

**Gamma + Kontrast Combo:**
1. **Gamma Correction**: Gesamthelligkeit anpassen
2. **Color Grading - Basic (Contrast)**: Punch hinzufügen
3. Reihenfolge zählt: Normalerweise Gamma zuerst, dann Kontrast

**Gamma für verschiedene Inhaltstypen:**
- **CGI/3D-Renders**: Brauchen oft Gamma 2.4-2.6 (Renders sind dunkler)
- **Live-Video**: Normalerweise Gamma 2.0-2.2 (bereits korrigiert)
- **Log-Footage**: Braucht signifikanten Gamma-Boost (2.6-3.2)
- **Gescannter Film**: Abhängig vom Scanner, oft 2.2-2.4

### 🎛️ Gammawerte verstehen

**Häufige Gamma-Einstellungen:**
- **1.0**: Linear (keine Gammakorrektur) - sehr dunkel
- **1.8**: Signifikant dunkler als Standard
- **2.0**: Moderat dunkler
- **2.2**: **Neutral/Standard** (EBU, Rec. 709, sRGB)
- **2.4**: Moderat heller
- **2.6**: Signifikant heller
- **3.0+**: Sehr hell, High-Key

**Gamma-Anpassungs-Richtlinien:**
- **Kleine Anpassungen**: ±0.1 bis ±0.2 von 2.2
- **Moderate Anpassungen**: ±0.3 bis ±0.5
- **Große Anpassungen**: ±0.6 bis ±1.0
- **Extrem**: <1.5 oder >3.0

**Visuelle Effekte von Gamma:**
```
Gamma 1.8: ■■■□□□□□□□ (dunkler)
Gamma 2.2: ■■■■■□□□□□ (neutral)
Gamma 2.6: ■■■■■■■□□□ (heller)
```

## 💡 Workflow-Beispiele

### Beispiel 1: Dunkles Bild aufhellen
1. Importieren Sie dunkles, unterbelichtetes Bild
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 2.8
4. Ergebnis: Signifikant heller, Mitteltöne gehoben
5. Feinabstimmung: Anpassen auf 2.6 oder 3.0 nach Bedarf

### Beispiel 2: Helles Bild abdunkeln
1. Importieren Sie helles, überbelichtetes Bild
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 1.9
4. Ergebnis: Insgesamt dunkler, kontrolliertere Helligkeit
5. Feinabstimmung: Anpassen auf 1.8 oder 2.0 nach Bedarf

### Beispiel 3: Film-Print-Look
1. Modernes Digital-Video
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 2.5
4. Kombinieren mit:
   - **Color Grading - Basic**: Saturation 0.9, Contrast +0.1
   - **Levels Correction**: Base 0.52 (gehobene Schwarztöne)
5. Ergebnis: Klassische Film-Print-Ästhetik

### Beispiel 4: Log-Footage-Konversion
1. Importieren Sie flache Log-Footage (sehr dunkel)
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 3.0 bis 3.5 (aggressives Heben)
4. Dann weiteres Color Grading hinzufügen
5. Ergebnis: Korrekte Helligkeit zum Betrachten

### Beispiel 5: Display-Kalibrierung
1. Inhalt für spezifisches Display (z.B. heller Projektor)
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 1.9 (kompensieren für hellen Projektor)
4. Inhalt sieht jetzt korrekt auf diesem Display aus

### Beispiel 6: Subtile Feinabstimmung
1. Nach vollständigem Color Grade
2. Bild leicht zu dunkel
3. Fügen Sie **Gamma Correction** hinzu
4. **Gamma**: 2.3 (subtiles Heben)
5. Finaler Polish ohne erneutes komplettes Grading

### Beispiel 7: Extremes Stimmungsvolles Dunkel
1. Horror/Thriller-Szene
2. Fügen Sie **Gamma Correction** hinzu
3. **Gamma**: 1.5 (sehr dunkel)
4. Kombinieren mit:
   - **Color Grading - Basic**: Saturation 0.7, Contrast +0.2
   - **Color Grading - Tonal**: Kühle blaue Tönung in Schatten
5. Ergebnis: Intensive, dunkle, stimmungsvolle Atmosphäre

## 🔧 Technische Details

- **Node-Typ**: Gamma Adjustment (UV→sRGB_StraightA)
- **Kategorie**: Color Grading / Color Correction
- **Algorithmus**: Power-Kurve (Gammakorrektur)
- **Standard**: Basierend auf EBU/Rec. 709 Gamma 2.2
- **Präzision**: Vollständige Fließkomma-Berechnungen
- **Performance**: Hoch optimiert, echtzeit-fähig

## 🧮 Verständnis des Algorithmus

### Gammakorrektur-Formel
```
gamma_factor = 2.2 / Gamma
rgb = pow(rgb, gamma_factor)
```

**Wie es funktioniert:**
- Wenn **Gamma = 2.2**: `gamma_factor = 2.2 / 2.2 = 1.0` → `pow(rgb, 1.0) = rgb` (keine Änderung)
- Wenn **Gamma > 2.2**: `gamma_factor < 1.0` → Power-Kurve weniger als 1 → **Heller**
- Wenn **Gamma < 2.2**: `gamma_factor > 1.0` → Power-Kurve größer als 1 → **Dunkler**

**Beispiele:**
```
Gamma 2.8: Faktor = 2.2/2.8 = 0.786 → pow(rgb, 0.786) = heller
Gamma 1.8: Faktor = 2.2/1.8 = 1.222 → pow(rgb, 1.222) = dunkler
```

### Warum Gamma 2.2 neutral ist

**Historischer Hintergrund:**
- **CRT-Displays**: Hatten inherentes Gamma von ~2.5
- **Kompensation**: Signale vorkorrigiert mit Gamma ~0.45 (1/2.2)
- **Kombiniert**: 0.45 × 2.5 ≈ 1.1 (ungefähr linear)
- **Moderner Standard**: Gamma 2.2 wurde die Referenz

**Standards:**
- **Rec. 709** (HDTV): Gamma 2.2 (ungefähr)
- **sRGB** (Computer): Gamma 2.2 (ungefähr)
- **EBU**: Gamma 2.2 Referenz

### Gamma vs Lineare Helligkeit

**Lineare Helligkeit:**
```
rgb = rgb + adjustment
```
- Addiert gleiche Menge zu allen Pixeln
- Kann Clipping verursachen
- Weniger natürlich aussehend

**Gammakorrektur:**
```
rgb = pow(rgb, factor)
```
- Nicht-lineare Power-Kurve
- Betrifft Mitteltöne mehr als Extreme
- Natürlicher, erhält Detail

**Vergleich:**
```
        Linear  Gamma
Schwarz: 0.0    0.0    (unverändert)
Dunkel:  0.2    0.3    (Gamma hebt mehr)
Mitte:   0.5    0.7    (signifikantes Heben)
Hell:    0.8    0.9    (leichtes Heben)
Weiß:    1.0    1.0    (unverändert)
```

## 🎬 Best Practices

### 🎯 Wann Gammakorrektur nutzen

**Gamma nutzen wenn:**
- ✅ Gesamte Helligkeits-Anpassung nötig
- ✅ Mit Log oder flacher Footage arbeiten
- ✅ Kompensation für Display-Unterschiede
- ✅ Feinabstimmung nach anderem Color Grading
- ✅ Emulation von Film/Broadcast-Standards

**Andere Tools nutzen wenn:**
- ❌ Selektive Ton-Kontrolle nötig → Nutzen Sie **Levels Correction**
- ❌ Schatten/Mid/Highlight-Trennung nötig → Nutzen Sie **Color Grading - Tonal**
- ❌ Kontrast-Anpassung nötig → Nutzen Sie **Color Grading - Basic**

### 💡 Anpassungs-Richtlinien

**Subtile Korrektur:**
- Gamma: 2.1 bis 2.3
- Kaum merklich, Feinabstimmung
- Finale Polish-Anpassungen

**Moderate Korrektur:**
- Gamma: 1.8 bis 2.0 (dunkler) oder 2.4 bis 2.8 (heller)
- Sichtbare aber natürliche Änderung
- Häufigste Anpassungen

**Starke Korrektur:**
- Gamma: 1.5 bis 1.7 (sehr dunkel) oder 2.9 bis 3.5 (sehr hell)
- Dramatische Änderung
- Log-Footage, extreme Stilisierung

**Extrem:**
- Gamma: <1.5 oder >3.5
- Extreme Looks, Sonderfälle
- Könnte zusätzliche Anpassungen erfordern

### ⚠️ Häufige Fehler vermeiden

- ❌ Gamma nutzen wenn Levels besser wäre (für Schwarz/Weiß-Punkt-Anpassung)
- ❌ Extreme Gamma-Werte ohne Ergebnis-Prüfung
- ❌ Vergessen, dass Gamma 2.2 neutral ist (nicht 1.0!)
- ❌ Nicht für andere Anpassungen kompensieren
- ❌ Lineares Helligkeits-Denken statt Gamma-Denken nutzen

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **⭐ Levels Correction**: Schwarz/Weiß-Punkte setzen, dann Gamma
- **🎨 Color Grading - Basic**: Kontrast, Sättigung nach Gamma
- **💡 Color Grading - Tonal**: Selektive Anpassungen nach Gamma
- **🔧 Zusätzliche Gamma Correction**: Feinabstimmung mit zweiter Instanz

**Empfohlene Workflows:**

**Standard-Farbkorrektur:**
```
Image → Levels Correction (Tonbereich setzen)
      → Gamma Correction (Gesamthelligkeit)
      → Color Grading - Basic (Kontrast, Sättigung)
      → Output
```

**Log-Footage-Workflow:**
```
Log Footage → Gamma Correction (initialer Lift, 2.8-3.2)
            → Levels Correction (Schwarztöne/Weißtöne setzen)
            → Color Grading - Tonal (selektive Arbeit)
            → Gamma Correction (finale Feinabstimmung, 2.1-2.3)
            → Output
```

**Display-Kompensation:**
```
Graded Image → Gamma Correction (für Ziel-Display anpassen)
             → Output zu spezifischem Display
```

**Film-Emulation:**
```
Image → Levels Correction (Schwarztöne leicht heben)
      → Gamma Correction (2.4-2.6)
      → Color Grading - Basic (Sättigung reduzieren, Kontrast hinzufügen)
      → Output
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Bild zu hell nach Gamma-Anpassung
**Lösungen**:
- ✅ **Gamma**-Wert reduzieren (versuchen Sie 2.0 oder weniger)
- ✅ Prüfen Sie, ob Sie stattdessen Levels Correction brauchen
- ✅ Mit Kontrast-Reduktion kombinieren
- ✅ Könnte Schatten speziell abdunkeln müssen (Tonal Grading nutzen)

### Problem: Bild zu dunkel nach Gamma-Anpassung
**Lösungen**:
- ✅ **Gamma**-Wert erhöhen (versuchen Sie 2.4 oder höher)
- ✅ Prüfen Sie, ob Quellmaterial extrem unterbelichtet ist
- ✅ Könnte zuerst Levels Correction brauchen
- ✅ Für Log-Footage könnte sehr hohes Gamma nötig sein (3.0+)

### Problem: Mitteltöne sehen ausgewaschen aus
**Lösungen**:
- ✅ **Gamma** leicht reduzieren
- ✅ Kontrast mit **Color Grading - Basic** hinzufügen
- ✅ **Color Grading - Tonal** für selektive Mittelton-Anpassung nutzen
- ✅ Prüfen Sie, ob auch Sättigung Anpassung braucht

### Problem: Verlust von Detail in Schatten oder Highlights
**Lösungen**:
- ✅ Gamma erhält Endpunkte, also Quellmaterial prüfen
- ✅ **Levels Correction** nutzen, um zuerst korrekte Schwarz/Weiß-Punkte zu etablieren
- ✅ Könnte selektive Anpassung mit **Color Grading - Tonal** brauchen
- ✅ Quelle könnte bereits geclippt sein

### Problem: Gamma-Anpassung sieht unnatürlich aus
**Lösungen**:
- ✅ Sie könnten zu extremen Wert nutzen
- ✅ Kleinere Inkremente versuchen (±0.2 von 2.2)
- ✅ Prüfen Sie, ob andere Anpassungen (Kontrast, Sättigung) nötig sind
- ✅ Könnte stattdessen Levels oder Tonal Grading brauchen

### Problem: Weiß nicht, welchen Gamma-Wert zu nutzen
**Lösungen**:
- ✅ Starten bei **2.2** (neutral)
- ✅ In 0.2-Schritten erhöhen falls zu dunkel
- ✅ In 0.2-Schritten verringern falls zu hell
- ✅ Feinabstimmung in 0.1-Schritten
- ✅ Vertrauen Sie Ihren Augen, Vorschau auf Ziel-Display

## ⚡ Performance-Tipps

- ✅ Extrem schnell (Power-Kurven-Berechnung)
- ✅ Echtzeit-fähig auch mit Video
- ✅ Kann mehrere Instanzen stapeln ohne Problem
- ✅ Vernachlässigbare Performance-Auswirkung
- ✅ Perfekt für Live-Grading

## 🎓 Fortgeschrittene Techniken

### Gamma für verschiedene Quelltypen

**Digital-Kamera (Standard):**
- Braucht normalerweise minimales Gamma: 2.1 bis 2.3

**Log/Flat-Profil:**
- Braucht signifikantes Gamma: 2.6 bis 3.5

**Film-Scan:**
- Abhängig vom Scanner: 2.2 bis 2.6

**CGI-Render (Linear):**
- Braucht inverses Gamma: 2.2 zur Konversion zu sRGB

**Screen-Capture:**
- Normalerweise bereits gamma-korrigiert: 2.2

### Display-spezifisches Gamma

**Computer-Monitor (sRGB):**
- Ziel-Gamma: 2.2

**Alte PC-Monitore:**
- Hatten Gamma ~2.4
- Inhalt für diese: Nutzen Sie Gamma 2.0

**Mac-Displays (Älter):**
- Hatten Gamma ~1.8
- Inhalt für diese: Nutzen Sie Gamma 2.4-2.5

**Projektoren (Hell):**
- Erscheinen oft heller
- Inhalt für Projektor: Nutzen Sie Gamma 1.9-2.0

**HDR-Displays:**
- Nutzen PQ oder HLG Gamma-Kurven (nicht simples Gamma 2.2)
- Dieser Node ist für SDR-Workflow

### Gamma in Farbräumen

**Linear RGB:**
- Gamma 1.0 (linear, keine Kurve)

**sRGB:**
- Gamma ~2.2 (tatsächlich komplexere Kurve)

**Adobe RGB:**
- Gamma 2.2 (exakt)

**ProPhoto RGB:**
- Gamma 1.8

**Rec. 709 (HD Video):**
- Gamma ~2.2 (Transfer-Funktion)

### Zwei-Pass-Gamma-Technik

**Erster Pass (Große Korrektur):**
```
Gamma Correction: 2.8 (falls zu dunkel)
```

**Zweiter Pass (Feinabstimmung):**
```
Gamma Correction: 2.15 (subtile Anpassung)
```

**Warum?**
- Einfacher, präzises Ergebnis einzustellen
- Geringere Chance zu überschiessen
- Mehr Kontrolle über finalen Look

## 💡 Warum dieser Node erstellt wurde

Gammakorrektur ist fundamental für Videoproduktion. **Gamma Correction** bietet:

- ✅ **Industrie-standard Gamma-Anpassung** (EBU 2.2 Referenz)
- ✅ **Einfache Ein-Parameter-Kontrolle**
- ✅ **Professionelle Power-Kurven**-Mathematik
- ✅ **Essentiell für Display-Kompensation**
- ✅ **Grundlage von Helligkeits-Workflows**
- ✅ **Echtzeit-interaktive Anpassung**

Dies ist dasselbe fundamentale Gamma-Tool, das in professioneller Videoproduktion genutzt wird, jetzt in Coollab!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
