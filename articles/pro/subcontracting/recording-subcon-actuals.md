---
title: Erfassung von Zeit, Ausgaben und Materialverbrauch für Fremdarbeitskomponenten
description: Dieser Artikel erklärt, wie Zeit-, Aufwands- und Materialdatensätze, die für Projekte aus untervergebenen Komponenten erfasst wurden, von Microsoft Dynamics 365 Project Operations verfolgt werden.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261135"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Erfassung von Zeit, Ausgaben und Materialverbrauch für Projekte aus Fremdarbeitskomponenten

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel erklärt, wie Zeit-, Aufwands- und Materialdatensätze, die für Projekte aus untervergebenen Komponenten erfasst wurden, von Microsoft Dynamics 365 Project Operations verfolgt werden.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kostenkalkulation für Fremdarbeitszeit bei Projekten
In Project Operations können Vertragsmitarbeiter die Zeit für Projekte auf ähnliche Weise wie Mitarbeiter erfassen. Bei der Eingabe von Zeit für Projekte und/oder Projektaufgaben kann ein Vertragsarbeiter eine bestimmte Fremdarbeit und eine Fremdarbeitsposition auswählen.

Wenn die von Vertragsarbeitern eingereichte Zeit genehmigt wird, werden die Projektkosten mit dem Einheitskostensatz erfasst, der für diese Vertragsarbeiterressource im Abschnitt **Rollenpreise** der Preisliste „Kauf“ zur Fremdarbeit eingerichtet ist.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kostenkalkulation für Fremdarbeitsausgaben bei Projekten
Beim Erfassen von Ausgaben, die für Projekte angefallen sind, können Sie in der Ausgabenerfassung eine Fremdarbeit und Fremdarbeitsposition auswählen. 

Wenn dieser Ausgabeneintrag eingereicht und genehmigt wird, werden die Ausgabenkosten projektbasiert mit dem Einheitskostensatz erfasst, der für diese Transaktionskategorie im Abschnitt **Kategoriepreise** der Preisliste „Kauf“ zur Fremdarbeit eingerichtet ist.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kostenkalkulation für Fremdarbeitsmaterialien bei Projekten
Beim Erfassen von Materialverbrauch, der für Projekte angefallen ist, können Sie im Materialverbrauchsprotokoll eine Fremdarbeit und Fremdarbeitsposition auswählen. Wenn das Materialverbrauchsprotokoll eingereicht und genehmigt wird, werden die Materialkosten projektbasiert mit dem Einheitskostensatz erfasst, der für dieses Produkt im Abschnitt **Preislistenelemente** der Preisliste für Fremdarbeit eingerichtet ist.

Der Materialverbrauch kann auch für manuell einzutragende Produkte in Projekten erfasst werden. Diese Art der Materialverwendung kann auch mit einer Fremdarbeit und einer Fremdarbeitsposition verknüpft werden. Bei der Erfassung des Materialverbrauchs für manuell einzutragende Produkte müssen Sie die Stückkosten des manuell einzutragenden Produkts eingeben. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
