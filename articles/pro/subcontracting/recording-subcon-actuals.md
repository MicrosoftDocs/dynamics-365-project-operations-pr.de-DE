---
title: Erfassung von Zeit, Ausgaben und Materialverbrauch für Fremdarbeitskomponenten
description: Dieser Artikel erklärt, wie Zeit-, Aufwands- und Materialdatensätze, die für Projekte aus untervergebenen Komponenten erfasst wurden, von Microsoft Dynamics 365 Project Operations verfolgt werden.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522512"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Erfassung von Zeit, Ausgaben und Materialverbrauch für Projekte aus Fremdarbeitskomponenten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

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
