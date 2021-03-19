---
title: Eine manuelle Proforma-Rechnung erstellen – Lite
description: Dieses Thema bietet Informationen zum Erstellen einer manuellen Proforma-Rechnung in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274187"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Eine manuelle Proforma-Rechnung erstellen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations können Proforma-Rechnungen nach Bedarf manuell erstellt werden. Sie können manuell eine Proforma-Rechnung über die Listenseite **Projektverträge** oder über die Listenseite **Projektvertrag** erstellen.

##  <a name="project-contracts-list-page"></a>Listenseite „Projektverträge“

Wählen Sie über die Listenseite **Projektverträge** eine oder mehrere Projektverträge aus, und erstellen Sie Rechnungen für alle ausgewählten Datensätze.

Das System prüft, um zu erkennen, welcher der ausgewählten Projektverträge einen Rückstand in **Bereit für die Rechnungsstellung** vor dem heutigen Datum aufweist. Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen. Wenn ein Projektvertrag mehrere Kunden hat, wird möglicherweise eine Rechnung pro Kunde und mehrere Rechnungen pro Projektvertrag erstellt.

Alle erstellten Projektrechnungen sind auf der Seite **Rechnung** im Abschnitt **Abrechnung** des Bereichs **Umsatz** verfügbar.

## <a name="project-contract-details-page"></a>Seite „Projektvertragsdetails“

Eine Proforma-Rechnung kann auch aus der **Projektvertrag** Detailseite erstellt werden. Das System prüft, ob der Projektvertrag das Rechnungsrückstandsprotokoll **Bereit für die Rechnungsstellung** aufweist, der vor dem heutigen Datum datiert ist. Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen basierend auf der Anzahl der Kunden in jeder Vertragszeile.

Wenn eine einzelne Proforma-Rechnung erstellt wird, wird die Seite **Rechnung** geöffnet. Wenn für diesen Projektvertrag mehrere Rechnungen erstellt wurden, wird die Listenseite **Rechnungen** geöffnet, um alle erstellten Rechnungen anzuzeigen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]