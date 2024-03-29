---
title: Transaktionskategorie als Preisdimension verwenden
description: In diesem Artikel erfahren Sie, wie Sie das Feld Transaktionskategorie als Dimension für die Preisgestaltung verwenden.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911693"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Transaktionskategorie als Preisdimension verwenden


_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dieser Artikel erklärt, wie Sie das Feld **Transaktionskategorie** als Dimension für die Preisgestaltung verwenden können. 

## <a name="prerequisites"></a>Anforderungen
Bevor Sie die Schritte in diesem Artikel ausführen, müssen Sie eine neue Lösung für Preisdimensionen in Ihrem Unternehmen haben. Wenn Sie noch keine erstellt haben, lesen Sie [Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen](create-custom-fields-entities-pricing-dimensions.md).

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