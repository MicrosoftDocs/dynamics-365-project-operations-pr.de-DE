---
title: Währung
description: Dieses Thema enthält Informationen zum Hinzufügen und Entfernen von Währungstypen in Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8d4e1d73dc183ed572fb5099d055d2fbe0c08746
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121217"
---
# <a name="currency"></a>Währung

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Währungen bestimmen die Preise für Produkte im Produktkatalog und die Transaktionskosten, z. B. für Vertriebsaufträge. Wenn die Kunden über mehrere Regionen verteilt sind, fügen Sie deren Währungen hinzu, um Ihre Transaktionen zu verwalten. Fügen Sie die Währungen hinzu, die am meisten Ihren aktuellen und zukünftigen Geschäftsanforderungen entsprechen.  

> [!NOTE]
> Wenn es sich bei Ihrer Umgebung um eine Common Data Service Umgebung handelt, befinden Sie sich im Power Platform Admin Center und wählen die Seite **Währungen** (**Umgebungen** > [Umgebung auswählen] > **Einstellungen** > **Unternehmen** > **Währungen**) aus, die Seite ist leer. Das liegt daran, dass das Einstellen einer Währung in Common Data Service-Umgebungen nicht unterstützt wird.

## <a name="add-a-currency"></a>Hinzufügen einer Währung  
Bevor Sie diesen Vorgang starten prüfen Sie, dass die Sicherheitsrollen die Systemadministratorberechtigungen enthalten. 

1. Wählen Sie im Power Platform-Admin-Center eine Umgebung aus. 
2. Wählen Sie **Einstellungen** > **Unternehmen** aus.
3. Wählen Sie **Währungen** aus.  
4. Wählen Sie **Neu** aus.  
5. Geben Sie die erforderlichen Daten ein.  


   |          Feld          |                                                                                                                                                                                                                                                                                                                                                                            Beschreibung                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Währungstyp**    | - **System** – Wählen Sie diese Option aus, wenn Sie die in modellgesteuerten Apps in Dynamics 365 verfügbaren Währungen verwenden möchten. Wählen Sie **Suche**, um nach einer Währung zu suchen. Wenn Sie einen Währungscode auswählen, werden **Währungsname** und **Währungssymbol** für die ausgewählte Währung automatisch hinzugefügt.<br />- **Benutzerdefiniert** – Wählen Sie diese Option aus, wenn Sie eine Währung hinzufügen möchten, die in modellgesteuerten Apps in Dynamics 365 nicht verfügbar ist. In diesem Fall müssen Sie die Werte für **Währungscode**, **Genauigkeit für die Angabe von Währungsbeträgen**, **Währungsname**, **Währungssymbol** und **Währungsumrechnung** manuell eingeben. |
   |    **Währungscode**    |                                                                                                                                                                                                                                                                                                                                            Kurzform der Währung. Z. B. **EUR** für Euro.                                                                                                                                                                                                                                                                                                                                            |
   | **Währungspräzision**  |                                                                                                                                                                                  Geben Sie die Anzahl der Dezimalstellen ein, die für diese Währung angezeigt werden sollen.  Sie können einen Wert zwischen 0 und 4 eingeben. **Hinweis:**  Wenn Sie einen Genauigkeitswert im Dialogfeld **Systemeinstellungen** festgelegt haben, wird dieser Wert hier angezeigt.                                                                                                                                                                                  |
   |    **Währungsname**    |                                                                                                                                                                                                                                         Wenn Sie aus der Liste der in modellgesteuerten Dynamics 365-Apps verfügbaren Währungen einen Währungscode ausgewählt haben, wird hier der Währungsname für den ausgewählten Code angezeigt. Wenn Sie **Benutzerdefiniert** ausgewählt haben, geben Sie den Namen der Währung ein.                                                                                                                                                                                                                                          |
   |   **Währungssymbol**   |                                                                                                                                                                                                                                                                      Wenn Sie aus der Liste der verfügbaren Währungen einen Währungscode ausgewählt haben, wird hier das Symbol für die ausgewählte Währung angezeigt. Wenn Sie **Benutzerdefiniert** als Währungstyp ausgewählt haben, geben Sie das Symbol für die neue Währung ein.                                                                                                                                                                                                                                                                       |
   | **Währungsumrechnung** |                                                                                                                                                                                                                                     Geben Sie den Wert der ausgewählten Währung in US-Dollar ein. Dies ist der Betrag über den die ausgewählte Währung in die Basiswährung umgerechnet wird. **Wichtig:**  Stellen Sie sicher, dass Sie diesen Wert so regelmäßig wie nötig aktualisieren, um ungenaue Berechnungen in Ihren Transaktionen zu vermeiden.                                                                                                                                                                                                                                      |


6. Wenn Sie fertig sind, wählen Sie auf der Befehlsleiste **Speichern** oder **Speichern und schließen** aus.  

   > [!TIP]
   >  Um eine Währung zu bearbeiten, wählen Sie die Währung aus, und geben Sie dann die neuen Werte ein oder wählen sie aus.  

## <a name="delete-a-currency"></a>Löschen einer Währung  

1. Wählen Sie im Power Platform-Admin-Center eine Umgebung aus. 
2. Wählen Sie **Einstellungen** > **Unternehmen** aus.
3. Wählen Sie **Währungen** aus.  
4. Wählen Sie in der angezeigten Liste der Währungen, die Währung aus, die Sie löschen wollen.  
5. Klicken Sie auf **Löschen**.  
6. Bestätigen Sie den Löschvorgang.  

> [!IMPORTANT]
>  Sie können keine Währungen löschen, die von anderen Datensätzen verwendet werden, sondern diese nur deaktivieren. Durch Deaktivieren der Währungsdatensätze werden die Währungsinformationen, die in vorhandenen Datensätzen wie Verkaufschancen oder Aufträgen gespeichert sind, nicht entfernt. Sie können jedoch die deaktivierte Währung nicht für neue Transaktionen auswählen.  
