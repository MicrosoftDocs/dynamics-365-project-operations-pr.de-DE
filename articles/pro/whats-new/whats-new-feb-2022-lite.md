---
title: Was ist neu für Februar 2022 – Bereitstellung von Project Operations Lite
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom Februar 2022 der Project Operations Lite-Bereitstellung verfügbar sind.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574567"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Was ist neu für Februar 2022 – Bereitstellung von Project Operations Lite

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

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
