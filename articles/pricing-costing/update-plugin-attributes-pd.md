---
title: Aktualisieren von Plug-In-Attributen mit neuen Preisdimensionen
description: In diesem Artikel erfahren Sie, wie Sie Plug-in-Attribute für Preisdimensionen aktualisieren.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920013"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Plug-In-Attribute mit neuen Preisdimensionen aktualisieren

In diesem Artikel erfahren Sie, wie Sie Plug-in-Attribute für Preisdimensionen aktualisieren.

> [!NOTE]
> Dieser Artikel gilt nur für die Funktionen für Angebote und Verträge in Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Anforderungen
Bevor Sie die Schritte in diesem Artikel ausführen, müssen Sie die Vorgänge in den folgenden Artikeln abgeschlossen haben:

  - [Erstellen von benutzerdefinierten Feldern und Entitäten](create-custom-fields-entities-pricing-dimensions.md) 
  - [Hinzufügen von benutzerdefinierten Feldern zur Preisgestaltung und zu Transaktionsentitäten ](add-custom-fields-price-setup-transactional-entities.md)
  - [Einrichten von benutzerdefinierten Feldern als Preisdimensionen](set-up-custom-fields-pricing-dimensions.md). 
  
Wenn Sie diese Prozeduren noch nicht abgeschlossen haben, schließen Sie sie ab und kehren Sie dann zu diesem Artikel zurück.

## <a name="register-a-plug-in"></a>Registrieren eines Plug-Ins
Wenn ein Angebotszeilendetail auf der **Angebotszeile**-Seite für eine Projektangebotszeile erstellt wird, erstellt das System zwei Schätzzeilen. Eine Zeile ist für die Kostenseite der Schätzung und die andere Zeile ist für den Verkauf auf der Seite. Selbes gilt auch für Projektvertragspositionen.

Wenn Sie eine Änderung der Menge oder eines Felds auf der Kostenseite vornehmen, wird die Änderung auf der Vertriebsseite übernommen. Dies ist möglich, weil die PreOperation-Plug-Ins für Quotelinedetail- und Contractline-Detailentitäten bestimmte Attribute auf der Kostenseite mit der Verkaufsseite der Transaktion verbinden. Wenn Änderungen an den Werten der Preisdimension auf der Verkaufsseite auch auf der Kostenseite vorgenommen werden müssen, müssen die folgenden Plug-Ins nach Änderungen an einer Preisdimension erneut registriert werden.

Dies sind die Plug-Ins zum Aktualisieren und erneuten Registrieren:

- PreOperationContractLineDetailUpdate – **msdyn_orderlinetransaction aktualisieren**.
- PreOperationQuoteLineDetailUpdate – **msdyn_quotelinetransaction aktualisieren**.

Führen Sie die folgenden Schritte aus, um die Plug-Ins zu aktualisieren und neu zu registrieren.

1. Öffnen Sie **PluginRegistrationTool** und stellen Sie eine Verbindung zu Ihrer Project Operations Dataverse-Umgebung her.
2. Wählen Sie **Suche** und geben Sie die ersten Buchstaben des zu aktualisierenden Plug-Ins ein.
3. Nachdem das Plug-In gefunden wurde, wählen Sie es aus, und klicken Sie dann auf **Hauptformular auswählen**.
4. Wählen Sie den Schritt **msdyn_orderlinetransaction aktualisieren** aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.
5. Klicken Sie im **Update**-Dialogfeld auf die Auslassungspunkte (**...**) in den Filterattributen.
6. Das Fenster „Filterattribute“ wird geöffnet und enthält eine Liste aller Attribute in der Entität und der Preisdimensionen. Aktivieren Sie die Kontrollkästchen für die Preisdimensionsattribute.
7. Wählen Sie **OK**, um die Seite zu schließen, und wählen Sie dann **Aktualisierungsschritt** aus.
8. Wiederholen Sie die Schritte 2 bis 7 für das zweite Plug-In, **PreOperationQuoteLineDetail**. Für dieses Plug-In müssen Sie den Schritt **msdyn_quotelinetransaction aktualisieren** aktualisieren.
9. Schließen Sie das **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]