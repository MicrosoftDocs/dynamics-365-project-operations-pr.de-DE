---
title: Eine Preisdimension deaktivieren
description: Dieses Thema enthält Informationen zum Deaktivieren von benutzerdefinierten Preisdimensionen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896505"
---
# <a name="turning-off-a-pricing-dimension"></a>Eine Preisdimension deaktivieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Möglicherweise müssen Sie Ihre Preisstrategie alle paar Jahre überprüfen und aktualisieren. Alle Updates, die Sie vornehmen, erfordern möglicherweise, dass Sie sämtliche vorhandenen Preisdimensionen deaktivieren und eine neue erstellen. Beispielsweise haben Sie möglicherweise die Preise nach **Rolle** festgelegt, aber jetzt haben Sie sich entschieden, die Preise nach **Berufserfahrung** festzulegen. Hierfür müssen sie möglicherweise **Rolle** als Preisdimension deaktivieren und **Berufserfahrung** als eine neue Preisdimension erstellen. 

Das Deaktivieren einer Preisdimension, unabhängig davon, ob sie vorkonfiguriert oder benutzerdefiniert ist, kann ausgeführt werden, indem die Felder **Gilt für Kosten** und **Gilt für Vertrieb** der Preisdimension auf **Nein** festgelegt werden.

Wenn Sie dies jedoch tun, erhalten Sie möglicherweise die Fehlermeldung: **Die Preisdimension kann nicht aktualisiert oder gelöscht werden, wenn Preisdatensätze zugeordnet sind.**

Diese Fehlermeldung gibt an, dass es Preisdatensätze gibt, die zuvor für die Dimension eingerichtet wurden, die gerade deaktiviert wird. Alle **Rollenpreis**- und **Rollenpreisaufschlag**-Datensätze, die auf eine Dimension verweisen, müssen gelöscht werden, bevor die Anwendbarkeit der Dimension auf **Nein** festgelegt werden kann. Diese Regel gilt sowohl für vorkonfigurierte Preisdimensionen als auch für sämtliche benutzerdefinierten Preisdimensionen, die Sie möglicherweise erstellt haben. Der Grund für diese Überprüfung liegt darin, dass jeder **Rollenpreis**-Datensatz eine eindeutige Kombination von Dimensionen haben muss. Für eine Preisliste mit der Bezeichnung **US-Kostensätze 2018** haben Sie die folgenden **Rollenpreis**-Zeilen. 

| Standardtitel         | Organisationseinheit    |Einheit   |Preis  |Währung  |
| -----------------------|-------------|-------|-------|----------|
| Systemtechniker|Contoso US|Hour| 100|USD|
| Leitender Systemtechniker|Contoso US|Hour| 150| USD|


Wenn Sie **Standardtitel** als Preisdimension deaktivieren und das Preismodul nach einem Preis sucht, verwendet es nur den Wert **Organisationseinheit** aus dem Eingabekontext. Wenn die **Organisationseinheit** des Eingabekontexts „Contoso US” ist, ist das Ergebnis nicht deterministisch, da beide Zeilen übereinstimmen werden. Um dieses Szenario zu vermeiden, wenn Sie **Rollenpreis**-Datensätze erstellen, überprüft das System, dass die Kombination der Dimensionen eindeutig ist. Wenn die Dimension deaktiviert wird, nachdem die **Rollenpreis**-Datensätze erstellt sind, kann gegen diese Einschränkung verstoßen werden. Daher ist es erforderlich, dass Sie, bevor Sie eine Dimension deaktivieren, alle **Rollenpreis**- und **Rollenpreisaufschlag**-Zeilen löschen, bei denen dieser Dimensionswert aufgefüllt ist.