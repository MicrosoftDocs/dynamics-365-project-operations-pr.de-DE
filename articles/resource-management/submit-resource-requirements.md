---
title: Eine Ressourcenanforderung übermitteln
description: Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076418"
---
# <a name="submit-a-resource-request"></a>Eine Ressourcenanforderung übermitteln

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.

1. Wählen Sie in Dynamics 365 Project Operations auf der Seite **Projekte** die Registerkarte **Team** aus, um eine Liste der buchbaren Ressourcen anzuzeigen. 
2. Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanforderung aus der Liste enthält, und klicken Sie dann auf **Anforderung einreichen**.

Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.

Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt. Wenn der Resource Manager andernfalls einen benannte Ressource vorschlägt, verbleibt die allgemeine Ressource im Team, und der Anforderungsstatus wird in **Prüfung erforderlich** geändert.
