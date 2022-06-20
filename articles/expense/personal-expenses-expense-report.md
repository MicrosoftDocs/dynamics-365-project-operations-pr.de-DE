---
title: Mit persönliche Ausgaben in einer Ausgabenabrechnung arbeiten
description: Dieser Artikel beschreibt, wie Sie mit persönlichen Ausgaben arbeiten können, die Mitarbeitern auf Geschäftsreisen entstehen.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 1cda5151a32482f92c69402bcc0056d7b6572db8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922267"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Mit persönliche Ausgaben in einer Ausgabenabrechnung arbeiten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Gelegentlich können Mitarbeiter ihre Firmenkreditkarte für persönliche Ausgaben während den Geschäftsreisen belasten. Wenn Sie keinen Prozess für die Behandlung persönlicher Ausgaben beim Einreichen detaillierter Ausgabenabrechnungen durch Mitarbeiter definieren, kann der Genehmigungsprozess für Ausgabenabrechnungen unterbrochen werden.

Es gibt zwei Methoden, mit denen Sie mit den persönlichen Ausgaben eines Mitarbeiters arbeiten können:

  - **Auf Kosten des Mitarbeiters**: Ihre Organisation zahlt keine persönlichen Ausgaben, die auf der Rechnung für die Firmenkreditkarte angegeben sind. Stattdessen bezahlt der Mitarbeiter den Kreditkartenanbieter direkt für die Ausgaben. 
  - **Von der Firma bezahlt**: Ihre Organisation bezahlt die vollständige Rechnung für die Firmenkreditkarte und belastet dann die persönlichen Ausgaben vom Konto des Arbeitnehmers.

Sie können die Methode auswählen, die Ihre Organisation für die Seite **Spesenverwaltungsparameter** verwendet.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Aktivieren Sie die Aufteilungsausgabenfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat

Das Merkmal **Aktivieren Sie die Ausgabenaufteilungsfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat** gilt nur für Ausgabenabrechnungen, die mit einem Workflow auf Zeilenebene genehmigt wurden. Berichte werden genehmigt, indem Sie zu **Ausgabenabrechnungen verarbeiten** > **Mir zugewiesene Ausgabenabrechnungen** > **Ausgabenabrechnung öffnen** gehen. 

Um diese Funktion zu aktivieren, gehen Sie zu **Arbeitsbereiche** > **Funktionsverwaltung**, wählen **Aktivieren Sie die Aufteilungsfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat**, und wählen Sie dann **Jetzt aktivieren**. 

Wenn die Funktion aktiviert ist, generieren Ausgabenzeilen, die diese Funktion verwenden, beim Senden des Berichts zwei Zeilen. Es werden zwei Zeilen generiert, damit der Genehmiger jede Zeile separat genehmigen kann.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
