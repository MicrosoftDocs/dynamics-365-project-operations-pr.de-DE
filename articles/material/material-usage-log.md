---
title: Materialverbrauch für Projekte und Projektaufgaben erfassen
description: Dieses Thema enthält Informationen zum Protokollieren der Materialnutzung für Projekte und Projektaufgaben.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999270"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Materialverbrauch für Projekte und Projektaufgaben erfassen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Während ein Projektteam Aufgaben an einem Projekt bearbeitet, verbraucht oder verwendet es Materialien. Ein Materialverwendungsprotokoll bietet eine Möglichkeit, diese Verwendung aufzuzeichnen, sodass sie vom Projektmanager genehmigt und schließlich dem Kunden in Rechnung gestellt werden kann. 

Gehen Sie folgendermaßen vor, um die Verwendung von Katalog- oder Schreibmaterialien aufzuzeichnen und an den Genehmigenden zu senden: 

1. Wählen Sie im linken Navigationsbereich **Materialverbrauch** aus, und klicken Sie dann auf **Neu**.
2. Auf der Seite **Neuer Materialverbrauch** geben Sie die erforderlichen Materialverwendungsinformationen ein, und wählen Sie dann **Speichern** aus.

Die folgende Tabelle enthält Informationen zu den Feldern auf der **Materialverbrauchsprotokoll**-Seite. 

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Beschreibung | Eine Beschreibung des spezifischen Materialverbrauchs. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Datum | Das Datum, an dem das Material voraussichtlich verwendet wird. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Project | Eine Liste der Projekte, die aktiv sind. | Die Auswahl eines Projekts für ein Materialverwendungsprotokoll wirkt sich auf das **Aufgabe**-Feld aus, sodass nur die Aufgaben angezeigt werden, die sich im Projekt befinden. |
| Aufgabe | Eine Liste der Aufgaben für das Projekt, einschließlich Zusammenfassungs- und Blattknotenaufgaben. | Die Auswahl einer Aufgabe für ein Materialverbrauchsprotokoll wirkt sich auf die tatsächlichen Materialkosten und den tatsächlichen Materialverkauf für eine Aufgabe aus. Wenn dieses Feld leer ist, werden die entsprechenden Materialverbrauchskosten und -verkäufe nur auf Projektebene verfolgt und zusammengefasst. |
| Produkt auswählen | Geben Sie an, ob diese Materialverwendung für ein **Vorhandenes** (Katalog-)Produkt oder ein **Manuell eintragen**-Produkt ist. | Dieses Feld bestimmt den Produkttyp. |
| Produkt | Die ID des Produkts aus dem Produktkatalog. Wenn Sie eine Produkt-ID auswählen, wird das **Produkt auswählen**-Feld automatisch auf **Vorhandenes Produkt** aktualisiert. Die ID wird verwendet, um Kosten und Verkaufspreise aus der Preisliste abzurufen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| WriteIn-Produktbeschreibung | Ein Textfeld zum Schreiben im Namen des Produkts. Dieses Feld ist verfügbar, wenn Sie ein **Manueller Eintrag**-Produkt im **Produkt auswählen**-Feld auswählen.| Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Buchbare Ressource| Ressource, die dieses Material für das Projekt verwendet hat. Die Standardeinstellung für dieses Feld ist die buchbare Ressource des angemeldeten Benutzers. Sie kann jedoch geändert werden, um die Verwendung im Namen anderer Mitglieder des Projektteams aufzuzeichnen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheitengruppe | Der Standardwert in diesem Feld stammt aus der Einheitengruppe, die als Standard für das Katalogprodukt eingerichtet wurde. Sie können dieses Feld aktualisieren, um eine andere Einheitengruppe auszuwählen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheit | Der Standardwert in diesem Feld ist die Standardeinheit des ausgewählten Produkts. Sie können dieses Feld aktualisieren, um eine andere Einheit auszuwählen. | Das Ändern der Einheit führt zu einem anderen Standardeinheitspreis und anderen Kosten. |
| Menge | Die Menge des Produkts, die für das Projekt oder die Projektaufgabe verwendet wurde. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Stückkosten | Die Stückkosten der ausgewählten Produkt- und Stückkombination, wie in der entsprechenden Kostenpreisliste angegeben. | Die Stückkosten werden immer in der Kostenwährung des Projekts angezeigt. Wenn in der Preisliste keine Stückkosten für das Kombinationsprodukt und die Einheit enthalten sind, werden die Stückkosten standardmäßig auf 0,00 gesetzt. |
| Gesamtkosten | Der Kostenbetrag wird als Menge \* Kosten pro Einheit berechnet.| Der Kostenbetrag wird immer in der Kostenwährung des Projekts angezeigt. |


## <a name="submit-material-usage-for-review-and-approval"></a>Senden Sie den Materialverbrauch zur Überprüfung und Genehmigung 
Nachdem Sie Ihren gesamten Materialverbrauch erfasst haben und bereit sind, ihn genehmigen zu lassen, müssen Sie die Nutzungsinformationen zur Überprüfung einreichen.

1. Gehen Sie zu **Materialverbrauchsprotokoll** und wählen Sie einen oder mehrere Einträge aus. Oder wählen Sie alle Materialverbrauchsdatensätze aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.
2. Wählen Sie **Übermitteln** aus. Das System verarbeitet die ausgewählten Einträge und erstellt dann Genehmigungsanforderungen für die Materialverwendung.

## <a name="recall-a-material-usage-log"></a>Ein Materialverbrauchsprotokoll zurückrufen

Bei Bedarf können Sie eine eingereichte Materialverbrauch zurückrufen. Die zum Abrufen eines Materialverbrauchseintrags erforderliche Zeit hängt von der Genehmigungsphase ab.  Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen. Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.

1. Gehen Sie zu **Materialverbrauch** und wählen Sie in der Liste der Materialverwendungsprotokolle die abzurufende Materialverwendung aus.
2. Klicken Sie auf **Zurückrufen**. Wenn der Materialverbrauchseintrag noch nicht genehmigt wurde, ruft das System ihn sofort zurück. Wenn der Materialeintrag bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie den Materialverbrauch zurückrufen möchten. Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.

## <a name="delete-a-material-usage-log"></a>Ein Materialverbrauchsprotokoll löschen

Sie können nicht übermittelte Materialverbrauchsprotokolle löschen. Um ein bereits übermitteltes Materialverbrauchsprotokoll zu löschen, müssen Sie es zunächst zurückrufen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
