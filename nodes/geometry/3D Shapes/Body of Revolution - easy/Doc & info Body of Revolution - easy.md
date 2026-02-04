[English](#body-of-revolution---easy---documentation) | [Deutsch](#body-of-revolution---easy---dokumentation)

---

# Body of Revolution - easy - Documentation

## Overview

**Body of Revolution - easy** creates pottery and sculptural forms with 5 radius control points and optional eccentricity. Closed top and bottom - ideal for beginners and intermediate users who want more control than the simple vase node but less complexity than the full version.

## Key Features

- 🏺 **7 Profile Types**: Cylinder, Cone, Sphere, Vase, Hourglass, Bulb, Bowl
- 📐 **5 Radius Control Points**: Base, R1, R2, R3, Top for custom profiles
- ↗️ **Optional Eccentricity**: Tilt and warp shapes asymmetrically
- 🔒 **Closed Caps**: Top and bottom sealed with flat caps
- 🎨 **Easy to Learn**: Simple yet powerful controls
- ⚡ **Real-time**: Interactive adjustment

## Parameters

| Parameter | Range | Description |
|-----------|-------|-------------|
| **Profile Type** | 0-6 | 0=Cylinder, 1=Cone, 2=Sphere, 3=Vase, 4=Hourglass, 5=Bulb, 6=Bowl |
| **Height** | 0.1+ | Total height of the object |
| **Base Radius** | 0.01+ | Radius at bottom (0/4 height) |
| **Radius 1** | 0.01+ | Radius at 25% height (1/4) |
| **Radius 2** | 0.01+ | Radius at 50% height (2/4, middle) |
| **Radius 3** | 0.01+ | Radius at 75% height (3/4) |
| **Top Radius** | 0.01+ | Radius at top (4/4 height) |
| **Bulge** | 0.0-2.0 | Bulge amount for profile types 3-6 |
| **Smoothness** | 0.01-0.99 | Curve smoothness for profiles |
| **Enable Eccentricity** | Boolean | Toggle off-center displacement on/off |
| **Eccentric Point** | 0.0-4.0 | Height position for eccentricity (smooth control) |
| **Eccentricity Amount** | 0.0+ | How far off-center to displace |
| **Eccentricity Angle** | 0-TAU | Direction of displacement in radians |
| **Position** | Any | XYZ position offset |

## Profile Types

### 0 - Cylinder
Uses the 5 radius control points as-is, linear interpolation between them.

### 1 - Cone
Same as Cylinder - uses control points directly for linear tapering.

### 2 - Sphere
Creates spherical shapes, partially overrides control points for circular profile.

### 3 - Vase
Applies smooth bulge in middle based on control points + Bulge parameter.

### 4 - Hourglass
Applies pinch/constriction in middle based on Bulge parameter.

### 5 - Bulb
Bulge at bottom, narrow at top - onion/bulb shape.

### 6 - Bowl
Smooth curve, wider at top - bowl/chalice shape.

## Eccentricity Feature

The eccentricity feature allows you to create asymmetric, tilted, or warped forms.

### How It Works
- **Eccentric Point** (0.0-4.0): Height where displacement is strongest
  - 0.0 = Bottom
  - 1.0 = 25% height
  - 2.0 = Middle (50%)
  - 3.0 = 75% height
  - 4.0 = Top
- **Amount**: How far off-center (0 = no effect, 0.5 = moderate, 1.0+ = extreme)
- **Angle**: Direction in radians (0 = +X, 1.57 = +Z, 3.14 = -X, 4.71 = -Z)

### Eccentricity Tips
- **Amount 0.0**: No effect (effectively disabled)
- **Amount 0.1-0.3**: Subtle tilt or lean
- **Amount 0.5-0.8**: Noticeable asymmetry
- **Amount 1.0+**: Dramatic warping
- **Smooth Control**: Eccentric Point is float 0.000-4.000 for precise positioning

## 📦 Included Presets

### Show One Eccental
- **Profile Type**: 4 (Hourglass)
- **Height**: 0.72
- **Base Radius**: 0.33
- **Radius 1**: 0.18
- **Enable Eccentricity**: True
- Demonstrates eccentricity feature with tilted hourglass form

## Quick Start

### Basic Use (No Eccentricity)

**Simple Vase:**
1. Add **Body of Revolution - easy**
2. **Profile Type**: 3 (Vase)
3. Set radii:
   - **Base Radius**: 0.3
   - **Radius 1**: 0.4
   - **Radius 2**: 0.5 (middle bulge)
   - **Radius 3**: 0.4
   - **Top Radius**: 0.3
4. **Bulge**: 0.2
5. Result: Vase with custom profile! 🏺

**Custom Profile:**
1. **Profile Type**: 0 (Cylinder - raw control)
2. Manually set all 5 radii to create any profile shape
3. Smooth interpolation between points
4. Full creative control

### With Eccentricity

**Tilted Vase:**
1. Create basic vase (see above)
2. **Enable Eccentricity**: True
3. **Eccentric Point**: 2.5 (slightly above middle)
4. **Eccentricity Amount**: 0.3
5. **Eccentricity Angle**: 0.0 (tilt in +X direction)
6. Result: Asymmetric, tilted vase ↗️

**Warped Bowl:**
1. **Profile Type**: 6 (Bowl)
2. Set radii for bowl shape
3. **Enable Eccentricity**: True
4. **Eccentric Point**: 4.0 (top)
5. **Eccentricity Amount**: 0.5
6. **Eccentricity Angle**: 1.57 (tilt in +Z)
7. Result: Bowl with warped rim

## Workflow Examples

### Example 1: Classic Pot
1. **Profile Type**: 4 (Hourglass)
2. **Height**: 1.0
3. **Base Radius**: 0.4
4. **Radius 1-3**: 0.4, 0.3, 0.4
5. **Top Radius**: 0.4
6. **Bulge**: 0.3
7. Result: Pot with slight waist

### Example 2: Bottle
1. **Profile Type**: 0 (Cylinder)
2. **Height**: 2.0
3. **Base Radius**: 0.5
4. **Radius 1-2**: 0.5
5. **Radius 3**: 0.2
6. **Top Radius**: 0.15
7. Result: Bottle with narrow neck

### Example 3: Asymmetric Sculpture
1. **Profile Type**: 3 (Vase)
2. Create basic vase profile
3. **Enable Eccentricity**: True
4. **Eccentric Point**: 1.5
5. **Eccentricity Amount**: 0.6
6. **Angle**: 2.0
7. Result: Abstract tilted sculpture

## Tips & Best Practices

### Radius Control
- **Smooth Transitions**: Avoid large jumps between adjacent radii
- **Gradual Changes**: Create smooth, natural profiles
- **Experiment**: Try different radius combinations

### Bulge Parameter
- Only affects Profile Types 3, 4, 5, 6
- Start with small values (0.1-0.3)
- Negative values create inverse effects

### Eccentricity
- **Disable When Not Needed**: Set Amount to 0.0 or uncheck Enable
- **Start Subtle**: Begin with Amount 0.2-0.3
- **Smooth Point Control**: Use decimal values (e.g., 2.5, 3.75)
- **Angle**: Remember TAU = 2π ≈ 6.28 for full rotation

### Closed Caps
- Both top and bottom are sealed with flat circular caps
- Caps use the respective radius (Base/Top) at that height
- Creates complete, solid objects

## Troubleshooting

**Shape doesn't appear?**
- Check all radii are > 0.0
- Verify Height is reasonable
- Check Position offset

**Visible ridges/steps?**
- Smooth radius transitions between points
- Avoid extreme jumps

**Eccentricity too extreme?**
- Reduce Amount value
- Check Eccentric Point placement

**Want open top?**
- Use **Body Vasus of Colab** instead (open top, closed bottom)

**Need more control points?**
- Use **Body of Revolution** (full version) with 9 radius points

## Comparison with Other Nodes

| Feature | Body Vasus of Colab | Body of Revolution - easy | Body of Revolution |
|---------|---------------------|---------------------------|-------------------|
| Radius Points | 2 (Base, Top) | 5 (Base, R1-R3, Top) | 9 (Base, R1-R7, Top) |
| Eccentricity | No | Yes (1 point) | Yes (2 points) |
| Top Cap | Open | Closed | Closed |
| Bottom Cap | Closed | Closed | Closed |
| Complexity | Beginner | Easy/Intermediate | Advanced |

## Credits

- Idea and project coordination: bennoH
- Coding: claude.ai (Sonnet-4.5 model, Anthropic PBC)
- License: GPLv3.0 by bennoH, 2026

---

*For more information on writing and using Coollab nodes, visit: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*

---

[English](#body-of-revolution---easy---documentation) | [Deutsch](#body-of-revolution---easy---dokumentation)

---

# Body of Revolution - easy - Dokumentation

## Übersicht

**Body of Revolution - easy** erstellt Töpferei- und skulpturale Formen mit 5 Radius-Kontrollpunkten und optionaler Exzentrizität. Oben und unten geschlossen - ideal für Anfänger und Fortgeschrittene, die mehr Kontrolle als der einfache Vasen-Node möchten, aber weniger Komplexität als die Vollversion.

## Hauptmerkmale

- 🏺 **7 Profiltypen**: Zylinder, Kegel, Kugel, Vase, Sanduhr, Birne, Schale
- 📐 **5 Radius-Kontrollpunkte**: Basis, R1, R2, R3, Oben für benutzerdefinierte Profile
- ↗️ **Optionale Exzentrizität**: Formen asymmetrisch kippen und verformen
- 🔒 **Geschlossene Abschlüsse**: Oben und unten mit flachen Abschlüssen versiegelt
- 🎨 **Einfach zu Lernen**: Einfache aber kraftvolle Kontrollen
- ⚡ **Echtzeit**: Interaktive Anpassung

## Parameter

| Parameter | Bereich | Beschreibung |
|-----------|---------|--------------|
| **Profile Type** | 0-6 | 0=Zylinder, 1=Kegel, 2=Kugel, 3=Vase, 4=Sanduhr, 5=Birne, 6=Schale |
| **Height** | 0.1+ | Gesamthöhe des Objekts |
| **Base Radius** | 0.01+ | Radius unten (0/4 Höhe) |
| **Radius 1** | 0.01+ | Radius bei 25% Höhe (1/4) |
| **Radius 2** | 0.01+ | Radius bei 50% Höhe (2/4, Mitte) |
| **Radius 3** | 0.01+ | Radius bei 75% Höhe (3/4) |
| **Top Radius** | 0.01+ | Radius oben (4/4 Höhe) |
| **Bulge** | 0.0-2.0 | Wölbungsstärke für Profiltypen 3-6 |
| **Smoothness** | 0.01-0.99 | Kurven-Glätte für Profile |
| **Enable Eccentricity** | Boolean | Schaltet Off-Center-Verschiebung ein/aus |
| **Eccentric Point** | 0.0-4.0 | Höhenposition für Exzentrizität (glatte Kontrolle) |
| **Eccentricity Amount** | 0.0+ | Wie weit off-center verschoben wird |
| **Eccentricity Angle** | 0-TAU | Richtung der Verschiebung in Radiant |
| **Position** | Beliebig | XYZ-Positions-Verschiebung |

## Profiltypen

### 0 - Zylinder
Nutzt die 5 Radius-Kontrollpunkte wie sie sind, lineare Interpolation zwischen ihnen.

### 1 - Kegel
Gleich wie Zylinder - nutzt Kontrollpunkte direkt für lineares Verjüngen.

### 2 - Kugel
Erstellt sphärische Formen, überschreibt teilweise Kontrollpunkte für kreisförmiges Profil.

### 3 - Vase
Wendet glatte Wölbung in der Mitte basierend auf Kontrollpunkten + Bulge-Parameter an.

### 4 - Sanduhr
Wendet Einschnürung in der Mitte basierend auf Bulge-Parameter an.

### 5 - Birne
Wölbung unten, schmal oben - Zwiebel-/Birnenform.

### 6 - Schale
Glatte Kurve, breiter oben - Schalen-/Kelch-Form.

## Exzentrizitäts-Feature

Das Exzentrizitäts-Feature ermöglicht es Ihnen, asymmetrische, gekippte oder verworfene Formen zu erstellen.

### Wie es funktioniert
- **Eccentric Point** (0.0-4.0): Höhe, wo Verschiebung am stärksten ist
  - 0.0 = Unten
  - 1.0 = 25% Höhe
  - 2.0 = Mitte (50%)
  - 3.0 = 75% Höhe
  - 4.0 = Oben
- **Amount**: Wie weit off-center (0 = kein Effekt, 0.5 = moderat, 1.0+ = extrem)
- **Angle**: Richtung in Radiant (0 = +X, 1.57 = +Z, 3.14 = -X, 4.71 = -Z)

### Exzentrizitäts-Tipps
- **Amount 0.0**: Kein Effekt (effektiv deaktiviert)
- **Amount 0.1-0.3**: Subtile Neigung oder Schräge
- **Amount 0.5-0.8**: Merkbare Asymmetrie
- **Amount 1.0+**: Dramatische Verwerfung
- **Glatte Kontrolle**: Eccentric Point ist float 0.000-4.000 für präzise Positionierung

## 📦 Mitgelieferte Presets

### Show One Eccental
- **Profile Type**: 4 (Sanduhr)
- **Height**: 0.72
- **Base Radius**: 0.33
- **Radius 1**: 0.18
- **Enable Eccentricity**: True
- Demonstriert Exzentrizitäts-Feature mit gekippter Sanduhr-Form

## Schnellstart

### Basis-Nutzung (Ohne Exzentrizität)

**Einfache Vase:**
1. **Body of Revolution - easy** hinzufügen
2. **Profile Type**: 3 (Vase)
3. Radien setzen:
   - **Base Radius**: 0.3
   - **Radius 1**: 0.4
   - **Radius 2**: 0.5 (mittlere Wölbung)
   - **Radius 3**: 0.4
   - **Top Radius**: 0.3
4. **Bulge**: 0.2
5. Ergebnis: Vase mit benutzerdefiniertem Profil! 🏺

**Benutzerdefiniertes Profil:**
1. **Profile Type**: 0 (Zylinder - rohe Kontrolle)
2. Manuell alle 5 Radien setzen um jede Profilform zu erstellen
3. Glatte Interpolation zwischen Punkten
4. Volle kreative Kontrolle

### Mit Exzentrizität

**Gekippte Vase:**
1. Basis-Vase erstellen (siehe oben)
2. **Enable Eccentricity**: True
3. **Eccentric Point**: 2.5 (leicht über Mitte)
4. **Eccentricity Amount**: 0.3
5. **Eccentricity Angle**: 0.0 (Kippen in +X Richtung)
6. Ergebnis: Asymmetrische, gekippte Vase ↗️

**Verworfene Schale:**
1. **Profile Type**: 6 (Schale)
2. Radien für Schalenform setzen
3. **Enable Eccentricity**: True
4. **Eccentric Point**: 4.0 (oben)
5. **Eccentricity Amount**: 0.5
6. **Eccentricity Angle**: 1.57 (Kippen in +Z)
7. Ergebnis: Schale mit verworfenem Rand

## Workflow-Beispiele

### Beispiel 1: Klassischer Topf
1. **Profile Type**: 4 (Sanduhr)
2. **Height**: 1.0
3. **Base Radius**: 0.4
4. **Radius 1-3**: 0.4, 0.3, 0.4
5. **Top Radius**: 0.4
6. **Bulge**: 0.3
7. Ergebnis: Topf mit leichter Taille

### Beispiel 2: Flasche
1. **Profile Type**: 0 (Zylinder)
2. **Height**: 2.0
3. **Base Radius**: 0.5
4. **Radius 1-2**: 0.5
5. **Radius 3**: 0.2
6. **Top Radius**: 0.15
7. Ergebnis: Flasche mit schmalem Hals

### Beispiel 3: Asymmetrische Skulptur
1. **Profile Type**: 3 (Vase)
2. Basis-Vasenprofil erstellen
3. **Enable Eccentricity**: True
4. **Eccentric Point**: 1.5
5. **Eccentricity Amount**: 0.6
6. **Angle**: 2.0
7. Ergebnis: Abstrakte gekippte Skulptur

## Tipps & Best Practices

### Radius-Kontrolle
- **Glatte Übergänge**: Vermeiden Sie große Sprünge zwischen benachbarten Radien
- **Graduelle Änderungen**: Erstellen Sie glatte, natürliche Profile
- **Experimentieren**: Probieren Sie verschiedene Radius-Kombinationen

### Bulge-Parameter
- Betrifft nur Profiltypen 3, 4, 5, 6
- Starten Sie mit kleinen Werten (0.1-0.3)
- Negative Werte erzeugen inverse Effekte

### Exzentrizität
- **Deaktivieren wenn nicht benötigt**: Amount auf 0.0 setzen oder Enable abwählen
- **Subtil starten**: Beginnen Sie mit Amount 0.2-0.3
- **Glatte Punkt-Kontrolle**: Nutzen Sie Dezimalwerte (z.B. 2.5, 3.75)
- **Angle**: Denken Sie daran TAU = 2π ≈ 6.28 für volle Rotation

### Geschlossene Abschlüsse
- Beide oben und unten sind mit flachen kreisförmigen Abschlüssen versiegelt
- Abschlüsse nutzen den jeweiligen Radius (Basis/Oben) bei dieser Höhe
- Erstellt komplette, solide Objekte

## Fehlerbehebung

**Form erscheint nicht?**
- Prüfen Sie, dass alle Radien > 0.0 sind
- Verifizieren Sie, dass Height vernünftig ist
- Prüfen Sie Position-Offset

**Sichtbare Grate/Stufen?**
- Glätten Sie Radius-Übergänge zwischen Punkten
- Vermeiden Sie extreme Sprünge

**Exzentrizität zu extrem?**
- Reduzieren Sie Amount-Wert
- Prüfen Sie Eccentric Point Platzierung

**Möchten offene Oberseite?**
- Nutzen Sie stattdessen **Body Vasus of Colab** (oben offen, unten geschlossen)

**Benötigen mehr Kontrollpunkte?**
- Nutzen Sie **Body of Revolution** (Vollversion) mit 9 Radiuspunkten

## Vergleich mit anderen Nodes

| Feature | Body Vasus of Colab | Body of Revolution - easy | Body of Revolution |
|---------|---------------------|---------------------------|-------------------|
| Radiuspunkte | 2 (Basis, Oben) | 5 (Basis, R1-R3, Oben) | 9 (Basis, R1-R7, Oben) |
| Exzentrizität | Nein | Ja (1 Punkt) | Ja (2 Punkte) |
| Oberer Abschluss | Offen | Geschlossen | Geschlossen |
| Unterer Abschluss | Geschlossen | Geschlossen | Geschlossen |
| Komplexität | Anfänger | Einfach/Fortgeschritten | Erweitert |

## Credits

- Idee und Projektkoordination: bennoH
- Programmierung: claude.ai (Sonnet-4.5 Modell, Anthropic PBC)
- Lizenz: GPLv3.0 by bennoH, 2026

---

*Für weitere Informationen zum Schreiben und Verwenden von Coollab-Nodes besuchen Sie: https://coollab-art.com/Tutorials/Writing%20Nodes/Intro*
