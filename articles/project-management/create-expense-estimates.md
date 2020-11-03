---
title: Ausgabenschätzungen
description: Dieses Thema enthält Informationen zum Definieren oder Kalkulieren projektbasierter Ausgaben.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076446"
---
# <a name="expense-estimates"></a>Ausgabenschätzungen
_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mit Dynamics 365 Project Operations können Projektmanager nicht nur ressourcenbasierte Schätzungen definieren, sondern auch projektbasierte Ausgaben für jedes Projekt definieren. Jeder Ausgabenposten kann einer bestimmten Projektaufgabe oder Ausgabenkategorie zugeordnet werden. Ausgabenkategorien werden normalerweise auf organisatorischer Ebene definiert. Die Preisgestaltung für jede Ausgabenkategorie wird normalerweise in der folgenden Hierarchie definiert:

- Organisation
- Kunde
- Angebot/Vertrag

Führen Sie die folgenden Schritte aus, um Projektkosten anzuzeigen, hinzuzufügen oder zu löschen.

1. Wechseln Sie zu **Projekte** und wählen Sie das Projekt aus, an dem Sie arbeiten möchten.
2. Wählen Sie die Registerkarte **Projektschätzungen** aus und zeigen Sie die Liste der Projektkosten an.
3. Wählen Sie **Neue Ausgabe** aus, um eine neue Ausgabe hinzuzufügen. Oder wählen Sie eine zu löschende Ausgabe aus und wählen Sie dann **Ausgabe löschen**.

Die folgenden Attribute sind für jede Ausgabenposition definiert:

- **Kategorie** : Die gemeinsamen Gruppierungen, mit denen alle für ein Projekt anfallenden Ausgaben beschrieben werden.
- **Anfangsdatum** : Das Datum, an dem die Ausgaben voraussichtlich anfallen werden.
- **Menge** : Die geschätzte Anzahl von Ausgabenposten für eine bestimmte Kategorie.
- **Stückpreis** : Der Einheitspreis, der zur Berechnung der Ausgabenkosten verwendet wird.
- **Stückverkaufspreis** : Der Einheitspreis, der zur Berechnung des Verkaufspreises verwendet wird.

