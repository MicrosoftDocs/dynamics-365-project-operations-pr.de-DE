---
title: Eine Ad-hoc-Vorauszahlung für einen Vertrag erstellen – Lite
description: Dieses Thema enthält Informationen zum Erstellen eines Vorschusses für einen Vertrag nach Bedarf.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181361"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Eine Ad-hoc-Vorauszahlung für einen Vertrag erstellen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Microsoft Dynamics 365 Project Operations unterstützt Rechnungsszenarien mit Vorauszahlungen und Vorschüssen. Der Prozess für die Verwendung von **Vorauszahlungen** in **Project Operations** ähnelt **Vorschuss**-Verträgen. 

Führen Sie die folgenden Schritte aus, um dem Kunden einen Vorschuss in Rechnung zu stellen.

1. Gehen Sie zur **Projektvertrag**-Seite, und wählen Sie dann die **Vorauszahlungen und Vorschüsse**-Registerkarte aus.
2. Wählen Sie im Unterraster, in dem alle zuvor erfassten Vorschüsse und Vorauszahlungen aufgeführt sind, die Option **+ Neuer Projektvertragsvorschuss** aus. 

    Das **Schnellerfassung**-Formular wird geöffnet, um eine Vorauszahlung oder einen Vorschuss zu erfassen.
    
3. In der folgenden Tabelle sind die Felder zum Aufzeichnen eines Vorschusses und die Überlegungen aufgeführt, die beim Erstellen neuer Felder zu berücksichtigen sind:

    | Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
    | --- | --- | --- |
    | **Projektvertragskunde** | Dieses Feld gibt an, welchem Kunden im Vertrag dieser Vorschuss in Rechnung gestellt wird. | Wenn Sie mehrere Kunden im Vertrag haben und jedem von ihnen einen bestimmten Einbehaltungs- oder Vorschussbetrag in Rechnung stellen möchten, erstellen Sie für jeden Kunden einen individuellen Vorschuss. |
    | **Beschreibung** | Die Beschreibung des Zwecks oder des Zeitpunkts des Vorschusses, um diesen Fortschritt zu identifizieren. | Diese Beschreibung wird in der Rechnungszeile für diesen Vorschuss angezeigt. |
    | **Betrag** | Der Betrag für die Vorauszahlung oder den Vorschuss. | Dieser Betrag wird in der Rechnungszeile für diesen Vorschuss angezeigt. |
    | **Rechnungsdatum** | Das Datum, an dem dieser Vorschuss dem Kunden in Rechnung gestellt wird. | Dies ist das Datum für den automatisierten Rechnungserstellungsprozess, um eine Rechnungsposition für diesen Vorschuss zu erstellen. |
    | **Rechnungsstatus** | Dies ist eine Optionseinstellung, die angibt, ob dieser Vorschuss einem Rechnungsentwurf für diesen Kunden hinzugefügt wird. Dies sind die möglichen Werte:</br>- **Nicht bereit für die Rechnungsstellung**</br>- **Bereit für die Rechnungsstellung** | Wenn eine Vorauszahlung oder ein Vorschuss als **Bereit für die Rechnungsstellung** markiert ist, wird dies als Zeilenzeit auf einem Rechnungsentwurf hinzugefügt. Nur ein vollständig in Rechnung gestellter Vorschuss kann verwendet werden, um die Projektkosten für den nächsten Rechnungszeitraum abzugleichen. |

4. Wählen Sie **Speichern und schließen** im Schnellerfassungs-Dialogfeld aus, um den Vorschuss oder die Vorauszahlung aufzuzeichnen.
