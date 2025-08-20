---
layout: page
title: Roboter-Schraubstation
description: 
background: '/img/bg-contact.jpg'
---

Ein wichtiger Bestandteil unseres Forschungsprojekts **INNO-SCREW** ist eine **roboterbasierte Schraubstation**, die ursprünglich im Projekt **SUPPLy** zur Produkt- und Prozessentwicklung eines automatisierungsgerechten Ladestation-Outlet-Moduls beschafft wurde.  
Heute setzen wir sie ein, um systematisch Verschraubungsdaten aufzunehmen und so eine **skalierbare Datenbasis für die Forschung** zu schaffen.

## Flexible Datenerfassung

Während klassische Schraubstationen oft auf feste Prozessabläufe zugeschnitten sind, erlaubt unsere Roboter-Schraubstation (RSS) durch den Einsatz eines **Cobots** flexible Verschraubungen durchzuführen. Damit können wir reproduzierbare Schraubexperimente in kontrollierter Umgebung durchführen und gleichzeitig große Mengen an Daten generieren, ohne den hohen Aufwand manueller Versuchsreihen.

Die Station besteht aus:

- **HCR-5A Cobot** (Hanwha Robotics) – für die präzise Handhabung und Bewegung
- **OnRobot Schraubmodul** – für die Verschraubung mit regelbarem Drehmoment und Vorschub
- **Schraubenhalterung mit 10×10 Raster** – als Vorrichtung zur Bereitstellung von bis zu 100 Schrauben

## Der Arbeitsablauf

Der Ablauf ist vollständig automatisiert:

1. Der Cobot fährt zur Schraubenhalterung und nimmt eine Schraube auf.  
2. Er positioniert sich am Bauteil und führt den Verschraubvorgang aus.  
3. Anschließend fährt er zurück, nimmt die nächste Schraube auf und wiederholt den Prozess.  
4. Sobald alle Schrauben am Bauteil verarbeitet sind oder der Schraubvorrat leer ist, stoppt die Station, bis ein neues Bauteil oder neue Schrauben bereitgestellt werden.  

Dieser Zyklus ermöglicht eine kontinuierliche Erfassung von einer großen Menge von Schraubdaten.

## Hardware im Detail

Die roboterbasierte Schraubstation besteht aus zwei zentralen Komponenten: dem **HCR-5A Cobot** von Hanwha Robotics und dem **OnRobot Screwdriver Modul**. Zusammen bilden sie eine flexible und zugleich hochpräzise Forschungsplattform für Verschraubungsprozesse.

Der **HCR-5A** ist ein kollaborativer 6-Achsen-Roboterarm mit einer Reichweite von 915 mm und einer maximalen Nutzlast von 5 kg. Er zeichnet sich durch eine Wiederholgenauigkeit von ±0,05 mm aus und ermöglicht lineare Bewegungen mit Geschwindigkeiten von bis zu 1 m/s. Jede Achse kann sich um 360° drehen und liefert dabei kontinuierlich Bewegungsdaten. Dank seiner Schutzklasse IP66 kann der Roboter auch in anspruchsvolleren Umgebungen eingesetzt werden, und integrierte Sicherheitsfunktionen wie virtuelle Begrenzungen, Kollisionsüberwachung und Geschwindigkeitslimits erlauben einen sicheren kollaborativen Betrieb. Über Modbus TCP und EtherCAT kommuniziert er mit der Steuerung und stellt in Echtzeit Daten zur Verfügung, darunter **Positionen, Gelenkwinkel, Geschwindigkeiten, Drehmomente sowie Gelenktemperaturen**.

Das zweite Kernstück ist das **OnRobot Screwdriver Modul**, das speziell für die automatisierte Schraubmontage entwickelt wurde. Es unterstützt Schrauben von M1.6 bis M6 und bis zu 50 mm Länge. Das Modul bietet eine präzise Drehmomentregelung im Bereich von 0,15 Nm bis 5 Nm und kann sowohl Standard- als auch selbstschneidende Schrauben verarbeiten. Besonders praktisch für Versuchsaufbauten: Schrauben bis 35 mm Länge werden vollständig im Schrauber eingezogen, sodass der Transport zwischen Schraubenhalterung und Bauteil sicher und stabil erfolgt. Darüber hinaus erkennt das Modul automatisch, ob Schrauben korrekt aufgenommen wurden, ob sie vollständig eingedreht sind oder ob Prozessabweichungen auftreten. Für die Forschung besonders relevant ist, dass das Schraubmodul kontinuierlich **Drehmoment- und Vorschubdaten** aufzeichnet, die für die Analyse von Schraubstrategien und Anomalien genutzt werden können.

In Kombination ergeben beide Systeme eine hochflexible Plattform: Der Cobot übernimmt die präzise Positionierung und Bewegung, während das Schraubmodul die eigentliche Verschraubung mit variablen Prozessparametern wie Zieldrehmoment, Schraubenlänge und Vorschubkraft steuert. Während der Versuche werden alle Datenströme über Modbus in Echtzeit erfasst und in einer Datenbank gespeichert. So entsteht ein umfassender Datensatz, der sowohl **roboterspezifische Größen** (z. B. Position, Geschwindigkeit, Gelenkdrehmomente, Temperaturen) als auch **prozessspezifische Größen** (z. B. Drehmomentverläufe, Vorschubkraft, Schraubparameter) abdeckt. Diese enge Verzahnung von Hardware und Datenerfassung schafft die Grundlage für systematische Analysen und datengetriebene Forschung im Bereich automatisierter Schraubprozesse.

## Software und Datenerfassung

Die gesamte Datenerfassung der Schraubstation erfolgt in Echtzeit über **Modbus**. Dabei werden die Sensordaten sowohl aus dem Cobot als auch aus dem Schraubmodul kontinuierlich abgefragt und in einer zentralen Datenbank gespeichert.  

Besonders wertvoll sind die dabei entstehenden **hochaufgelösten Zeitreihen**, die während jeder Verschraubung aufgezeichnet werden. Sie umfassen unter anderem Drehmoment- und Vorschubverläufe des Schraubmoduls sowie Positions-, Geschwindigkeits- und Gelenkdrehmomentdaten des Roboters. 

## Warum das wichtig ist

Mit der roboterbasierten Schraubstation verfügen wir über eine **hochflexible Forschungsplattform**, die reproduzierbare Schraubexperimente in variablen Szenarien ermöglicht.  
Im Zusammenspiel mit weiteren Schraubanlagen im Projekt INNO-SCREW entsteht ein vielfältiger **Open-Source-Datenpool**, der es anderen Forschenden erlaubt, eigene Modelle zu entwickeln, zu testen und zu vergleichen.