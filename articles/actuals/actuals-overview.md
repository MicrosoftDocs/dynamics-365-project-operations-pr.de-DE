---
title: Tatsächliche Transaktionen
description: Dieses Thema enthält Informationen zum Arbeiten mit Istwerten in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581283"
---
# <a name="actuals"></a>Tatsächliche Transaktionen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die tatsächlichen Werte repräsentieren den überprüften und genehmigten finanziellen und geplanten Fortschritt eines Projekts. Sie werden erstellt, wenn Zeit-, Ausgaben- und Materialnutzungsbuchungen, Journalbuchungen und Rechnungen genehmigt werden.

> [!IMPORTANT]
> Ist-Werte sollten nicht bearbeitet oder aus dem System gelöscht werden. Andernfalls könnten die finanzielle Integrität und jegliche Integration mit anderen Finanz- und Buchhaltungssystemen beeinträchtigt werden. Mit Microsoft Dynamics 365 Project Operations können Sie Ist-Werte stornieren und ersetzen, um Ist-Werte an verschiedenen Punkten im Geschäftsprozess-Lebenszyklus Ihrer Projekte zu bearbeiten.

## <a name="recording-actuals-based-on-project-events"></a>Erfassen von Ist-Werten basierend auf Projektereignissen

Project Operations zeichnet die Finanztransaktionen, die während des Lebenszyklus eines Projektengagements auftreten, als Ist-Werte auf. Die Erstellung von Ist-Werten zu verschiedenen Zeitpunkten im Lebenszyklus variiert, je nachdem, ob das Projektengagement das Zeit- und Materialabrechnungsmodell oder das Festpreisabrechnungsmodell verwendet und ob es sich in der Vorverkaufsphase oder um ein internes Projekt handelt.

Die folgenden Themen erläutern die Auswirkungen auf die Ist-Tabelle bei verschiedenen Ereignissen für verschiedene Variationen:

- [Die Auswirkungen von Ist-Werten bei einer Zeit- und Materialbindung](ActualsonTM.md)
- [Auswirkung der Ist-Werte bei einem Festpreisengagement](ActualonFP.md)
- [Auswirkung der Ist-Werte während der Presales-Phase eines Engagements](ActualonPreSales.md)
- [Auswirkung der Ist-Werte bei einem internen Projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
