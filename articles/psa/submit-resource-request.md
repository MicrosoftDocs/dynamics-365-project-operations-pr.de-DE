---
title: Übermitteln einer Ressourcenanforderung
description: Dieses Thema enthält Informationen zum Übermitteln einer Anforderung für eine Projektressource.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013170"
---
# <a name="submitting-a-resource-request"></a>Übermitteln einer Ressourcenanforderung

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.

1. Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**, um eine Liste der buchbaren Ressourcen anzuzeigen. 
2. Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanfrage aus der Liste enthält, und klicken Sie dann auf **Anforderung übermitteln**.

![Übermitteln einer Ressourcenanforderung](media/RM-how-to-18.png)

Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.

Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt. Andernfalls verbleibt die allgemeine Ressource im Team und der Anforderungsstatus wird in **Prüfung erforderlich** geändert, falls der Resource Manager eine benannte Ressource vorschlägt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]