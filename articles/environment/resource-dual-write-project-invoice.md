---
title: Projektrechnungsintegration
description: Dieses Thema enthält Informationen zur Dual-Write-Integration von Project Operations für Debitorenfakturierung.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996565"
---
# <a name="project-invoice-integration"></a>Projektrechnungsintegration

Dieses Thema enthält Informationen zur Dual-Write-Integration von Project Operations für Debitorenfakturierung.

Im Project Operations verwaltet der Projektmanager den Projektabrechnungsstau und erstellt eine Proforma-Rechnung für den Debitor in Microsoft Dataverse. Basierend auf dieser Proforma-Rechnung erstellt der Debitorenbuchhalter oder Projektbuchhalter eine kundenorientierte Rechnung. Durch die Dual-Write-Integration wird sichergestellt, dass die Proforma-Rechnungsdetails mit Finance and Operations Apps synchronisiert werden. Nachdem die kundenorientierte Rechnung gebucht wurde, aktualisiert das System die relevanten Projektdaten in Dataverse mit dem Buchhaltungsdetail. Die folgende Grafik bietet einen allgemeinen konzeptionellen Überblick über diese Integration.

   ![Projektrechnungsintegration](./media/DW5Invoicing.png)

Nachdem der Projektmanager die Proforma-Rechnung in Dataverse bestätigt hat, werden die Proforma-Rechnungskopfinformationen mit Finance and Operations Apps synchronisiert, die die Dual-Write-Tabellenzuordnung **Projektrechnungsvorschlag V2 (Rechnungen)** verwenden. Dies ist eine Einwegintegration von Dataverse zu Finance and Operations Apps. Erstellen oder Löschen von Projektrechnungsvorschlägen direkt in Finance and Operations Apps werden nicht unterstützt.

Rechnungsbestätigung in Dataverse löst auch die Geschäftslogik aus, um abrechnungsbezogene Datensätze in der Entität **Istwerte** zu erstellen. Diese Datensätze werden mit Finance and Operations mithilfe der Dual-Write-Tabellenzuordnung **Project Operations Integrationsistwerte (msdyn\_actuals) synchronisiert.** Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md). 

Projektrechnungsvorschlagszeilen werden mithilfe des periodischen Prozesses **Aus Stagingtabelle importieren** erstellt. Dieser Prozess basiert auf den Angaben zu den in Rechnung gestellten Verkaufszahlen in der Tabelle **Istwerte-Staging**. Weitere Informationen finden Sie unter [Projektrechnungsvorschläge verwalten](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
