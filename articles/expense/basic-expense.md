---
title: Ausgabeneintrag (Lite)
description: Dieses Thema enthält Informationen zum Arbeiten mit Ausgabeneintrag in einer Lite-Bereitstellung.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 774bf2f8f54d2e314740fbad40ea15ce83d38297
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578339"
---
# <a name="expense-entry-lite"></a>Ausgabeneintrag (Lite)

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Basic oder Lite, die Ausgabenverwaltung ist die Fähigkeit, einfache Ausgaben zu erfassen. Sie können Ausgaben für ein Projekt erfassen, und der Projektgenehmiger überprüft und genehmigt sie.

Weitere Informationen zu Kostenfunktionen in Dynamics 365 Project Operations finden Sie unter [Ausgaben – Übersicht](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Eine Grundausgabe erfassen

Sie können Ihre Ausgaben erfassen, um sie dem Genehmigenden vorzulegen.

1. Wechseln Sie zu **Spesen**, und wählen Sie dann **Neu** aus.
2. Geben Sie auf der Seite **Neue Ausgabe** die erforderlichen Ausgabeinformationen ein, und wählen Sie **Speichern**.

## <a name="submit-a-basic-expense"></a>Eine Grundausgabe einreichen

Nachdem Sie alle Ihre Ausgaben erfasst haben und bereit sind, sie genehmigen zu lassen, müssen Sie sie einreichen.

1. Wechseln Sie zu **Spesen**, und wählen Sie dann die Spesen aus. Oder wählen Sie alle Spesen aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.
2. Wählen Sie **Übermitteln** aus. Das System verarbeitet die ausgewählten Einträge und erstellt dann Kostengenehmigungsanforderungen.

## <a name="add-an-attachment"></a>Anlage hinzufügen

Möglicherweise müssen Sie dem Genehmigenden zusätzliche Unterlagen zu Ihren Ausgaben vorlegen. Sie können eine Quittung in der Zeitleiste der Spesenbuchung anhängen. Wählen Sie **Bearbeiten** und im Bereich **Zeitleiste** dann das Büroklammersymbol aus, um Ihre Quittung anzuhängen.

## <a name="recall-a-basic-expense"></a>Eine Grundausgabe zurückrufen

Wenn Sie versehentlich eine Ausgabe einreichen, können Sie diese zurückrufen. Die Zeit, die erforderlich ist, um eine Spesenabrechnung zurückzurufen, hängt von der Genehmigungsphase ab.  Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen. Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.

1. Wählen Sie **Spesen** und dann in der Liste der Spesen die Spesen zum Zurückrufen aus.
2. Wählen Sie **Zurückrufen** aus. Wenn die Spesenerfassung noch nicht genehmigt wurde, ruft das System sie sofort zurück. Wenn die Spesenbuchung bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie die Spesen stornieren möchten. Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.

## <a name="delete-a-basic-expense"></a>Eine Grundausgabe löschen

Noch nicht eingereichte Ausgaben können gelöscht werden. Um eine bereits eingereichte Ausgabe zu löschen, müssen Sie sie zunächst zurückrufen.

## <a name="see-also"></a>Siehe auch

- [Genehmigungen – Übersicht](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]