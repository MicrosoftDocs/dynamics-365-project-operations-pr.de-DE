---
title: Kilometerleistung mithilfe von Kilometertarifstufen einrichten
description: Dieses Thema bietet Informationen zu Kilometersätzen und Kilometertarifstufen.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083670"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Kilometerleistung mithilfe von Kilometertarifstufen einrichten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn ein Aufwand gemeldet wird und die ausgewählte Aufwandskategorie **Kilometerstand** ist, wird der Betrag für diese Aufwandszeile nach dem Betrag *Tarif pro Kilometer* berechnet. Dieser Betrag wird anhand definierter Meilenstufen oder, falls keine Meilenstufen eingerichtet sind, anhand eines Standard-Kilometersatzes ermittelt. 

Kilometertarifstufen können eingerichtet werden, indem Sie zu **Ausgabenverwaltung** > **Einrichten** > **Allgemeines** > **Ausgabenkategorien** > **Kilometerstand** > **Kategorie einrichten** gehen.

Wenn Ihr Unternehmen nach dem Upgrade auf 10.0.18 die Kategorie der Kilometerausgaben verwendet, sollten Sie die Kilometerfunktion aktivieren, nachdem Sie die unten aufgeführten Designänderungen überprüft haben. 

Das neue Design der Kilometertarifstufen beeinflusst, wie der Wert in dem Feld **Menge** bearbeitet wird. Vor der Veröffentlichung von 10.0.18 galt der Wert im Feld **Menge** als untere Grenze. Wenn die Akkumulation diesen Wert überschritt, wurde die entsprechende Rate verwendet.  Ab 10.0.18 gilt der Wert im Feld **Menge** als obere Grenze. Der entsprechende Tarif wird verwendet, wenn die Kilometerleistung geringer ist als der Wert in dem Feld **Menge**.  Das neue Modell für Kilometerstufen hilft bei der Konsistenz über die Kilometerstufen hinweg und verbessert die Benutzerfreundlichkeit.   

Alle genehmigten Ausgabenabrechnungen werden bei der Buchung entsprechend dem neuen Design neu berechnet.

## <a name="example"></a>Beispiel
 
### <a name="before-version-10018"></a>Vor Version 10.0.18
Mit zwei Kilometertarifstufen steht das Feld **Menge** in jeder Stufe für die untere Kilometerbegrenzung. Derzeit hat Ebene eins einen Wert von Null (0) und eine Rate von 0,45, und Ebene zwei hat einen Wert von 1000 und eine Rate von 0,25. Wenn die kumulierten Meilen oder Kilometer den Wert im Feld überschreiten, wird der entsprechende Tarif verwendet. Wenn keine Zeile mit Menge Null vorhanden ist, verwendet das System den Kilometersatz, der in der Spesenverwaltung definiert ist. 
 
Wenn ein Mitarbeiter eine Ausgabenabrechnung mit 1.500 Kilometer einreicht, lauten die beiden Kilometerzeilen auf der gebuchten Ausgabenabrechnung: 1000 (Tarif 0,45) + 500 (Tarif 0,25) = 575,00.

### <a name="after-version-10018"></a>Nach Version 10.0.18
In 10.0.18 stellt das Feld **Menge** in jeder Ebene die Obergrenze der Ebene dar. Derzeit hat Ebene eins einen Wert von 999 und eine Rate von 0,45, und Ebene zwei hat einen Wert von 999,999,999.00 und eine Rate von 0,25. Wenn die kumulierten Meilen oder Kilometer den Wert im Feld **Menge** überschreiten, wird der entsprechende Tarif verwendet. Wenn alle oberen Grenzwerte überschritten sind, verwendet das System den Kilometersatz, der in der Ausgabenverwaltung definiert ist. 
 
Um das gleiche Szenario korrekt zu berechnen, muss die Einrichtung der Stufe geändert werden. Das Feld **Menge** in Ebene 1 hat einen Wert von 999,00 und einen Wert von 999,999,999.00 in Ebene 2. Überschreitet ein Mitarbeiter die Gesamtmenge der Meilen oder Kilometer in Stufe eins, verwendet das System den in der Spesenverwaltung definierten Kilometersatz. 
  
Wenn ein Mitarbeiter eine Ausgabenabrechnung mit 1.500 Kilometer einreicht, lauten die beiden Kilometerzeilen auf der gebuchten Ausgabenabrechnung: 1000 (Tarif 0,45) + 500 (Tarif 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktivieren Sie die Meilenberechnung für mehrere Meilenstufen mit derselben Tariffunktion

Die Funktion **Kilometerberechnung für mehrere Kilometerstufen mit derselben Tariffunktion** verbessert die Kilometerberechnung. Gehen Sie wie folgt vor, um diese Funktion zu aktivieren.

1. Gehen Sie zu **Arbeitsbereiche** > **Funktionenverwaltung**. 
2. Suchen und wählen Sie in der Liste **Berechnung des Kilometerbetrags für mehrere Kilometerstufen mit demselben Tarif**, und wählen Sie dann **Jetzt aktivieren**.

Nachdem Sie die Funktion aktiviert haben, setzen Sie die Meilenstufen zurück, um den Wert des Felds **Menge** zu reflektieren. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
