---
title: Header/Zusammenfassung der Verkaufschance
description: Dieses Thema enthält Informationen zu projektbasierten Deals und den projektbasierten Verkaufschancenpositionen.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1344e21d58fbc28198468146f9cea9cf00572d7d
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181226"
---
# <a name="opportunity-settings"></a>Verkaufschancen-Einstellungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Der Header oder die Zusammenfassung der Verkaufschance erfasst die Gesamtinformationen zu einem projektbasierten Geschäft, die für alle Zeilen einer projektbasierten Verkaufschance gelten.

Projektbasierte Verkaufschancen in Dynamics 365 Project Operations sind Erweiterungen von Verkaufschancen in Dynamics 365 Sales. Diese Erweiterungen bieten zusätzliche Funktionen, die für projektbasierte Geschäftschancen spezifisch und für diese erforderlich sind. Diese Erweiterungen können neue Felder und Multifunktionsleistenaktionen enthalten, die in projektbasierten Verkaufschancen verfügbar sind. Möglicherweise finden Sie einige Felder, Funktionen und Standardlogiken, die in Sales verfügbar sind, nicht in Project Operations.

Die folgende Tabelle enthält die Felder in einer projektbasierten Verkaufschance, die entweder nur für Project Operations gelten oder einige wichtige Verhaltensänderungen gegenüber den Verkaufschancen in Sales aufweisen.

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Art | Registerkarte „Allgemein“ (ausgeblendet) | Dieses Optionssatzfeld enthält die folgenden Optionen:</br>- Arbeitsbasiert (nur bei Project Operations verfügbar)</br>- Positionsbasiert (nur verfügbar, wenn Project Operations und Sales installiert sind)</br>- Servicewartungsbasiert (verfügbar, wenn Field Service installiert ist) | Wenn Sie Project Operations verwenden, wird dieser Feldwert automatisch auf **Arbeitsbasiert** festgelegt. Dadurch wird die Verkaufschance als projektbasiert klassifiziert. Eine Verkaufschance sollte projektbasiert sein, um alle projektspezifischen Erweiterungen und Funktionen im nachgelagerten Verkaufsprozess für dieses Geschäft zu aktivieren. |
| Zuständiges Unternehmen | Registerkarte „Allgemein“ | Dies ist das Unternehmen oder die juristische Person, die das Projekt für den Kunden bereitstellt. | Diese Feldinformationen werden in das entsprechende Feld im Projektangebot kopiert, das aus dieser Verkaufschance erstellt wird. |
| Kontakt | Registerkarte „Allgemein“ | Verweis auf den Hauptkontakt des Kunden für dieses Geschäft. | |
| Konto | Registerkarte „Allgemein“ | Verweis auf die Firma oder den Kontodatensatz des Kunden. | |
| Konto-Manager | Registerkarte „Allgemein“ | Der Name des Account Managers für diese projektbasierte Verkaufschance. | Der Account Manager ist verantwortlich für die Verwaltung der Beziehung zum Kunden bis zum Abschluss dieses Projekts. Basierend auf dem buchbaren Ressourceneintrag, der an den Account Manager gebunden ist, ist die Vertragseinheit voreingestellt. |
| Vertragseinheit | Registerkarte „Allgemein“ | Die Organisationseinheit, die für die Bereitstellung des Projekts oder der mit diesem Geschäft verbundenen Projekte verantwortlich ist. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Jede Vertragseinheit hat eine Währung, und diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während des Projekts anfallen. |

Für alle anderen Felder und Abschnitte auf der Registerkarte **Zusammenfassung** der Verkaufschance siehe [Erstellen oder Bearbeiten einer Verkaufschance (Vertrieb und Vertriebs-Hub)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
