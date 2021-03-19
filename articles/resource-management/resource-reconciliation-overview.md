---
title: Ressourcenabstimmung – Übersicht
description: Dieses Thema enthält Informationen, mit denen Sie sicherstellen können, dass Ressourcenbuchungen und Zuweisungen für Projekte aufeinander abgestimmt sind.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0416e93944e7b6686a0e4da1d633188dd51e590b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279362"
---
# <a name="resource-reconciliation-overview"></a>Ressourcenabstimmung – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Teammitglieder werden für Buchungen und Zuweisungen lose verbunden. Das bedeutet, Ressourcen können Zuweisungen haben, jedoch keine Buchungen, oder sie können Buchungen, aber keine Zuweisungen haben. Idealerweise sollten Buchungen und Zuweisungen angepasst werden, sodass die Ressourcen ihre Kapazität für die Aufgabenzuordnungen festgelegt haben. Unter Umständen basieren die Buchungen auf der Verfügbarkeit, und die Aufgabenzeitplanung wird im Laufe des Projekts geändert. Daher bietet die lose Verbindung von Buchungen und Zuweisungen Flexibilität.

Die Registerkarte **Abstimmung** auf der Seite **Projekte** ermöglicht es den Projektmanagern, die Buchungen und Zuweisungen der Teammitglieder für die Projektteams abzustimmen.

Auf der Registerkarte **Abstimmung** werden Buchungen und Zuweisungen bis zu Ebene der einzelnen Aufgabenzuordnungen für jedes Teammitglied angezeigt. Stunden werden in Zellen angezeigt, die für Zeitperioden von Monaten bis Tagen stehen können. Auf der Registerkarte wird auch die allgemeine Nettosumme für das Projekt zusammen mit einer der Spalte **Total** angezeigt.

Für jede Ressource berechnet die Registerkarte **Abstimmung** den Unterschied zwischen den Buchungen des Teammitglieds und einem Rollup der Aufgabenzuordnungen des Teammitglieds. Idealerweise sollte der Unterschied 0 (null) sein. Das bedeutet, dass es keinen Unterschied zwischen Buchungen und Zuweisungen geben sollte. Die Unterschiede werden farbig und schattiert angezeigt, um auf zwei Bedingungen hinzuweisen:

- **Verlust der Buchung** – Ein Buchungsverlust tritt auf, wenn eine Ressource mehr Zuweisungen als Buchungen hat. Da die Kapazität nicht reserviert wurde, kann ein Projektmanager diesen Zustand korrigieren, indem er die Ressourcenbuchungen erweitert, um das Defizit abzudecken.
- **Überzählige Buchungen** – Überzählige Buchungen treten auf, wenn eine Ressource für das Projekt zwar gebucht, aber keinen Aufgaben zugewiesen wurde. Dieser Zustand kann akzeptabel sein, wenn die Ressource im Projekt gebucht wurde, bevor die Aufgabenzuordnung erfolgt ist. In anderen Fällen, in denen nicht geplant ist, der Ressource Aufgaben zuzuweisen, sollte der Projektmanager in Betracht ziehen, die Buchungen der Ressource zu stornieren. Auf diese Weise kann die Kapazität für ein anderes Projekt verwendet werden.

Wenn Sie die Zeit in einigen Fällen auf einer höheren als der Tagsebene (z. B. auf Monatsebene) anzeigen, sehen Sie einen Nettounterschied von null für eine Ressource (d. h.: Buchungen entsprechen Zuweisungen). Wenn Sie die Zeit jedoch auf Wochenebene anzeigen, sehen Sie, dass es Zuweisungen mit null Stunden und Buchungen mit 40 Stunden in der ersten Woche gibt, aber Zuweisungen von 40 Stunden und Buchungen von null Stunden in der zweiten Woche. Die Buchungen und Zuweisungen werden insgesamt abgestimmt, sie unterscheiden sich jedoch von einer Woche zur nächsten.

Wenn Sie Zeit auf höheren Ebenen anzeigen, haben die Zellen auf der Registerkarte **Abstimmung** einen Indikator, um Sie darüber zu informieren, dass es Unterschiede auf tieferen Ebenen gibt. Wenn Sie in einer Zelle doppelklicken, können Sie die Ansicht vergrößern, um so die Unterschiede anzuzeigen. Wählen und halten Sie (oder mit rechten Maustaste klicken), um die Ansicht wieder zu verkleinern. Sie können eine Ressource auswählen und dann mithilfe des **Nächster Unterschied**-Steuerelements auf der Rastersymbolleiste zu den folgenden Unterschieden zwischen Buchungen und Zuweisungen für die Ressource wechseln. Das Steuerelement **Vorheriger Unterschied** navigiert zurück. Sie können den Unterschiedindikator und das Navigationsverhalten unter **Einstellungen** deaktivieren.

Wenn Sie Aufgabenzuordnungen für eine Ressource, jedoch keine Buchungen haben, wählen Sie auf der **Projekte**-Seite, auf der Registerkarte **Abstimmung** den Buchungsverlust aus, und wählen Sie **Buchung erweitern** aus. Das Dialogfeld **Buchung erweitern** zeigt die Buchung an, die benötigt wird, um einen Ressourcenmangel zu beheben. Das Dialogfeld enthält außerdem die vorhandenen Buchungen der Ressource in allen Projekten oder anderen planbaren Entitäten. Wenn Sie **OK** auswählen, um die Buchung für die Ressource zu erstellen, entsteht ungeachtet der Verfügbarkeit der Ressource möglicherweise eine Überbuchung.

Buchungen, die über die Aktionen **Buchung verlängern** erstellt werden sind mit der primären Projektanforderung verbunden. Wenn eine Erweiterung initiiert wird, kann die spezifische Anforderung, die erweitert werden muss, nicht bestimmt werden, da die Ressource möglicherweise mehr als einer Anforderung für das Projekt zugeordnet ist.

Der Projektmanager oder der Ressourcenmanager kann dann die Zeitplanansicht verwenden, um alle Situationen zu verwalten, in denen eine Ressource über die Kapazität überbucht wird.


[!INCLUDE[footer-include](../includes/footer-banner.md)]