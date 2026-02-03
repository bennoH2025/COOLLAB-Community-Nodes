[English](#brightness--contrast---documentation) | [Deutsch](#brightness--contrast---dokumentation)

---

# Brightness & Contrast - Documentation

## Overview

**Brightness & Contrast** is a simple, essential tool for quick image adjustments. Two controls, instant results - perfect when you need fast corrections without complex color grading workflows.

## Key Features

- **Brightness**: Lighten or darken your image (-1 to +1)
- **Contrast**: Increase or decrease tonal separation (-1 to +1)
- **Simple & Fast**: Two sliders, that's it
- **Real-time**: Instant visual feedback

## Parameters

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Input** | UV→sRGB_StraightA | - | The image to adjust |
| **Brightness** | -1.0 - 1.0 | 0.0 | Brightness adjustment. Negative = darker, positive = lighter |
| **Contrast** | -1.0 - 1.0 | 0.0 | Contrast adjustment. Negative = flat, positive = punchy |

## Usage Tips

### Quick Adjustments

**Brighten Dark Image:**
- Brightness: +0.2 to +0.4
- Contrast: 0.0 or +0.1

**Darken Bright Image:**
- Brightness: -0.2 to -0.3
- Contrast: 0.0 or slight increase

**Add Punch:**
- Brightness: 0.0
- Contrast: +0.2 to +0.4

**Flatten/Soften:**
- Brightness: 0.0
- Contrast: -0.2 to -0.3

### Common Combinations

**Washed Out Fix:**
- Brightness: -0.1
- Contrast: +0.3

**Low-Light Recovery:**
- Brightness: +0.3
- Contrast: +0.15

**Soft Dreamy Look:**
- Brightness: +0.15
- Contrast: -0.2

**High Contrast Drama:**
- Brightness: -0.05
- Contrast: +0.5

## How It Works

**Brightness:**
- Adds value to all pixels
- Simple: `rgb = rgb + brightness`
- Affects entire image uniformly

**Contrast:**
- Expands or compresses tonal range
- Pivots around midpoint (0.5)
- Formula: `(rgb - 0.5) × factor + 0.5`
- Positive: darker darks, brighter brights
- Negative: compressed, flat look

## When to Use

**Use Brightness & Contrast when:**
- ✅ Need quick adjustments
- ✅ Simple corrections
- ✅ Starting point before detailed grading
- ✅ Fast preview/experimentation

**Use Color Grading nodes when:**
- ❌ Need selective control (shadows/mids/highlights)
- ❌ Color shifts required
- ❌ Professional color correction
- ❌ Complex tonal adjustments

## Tips

- Start with **Brightness** first, then adjust **Contrast**
- Small values (±0.1 to ±0.2) often enough
- Extreme values (±0.5+) can clip blacks/whites
- Combine with saturation for complete look

## Troubleshooting

**Problem: Image too dark after contrast**
- Increase Brightness to compensate

**Problem: Lost detail in shadows/highlights**
- Reduce Contrast value
- Use Color Grading - Tonal for selective control

**Problem: Colors look wrong**
- This node doesn't affect color
- Use Color Grading - Basic for saturation

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#brightness--contrast---documentation) | [Deutsch](#brightness--contrast---dokumentation)

---

# Brightness & Contrast - Dokumentation

## Übersicht

**Brightness & Contrast** ist ein einfaches, essentielles Tool für schnelle Bildanpassungen. Zwei Kontrollen, sofortige Ergebnisse - perfekt, wenn Sie schnelle Korrekturen ohne komplexe Color-Grading-Workflows benötigen.

## Hauptmerkmale

- **Brightness**: Hellen Sie Ihr Bild auf oder dunkeln Sie es ab (-1 bis +1)
- **Contrast**: Erhöhen oder verringern Sie tonale Trennung (-1 bis +1)
- **Einfach & Schnell**: Zwei Slider, das war's
- **Echtzeit**: Sofortiges visuelles Feedback

## Parameter

| Parameter | Bereich | Standard | Beschreibung |
|-----------|---------|----------|--------------|
| **Input** | UV→sRGB_StraightA | - | Das anzupassende Bild |
| **Brightness** | -1.0 - 1.0 | 0.0 | Helligkeits-Anpassung. Negativ = dunkler, positiv = heller |
| **Contrast** | -1.0 - 1.0 | 0.0 | Kontrast-Anpassung. Negativ = flach, positiv = knackig |

## Nutzungstipps

### Schnelle Anpassungen

**Dunkles Bild aufhellen:**
- Brightness: +0.2 bis +0.4
- Contrast: 0.0 oder +0.1

**Helles Bild abdunkeln:**
- Brightness: -0.2 bis -0.3
- Contrast: 0.0 oder leichte Erhöhung

**Punch hinzufügen:**
- Brightness: 0.0
- Contrast: +0.2 bis +0.4

**Abflachen/Weicher machen:**
- Brightness: 0.0
- Contrast: -0.2 bis -0.3

### Häufige Kombinationen

**Ausgewaschenes Fix:**
- Brightness: -0.1
- Contrast: +0.3

**Low-Light-Wiederherstellung:**
- Brightness: +0.3
- Contrast: +0.15

**Weicher Verträumter Look:**
- Brightness: +0.15
- Contrast: -0.2

**Hochkontrast-Drama:**
- Brightness: -0.05
- Contrast: +0.5

## Wie es funktioniert

**Brightness:**
- Addiert Wert zu allen Pixeln
- Einfach: `rgb = rgb + brightness`
- Betrifft gesamtes Bild gleichmäßig

**Contrast:**
- Expandiert oder komprimiert Tonbereich
- Dreht um Mittelpunkt (0.5)
- Formel: `(rgb - 0.5) × factor + 0.5`
- Positiv: dunklere Dunkeltöne, hellere Helltöne
- Negativ: komprimiert, flacher Look

## Wann nutzen

**Nutzen Sie Brightness & Contrast wenn:**
- ✅ Schnelle Anpassungen nötig
- ✅ Einfache Korrekturen
- ✅ Startpunkt vor detailliertem Grading
- ✅ Schnelle Vorschau/Experimentieren

**Nutzen Sie Color Grading Nodes wenn:**
- ❌ Selektive Kontrolle nötig (Schatten/Mids/Highlights)
- ❌ Farbverschiebungen erforderlich
- ❌ Professionelle Farbkorrektur
- ❌ Komplexe tonale Anpassungen

## Tipps

- Starten Sie mit **Brightness** zuerst, dann **Contrast** anpassen
- Kleine Werte (±0.1 bis ±0.2) oft ausreichend
- Extreme Werte (±0.5+) können Schwarztöne/Weißtöne clippen
- Mit Sättigung kombinieren für kompletten Look

## Fehlerbehebung

**Problem: Bild zu dunkel nach Kontrast**
- Erhöhen Sie Brightness zur Kompensation

**Problem: Verlust von Detail in Schatten/Highlights**
- Reduzieren Sie Contrast-Wert
- Nutzen Sie Color Grading - Tonal für selektive Kontrolle

**Problem: Farben sehen falsch aus**
- Dieser Node beeinflusst Farbe nicht
- Nutzen Sie Color Grading - Basic für Sättigung

## Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
