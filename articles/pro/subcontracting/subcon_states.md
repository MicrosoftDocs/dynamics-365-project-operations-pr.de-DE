---
title: Statusübergänge bei einer Fremdarbeit in Project Operations
description: Dieses Thema erklärt die Statusübergänge bei Fremdarbeit in Microsoft Dynamics 365 Project Operations, während die Fremdarbeit angelegt, ausgeführt und geschlossen wird.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902862"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Statusübergänge bei einer Fremdarbeit in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema erklärt die Statusübergänge bei einer Fremdarbeit in Microsoft Dynamics 365 Project Operations. Jeder Status wird entweder als Entwurf, bestätigt, geschlossen oder storniert dargestellt. Das folgende Bild stellt die Statusübergänge dar.

![Fremdarbeit-Statusmodell](../media/SubconStates.png)  

Die folgende Tabelle enthält eine Beschreibung dessen, was die einzelnen Status im Lebenszyklus einer Fremdarbeit in Project Operations darstellen.

| Bundesstaat | Beschreibung des Dataflows | Zulässige Übergänge |
| --- | --- | --- |
| Entwurf | Dies stellt den Ausgangsstatus einer Fremdarbeit dar. Verhandlungen mit dem Anbieter laufen. Die Positionen und Preise können sich ändern. Eine Fremdarbeit in diesem Status kann verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann auch auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann bearbeitet und gelöscht werden. | Bestätigt |
| Bestätigt | Dies stellt die Phase einer Fremdarbeit dar, nachdem die Verhandlungen mit dem Lieferanten über die Preisgestaltung und die zu kaufenden Einzelposten abgeschlossen sind. Die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen dauert jedoch noch an. Eine Fremdarbeit in diesem Status kann verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann auch auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. Mit der Schaltfläche **Abbrechen** können Sie eine bestätigte Fremdarbeit stornieren. Mit der Schaltfläche **Wieder öffnen** können Sie die Fremdarbeit erneut öffnen, um sie wieder in den Status **Entwurf** zu versetzen. Verwenden Sie die Schaltfläche **Schließen**, um eine bestätigte Fremdarbeit zu schließen. | Geschlossen <br> Abgesagt <br> Entwurf |
| Geschlossen | Dies stellt die Phase einer Fremdarbeit dar, wenn die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen abgeschlossen ist. Eine Fremdarbeit in diesem Status kann nicht mehr verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann außerdem nicht mehr auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. | Nein |
| Abgesagt | Dies stellt die Phase einer Fremdarbeit dar, wenn die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen nicht mehr benötigt wird. Eine Fremdarbeit in diesem Status kann nicht verwendet werden, um den Projektbedarf für Ressourcen und Materialien zu schätzen und zu besetzen, noch kann auf Zeit, Kosten und Materialverbrauch für ein Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. | Nein |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
