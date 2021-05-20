---
title: Projektrechnungsintegration
description: Dieses Thema enthält Informationen zur Dual-Write-Integration von Project Operations für Debitorenfakturierung.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955751"
---
# <a name="project-invoice-integration"></a>Projektrechnungsintegration

Dieses Thema enthält Informationen zur Dual-Write-Integration von Project Operations für Debitorenfakturierung.

Im Project Operations verwaltet der Projektmanager den Projektabrechnungsstau und erstellt eine Proforma-Rechnung für den Debitor in Microsoft Dataverse. Basierend auf dieser Proforma-Rechnung erstellt der Debitorenbuchhalter oder Projektbuchhalter eine kundenorientierte Rechnung. Durch die Dual-Write-Integration wird sichergestellt, dass die Proforma-Rechnungsdetails mit Finance and Operations Apps synchronisiert werden. Nachdem die kundenorientierte Rechnung gebucht wurde, aktualisiert das System die relevanten Projektdaten in Dataverse mit dem Buchhaltungsdetail. Die folgende Grafik bietet einen allgemeinen konzeptionellen Überblick über diese Integration.

   ![Projektrechnungsintegration](./media/DW5Invoicing.png)

Nachdem der Projektmanager die Proforma-Rechnung in Dataverse bestätigt hat, werden die Proforma-Rechnungskopfinformationen mit Finance and Operations Apps synchronisiert, die die Dual-Write-Tabellenzuordnung **Projektrechnungsvorschlag V2 (Rechnungen)** verwenden. Dies ist eine Einwegintegration von Dataverse zu Finance and Operations Apps. Erstellen oder Löschen von Projektrechnungsvorschlägen direkt in Finance and Operations Apps werden nicht unterstützt.

Rechnungsbestätigung in Dataverse löst auch die Geschäftslogik aus, um abrechnungsbezogene Datensätze in der Entität **Istwerte** zu erstellen. Diese Datensätze werden mit Finance and Operations mithilfe der Dual-Write-Tabellenzuordnung **Project Operations Integrationsistwerte (msdyn\_actuals) synchronisiert.** Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md). 

Projektrechnungsvorschlagszeilen werden mithilfe des periodischen Prozesses **Aus Stagingtabelle importieren** erstellt. Dieser Prozess basiert auf den Angaben zu den in Rechnung gestellten Verkaufszahlen in der Tabelle **Istwerte-Staging**. Weitere Informationen finden Sie unter [Projektrechnungsvorschläge verwalten](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
