---
layout: post
title: "Unsere Automatische Schraubstation (ASS):"
subtitle: "Von der Praxis zur Open-Source-Forschung"
date: 2025-04-12 23:45:13 -0400
background:
---

Ein Kernstück unseres INNO-SCREW Projekts ist eine echte industrielle Schraubstation, mit der wir bereits über 34.000 Verschraubungen aufgenommen haben. Diese Daten sind als Open-Source-Dataset auf Zenodo verfügbar und bilden die Grundlage für verschiedene Forschungsarbeiten.

## Der Weg von der Serie zur Forschung

Was unsere Schraubstation besonders macht: Sie stammt direkt aus der Serienfertigung. Ursprünglich wurde sie eingesetzt, um zwei Kunststoffgehäuseteile einer Motorsteuerung für elektrisch betriebene Kinderwagen zu verschrauben. Das heißt, wir arbeiten nicht mit Laborbedingungen, sondern mit echten industriellen Herausforderungen.

Die Station besteht aus einem kompakten Steuer- und Leistungssystem, einem Förderband für die Zuführung und Entnahme der Bauteile, dem Schraubwerkzeug selbst und einem Hubschienenförderer, der die Schrauben zum Werkzeug transportiert. Bevor der erste Verschraubvorgang beginnt, wird jedes Bauteil über einen Datamatrix-Code (DMC) identifiziert.

## Hardware im Detail

### Das Schraubwerkzeug
Unser Schraubwerkzeug stammt von der Rexroth Bosch Group und lässt sich modular für verschiedene Anwendungen zusammenstellen. Unsere Konfiguration umfasst:

- **CS351S-D Kompaktsystem** für Steuerung und elektrische Leistungsaufnahme
- **EC302 Servomotor** für präzise Bewegungen
- **2DMC006 Messumformer** – das Herzstück für unsere Datenerfassung, er zeichnet Drehmoment, Drehwinkel und Gradienten auf
- **2GE26 Planetengetriebe** für die richtige Übersetzung
- **2GB82F73 SZ2 Geradeabtrieb** – modifiziert mit Vakuumaufnahme für die Schrauben

Das besondere Detail: Der Geradeabtrieb wurde speziell angepasst, damit die Schrauben über Vakuum aufgenommen werden können. Das Schraubwerkzeug ist auf drei Linearachsen positionierbar, was eine flexible Anfahrt verschiedener Verschraubpositionen ermöglicht.

### Schraubenzuführung und Logistik
Die Schrauben (Delta PT 40x12 von EJOT) werden über einen DEPRAG Hubschienenförderer Typ 01811-EP/1.5 zugeführt. Dieser ist mit einem Ablaufsteuerungsgerät und einem PFC18L Controller (Schutzart IP30) ausgestattet. Eine Schwenkbewegung der Hubschiene bringt die Schrauben aus dem Vorratsbehälter in die richtige Position. Von der Zuführschiene werden die Schrauben einzeln durch ein Vakuumrohr zum Schraubwerkzeug gefördert.

### Der Arbeitsablauf
Der Prozess läuft vollautomatisch ab: Ein Werkstückträger transportiert das zu verschraubende Bauteil über das Förderband zur Schraubstation. Der DMC-Scanner erkennt das Bauteil, der Werkstückträger wird über Positionierungsbolzen fixiert und mittels Hubeinheit vertikal unter die Schraubspindel positioniert. Während des Verschraubvorgangs sorgt der Werkstückträger dafür, dass das Bauteil nicht verdreht – ein wichtiger Punkt für gleichbleibende Messbedingungen.

## Software und Datenerfassung

Die BS351 Software von Bosch Rexroth ermöglicht es, Schraubprogramme zu erstellen und auf das System zu laden. Wir können beliebig viele Schritte definieren, in denen jeweils die Kurvenauflösung, Zielfunktion und Zielwerte festgelegt werden. Zusätzlich lassen sich Überwachungsfunktionen, Geschwindigkeit, Anlaufsperren, Drehmomentschwellen und maximale Zeitvorgaben definieren.

Für unsere Forschung besonders relevant: Das System erfasst kontinuierlich Drehmoment, Drehwinkel und Gradienten mit Zeitstempeln. Diese Zeitreihendaten werden zusammen mit der Werkstückidentifikation in JSON-Dateien gespeichert – perfekt für unsere Machine Learning-Anwendungen.

## Daten für die Forschung

Mit unserer ASS haben wir bereits über 34.000 Verschraubungen unter kontrollierten experimentellen Bedingungen dokumentiert. Die Daten sind vollständig Open Source und auf Zenodo verfügbar.
Die sechs Datasets decken unterschiedliche Aspekte der industriellen Schraubtechnik ab: von der natürlichen Degradation von Gewinden über Variationen in Oberflächenbedingungen und Materialeigenschaften bis hin zu systematischen Prozessparameteränderungen, Werkzeugverschleiß und umfassenden Multi-Class-Fehlererkennungsszenarien. Jedes Dataset wurde speziell entwickelt, um verschiedene Herausforderungen und Anomalien zu erfassen, die in der industriellen Praxis auftreten können.

## PyScrew: Unser Python-Paket für die Forschung

PyScrew: Unser Python-Paket für die Forschung
PyScrew ist ein Python-Paket, das den Zugang zu industriellen Forschungsdaten aus Schraubexperimenten vereinfacht und eine benutzerfreundliche Schnittstelle zum Herunterladen, Validieren und Aufbereiten von auf Zenodo gehosteten experimentellen Datensätzen bietet. Das Paket ermöglicht es anderen Forschern, schnell in die Analyse einzusteigen, ohne sich erst durch komplexe Datenstrukturen arbeiten zu müssen.

Für weitere Informationen zu den Anwendungen der Daten schau dir unsere Veröffentlichungen an.

## Warum das wichtig ist

Die Kombination aus echter industrieller Hardware, umfangreichen Open-Source-Daten und benutzerfreundlichen Tools wie PyScrew schafft eine einzigartige Forschungsplattform. Andere können unsere Arbeit reproduzieren, ihre eigenen Ansätze testen und faire Vergleiche analytischer Methoden durchführen.
Wir tragen einen öffentlichen Datensatz mit gelabelten Schraubvorgängen bei, der verschiedene Fehlertypen abdeckt, ein mehrstufiges Analyse-Framework zur Bewertung von Fehlererkennungsfähigkeiten und empirische Belege für unterschiedliche Erkennbarkeit verschiedener Fehlerkategorien.
Das ist besonders wichtig in einem Bereich wie der industriellen Automatisierung, wo reproduzierbare Forschung oft schwierig ist, weil die Daten proprietär sind oder die Versuchsaufbauten nicht öffentlich zugänglich. Deswegen werden die Datensätze in INNO-SCREW mit weiteren Schraubanlagen ergänzt, um die Vielfalt der verfügbaren Forschungsdaten zu erweitern und verschiedene industrielle Szenarien abzudecken.

**Interesse an unseren Daten oder PyScrew? Die Daten sind frei verfügbar auf Zenodo, das PyScrew-Paket findet ihr auf GitHub. Wir freuen uns über Feedback und sind gespannt auf eure Forschungsarbeiten mit unseren Daten! Meldet euch gern bei uns.**