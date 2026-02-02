[English](#color-grading---tonal---documentation) | [Deutsch](#color-grading---tonal---dokumentation)

---

# Color Grading - Classical - Documentation

## Overview

**Color Grading - Classical** provides professional three-way color correction, giving you independent control over shadows, midtones, and highlights. This is the cornerstone of professional color grading workflows used in cinema and broadcast, allowing you to adjust the intensity and hue of different tonal regions separately for precise, targeted color correction and creative looks.

## Inspiration & Design Philosophy

Based on the professional three-way color corrector found in high-end grading suites:

- **Tonal Separation**: Independent control over shadows, mids, and highlights
- **Dual Control**: Both intensity (brightness) and hue shift for each tonal range
- **Masked Adjustments**: Changes smoothly blend at tonal boundaries
- **Professional Workflow**: The same tool used by Hollywood colorists
- **Creative Freedom**: Precise control for both correction and stylization

This node brings professional three-way color correction to Coollab, enabling the kind of selective tonal work that defines high-end color grading.

## Key Features

### 🌑 Shadows Control
Affect only the dark areas:
- **Intensity**: Brighten or darken shadows (-1 to +1)
- **Hue Shift**: Add color tint to shadows only (0 to 1 = 0° to 360°)
- **Auto-Masked**: Affects only pixels with low luminance (<0.33)

### 🌓 Mids Control
Affect only the midtones:
- **Intensity**: Brighten or darken midtones (-1 to +1)
- **Hue Shift**: Add color tint to midtones only (0 to 1 = 0° to 360°)
- **Auto-Masked**: Affects middle luminance range (~0.33-0.66)

### 🌕 Highlights Control
Affect only the bright areas:
- **Intensity**: Brighten or darken highlights (-1 to +1)
- **Hue Shift**: Add color tint to highlights only (0 to 1 = 0° to 360°)
- **Auto-Masked**: Affects only pixels with high luminance (>0.66)

### 🎭 Automatic Masking
- Smart luminance-based masks
- Smooth transitions between tonal regions
- No manual masking required
- Professional smoothstep blending

### ⚡ Real-time Performance
- Fast HSV conversion
- Optimized masking calculations
- Suitable for video playback
- Interactive adjustment feedback

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to grade |
| **Highlights Intensity** | -1.0 - 1.0 | 0.0 | Adjust brightness of highlights. Negative = darker, positive = brighter. |
| **Highlights Hue Shift** | 0.0 - 1.0 | 0.0 | Shift hue in highlights (0 to 1 = 0° to 360°). |
| **Mids Intensity** | -1.0 - 1.0 | 0.0 | Adjust brightness of midtones. Negative = darker, positive = brighter. |
| **Mids Hue Shift** | 0.0 - 1.0 | 0.0 | Shift hue in midtones (0 to 1 = 0° to 360°). |
| **Shadows Intensity** | -1.0 - 1.0 | 0.0 | Adjust brightness of shadows. Negative = darker, positive = brighter. |
| **Shadows Hue Shift** | 0.0 - 1.0 | 0.0 | Shift hue in shadows (0 to 1 = 0° to 360°). |

## Creative Usage Tips

### 🎬 Corrective Color Grading

**Split-Tone Correction:**
1. Warm shadows, cool highlights (classic film look)
2. **Shadows Hue Shift**: 0.05-0.08 (warm orange/yellow)
3. **Highlights Hue Shift**: 0.55-0.6 (cool cyan/blue)
4. Keep **Intensity** values at 0.0
5. Creates dimensional, filmic separation

**Shadow Detail Recovery:**
1. Image with blocked-up, dark shadows
2. **Shadows Intensity**: +0.2 to +0.4 (lift shadows)
3. **Mids Intensity**: -0.05 to -0.1 (compensate to prevent washout)
4. **Highlights Intensity**: 0.0 (keep highlights)
5. Reveals hidden shadow detail

**Highlight Detail Protection:**
1. Overexposed highlights losing detail
2. **Highlights Intensity**: -0.15 to -0.3 (pull down highlights)
3. **Mids Intensity**: +0.05 to +0.1 (compensate midtones)
4. **Shadows Intensity**: 0.0 (keep shadows)
5. Recovers blown highlights

**Color Cast Removal:**
1. Unwanted color tint in specific tonal range
2. Identify which range has the cast (shadows/mids/highlights)
3. Use corresponding **Hue Shift** to counteract
4. Example: Green cast in shadows → Shadows Hue Shift to magenta (0.83)
5. Selective correction without affecting entire image

### 🎨 Creative Stylization

**Teal & Orange Look (Blockbuster):**
1. **Shadows Hue Shift**: 0.05 (warm orange)
2. **Shadows Intensity**: +0.05 (slight lift)
3. **Highlights Hue Shift**: 0.52 (teal/cyan)
4. **Highlights Intensity**: 0.0
5. **Mids**: Leave neutral or subtle warm (0.02)
6. Classic modern cinema look

**Golden Hour Effect:**
1. **Shadows Hue Shift**: 0.08 (warm orange)
2. **Shadows Intensity**: -0.1 (deepen shadows)
3. **Mids Hue Shift**: 0.06 (golden yellow)
4. **Mids Intensity**: +0.05 (lift)
5. **Highlights Hue Shift**: 0.10 (warm yellow)
6. **Highlights Intensity**: +0.1 (bright)
7. Simulates sunset/sunrise lighting

**Cool Moonlight:**
1. **Shadows Hue Shift**: 0.62 (deep blue)
2. **Shadows Intensity**: -0.15 (darken)
3. **Mids Hue Shift**: 0.58 (blue-cyan)
4. **Mids Intensity**: -0.05 (slightly darker)
5. **Highlights Hue Shift**: 0.54 (cyan)
6. **Highlights Intensity**: +0.05 (slightly brighter)
7. Creates nighttime/moonlit aesthetic

**Cross-Processing Effect:**
1. **Shadows Hue Shift**: 0.55 (cyan)
2. **Shadows Intensity**: +0.1 (lift)
3. **Highlights Hue Shift**: 0.08 (yellow-orange)
4. **Highlights Intensity**: -0.05 (compress)
5. **Mids**: Leave neutral
6. Vintage cross-processed film look

**Vintage Sepia Tone:**
1. First desaturate image (Color Grading - Basic, Saturation = 0.3)
2. **Shadows Hue Shift**: 0.06 (warm brown)
3. **Mids Hue Shift**: 0.08 (sepia)
4. **Highlights Hue Shift**: 0.10 (light sepia/cream)
5. All **Intensity** values: 0.0
6. Classic sepia photograph look

**High-Contrast Drama:**
1. **Shadows Intensity**: -0.3 (crush blacks)
2. **Shadows Hue Shift**: 0.6 (add blue tint)
3. **Highlights Intensity**: +0.2 (blow out highlights)
4. **Highlights Hue Shift**: 0.05 (warm highlights)
5. **Mids Intensity**: -0.05 (slight compression)
6. Creates dramatic, contrasty look

### 🌈 Advanced Techniques

**Complementary Split Tone:**
1. Choose two complementary colors (opposite on color wheel)
2. **Shadows Hue Shift**: Color A (e.g., 0.05 = orange)
3. **Highlights Hue Shift**: Color B (e.g., 0.55 = cyan)
4. **Mids**: Neutral or blend (0.3 between the two)
5. Maximum color contrast and visual interest

**Graduated Color Shift:**
1. **Shadows Hue Shift**: Starting color (e.g., 0.0 = red)
2. **Mids Hue Shift**: Middle color (e.g., 0.08 = orange)
3. **Highlights Hue Shift**: End color (e.g., 0.16 = yellow)
4. Creates smooth color gradient across tonal range

**Selective Tonal Boost:**
1. Identify which range needs more punch
2. Boost only that range's **Intensity**
3. Example: Flat midtones → **Mids Intensity**: +0.15
4. Leaves shadows and highlights untouched
5. Targeted enhancement without global changes

**Color Temperature Correction:**
1. Image too warm overall
2. **Shadows Hue Shift**: 0.5-0.6 (cool it down in shadows)
3. **Mids Hue Shift**: 0.52-0.58 (cool midtones)
4. **Highlights Hue Shift**: 0.54-0.6 (cool highlights)
5. Different amounts per range for natural look

### 🎛️ Working with Intensity & Hue

**Understanding the Interaction:**
- **Intensity** affects brightness in that tonal range
- **Hue Shift** adds color tint to that range
- Both work together for complete tonal control

**Intensity Guidelines:**
- Subtle: ±0.05 to ±0.1
- Moderate: ±0.15 to ±0.25
- Strong: ±0.3 to ±0.5
- Extreme: ±0.6+

**Hue Shift Color Guide:**
- **0.0** = Red
- **0.05-0.08** = Orange (warm)
- **0.16** = Yellow
- **0.25-0.3** = Yellow-green
- **0.33** = Green
- **0.5** = Cyan
- **0.55-0.6** = Blue-cyan (cool)
- **0.66** = Blue
- **0.75** = Purple
- **0.83** = Magenta
- **0.91-0.99** = Red-pink

## Workflow Examples

### Example 1: Classic Teal & Orange
1. Load any image
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: 0.0
   - Hue Shift: 0.05 (orange)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.02 (subtle warm)
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.52 (teal)
6. Result: Modern blockbuster color palette

### Example 2: Recover Dark Shadows
1. Image with very dark, blocked shadows
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: +0.35 (aggressive lift)
   - Hue Shift: 0.0
4. **Mids**:
   - Intensity: -0.1 (darken to compensate)
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.0
6. Result: Revealed shadow detail without washing out

### Example 3: Golden Sunset Look
1. Daytime outdoor scene
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: -0.05 (slightly darker)
   - Hue Shift: 0.08 (warm orange)
4. **Mids**:
   - Intensity: +0.08 (lift)
   - Hue Shift: 0.07 (golden)
5. **Highlights**:
   - Intensity: +0.12 (bright)
   - Hue Shift: 0.10 (warm yellow)
6. Result: Beautiful golden hour aesthetic

### Example 4: Cool Night Scene
1. Any scene to convert to nighttime feel
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: -0.2 (darken significantly)
   - Hue Shift: 0.6 (deep blue)
4. **Mids**:
   - Intensity: -0.1 (darker)
   - Hue Shift: 0.58 (blue-cyan)
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.54 (cyan - moonlight)
6. Combine with **Color Grading - Basic** (reduce saturation to 0.7)
7. Result: Convincing nighttime look

### Example 5: Vintage Cross-Process
1. Portrait or fashion photo
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: +0.12 (lift)
   - Hue Shift: 0.55 (cyan-green)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: -0.08 (compress)
   - Hue Shift: 0.08 (yellow)
6. Result: Classic cross-processed film aesthetic

### Example 6: Selective Midtone Enhancement
1. Flat, low-contrast image
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: 0.0
   - Hue Shift: 0.0
4. **Mids**:
   - Intensity: +0.2 (significant boost)
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.0
6. Result: Punchy midtones, preserved shadows/highlights

### Example 7: Film Print Fade Emulation
1. Modern digital image
2. Add **Color Grading - Classical**
3. **Shadows**:
   - Intensity: +0.15 (lift - characteristic of faded prints)
   - Hue Shift: 0.05 (warm)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.06 (warm)
5. **Highlights**:
   - Intensity: -0.05 (slight compression)
   - Hue Shift: 0.08 (warm sepia)
6. Combine with reduced saturation (0.75)
7. Result: Vintage faded film print

## Technical Details

- **Node Type**: Tonal Color Grading (UV→sRGB_StraightA)
- **Category**: Color Grading / Color Correction
- **Algorithm**: Luminance-based masking + HSV hue/brightness
- **Masking**: Automatic smoothstep transitions
- **Color Space**: sRGB input/output, HSV for modifications
- **Performance**: Real-time capable, optimized

## Understanding the Algorithm

### Luminance Calculation
```
luma = dot(rgb, vec3(0.299, 0.587, 0.114))
```
- Standard Rec. 601 luminance calculation
- Determines which tonal range each pixel belongs to

### Tonal Masks
```
shadow_mask = smoothstep(0.33, 0.0, luma)
mid_mask = 1.0 - abs(luma - 0.5) × 2.0, then smoothstep
highlight_mask = smoothstep(0.66, 1.0, luma)
```
- **Shadow mask**: High for dark pixels (luma < 0.33)
- **Mid mask**: High for middle pixels (luma ~0.33-0.66)
- **Highlight mask**: High for bright pixels (luma > 0.66)
- **Smoothstep**: Creates soft transitions between ranges

### Intensity Application
```
rgb += Intensity × mask
```
- Additive brightness adjustment
- Masked to affect only specific tonal range
- Multiple adjustments accumulate

### Hue Shift Application
```
1. Convert RGB to HSV
2. total_hue_shift = (Highlights_Hue × highlight_mask) +
                     (Mids_Hue × mid_mask) +
                     (Shadows_Hue × shadow_mask)
3. hsv.hue = fract(hsv.hue + total_hue_shift)
4. Convert back to RGB
```
- Each hue shift is masked
- All shifts accumulate based on pixel's luminance
- Smooth blending at tonal boundaries

## Best Practices

### 🎯 Adjustment Strategy

**Work One Range at a Time:**
1. Start with **Shadows**
2. Then adjust **Highlights**
3. Finally fine-tune **Mids**
4. Review overall balance

**Start with Hue, Then Intensity:**
- Set color tints first (Hue Shift)
- Then adjust brightness (Intensity)
- Easier to see the effect

**Use Subtle Adjustments:**
- **Intensity**: ±0.1 to ±0.2 for most work
- **Hue Shift**: 0.02-0.1 for subtle tints
- Build up gradually

### 💡 Common Combinations

**Split Tone (Warm/Cool):**
- Shadows: Hue 0.05, Intensity 0.0
- Mids: Hue 0.0, Intensity 0.0
- Highlights: Hue 0.55, Intensity 0.0

**Shadow Lift:**
- Shadows: Hue 0.0, Intensity +0.2 to +0.4
- Mids: Hue 0.0, Intensity -0.05 to -0.1
- Highlights: Hue 0.0, Intensity 0.0

**Highlight Compression:**
- Shadows: Hue 0.0, Intensity 0.0
- Mids: Hue 0.0, Intensity +0.05
- Highlights: Hue 0.0, Intensity -0.2 to -0.3

### ⚠️ Common Mistakes to Avoid

- ❌ Extreme intensity values (±0.5+) on all ranges
- ❌ Clashing hue shifts (random colors in each range)
- ❌ Forgetting that adjustments accumulate
- ❌ Not considering the natural color harmony
- ❌ Oversaturating by using only hue shifts without checking result

## Combining with Other Nodes

**Essential Workflow Companions:**
- **⭐ Color Grading - Basic**: Use before or after for global adjustments
- **🎨 Levels Correction**: Set tonal foundation first
- **💡 Gamma Correction**: Overall gamma adjustment
- **🔧 Color Replace**: Additional selective color work
- **🌈 Additional Color Grading - Classical**: Stack for complex looks

**Recommended Workflows:**

**Professional Color Correction:**
```
Image → Levels Correction (establish tonal range)
      → Color Grading - Classical (selective tonal work)
      → Color Grading - Basic (final polish)
      → Output
```

**Cinematic Look:**
```
Image → Color Grading - Basic (contrast, saturation)
      → Color Grading - Classical (teal & orange split)
      → Gamma Correction (overall gamma)
      → Output
```

**Vintage Film Emulation:**
```
Image → Levels Correction (lift blacks)
      → Color Grading - Tonal (warm shadows, warm highlights)
      → Color Grading - Basic (reduce saturation)
      → Output
```

## Troubleshooting Guide

### Problem: Changes too subtle / not visible
**Solutions**:
- ✅ Increase **Intensity** values (try ±0.2 to ±0.3)
- ✅ Use more dramatic **Hue Shift** values (0.1+)
- ✅ Check if image has the tonal range you're adjusting
- ✅ Very dark image may not have highlights to adjust

### Problem: Colors look unnatural / weird
**Solutions**:
- ✅ Reduce **Hue Shift** amounts (use 0.02-0.08 for subtle)
- ✅ Consider color harmony (complementary vs analogous)
- ✅ Don't shift all three ranges to random colors
- ✅ Use reference images for color grading inspiration

### Problem: Lost detail in shadows after lifting
**Solutions**:
- ✅ Reduce **Shadows Intensity** (don't lift too much)
- ✅ Compensate with **Mids Intensity** reduction
- ✅ May need better source material
- ✅ Combine with Levels Correction for more control

### Problem: Highlights too bright / blown out
**Solutions**:
- ✅ Reduce **Highlights Intensity** (use negative values)
- ✅ Compensate with **Mids Intensity** boost
- ✅ May need Levels Correction to compress highlights first
- ✅ Check original footage exposure

### Problem: Muddy midtones
**Solutions**:
- ✅ Reduce **Mids Intensity** or set to negative
- ✅ Check if shadows and highlights are both being lifted
- ✅ Use **Color Grading - Basic** to add global contrast
- ✅ May need saturation boost

### Problem: Tonal ranges bleeding into each other
**Solutions**:
- ✅ This is normal - masks have soft transitions
- ✅ Use more extreme adjustments for clear separation
- ✅ Accept that mid-tones will show blend of adjustments
- ✅ This creates natural, professional results

## Performance Tips

- ✅ Fast HSV conversion
- ✅ Optimized masking calculations
- ✅ Real-time capable for video
- ✅ Can stack multiple instances
- ✅ Suitable for live performance

## Advanced Techniques

### Film Stock Emulation

**Kodak Portra (Warm, Portrait):**
- Shadows: Hue 0.05, Intensity -0.05
- Mids: Hue 0.04, Intensity +0.02
- Highlights: Hue 0.06, Intensity +0.05

**Fuji Velvia (Vivid Landscape):**
- Shadows: Hue 0.0, Intensity -0.1
- Mids: Hue 0.0, Intensity 0.0
- Highlights: Hue 0.0, Intensity +0.05
- Combine with high saturation (1.4)

**Cinestill 800T (Tungsten, Night):**
- Shadows: Hue 0.55, Intensity 0.0
- Mids: Hue 0.52, Intensity 0.0
- Highlights: Hue 0.08, Intensity +0.1 (warm halos)

### Time of Day Simulation

**Morning (Cool to Warm):**
- Shadows: Hue 0.58, Intensity 0.0
- Mids: Hue 0.05, Intensity +0.05
- Highlights: Hue 0.08, Intensity +0.1

**Afternoon (Neutral Bright):**
- Shadows: Hue 0.0, Intensity +0.05
- Mids: Hue 0.02, Intensity +0.05
- Highlights: Hue 0.0, Intensity 0.0

**Sunset (Golden):**
- Shadows: Hue 0.08, Intensity -0.05
- Mids: Hue 0.07, Intensity +0.08
- Highlights: Hue 0.10, Intensity +0.15

**Night (Blue/Cool):**
- Shadows: Hue 0.62, Intensity -0.2
- Mids: Hue 0.58, Intensity -0.1
- Highlights: Hue 0.54, Intensity 0.0

### Matching Shots in Sequence

1. **Reference Shot**: Grade your hero shot
2. **Note Values**: Record exact Intensity/Hue values
3. **Apply**: Use on other shots in sequence
4. **Fine-Tune**: Adjust for lighting differences
5. **Consistency**: Maintain overall look

## Why This Node Was Created

Professional color grading requires selective tonal control. **Color Grading - Classical** provides:

- ✅ **Industry-standard three-way correction**
- ✅ **Independent shadow/mid/highlight control**
- ✅ **Automatic tonal masking**
- ✅ **Both intensity and hue control** per range
- ✅ **Professional results** with intuitive interface
- ✅ **Creative freedom** for stylization

This is the same tool used by professional colorists, now in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#color-grading---tonal---documentation) | [Deutsch](#color-grading---Classical---dokumentation)

---

# Color Grading - Classical - Dokumentation

## Übersicht

**Color Grading - Classical** bietet professionelle Drei-Wege-Farbkorrektur und gibt Ihnen unabhängige Kontrolle über Schatten, Mitteltöne und Highlights. Dies ist der Eckpfeiler professioneller Color-Grading-Workflows in Kino und Broadcast und ermöglicht es Ihnen, Intensität und Farbton verschiedener Tonbereiche separat anzupassen für präzise, gezielte Farbkorrektur und kreative Looks.

## 🎯 Inspiration & Design-Philosophie

Basierend auf dem professionellen Drei-Wege-Color-Corrector aus High-End-Grading-Suiten:

- **Tonale Trennung**: Unabhängige Kontrolle über Schatten, Mids und Highlights
- **Doppel-Kontrolle**: Sowohl Intensität (Helligkeit) als auch Hue-Shift für jeden Tonbereich
- **Maskierte Anpassungen**: Änderungen blenden weich an tonalen Grenzen
- **Professioneller Workflow**: Das selbe Tool, das von Hollywood-Coloristen genutzt wird
- **Kreative Freiheit**: Präzise Kontrolle für sowohl Korrektur als auch Stilisierung

Dieser Node bringt professionelle Drei-Wege-Farbkorrektur zu Coollab und ermöglicht die Art von selektiver tonaler Arbeit, die High-End-Color-Grading definiert.

## ⭐ Hauptmerkmale

### 🌑 Schatten-Kontrolle
Betrifft nur die dunklen Bereiche:
- **Intensity**: Hellt Schatten auf oder verdunkelt sie (-1 bis +1)
- **Hue Shift**: Fügt Farbtönung nur zu Schatten hinzu (0 bis 1 = 0° bis 360°)
- **Auto-Maskiert**: Betrifft nur Pixel mit niedriger Luminanz (<0.33)

### 🌓 Mids-Kontrolle
Betrifft nur die Mitteltöne:
- **Intensity**: Hellt Mitteltöne auf oder verdunkelt sie (-1 bis +1)
- **Hue Shift**: Fügt Farbtönung nur zu Mitteltönen hinzu (0 bis 1 = 0° bis 360°)
- **Auto-Maskiert**: Betrifft mittleren Luminanz-Bereich (~0.33-0.66)

### 🌕 Highlights-Kontrolle
Betrifft nur die hellen Bereiche:
- **Intensity**: Hellt Highlights auf oder verdunkelt sie (-1 bis +1)
- **Hue Shift**: Fügt Farbtönung nur zu Highlights hinzu (0 bis 1 = 0° bis 360°)
- **Auto-Maskiert**: Betrifft nur Pixel mit hoher Luminanz (>0.66)

### 🎭 Automatische Maskierung
- Smarte luminanz-basierte Masken
- Weiche Übergänge zwischen tonalen Regionen
- Keine manuelle Maskierung nötig
- Professionelles Smoothstep-Blending

### ⚡ Echtzeit-Performance
- Schnelle HSV-Konversion
- Optimierte Maskierungs-Berechnungen
- Geeignet für Video-Wiedergabe
- Interaktives Anpassungs-Feedback

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu gradende Bild |
| **Highlights Intensity** | -1.0 - 1.0 | 0.0 | Passt Helligkeit der Highlights an. Negativ = dunkler, positiv = heller. |
| **Highlights Hue Shift** | 0.0 - 1.0 | 0.0 | Verschiebt Hue in Highlights (0 bis 1 = 0° bis 360°). |
| **Mids Intensity** | -1.0 - 1.0 | 0.0 | Passt Helligkeit der Mitteltöne an. Negativ = dunkler, positiv = heller. |
| **Mids Hue Shift** | 0.0 - 1.0 | 0.0 | Verschiebt Hue in Mitteltönen (0 bis 1 = 0° bis 360°). |
| **Shadows Intensity** | -1.0 - 1.0 | 0.0 | Passt Helligkeit der Schatten an. Negativ = dunkler, positiv = heller. |
| **Shadows Hue Shift** | 0.0 - 1.0 | 0.0 | Verschiebt Hue in Schatten (0 bis 1 = 0° bis 360°). |

## 🎨 Kreative Nutzungstipps

### 🎬 Korrigierende Color-Grading

**Split-Tone-Korrektur:**
1. Warme Schatten, kühle Highlights (klassischer Film-Look)
2. **Shadows Hue Shift**: 0.05-0.08 (warm orange/gelb)
3. **Highlights Hue Shift**: 0.55-0.6 (kühl cyan/blau)
4. **Intensity**-Werte bei 0.0 halten
5. Erzeugt dimensionale, filmische Trennung

**Schatten-Detail-Wiederherstellung:**
1. Bild mit zugemachten, dunklen Schatten
2. **Shadows Intensity**: +0.2 bis +0.4 (Schatten heben)
3. **Mids Intensity**: -0.05 bis -0.1 (kompensieren zur Vermeidung von Auswaschen)
4. **Highlights Intensity**: 0.0 (Highlights behalten)
5. Enthüllt verstecktes Schatten-Detail

**Highlight-Detail-Schutz:**
1. Überbelichtete Highlights verlieren Detail
2. **Highlights Intensity**: -0.15 bis -0.3 (Highlights runterziehen)
3. **Mids Intensity**: +0.05 bis +0.1 (Mitteltöne kompensieren)
4. **Shadows Intensity**: 0.0 (Schatten behalten)
5. Stellt durchgebrannte Highlights wieder her

**Farbstich-Entfernung:**
1. Unerwünschte Farbtönung in spezifischem Tonbereich
2. Identifizieren Sie, welcher Bereich den Stich hat (Schatten/Mids/Highlights)
3. Nutzen Sie entsprechenden **Hue Shift** zur Gegenwirkung
4. Beispiel: Grüner Stich in Schatten → Shadows Hue Shift zu Magenta (0.83)
5. Selektive Korrektur ohne gesamtes Bild zu beeinflussen

### 🎨 Kreative Stilisierung

**Teal & Orange Look (Blockbuster):**
1. **Shadows Hue Shift**: 0.05 (warm orange)
2. **Shadows Intensity**: +0.05 (leichtes Heben)
3. **Highlights Hue Shift**: 0.52 (teal/cyan)
4. **Highlights Intensity**: 0.0
5. **Mids**: Neutral lassen oder subtil warm (0.02)
6. Klassischer moderner Kino-Look

**Golden Hour Effekt:**
1. **Shadows Hue Shift**: 0.08 (warm orange)
2. **Shadows Intensity**: -0.1 (Schatten vertiefen)
3. **Mids Hue Shift**: 0.06 (goldgelb)
4. **Mids Intensity**: +0.05 (heben)
5. **Highlights Hue Shift**: 0.10 (warm gelb)
6. **Highlights Intensity**: +0.1 (hell)
7. Simuliert Sonnenuntergangs-/Sonnenaufgangs-Beleuchtung

**Kühles Mondlicht:**
1. **Shadows Hue Shift**: 0.62 (tiefblau)
2. **Shadows Intensity**: -0.15 (verdunkeln)
3. **Mids Hue Shift**: 0.58 (blau-cyan)
4. **Mids Intensity**: -0.05 (leicht dunkler)
5. **Highlights Hue Shift**: 0.54 (cyan)
6. **Highlights Intensity**: +0.05 (leicht heller)
7. Erzeugt nächtliche/mondbeleuchtete Ästhetik

**Cross-Processing-Effekt:**
1. **Shadows Hue Shift**: 0.55 (cyan)
2. **Shadows Intensity**: +0.1 (heben)
3. **Highlights Hue Shift**: 0.08 (gelb-orange)
4. **Highlights Intensity**: -0.05 (komprimieren)
5. **Mids**: Neutral lassen
6. Vintage cross-processed Film-Look

**Vintage Sepia-Ton:**
1. Erst Bild entsättigen (Color Grading - Basic, Saturation = 0.3)
2. **Shadows Hue Shift**: 0.06 (warm braun)
3. **Mids Hue Shift**: 0.08 (sepia)
4. **Highlights Hue Shift**: 0.10 (helles Sepia/Creme)
5. Alle **Intensity**-Werte: 0.0
6. Klassischer Sepia-Foto-Look

**High-Contrast Drama:**
1. **Shadows Intensity**: -0.3 (Schwarztöne crushen)
2. **Shadows Hue Shift**: 0.6 (blaue Tönung hinzufügen)
3. **Highlights Intensity**: +0.2 (Highlights ausblasen)
4. **Highlights Hue Shift**: 0.05 (Highlights warm)
5. **Mids Intensity**: -0.05 (leichte Kompression)
6. Erzeugt dramatischen, kontrastigen Look

### 🌈 Fortgeschrittene Techniken

**Komplementärer Split-Tone:**
1. Wählen Sie zwei komplementäre Farben (gegenüber auf Farbrad)
2. **Shadows Hue Shift**: Farbe A (z.B. 0.05 = orange)
3. **Highlights Hue Shift**: Farbe B (z.B. 0.55 = cyan)
4. **Mids**: Neutral oder Blend (0.3 zwischen beiden)
5. Maximaler Farbkontrast und visuelles Interesse

**Graduierter Farb-Shift:**
1. **Shadows Hue Shift**: Startfarbe (z.B. 0.0 = rot)
2. **Mids Hue Shift**: Mittelfarbe (z.B. 0.08 = orange)
3. **Highlights Hue Shift**: Endfarbe (z.B. 0.16 = gelb)
4. Erzeugt weichen Farbgradienten über Tonbereich

**Selektiver Tonal-Boost:**
1. Identifizieren Sie, welcher Bereich mehr Punch braucht
2. Steigern Sie nur **Intensity** dieses Bereichs
3. Beispiel: Flache Mitteltöne → **Mids Intensity**: +0.15
4. Lässt Schatten und Highlights unberührt
5. Gezielte Verbesserung ohne globale Änderungen

**Farbtemperatur-Korrektur:**
1. Bild insgesamt zu warm
2. **Shadows Hue Shift**: 0.5-0.6 (in Schatten abkühlen)
3. **Mids Hue Shift**: 0.52-0.58 (Mitteltöne kühlen)
4. **Highlights Hue Shift**: 0.54-0.6 (Highlights kühlen)
5. Unterschiedliche Mengen pro Bereich für natürlichen Look

## 💡 Workflow-Beispiele

### Beispiel 1: Klassisches Teal & Orange
1. Laden Sie beliebiges Bild
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: 0.0
   - Hue Shift: 0.05 (orange)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.02 (subtil warm)
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.52 (teal)
6. Ergebnis: Moderne Blockbuster-Farbpalette

### Beispiel 2: Dunkle Schatten wiederherstellen
1. Bild mit sehr dunklen, zugemachten Schatten
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: +0.35 (aggressives Heben)
   - Hue Shift: 0.0
4. **Mids**:
   - Intensity: -0.1 (verdunkeln zur Kompensation)
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.0
6. Ergebnis: Enthülltes Schatten-Detail ohne Auswaschen

### Beispiel 3: Goldener Sonnenuntergangs-Look
1. Tagsüber-Außenszene
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: -0.05 (leicht dunkler)
   - Hue Shift: 0.08 (warm orange)
4. **Mids**:
   - Intensity: +0.08 (heben)
   - Hue Shift: 0.07 (golden)
5. **Highlights**:
   - Intensity: +0.12 (hell)
   - Hue Shift: 0.10 (warm gelb)
6. Ergebnis: Wunderschöne Golden-Hour-Ästhetik

### Beispiel 4: Kühle Nacht-Szene
1. Beliebige Szene zur Konversion in Nachtzeit-Feeling
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: -0.2 (signifikant verdunkeln)
   - Hue Shift: 0.6 (tiefblau)
4. **Mids**:
   - Intensity: -0.1 (dunkler)
   - Hue Shift: 0.58 (blau-cyan)
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.54 (cyan - Mondlicht)
6. Kombinieren mit **Color Grading - Basic** (Saturation auf 0.7 reduzieren)
7. Ergebnis: Überzeugende Nachtzeit-Optik

### Beispiel 5: Vintage Cross-Process
1. Portrait oder Mode-Foto
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: +0.12 (heben)
   - Hue Shift: 0.55 (cyan-grün)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: -0.08 (komprimieren)
   - Hue Shift: 0.08 (gelb)
6. Ergebnis: Klassische cross-processed Film-Ästhetik

### Beispiel 6: Selektive Mittelton-Verbesserung
1. Flaches, niedriger-Kontrast-Bild
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: 0.0
   - Hue Shift: 0.0
4. **Mids**:
   - Intensity: +0.2 (signifikanter Boost)
   - Hue Shift: 0.0
5. **Highlights**:
   - Intensity: 0.0
   - Hue Shift: 0.0
6. Ergebnis: Knackige Mitteltöne, erhaltene Schatten/Highlights

### Beispiel 7: Film-Print-Fade-Emulation
1. Modernes Digital-Bild
2. Fügen Sie **Color Grading - Classical** hinzu
3. **Shadows**:
   - Intensity: +0.15 (heben - charakteristisch für verblasste Prints)
   - Hue Shift: 0.05 (warm)
4. **Mids**:
   - Intensity: 0.0
   - Hue Shift: 0.06 (warm)
5. **Highlights**:
   - Intensity: -0.05 (leichte Kompression)
   - Hue Shift: 0.08 (warm sepia)
6. Kombinieren mit reduzierter Sättigung (0.75)
7. Ergebnis: Vintage verblasster Film-Print

## 🔧 Technische Details

- **Node-Typ**: Tonal Color Grading (UV→sRGB_StraightA)
- **Kategorie**: Color Grading / Color Correction
- **Algorithmus**: Luminanz-basierte Maskierung + HSV Hue/Brightness
- **Maskierung**: Automatische Smoothstep-Übergänge
- **Farbraum**: sRGB Input/Output, HSV für Modifikationen
- **Performance**: Echtzeit-fähig, optimiert

## 🧮 Verständnis des Algorithmus

### Luminanz-Berechnung
```
luma = dot(rgb, vec3(0.299, 0.587, 0.114))
```
- Standard Rec. 601 Luminanz-Berechnung
- Bestimmt, zu welchem Tonbereich jedes Pixel gehört

### Tonale Masken
```
shadow_mask = smoothstep(0.33, 0.0, luma)
mid_mask = 1.0 - abs(luma - 0.5) × 2.0, dann smoothstep
highlight_mask = smoothstep(0.66, 1.0, luma)
```
- **Schatten-Maske**: Hoch für dunkle Pixel (luma < 0.33)
- **Mid-Maske**: Hoch für mittlere Pixel (luma ~0.33-0.66)
- **Highlight-Maske**: Hoch für helle Pixel (luma > 0.66)
- **Smoothstep**: Erzeugt weiche Übergänge zwischen Bereichen

### Intensity-Anwendung
```
rgb += Intensity × mask
```
- Additive Helligkeits-Anpassung
- Maskiert zur Beeinflussung nur spezifischer Tonbereiche
- Mehrere Anpassungen akkumulieren

### Hue-Shift-Anwendung
```
1. Konvertiere RGB zu HSV
2. total_hue_shift = (Highlights_Hue × highlight_mask) +
                     (Mids_Hue × mid_mask) +
                     (Shadows_Hue × shadow_mask)
3. hsv.hue = fract(hsv.hue + total_hue_shift)
4. Konvertiere zurück zu RGB
```
- Jeder Hue-Shift ist maskiert
- Alle Shifts akkumulieren basierend auf Pixel-Luminanz
- Weiches Blending an tonalen Grenzen

## 🎬 Best Practices

### 🎯 Anpassungs-Strategie

**Arbeiten Sie einen Bereich nach dem anderen:**
1. Starten Sie mit **Shadows**
2. Dann passen Sie **Highlights** an
3. Schließlich feinabstimmen **Mids**
4. Überprüfen Sie Gesamt-Balance

**Starten Sie mit Hue, dann Intensity:**
- Setzen Sie zuerst Farbtönungen (Hue Shift)
- Dann passen Sie Helligkeit an (Intensity)
- Einfacher, den Effekt zu sehen

**Nutzen Sie subtile Anpassungen:**
- **Intensity**: ±0.1 bis ±0.2 für die meiste Arbeit
- **Hue Shift**: 0.02-0.1 für subtile Tönungen
- Graduell aufbauen

### 💡 Häufige Kombinationen

**Split Tone (Warm/Kühl):**
- Shadows: Hue 0.05, Intensity 0.0
- Mids: Hue 0.0, Intensity 0.0
- Highlights: Hue 0.55, Intensity 0.0

**Schatten-Heben:**
- Shadows: Hue 0.0, Intensity +0.2 bis +0.4
- Mids: Hue 0.0, Intensity -0.05 bis -0.1
- Highlights: Hue 0.0, Intensity 0.0

**Highlight-Kompression:**
- Shadows: Hue 0.0, Intensity 0.0
- Mids: Hue 0.0, Intensity +0.05
- Highlights: Hue 0.0, Intensity -0.2 bis -0.3

### ⚠️ Häufige Fehler vermeiden

- ❌ Extreme Intensity-Werte (±0.5+) auf allen Bereichen
- ❌ Widersprechende Hue-Shifts (zufällige Farben in jedem Bereich)
- ❌ Vergessen, dass Anpassungen akkumulieren
- ❌ Nicht natürliche Farbharmonie berücksichtigen
- ❌ Übersättigung durch nur Hue-Shifts ohne Ergebnis-Prüfung

## 🔗 Kombination mit anderen Nodes

**Essentielle Workflow-Begleiter:**
- **⭐ Color Grading - Basic**: Vor oder nach für globale Anpassungen nutzen
- **🎨 Levels Correction**: Tonale Grundlage zuerst setzen
- **💡 Gamma Correction**: Gesamt-Gamma-Anpassung
- **🔧 Color Replace**: Zusätzliche selektive Farbarbeit
- **🌈 Zusätzliche Color Grading - Classical**: Stapeln für komplexe Looks

**Empfohlene Workflows:**

**Professionelle Farbkorrektur:**
```
Image → Levels Correction (Tonbereich etablieren)
      → Color Grading - Classical (selektive tonale Arbeit)
      → Color Grading - Basic (finaler Polish)
      → Output
```

**Kinematischer Look:**
```
Image → Color Grading - Basic (Kontrast, Sättigung)
      → Color Grading - Classical (Teal & Orange Split)
      → Gamma Correction (Gesamt-Gamma)
      → Output
```

**Vintage-Film-Emulation:**
```
Image → Levels Correction (Schwarztöne heben)
      → Color Grading - Tonal (warme Schatten, warme Highlights)
      → Color Grading - Basic (Sättigung reduzieren)
      → Output
```

## 🔧 Fehlerbehebungs-Guide

### Problem: Änderungen zu subtil / nicht sichtbar
**Lösungen**:
- ✅ **Intensity**-Werte erhöhen (versuchen Sie ±0.2 bis ±0.3)
- ✅ Dramatischere **Hue Shift**-Werte nutzen (0.1+)
- ✅ Prüfen Sie, ob Bild den Tonbereich hat, den Sie anpassen
- ✅ Sehr dunkles Bild könnte keine Highlights zum Anpassen haben

### Problem: Farben sehen unnatürlich / seltsam aus
**Lösungen**:
- ✅ **Hue Shift**-Mengen reduzieren (nutzen Sie 0.02-0.08 für subtil)
- ✅ Farbharmonie berücksichtigen (komplementär vs analog)
- ✅ Nicht alle drei Bereiche zu zufälligen Farben shiften
- ✅ Referenz-Bilder für Color-Grading-Inspiration nutzen

### Problem: Verlust von Detail in Schatten nach Heben
**Lösungen**:
- ✅ **Shadows Intensity** reduzieren (nicht zu viel heben)
- ✅ Mit **Mids Intensity**-Reduktion kompensieren
- ✅ Könnte besseres Quellmaterial brauchen
- ✅ Mit Levels Correction für mehr Kontrolle kombinieren

### Problem: Highlights zu hell / ausgeblasen
**Lösungen**:
- ✅ **Highlights Intensity** reduzieren (negative Werte nutzen)
- ✅ Mit **Mids Intensity**-Boost kompensieren
- ✅ Könnte zuerst Levels Correction zur Highlight-Kompression brauchen
- ✅ Original-Footage-Belichtung prüfen

### Problem: Schlammige Mitteltöne
**Lösungen**:
- ✅ **Mids Intensity** reduzieren oder auf negativ setzen
- ✅ Prüfen Sie, ob Schatten und Highlights beide gehoben werden
- ✅ **Color Grading - Basic** nutzen, um globalen Kontrast hinzuzufügen
- ✅ Könnte Sättigungs-Boost brauchen

### Problem: Tonale Bereiche bluten ineinander
**Lösungen**:
- ✅ Dies ist normal - Masken haben weiche Übergänge
- ✅ Extremere Anpassungen für klare Trennung nutzen
- ✅ Akzeptieren Sie, dass Mitteltöne Blend von Anpassungen zeigen
- ✅ Dies erzeugt natürliche, professionelle Ergebnisse

## ⚡ Performance-Tipps

- ✅ Schnelle HSV-Konversion
- ✅ Optimierte Maskierungs-Berechnungen
- ✅ Echtzeit-fähig für Video
- ✅ Kann mehrere Instanzen stapeln
- ✅ Geeignet für Live-Performance

## 🎓 Fortgeschrittene Techniken

### Filmstock-Emulation

**Kodak Portra (Warm, Portrait):**
- Shadows: Hue 0.05, Intensity -0.05
- Mids: Hue 0.04, Intensity +0.02
- Highlights: Hue 0.06, Intensity +0.05

**Fuji Velvia (Lebendige Landschaft):**
- Shadows: Hue 0.0, Intensity -0.1
- Mids: Hue 0.0, Intensity 0.0
- Highlights: Hue 0.0, Intensity +0.05
- Mit hoher Sättigung kombinieren (1.4)

**Cinestill 800T (Tungsten, Nacht):**
- Shadows: Hue 0.55, Intensity 0.0
- Mids: Hue 0.52, Intensity 0.0
- Highlights: Hue 0.08, Intensity +0.1 (warme Halos)

### Tageszeit-Simulation

**Morgen (Kühl zu Warm):**
- Shadows: Hue 0.58, Intensity 0.0
- Mids: Hue 0.05, Intensity +0.05
- Highlights: Hue 0.08, Intensity +0.1

**Nachmittag (Neutral Hell):**
- Shadows: Hue 0.0, Intensity +0.05
- Mids: Hue 0.02, Intensity +0.05
- Highlights: Hue 0.0, Intensity 0.0

**Sonnenuntergang (Golden):**
- Shadows: Hue 0.08, Intensity -0.05
- Mids: Hue 0.07, Intensity +0.08
- Highlights: Hue 0.10, Intensity +0.15

**Nacht (Blau/Kühl):**
- Shadows: Hue 0.62, Intensity -0.2
- Mids: Hue 0.58, Intensity -0.1
- Highlights: Hue 0.54, Intensity 0.0

### Shots in Sequenz angleichen

1. **Referenz-Shot**: Graden Sie Ihren Hero-Shot
2. **Werte notieren**: Notieren Sie exakte Intensity/Hue-Werte
3. **Anwenden**: Auf anderen Shots in Sequenz nutzen
4. **Feinabstimmung**: Für Beleuchtungs-Unterschiede anpassen
5. **Konsistenz**: Gesamt-Look erhalten

## 💡 Warum dieser Node erstellt wurde

Professionelles Color Grading erfordert selektive tonale Kontrolle. **Color Grading - Classical** bietet:

- ✅ **Industrie-standard Drei-Wege-Korrektur**
- ✅ **Unabhängige Schatten/Mid/Highlight-Kontrolle**
- ✅ **Automatische tonale Maskierung**
- ✅ **Sowohl Intensity als auch Hue-Kontrolle** pro Bereich
- ✅ **Professionelle Ergebnisse** mit intuitiver Oberfläche
- ✅ **Kreative Freiheit** für Stilisierung

Dies ist dasselbe Tool, das von professionellen Coloristen genutzt wird, jetzt in Coollab!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
