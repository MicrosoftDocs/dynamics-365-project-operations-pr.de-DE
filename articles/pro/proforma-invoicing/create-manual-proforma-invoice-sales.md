---
title: Eine manuelle Proforma-Rechnung erstellen – Lite
description: Dieses Thema bietet Informationen zum Erstellen einer manuellen Proforma-Rechnung in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176385"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Eine manuelle Proforma-Rechnung erstellen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations können Proforma-Rechnungen nach Bedarf manuell erstellt werden. Sie können manuell eine Proforma-Rechnung über die Listenseite **Projektverträge** oder über die Listenseite **Projektvertrag** erstellen.

##  <a name="project-contracts-list-page"></a>Listenseite „Projektverträge“

Wählen Sie über die Listenseite **Projektverträge** eine oder mehrere Projektverträge aus, und erstellen Sie Rechnungen für alle ausgewählten Datensätze.

Das System prüft, um zu erkennen, welcher der ausgewählten Projektverträge einen Rückstand in **Bereit für die Rechnungsstellung** vor dem heutigen Datum aufweist. Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen. Wenn ein Projektvertrag mehrere Kunden hat, wird möglicherweise eine Rechnung pro Kunde und mehrere Rechnungen pro Projektvertrag erstellt.

Alle erstellten Projektrechnungen sind auf der Seite **Rechnung** im Abschnitt **Abrechnung** des Bereichs **Umsatz** verfügbar.

## <a name="project-contract-details-page"></a>Detailseite zu Projektverträgen

Eine Proforma-Rechnung kann auch über die Detailseite **Projektvertrag** erstellt werden, auf der die Rechnung für diesen bestimmten Projektvertrag erstellt wird. Das System prüft, ob der Projektvertrag einen Rückstand für **Bereit für die Rechnungsstellung** aufweist, der vor dem heutigen Datum liegt. Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen basierend auf der Anzahl der Kunden in jeder Vertragszeile.

Wenn eine einzelne Proforma-Rechnung erstellt wird, wird die Seite **Rechnung** geöffnet. Wenn für diesen Projektvertrag mehrere Rechnungen erstellt wurden, wird die Listenseite **Rechnungen** geöffnet, um alle erstellten Rechnungen anzuzeigen.
