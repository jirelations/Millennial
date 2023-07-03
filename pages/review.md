---
layout: page
title: Review
permalink: /review
---

## Arbeitsverfahren für digitale Forschungsprojekte

| **Schokoladen-herstellungsmodell** | **Allgemeines Arbeitsverfahren** | **Beispiele** |
| -- | -- | -- |
| ? Forschungsfrage | Anpassung von Jeder Schritt an die Forschungsfrage | -- |
| <i class="fa-solid fa-seedling"></i> 1. Pick | Sammlung von Daten | Social-Media-Posts durch Kopieren/Scraping; Handschriften, Bücher, Archivmaterialien durch Digitalisierung; Interviews mit Aufzeichnungen bzw. Notizen; Feldnotizen |
| <i class="fa-solid fa-gears"></i> 2. Prepare | Strukturierung bzw. Formatierung von Daten | Reinigung und Standardisierung; Organisieren in Datenbanken bzw. Tabellen; Texterkennung von Bilddateien |
| <i class="fa-solid fa-fire-burner"></i> 3. Process | Analyse | Textanalyse, z.B. Tagging von sprachlichen oder historischen Merkmalen, Sentiment-Analyse; Bildanalyse, z.B. Farben, Objekte; Kodierung von Notizen; quantitative Analyse von Tags/Kodierung |
| <i class="fa-solid fa-gift"></i> 4. Package | Darstellung von Forschungs-ergebnissen | narrative Erzählungen; (dynamische) Graphen, Karten, Zeitleisten, Netzwerken; erweiterter Text mit Links bzw. dynamischen Funktionen |

### Zu Ihrem Projekt 

| **Schokoladen-herstellungsmodell** | **Zu Ihrem Projekt** |
| -- | -- | -- |
| ? Forschungsfrage | Was ist Ihre Forschungsfrage? |
| <i class="fa-solid fa-seedling"></i> 1. Pick | Warum passen Ihre Daten zu dieser Forschungsfrage? |
| <i class="fa-solid fa-gears"></i> 2. Prepare | Mit welchen Prozessen und Werkzeugen mussten Sie Ihre Daten vorbereiten, um sie analysieren zu können?  |
| <i class="fa-solid fa-fire-burner"></i> 3. Process | a. Wie antwortet Ihre Analyse auf die Forschungsfrage? b. Welche Hindernisse mussten Sie dabei umgehen? |
| <i class="fa-solid fa-gift"></i> 4. Package | a. Warum haben Sie sich für diese Darstellungsform entschieden? b. Welche Lücken oder Anomalien sollen dabei beachtet werden? |

## FAIR Forschungsdaten

| FAIR | Description | ✅ Good | ❌ Bad |
| -- | -- | -- | -- |
| Findable | unique identifiers, metadata, in a searchable resource | items in data have stable URIs, metadata is submitted to libraries and visible to search engines | links are temporary, metadata is only available to subscribers |
| Accessible | data can be accessed using a standard system on the basis of identifiers | open-access, URIs/identifiers go to web pages | subscription only, identifiers are only for internal use |
| Interoperable | data is in a format that can be used by common systems and is linked to other datasets | open-source formats that can be used by a variety of programs (e.g., text, XML) | closed-source formats that can only be used in one program (e.g., Word, Photoshop) |
| Re-usable | data is licensed for re-use, source is known, meets community standards | CC-BY or other open license | copyright unclear or exclusive to publisher |


## 1.-2. Sitzung

- Lernziel: Begin critically questioning the origins, scope, and biases of data sets.
- Inhalte vs. Formate: Was ist der Unterschied?
- Beispiele geben: "born-digital" Formate, analoge Formate
- Warum ist es wichtig, die Entstehungsgeschichten von bestimmten Daten zu verstehen, bevor Sie sie verwenden? Welche Aspekte könnten dabei wichtig sein?

## 3.-6. Sitzung

- Lernziele: 
  - Grasp the basics of storing your data in a transparent way (note the "FAIR" acronym).
  - Practice cleaning and formatting data using a variety of tools.
- s. FAIR Forschungsdaten oben
- Was ist Git? Wie kann Git mit Forschungsdaten helfen?

## 7.-10. Sitzung

- Lernziele:
  - Practice cleaning and formatting data using a variety of tools. (Fortsetzung)
  - Explore some ways to enrich your data with markup.
  - Practice applying a research question to text and visual data using off-the-shelf tools.
  - ~~Practice applying a research question to quantitative and network data.~~ (nicht gemacht)
- Beispiele geben: Was kann bei der Datenverarbeitung bzw. -formatierung problematisch sein? Was sind mögliche Lösungen dafür?
  - Tabellen
  - Textdateien
  - Bilddateien
- Was sind **Metadaten**? Was für Details beinhalten sie typischerweise? 
- Beispiele geben: Was sind mögliche Ansätze für die **Analyse** von 
  - Texten?
  - Bildern?
- Beispiele geben: Was sind Darstellungs- bzw. Visualisierungsmöglichkeiten für die 
  - Textanalyse? 
  - Bildanalyse?
  - geographische Analyse?
- **Websites:** Welche Möglichkeiten haben Sie, wenn Sie Ihr Forschungsprojekt auf eine Website publizieren wollen? Welche Nachhaltigkeitsfragen sind dabei zu beachten?

| Plattform | Einfach? | Nachhaltig? | Anpassbar? |
| -- | -- | -- | -- |
| Analyse- bzw. Visualisierungsplattform verwenden (z.B. Google Sheets, Voyant Tools, Recogito) | ★★★ <br /> (nichts zu installieren) | ★ <br />(Zukunft der Plattform nicht garantiert) | ★ |
| Standard Content Management System (CMS, z.B. WordPress) auf Uni- bzw. auf eigenem Server | ★★ <br />(vorinstalliert, muss noch konfiguriert werden) | <br />★★ (Standardsoftware wird leichter und auf länger aktualisiert) | ★★ <br />(relativ anpassbar) |
| HTML-Seiten auf Uni- bzw. auf eigenem Server | ★★ <br />(wenig zu installieren) | ★★★ (wartungsfreundlich, wenig Aktualisierungen notwendig) | ★★ <br />(individuell anpassbar aber keine dynamische Datenbank-Funktionen) |
| Individuelle Software auf Uni- bzw. auf eigenem Server | ★ <br />(Installation durch Expert:Innen) | ★ <br />(Wartungsarbeiten bzw. Aktualisierungen und deswegen teuer) | ★★★ <br />(alles ist möglich) |