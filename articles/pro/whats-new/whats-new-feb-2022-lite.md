---
title: Was ist neu für Februar 2022 – Bereitstellung von Project Operations Lite
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Project Operations im Februar 2022 zur Verfügung stehen.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922819"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Was ist neu für Februar 2022 – Bereitstellung von Project Operations Lite

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.28.0.120

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Ab dieser Version können Sie einem einzelnen Projekt bis zu 300 Teammitglieder hinzufügen. Bisher war die Anzahl der Teammitglieder auf 150 begrenzt. Weitere Informationen finden Sie unter [Projekt-Limits](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2497369 | Die Materialkorrektur muss dem Datumswert im **Korrektur**-Parameter folgen. |
| Preise und Abrechnung | 2498697 | Verbesserte Sicherheitskonfiguration für **Rückruf des Zeiteintrags**. |
| Preise und Abrechnung | 2517455 | Die **Aktualisierte Rechnungspostenbuchungen**-Aktion darf nicht mehrfach gleichzeitig für dieselbe Rechnung ausgelöst werden. |
| Preise und Abrechnung | 2517465 | Die **Rechnungspostendetails deaktivieren**-Aktion ist blockiert, da sie nicht unterstützt wird. |
| Preise und Abrechnung | 2556660 | Die Datumsgültigkeitsprüfungen, die für die Preisliste durchgeführt werden, die an einen Projektparameterdatensatz angehängt ist, wurde korrigiert. |
| Verkaufschancenmanagement | 2369202 | Die Geschäftslogik wurde korrigiert, die überprüft, ob Preislisten mit sich überschneidenden Gültigkeitsdaten demselben Projektvertrag angehängt werden können. |
| Verkaufschancenmanagement | 2385965 | Das Verhalten auf der **Kunden**-Registerkarte der **Projektvertrag**-Seite wurde korrigiert, wenn Sie **Speichern und schließen** auswählen. |
