---
title: Projektrechnungsintegration
description: Dieser Artikel enthält Informationen über Project Operations Dual-write Integration für die Kundenfakturierung.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912101"
---
# <a name="project-invoice-integration"></a>Projektrechnungsintegration

Dieser Artikel enthält Informationen über Project Operations Dual-write Integration für die Kundenfakturierung.

Im Project Operations verwaltet der Projektmanager den Projektabrechnungsstau und erstellt eine Proforma-Rechnung für den Debitor in Microsoft Dataverse. Basierend auf dieser Proforma-Rechnung erstellt der Debitorenbuchhalter oder Projektbuchhalter eine kundenorientierte Rechnung. Die Integration des dualen Schreibens stellt sicher, dass die Proforma-Rechnungsdetails mit Finanz- und Betriebs-Apps synchronisiert werden. Nachdem die kundenorientierte Rechnung gebucht wurde, aktualisiert das System die relevanten Projektdaten in Dataverse mit dem Buchhaltungsdetail. Die folgende Grafik bietet einen allgemeinen konzeptionellen Überblick über diese Integration.

   ![Projektrechnungsintegration.](./media/DW5Invoicing.png)

Nachdem der Projektmanager die Proforma-Rechnung in Dataverse bestätigt hat, werden die Proforma-Rechnungskopfinformationen mithilfe der Tabellenzuordnung für duales Schreiben **Projektrechnungsvorschlag V2 (Rechnungen)** mit Finanz- und Betriebs-Apps synchronisiert. Dies ist eine Einweg-Integration von Dataverse zu Finanz- und Betriebs-Apps. Das direkte Erstellen oder Löschen von Projektrechnungsvorschlägen in Finanz- und Betriebs-Apps wird nicht unterstützt.

Rechnungsbestätigung in Dataverse löst auch die Geschäftslogik aus, um abrechnungsbezogene Datensätze in der Entität **Istwerte** zu erstellen. Diese Datensätze werden mithilfe der Tabellenzuordnung **Ist-Werte für die Project Operations-Integration (msdyn\_actuals)** für duales Schreiben mit Finance and Operations synchronisiert. Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md). 

Projektrechnungsvorschlagszeilen werden mithilfe des periodischen Prozesses **Aus Stagingtabelle importieren** erstellt. Dieser Prozess basiert auf den Angaben zu den in Rechnung gestellten Verkaufszahlen in der Tabelle **Istwerte-Staging**. Weitere Informationen finden Sie unter [Projektrechnungsvorschläge verwalten](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
