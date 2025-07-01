# CreativeTechnologyMinor - DJ SET "mami tereza"
Doku der Arbeit für Creative Technology von Dario Luciano Giger und Nora-Lee Rüttimann

# mami tereza – live DJ set mit visuals

## Projektbeschreibung

Im Rahmen des Minors **Creative Technology** haben wir zum ersten Mal mit **TouchDesigner** gearbeitet. Das Tool hat uns direkt fasziniert – besonders die Idee, visuelle Designs zu erstellen, die live auf Musik reagieren. Schnell war klar: Wir wollen ein audioreaktives Visual-Set gestalten.

Zusammen mit der DJane unseres Vertrauens, **mami tereza**, haben wir ein DJ-Set geplant, aufgenommen und mit interaktiven Visuals ergänzt. Gemeinsam wurde eine passende Trackliste zusammengestellt, und parallel dazu entwickelten wir visuelle Elemente, die in Echtzeit auf die Musik reagieren.

## Tools & Ressourcen

- [TouchDesigner](https://derivative.ca/)
- [Audacity](https://www.audacityteam.org/)
- [YouTube-Tutorials](https://www.youtube.com):
  - von **elekktronaut**
- Unterstützung durch:
  - **ChatGPT** für technische Hilfe und Debugging

## Einarbeitung & Lernprozess

Da es kaum strukturierte Einführung oder Betreuung seitens der Hochschule gab, mussten wir uns praktisch alles selbst beibringen. Der Lernprozess war dementsprechend langwierig, aber auch sehr intensiv. Mit Geduld, YouTube-Tutorials, Foren und ChatGPT konnten wir uns Schritt für Schritt in TouchDesigner einarbeiten. 

Auch wenn wir den eigenständigen Lernprozess grundsätzlich schätzen, empfinden wir die mangelnde Begleitung – wie sie an der **FHGR** leider häufiger vorkommt – als klaren Schwachpunkt. Eine fundierte Einführung hätte vieles erleichtert und uns schneller zu kreativeren Ergebnissen geführt.

## Umsetzung & Technische Herausforderungen

Die Verknüpfung der Visuals mit Audio-Daten stellte sich als wesentlich komplexer heraus als erwartet. Die Konzeption der Visuals war kreativ spannend, aber die Umsetzung der Reaktion auf Audiofrequenzen – insbesondere durch Snare- und Kick-Detection – erforderte viel technisches Verständnis und Feintuning.

Ursprünglich wollten wir das Set mit CDJs und einem Mixer aufnehmen. Allerdings ließ sich dieses Audio-Setup nicht wie geplant gleichzeitig mit **Audacity** und **TouchDesigner** verbinden. Daher sind wir kurzfristig auf einen **Controller** umgestiegen. Zwar ließ sich der Sound so problemlos aufnehmen, doch die Reaktivität der Visuals auf die Musik war dadurch leider eingeschränkt. Die direkte Verbindung zwischen Audio-Input und Visuals hat unter der technischen Limitierung gelitten.

## Ergebnis

Vorort kümmerte sich Dario Giger um die Videoaufnahmen, während Nora Rütimann Setdesign, Visuals und Projektion übernahm. Das Ergebnis ist ein stimmiges audiovisuelles Set, bei dem Bild und Ton auf ästhetische Weise miteinander verschmelzen – auch wenn es technisch nicht durchgehend so reaktiv wurde wie ursprünglich geplant.

## Fazit

Das Projekt war aufwendig, aber extrem lehrreich. Wir haben unsere Fähigkeiten in der kreativen Arbeit mit Echtzeit-Visuals deutlich erweitert und gelernt, mit neuen Tools, unerwarteten Problemen und limitierten Ressourcen umzugehen. Besonders im Bereich der visuellen Gestaltung konnten wir unsere Stärken einsetzen und weiterentwickeln.

TouchDesigner hat uns gezeigt, wie viel kreatives Potenzial in der Verbindung von Klang und Bild steckt – und wir sind motiviert, diesen Weg weiterzuverfolgen. Trotz aller Stolpersteine sind wir mit dem Resultat sehr zufrieden und stolz auf das, was wir eigenständig auf die Beine gestellt haben.

# 🎧 Audio-Visualisierung mit Blender – Projektdokumentation (Art Installation)

In diesem Projekt haben wir untersucht, wie Audio-Input in Blender genutzt werden kann, um visuelle Effekte in Echtzeit für eine Art-Installation zu steuern. Die Installation basiert auf synchronisierten 3D-Visuals, die auf musikalische Elemente reagieren.

## 🔧 Voraussetzungen

- Blender (mit aktiviertem Python-Scripting)
- Ein Audiofile oder ein externes Audio-Device
- Grundkenntnisse in Node-basiertem Arbeiten (Geometry Nodes, Shader Nodes etc.)

---

## 📝 Schritt-für-Schritt-Dokumentation

### 1. 🎵 Vorbereitung des Audio-Inputs

- Wir haben zu Beginn ein fixes Audiofile verwendet, um unser Setup zu testen.
- Während des Live-Sets sind wir dann auf ein externes Audio-Device umgestiegen.

---

### 2. 🔍 Analyse der Audiodaten

Wir haben drei Hauptbereiche zur Analyse des Audiosignals eingerichtet:

- **Kick-Detection**: zur Erkennung der Bassdrums (hohe Pegel).
- **Snare-Detection**: zur Erkennung mittlerer Frequenzimpulse.
- **Speed-Detection**: zur Messung der Geschwindigkeit (Tempo) des Tracks.

#### Aufbau:

- Jeder dieser Bereiche war als eigener Ordner bzw. Subnetz im Node-Netzwerk organisiert.
- Über `In`-Nodes haben wir Daten aus dem übergeordneten Node-Baum eingebunden.
- Die Analyse erfolgte über `Audio Aspect Analyze Trail`-Methoden.
- Die Ergebnisse wurden mit `Out`-Nodes zurück ins Hauptnetzwerk geführt.

---

### 3. 🎚 Visuelle Steuerung über Cues

- Wir haben `Cues` definiert, um visuelle Abläufe synchron zur Musik zu steuern.
- Beispiel: Die Bewegung von Ballerinas war an den Beat bzw. die Musikgeschwindigkeit gekoppelt.

---

### 4. 🌀 Umsetzung der Visuals

- Insgesamt haben wir sechs verschiedene Visuals umgesetzt.
- Für dynamische Farb- und Bewegungseffekte haben wir intensiv mit **Noise**-Patterns und **Loops** gearbeitet.
- Python-Skripte wurden verwendet, um Noise-Werte dynamisch zu animieren, z. B.:

### 5. 🍩 Beispielvisual: Donut mit Text

- Wir haben einen `Torus` (Donut) als zentrales 3D-Objekt verwendet.
- Darauf wurde ein Textobjekt (z. B. „Mami Teresa“) platziert.
- Über `SOPs` (Surface Operators) haben wir die Geometrie verändert.
- Licht, Kamera und Animationen wurden integriert und durch Audiosignale gesteuert.
- Python-Skripte wurden verwendet, um Noise-Werte dynamisch zu animieren, z. B.:

  ```python
  noise_value = 0.5  # Geringe Bewegungsgeschwindigkeit
