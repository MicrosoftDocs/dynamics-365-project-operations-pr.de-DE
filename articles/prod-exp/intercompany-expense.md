---
title: Intercompany-Ausgaben
description: In diesem Artikel erfahren Sie, wie Sie mit Intercompany-Aufwendungen die Kosten einer Arbeitskraft der juristischen Entität zuordnen, für die die Arbeit geleistet wurde.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932387"
---
# <a name="intercompany-expenses"></a>Intercompany-Ausgaben

Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen. In dieser Situation können Sie die konzerninterne Ausgaben verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde. Die juristische Person, die den Arbeitnehmer beschäftigt, wird als leihende juristische Person bezeichnet. Die juristische Person, für die dem Arbeitnehmer Kosten entstehen, wird als leihende juristische Person bezeichnet. 

Bevor ein Mitarbeiter konzerninterne Ausgaben erstellen und einreichen kann, müssen Sie konzerninterne Ausgabenzeilen aktivieren. In der ausleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** wählen Sie **Konzerninterne Ausgabenzeilen zulassen**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Steuerbuchung für konzerninterne Ausgaben

[!include [banner](../includes/banner.md)]

Bevor Sie Ihre Steuergruppen verwenden können, die der ausleihenden juristischen Person anstelle der ausleihenden juristischen Person zugeordnet sind, müssen Sie diese auf der Seite Hauptbuchparameter im Inforegister Mehrwertsteuer aktivieren. Wenn der Parameter **Juristische Person für konzerninterne-Steuerbuchungen** auf **Quelle** und das Feld **Mehrwertsteuerregeln anwenden** auf **Nein** festgelegt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet. Wenn der gleiche Parameter auf **Ziel** eingestellt wird, wird die Steuerkombination für die ausleihende juristischen Person verwendet. Wenn der Parameter bei juristischen Personen in den USA auf **Quelle** festgelegt ist, muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert sein. Das Buchhaltungsmodul verwendet die Informationen aus diesem Feld für steuerbezogene Buchhaltungseinträge.   
Das Verhalten ist für Vorkalkulationspositionen konsistent, die mit oder ohne Projekt gebucht wurden.  

## <a name="new-expense-expression-builder"></a>Neuer Builder für Ausgabenausdrücke

Der neue Builder für Ausgabenausdrücke behebt Probleme mit konzerninternen Ausgabenszenarien, die Projekte verwenden. Diese Funktion stellt sicher, dass beim Erstellen einer konzerninternen Ausgabe die Ausgabenrichtlinie korrekt anhand des in der Ausgabenzeile ausgewählten Projekts validiert wird und die Ausgabenabrechnung erfolgreich übermittelt werden kann.

Damit die Funktion zum Erstellen von Ausgabenausdrücken funktioniert, muss sie aktiviert sein. Außerdem sollte die Ausgabenrichtlinie mit einer Projekt-ID eingerichtet werden.

Wenn Sie bereits Richtlinien konfiguriert haben, die die Projekt-ID in der Ausgabenzeile validieren, müssen diese Richtlinien zurückgezogen werden. Anschließend können Sie die Funktion aktivieren und die Richtlinien neu konfigurieren.

Um diese Funktion einzuschalten, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Arbeitsbereiche** \> **Funktionenverwaltung**.
2. Wählen Sie in der Liste **Der neue Builder für Ausgabenausdrücke behebt Probleme mit konzerninternen Ausgabenszenarien, die Projekte verwenden** aus. Wählen Sie dann **Jetzt aktivieren** aus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
