---
title: Projektkategorien konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Projektkategorien.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995170"
---
# <a name="configure-project-categories"></a>Projektkategorien konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Project Operations bietet robuste Funktionen zum Kategorisieren von Einnahmen und Ausgaben für Projekte. Kategorien bieten die Möglichkeit, Projekttransaktionen zu melden und zu analysieren und die Buchung in die Finanzbuchhaltung zu steuern.

Das folgende Diagramm zeigt die Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien. 

Transaktionskategorien sind die grundlegende Gruppierung für Projekttransaktionen. Innerhalb dieser Gruppierung gibt es eine Reihe von geteilten Kategorien, die von Anwendungen und Modulen gemeinsam genutzt werden können. Tiefer in die Details gehend, sind Projektkategorien die detailliertesten Kategorien. Projektkategorien sind spezifisch für juristische Personen, Module und Anwendungen.

![Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien](media/project-categories.png)

## <a name="transaction-categories"></a>Transaktionskategorien

Transaktionskategorien stellen die grundlegende Gruppierung für Projekttransaktionen dar und sind nicht unternehmens- oder transaktionsartspezifisch. Beispielsweise verwendet Contoso Robotics die Kategorien Design, Reise, Installation und Service-Transaktion, um Projekttransaktionen zu gruppieren.

Transaktionskategorien werden im Project Operations-Modul definiert. 
1. Wechseln Sie zu **Einstellungen** \> **Transaktionskategorien**, um das Formular zu öffnen. 
2. Erstellen Sie eine neue Transaktionskategorie, indem Sie entweder **Neu** oder **Aus Excel importieren** auswählen.

## <a name="shared-categories"></a>Gemeinsam genutzte Kategorien

Dynamics 365 verwendet das Konzept der gemeinsam genutzten Kategorien, um Ausgaben in verschiedenen Anwendungen, wie beispielsweise Dynamics 365 Finance, Dynamics 365 Supply Chain und Dynamics 365 Project Operations, zu kategorisieren. Für jede erstellte Transaktionskategorie erstellt Project Operations automatisch vier verwandte gemeinsame Kategorien: Stunden, Kosten, Gebühren und Artikel. Sie können die gemeinsamen Kategorien überprüfen und anpassen, indem Sie zu **Projektmanagement und Buchhaltung** \> **Einrichten** \> **Kategorien** \> **Gemeinsame Kategorien** wechseln.

## <a name="project-categories"></a>Projektkategorien

Projektkategorien stellen die detaillierteste Ebene der Kategoriekonfiguration dar und müssen von einem Projektbuchhalter separat und für jedes Unternehmen konfiguriert werden.

1. Wechseln Sie zu **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Projektkategorien**.
2. Wählen Sie **Neu**.
3. Wählen Sie die **Kategorie-ID** der gemeinsamen Kategorie aus, die Sie im vorherigen Abschnitt erstellt haben. Mit Project Operations können nur die gemeinsam genutzten Kategorien verwendet werden, die Transaktionskategorien zugeordnet sind.
4. Wählen Sie eine Kategoriegruppe aus.

## <a name="category-groups"></a>Kategoriegruppen

Kategoriegruppen werden verwendet, um Eigenschaften, hauptsächlich Buchungsprofile, für verwandte Projektkategorien freizugeben. Für jeden Transaktionstyp muss mindestens eine Kategoriegruppe vorhanden sein, und jeder Projektkategorie ist eine Gruppe zugeordnet.

Die Buchungsspezifikationen in Project Operations werden durch die Projektkosten- und Ertragsprofilregeln, Projektkategorien sowie Kategoriegruppen definiert. Sie können Kategoriegruppen unter **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Kategoriegruppen** einrichten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]