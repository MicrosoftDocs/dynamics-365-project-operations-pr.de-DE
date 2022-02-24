---
title: Eine Ressourcenanforderung übermitteln
description: Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128822"
---
# <a name="submit-a-resource-request"></a>Eine Ressourcenanforderung übermitteln

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.

1. Wählen Sie in Dynamics 365 Project Operations auf der Seite **Projekte** die Registerkarte **Team** aus, um eine Liste der buchbaren Ressourcen anzuzeigen. 
2. Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanforderung aus der Liste enthält, und klicken Sie dann auf **Anforderung einreichen**.

Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.

Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt. Wenn der Resource Manager andernfalls einen benannte Ressource vorschlägt, verbleibt die allgemeine Ressource im Team, und der Anforderungsstatus wird in **Prüfung erforderlich** geändert.
