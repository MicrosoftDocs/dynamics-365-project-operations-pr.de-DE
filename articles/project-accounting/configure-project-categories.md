---
title: Projektkategorien konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Projektkategorien.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287507"
---
# <a name="configure-project-categories"></a>Projektkategorien konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Project Operations bietet robuste Funktionen zum Kategorisieren von Einnahmen und Ausgaben für Projekte. Kategorien bieten die Möglichkeit, über Projekttransaktionen zu berichten und diese zu analysieren und die Buchung in das Hauptbuch zu steuern.

Das folgende Diagramm zeigt die Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien. 

Transaktionskategorien sind die grundlegende Gruppierung für Projekttransaktionen. Innerhalb dieser Gruppierung gibt es eine Reihe von gemeinsam genutzten Kategorien, die von Anwendungen und Modulen gemeinsam genutzt werden können. Projektkategorien sind die detailliertesten Kategorien. So wird es noch spezifischer. Projektkategorien sind spezifisch für juristische Personen, Module und Anwendungen.

![Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien](media/project-categories.png)

## <a name="transaction-categories"></a>Transaktionskategorien

Transaktionskategorien stellen die grundlegende Gruppierung für Projekttransaktionen dar und sind nicht unternehmens- oder transaktionsartspezifisch. Beispielsweise verwendet Contoso Robotics die Kategorien Design, Travel, Installation und Service Transaction, um Projekttransaktionen zu gruppieren.

Transaktionskategorien werden im Project Operations-Modul definiert. 
1. Wechseln Sie zu **Einstellungen** \> **Transaktionskategorien**, um das Formular zu öffnen. 
2. Erstellen Sie eine neue Transaktionskategorie, indem Sie entweder **Neu** oder **Aus Excel importieren** auswählen.

## <a name="shared-categories"></a>Gemeinsame Kategorien

Dynamics 365 verwendet das Konzept der gemeinsam genutzten Kategorien, um Ausgaben in verschiedenen Anwendungen, wie beispielsweise Dynamics 365 Finance, Dynamics 365 Supply Chain und Dynamics 365 Project Operations, zu kategorisieren. Für jede erstellte Transaktionskategorie erstellt Project Operations automatisch vier verwandte gemeinsame Kategorien: Stunden, Kosten, Gebühren und Artikel. Sie können die gemeinsamen Kategorien überprüfen und anpassen, indem Sie zu **Projektmanagement und Buchhaltung** \> **Einrichten** \> **Kategorien** \> **Gemeinsame Kategorien** wechseln.

## <a name="project-categories"></a>Projektkategorien

Projektkategorien stellen die detaillierteste Ebene der Kategoriekonfiguration dar und müssen von einem Projektbuchhalter separat und für jedes Unternehmen konfiguriert werden.

1. Wechseln Sie zu **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Projektkategorien**.
2. Wählen Sie **Neu**.
3. Wählen Sie die **Kategorie-ID** der gemeinsamen Kategorie aus, die Sie im vorherigen Abschnitt erstellt haben. Mit Project Operations können nur die gemeinsame Kategorien verwendet werden, die Transaktionskategorien zugeordnet sind.
4. Wählen Sie eine Kategoriegruppe aus.

## <a name="category-groups"></a>Kategoriegruppen

Kategoriegruppen werden verwendet, um Eigenschaften, hauptsächlich Buchungsprofile, zwischen verwandten Projektkategorien freizugeben. Für jeden Transaktionstyp muss mindestens eine Kategoriegruppe vorhanden sein, und jeder Projektkategorie ist eine Gruppe zugeordnet.

Die Buchungsspezifikationen in Project Operations werden durch die Projektkosten- und Ertragsprofilregeln, Projektkategorien sowie Kategoriegruppen definiert. Sie können Kategoriegruppen unter **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Kategoriegruppen** einrichten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]