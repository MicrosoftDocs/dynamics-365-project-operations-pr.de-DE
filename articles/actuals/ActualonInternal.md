---
title: Ist-Werte wirken sich auf ein internes Projekt aus
description: Dieses Thema liefert Informationen über die Auswirkungen auf die Ist-Werte-Tabelle bei verschiedenen Ereignissen für ein internes Projekt in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579765"
---
# <a name="actuals-impact-for-an-internal-project"></a>Ist-Werte wirken sich auf ein internes Projekt aus

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die folgende Tabelle listet die Ist-Werte verschiedener Transaktionstypen auf, die bei verschiedenen Ereignissen in einer einer internen Projektbindung erstellt werden.

| Veranstaltung | Kosten-Istwert | Beispiel |
|---|---|---|
| Zeit wird erstellt. | Nicht zutreffend | <p>Bob Kozack von der Organisationseinheit Fabrikam US, die einen Kostensatz von 100 US-Dollar (100 USD) pro Stunde hat, arbeitet an einem Projekt mit dem Namen „Arm-Installation at Adatum“. Dieses Projekt wird einer Festpreisabrechnungsmethode in der Vertragsposition zugeordnet. Hier ist ein Beispielzeiteintrag von Bob Kozak:</p><p>Bob Kozack - 8 Stunden</p> |
| Zeit wird eingereicht. | Nicht zutreffend | Für den Zeiteintrag wird eine Kostenerfassungszeile erstellt. Der Standardkostensatz wird in den Erfassungseintrag eingegeben. |
| Der Zeiteintrag wird vor der Bestätigung abgerufen. | Nicht zutreffend | |
| Zeit wird genehmigt. | Es wird ein Kosten-Ist-Wert erstellt. | <p>Neuer Ist-Wert, die erstellt wird:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul> |
| Die Zeitgenehmigung wird storniert. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |
| Der Zeiteintrag wird nach der Bestätigung abgerufen. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
