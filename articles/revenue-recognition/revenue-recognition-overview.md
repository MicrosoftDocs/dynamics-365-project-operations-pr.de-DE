---
title: Umsatzrealisierungsübersicht
description: Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531428"
---
# <a name="revenue-recognition-overview"></a>Umsatzrealisierungsübersicht

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In Dynamics 365 Project Operations variieren die Grundsätze für die Umsatzrealisierung je nach ausgewählter Abrechnungsmethode für ein Projekt oder einen Teil des Projekts. Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Zugeordnete Transaktionen mit Zeit- und Materialabrechnungsmethode

- Kosten- und Ertragsrealisierung sind miteinander verbunden. Transaktionskosten und nicht abgerechnete Verkäufe werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht.
- Das Projektkosten- und Ertragsprofil bestimmt, ob nicht in Rechnung gestellte Verkaufstransaktionen in das Hauptbuch gebucht werden. Wenn **Einnahmen erzielen** ausgewählt ist, verwendet das System den **WIP-Verkaufswert** und die **Aufgelaufene Umsatzerlös**-Konten während der Buchung. Nachfolgend ist ein Beispiel für diese Methode aufgeführt.  

  | Transaktionstyp | Soll/Haben | Betrag |
  | --- | --- | --- |
  | WIP-Verkaufswert | Belastung | 100 |
  | Antizipierter Umsatzerlös - Verkaufswert | Gutschrift | 100 |

- Der Umsatz wird bei Rechnungsstellung erfasst. Das System verwendet das **Abgerechnete Einnahmen**-Konto während der Buchung. Nachfolgend ist ein Beispiel für diese Methode aufgeführt.  

  | Transaktionstyp | Soll/Haben | Betrag |
  | --- | --- | --- |
  | Kundenguthaben | Belastung | 120 |
  | Zu zahlende Mehrwertsteuer | Gutschrift | 20 |
  | Rechnungsumsatz | Gutschrift | 100 |

- Wenn bei der Buchung der nicht in Rechnung gestellten Verkäufe Umsatzerlöse angefallen sind, storniert das System die aufgelaufenen Umsatzerlöse bei Rechnungsstellung.

  | Transaktionstyp | Soll/Haben | Betrag |
  | --- | --- | --- |
  | WIP-Verkaufswert | Gutschrift | 100 |
  | Antizipierter Umsatzerlös - Verkaufswert | Belastung | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Zugeordnete Transaktionen mit Festpreisabrechnungsmethode

- Kosten- und Ertragsrealisierung sind separat. Transaktionskosten werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht. Nicht in Rechnung gestellte Verkaufstransaktionen werden nicht erstellt.
- Umsatzerlöse können während der Rechnungsstellung erfasst werden, wenn für das Projektkosten- und Umsatzprofil **Prinzip für Projektabschlussberechnungen** auf **Kein WIP** eingestellt ist. Verwenden Sie diese Methode nur für kurzfristige, einfache Projekte.
- Umsatzerlöse können anhand von Festpreisschätzungen mit den Mthoden **Vertrag abgeschlossen** oder **Umsatzrealisierung in Prozent** erfasst werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Artikel „Buchhaltung für fakturierbare Projekte konfigurieren“](../project-accounting/configure-accounting-billable-projects.md)

[Projektvorkalkulation (Festpreis) des Umsatzes](rev-rec-percentage-completion-method.md)

[Umsatzschätzungen verwalten](rev-rec-completed-contract-method.md)

[Methoden für die Kosten zur Fertigstellung](cost-complete-methods.md)
