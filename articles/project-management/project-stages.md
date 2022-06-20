---
title: Projektphasen
description: Dieser Artikel informiert Sie über die Projektphasen, die in Project Operations Microsoft Dynamics verfügbar sind.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b146174583fdea45481b87375158ebe83ed63418
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911135"
---
# <a name="project-stages"></a>Projektphasen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektphasen sind so konzipiert, dass sie den Status des Projekts während seines Fortschritts widerspiegeln. Anpassungen können verwendet werden, um die Phasen automatisch mit Geschäftsprozessflüssen, Power Automate oder Plug-In-Erweiterungen zu aktualisieren.

Die folgenden Phasen sind standardmäßig im Geschäftsprozessfluss definiert:

- Neu
- Angebot
- Plan
- Bereitstellen
- Abschließen
- Schließen 

## <a name="new"></a>Neu

Wenn Sie ein Projekt erstellen, wird die Projektphase auf **Neu** festgelegt. Wenn das Projekt anhand einer Vorlage erstellt wurde, verfügt es unter Umständen über einen Zeitplan, Schätzungen und Teamdaten. Andernfalls handelt es sich lediglich um einen Entwurf des Projekts und die restlichen Komponenten müssen eingegeben werden.

## <a name="quote"></a>Angebot

Wenn Sie ein Projekt einem Angebot zuordnen oder aus einem Angebot ein Projekt erstellen, wird die Projektphase auf **Angebot** festgelegt und die geschätzten Start- und Enddaten werden aktualisiert. Während sich das Projekt in der Phase **Angebot** befindet, werden auf der Registerkarte **Vertrieb** auf der Seite **Projektentität** Details zum Angebot angezeigt.

## <a name="plan"></a>Planen

Wenn Sie für ein Angebot den Zuschlag erhalten, das einem Projekt zugeordnet ist, und das Projekt in die Phase **Vertrag** verschoben wird, wird die Projektphase zu **Planen** aktualisiert. Während sich das Projekt in der Phase **Planen** befindet, werden auf der Seite **Projektentität** Details zum Vertrag angezeigt.

## <a name="deliver"></a>Bereitstellen

Wenn der Projektplan vollständig ist und Sie mit dem Projekt beginnen können, sollte der Projektmanager die Projektphase zu **Bereitstellen** aktualisieren, um anzuzeigen, dass das Projekt gestartet wurde.

## <a name="complete"></a>Abschließen 

Wenn die Arbeit für das Projekt abgeschlossen wurde, kann der Projektmanager die Phase zu **Abgeschlossen** aktualisieren. Indem er die Projektphase zu **Abgeschlossen** aktualisiert, zeigt der Projektmanager an, dass die Arbeit zwar vollständig abgeschlossen ist, das Projekt aber offen bleibt, damit alle ausstehenden Zeit- oder Ausgabeneingaben erfasst werden können.

## <a name="close"></a>Schließen

Sobald alle Transaktionen für das Projekt erfasst wurden, kann der Projektmanager die Phase zu **Schließen** aktualisieren. An diesem Punkt können keine Transaktionen mehr erfasst werden und das Projekt ist schreibgeschützt.



[!INCLUDE[footer-include](../includes/footer-banner.md)]