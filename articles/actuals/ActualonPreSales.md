---
title: Auswirkung der Ist-Werte während der Presales-Phase eines Engagements
description: Dieses Thema enthält Informationen über die Auswirkungen auf die Ist-Wert-Tabelle bei verschiedenen Ereignissen während eine Bindung in Microsoft Dynamics 365 Project Operations im Presales-Phase ist.
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
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577235"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Auswirkung der Ist-Werte während der Presales-Phase eines Engagements

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die folgende Tabelle listet die Ist-Werte verschiedener Transaktionstypen auf, die bei verschiedenen Ereignissen während der Presales-Phase einer Projektbindung erstellt werden.

| Veranstaltung | Kosten-Istwert | Beispiel |
|---|---|---|
| Zeit wird erstellt. | Nicht zutreffend | <p>Bob Kozack von der Organisationseinheit Fabrikam US, die einen Kostensatz von 100 US-Dollar (100 USD) pro Stunde hat, arbeitet an einem Projekt mit dem Namen „Arm-Installation at Adatum“. Dieses Projekt wird einer Festpreisabrechnungsmethode in der Vertragsposition zugeordnet. Hier ist ein Beispielzeiteintrag von Bob Kozak:</p><p>Bob Kozack - 8 Stunden</p> |
| Zeit wird eingereicht. | Nicht zutreffend | Für den Zeiteintrag wird eine Kostenerfassungszeile erstellt. Der Standardkostensatz wird in den Erfassungseintrag eingegeben. |
| Der Zeiteintrag wird vor der Bestätigung abgerufen. | Nicht zutreffend | |
| Zeit wird genehmigt. | Es wird ein Kosten-Ist-Wert erstellt. | <p>Neuer Ist-Wert, die erstellt wird:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul> |
| Die Zeitgenehmigung wird storniert. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |
| Der Zeiteintrag wird nach der Bestätigung abgerufen. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |
| Das Angebot wird gewonnen und ein Vertrag wird erstellt. | <p>Der Regulierungsstatus der alten Kosten-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Kosten-Ist-Werte einer Stornierung werden erstellt, die einen Regulierungsstatus von **Nicht regulierbar** haben.</p><p>Neue Kosten-Ist-Werte werden erstellt, nachdem die Vertragsregeln neu bewertet wurden.</p> | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul><p>Neue Ist-Werte, die für die neu bewerteten finanziellen Auswirkungen erstellt werden, wenn das Angebot gewonnen und der Vertrag erstellt wird:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
