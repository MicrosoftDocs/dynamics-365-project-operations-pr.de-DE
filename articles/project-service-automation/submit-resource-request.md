---
title: Eine Ressourcenanforderung übermitteln
description: Dieses Thema enthält Informationen zum Übermitteln einer Anforderung für eine Projektressource.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722021"
---
# <a name="submit-a-resource-request"></a>Eine Ressourcenanforderung übermitteln

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.

1. Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**, um eine Liste der buchbaren Ressourcen anzuzeigen. 
2. Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanfrage aus der Liste enthält, und klicken Sie dann auf **Anforderung übermitteln**.

![Übermitteln einer Ressourcenanforderung](media/RM-how-to-18.png)

Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.

Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt. Andernfalls verbleibt die allgemeine Ressource im Team und der Anforderungsstatus wird in **Prüfung erforderlich** geändert, falls der Resource Manager eine benannte Ressource vorschlägt.
