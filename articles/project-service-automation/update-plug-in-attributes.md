---
title: Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten
description: Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722012"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten

> [!NOTE]
> Wenn Sie die Funktionen zu Angebotserstellung und Vertragsabschluss der Project Service Automation (PSA) nicht verwenden, können Sie dieses Thema überspringen.

In diesem Thema wird davon ausgegangen, dass Sie die Prozeduren in den Themen [Benutzerdefinierte Felder und Entitäten erstellen](create-custom-fields-entities.md), [Benutzerdefinierte Felder zur Preiseinrichtung und zu Transaktionsentitäten hinzufügen](field-references.md) und [Benutzerdefinierte Felder als Preisdimensionen einrichten](set-up-pricing-dimensions.md) abgeschlossen haben. Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, kehren Sie zurück und schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück.

Wenn ein Angebotspositionsdetail auf der Seite **Angebotsposition** für eine Projektangebotszeile erstellt wird, erstellt das System zwei Vorkalkulationspositionen im Hintergrund – eine Position für die Kostenseite der Vorkalkulation und eine für die Vertriebsseite. Selbes gilt auch für Projektvertragspositionen.

Wenn Sie eine Änderung der Menge oder eines Felds auf der Kostenseite vornehmen, wird die Änderung auf die Vertriebsseite übertragen. Dies ist möglich wegen der folgenden Plug-Ins, die nach einer Änderung der Preisdimensionen erneut registriert werden müssen.

- PreOperationContractLineDetailUpdate – aktualisiert **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – aktualisiert **msdyn_quotelinetransaction**.

Die folgenden Schritte führen Sie durch den Prozess der Registrierung der Plug-Ins.

1. Öffnen Sie das **PluginRegistrationTool**, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.
2. Klicken Sie auf **Suchen**, und suchen Sie nach dem Plug-In, das aktualisiert werden soll.

 ![Screenshot der Suchstruktur](media/PRT-1.png)

3. Nachdem das Plug-In gefunden wurde, wählen Sie es aus, und klicken Sie dann auf **Hauptformular auswählen**.

4. Wählen Sie den Schritt des Plug-Ins, das aktualisiert werden soll, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.

 ![Screenshot des Plug-Ins, das aktualisiert werden soll](media/PRT-2.png)
 
5. Klicken Sie im Updatefenster auf die Auslassungspunkte (**...**) in den Filterattributen.

 ![Screenshot der Informationen zu „Vorhandene Schrittkonfiguration aktualisieren”](media/PRT-3.png)
 
6. Aktivieren Sie die Preisattribut-Kontrollkästchen.

 ![Screenshot, der die Kontrollkästchenauswahl für Preisattribute zeigt](media/PRT-4.png)

7. Klicken Sie auf **OK**, um die Seite zu schließen, und wählen Sie dann **Aktualisierungsschritt** aus.

 ![Screenshot, der die Schaltfläche „Aktualisierungsschritt” anzeigt](media/PRT-5.png)
 
8. Wiederholen Sie diesen Prozess für das zweite Plug-In, **PreOperationQuoteLineDetail – Update von msdyn_quotelinetransaction**.

9. Schließen Sie das Plug-in-Registrierungstool.

