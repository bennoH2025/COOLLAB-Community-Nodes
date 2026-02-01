[English](#chroma-key---classical---documentation) | [Deutsch](#chroma-key---classical---dokumentation)

---

# Chroma Key - classical - Documentation

## Overview

**Chroma Key - classical** is a professional-grade keying node that removes color backgrounds (like greenscreens or bluescreens) and creates clean transparency for compositing. With advanced features like spill suppression and edge refinement, this node delivers broadcast-quality keying results directly in Coollab.

## Inspiration & Design Philosophy

Designed to bring professional video production capabilities to Coollab:

- **Industry-Standard Keying**: Implements proven chroma key algorithms used in professional video software
- **Spill Suppression**: Removes unwanted color reflections from the key color onto the subject
- **Edge Control**: Fine-tune matte edges with erode/grow capabilities
- **Visual Feedback**: "Show Matte" feature for precise adjustment and troubleshooting
- **Flexible Workflow**: Works seamlessly with Alpha Composite for complete compositing pipeline

This node transforms Coollab into a capable keying and compositing environment, perfect for greenscreen work, visual effects, and creative video production.

## Key Features

### 🎬 Professional Color Keying
Removes backgrounds based on color selection:
- RGB-based color distance calculation
- Adjustable tolerance for varying lighting conditions
- Soft edge control for natural-looking mattes
- Works with any solid color background (green, blue, or custom)

### 🌈 Advanced Spill Suppression
Eliminates color contamination from the background:
- Removes green/blue spill from subject edges
- HSV-based intelligent color reduction
- Preserves subject's natural colors
- Adjustable intensity from 0% to 100%

### ✂️ Edge Refinement
Perfect control over matte edges:
- **Edge Erode** with positive values: Shrinks the matte (removes edge pixels)
- **Edge Erode** with negative values: Grows the matte (adds edge pixels)
- Fix edge problems without re-shooting
- Clean up minor keying artifacts

### 👁️ Show Matte Visualization
See exactly what you're keying:
- White = Opaque (subject kept)
- Black = Transparent (background removed)
- Gray = Partial transparency (edge transitions)
- Perfect for fine-tuning Tolerance and Softness

### ⚡ Real-time Performance
- Optimized shader code for live keying
- Smooth playback even with video input
- Suitable for live performances and real-time visuals

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image/video to key (e.g., greenscreen footage) |
| **Key Color** | sRGB | Green | The background color to remove. Use color picker or input RGB values. |
| **Tolerance** | 0.0 - 1.0 | 0.3 | How similar colors must be to be keyed. Lower = stricter, higher = more permissive. |
| **Softness** | 0.0 - 1.0 | 0.1 | Edge softness of the matte. 0 = hard edge, higher = softer transition. |
| **Show Matte** | Boolean | false | Display the alpha matte in white/black for adjustment. |
| **Spill Suppression** | 0.0 - 1.0 | 0.5 | Reduce color spill from background. 0 = none, 1 = maximum removal. |
| **Edge Erode** | -1.0 - 1.0 | 0.0 | Shrink (+) or grow (-) matte edges. Use to fix edge artifacts. |

## Creative Usage Tips

### 🎥 Basic Greenscreen Workflow

**Step-by-Step Keying:**
1. Load your greenscreen footage with **Image** node
2. Add **Chroma Key - classical**
3. Use **color picker** on Key Color parameter
4. Click on green background in your footage
5. Enable **Show Matte** to see selection
6. Adjust **Tolerance** until background is fully black
7. Adjust **Softness** for natural edge transitions
8. Fine-tune with **Edge Erode** if needed
9. Enable **Spill Suppression** to remove green fringe
10. Connect to **Alpha Composite** for final composition

### 🎨 Advanced Keying Techniques

**Difficult Lighting Situations:**
- **Uneven greenscreen**: Increase Tolerance gradually
- **Dark shadows**: Higher Tolerance with higher Softness
- **Bright highlights**: Use Edge Erode to shrink matte
- **Mixed lighting**: Consider using multiple Chroma Key nodes for different regions

**Edge Quality:**
- **Soft natural edges**: Softness = 0.15-0.25
- **Sharp crisp edges**: Softness = 0.05-0.1
- **Blurred/motion blur**: Higher Softness = 0.3-0.5

**Spill Removal:**
- **Heavy spill**: Spill Suppression = 0.7-1.0
- **Moderate spill**: Spill Suppression = 0.4-0.6
- **Minimal spill**: Spill Suppression = 0.2-0.3
- **No spill**: Spill Suppression = 0.0

### 🔧 Problem Solving with Show Matte

Enable **Show Matte** to diagnose issues:

**White areas** = What will be kept (opaque)
**Black areas** = What will be removed (transparent)
**Gray areas** = Partial transparency (edges)

**Common Issues:**
- **Subject has black holes**: Increase Tolerance
- **Background not fully black**: Increase Tolerance or adjust Key Color
- **Edges too sharp/hard**: Increase Softness
- **Subject partially transparent**: Decrease Tolerance
- **Fringing/halos**: Increase Spill Suppression or adjust Edge Erode

### 🌈 Non-Green Keying

Works with any solid background color:

**Blue Screen:**
- Set Key Color to blue
- Same workflow as greenscreen
- Often better for blonde hair or green costumes

**Custom Colors:**
- Any solid color can be keyed
- Red, yellow, magenta - experiment!
- Useful for creative effects and stylized looks

**Multi-Color Keying:**
- Stack multiple Chroma Key nodes
- Key different colors sequentially
- Each removes a different background element

### 🎭 Creative Effects

**Partial Keying:**
1. Set Tolerance very low (0.1-0.2)
2. Only removes exact color matches
3. Creates stylized, selective transparency
4. Artistic rather than realistic results

**Inverted Keying:**
1. Key the subject instead of background
2. Creates subject-shaped transparency
3. Useful for creating masks and mattes
4. Combine with other effects for unique looks

## Workflow Examples

### Example 1: Perfect Greenscreen Key
1. **Import** greenscreen footage (Image node)
2. **Add Chroma Key - classical**
3. **Set Key Color** using color picker on green background
4. **Enable Show Matte**
5. **Adjust Tolerance** until background is pure black (start at 0.3)
6. **Adjust Softness** for natural edges (typically 0.1-0.15)
7. **Check edges** carefully - zoom in if needed
8. **Disable Show Matte**
9. **Adjust Spill Suppression** to 0.5-0.7 to remove green fringe
10. **Fine-tune Edge Erode** if edges need correction (±0.05)
11. **Connect to Alpha Composite** with your background

### Example 2: Difficult Lighting Scenario
1. Start with greenscreen with uneven lighting
2. Add **Chroma Key - classical**
3. Pick the **mid-tone green** (not darkest or lightest)
4. **Increase Tolerance** to 0.4-0.5 (higher than normal)
5. **Increase Softness** to 0.2 to handle gradual transitions
6. Use **Show Matte** to check coverage
7. If subject has transparency, add **second Chroma Key node**:
   - Pick darker green areas
   - Lower Tolerance (0.2-0.3)
   - Combine both keys
8. Apply **Spill Suppression** (0.6-0.8)

### Example 3: Hair Detail Preservation
1. Load footage with detailed hair
2. Add **Chroma Key - classical**
3. Set Key Color and basic Tolerance (0.3)
4. **Increase Softness** to 0.25-0.35 for fine hair strands
5. Enable **Show Matte** - check hair is white/gray
6. **Reduce Edge Erode** to -0.1 to -0.2 (grow matte slightly)
7. This captures more fine details
8. **Spill Suppression** to 0.4-0.6 to clean hair edges
9. Disable Show Matte and check result

### Example 4: Motion Blur Handling
1. Key footage with fast motion/blur
2. Add **Chroma Key - classical**
3. Set Key Color (standard green)
4. **Increase Softness** significantly (0.3-0.5)
5. This handles the blurred edges between subject and background
6. Adjust **Tolerance** to taste (0.3-0.4)
7. **Spill Suppression** helps with motion blur artifacts (0.6)
8. Accept some transparency in motion - natural look

### Example 5: Creative Partial Transparency
1. Start with any colorful image
2. Add **Chroma Key - classical**
3. Set Key Color to a prominent color
4. Set **very low Tolerance** (0.1-0.15)
5. Set **low Softness** (0.05)
6. Creates selective transparency
7. Composite over contrasting background
8. Results in stylized, artistic effect

## Technical Details

- **Node Type**: Keyer (UV→sRGB_StraightA input/output)
- **Category**: Keying / Compositing
- **Algorithm**: RGB color distance with HSV spill suppression
- **Color Space**: sRGB with straight alpha output
- **Matte Type**: Luminance-based alpha channel
- **Performance**: Real-time capable, optimized shader

## Understanding the Algorithm

### Color Distance Keying
```
distance = length(pixel.RGB - KeyColor.RGB)
alpha = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
```

- Calculates Euclidean distance in RGB color space
- Closer to Key Color = more transparent
- Softness creates gradual transition

### Spill Suppression
```
1. Convert pixel to HSV color space
2. Compare pixel hue to Key Color hue
3. If hues are similar, reduce saturation
4. Convert back to RGB
```

- Removes color contamination intelligently
- Preserves natural subject colors
- Focuses on edges where spill occurs

### Edge Erode/Grow
```
alpha = clamp(alpha + EdgeErode, 0.0, 1.0)
```

- Positive values: Shrink matte (erode)
- Negative values: Expand matte (grow)
- Simple but effective edge control

## Best Practices

### 🎬 Shooting Tips (for best keying results)
- **Even lighting** on greenscreen is critical
- **Separate subject** from background (2-3 meters minimum)
- **Avoid shadows** on greenscreen
- **Use proper exposure** - not too bright, not too dark
- **Match subject lighting** to intended background

### 🔧 Keying Workflow
1. Always start with **Show Matte** enabled
2. Adjust **Tolerance** first (get coverage)
3. Then adjust **Softness** (refine edges)
4. Apply **Spill Suppression** after keying is good
5. Use **Edge Erode** as final touch-up
6. Disable Show Matte and check final result
7. Composite and adjust lighting/color to match

### ⚠️ Common Mistakes to Avoid
- ❌ Setting Tolerance too high (removes subject details)
- ❌ Forgetting Spill Suppression (green/blue fringing)
- ❌ Using Edge Erode before getting good base key
- ❌ Not checking Show Matte (blind adjustments)
- ❌ Keying in wrong color space (use sRGB as provided)

## Combining with Other Nodes

**Essential Companions:**
- **⭐ Alpha Composite - for Key-in-Mix**: Composite keyed footage over backgrounds
- **🎨 Color Grading nodes**: Match foreground/background lighting and color
- **💡 Color Replace**: Additional spill removal or color correction
- **🔄 2D Modifiers**: Apply effects before or after keying

**Advanced Combinations:**
- **Garbage Mattes**: Use masks to isolate keying area
- **Multiple Keys**: Stack for complex multi-color backgrounds
- **Color Correction**: Match lighting between layers
- **Edge Effects**: Add glows, outlines after keying

## Troubleshooting Guide

### Problem: Background not fully removed
**Solutions**:
- ✅ Increase Tolerance
- ✅ Check Key Color is correct (use picker on background)
- ✅ Enable Show Matte to see what's not being keyed
- ✅ Lighting may be too uneven - consider multiple keys

### Problem: Subject becoming transparent
**Solutions**:
- ✅ Decrease Tolerance
- ✅ Subject may contain key color - use Color Replace first
- ✅ Check if subject is too similar to background color
- ✅ Use Edge Erode negative value to grow matte

### Problem: Green/blue fringing on edges
**Solutions**:
- ✅ Increase Spill Suppression (0.5-0.8)
- ✅ Use Color Replace node after Chroma Key
- ✅ Adjust Edge Erode slightly positive (+0.05 to +0.1)
- ✅ May need better separation during filming

### Problem: Edges too sharp/hard
**Solutions**:
- ✅ Increase Softness (0.15-0.3)
- ✅ Slightly decrease Tolerance
- ✅ Check if original footage has sharp edges (intended)
- ✅ May need motion blur or edge blur effect

### Problem: Holes in subject
**Solutions**:
- ✅ Decrease Tolerance
- ✅ Subject may have key color elements (costume, props)
- ✅ Use negative Edge Erode to fill small holes
- ✅ Consider masking problem areas separately

### Problem: Hair/fine details lost
**Solutions**:
- ✅ Increase Softness significantly (0.25-0.4)
- ✅ Use negative Edge Erode (-0.1 to -0.2)
- ✅ Reduce Tolerance slightly
- ✅ Film with better background separation

## Performance Tips

- ✅ Disable **Show Matte** when not adjusting (slight performance gain)
- ✅ Use appropriate **Softness** - excessive values slow down
- ✅ **Spill Suppression** has minimal performance cost
- ✅ Node is optimized for real-time use
- ✅ Works well with video playback and live input

## Why This Node Was Created

Many keying solutions are either too simple (poor results) or too complex (overwhelming). **Chroma Key - classical** finds the perfect balance:

- ✅ **Professional results** without professional complexity
- ✅ **Essential features** (keying, spill, edge control) in one node
- ✅ **Visual feedback** with Show Matte feature
- ✅ **Seamless integration** with Alpha Composite workflow
- ✅ **Real-time capable** for live and interactive work

This makes professional greenscreen work accessible to everyone in Coollab!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#chroma-key---classical---documentation) | [Deutsch](#chroma-key---classical---dokumentation)

---

# Chroma Key - classical - Dokumentation

## Übersicht

**Chroma Key - classical** ist ein professioneller Keying-Node, der Farbhintergründe (wie Greenscreens oder Bluescreens) entfernt und saubere Transparenz für Compositing erstellt. Mit erweiterten Funktionen wie Spill Suppression und Edge Refinement liefert dieser Node Broadcast-qualitative Keying-Ergebnisse direkt in Coollab.

## 🎯 Inspiration & Design-Philosophie

Entwickelt, um professionelle Videoproduktions-Fähigkeiten zu Coollab zu bringen:

- **Industrie-Standard-Keying**: Implementiert bewährte Chroma-Key-Algorithmen aus professioneller Video-Software
- **Spill Suppression**: Entfernt unerwünschte Farbreflexionen von der Key-Farbe auf das Motiv
- **Edge Control**: Feinabstimmung der Matten-Kanten mit Erode/Grow-Funktionen
- **Visuelles Feedback**: "Show Matte"-Feature für präzise Anpassung und Fehlersuche
- **Flexibler Workflow**: Funktioniert nahtlos mit Alpha Composite für komplette Compositing-Pipeline

Dieser Node verwandelt Coollab in eine leistungsfähige Keying- und Compositing-Umgebung, perfekt für Greenscreen-Arbeit, visuelle Effekte und kreative Videoproduktion.

## ⭐ Hauptmerkmale

### 🎬 Professionelles Farb-Keying
Entfernt Hintergründe basierend auf Farbauswahl:
- RGB-basierte Farbdistanz-Berechnung
- Anpassbare Toleranz für variierende Lichtverhältnisse
- Weiche Kantenkontrolle für natürlich aussehende Matten
- Funktioniert mit jedem einfarbigen Hintergrund (grün, blau oder custom)

### 🌈 Erweiterte Spill Suppression
Eliminiert Farbkontamination vom Hintergrund:
- Entfernt Grün-/Blau-Spill von Motivkanten
- HSV-basierte intelligente Farbreduktion
- Erhält natürliche Farben des Motivs
- Anpassbare Intensität von 0% bis 100%

### ✂️ Edge Refinement
Perfekte Kontrolle über Matten-Kanten:
- **Edge Erode** mit positiven Werten: Schrumpft die Matte (entfernt Kantenpixel)
- **Edge Erode** mit negativen Werten: Erweitert die Matte (fügt Kantenpixel hinzu)
- Behebt Kantenprobleme ohne Neudreh
- Bereinigt kleine Keying-Artefakte

### 👁️ Show Matte Visualisierung
Sehen Sie genau, was Sie keyen:
- Weiß = Undurchsichtig (Motiv behalten)
- Schwarz = Transparent (Hintergrund entfernt)
- Grau = Teilweise Transparenz (Kanten-Übergänge)
- Perfekt für Feinabstimmung von Tolerance und Softness

### ⚡ Echtzeit-Performance
- Optimierter Shader-Code für Live-Keying
- Flüssige Wiedergabe auch mit Video-Input
- Geeignet für Live-Performances und Echtzeit-Visuals

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das zu keyende Bild/Video (z.B. Greenscreen-Footage) |
| **Key Color** | sRGB | Grün | Die zu entfernende Hintergrundfarbe. Farbwähler nutzen oder RGB-Werte eingeben. |
| **Tolerance** | 0.0 - 1.0 | 0.3 | Wie ähnlich Farben sein müssen, um gekeyt zu werden. Niedriger = strenger, höher = permissiver. |
| **Softness** | 0.0 - 1.0 | 0.1 | Kanten-Weichheit der Matte. 0 = harte Kante, höher = weicherer Übergang. |
| **Show Matte** | Boolean | false | Zeigt die Alpha-Matte in Weiß/Schwarz zur Anpassung an. |
| **Spill Suppression** | 0.0 - 1.0 | 0.5 | Reduziert Farb-Spill vom Hintergrund. 0 = keine, 1 = maximale Entfernung. |
| **Edge Erode** | -1.0 - 1.0 | 0.0 | Schrumpft (+) oder erweitert (-) Matten-Kanten. Zum Beheben von Kanten-Artefakten. |

## 🎨 Kreative Nutzungstipps

### 🎥 Basis-Greenscreen-Workflow

**Schritt-für-Schritt-Keying:**
1. Laden Sie Ihre Greenscreen-Footage mit **Image** Node
2. Fügen Sie **Chroma Key - classical** hinzu
3. Nutzen Sie **Farbwähler** beim Key-Color-Parameter
4. Klicken Sie auf grünen Hintergrund in Ihrer Footage
5. Aktivieren Sie **Show Matte**, um Auswahl zu sehen
6. Passen Sie **Tolerance** an, bis Hintergrund vollständig schwarz ist
7. Passen Sie **Softness** für natürliche Kanten-Übergänge an
8. Feinabstimmung mit **Edge Erode** falls nötig
9. Aktivieren Sie **Spill Suppression**, um grünen Rand zu entfernen
10. Verbinden Sie mit **Alpha Composite** für finale Komposition

### 🎨 Fortgeschrittene Keying-Techniken

**Schwierige Lichtsituationen:**
- **Ungleichmäßiger Greenscreen**: Erhöhen Sie Tolerance graduell
- **Dunkle Schatten**: Höhere Tolerance mit höherer Softness
- **Helle Highlights**: Nutzen Sie Edge Erode zum Schrumpfen der Matte
- **Gemischte Beleuchtung**: Erwägen Sie mehrere Chroma-Key-Nodes für verschiedene Regionen

**Kanten-Qualität:**
- **Weiche natürliche Kanten**: Softness = 0.15-0.25
- **Scharfe klare Kanten**: Softness = 0.05-0.1
- **Verschwommen/Motion Blur**: Höhere Softness = 0.3-0.5

**Spill-Entfernung:**
- **Starker Spill**: Spill Suppression = 0.7-1.0
- **Moderater Spill**: Spill Suppression = 0.4-0.6
- **Minimaler Spill**: Spill Suppression = 0.2-0.3
- **Kein Spill**: Spill Suppression = 0.0

### 🔧 Problemlösung mit Show Matte

Aktivieren Sie **Show Matte** zur Diagnose von Problemen:

**Weiße Bereiche** = Was behalten wird (undurchsichtig)
**Schwarze Bereiche** = Was entfernt wird (transparent)
**Graue Bereiche** = Teilweise Transparenz (Kanten)

**Häufige Probleme:**
- **Motiv hat schwarze Löcher**: Erhöhen Sie Tolerance
- **Hintergrund nicht vollständig schwarz**: Erhöhen Sie Tolerance oder passen Sie Key Color an
- **Kanten zu scharf/hart**: Erhöhen Sie Softness
- **Motiv teilweise transparent**: Verringern Sie Tolerance
- **Fringing/Halos**: Erhöhen Sie Spill Suppression oder passen Sie Edge Erode an

### 🌈 Nicht-Grün-Keying

Funktioniert mit jedem einfarbigen Hintergrund:

**Blue Screen:**
- Setzen Sie Key Color auf Blau
- Gleicher Workflow wie Greenscreen
- Oft besser für blonde Haare oder grüne Kostüme

**Custom-Farben:**
- Jede einfarbige Farbe kann gekeyt werden
- Rot, Gelb, Magenta - experimentieren Sie!
- Nützlich für kreative Effekte und stilisierte Looks

**Multi-Color-Keying:**
- Stapeln Sie mehrere Chroma-Key-Nodes
- Keyen Sie verschiedene Farben sequenziell
- Jeder entfernt ein anderes Hintergrund-Element

### 🎭 Kreative Effekte

**Partielles Keying:**
1. Setzen Sie Tolerance sehr niedrig (0.1-0.2)
2. Entfernt nur exakte Farb-Treffer
3. Erzeugt stilisierte, selektive Transparenz
4. Künstlerische statt realistische Ergebnisse

**Invertiertes Keying:**
1. Keyen Sie das Motiv statt Hintergrund
2. Erzeugt motivförmige Transparenz
3. Nützlich zum Erstellen von Masken und Matten
4. Kombinieren Sie mit anderen Effekten für einzigartige Looks

## 💡 Workflow-Beispiele

### Beispiel 1: Perfekter Greenscreen-Key
1. **Importieren** Sie Greenscreen-Footage (Image-Node)
2. **Fügen Sie Chroma Key - classical hinzu**
3. **Setzen Sie Key Color** mit Farbwähler auf grünem Hintergrund
4. **Aktivieren Sie Show Matte**
5. **Passen Sie Tolerance an**, bis Hintergrund rein schwarz ist (Start bei 0.3)
6. **Passen Sie Softness an** für natürliche Kanten (typisch 0.1-0.15)
7. **Prüfen Sie Kanten** sorgfältig - zoomen Sie bei Bedarf
8. **Deaktivieren Sie Show Matte**
9. **Passen Sie Spill Suppression an** auf 0.5-0.7, um grünen Rand zu entfernen
10. **Feinabstimmung Edge Erode**, falls Kanten Korrektur brauchen (±0.05)
11. **Verbinden Sie mit Alpha Composite** mit Ihrem Hintergrund

### Beispiel 2: Schwieriges Beleuchtungs-Szenario
1. Starten Sie mit Greenscreen mit ungleichmäßiger Beleuchtung
2. Fügen Sie **Chroma Key - classical** hinzu
3. Wählen Sie das **Mittelton-Grün** (nicht dunkelsten oder hellsten)
4. **Erhöhen Sie Tolerance** auf 0.4-0.5 (höher als normal)
5. **Erhöhen Sie Softness** auf 0.2 für graduelle Übergänge
6. Nutzen Sie **Show Matte** zur Abdeckungsprüfung
7. Falls Motiv Transparenz hat, fügen Sie **zweiten Chroma-Key-Node** hinzu:
   - Wählen Sie dunklere grüne Bereiche
   - Niedrigere Tolerance (0.2-0.3)
   - Kombinieren Sie beide Keys
8. Wenden Sie **Spill Suppression** an (0.6-0.8)

### Beispiel 3: Haar-Detail-Erhaltung
1. Laden Sie Footage mit detailliertem Haar
2. Fügen Sie **Chroma Key - classical** hinzu
3. Setzen Sie Key Color und Basis-Tolerance (0.3)
4. **Erhöhen Sie Softness** auf 0.25-0.35 für feine Haarsträhnen
5. Aktivieren Sie **Show Matte** - prüfen Sie, dass Haar weiß/grau ist
6. **Reduzieren Sie Edge Erode** auf -0.1 bis -0.2 (erweitern Sie Matte leicht)
7. Dies erfasst mehr feine Details
8. **Spill Suppression** auf 0.4-0.6 zur Reinigung der Haarkanten
9. Deaktivieren Sie Show Matte und prüfen Sie Ergebnis

### Beispiel 4: Motion-Blur-Handhabung
1. Keyen Sie Footage mit schneller Bewegung/Blur
2. Fügen Sie **Chroma Key - classical** hinzu
3. Setzen Sie Key Color (Standard-Grün)
4. **Erhöhen Sie Softness** signifikant (0.3-0.5)
5. Dies behandelt die verschwommenen Kanten zwischen Motiv und Hintergrund
6. Passen Sie **Tolerance** nach Geschmack an (0.3-0.4)
7. **Spill Suppression** hilft bei Motion-Blur-Artefakten (0.6)
8. Akzeptieren Sie etwas Transparenz in Bewegung - natürlicher Look

### Beispiel 5: Kreative Partielle Transparenz
1. Starten Sie mit einem beliebigen farbenfrohen Bild
2. Fügen Sie **Chroma Key - classical** hinzu
3. Setzen Sie Key Color auf eine prominente Farbe
4. Setzen Sie **sehr niedrige Tolerance** (0.1-0.15)
5. Setzen Sie **niedrige Softness** (0.05)
6. Erzeugt selektive Transparenz
7. Compositen Sie über kontrastierenden Hintergrund
8. Ergebnis ist stilisierter, künstlerischer Effekt

## 🔧 Technische Details

- **Node-Typ**: Keyer (UV→sRGB_StraightA Input/Output)
- **Kategorie**: Keying / Compositing
- **Algorithmus**: RGB-Farbdistanz mit HSV-Spill-Suppression
- **Farbraum**: sRGB mit Straight-Alpha-Ausgabe
- **Matten-Typ**: Luminanz-basierter Alpha-Kanal
- **Performance**: Echtzeit-fähig, optimierter Shader

## 🧮 Verständnis des Algorithmus

### Farbdistanz-Keying
```
distance = length(pixel.RGB - KeyColor.RGB)
alpha = 1.0 - smoothstep(Tolerance - Softness, Tolerance + Softness, distance)
```

- Berechnet euklidische Distanz im RGB-Farbraum
- Näher an Key Color = transparenter
- Softness erzeugt graduellen Übergang

### Spill Suppression
```
1. Konvertiere Pixel zu HSV-Farbraum
2. Vergleiche Pixel-Hue mit Key-Color-Hue
3. Falls Hues ähnlich, reduziere Sättigung
4. Konvertiere zurück zu RGB
```

- Entfernt Farbkontamination intelligent
- Erhält natürliche Motivfarben
- Fokussiert auf Kanten, wo Spill auftritt

### Edge Erode/Grow
```
alpha = clamp(alpha + EdgeErode, 0.0, 1.0)
```

- Positive Werte: Schrumpft Matte (erode)
- Negative Werte: Erweitert Matte (grow)
- Einfache aber effektive Kantenkontrolle

## 🎬 Best Practices

### 🎬 Dreh-Tipps (für beste Keying-Ergebnisse)
- **Gleichmäßige Beleuchtung** am Greenscreen ist kritisch
- **Trennen Sie Motiv** vom Hintergrund (2-3 Meter Minimum)
- **Vermeiden Sie Schatten** auf Greenscreen
- **Nutzen Sie korrekte Belichtung** - nicht zu hell, nicht zu dunkel
- **Gleichen Sie Motiv-Beleuchtung** an beabsichtigten Hintergrund an

### 🔧 Keying-Workflow
1. Starten Sie immer mit aktiviertem **Show Matte**
2. Passen Sie zuerst **Tolerance** an (Abdeckung erzielen)
3. Dann passen Sie **Softness** an (Kanten verfeinern)
4. Wenden Sie **Spill Suppression** an, nachdem Keying gut ist
5. Nutzen Sie **Edge Erode** als finale Feinabstimmung
6. Deaktivieren Sie Show Matte und prüfen Sie finales Ergebnis
7. Compositen und passen Sie Beleuchtung/Farbe zum Angleichen an

### ⚠️ Häufige Fehler vermeiden
- ❌ Tolerance zu hoch setzen (entfernt Motiv-Details)
- ❌ Spill Suppression vergessen (Grün-/Blau-Fringing)
- ❌ Edge Erode nutzen bevor guter Basis-Key vorhanden
- ❌ Show Matte nicht prüfen (blinde Anpassungen)
- ❌ Im falschen Farbraum keyen (nutzen Sie sRGB wie bereitgestellt)

## 🔗 Kombination mit anderen Nodes

**Essentielle Begleiter:**
- **⭐ Alpha Composite - for Key-in-Mix**: Compositen Sie gekeyte Footage über Hintergründe
- **🎨 Color Grading Nodes**: Gleichen Sie Vordergrund-/Hintergrund-Beleuchtung und Farbe an
- **💡 Color Replace**: Zusätzliche Spill-Entfernung oder Farbkorrektur
- **🔄 2D Modifier**: Wenden Sie Effekte vor oder nach Keying an

**Fortgeschrittene Kombinationen:**
- **Garbage Mattes**: Nutzen Sie Masken zur Isolierung des Keying-Bereichs
- **Multiple Keys**: Stapeln Sie für komplexe Mehrfarb-Hintergründe
- **Color Correction**: Gleichen Sie Beleuchtung zwischen Layern an
- **Edge Effects**: Fügen Sie Glows, Outlines nach Keying hinzu

## 🔧 Fehlerbehebungs-Guide

### Problem: Hintergrund nicht vollständig entfernt
**Lösungen**:
- ✅ Erhöhen Sie Tolerance
- ✅ Prüfen Sie, ob Key Color korrekt ist (nutzen Sie Picker auf Hintergrund)
- ✅ Aktivieren Sie Show Matte, um zu sehen, was nicht gekeyt wird
- ✅ Beleuchtung könnte zu ungleichmäßig sein - erwägen Sie mehrere Keys

### Problem: Motiv wird transparent
**Lösungen**:
- ✅ Verringern Sie Tolerance
- ✅ Motiv könnte Key-Farbe enthalten - nutzen Sie zuerst Color Replace
- ✅ Prüfen Sie, ob Motiv zu ähnlich zur Hintergrundfarbe ist
- ✅ Nutzen Sie negativen Edge-Erode-Wert zum Erweitern der Matte

### Problem: Grün-/Blau-Fringing an Kanten
**Lösungen**:
- ✅ Erhöhen Sie Spill Suppression (0.5-0.8)
- ✅ Nutzen Sie Color-Replace-Node nach Chroma Key
- ✅ Passen Sie Edge Erode leicht positiv an (+0.05 bis +0.1)
- ✅ Könnte bessere Trennung beim Filmen benötigen

### Problem: Kanten zu scharf/hart
**Lösungen**:
- ✅ Erhöhen Sie Softness (0.15-0.3)
- ✅ Verringern Sie Tolerance leicht
- ✅ Prüfen Sie, ob Original-Footage scharfe Kanten hat (beabsichtigt)
- ✅ Könnte Motion-Blur- oder Edge-Blur-Effekt benötigen

### Problem: Löcher im Motiv
**Lösungen**:
- ✅ Verringern Sie Tolerance
- ✅ Motiv könnte Key-Farb-Elemente haben (Kostüm, Requisiten)
- ✅ Nutzen Sie negativen Edge Erode zum Füllen kleiner Löcher
- ✅ Erwägen Sie separate Maskierung von Problembereichen

### Problem: Haar/feine Details verloren
**Lösungen**:
- ✅ Erhöhen Sie Softness signifikant (0.25-0.4)
- ✅ Nutzen Sie negativen Edge Erode (-0.1 bis -0.2)
- ✅ Reduzieren Sie Tolerance leicht
- ✅ Filmen Sie mit besserer Hintergrund-Trennung

## ⚡ Performance-Tipps

- ✅ Deaktivieren Sie **Show Matte**, wenn nicht angepasst wird (leichter Performance-Gewinn)
- ✅ Nutzen Sie angemessene **Softness** - übermäßige Werte verlangsamen
- ✅ **Spill Suppression** hat minimale Performance-Kosten
- ✅ Node ist für Echtzeit-Nutzung optimiert
- ✅ Funktioniert gut mit Video-Wiedergabe und Live-Input

## 💡 Warum dieser Node erstellt wurde

Viele Keying-Lösungen sind entweder zu einfach (schlechte Ergebnisse) oder zu komplex (überwältigend). **Chroma Key - classical** findet die perfekte Balance:

- ✅ **Professionelle Ergebnisse** ohne professionelle Komplexität
- ✅ **Essentielle Features** (Keying, Spill, Edge-Control) in einem Node
- ✅ **Visuelles Feedback** mit Show-Matte-Feature
- ✅ **Nahtlose Integration** mit Alpha-Composite-Workflow
- ✅ **Echtzeit-fähig** für Live- und interaktive Arbeit

Dies macht professionelle Greenscreen-Arbeit für jeden in Coollab zugänglich!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
