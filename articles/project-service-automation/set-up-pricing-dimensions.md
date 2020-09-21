---
title: Einrichten von benutzerdefinierten Feldern als Preisdimensionen
description: Dieses Thema enthält Informationen zum Einrichten von benutzerdefinierten Preisdimensionen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721954"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Einrichten von benutzerdefinierten Feldern als Preisdimensionen 

Bevor Sie beginnen, wird in diesem Thema davon ausgegangen, dass Sie die Verfahren in den Themen [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities.md) und [Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten](field-references.md) abgeschlossen haben. Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, kehren Sie zurück und schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück. 

Dieses Thema enthält Informationen zum Einrichten von benutzerdefinierten Preisdimensionen. In der Project Service-Weboberfläche werden auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** die Datensätze in den Entitäten der Preisdimensionen angezeigt. Standardmäßig werden durch die Project Service-Installation zwei Zeilen im Raster auf dieser Registerkarte erstellt:

- **msdyn_resourcecategory** (Rolle)
- **msdyn_OrganizationalUnit** (Organisationseinheit)

> [!IMPORTANT]
> Löschen Sie diese Zeilen nicht. Wenn Sie sie jedoch nicht benötigen, können Sie sie in einem bestimmten Kontext als nicht erforderlich festlegen, indem Sie **Gilt für Kosten**, **Gilt für Vertrieb** und **Gilt für Kauf** auf **Nein** setzen. Das Festlegen dieser Attributwerte auf **Nein** hat denselben Effekt, als ob das Feld als Preisdimension nicht vorhanden ist.

Damit ein Feld zu einer Preisdimension wird, muss es:

- als Feld in den Entitäten **Rollenpreis** und **Rollenpreisaufschlag** erstellt werden. Weitere Informationen hierzu erhalten Sie unter [Hinzufügen benutzerdefinierter Felder zum Preis und zu Transaktionsentitäten](field-references.md).
- als Zeile in der Tabelle **Preisdimension** erstellt worden sein. Beispielsweise können Sie Preisdimensionszeilen, wie in der folgenden Grafik dargestellt, hinzufügen. 

![Betragsbasierte Preisdimensionszeilen](media/Amt-based-PD.png)

Beachten Sie, dass die Arbeitszeiten der Ressource (**msdyn_resourceworkhours**) als aufschlagsbasierte Dimension und zum Raster auf der Registerkarte **Aufschlagsbasierte Preisdimension** hinzugefügt wurden.

![Aufschlagsbasierte Preisdimensionszeilen](media/Markup-based-PD.png)

> [!IMPORTANT]
> Jegliche Änderungen an Preisdimensionsdaten in der Tabelle, ob bei vorhandenen oder neuen Daten, werden erst an die Project Service-Geschäftslogik für Preise weitergegeben, wenn der Cache aktualisiert wird. Die Aktualisierungszeit des Cache kann bis zu 10 Minuten betragen. Warten Sie diese Zeit ab, um die Änderungen in der Preis-Standardlogik anzuzeigen, die aus Änderungen an den Preisdimensionsdaten resultieren müssen.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Tabelle mit Attributen der Preisdimensionen
Die folgenden Abschnitte enthalten Informationen zu den verschiedenen Attributen in der Tabelle **Preisdimensionen**.

### <a name="pricing-dimension-name"></a>Preisdimensionsname
Dieser Wert muss genau dem Schemanamen des Feldes entsprechen, das der Tabelle **Rollenpreis** für benutzerdefinierte Preisdimensionen hinzugefügt wurde. Weitere Informationen zum Hinzufügen von Feldern zur Tabelle **Rollenpreis** erhalten Sie unter [Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten](field-references.md).

