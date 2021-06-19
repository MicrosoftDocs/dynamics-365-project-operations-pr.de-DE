---
title: Transaktionskategorie als Preisdimension verwenden
description: Dieses Thema bietet Informationen über das Verwenden des Transaktionskategoriefelds als Preisdimension.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d956545e1ad38fb09660f107e085f38d099c2207
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004440"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Transaktionskategorie als Preisdimension verwenden


_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dieses Thema erklärt, wie ein **Transaktionskategorie**-Feld als Preisdimension verwendet wird. 

## <a name="prerequisites"></a>Anforderungen
Bevor Sie die in diesem Thema beschriebenen Verfahren ausführen, müssen Sie über eine neue Lösung für die Preisdimension für Ihr Unternehmen verfügen. Wenn Sie noch keine erstellt haben, lesen Sie [Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Transaktionskategoriefeld zu Formularen und Ansichten hinzufügen
Um das **Transaktionskategorie**-Feld in der Preisdimensionslösung anzuzeigen, müssen Sie das Feld allen Formularen und Ansichten als Entität hinzufügen.

In der folgenden Tabelle sind alle sofort einsatzbereiten Formulare und Ansichten nach Entitäten aufgeführt. Sie müssen das neue Feld auch zusätzlichen Formularen oder Ansichten in Ihren benutzerdefinierten Entitäten hinzufügen.

|  Entity        | Formulare     |Ansichten        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollenpreis| Information |– Preise der aktiven Ressourcenkategorie<br> – Zugeordnete Ansicht: Preis der Ressourcenkategorie |
|  Rollenpreisaufschlag| Information|– Aktive Rollenpreisaufschläge<br>– Zugeordnete Ansicht: Rollenpreisaufschlag |
|  Detailinformationen zur Angebotsposition|– Projektinformationen<br>– Projektschnellerfassung| – Details zu aktiver Angebotsposition<br>– Kombinierte Angebotspositionen<br>– Zugeordnete Ansicht: Angebotsposition |
|  Projektvertragsposition|– Projektinformationen<br>– Projektschnellerfassung|– Kombinierte Vertragszeilendetails<br>– Aktive Vertragszeilendetails<br>– Zugeordnete Vertragspositionsdetail |
|  Projektaufgabe|– Information<br>– Neues Formular| &nbsp; |
|  Projektteammitglied|– Information<br>– Neues Formular|– Aktive Projektteammitglieder<br>– Projektteammitglieder<br>– Zugeordnete Projektteammitglieder |
|  Zeiteintrag|– Information<br>– Zeiteintrag erstellen|– Meine Zeiteinträge nach Datum<br>– Meine Zeiteinträge für diese Woche<br>– Zeiteinträge zur Genehmigung|
|  Erfassungsposition|– Information<br>– Schnellerstellung|– Aktive Erfassungspositionen<br>– Zugeordnete Erfassungsposition|
|  Rechnungsposition|– Information<br>– Schnellerstellung|– Aktive Rechnungspositionen<br>– Fakturierbare Rechnungsbuchungen<br>– Kostenlose Rechnungsbuchungen<br>– Zugeordnete Rechnungsposition <br>– Nicht-fakturierbare Rechnungsbuchungen|
|  Tatsächl.|– Information<br>– Aktive tatsächliche Transaktionen| Zugeordnete Tatsächliche Transaktionen |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Transaktionskategoriefeld als Preisdimension einrichten

1. Gehen Sie zu **Einstellungen** > **Parameter**. 
2. Auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** stellen Sie sicher, dass das Raster in der Registerkarte die Datensätze in der Entität **Preisdimensionen** anzeigt.
3. Fügen Sie **Transaktionskategorie** zu dieser Liste hinzu, und legen Sie die Felder **Gilt für Kosten** und **Gilt für Vertrieb** auf **Ja** fest.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus, und wählen Sie anschließend die Priorität für **Transaktionskategorie** in Bezug auf Kosten und Vertrieb fest.


[!INCLUDE[footer-include](../includes/footer-banner.md)]