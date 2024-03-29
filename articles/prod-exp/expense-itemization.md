---
title: Ausgabenaufschlüsselung
description: Dieser Artikel erklärt, wie Sie Ausgaben mit Hilfe des neu gestalteten Arbeitsbereichs Ausgaben aufschlüsseln können.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920933"
---
# <a name="expense-itemization"></a>Ausgabenaufschlüsselung

[!include [banner](../includes/banner.md)]

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Unternehmen verlangen von ihren Mitarbeitern oft eine detaillierte Aufstellung der Reisekosten. Eine Hotelrechnung kann beispielsweise mehrere aufgeschlüsselte Positionen für Zimmerpreis, Steuern, Parken und andere sonstige Ausgaben enthalten, die täglich während der Aufenthaltsdauer anfallen. Oder eine Essensausgabe erfordert möglicherweise eine detailliertere Aufschlüsselung für Frühstück, Mittag‑ oder Abendessen. Unabhängig von den Anforderungen der Organisation kann jede Ausgabenkategorie so eingerichtet werden, dass sie die Unterkategorien oder Einzelposten widerspiegelt, aus denen eine Ausgabe besteht. Während die Aufschlüsselung in **Ausgabenverwaltung** immer unterstützt wurde, ermöglicht der Arbeitsbereich **Neu gestaltete Spesen** eine effizientere Aufschlüsselung, wenn die Funktion **Möglichkeit, wiederkehrende Ausgaben schnell aufzuschlüsseln** aktiviert ist.  

## <a name="enable-quick-itemization"></a>Schnellaufschlüsselung aktivieren 

Sie können die Funktion **Möglichkeit, wiederkehrende Ausgaben schnell aufzuschlüsseln** verwenden, um wiederkehrende Ausgaben schnell aufzuschlüsseln und gleichzeitig die täglichen Ausgaben nicht jedes Mal für die Dauer des Aufenthalts eingeben zu müssen. Führen Sie die folgenden Schritte aus, um die Schnellaufschlüsselung zu aktivieren.

1. Gehen Sie zum Arbeitsbereich **Funktionsverwaltung** und suchen und wählen Sie in der Liste der Funktionen **Spesenabrechnungen neu gedacht** aus. 
2. Wählen Sie **Jetzt aktivieren** aus. 
3. Suchen und wählen Sie in der Funktionsliste **Möglichkeit, wiederkehrende Ausgaben schnell aufzuschlüsseln**.
4. Wählen Sie **Jetzt aktivieren** aus. 

## <a name="itemization-grid"></a>Aufschlüsselungsraster 

Wenn eine Ausgabenkategorie Unterkategorien oder verschiedene Komponenten hat, aus denen diese Ausgaben bestehen, kann sie aufgeschlüsselt werden. Um eine Ausgabe aufzuschlüsseln, wählen Sie in der Spesenabrechnung die Spesenzeile aus und wählen Sie im **Kostendetails**-Bereich **Aktionen** > **Aufschlüsseln**. Der **Aufschlüsselung**-Schieberegler zeigt ein Raster mit Feldern an. Die folgende Tabelle enthält ein Beispiel für jedes Feld im Raster und wie das Feld in der Spesenabrechnung dargestellt wird. 

|     Feld          |     Beschreibung des Dataflows                                                                                  |     Beispiel              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Unterkategorie    |     Die Liste der Unterkategorien, die unter dem Ausgabenkategorietyp **Hotel** konfiguriert sind.             |     Täglicher Zimmerpreis      |
|     Startdatum     |     Das Datum, an dem der Aufwandsposten zum ersten Mal angefallen ist.                                           |     13.09.2021           |
|     Tagesrate     |     Der angefallene Betrag des Ausgabenelements.                                                    |     200                  |
|     Menge       |     Die Häufigkeit, mit der die Gebühr über einen kontinuierlichen Zeitraum wiederholt wird.                       |     3                    |

![Ausgaben aufschlüsseln.](media/Itemization%20screen%201.png)

Wenn Sie eine Aufschlüsselung speichern, sehen Sie eine einzelne aufgeschlüsselte Zeile für die im Aufschlüsselungsraster angegebene Menge. Jede Zeile beginnt an dem im Raster angegebenen Datum.

![Aufgeschlüsselter Bericht.](media/Itemization%20screen%202.png)

