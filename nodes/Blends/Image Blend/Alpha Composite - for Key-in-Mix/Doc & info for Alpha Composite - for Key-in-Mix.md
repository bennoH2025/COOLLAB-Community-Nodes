[English](#alpha-composite---for-key-in-mix---documentation) | [Deutsch](#alpha-composite---for-key-in-mix---dokumentation)

---

# Alpha Composite - for Key-in-Mix - Documentation

## Overview

**Alpha Composite - for Key-in-Mix** is a professional compositing node designed to seamlessly blend foreground images (with transparency/alpha channel) over background images with precise mix control. This node is the perfect companion for chroma key workflows, making it easy to composite keyed footage over any background with full creative control.

## Inspiration & Design Philosophy

Born from the need for a reliable, professional-grade compositing tool in Coollab:

- **Proper Alpha Handling**: Correctly implements alpha compositing mathematics for clean, artifact-free results
- **Mix Control**: Unlike simple "over" operations, this node allows gradual blending from 0% to 100%
- **Chroma Key Workflow**: Specifically designed to work perfectly with Chroma Key nodes
- **Professional Standard**: Implements industry-standard "over" compositing algorithm

This node fills a critical gap in the Coollab ecosystem, providing the missing link between keying and final composition.

## Key Features

### 🎬 Professional Alpha Compositing
Implements the standard "over" operation used in professional video compositing:
- Mathematically correct alpha blending
- No artifacts or unexpected transparency issues
- Clean edges and smooth transitions
- Works with premultiplied or straight alpha

### 🎚️ Mix Control
The Mix parameter provides unprecedented control:
- **0.0** = Background only (foreground completely invisible)
- **0.5** = 50/50 blend between foreground and background
- **1.0** = Full composite (standard compositing result)
- Smooth interpolation between all values

### 🔑 Perfect for Keying
Designed specifically to work with chroma key workflows:
- Accepts alpha channel from Chroma Key nodes
- Respects transparency perfectly
- No "50/50 problem" found in other blend nodes
- Clean integration with keyed footage

### ⚡ Real-time Performance
- Optimized for live performance
- Fast compositing calculations
- Suitable for video playback and live visuals

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Foreground** | UV→sRGB_StraightA | - | The image with transparency (e.g., from Chroma Key node). This layer will be composited over the background. |
| **Background** | UV→sRGB_StraightA | - | The background image that will be visible behind/through the foreground. |
| **Mix** | 0.0 - 1.0 | 1.0 | Blend amount: 0 = background only, 1 = full composite, 0.5 = 50/50 blend. |

## Creative Usage Tips

### 🎥 Chroma Key Workflow

**Standard Greenscreen Compositing:**
1. Import your greenscreen footage → **Foreground source**
2. Apply **Chroma Key** node to remove green
3. Connect Chroma Key output → **Alpha Composite Foreground input**
4. Import/create background image → **Background input**
5. Set **Mix to 1.0** for full composite
6. Adjust Chroma Key parameters to perfect the matte

**Advanced Keying:**
- Use **Color Replace** before compositing to fix color spill
- Stack multiple **Chroma Key** nodes for difficult shots
- Add **Color Grading** nodes to match foreground and background lighting

### 🎨 Creative Blending

**Ghosting Effect:**
1. Use same image for Foreground and Background
2. Apply different effects to each path
3. Set Mix to 0.3-0.7 for semi-transparent overlay
4. Creates double-exposure or ghosting effects

**Transition Effect:**
1. Use two different images (Foreground and Background)
2. Animate Mix from 0 to 1 over time
3. Creates smooth crossfade transition
4. Add movement to either layer for dynamic transitions

**Layered Compositions:**
1. Create multiple Alpha Composite nodes in sequence
2. Each one adds a new layer to the composition
3. Control each layer's visibility independently with Mix
4. Build complex multi-layer scenes

### 🌈 Combining with Effects

**Highly Recommended Combinations:**
- **⭐ Chroma Key**: The primary use case - removes backgrounds
- **🎨 Color Grading nodes**: Match foreground and background color/lighting
- **💡 Color Replace**: Fix color spill before compositing
- **🔄 2D Modifiers**: Apply effects to foreground before compositing
- **🎭 Blend Modes**: Stack Alpha Composite with artistic blend modes

## Workflow Examples

### Example 1: Simple Greenscreen Composite
1. Load greenscreen footage with **Image** node
2. Add **Chroma Key** node:
   - Set Key Color to green (use color picker)
   - Adjust Tolerance: ~0.3
   - Adjust Softness: ~0.1
   - Enable "Show Matte" to preview selection
3. Add **Alpha Composite - for Key-in-Mix**:
   - Connect Chroma Key → Foreground
   - Load background image → Background
   - Set Mix: 1.0
4. Fine-tune Chroma Key parameters until edges are clean

### Example 2: Spill Correction Workflow
1. Apply **Chroma Key** to remove green background
2. Add **Color Replace** node:
   - Target Color: green
   - Adjust to remove green spill from foreground
3. Connect to **Alpha Composite**:
   - Add your desired background
   - Set Mix: 1.0
4. Optionally add **Color Grading** to match lighting

### Example 3: Animated Reveal
1. Set up foreground with transparency
2. Set up background image
3. Connect to **Alpha Composite**
4. Animate **Mix** parameter:
   - Start at 0.0 (only background)
   - Animate to 1.0 (full composite)
   - Use **Time** node for automatic animation
5. Creates smooth reveal effect

### Example 4: Multi-Layer Composite
1. **First Layer**: Background image → Input to first Alpha Composite
2. **Second Layer**: Keyed footage → Foreground of first Alpha Composite
3. **Third Layer**: Output of first → Background of second Alpha Composite
4. **Fourth Layer**: Another keyed element → Foreground of second Alpha Composite
5. Continue stacking for complex scenes

## Technical Details

- **Node Type**: Compositor (UV inputs → sRGB_StraightA output)
- **Category**: Compositing / Blending
- **Algorithm**: Standard "over" operation with mix interpolation
- **Alpha Handling**: Proper alpha compositing mathematics
- **Color Space**: sRGB with straight alpha
- **Performance**: Optimized for real-time use

## Understanding the Algorithm

The node implements the standard alpha compositing formula:
```
Result.RGB = (Foreground.RGB × Foreground.A + Background.RGB × Background.A × (1 - Foreground.A)) / Result.A
Result.A = Foreground.A + Background.A × (1 - Foreground.A)
```

This ensures:
- ✅ Proper transparency handling
- ✅ No edge artifacts
- ✅ Mathematically correct color blending
- ✅ Industry-standard results

The **Mix** parameter then blends between the pure background and this composited result.

## Troubleshooting

### Problem: Edges look wrong
**Solution**: 
- Check your Chroma Key settings (Softness, Tolerance)
- Ensure Foreground has proper alpha channel
- Try adjusting Edge Erode in Chroma Key node

### Problem: Foreground too transparent
**Solution**:
- Check Mix is set to 1.0
- Verify Chroma Key isn't removing too much
- Disable "Show Matte" in Chroma Key if enabled

### Problem: Color spill visible
**Solution**:
- Add **Color Replace** node after Chroma Key
- Or increase Spill Suppression in Chroma Key
- Match foreground/background lighting with Color Grading

### Problem: 50/50 blend when I want full composite
**Solution**:
- Set Mix parameter to **1.0** (not 0.5!)
- Mix at 0.5 is intentionally a 50/50 blend

## Why This Node Was Created

Many existing blend nodes in Coollab had a critical flaw: they would always create 50/50 blends, making proper compositing impossible. This node was specifically designed to:

- ✅ Provide **proper alpha compositing** (not just 50/50 mixing)
- ✅ Allow **full control** over blend amount via Mix parameter
- ✅ Work **perfectly with Chroma Key** workflows
- ✅ Implement **industry-standard** compositing mathematics

This fills a critical gap in the Coollab ecosystem!

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#alpha-composite---for-key-in-mix---documentation) | [Deutsch](#alpha-composite---for-key-in-mix---dokumentation)

---

# Alpha Composite - for Key-in-Mix - Dokumentation

## Übersicht

**Alpha Composite - for Key-in-Mix** ist ein professioneller Compositing-Node, der entwickelt wurde, um Vordergrundbilder (mit Transparenz/Alpha-Kanal) nahtlos über Hintergrundbilder mit präziser Mix-Kontrolle zu blenden. Dieser Node ist der perfekte Begleiter für Chroma-Key-Workflows und macht es einfach, gekeyte Aufnahmen über jeden Hintergrund mit voller kreativer Kontrolle zu compositen.

## 🎯 Inspiration & Design-Philosophie

Geboren aus dem Bedarf nach einem zuverlässigen, professionellen Compositing-Tool in Coollab:

- **Korrekte Alpha-Handhabung**: Implementiert mathematisch korrekte Alpha-Compositing für saubere, artefaktfreie Ergebnisse
- **Mix-Kontrolle**: Im Gegensatz zu einfachen "Over"-Operationen ermöglicht dieser Node graduelles Blending von 0% bis 100%
- **Chroma-Key-Workflow**: Speziell entwickelt, um perfekt mit Chroma-Key-Nodes zu funktionieren
- **Professioneller Standard**: Implementiert den industriestandard "Over"-Compositing-Algorithmus

Dieser Node füllt eine kritische Lücke im Coollab-Ökosystem und bietet die fehlende Verbindung zwischen Keying und finaler Komposition.

## ⭐ Hauptmerkmale

### 🎬 Professionelles Alpha-Compositing
Implementiert die Standard-"Over"-Operation aus professionellem Video-Compositing:
- Mathematisch korrektes Alpha-Blending
- Keine Artefakte oder unerwartete Transparenzprobleme
- Saubere Kanten und weiche Übergänge
- Funktioniert mit premultiplied oder straight alpha

### 🎚️ Mix-Kontrolle
Der Mix-Parameter bietet beispiellose Kontrolle:
- **0.0** = Nur Hintergrund (Vordergrund komplett unsichtbar)
- **0.5** = 50/50 Blend zwischen Vordergrund und Hintergrund
- **1.0** = Vollständiges Composite (Standard-Compositing-Ergebnis)
- Weiche Interpolation zwischen allen Werten

### 🔑 Perfekt für Keying
Speziell für Chroma-Key-Workflows entwickelt:
- Akzeptiert Alpha-Kanal von Chroma-Key-Nodes
- Respektiert Transparenz perfekt
- Kein "50/50-Problem" anderer Blend-Nodes
- Saubere Integration mit gekeyter Footage

### ⚡ Echtzeit-Performance
- Optimiert für Live-Performance
- Schnelle Compositing-Berechnungen
- Geeignet für Video-Wiedergabe und Live-Visuals

## 📊 Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Foreground** | UV→sRGB_StraightA | - | Das Bild mit Transparenz (z.B. von Chroma-Key-Node). Dieser Layer wird über den Hintergrund compositet. |
| **Background** | UV→sRGB_StraightA | - | Das Hintergrundbild, das hinter/durch den Vordergrund sichtbar sein wird. |
| **Mix** | 0.0 - 1.0 | 1.0 | Blend-Menge: 0 = nur Hintergrund, 1 = vollständiges Composite, 0.5 = 50/50 Blend. |

## 🎨 Kreative Nutzungstipps

### 🎥 Chroma-Key-Workflow

**Standard-Greenscreen-Compositing:**
1. Importieren Sie Ihre Greenscreen-Footage → **Foreground-Quelle**
2. Wenden Sie **Chroma Key** Node an, um Grün zu entfernen
3. Verbinden Sie Chroma-Key-Ausgabe → **Alpha Composite Foreground-Eingang**
4. Importieren/erstellen Sie Hintergrundbild → **Background-Eingang**
5. Setzen Sie **Mix auf 1.0** für vollständiges Composite
6. Passen Sie Chroma-Key-Parameter an, um die Matte zu perfektionieren

**Fortgeschrittenes Keying:**
- Nutzen Sie **Color Replace** vor dem Compositing, um Color Spill zu korrigieren
- Stapeln Sie mehrere **Chroma Key** Nodes für schwierige Aufnahmen
- Fügen Sie **Color Grading** Nodes hinzu, um Vordergrund- und Hintergrundbeleuchtung anzugleichen

### 🎨 Kreatives Blending

**Geistereffekt:**
1. Nutzen Sie dasselbe Bild für Foreground und Background
2. Wenden Sie verschiedene Effekte auf jeden Pfad an
3. Setzen Sie Mix auf 0.3-0.7 für halbtransparentes Overlay
4. Erzeugt Doppelbelichtungs- oder Geistereffekte

**Übergangseffekt:**
1. Nutzen Sie zwei verschiedene Bilder (Foreground und Background)
2. Animieren Sie Mix von 0 bis 1 über Zeit
3. Erzeugt weichen Crossfade-Übergang
4. Fügen Sie Bewegung zu beiden Layern für dynamische Übergänge hinzu

**Mehrschichtige Kompositionen:**
1. Erstellen Sie mehrere Alpha-Composite-Nodes in Sequenz
2. Jeder fügt einen neuen Layer zur Komposition hinzu
3. Kontrollieren Sie die Sichtbarkeit jedes Layers unabhängig mit Mix
4. Bauen Sie komplexe Multi-Layer-Szenen

### 🌈 Kombination mit Effekten

**Sehr empfohlene Kombinationen:**
- **⭐ Chroma Key**: Der primäre Anwendungsfall - entfernt Hintergründe
- **🎨 Color Grading Nodes**: Gleichen Sie Vordergrund- und Hintergrundfarbe/Beleuchtung an
- **💡 Color Replace**: Korrigieren Sie Color Spill vor dem Compositing
- **🔄 2D Modifier**: Wenden Sie Effekte auf Vordergrund vor dem Compositing an
- **🎭 Blend Modes**: Stapeln Sie Alpha Composite mit künstlerischen Blend-Modi

## 💡 Workflow-Beispiele

### Beispiel 1: Einfaches Greenscreen-Composite
1. Laden Sie Greenscreen-Footage mit **Image** Node
2. Fügen Sie **Chroma Key** Node hinzu:
   - Setzen Sie Key Color auf Grün (Farbwähler nutzen)
   - Passen Sie Tolerance an: ~0.3
   - Passen Sie Softness an: ~0.1
   - Aktivieren Sie "Show Matte" zur Vorschau der Auswahl
3. Fügen Sie **Alpha Composite - for Key-in-Mix** hinzu:
   - Verbinden Sie Chroma Key → Foreground
   - Laden Sie Hintergrundbild → Background
   - Setzen Sie Mix: 1.0
4. Feinabstimmung der Chroma-Key-Parameter bis Kanten sauber sind

### Beispiel 2: Spill-Korrektur-Workflow
1. Wenden Sie **Chroma Key** an, um grünen Hintergrund zu entfernen
2. Fügen Sie **Color Replace** Node hinzu:
   - Target Color: Grün
   - Anpassen, um grünen Spill vom Vordergrund zu entfernen
3. Verbinden Sie mit **Alpha Composite**:
   - Fügen Sie gewünschten Hintergrund hinzu
   - Setzen Sie Mix: 1.0
4. Optional **Color Grading** hinzufügen, um Beleuchtung anzugleichen

### Beispiel 3: Animiertes Reveal
1. Richten Sie Vordergrund mit Transparenz ein
2. Richten Sie Hintergrundbild ein
3. Verbinden Sie mit **Alpha Composite**
4. Animieren Sie **Mix**-Parameter:
   - Start bei 0.0 (nur Hintergrund)
   - Animieren zu 1.0 (vollständiges Composite)
   - Nutzen Sie **Time** Node für automatische Animation
5. Erzeugt weichen Reveal-Effekt

### Beispiel 4: Multi-Layer-Composite
1. **Erster Layer**: Hintergrundbild → Eingang zu erstem Alpha Composite
2. **Zweiter Layer**: Gekeyte Footage → Foreground des ersten Alpha Composite
3. **Dritter Layer**: Ausgabe des ersten → Background des zweiten Alpha Composite
4. **Vierter Layer**: Weiteres gekeytes Element → Foreground des zweiten Alpha Composite
5. Weiteres Stapeln für komplexe Szenen

## 🔧 Technische Details

- **Node-Typ**: Compositor (UV-Eingänge → sRGB_StraightA-Ausgabe)
- **Kategorie**: Compositing / Blending
- **Algorithmus**: Standard-"Over"-Operation mit Mix-Interpolation
- **Alpha-Handhabung**: Korrekte Alpha-Compositing-Mathematik
- **Farbraum**: sRGB mit straight alpha
- **Performance**: Optimiert für Echtzeit-Nutzung

## 🧮 Verständnis des Algorithmus

Der Node implementiert die Standard-Alpha-Compositing-Formel:
```
Ergebnis.RGB = (Vordergrund.RGB × Vordergrund.A + Hintergrund.RGB × Hintergrund.A × (1 - Vordergrund.A)) / Ergebnis.A
Ergebnis.A = Vordergrund.A + Hintergrund.A × (1 - Vordergrund.A)
```

Dies gewährleistet:
- ✅ Korrekte Transparenz-Handhabung
- ✅ Keine Kanten-Artefakte
- ✅ Mathematisch korrektes Farb-Blending
- ✅ Industriestandard-Ergebnisse

Der **Mix**-Parameter blendet dann zwischen dem reinen Hintergrund und diesem compositeten Ergebnis.

## 🔧 Fehlerbehebung

### Problem: Kanten sehen falsch aus
**Lösung**: 
- Überprüfen Sie Chroma-Key-Einstellungen (Softness, Tolerance)
- Stellen Sie sicher, dass Foreground korrekten Alpha-Kanal hat
- Versuchen Sie Edge Erode im Chroma-Key-Node anzupassen

### Problem: Vordergrund zu transparent
**Lösung**:
- Prüfen Sie, ob Mix auf 1.0 gesetzt ist
- Verifizieren Sie, dass Chroma Key nicht zu viel entfernt
- Deaktivieren Sie "Show Matte" in Chroma Key, falls aktiviert

### Problem: Color Spill sichtbar
**Lösung**:
- Fügen Sie **Color Replace** Node nach Chroma Key hinzu
- Oder erhöhen Sie Spill Suppression in Chroma Key
- Gleichen Sie Vordergrund-/Hintergrundbeleuchtung mit Color Grading an

### Problem: 50/50 Blend statt vollständigem Composite
**Lösung**:
- Setzen Sie Mix-Parameter auf **1.0** (nicht 0.5!)
- Mix bei 0.5 ist absichtlich ein 50/50 Blend

## 💡 Warum dieser Node erstellt wurde

Viele existierende Blend-Nodes in Coollab hatten einen kritischen Fehler: Sie erzeugten immer 50/50-Blends, was korrektes Compositing unmöglich machte. Dieser Node wurde speziell entwickelt, um:

- ✅ **Korrektes Alpha-Compositing** zu bieten (nicht nur 50/50-Mixing)
- ✅ **Volle Kontrolle** über Blend-Menge via Mix-Parameter zu ermöglichen
- ✅ **Perfekt mit Chroma-Key-Workflows** zu funktionieren
- ✅ **Industriestandard**-Compositing-Mathematik zu implementieren

Dies füllt eine kritische Lücke im Coollab-Ökosystem!

## 📜 Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
