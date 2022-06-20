---
title: Auswirkung der Ist-Werte bei einem Festpreisengagement
description: Dieser Artikel enthält Informationen über die Auswirkungen auf die Tabelle Actuals bei verschiedenen Ereignissen während des Lebenszyklus eines Festpreisvertrags in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918127"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Auswirkung der Ist-Werte bei einem Festpreisengagement

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die folgende Tabelle listet die Ist-Werte verschiedener Transaktionstypen auf, die bei verschiedenen Ereignissen in einer einer internen Festpreisbindung erstellt werden.

| Veranstaltung | Kosten-Istwert | Nicht fakturierter Umsatz-Istwert | Fakturierter Umsatz-Ist-Wert | Beispiel |
|---|---|---|---|---|
| Zeit wird erstellt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | <p>Bob Kozack von der Organisationseinheit Fabrikam US, die einen Kostensatz von 100 US-Dollar (100 USD) pro Stunde hat, arbeitet an einem Projekt mit dem Namen „Arm-Installation at Adatum“. Dieses Projekt wird einer Festpreisabrechnungsmethode in der Vertragsposition zugeordnet. Hier ist ein Beispielzeiteintrag von Bob Kozak:</p><p>Bob Kozack - 8 Stunden</p> |
| Zeit wird eingereicht. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Für den Zeiteintrag wird eine Kostenerfassungszeile erstellt. Der Standardkostensatz wird in den Erfassungseintrag eingegeben. |
| Der Zeiteintrag wird vor der Bestätigung abgerufen. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | |
| Zeit wird genehmigt. | Es wird ein Kosten-Ist-Wert erstellt. | Nicht zutreffend | Nicht zutreffend | <p>Neuer Ist-Wert, die erstellt wird:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul> |
| Die Zeitgenehmigung wird storniert. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | Nicht zutreffend | Nicht zutreffend | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |
| Der Zeiteintrag wird nach der Bestätigung abgerufen. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | Nicht zutreffend | Nicht zutreffend | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul> |
| Der Vertrag ist bestätigt. | <p>Der Regulierungsstatus der alten Kosten-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Kosten-Ist-Werte einer Stornierung werden erstellt, die einen Regulierungsstatus von **Nicht regulierbar** haben.</p><p>Neue Kosten-Ist-Werte werden erstellt, nachdem die Vertragsregeln neu bewertet wurden.</p> | Nicht zutreffend | Nicht zutreffend | <p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li></ul><p>Neuer Ist-Wert, der für die neubewerteten finanziellen Auswirkungen erstellt wird:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul> |
| Eine Rechnung wird erstellt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | |
| Die Rechnung wird mit einem Meilenstein bestätigt. | Nicht zutreffend | Nicht zutreffend | Neue meilensteinbasierte fakturierte Umsatz-Ist-Werte werden erstellt. | <p>Bestehender Ist-Wert, das unverändert bleibt:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Umsatz-Ist-Wert:** Meilenstein, 5.000 USD</li></ul> |
| Die Rechnung wird korrigiert, um den Meilenstein gutzuschreiben. | Nicht zutreffend | Nicht zutreffend | Zwei stornierte, fakturierte Verkäufe werden erstellt. | <p>Bestehender Ist-Wert, das unverändert bleibt:</p><ul><li>**Kosten-Ist-Wert:** Bob Kozack, 8 Stunden, 800 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Fakturierter Umsatz-Ist-Wert:** Meilenstein, 5.000 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die zuvor fakturierten Verkaufswerte zu stornieren:</p><ul><li>**Fakturierter Umsatz-Ist-Wert:** Meilenstein, 5.000 USD, *Nicht regulierbar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
