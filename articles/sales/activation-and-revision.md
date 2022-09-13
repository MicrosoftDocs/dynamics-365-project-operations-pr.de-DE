---
title: Projektangebot aktivieren und überarbeiten
description: Dieser Artikel informiert Sie darüber, wie Sie Angebote in Microsoft Dynamics 365 Project Operations aktivieren und überarbeiten können.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410332"
---
# <a name="activate-and-revise-a-project-quote"></a>Projektangebot aktivieren und überarbeiten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Aktivierungs- und Überarbeitungsfunktionen helfen Ihnen, die Versionierung für projektbasierte Angebote während der Kalkulations- und Verhandlungsphase im Auge zu behalten. Wenn ein Angebotsentwurf aktiviert wird, wird er schreibgeschützt.

Mit den Aktivierungs- und Überarbeitungsfunktionen können Sie die folgenden Aufgaben ausführen:

- Gewinnen oder verlieren Sie Angebote erst nach der Aktivierung.
- Überarbeiten Sie ein Angebot, um entweder Änderungen am vorhandenen Angebot vorzunehmen oder eine neue Version zu erstellen.

> [!NOTE]
> Nachdem die Funktion zur Aktivierung und Überarbeitung von Angeboten aktiviert wurde, kann sie nicht mehr deaktiviert werden.

Gehen Sie wie folgt vor, um die Möglichkeit zum Aktivieren und Überarbeiten projektbasierter Angebote zu aktivieren.

1. Gehen Sie zu **Einstellungen** \> **Parameter**.
1. Datensatz **Parameter** öffnen.
1. Klicken Sie im Aktionsbereich auf die Registerkarte **Funktionssteuerung** und wählen Sie **Aktivieren und Überarbeiten von Angeboten aktivieren**.
1. Wählen Sie im Bestätigungsdialogfeld **OK**.
1. Aktualisieren Sie nach einigen Augenblicken Ihren Browser. Aktivierungs- und Überarbeitungsfunktionen sollten jetzt verfügbar sein. Sie werden wissen, dass diese Funktionen aktiviert wurden, wenn die Schaltfläche **Aktivieren und Überarbeiten von Angeboten aktivieren** nicht mehr im Aktivitätsbereich angezeigt.

## <a name="activating-a-quote"></a>Ein Angebot aktivieren

Nachdem die Funktion zur Aktivierung und Überarbeitung von Angeboten aktiviert wurde, werden die Schaltflächen **Angebot als gewonnen schließen** und **Angebot als verloren schließen** im Aktivitätsbereich sind für Projektangebotsentwürfe nicht mehr verfügbar sein. Sie sind erst verfügbar, nachdem ein Angebot aktiviert wurde.

Die Aktivierung stellt die Phase im Angebotsprozess dar, in der Sie weitere Änderungen am Angebot verhindern möchten. In dieser Phase wird das Angebot zur internen Überprüfung oder an den Kunden gesendet.

Die Schaltflächen **Angebot als gewonnen schließen** und **Angebot als verloren schließen** im Aktionsbereich sind für aktivierte Angebote verfügbar. Abhängig vom Ergebnis der internen oder Kundenbewertung können Sie eine dieser Schaltflächen verwenden, um ein aktiviertes Angebot zu schließen. Sie können Verhandlungen und Änderungen an aktivierten Angeboten vornehmen, indem Sie **Angebot überarbeiten** auswählen.

## <a name="revising-a-quote"></a>Ein Angebot überarbeiten

Wenn Sie Änderungen an einem aktivierten Angebot vornehmen müssen, wählen Sie **Angebot überarbeiten** aus. Das Angebot ist geschlossen, und der **überarbeitet** Ursachencode wird verwendet. Dann wird ein neues Angebot erstellt, das dieselbe ID und einer höheren Revisionsnummer hat. Alle Details aus dem ursprünglichen Angebot werden in das neue Angebot kopiert. Das neue Angebot befindet sich im Entwurfsstatus und kann nach Bedarf bearbeitet werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
