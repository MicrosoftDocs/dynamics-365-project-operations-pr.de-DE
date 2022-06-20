---
title: Tatsächliche Transaktionen
description: Dieser Artikel informiert Sie darüber, wie Sie in Microsoft Dynamics 365 Project Operations mit Istwerten arbeiten können.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924797"
---
# <a name="actuals"></a>Tatsächliche Transaktionen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die tatsächlichen Werte repräsentieren den überprüften und genehmigten finanziellen und geplanten Fortschritt eines Projekts. Sie werden erstellt, wenn Zeit-, Ausgaben- und Materialnutzungsbuchungen, Journalbuchungen und Rechnungen genehmigt werden.

> [!IMPORTANT]
> Ist-Werte sollten nicht bearbeitet oder aus dem System gelöscht werden. Andernfalls könnten die finanzielle Integrität und jegliche Integration mit anderen Finanz- und Buchhaltungssystemen beeinträchtigt werden. Mit Microsoft Dynamics 365 Project Operations können Sie Ist-Werte stornieren und ersetzen, um Ist-Werte an verschiedenen Punkten im Geschäftsprozess-Lebenszyklus Ihrer Projekte zu bearbeiten.

## <a name="recording-actuals-based-on-project-events"></a>Erfassen von Ist-Werten basierend auf Projektereignissen

Project Operations zeichnet die Finanztransaktionen, die während des Lebenszyklus eines Projektengagements auftreten, als Ist-Werte auf. Die Erstellung von Ist-Werten zu verschiedenen Zeitpunkten im Lebenszyklus variiert, je nachdem, ob das Projektengagement das Zeit- und Materialabrechnungsmodell oder das Festpreisabrechnungsmodell verwendet und ob es sich in der Vorverkaufsphase oder um ein internes Projekt handelt.

Die folgenden Artikel erläutern die Auswirkungen auf die Tabelle „Actuals“ bei verschiedenen Ereignissen für unterschiedliche Varianten:

- [Die Auswirkungen von Ist-Werten bei einer Zeit- und Materialbindung](ActualsonTM.md)
- [Auswirkung der Ist-Werte bei einem Festpreisengagement](ActualonFP.md)
- [Auswirkung der Ist-Werte während der Presales-Phase eines Engagements](ActualonPreSales.md)
- [Auswirkung der Ist-Werte bei einem internen Projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
