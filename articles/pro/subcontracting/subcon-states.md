---
title: Statusübergänge bei Fremdarbeit
description: Dieser Artikel erklärt die Statusübergänge eines Untervertrags in Microsoft Dynamics 365 Project Operations, wenn der Untervertrag erstellt, ausgeführt und geschlossen wird.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522888"
---
# <a name="state-transitions-on-a-subcontract"></a>Statusübergänge bei Fremdarbeit 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dieser Artikel erklärt die Statusübergänge eines Untervertrags in Microsoft Dynamics 365 Project Operations. Jeder Status wird entweder als Entwurf, bestätigt, geschlossen oder storniert dargestellt. Das folgende Bild stellt die Statusübergänge dar.

![Fremdarbeit-Statusmodell](../media/SubconStates.png)  

Die folgende Tabelle enthält eine Beschreibung dessen, was die einzelnen Status im Lebenszyklus einer Fremdarbeit in Project Operations darstellen.

| Bundesstaat | Beschreibung des Dataflows | Zulässige Übergänge |
| --- | --- | --- |
| Entwurf | Dies stellt den Ausgangsstatus einer Fremdarbeit dar. Verhandlungen mit dem Anbieter laufen. Die Positionen und Preise können sich ändern. Eine Fremdarbeit in diesem Status kann verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann auch auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann bearbeitet und gelöscht werden. | Bestätigt |
| Bestätigt | Dies stellt die Phase einer Fremdarbeit dar, nachdem die Verhandlungen mit dem Lieferanten über die Preisgestaltung und die zu kaufenden Einzelposten abgeschlossen sind. Die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen dauert jedoch noch an. Eine Fremdarbeit in diesem Status kann verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann auch auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. Mit der Schaltfläche **Abbrechen** können Sie eine bestätigte Fremdarbeit stornieren. Mit der Schaltfläche **Wieder öffnen** können Sie die Fremdarbeit erneut öffnen, um sie wieder in den Status **Entwurf** zu versetzen. Verwenden Sie die Schaltfläche **Schließen**, um eine bestätigte Fremdarbeit zu schließen. | Geschlossen <br> Abgesagt <br> Entwurf |
| Geschlossen | Dies stellt die Phase einer Fremdarbeit dar, wenn die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen abgeschlossen ist. Eine Fremdarbeit in diesem Status kann nicht mehr verwendet werden, um den Projektbedarf an Ressourcen und Materialien zu schätzen und zu besetzen. Es kann außerdem nicht mehr auf Zeit, Kosten und Materialverbrauch in einem Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. | Nein |
| Abgesagt | Dies stellt die Phase einer Fremdarbeit dar, wenn die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen nicht mehr benötigt wird. Eine Fremdarbeit in diesem Status kann nicht verwendet werden, um den Projektbedarf für Ressourcen und Materialien zu schätzen und zu besetzen, noch kann auf Zeit, Kosten und Materialverbrauch für ein Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. | Nein |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
