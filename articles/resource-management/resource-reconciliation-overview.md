---
title: Ressourcenabstimmung – Übersicht
description: Diese Thema enthält Informationen, um sicherzustellen, dass Ressourcenbuchungen und Arbeitsaufträge zu Projekten abgestimmt sind.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125717"
---
# <a name="resource-reconciliation-overview"></a>Ressourcenabstimmung – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Teammitglieder werden für Buchungen und Zuweisungen lose verbunden. Das bedeutet, Ressourcen können Zuweisungen haben, jedoch keine Buchungen, oder sie können Buchungen, jedoch keine Zuweisungen haben. Idealerweise sollten Buchungen und Zuweisungen angepasst werden, sodass die Ressourcen ihre Kapazität für die Aufgabenzuordnungen festgelegt haben. Unter Umständen basieren die Buchungen auf der Verfügbarkeit, und die Aufgabenzeitplanung wird im Laufe des Projekts geändert. Daher bietet die lose Verbindung von Buchungen und Zuweisungen Flexibilität.

Mit der Registerkarte **Abstimmung** auf dem Formular **Projekt** können Projektmanager Buchungen und Zuweisungen der Teammitglieder für die Projektteams abstimmen.

Auf der Registerkarte **Abstimmung** werden auch Buchungen und Zuweisungen bis zu Ebene der einzelnen Aufgabenzuordnungen für jedes Teammitglied angezeigt. Stunden werden in Zellen angezeigt, was für Zeitperioden von Monaten bis Tagen stehen kann.

Auf der Registerkarte wird auch die allgemeine Nettosumme für das Projekt zusammen mit einer der Spalte **Total** angezeigt.

Für jede Ressource berechnet die Registerkarte den Unterschied zwischen den Buchungen des Teammitglieds und einem Rollup der Aufgabenzuordnungen des Teammitglieds. Idealerweise sollte der Unterschied 0 (null) sein. Das bedeutet, dass es keinen Unterschied zwischen Buchungen und Zuweisungen geben sollte. Die Unterschiede werden farbig und schattiert angezeigt, um auf zwei Bedingungen hinzuweisen:

- **Verlust der Buchung** – Ein Buchungsverlust tritt auf, wenn eine Ressource mehr Zuweisungen als Buchungen hat. Da diese Kapazität nicht reserviert wurde, kann ein Projektmanager diesen Zustand korrigieren, indem er die Ressourcenbuchungen erweitert, um das Defizit abzudecken.
- **Überzählige Buchungen** – Überzählige Buchungen treten auf, wenn eine Ressource für das Projekt zwar gebucht, aber keinen Aufgaben zugewiesen wurde. Dieser Zustand kann akzeptabel sein, wenn die Ressource im Projekt gebucht wurde, bevor die Aufgabenzuordnung erfolgt ist. In anderen Fällen wird die Ressource jedoch nicht eingeplant, um Aufgaben zugewiesen zu werden. In diesen Fällen sollte es der Projektmanager in Betracht ziehen, die Buchungen der Ressource zu stornieren, sodass die Kapazität für ein anderes Projekt verwendet werden kann.

Wenn Sie die Zeit in einigen Fällen auf einer höheren als der Tagsebene (z. B. auf Monatsebene) anzeigen, sehen Sie einen Nettounterschied von null für eine Ressource (d. h.: Buchungen =Zuweisungen). Wenn Sie die Zeit jedoch auf Wochenebene anzeigen, sehen Sie, dass es Zuweisungen mit null Stunden und Buchungen mit 40 Stunden in der ersten Woche gibt, aber Zuweisungen von 40 Stunden und Buchungen von null Stunden in der zweiten Woche. Die Buchungen und Zuweisungen werden insgesamt abgestimmt, sie unterscheiden sich jedoch von einer Woche zur nächsten.

Wenn Sie Zeit auf höheren Ebenen anzeigen, haben die Zellen auf der Registerkarte **Abstimmung** einen Indikator, um Sie darüber zu informieren, dass es Unterschiede auf tieferen Ebenen gibt. Wenn Sie in einer Zelle doppelklicken, können Sie die Ansicht vergrößern, um die Unterschiede anzuzeigen. Sie können dann mit der rechten Maustaste klicken, um die Ansicht wieder zu verkleinern. Sie können eine Ressource auswählen und dann mithilfe des **Nächster Unterschied**-Steuerelements auf der Rastersymbolleiste zu den folgenden Unterschieden zwischen Buchungen und Zuweisungen für die Ressource wechseln. Das Steuerelement **Vorheriger Unterschied** navigiert zurück. Sie können den Unterschiedindikator und das Navigationsverhalten unter **Einstellungen** deaktivieren.


Wenn Sie Aufgabenzuordnungen für eine Ressource, jedoch keine Buchungen haben, wählen Sie auf der **Projekte**-Seite, auf der Registerkarte **Abstimmung** den Buchungsverlust aus, und wählen Sie dann **Buchung erweitern** aus. Das Dialogfeld **Buchung erweitern** wird mit der Buchung angezeigt, die benötigt wird, um einen Ressourcenmangel zu beheben. Es enthält außerdem die vorhandenen Buchungen der Ressource in allen Projekten oder anderen planbaren Entitäten. Wenn Sie **OK** auswählen, um die Buchung für die Ressource zu erstellen, entsteht ungeachtet der Verfügbarkeit der Ressource möglicherweise eine Überbuchung.

Der Projektmanager oder der Ressourcenmanager kann dann die Zeitplanübersicht verwenden, um alle Situationen zu verwalten, in denen eine Ressource über die Kapazität überbucht wird.