### <a name="type-of-dimension"></a>Dimensionstyp
Es gibt zwei Arten von Preisdimensionen:
  
  - **Betragsbasierte Dimensionen**: Diese Dimensionswerte aus dem Eingabekontext werden mit den Dimensionswerten in der Position **Rollenpreis** abgeglichen und Preise/Kosten werden standardmäßig der Tabelle **Rollenpreis** entnommen.
  - **Aufschlagsbasierte Dimensionen**: Dies sind Dimensionen, bei denen Project Service den folgenden 3-Schritte-Prozess übernimmt, um Preise/Kosten abzurufen
 
    1. Project Service gleicht die nicht aufschlagsbasierten Dimensionswerte aus dem Eingabekontext mit der Rollenpreisposition ab, um den Basistarif abzurufen.
    2. Project Service gleicht alle Dimensionswerte aus dem Eingabekontext mit der Position **Rollenpreisaufschlag** ab, um den Aufschlagsprozentsatz abzurufen.
    3. Project Service wendet den Aufschlagsprozentsatz aus dem zweiten Schritt auf den im ersten Schritt aus der Tabelle **Rollenpreis** erhaltenen Basistarif an, um die Endpreise/-kosten zu erhalten.
   
   In der folgenden Tabelle wird die Berechnung der Preisaufschläge dargestellt.
  
| Rolle        | Organisationseinheit    |Arbeitsstandort      |Standardtitel      |Arbeitszeiten der Ressource      |  Aufschlag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Koch Indien|Vor Ort            |                    |Überstunden                 |15     |
|             | Koch Indien|Lokal             |                    |Überstunden                 |10     |
|             | Contoso US   |Lokal             |                    |Überstunden                 |20     |


Wenn eine Ressource von Koch, Indien, deren Basistarif 100 USD beträgt, vor Ort arbeitet, und sie 8 Stunden an regulärer Arbeitszeit und 2 Überstunden im Zeiteintrag protokolliert, verwendet die Project Service-Preis-Engine den Basistarif von 100 für die 8 Stunden, um 800 USD zu erfassen. Für die 2 Überstunden wird ein Aufschlag von 15 % auf den Basistarif von 100 angewendet, um einen Einheitspreis von 115 USD zu erhalten und Gesamtkosten von 230 USD zu erfassen.

### <a name="applicable-to-cost"></a>Gilt für Kosten 
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn die Kosten und Aufschlagsraten abgerufen werden.

### <a name="applicable-to-sales"></a>Gilt für Vertrieb
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn die Rechnung und die Aufschlagsraten abgerufen werden.

### <a name="applicable-to-purchase"></a>Gilt für Einkauf
Falls diese Option auf **Ja** eingestellt ist, gibt sie an, dass der Dimensionswert aus dem Eingabekontext verwendet werden sollte, um den **Rollenpreis** und den **Rollenpreisaufschlag** abzugleichen, wenn der Einkaufspreis abgerufen wird. Derzeit unterstützt Project Service keine Szenarien für Unteraufträge. Daher wird dieses Feld nicht verwendet. 

### <a name="priority"></a>Priorität
Das Festlegen der Dimensionspriorität unterstützt Project Service dabei, einen Preis auch dann zu bestimmen, wenn kein genauer Abgleich zwischen den Eingabedimensionswerten und den Werten aus den Tabellen **Rollenpreis** oder **Rollenpreisaufschlag** möglich ist. In diesem Szenario verwendet Project Service Nullwerte bei nicht übereinstimmenden Dimensionswerten, indem die Dimensionen gemäß ihrer Priorität gewichtet werden.

- **Kostenpriorität**: Der Wert der Kostenpriorität der Dimension gibt die Gewichtung dieser Dimension beim Abgleich mit dem Setup der Einstandspreise an. Der Wert der **Kostenpriorität** muss über alle Dimensionen hinweg einheitlich sein, die den Status **Gilt für Kosten** aufweisen.
- **Vertriebspriorität**: Der Wert der Vertriebspriorität der Dimension gibt die Gewichtung dieser Dimension beim Abgleich mit dem Setup der Verkaufspreise oder Rechnungssätze an. Der Wert der **Vertriebspriorität** muss über alle Dimensionen hinweg einheitlich sein, die den Status **Gilt für Vertrieb** aufweisen.
