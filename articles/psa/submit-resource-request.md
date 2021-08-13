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
ms.openlocfilehash: da3e2798079816409ffbcfed911c05f3d51307fef22c48d112802927828faeb2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985005"
---
# <a name="submitting-a-resource-request"></a>Übermitteln einer Ressourcenanforderung

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.

1. Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**, um eine Liste der buchbaren Ressourcen anzuzeigen. 
2. Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanfrage aus der Liste enthält, und klicken Sie dann auf **Anforderung übermitteln**.

![Übermitteln einer Ressourcenanforderung.](media/RM-how-to-18.png)

Der Anforderungsstatus des generischen Teammitglieds ändert sich auf **Gesendet**.

Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt. Andernfalls verbleibt die allgemeine Ressource im Team und der Anforderungsstatus wird in **Prüfung erforderlich** geändert, falls der Resource Manager eine benannte Ressource vorschlägt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]