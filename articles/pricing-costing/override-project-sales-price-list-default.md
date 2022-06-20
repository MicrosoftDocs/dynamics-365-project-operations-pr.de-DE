---
title: Standardeinstellungen für Projektvertriebs-Preislisten außer Kraft setzen
description: In diesem Artikel erfahren Sie, wie Sie angepasste Verkaufspreislisten erstellen.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911917"
---
# <a name="override-project-sales-price-lists"></a>Standardeinstellungen für Projektvertriebs-Preislisten außer Kraft setzen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="customer-specific-project-price-lists"></a>Kundenspezifische Projektpreislisten

Kundenspezifische Preisvereinbarungen können als Projektpreislisten in einem Kontodatensatz in Dynamics 365 Project Operations eingerichtet werden.

Um eine kundenspezifische Projektpreisliste einzurichten, navigieren Sie im Bereich **Vertrieb** zum Kontodatensatz.

1. Öffnen Sie die **Konten**-Listenseite.
2. Suchen Sie einen Kundendatensatz und doppelklicken Sie darauf, um die **Konto**-Detailseite zu öffnen.
3. Wählen Sie auf der **Projektpreislisten**-Registerkarte **+ Neue Projektpreisliste hinzufügen**.
4. Auf der Seite **Neue Projektpreisliste** wählen Sie eine Preisliste aus der Dropdown-Liste aus. Nur Preislisten, für die der Kontext auf **Vertrieb** festgelegt ist und deren Währung mit der Kontowährung übereinstimmt, sind enthalten.
5. Geben Sie einen Namen für die Zuordnung ein, und wählen Sie **Speichern** aus. Es wird eine kundenspezifische Projektpreisliste erstellt. Diese Preisliste wird verwendet, um Projektpreise für Projektangebote oder Verträge, die für diesen Kunden erstellt wurden, als Standard festzulegen, wenn das Erstellungsdatum des Angebots oder des Projektvertrags innerhalb des Datums der Gültigkeitsdauer der Preisliste liegt.

## <a name="custom-pricing-on-project-quotes"></a>Benutzerdefinierte Preisgestaltung für Projektangebote

In Projektangeboten können Sie Projektpreise festlegen, die mit einer Standardpreisliste beginnen, die standardmäßig vom Kunden oder von den Projektparametern verwendet wird.

Wenn Sie benutzerdefinierte Preise für projektbezogene Arbeiten an einem bestimmten Angebot benötigen, können Sie diese aus den zugehörigen Entitäten der Projektpreislisten abrufen.

Führen Sie die folgenden Schritte aus, um die angebotsspezifische Projektpreisgestaltung einzurichten.

1. Öffnen Sie im Projektangebot die Registerkarte **Projektpreislisten**.
2. Wählen Sie im Untergitter **Benutzerdefinierte Preisberechnung erstellen**.

Alle dem Angebot beigefügten Projektpreislisten werden in neue Preislisten kopiert. Die Namen der neuen Preislisten geben den Namen des Angebots mit einem Datums-/Zeitstempel für die Erstellung dieser Preislisten wieder.

Sie können jede dieser Preislisten verwenden und die Preise für Arbeit (Rollenpreis) und Kosten (Kategoriepreis) aktualisieren. Diese Preise gelten nur für dieses Projektangebot.

## <a name="price-lists-on-a-project-contract"></a>Preislisten in einem Projektvertrag

Bei einem Projektvertrag wird die Projektpreisgestaltung standardmäßig immer als benutzerdefinierte Preisliste mit dem Namen des Vertrags und dem an den Namen angehängten erstellten Datums- und Zeitstempel verwendet. Dies gilt unabhängig davon, ob der Vertrag zum Zeitpunkt des Gewinns des Angebots erstellt wurde oder ob der Vertrag von Grund auf neu erstellt wurde. Bei Bedarf können Sie diese Zuordnung zur benutzerdefinierten Preisliste entfernen und stattdessen dem Projektvertrag eine Standardpreisliste zuordnen.

Wenn Sie den Projektpreislisten auf Angebot oder Vertrag eine Standardpreisliste zuordnen, wirken sich Änderungen an den Preisen in der Preisliste auf alle Angebote und Verträge aus, die die Preisliste verwenden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]