---
title: Die Auswirkungen von Ist-Werten bei einer Zeit- und Materialbindung
description: Dieses Thema enthält Informationen über die Auswirkungen auf die Ist-Wert-Tabelle bei verschiedenen Ereignissen während des Lebenszyklus einer Zeit- und-Materialbindung in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: a4ea3f9cf74d8a67447571001b75065b8cde5c00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580823"
---
# <a name="actuals-impact-in-a-time-and-materials-engagement"></a>Die Auswirkungen von Ist-Werten bei einer Zeit- und Materialbindung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die folgende Tabelle listet die Ist-Werte verschiedener Transaktionstypen auf, die bei verschiedenen Ereignissen in einer Zeit- und Materialbindung erstellt werden.

| Veranstaltung | Kosten-Istwert | Nicht fakturierter Umsatz-Istwert | Fakturierter Umsatz-Ist-Wert | Beispiel |
|---|---|---|---|---|
| Zeit wird erstellt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | <p>Bob Kozack von der Organisationseinheit Fabrikam US, die einen Kostensatz von 100 US-Dollar (100 USD) pro Stunde hat, arbeitet an einem Projekt mit dem Namen „Arm-Installation at Adatum“. Für dieses Projekt beträgt sein vertraglich vereinbarter Rechnungssatz 200 USD pro Stunde. Hier ist ein Beispielzeiteintrag von Bob Kozak:</p><p>Bob Kozack, 8 Stunden</p> |
| Zeit wird eingereicht. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | Für den Zeiteintrag werden eine Kostenerfassungsposition und Erfassungen für nicht fakturierte Verkäufe erstellt. Der Standardpreis und der Kostensatz werden in den Journaleintrag eingegeben. |
| Der Zeiteintrag wird vor der Bestätigung abgerufen. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | |
| Zeit ist genehmigt: Eingereichte Stunden entsprechen abrechenbaren Stunden. | Es wird ein Kosten-Ist-Wert erstellt. | Ein nicht fakturierter Verkaufs-Ist-Wert wird erstellt. | Nicht zutreffend | <p>Neue Ist-Werte, die erstellt werden:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD</li></ul> |
| Zeit ist genehmigt: Abrechenbare Stunden werden unter eingereichten Stunden verringert. | Es wird ein Kosten-Ist-Wert erstellt. | <p>Zwei nicht fakturierte Verkäufe werden erstellt:</p><ul><li>Fakturierbarer nicht fakturierter Verkaufs-Ist-Wert für die abrechenbaren Stunden</li><li>Nicht fakturierbarer, nicht fakturierter Verkaufs-Ist-Wert für die verbleibende Menge</li></ul> | Nicht zutreffend | <p>Neue Ist-Werte, die erstellt werden:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 6 Stunden, 1.200 USD, *Fakturierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 2 Stunden, 400 USD, *Nicht fakturierbar*</li></ul> |
| Zeit ist genehmigt: Abrechenbare Stunden werden über eingereichten Stunden erhöht. | Es wird ein Kosten-Ist-Wert erstellt. | Ein nicht fakturierter Verkaufs-Ist-Wert wird erstellt. | Nicht zutreffend | <p>Neue Ist-Werte, die erstellt werden:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 10 Stunden, 2.000 USD</li></ul> |
| Die Zeitgenehmigung wird storniert. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Der Regulierungsstatus der ursprünglichen, nicht fakturierten Verkaufs-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Es wird eine Stornierung eines nicht fakturierten Verkaufs-Ist-Werts erstellt, der einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | Nicht zutreffend | <p>Bestehende Ist-Werte, die aktualisiert werden:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD, *Reguliert*</li></ul><p>Neue Ist-Werte, die erstellt werden, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD, *Nicht regulierbar*</li></ul> |
| Der Zeiteintrag wird nach der Bestätigung abgerufen. | <p>Der Regulierungsstatus der ursprünglichen, Kosten-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Ein Kosten-Ist-Werte einer Stornierung wird erstellt, die einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | <p>Der Regulierungsstatus der ursprünglichen, nicht fakturierten Verkaufs-Ist-Werts wird auf **Reguliert** aktualisiert.</p><p>Es wird eine Stornierung eines nicht fakturierten Verkaufs-Ist-Werts erstellt, der einen Regulierungsstatus von **Nicht regulierbar** hat.</p> | Nicht zutreffend | <p>Bestehende Ist-Werte, die aktualisiert werden:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD, *Reguliert*</li></ul><p>Neue Ist-Werte, die erstellt werden, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD, *Nicht regulierbar*</li></ul> |
| Der Vertrag ist bestätigt. | <p>Der Regulierungsstatus der alten Kosten-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Kosten-Ist-Werte einer Stornierung werden erstellt, die einen Regulierungsstatus von **Nicht regulierbar** haben.</p><p>Neue Kosten-Ist-Werte werden erstellt, nachdem die Vertragsregeln neu bewertet wurden.</p> | <p>Der Regulierungsstatus der alten, nicht fakturierten Verkaufs-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Die Stornierung von nicht fakturierten Verkaufs-Ist-Werten, die einen Regulierungsstatus von **Nicht regulierbar** haben, werden erstellt.</p><p>Neue nicht fakturierte Verkaufs-Ist-Werte werden erstellt, nachdem die Vertragsregeln neu bewertet wurden.</p> | Nicht zutreffend | <p>Bestehende Ist-Werte, die aktualisiert werden:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, 8 Stunden, 800 USD, *Reguliert*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD, *Reguliert*</li></ul><p>Neue Ist-Werte, die erstellt werden, um die vorherigen finanziellen Auswirkungen umzukehren:</p><ul><li>**Kosten-Ist-Wert**: Bob Kozack, (8 h),( 800 USD), *Nicht regulierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD, *Nicht regulierbar*</li></ul><p>Neue Ist-Werte, die für die neubewerteten finanziellen Auswirkungen erstellt werden:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD</li></ul> |
| Eine Rechnung wird erstellt. | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend | |
| Die Rechnung ist bestätigt. Es gibt keine Änderung bei der Menge im Rechnungspositionsdetail gegenüber der Menge bei den nicht fakturierten Verkaufs-Ist-Werten. | Nicht zutreffend | <p>Der Rechnungsstatus des alten nicht fakturierten Verkaufs-Ist-Werts wird aktualisiert.</p><p>Die Stornierung von nicht fakturierten Verkaufs-Ist-Werten, die einen Regulierungsstatus von **Nicht regulierbar** haben, werden erstellt. | Ein fakturierter Verkaufs-Ist-Wert wird erstellt. | <p>Bestehender Ist-Wert, das unverändert bleibt:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Nicht fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 8 h, 1.600 USD, *Kundenrechnung gebucht*</li></ul>Neuer Ist-Wert, der erstellt wird, um die laufende finanzielle Arbeit (WIP) zu stornieren:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 h, 1.600 USD</li></ul> |
| Die Rechnung ist bestätigt, nachdem die Menge im Rechnungspositionsdetail gegenüber der Menge bei den nicht fakturierten Verkaufs-Ist-Werten verringert wird. | Nicht zutreffend | <p>Der Regulierungsstatus der ursprünglichen, nicht fakturierten Verkaufs-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die ursprünglichen, nicht fakturierten Verkaufs-Ist-Werte erstellt. Sie haben einen Regulierungsstatus von **Nicht regulierbar**.</p><p>Zwei neue nicht fakturierte Verkäufe werden erstellt:</p><ul><li>Fakturierbarer nicht fakturierter Verkaufs-Ist-Wert für die abrechenbaren Stunden</li><li>Nicht fakturierbarer, nicht fakturierter Verkaufs-Ist-Wert für die verbleibende Menge</li></ul><p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die beiden neuen, nicht fakturierten Verkaufs-Ist-Werte erstellt.</p> | <p>Zwei fakturierte Verkäufe werden erstellt:</p><ul><li>Fakturierbarer fakturierter Verkaufs-Ist-Wert für die abrechenbaren Stunden</li><li>Nicht fakturierbarer, fakturierter Verkaufs-Ist-Wert für die verbleibende Menge</li></ul> | <p>Bestehender Ist-Wert, das unverändert bleibt:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen WIP umzukehren:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD, *Nicht regulierbar*</li></ul><p>Neue Ist-Werte, die erstellt werden, um den aktualisierten Verkaufs-WIP zu erfassen:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 6 Stunden, 1.200 USD, *Fakturierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 2 Stunden, 400 USD, *Nicht fakturierbar*</li></ul><p>Neue Ist-Werte, die erstellt werden, um den aktualisierten Verkaufs-WIP zu stornieren:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (6 h), (1.200 USD), *Fakturierbar*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (2 h), (400 USD), *Nicht fakturierbar*</li></ul><p>Neue Ist-Werte, die erstellt werden, um die fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 6 h, 1.200 USD, *Fakturierbar*</li><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 2 h, 400 USD, *Nicht fakturierbar*</li></ul> |
| Die Rechnung ist bestätigt, nachdem die Menge im Rechnungspositionsdetail gegenüber der Menge bei den nicht fakturierten Verkaufs-Ist-Werten erhöht wird. | Nicht zutreffend | <p>Der Regulierungsstatus der ursprünglichen, nicht fakturierten Verkaufs-Ist-Werte wird auf **Reguliert** aktualisiert.</p><p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die ursprünglichen, nicht fakturierten Verkaufs-Ist-Werte erstellt. Sie haben einen Regulierungsstatus von **Nicht regulierbar**.</p><p>Neue nicht fakturierter Verkaufs-Ist-Werte werden für die neue Menge erstellt.</p><p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die neuen, nicht fakturierten Verkaufs-Ist-Werte erstellt.</p> | Fakturierter Verkaufs-Ist-Werte werden für die neue Menge erstellt. | <p>Bestehender Ist-Wert, das unverändert bleibt:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 8 Stunden, 1.600 USD, *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die vorherigen finanziellen WIP umzukehren:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD, *Nicht regulierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um den aktualisierten Verkaufs-WIP zu erfassen:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 10 Stunden, 2.000 USD, *Fakturierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um den aktualisierten Verkaufs-WIP zu stornieren:</p><ul><li>**Nicht fakturierter Verkaufs-Ist-Wert**: Bob Kozack, (10 h), (2.000 USD), *Fakturierbar *,* Nicht regulierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 10 h, 2.000 USD, *Fakturierbar*</li></ul> |
| Die Rechnung wird korrigiert, um die fakturierbare Menge oder den Preis zu verringern. | Nicht zutreffend | <p>Zwei nicht fakturierte Verkäufe werden erstellt:</p><ul><li>Fakturierbare, nicht fakturierte Verkäufe für die Menge auf der Korrekturrechnung</li><li>Fakturierbarer, nicht fakturierter Verkaufs-Ist-Wert für die verbleibende Menge</li></ul><p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die beiden neuen, nicht fakturierten Verkaufs-Ist-Werte erstellt.</p> | <p>Zwei stornierte, fakturierte Verkäufe werden erstellt.</p><p>Neue fakturierter Verkaufs-Ist-Werte werden für die neue Menge erstellt. | <p>Bestehende Ist-Werte, die unverändert bleiben:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 8 h, 1.600 USD, *Kundenrechnung gebucht*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Fakturierter Verkafus-Ist-Wert:** Bob Kozack, (8 h), (1.600 USD), *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die zuvor fakturierten Verkaufswerte zu stornieren:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, (8 h), (1.600 USD), *Nicht regulierbar*</li></ul><p>Neue Ist-Werte, die erstellt werden, um den korrigierten Verkaufs-WIP zu erfassen:</p><ul><li>**Nicht fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 6 h, 1.200 USD, *Fakturierbar*, *Kundenrechnung gebucht*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, 2 Stunden, 400 USD, *Fakturierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um den korrigierten Verkaufs-WIP zu stornieren:</p><ul><li>**Nicht fakturierter Verkaufs-Ist-Wert**: Bob Kozack, (6 h), (1.200 USD), *Fakturierbar *,* Nicht regulierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die korrigierten, fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 6 h, 1.200 USD, *Fakturierbar*</li></ul> |
| Die Rechnung wird korrigiert, um die fakturierbare Menge oder den Preis zu erhöhen. | Nicht zutreffend | <p>Neue nicht fakturierter Verkaufs-Ist-Werte werden für die neue Menge erstellt.</p> <p>Nicht fakturierte Verkaufs-Ist-Werte zur Stornierung werden für die neuen, nicht fakturierten Verkaufs-Ist-Werte erstellt.</p> | <p>Zwei stornierte, fakturierte Verkäufe werden erstellt.</p>Neue fakturierter Verkaufs-Ist-Werte werden für die neue Menge erstellt.</p> | <p>Bestehende Ist-Werte, die unverändert bleiben:</p><ul><li>**Kosten-Ist-Werte:** Bob Kozack, 8 Stunden, 800 USD</li><li>**Nicht fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 8 h, 1.600 USD, *Kundenrechnung gebucht*</li><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (8 h), 1.600 USD</li></ul><p>Bestehender Ist-Wert, der aktualisiert wird:</p><ul><li>**Fakturierter Verkafus-Ist-Wert:** Bob Kozack, (8 h), (1.600 USD), *Reguliert*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die zuvor fakturierten Verkaufswerte zu stornieren:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, (8 h), (1.600 USD), *Nicht regulierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um den korrigierten Verkaufs-WIP aufzuzeichnen:</p><ul><li>**Nicht fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 10 h, 2.000 USD, *Fakturierbar*, *Kundenrechnung gebucht*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um den korrigierten Verkaufs-WIP zu stornieren:</p><ul><li>**Nicht fakturierter Umsatz-Ist-Wert:** Bob Kozack, (10 h), (2.000 USD), *Fakturierbar*</li></ul><p>Neuer Ist-Wert, der erstellt wird, um die korrigierten, fakturierten Verkaufswerte zu erfassen:</p><ul><li>**Fakturierter Verkaufs-Ist-Wert:** Bob Kozack, 10 h, 2.000 USD, *Fakturierbar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]