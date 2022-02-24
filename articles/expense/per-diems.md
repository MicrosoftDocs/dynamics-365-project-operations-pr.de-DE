---
title: Pro Tag
description: Dieses Thema enthält Informationen zu den Tagessatzregeln, die in der Ausgabenverwaltung verwendet werden.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128507"
---
# <a name="per-diems"></a>Pro Tag

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Ein Tagessatz ist eine Zulage, die an einen Arbeitnehmer gezahlt wird, der zur Arbeit reist. In der Ausgabenverwaltung können Sie Tagessatzregeln für verschiedene Reisesituationen erstellen. Die Tagessätze können auf der Jahreszeit, dem Reiseort oder beiden basieren. Wenn Sie eine Tagessatzregel erstellen, können Sie festlegen, dass ein Prozentsatz des Tagessatzes einbehalten wird, wenn ein Mitarbeiter kostenlose Mahlzeiten oder Dienstleistungen erhält. Sie können auch eine minimale und maximale Anzahl von Stunden festlegen, für die der Tagessatz für die Reise eines Arbeitnehmers gelten kann.

## <a name="configuration"></a>Konfiguration 

1. Um Tagessätze hinzuzufügen, gehen Sie zu **Einrichten** > **Berechnungen und Codes** > **Tagessatz (Lagerplätze)**.
2. Wählen Sie für jeden der oben hinzugefügten Standorte einen Tagessatz und eine Währung aus, die zwischen einem bestimmten Start- und Enddatum für Hotel, Mahlzeiten und andere Ausgaben gültig sind. Tagessätze und Währungen werden unter **Einrichten** > **Berechnungen und Codes** > **Tagessätze** konfiguriert.
3. Konfigurieren Sie auf der Seite **Tagessatz (Lagerplätze)** die Tagessatzstufen. Mit den Tagessatzstufen können Sie die prozentuale Aufteilung eines Tagegelds für Hotel-, Verpflegungs- und andere Ausgaben festlegen. 
4. Um die prozentuale Aufteilung der Mahlzeit für Frühstück, Mittag- oder Abendessen festzulegen, aktualisieren Sie die Felder auf der Seite **Ausgabenverwaltungsparameter** auf der Registerkarte **Pro Tag**. 
    
## <a name="submit-expenses-using-per-diem"></a>Ausgaben mit „Pro Tag“ einreichen
Um Ausgaben mit Tagessätzen einzureichen, verwenden Sie die Ausgabenkategorie **Pro Tag**, wenn Sie eine Spesenabrechnung erstellen. Geben Sie **Tagessatz von Datum**, **Tagessatz bis Datum** und **Tagessatz (Lagerplätze)** ein. Der Betrag wird basierend auf den Tagessätzen für den ausgewählten Standort berechnet, und die Reduzierung der Mahlzeiten wird basierend auf den Tagessätzen berechnet.
