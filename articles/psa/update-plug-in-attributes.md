---
title: Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten
description: Dieser Artikel enthält Informationen über die Aktualisierung von Plug-In-Attributen für Dimensionen zur Preisgestaltung.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913205"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Wenn Sie die Funktionen der Project Service Automation (PSA) zur Angebotserstellung und Vertragsabwicklung nicht verwenden, können Sie diesen Artikel auslassen.

Dieser Artikel setzt voraus, dass Sie die Verfahren in den Artikeln [Erstellen von angepassten Feldern und Entitäten](create-custom-fields-entities.md), [Hinzufügen von angepassten Feldern zu Preiseinstellungen und transaktionalen Entitäten](field-references.md) und [Einrichten von angepassten Feldern als Preisdimensionen](set-up-pricing-dimensions.md) abgeschlossen haben. Wenn Sie diese Prozeduren nicht abgeschlossen haben, gehen Sie zurück und schließen Sie sie ab und kehren Sie dann zu diesem Artikel zurück.

Wenn ein Angebotspositionsdetail auf der Seite **Angebotsposition** für eine Projektangebotszeile erstellt wird, erstellt das System zwei Vorkalkulationspositionen im Hintergrund – eine Position für die Kostenseite der Vorkalkulation und eine für die Vertriebsseite. Selbes gilt auch für Projektvertragspositionen.

Wenn Sie eine Änderung der Menge oder eines Felds auf der Kostenseite vornehmen, wird die Änderung auf die Vertriebsseite übertragen. Dies ist möglich wegen der folgenden Plug-Ins, die nach einer Änderung der Preisdimensionen erneut registriert werden müssen.

- PreOperationContractLineDetailUpdate – aktualisiert **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – aktualisiert **msdyn_quotelinetransaction**.

Die folgenden Schritte führen Sie durch den Prozess der Registrierung der Plug-Ins.

1. Öffnen Sie das **PluginRegistrationTool**, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.
2. Klicken Sie auf **Suchen**, und suchen Sie nach dem Plug-In, das aktualisiert werden soll.

 ![Screenshot der Suchstruktur.](media/PRT-1.png)

3. Nachdem das Plug-In gefunden wurde, wählen Sie es aus, und klicken Sie dann auf **Hauptformular auswählen**.

4. Wählen Sie den Schritt des Plug-Ins, das aktualisiert werden soll, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.

 ![Screenshot des Plug-Ins, das aktualisiert werden soll.](media/PRT-2.png)
 
5. Klicken Sie im Updatefenster auf die Auslassungspunkte (**...**) in den Filterattributen.

 ![Screenshot der Informationen zu „Vorhandene Schrittkonfiguration aktualisieren“.](media/PRT-3.png)
 
6. Aktivieren Sie die Preisattribut-Kontrollkästchen.

 ![Screenshot, der die Kontrollkästchenauswahl für Preisattribute zeigt.](media/PRT-4.png)

7. Klicken Sie auf **OK**, um die Seite zu schließen, und wählen Sie dann **Aktualisierungsschritt** aus.

 ![Screenshot, der die Schaltfläche „Aktualisierungsschritt“ anzeigt.](media/PRT-5.png)
 
8. Wiederholen Sie diesen Prozess für das zweite Plug-In, **PreOperationQuoteLineDetail – Update von msdyn_quotelinetransaction**.

9. Schließen Sie das Plug-in-Registrierungstool.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
