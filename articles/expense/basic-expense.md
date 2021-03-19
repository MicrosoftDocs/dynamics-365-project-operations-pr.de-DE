---
title: Ausgabeneintrag (Lite)
description: Dieses Thema enthält Informationen zum Arbeiten mit Ausgabeneintrag in einer Lite-Bereitstellung.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276752"
---
# <a name="expense-entry-lite"></a>Ausgabeneintrag (Lite)

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Basic oder Lite, die Ausgabenverwaltung ist die Fähigkeit, einfache Ausgaben zu erfassen. Sie können Ausgaben gegen ein Projekt aufzeichnen, und der Projektgenehmiger wird sie dann überprüfen und genehmigen.

Weitere Informationen zu Kostenfunktionen in Dynamics 365 Project Operations finden Sie unter [Ausgaben – Übersicht](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Eine Grundausgabe erfassen

Sie können Ihre Ausgaben erfassen, um sie dem Genehmigenden vorzulegen.

1. Wechseln Sie zu **Ausgaben** und wählen Sie **Neu**.
2. Geben Sie auf der Seite **Neue Ausgabe** die erforderlichen Ausgabeinformationen ein, und wählen Sie **Speichern**.

## <a name="submit-a-basic-expense"></a>Eine Grundausgabe einreichen

Nachdem Sie alle Ihre Ausgaben erfasst haben und bereit sind, sie genehmigen zu lassen, müssen Sie sie einreichen.

1. Wechseln Sie zu **Ausgaben** und wählen Sie eine Ausgabe. Oder wählen Sie alle Ausgaben aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.
2. Wählen Sie **Übermitteln** aus. Das System verarbeitet die ausgewählten Einträge und erstellt dann Kostengenehmigungsanforderungen.

## <a name="add-an-attachment"></a>Anlage hinzufügen

Möglicherweise müssen Sie dem Genehmigenden zusätzliche Unterlagen zu Ihren Ausgaben vorlegen. Sie können eine Quittung in der Zeitleiste der Spesenbuchung anhängen. Wählen Sie **Bearbeiten** und im Bereich **Zeitleiste** dann das Büroklammersymbol aus, um Ihre Quittung anzuhängen.

## <a name="recall-a-basic-expense"></a>Eine Grundausgabe zurückrufen

Wenn Sie versehentlich eine Ausgabe einreichen, können Sie diese zurückrufen. Die Zeit, die erforderlich ist, um eine Ausgabenabrechnung zurückzurufen, hängt von der Genehmigungsphase ab.  Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen. Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.

1. Wechseln Sie zu **Ausgaben** und wählen Sie dann in der Liste der Ausgaben die zurückzurufende Ausgaben aus.
2. Klicken Sie auf **Zurückrufen**. Wenn der Ausgabeneintrag noch nicht genehmigt wurde, ruft das System sie sofort zurück. Wenn der Ausgabeneintrag bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie die Ausgabe stornieren möchten. Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.

## <a name="delete-a-basic-expense"></a>Eine Grundausgabe löschen

Noch nicht eingereichte Ausgaben können gelöscht werden. Um eine bereits eingereichte Ausgabe zu löschen, müssen Sie sie zunächst zurückrufen.

## <a name="see-also"></a>Siehe auch

- [Genehmigungen – Übersicht](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]