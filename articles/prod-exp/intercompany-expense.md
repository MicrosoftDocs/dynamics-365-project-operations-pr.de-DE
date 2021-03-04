---
title: Intercompany-Ausgaben
description: Dieses Thema enthält Informationen zur Nutzung von konzerninternen Ausgaben, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960831"
---
# <a name="intercompany-expenses"></a>Intercompany-Ausgaben

Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen. In dieser Situation können Sie die konzerninterne Ausgaben verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde. Die juristische Person, die den Arbeitnehmer beschäftigt, wird als leihende juristische Person bezeichnet. Die juristische Person, für die dem Arbeitnehmer Kosten entstehen, wird als leihende juristische Person bezeichnet. 

Bevor ein Mitarbeiter konzerninterne Ausgaben erstellen und einreichen kann, müssen Sie konzerninterne Ausgabenzeilen aktivieren. In der ausleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** wählen Sie **Konzerninterne Ausgabenzeilen zulassen**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Steuerbuchung für konzerninterne Ausgaben

[!include [banner](../includes/banner.md)]

Bevor Sie Ihre Steuergruppen verwenden können, die der ausleihenden juristischen Person anstelle der ausleihenden juristischen Person zugeordnet sind, müssen Sie diese auf der Seite Hauptbuchparameter im Inforegister Mehrwertsteuer aktivieren. Wenn der Parameter **Juristische Person für konzerninterne-Steuerbuchungen** auf **Quelle** und das Feld **Mehrwertsteuerregeln anwenden** auf **Nein** festgelegt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet. Wenn der gleiche Parameter auf **Ziel** eingestellt wird, wird die Steuerkombination für die ausleihende juristischen Person verwendet. Wenn der Parameter bei juristischen Personen in den USA auf **Quelle** festgelegt ist, muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert sein. Das Buchhaltungsmodul verwendet die Informationen aus diesem Feld für steuerbezogene Buchhaltungseinträge.   
Das Verhalten ist für Vorkalkulationspositionen konsistent, die mit oder ohne Projekt gebucht wurden.  
