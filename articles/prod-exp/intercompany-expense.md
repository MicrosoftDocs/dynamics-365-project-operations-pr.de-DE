---
title: Intercompany-Ausgaben
description: Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen. In dieser Situation können Sie die konzerninterne Kostenfunktion verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076675"
---
# <a name="intercompany-expenses"></a>Intercompany-Ausgaben

[!include [banner](../includes/banner.md)]

Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen. In dieser Situation können Sie die konzerninterne Kostenfunktion verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde. Die juristische Person, die den Arbeitnehmer beschäftigt, wird als leihende juristische Person bezeichnet. Die juristische Person, für die dem Arbeitnehmer Kosten entstehen, wird als leihende juristische Person bezeichnet. 

Bevor ein Arbeitnehmer Ausgaben für Arbeiten erstellen und einreichen kann, die für eine andere juristische Person ausgeführt werden, wählen Sie in der ausleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** die Option **Konzerninterne Ausgabenpositionen zulassen** aus. 

## <a name="tax-posting-for-intercompany-expenses"></a>Steuerbuchung für konzerninterne Ausgaben

[!include [banner](../includes/banner.md)]

Wenn Sie in Ihrer Spesenabrechnung Steuergruppen verwenden möchten, die der juristischen Person des Darlehens (Quelle) anstelle der juristischen Person des Darlehens (Ziel) zugeordnet sind, müssen Sie dies in der eingerichteten Umsatzsteuer der Finanzbuchhaltung konfigurieren. Wenn der Parameter der Finanzbuchhaltung **Juristische Person für innerbetriebliche Steuerbuchungen** auf **Quelle** und **Mehrwertsteuerregeln anwenden** auf **Nein** eingestellt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet. Wenn der gleiche Parameter auf **Ziel** eingestellt wird, wird die Steuerkombination für die ausleihende juristischen Person verwendet. Wenn der Parameter bei juristischen Personen in den USA auf **Quelle** festgelegt ist, muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert sein. Das Buchhaltungsmodul verwendet die Informationen aus diesem Feld für steuerliche Buchhaltungseinträge.   
Das Verhalten ist für Vorkalkulationspositionen konsistent, die mit oder ohne Projekt gebucht wurden.  
