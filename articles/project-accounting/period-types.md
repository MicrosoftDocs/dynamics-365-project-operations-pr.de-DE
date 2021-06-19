---
title: Periodentypen
description: Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013485"
---
# <a name="period-types"></a>Periodentypen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Ein Periodentyp definiert, wie häufig die Einnahmen aus einem Projekt geschätzt werden. Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen. 

## <a name="create-and-work-with-period-types"></a>Erstellen und Arbeiten mit Periodentypen
Führen Sie die folgenden Schritte aus, um Periodentypen zu erstellen und damit zu arbeiten:

1. Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Schätzungen** > **Periodentypen**.
2. Wählen Sie **Neu** aus, um einen neuen Periodentyp zu erstellen. Geben Sie einen Namen und eine Beschreibung ein.
3. Wählen Sie einen Wert im **Häufigkeit** aus:

    - Wenn Sie **Woche**, **Zweiwöchentlich**, **Halbmonatlich**, **Monat**, **Tag**, **Quartal** oder **Jahr** auswählen, wird der Kalender verwendet, um die Perioden zu generieren. 
    - Wenn Sie **Hauptbuchzeitraum** auswählen, werden Sachkontoperioden aus der Hauptbuchkonfiguration zum Generieren von Perioden verwendet.
    - Wenn Sie **Unbegrenzt** auswählen, können Sie benutzerdefinierte Zeiträume angeben.
4. Wählen Sie den Periodentyp-Datensatz aus und dann **Perioden generieren**, um Perioden für den Periodentyp zu erstellen. Basierend auf der von Ihnen ausgewählten Periodenhäufigkeit haben Sie möglicherweise die Möglichkeit, ein Startdatum oder die Anzahl der zu generierenden Perioden anzugeben.
5. Wählen Sie **Perioden** aus, um generierte Perioden zu überprüfen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]