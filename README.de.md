# 🦷 CAD_CAM – 3D Zahn-Visualisierung

[English](README.md) | **Deutsch**

Browserbasiertes Werkzeug zur **Darstellung und Vermessung von 3D-Zahnmodellen** (STL/PLY).
Die Anwendung läuft direkt im Browser über GitHub Pages – ohne Installation.

**Live-Anwendung:** https://digitaleaesthetischezahnmedizin.github.io/CAD_CAM/

---

## Inhaltsverzeichnis

- [Zweck](#zweck)
- [Funktionen](#funktionen)
- [Verzeichnisstruktur](#verzeichnisstruktur)
- [Kurzanleitung: Messung durchführen](#kurzanleitung-messung-durchführen)
- [Verwendete Bibliotheken / Lizenzhinweise](#verwendete-bibliotheken--lizenzhinweise)
- [Lizenz](#lizenz)
- [Hinweise & Haftungsausschluss](#hinweise--haftungsausschluss)

> 📖 Die vollständige Bedienungsanleitung mit Screenshots findet sich in **[`doc/README.md`](doc/README.md)**.

---

## Zweck

Das Programm dient der **objektiven Visualisierung und Vermessung** von Veränderungen an Zähnen
anhand digitaler 3D-Scans aus unterschiedlichen Behandlungsphasen (z. B. vor und nach einer
Präparation sowie mit eingesetzten Restaurationen).

Es wird im Rahmen eines **selbständigen Beweisverfahrens** (§§ 485 ff. ZPO) genutzt, das einen
**behaupteten bzw. strittigen** Veneer-Behandlungsfehler bei einem Zahnarzt in Heilbronn (Deutschland) zum
Gegenstand hat. Strittig ist dabei unter anderem, ob die Versorgung als Veneers oder als Teilkronen
einzuordnen ist. Die Anwendung dient ausschließlich der technischen Veranschaulichung des
streitgegenständlichen Sachverhalts.

> **Hinweis:** Es handelt sich um eine Parteidokumentation zur Veranschaulichung. Die
> abschließende fachliche und rechtliche Bewertung obliegt allein dem gerichtlich bestellten
> Sachverständigen und dem Gericht. Mit dieser Darstellung ist **keine** abschließende oder
> verbindliche Feststellung eines Behandlungsfehlers verbunden.

---

## Funktionen

- **Modelle laden** – STL/PLY per Weblink oder lokaler Datei; optionale Textur (JPG) für PLY-Modelle.
- **Anzeige-Einstellungen** – Skalierung, FOV, Hintergrundfarbe, Gitter, Kameraposition (X/Y/Z).
- **Abweichungs-Heatmap** – signierte Farbskala (±4 mm) zum Vergleich von Referenz- und Zielmodell.
- **Toleranzbänder** – einstellbarer Grünbereich, Gelb/Rot- und Hellblau/Dunkelblau-Bereich, Maximalgrenzwert.
- **Maus-Messung (Pins)** – Punkt-zu-Fläche-Abstände mit einstellbarer Punktgröße.
- **Iterative Hochpräzisions-Messung** („Sonne/Fächer") – Strahlen pro Stufe, Iterationen, Sichtlinien-Prüfung zum Überspringen von Lücken.
- **2D-Schnittvermessung** – Clipping-Plane zur exakten Kantenmessung im Querschnitt.
- Mehrsprachig sowie Hell-/Dunkelmodus.

---

## Verzeichnisstruktur

| Datei / Ordner | Inhalt |
| --- | --- |
| `index.html` | Die vollständige Web-Anwendung (3D-Viewer & Vermessung). |
| `STL/` | Die für den Vergleich verwendeten 3D-Modelle. |
| `doc/` | Bedienungsanleitung mit nummerierten Screenshots (siehe unten). |

📖 **Dokumentation:** Eine ausführliche Bedienungsanleitung (Englisch) findet sich in **[`doc/README.md`](doc/README.md)**.

---

## Kurzanleitung: Messung durchführen

Folgende Schritte sind nötig, um eine Abstandsmessung zwischen zwei Modellen durchzuführen:

1. Webseite öffnen.
2. Warten, bis alle Modelle geladen sind (Status unten in der Seitenleiste).
3. Im Bereich „Geladene Modelle": Ein Modell als „Referenz" und ein anderes als „Ziel" festlegen.
4. Im Bereich „STL/PLY Vergleich": Auf „Messung vorbereiten" klicken.
5. „Maus-Messung (Pins)" aktivieren – beim Überfahren des Zielmodells werden nun Abstände angezeigt.
6. Durch Klick auf das Modell Messpunkte (Pins) setzen.
7. Optional: „Heatmap anzeigen" aktivieren für eine flächendeckende Abweichungsdarstellung.
8. Optional: Abschnitt-Vermessung nutzen für exakte 2D-Schnittmessungen.

**Tastenkombinationen**

- **ESC** – Maus-Messung und Schnittebenen-Zeichnen deaktivieren
- **Mausrad** – Zoom
- **Linke Maustaste + Ziehen** – Modell drehen
- **Rechte Maustaste + Ziehen** – Modell verschieben

---

## Verwendete Bibliotheken / Lizenzhinweise

Die folgenden Open-Source-Bibliotheken werden zur Laufzeit über das jsDelivr-CDN geladen
(sie sind **nicht** in diesem Repository enthalten) und unterliegen ihren eigenen Lizenzen:

- **three.js** (v0.172.0) – MIT-Lizenz – © three.js authors – https://github.com/mrdoob/three.js
  (einschließlich der Module `OrbitControls`, `STLLoader`, `PLYLoader`)
- **three-mesh-bvh** (v0.9.8) – MIT-Lizenz – © Garrett Johnson – https://github.com/gkjohnson/three-mesh-bvh
- **Schriftarten** *DM Sans* und *JetBrains Mono* (SIL Open Font License) – geladen über Google Fonts

---

## Lizenz

Der **eigene Code und die eigenen Inhalte** dieses Repositories stehen unter der
**Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.
Den vollständigen Lizenztext findest du in der Datei [`LICENSE`](LICENSE).

Das bedeutet: Die Anwendung darf bei Namensnennung weitergegeben werden, jedoch
**nicht verändert** und **nicht kommerziell genutzt** werden.
Lizenztext: https://creativecommons.org/licenses/by-nc-nd/4.0/deed.de

> Diese Lizenz gilt nur für den eigenen Code dieses Projekts. Die oben genannten
> Bibliotheken (three.js, three-mesh-bvh) verbleiben unter ihrer jeweiligen MIT-Lizenz.

---

## Hinweise & Haftungsausschluss

- Reines **Visualisierungs- und Messwerkzeug** – **kein Medizinprodukt**, keine Diagnose und keine Behandlungsempfehlung.
- Mess- und Heatmap-Ergebnisse hängen von Qualität, Auflösung und Ausrichtung (Registrierung) der Eingangsdaten ab.
