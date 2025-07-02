# CreativeTechnologyMinor - DJ SET "mami tereza"
Doku der Arbeit für Creative Technology von Dario Luciano Giger und Nora-Lee Rüttimann


# Vlog
https://youtu.be/b5U8JOe641s

# mami tereza – live DJ set mit visuals

## Projektbeschreibung

Im Rahmen des Minors **Creative Technology** haben wir zum ersten Mal mit **TouchDesigner** gearbeitet. Das Tool hat uns direkt fasziniert – besonders die Idee, visuelle Designs zu erstellen, die live auf Musik reagieren. Schnell war klar: Wir wollen ein audioreaktives Visual-Set gestalten.

Zusammen mit der DJane unseres Vertrauens, **mami tereza**, haben wir ein DJ-Set geplant, aufgenommen und mit interaktiven Visuals ergänzt. Gemeinsam wurde eine passende Trackliste zusammengestellt, und parallel dazu entwickelten wir visuelle Elemente, die in Echtzeit auf die Musik reagieren.

## Tools & Ressourcen

- [TouchDesigner](https://derivative.ca/)
- [Audacity](https://www.audacityteam.org/)
- YouTube-Tutorials von:
  - [Elekktronaut](https://www.youtube.com/@elekktronaut)
  - [pppanik](https://www.youtube.com/@pppanik)
- Unterstützung durch:
  - **ChatGPT** für technische Hilfe und Debugging

## Einarbeitung & Lernprozess

Da es seitens der Hochschule keine strukturierte Einführung oder kontinuierliche Betreuung gab, waren wir gezwungen, uns die nötigen Kenntnisse eigenständig anzueignen. Das stellte insbesondere zu Beginn eine große Herausforderung dar – zumal uns generell nur sehr wenig Zeit zur Verfügung stand und ein hohes Maß an Eigeninitiative gefordert war.

Die Grundlagen von TouchDesigner konnten wir uns dank zahlreicher YouTube-Tutorials, Online-Foren und ChatGPT schrittweise gut erarbeiten. Deutlich anspruchsvoller war hingegen die technische Umsetzung unserer Ideen, insbesondere ohne Vorerfahrung und ohne die Möglichkeit, regelmäßig auf fachliche Unterstützung zurückzugreifen.

Auch wenn wir den eigenverantwortlichen Lernprozess als bereichernd erlebt haben, hätten wir uns punktuell mehr inhaltliche Begleitung gewünscht. Eine fundierte Einführung und gezielter Support hätten den Einstieg erleichtert und uns geholfen, schneller zu kreativeren und technisch ausgereifteren Ergebnissen zu gelangen.

## Umsetzung & Technische Herausforderungen

Die Verknüpfung der Visuals mit Audio-Daten stellte sich als wesentlich komplexer heraus als erwartet. Die Konzeption der Visuals war kreativ spannend, aber die Umsetzung der Reaktion auf Audiofrequenzen – insbesondere durch Snare- und Kick-Detection – erforderte viel technisches Verständnis und Feintuning.

Ursprünglich wollten wir das Set mit CDJs und einem Mixer aufnehmen. Allerdings ließ sich dieses Audio-Setup nicht wie geplant gleichzeitig mit **Audacity** und **TouchDesigner** verbinden. Daher sind wir kurzfristig auf einen **Controller** umgestiegen. Zwar ließ sich der Sound so problemlos aufnehmen, doch die Reaktivität der Visuals auf die Musik war dadurch leider eingeschränkt. Die direkte Verbindung zwischen Audio-Input und Visuals hat unter der technischen Limitierung gelitten.

## Ergebnis

Vorort kümmerte sich Dario Giger um die Videoaufnahmen, während Nora Rütimann Setdesign, Visuals und Projektion übernahm. Das Ergebnis ist ein stimmiges audiovisuelles Set, bei dem Bild und Ton auf ästhetische Weise miteinander verschmelzen – auch wenn es technisch nicht durchgehend so reaktiv wurde wie ursprünglich geplant.

## Fazit

Das Projekt war aufwendig, aber extrem lehrreich. Wir haben unsere Fähigkeiten in der kreativen Arbeit mit Echtzeit-Visuals deutlich erweitert und gelernt, mit neuen Tools, unerwarteten Problemen und limitierten Ressourcen umzugehen. Besonders im Bereich der visuellen Gestaltung konnten wir unsere Stärken einsetzen und weiterentwickeln.

TouchDesigner hat uns gezeigt, wie viel kreatives Potenzial in der Verbindung von Klang und Bild steckt – und wir sind motiviert, diesen Weg weiterzuverfolgen. Trotz aller Stolpersteine sind wir mit dem Resultat sehr zufrieden und stolz auf das, was wir eigenständig auf die Beine gestellt haben.

---

## 📝 Schritt-für-Schritt-Dokumentation

### 1. 🎵 Vorbereitung des Audio-Inputs

- Wir haben zu Beginn ein fixes Audiofile verwendet, um unser Setup zu testen.
- Während des Live-Sets sind wir dann auf ein externes Audio-Device umgestiegen.

![1](https://github.com/user-attachments/assets/e430f880-a935-454b-9e7d-76c245e06005)

---

### 2. 🔍 Analyse der Audiodaten

Wir haben drei Hauptbereiche zur Analyse des Audiosignals eingerichtet:

- **Kick-Detection**: zur Erkennung der Bassdrums (hohe Pegel).
- **Snare-Detection**: zur Erkennung mittlerer Frequenzimpulse.
- **Speed-Detection**: zur Messung der Geschwindigkeit (Tempo) des Tracks.

#### Aufbau:

- Jeder dieser Bereiche war als eigener Ordner bzw. Subnetz im Node-Netzwerk organisiert.
- Über `In`-Nodes haben wir Daten aus dem übergeordneten Node-Baum eingebunden.
- Die Ergebnisse wurden mit `Out`-Nodes zurück ins Hauptnetzwerk geführt.

![2](https://github.com/user-attachments/assets/908beaef-1d76-4387-85dd-07a36ece78bc)

---

### 3. 🎚 Visuelle Steuerung über Cues

- Wir haben `Cues` definiert, um visuelle Abläufe synchron zur Musik zu steuern.
- Beispiel: Die Bewegung von Ballerinas war an den Beat bzw. die Musikgeschwindigkeit gekoppelt.

![3](https://github.com/user-attachments/assets/40426221-b4ec-499d-bd28-92148d89a193)

---

### 4. 🌀 Umsetzung der Visuals

- Insgesamt haben wir sechs verschiedene Visuals umgesetzt.
- Für dynamische Farb- und Bewegungseffekte haben wir intensiv mit **Noise**-Patterns und **Loops** gearbeitet.

![4](https://github.com/user-attachments/assets/e4a027e5-2c86-41d4-af13-9a500ef3541a)


---

### 5. 🍩 Beispielvisual: Donut mit Text

- Wir haben einen `SOP - Torus` (Donut) als zentrales 3D-Objekt verwendet.
- Darauf wurde ein Textobjekt (z. B. „Mami Tereza“) platziert.
- Licht, Kamera und Animationen wurden integriert und durch Audiosignale gesteuert.

![5](https://github.com/user-attachments/assets/ba10db3f-3a43-4e02-a7e6-710dfc8be0ae)

