---
title: Deaktivieren einer Preisdimension
description: In diesem Thema wird gezeigt, wie Preisdimensionen in der Project Service-Lösung eingerichtet werden.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722014"
---
# <a name="turn-off-a-pricing-dimension"></a>Deaktivieren einer Preisdimension

Möglicherweise müssen Sie Ihre Preisstrategie alle paar Jahre überprüfen und aktualisieren. Alle Updates, die Sie vornehmen, erfordern möglicherweise, dass Sie sämtliche vorhandenen Preisdimensionen deaktivieren und eine neue erstellen. Beispielsweise haben Sie möglicherweise die Preise nach **Rolle** festgelegt, aber jetzt haben Sie sich entschieden, die Preise nach **Berufserfahrung** festzulegen. Hierfür müssen sie möglicherweise **Rolle** als Preisdimension deaktivieren und **Berufserfahrung** als neue Preisdimension erstellen. 

Das Deaktivieren einer Preisdimension, unabhängig davon, ob sie vorkonfiguriert oder benutzerdefiniert ist, kann ausgeführt werden, indem die Felder **Gilt für Kosten** und **Gilt für Vertrieb** der Preisdimension auf **Nein** festgelegt werden.

Dabei erhalten Sie aber möglicherweise die folgende Fehlermeldung.

![Geschäftsprozessfehler wahrscheinlich, wenn eine Preisdimension deaktiviert wird](media/Business-Process-Error.png)


Diese Fehlermeldung gibt an, dass es Preisdatensätze gibt, die zuvor für die Dimension eingerichtet wurden, die gerade deaktiviert wird. Alle **Rollenpreis**- und **Rollenpreisaufschlag**-Datensätze, die auf eine Dimension verweisen, müssen gelöscht werden, bevor die Anwendbarkeit der Dimension auf **Nein** festgelegt werden kann. Diese Regel gilt sowohl für vorkonfigurierte Preisdimensionen als auch für sämtliche benutzerdefinierten Preisdimensionen, die Sie möglicherweise erstellt haben. Der Grund für diese Überprüfung liegt darin, dass Project Service eine Einschränkung hat, dass jeder **Rollenpreis**-Datensatz eine eindeutige Kombination von Dimensionen haben muss. Für eine Preisliste mit der Bezeichnung **US-Kostensätze 2018** haben Sie die folgenden **Rollenpreis**-Zeilen. 

| Standardtitel         | Organisationseinheit    |Einheit   |Preis  |Währung  |
| -----------------------|-------------|-------|-------|----------|
| Systemtechniker|Contoso US|Hour| 100|USD|
| Leitender Systemtechniker|Contoso US|Hour| 150| USD|


Wenn Sie **Standardtitel** als Preisdimension deaktivieren und das Project Service-Preismodul nach einem Preis sucht, verwendet es nur den Wert **Organisationseinheit** aus dem Eingabekontext. Wenn die **Organisationseinheit** des Eingabekontexts „Contoso US” ist, ist das Ergebnis nicht deterministisch, da beide Zeilen übereinstimmen werden. Um dieses Szenario zu vermeiden, wenn Sie **Rollenpreis**-Datensätze erstellen, überprüft Project Service, dass die Kombination der Dimensionen eindeutig ist. Wenn die Dimension deaktiviert wird, nachdem die **Rollenpreis**-Datensätze erstellt sind, kann gegen diese Einschränkung verstoßen werden. Daher ist es erforderlich, dass Sie, bevor Sie eine Dimension deaktivieren, alle **Rollenpreis**- und **Rollenpreisaufschlag**-Zeilen löschen, bei denen dieser Dimensionswert aufgefüllt ist.

