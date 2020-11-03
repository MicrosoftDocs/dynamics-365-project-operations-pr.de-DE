---
title: Benutzerdefinierte Felder als Preisdimensionen einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Preisdimensionen mit benutzerdefinierten Feldern.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 087950c9639a95868a20d71286dfad4437555108
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076519"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Benutzerdefinierte Felder als Preisdimensionen einrichten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Bevor Sie beginnen, wird in diesem Thema davon ausgegangen, dass Sie die Verfahren in den Themen [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities-pricing-dimensions.md) und [Hinzufügen von benutzerdefinierten Feldern zur Preiseinrichtung und zu Transaktionsentitäten](add-custom-fields-price-setup-transactional-entities.md) abgeschlossen haben. Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, kehren Sie zurück und schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück. 

Dieses Thema enthält Informationen zum Einrichten von benutzerdefinierten Preisdimensionen. Auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** beachten Sie, dass das Raster in der Registerkarte die Datensätze in der Entität Preisdimensionen anzeigt. Standardmäßig befinden sich auf dieser Registerkarte zwei Zeilen im Raster:

- **msdyn_resourcecategory** (Rolle)
- **msdyn_OrganizationalUnit** (Organisationseinheit)

> [!IMPORTANT]
> Löschen Sie diese Zeilen nicht. Wenn Sie sie jedoch nicht benötigen, können Sie sie in einem bestimmten Kontext als nicht erforderlich festlegen, indem Sie **Gilt für Kosten** , **Gilt für Vertrieb** und **Gilt für Kauf** auf **Nein** setzen. Das Festlegen dieser Attributwerte auf **Nein** hat denselben Effekt, als ob das Feld als Preisdimension nicht vorhanden ist.

Damit ein Feld zu einer Preisdimension wird, muss es:

- als Feld in den Entitäten **Rollenpreis** und **Rollenpreisaufschlag** erstellt werden. Weitere Informationen hierzu erhalten Sie unter [Hinzufügen benutzerdefinierter Felder zum Preis und zu Transaktionsentitäten](add-custom-fields-price-setup-transactional-entities.md).
- als Zeile in der Tabelle **Preisdimension** erstellt worden sein. Beispielsweise können Sie Preisdimensionszeilen, wie in der folgenden Grafik dargestellt, hinzufügen. 

Beachten Sie, dass die Arbeitszeiten ( **msdyn_resourceworkhours** ) als aufschlagsbasierte Dimension hinzugefügt wurde und zum Raster auf der Registerkarte **Aufschlagsbasierte Preisdimension** hinzugefügt wurden.

> [!IMPORTANT]
> Jegliche Änderungen an Preisdimensionsdaten in der Tabelle, ob bei vorhandenen oder neuen Daten, werden erst weitergegeben, wenn der Cache aktualisiert wird. Die Aktualisierungszeit des Cache kann bis zu 10 Minuten betragen. Warten Sie diese Zeit ab, um die Änderungen in der Preis-Standardlogik anzuzeigen, die aus Änderungen an den Preisdimensionsdaten resultieren müssen.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Tabelle mit Attributen der Preisdimensionen
Die folgenden Abschnitte enthalten Informationen zu den verschiedenen Attributen in der Tabelle **Preisdimensionen**.

### <a name="pricing-dimension-name"></a>Preisdimensionsname
Dieser Wert muss genau dem Schemanamen des Feldes entsprechen, das der Tabelle **Rollenpreis** für benutzerdefinierte Preisdimensionen hinzugefügt wurde. Weitere Informationen zum Hinzufügen von Feldern zur Tabelle **Rollenpreis** erhalten Sie unter [Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimensionstyp
Es gibt zwei Arten von Preisdimensionen:
  
  - **Betragsbasierte Dimensionen** : Diese Dimensionswerte aus dem Eingabekontext werden mit den Dimensionswerten in der Position **Rollenpreis** abgeglichen und Preise/Kosten werden standardmäßig der Tabelle **Rollenpreis** entnommen.
  - **Aufschlagsbasierte Dimensionen** : Dies sind Dimensionen, bei denen ein 3-Schritte-Prozess erfolgt, um Preise/Kosten abzurufen:
 
    1. Die nicht aufschlagsbasierten Dimensionswerte aus dem Eingabekontext werden mit der Rollenpreisposition abgegelichen, um den Basistarif abzurufen.
    2. Die Dimensionswerte aus dem Eingabekontext werden mit dem **Rollenpreisaufschlag** abgegelichen, um den Aufschlagsprozentsatz abzurufen.
    3. Der Aufschlagsprozentsatz aus dem zweiten Schritt wird auf den Basistarif angewendet, der aus der Tabelle **Rollenpreis** aus dem ersten Schritt statt, um die Endpreise/-kosten zu erhalten.
   
   In der folgenden Tabelle wird die Berechnung der Preisaufschläge dargestellt.
  
| Rolle        | Organisationseinheit    |Arbeitsstandort      |Standardtitel      |Arbeitszeiten der Ressource      |  Aufschlag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Koch Indien|Vor Ort            |                    |Überstunden                 |15     |
|             | Koch Indien|Lokal             |                    |Überstunden                 |10     |
|             | Contoso US   |Lokal             |                    |Überstunden                 |20     |


Wenn eine Ressource von Contoso Indien, deren Basistarif 100 USD beträgt, vor Ort arbeitet, und sie 8 Stunden an regulärer Arbeitszeit und 2 Überstunden im Zeiteintrag protokolliert, verwendet die Preis-Engine den Basistarif von 100 für die 8 Stunden, um 800 USD zu erfassen. Für die 2 Überstunden wird ein Aufschlag von 15 % auf den Basistarif von 100 angewendet, um einen Einheitspreis von 115 USD zu erhalten und Gesamtkosten von 230 USD zu erfassen.

### <a name="applicable-to-cost"></a>Gilt für Kosten 
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn die Kosten und Aufschlagsraten abgerufen werden.

### <a name="applicable-to-sales"></a>Gilt für Vertrieb
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn die Rechnung und die Aufschlagsraten abgerufen werden.

### <a name="applicable-to-purchase"></a>Gilt für Einkauf
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn der Einkaufspreis abgerufen wird. Szenarien für die Vergabe werden nicht unterstützt, daher wird dieses Feld nicht verwendet. 

### <a name="priority"></a>Priorität
Das Festlegen der Dimensionspriorität hilfte einen Preis auch dann zu bestimmen, wenn kein genauer Abgleich zwischen den Eingabedimensionswerten und den Werten aus den Tabellen **Rollenpreis** oder **Rollenpreisaufschlag** möglich ist. In diesem Szenario werden Nullwerte bei nicht übereinstimmenden Dimensionswerten verwendet, indem die Dimensionen gemäß ihrer Priorität gewichtet werden.

- **Kostenpriorität** : Der Wert der Kostenpriorität der Dimension gibt die Gewichtung dieser Dimension beim Abgleich mit dem Setup der Einstandspreise an. Der Wert der **Kostenpriorität** muss über alle Dimensionen hinweg einheitlich sein, die den Status **Gilt für Kosten** aufweisen.
- **Vertriebspriorität** : Der Wert der Vertriebspriorität der Dimension gibt die Gewichtung dieser Dimension beim Abgleich mit dem Setup der Verkaufspreise oder Rechnungssätze an. Der Wert der **Vertriebspriorität** muss über alle Dimensionen hinweg einheitlich sein, die den Status **Gilt für Vertrieb** aufweisen.
