---
title: Deaktivieren einer Preisdimension
description: In diesem Thema wird gezeigt, wie Preisdimensionen in der Project Service-Lösung eingerichtet werden.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
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
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014295"
---
# <a name="turn-off-a-pricing-dimension"></a>Deaktivieren einer Preisdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Möglicherweise müssen Sie Ihre Preisstrategie alle paar Jahre überprüfen und aktualisieren. Alle Updates, die Sie vornehmen, erfordern möglicherweise, dass Sie sämtliche vorhandenen Preisdimensionen deaktivieren und eine neue erstellen. Beispielsweise haben Sie möglicherweise die Preise nach **Rolle** festgelegt, aber jetzt haben Sie sich entschieden, die Preise nach **Berufserfahrung** festzulegen. Hierfür müssen sie möglicherweise **Rolle** als Preisdimension deaktivieren und **Berufserfahrung** als neue Preisdimension erstellen. 

Das Deaktivieren einer Preisdimension, unabhängig davon, ob sie vorkonfiguriert oder benutzerdefiniert ist, kann ausgeführt werden, indem die Felder **Gilt für Kosten** und **Gilt für Vertrieb** der Preisdimension auf **Nein** festgelegt werden.

Dabei erhalten Sie aber möglicherweise die folgende Fehlermeldung.

![Geschäftsprozessfehler wahrscheinlich, wenn eine Preisdimension deaktiviert wird](media/Business-Process-Error.png)


Diese Fehlermeldung gibt an, dass es Preisdatensätze gibt, die zuvor für die Dimension eingerichtet wurden, die gerade deaktiviert wird. Alle **Rollenpreis**- und **Rollenpreisaufschlag**-Datensätze, die auf eine Dimension verweisen, müssen gelöscht werden, bevor die Anwendbarkeit der Dimension auf **Nein** festgelegt werden kann. Diese Regel gilt sowohl für vorkonfigurierte Preisdimensionen als auch für sämtliche benutzerdefinierten Preisdimensionen, die Sie möglicherweise erstellt haben. Der Grund für diese Überprüfung liegt darin, dass Project Service eine Einschränkung hat, dass jeder **Rollenpreis**-Datensatz eine eindeutige Kombination von Dimensionen haben muss. Für eine Preisliste mit der Bezeichnung **US-Kostensätze 2018** haben Sie die folgenden **Rollenpreis**-Zeilen. 

| Standardtitel         | Organisationseinheit    |Einheit   |Preis  |Währung  |
| -----------------------|-------------|-------|-------|----------|
| Systemtechniker|Contoso (USA)|Stunde| 100|US-Dollar|
| Leitender Systemtechniker|Contoso (USA)|Stunde| 150| US-Dollar|


Wenn Sie **Standardtitel** als Preisdimension deaktivieren und das Project Service-Preismodul nach einem Preis sucht, verwendet es nur den Wert **Organisationseinheit** aus dem Eingabekontext. Wenn die **Organisationseinheit** des Eingabekontexts Contoso USA ist, ist das Ergebnis nicht deterministisch, da beide Zeilen übereinstimmen werden. Um dieses Szenario zu vermeiden, wenn Sie **Rollenpreis**-Datensätze erstellen, überprüft Project Service, dass die Kombination der Dimensionen eindeutig ist. Wenn die Dimension deaktiviert wird, nachdem die **Rollenpreis**-Datensätze erstellt sind, kann gegen diese Einschränkung verstoßen werden. Daher ist es erforderlich, dass Sie, bevor Sie eine Dimension deaktivieren, alle **Rollenpreis**- und **Rollenpreisaufschlag**-Zeilen löschen, bei denen dieser Dimensionswert aufgefüllt ist.



[!INCLUDE[footer-include](../includes/footer-banner.md)]