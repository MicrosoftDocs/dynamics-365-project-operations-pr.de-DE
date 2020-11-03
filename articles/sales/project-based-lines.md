---
title: Projektbasierte Verkaufschancenpositionen
description: Dieses Thema bietet Informationen zur Arbeit mit projektbasierten Verkaufschancenpositionen.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076385"
---
# <a name="project-based-opportunity-lines"></a>Projektbasierte Verkaufschancenpositionen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Projektbasierte Verkaufschancenpositionen sind nur in projektbasierten Verkaufschancen verfügbar. Bei projektbasierten Verkaufschancendatensätze wird der Feldwert **Typ** auf **Arbeitsbasiert** festgelegt.

Projektbasierte Verkaufschancenpositionen sind die Positionen, die dem Kunden über ein Projekt bereitgestellt werden. Ein Projekt kann jedoch nicht an eine projektbasierte Verkaufschancenposition gebunden werden. Projekte können mit Positionen ab der Phase des **Angebots** verknüpft werden, da die Verkaufschance in der Regel in einer frühen Phase des Geschäfts auftritt. Die Festlegung, wie viele Projekte verwendet werden, um die Arbeit für den Kunden bereitzustellen, ist eine Entscheidung, die später in der Verkaufsphase getroffen wird. Nutzen Sie die Phase der Verkaufschance, um die einzelnen Bereitstellungskomponenten für den Kunden zu identifizieren. Die Entscheidungen bezüglich der tatsächlichen Anzahl der Projekte, die zur Bereitstellung dieser Komponenten verwendet werden, können verschoben werden, bis weitere Informationen über die Arbeit selbst bekannt sind.

Nachfolgend sind die Felder in einer projektbasierten Verkaufschancenposition aufgeführt:

| **Feld** | **Ort** | **Relevanz, Zweck und Anleitung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Produkttyp | Registerkarte „Allgemein“ (ausgeblendet) | Dies ist ein Optionssatzfeld. Wenn Sie Dynamics 365 Operations installiert haben, steht Ihnen als eine der verfügbaren Optionen **Projektbasierter Service** zur Verfügung.  | Der Wert dieses Feldes wird auf **Projektbasierter Service** festgelegt, wenn Sie die projektbasierte Verkaufschancenposition aus dem projektbasierten Positionsraster in der Verkaufschance erstellen. <br> Wenn Sie diesen Wert ändern oder überschreiben, wird die Projektfunktionalität für Ihre projektbasierten Positionen nicht aktiviert. |
| Verkaufschance | Registerkarte „Allgemein“ | Dieses Feld ist schreibgeschützt und verweist auf den übergeordneten Verkaufschancendatensatz, zu dem diese Position gehört. | Es gibt keine nachgelagerten Auswirkungen von diesem Feld. |
| Name des Dataflows | Registerkarte „Allgemein“ | Dies ist ein bearbeitbares Textfeld, mit dem dieser Position eine kurze Identität zugewiesen werden kann. | Dieser Wert wird in die Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Kundenbudget | Registerkarte „Allgemein“ | Dieses bearbeitbare Währungsfeld kann verwendet werden, um den Betrag zu verfolgen, den der Kunde bereit ist, für diese Position auszugeben. | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Fakturierungsmethode | Registerkarte „Allgemein“ | Dieses bearbeitbare Feld weist die folgenden Werte auf:</br>- Zeit und Material</br>- Festpreis | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. Nachdem die Angebotsposition erstellt wurde, ist das Feld gesperrt und kann nicht geändert werden. Weisen Sie diesen Feldwert so genau wie möglich zu. Wenn Sie den Wert dieses Felds in der Angebotsposition ändern müssen, löschen Sie die Angebotsposition und erstellen Sie sie neu. |
