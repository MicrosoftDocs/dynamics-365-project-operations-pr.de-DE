---
title: Aktualisieren von Plug-In-Attributen mit neuen Preisdimensionen
description: Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575027"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Plug-In-Attribute mit neuen Preisdimensionen aktualisieren

Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.

> [!NOTE]
> Dieses Thema gilt nur für die Angebots- und Vertragsfunktionen in Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Anforderungen
Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Verfahren in den folgenden Themen ausgeführt haben:

  - [Erstellen von benutzerdefinierten Feldern und Entitäten](create-custom-fields-entities-pricing-dimensions.md) 
  - [Hinzufügen von benutzerdefinierten Feldern zur Preisgestaltung und zu Transaktionsentitäten ](add-custom-fields-price-setup-transactional-entities.md)
  - [Einrichten von benutzerdefinierten Feldern als Preisdimensionen](set-up-custom-fields-pricing-dimensions.md). 
  
Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück.

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