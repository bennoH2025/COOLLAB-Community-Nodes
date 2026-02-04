[English](#body-vasus-of-colab---documentation) | [Deutsch](#body-vasus-of-colab---dokumentation)

---

# Body Vasus of Colab - Documentation

## Overview

**Body Vasus of Colab** creates simple pottery and vase shapes by rotating a profile around a vertical axis. Open top, closed bottom - perfect for vases, pots, bowls, and containers.

## Key Features

- 🏺 **7 Profile Types**: Cylinder, Cone, Sphere, Vase, Hourglass, Bulb, Bowl
- 🔓 **Open Top**: Natural vase opening
- 🔒 **Closed Bottom**: Flat base cap
- 🎨 **Simple Controls**: Easy to use, perfect for beginners
- ⚡ **Real-time**: Interactive adjustment

## Parameters

| Parameter | Description |
|-----------|-------------|
| **Profile Type** | 0=Cylinder, 1=Cone, 2=Sphere, 3=Vase, 4=Hourglass, 5=Bulb, 6=Bowl |
| **Height** | Total height of the object |
| **Base Radius** | Radius at bottom |
| **Top Radius** | Radius at top opening |
| **Bulge** | Bulge amount (for Vase/Hourglass/Bulb/Bowl profiles) |
| **Smoothness** | Curve smoothness (for vase/bowl shapes) |
| **Position** | XYZ position offset |

## Profile Types

### 0 - Cylinder
Straight sides, linear taper from base to top radius.

### 1 - Cone
Linear taper, same as cylinder.

### 2 - Sphere
Circular profile creates spherical or egg-like forms.

### 3 - Vase
Smooth bulge in the middle, classic vase shape.

### 4 - Hourglass
Pinch/constriction in the middle, creates hourglass forms.

### 5 - Bulb
Bulge at bottom, narrow at top - onion or bulb shape.

### 6 - Bowl
Smooth curve, wider at top - bowl or chalice shape.

## 📦 Included Presets

### Big Pot
- **Profile Type**: 4 (Hourglass)
- **Height**: 0.7
- **Base Radius**: 0.15
- **Top Radius**: 0.22
- **Bulge**: -0.59
- Creates a wide pot with slight inward pinch

### Ovum Vase
- **Profile Type**: 2 (Sphere)
- **Height**: 0.7
- Rounded egg-like vase form

### Standard Vase
- **Profile Type**: 6 (Bowl)
- **Height**: 0.6
- **Base Radius**: 0.19
- **Top Radius**: 0.37
- **Bulge**: -2.97
- Classic vase with wide opening

## Quick Start

### Create a Simple Vase
1. Add **Body Vasus of Colab** node
2. Set **Profile Type**: 3 (Vase)
3. **Height**: 1.0
4. **Base Radius**: 0.3
5. **Top Radius**: 0.4
6. **Bulge**: 0.3
7. Result: Classic vase shape! 🏺

### Create a Bowl
1. **Profile Type**: 6 (Bowl)
2. **Height**: 0.5
3. **Base Radius**: 0.2
4. **Top Radius**: 0.6
5. **Bulge**: 0.2
6. Result: Wide, shallow bowl

### Create a Bottle
1. **Profile Type**: 0 (Cylinder)
2. **Height**: 2.0
3. **Base Radius**: 0.5
4. **Top Radius**: 0.2
5. Result: Bottle with narrow neck

## Tips

- **Bulge Parameter**: Only affects types 3, 4, 5, 6
- **Negative Bulge**: Creates inward curves (pinch)
- **Positive Bulge**: Creates outward curves (expand)
- **Open Top**: Perfect for vases, containers, pots
- **Closed Bottom**: Solid base, stands upright

## Troubleshooting

**Shape too tall/short?**
- Adjust **Height** parameter

**Opening too wide/narrow?**
- Adjust **Top Radius**

**Base unstable?**
- Increase **Base Radius** for wider, more stable base

**Want more control?**
- Try **Body of Revolution - easy** for 5 radius control points

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#body-vasus-of-colab---documentation) | [Deutsch](#body-vasus-of-colab---dokumentation)

---

# Body Vasus of Colab - Dokumentation

## Übersicht

**Body Vasus of Colab** erstellt einfache Töpferei- und Vasenformen durch Rotation eines Profils um eine vertikale Achse. Oben offen, unten geschlossen - perfekt für Vasen, Töpfe, Schalen und Behälter.

## Hauptmerkmale

- 🏺 **7 Profiltypen**: Zylinder, Kegel, Kugel, Vase, Sanduhr, Birne, Schale
- 🔓 **Offene Oberseite**: Natürliche Vasenöffnung
- 🔒 **Geschlossener Boden**: Flacher Boden-Abschluss
- 🎨 **Einfache Kontrollen**: Leicht zu nutzen, perfekt für Anfänger
- ⚡ **Echtzeit**: Interaktive Anpassung

## Parameter

| Parameter | Beschreibung |
|-----------|--------------|
| **Profile Type** | 0=Zylinder, 1=Kegel, 2=Kugel, 3=Vase, 4=Sanduhr, 5=Birne, 6=Schale |
| **Height** | Gesamthöhe des Objekts |
| **Base Radius** | Radius unten |
| **Top Radius** | Radius bei Öffnung oben |
| **Bulge** | Wölbungsstärke (für Vase/Sanduhr/Birne/Schale-Profile) |
| **Smoothness** | Kurven-Glätte (für Vasen/Schalen-Formen) |
| **Position** | XYZ-Positions-Verschiebung |

## Profiltypen

### 0 - Zylinder
Gerade Seiten, lineares Verjüngen von Basis zu Oben-Radius.

### 1 - Kegel
Lineares Verjüngen, gleich wie Zylinder.

### 2 - Kugel
Kreisförmiges Profil erzeugt sphärische oder ei-artige Formen.

### 3 - Vase
Glatte Wölbung in der Mitte, klassische Vasenform.

### 4 - Sanduhr
Einschnürung in der Mitte, erzeugt Sanduhr-Formen.

### 5 - Birne
Wölbung unten, schmal oben - Zwiebel- oder Birnenform.

### 6 - Schale
Glatte Kurve, breiter oben - Schalen- oder Kelch-Form.

## 📦 Mitgelieferte Presets

### Big Pot
- **Profile Type**: 4 (Sanduhr)
- **Height**: 0.7
- **Base Radius**: 0.15
- **Top Radius**: 0.22
- **Bulge**: -0.59
- Erzeugt breiten Topf mit leichter Einwärts-Einschnürung

### Ovum Vase
- **Profile Type**: 2 (Kugel)
- **Height**: 0.7
- Abgerundete ei-artige Vasenform

### Standard Vase
- **Profile Type**: 6 (Schale)
- **Height**: 0.6
- **Base Radius**: 0.19
- **Top Radius**: 0.37
- **Bulge**: -2.97
- Klassische Vase mit breiter Öffnung

## Schnellstart

### Einfache Vase Erstellen
1. **Body Vasus of Colab** Node hinzufügen
2. **Profile Type**: 3 (Vase) setzen
3. **Height**: 1.0
4. **Base Radius**: 0.3
5. **Top Radius**: 0.4
6. **Bulge**: 0.3
7. Ergebnis: Klassische Vasenform! 🏺

### Schale Erstellen
1. **Profile Type**: 6 (Schale)
2. **Height**: 0.5
3. **Base Radius**: 0.2
4. **Top Radius**: 0.6
5. **Bulge**: 0.2
6. Ergebnis: Breite, flache Schale

### Flasche Erstellen
1. **Profile Type**: 0 (Zylinder)
2. **Height**: 2.0
3. **Base Radius**: 0.5
4. **Top Radius**: 0.2
5. Ergebnis: Flasche mit schmalem Hals

## Tipps

- **Bulge-Parameter**: Betrifft nur Typen 3, 4, 5, 6
- **Negative Wölbung**: Erzeugt Einwärts-Kurven (Einschnürung)
- **Positive Wölbung**: Erzeugt Auswärts-Kurven (Expansion)
- **Offene Oberseite**: Perfekt für Vasen, Behälter, Töpfe
- **Geschlossener Boden**: Solide Basis, steht aufrecht

## Fehlerbehebung

**Form zu groß/klein?**
- **Height**-Parameter anpassen

**Öffnung zu breit/schmal?**
- **Top Radius** anpassen

**Basis instabil?**
- **Base Radius** erhöhen für breitere, stabilere Basis

**Mehr Kontrolle gewünscht?**
- Probieren Sie **Body of Revolution - easy** für 5 Radius-Kontrollpunkte

## Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
