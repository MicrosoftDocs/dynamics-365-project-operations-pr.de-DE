---
title: Zulieferer als buchbare Ressourcen einrichten
description: Dieser Artikel erläutert, wie Sie Ressourcen für Unterauftragnehmer, die aus Benutzern und Kontakten im System erstellt werden, festlegen und pflegen, damit sie mit Unteraufträgen in Microsoft Dynamics 365 Project Operations verknüpft werden können.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522700"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Zulieferer als buchbare Ressourcen einrichten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Befolgen Sie diese Schritte, um Zulieferer als buchbare Ressourcen in Microsoft Dynamics 365 Project Operations einzurichten.

1. Wechseln Sie zu **Projekt** \> **Ressourcen**, und wählen Sie dann **Neu** aus.
2. Wählen Sie auf der Seite **Neue buchbare Ressource** im Feld **Ressourcentyp** eine der folgenden Optionen aus:

    - **Benutzer** – Wählen Sie diesen Ressourcentyp aus, wenn der Zulieferer auf Project Operations zugreifen muss, um Zeit oder Ausgaben einzugeben. Wenn Sie **Benutzer** auswählen, benötigt der Zulieferer eine gültige Lizenz, um auf das System zuzugreifen.
    - **Kontakt** oder **Konto** – Wählen Sie einen dieser Ressourcentypen aus, wenn der Zulieferer keinen Zugriff auf Project Operations benötigt, aber für Aufgabenzuweisungen oder Buchungen für Projekte verfügbar sein muss. Keiner dieser Ressourcentypen bietet Zugriff auf das System. Wählen Sie **Konto**, um das Unternehmen des Zulieferers als buchbare Ressource darzustellen. Wählen Sie **Kontakt**, um die einzelnen Mitarbeiter des Kreditors zu repräsentieren.

3. Je nach ausgewähltem Ressourcentyp werden Sie aufgefordert, den entsprechenden Benutzer, das Konto oder den Kontaktdatensatz auszuwählen.
4. Wählen Sie **Art der Arbeiters**-Feld „Vertragsmitarbeiter“ aus, um den Zulieferer als buchbare Ressource einzurichten.

    > [!NOTE]
    > Wenn Sie das Feld **Art der Arbeiters** leer lassen, wird die buchbare Ressource als Mitarbeiter betrachtet.

5. Wenn Sie **Vertragsmitarbeiter** als Arbeitertyp ausgewählt haben, wählen Sie den Kreditor aus, für den die Ressource arbeitet.
6. Wählen Sie die Zeitzone der Ressource aus, und wählen Sie dann **Speichern**. Um der buchbaren Ressource eine Arbeitszeitvorlage zuzuweisen, können Sie **Kalender festlegen** auf der **Buchbare Ressource**-Listenseite auswählen.

Um einer Fremdarbeitsposition zugeordnet werden zu können, muss die buchbare Ressource folgende Bedingungen erfüllen:

- Die buchbare Ressource muss ein Vertragsarbeiter sein.
- Eine buchbare Ressource des **Kontakt**-Ressourcentyp muss dem Kreditorenkonto als Kontakt zugeordnet sein. Eine buchbare Ressource des **Benutzer**-Ressourcentyps muss dem Kreditorenkonto nicht als Kontakt zugeordnet sein.
- Der Wert des **Kreditor**-Felds für die buchbare Ressource muss mit dem Wert des **Kreditor**-Feld für den Fremdarbeitsvertrag übereinstimmen.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Aktualisieren Sie die Art der Arbeiter- und Kreditorzuordnung für buchbare Ressourcen

Das **Art der Arbeiters**-Feld für eine buchbare Ressource bestimmt, ob es sich bei der buchbaren Ressource um einen Vertragsmitarbeiter oder einen Mitarbeiter handelt. Das **Kreditor**-Feld definiert das Kreditorenkonto, dem die buchbare Ressource zugeordnet ist. Indem Sie einem Kreditor eine buchbare Ressource als Kontakt zuordnen, geben Sie an, dass der Kontakt ein Mitarbeiter des Kreditorenunternehmens ist.

Wenn die Felder **Art des Arbeiters** und **Anbieter** für eine buchbare Ressource geändert werden, wirken sich die Änderungen auf alle zukünftigen Validierungen für neue Datensätze aus, die die buchbare Ressource erstellt, wie z. B. Zeiteinträge. Die Änderungen machen jedoch vorhandene Datensätze nicht ungültig.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
