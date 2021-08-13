---
title: Mit persönliche Ausgaben in einer Ausgabenabrechnung arbeiten
description: Dieses Thema enthält Informationen zum Umgang mit persönlichen Ausgaben, die Mitarbeitern auf Geschäftsreisen entstehen.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993150"
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
