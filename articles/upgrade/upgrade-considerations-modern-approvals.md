---
title: Upgrade-Überlegungen für moderne Genehmigungen
description: Das Thema behandelt die Punkte, die Administratoren berücksichtigen sollten, wenn sie die Funktionalität für moderne Genehmigungen aktivieren.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578385"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Upgrade-Überlegungen für moderne Genehmigungen 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Als Teil der Veröffentlichung von Zyklus 1 vom April 2022 wird die Funktion „Moderne Genehmigungen“ standardmäßig aktiviert. Diese Funktion verbessert die Zuverlässigkeit der Genehmigungslogik und stellt sicher, dass Sie den Grund ermitteln können, wenn die Genehmigungslogik fehlschlägt.

Im Rahmen dieser Änderung werden Statusänderungen für Projektgenehmigungen aktualisiert. Der Status geht jetzt direkt von **Eingereicht** zu **Genehmigt**. **Ausstehend** ist kein Status für Genehmigungen mehr. Um festzustellen, ob eine Genehmigung aussteht, vergewissern Sie sich, dass die Genehmigung Teil eines Genehmigungssatzes ist, und überprüfen Sie den Status des angehängten Genehmigungssatzes.

## <a name="before-you-upgrade"></a>Vor dem Upgrade

Stellen Sie vor dem Upgrade auf moderne Genehmigungen sicher, dass Sie keine ausstehenden Genehmigungen haben. Moderne Genehmigungen verwendet den **Ausstehend**-Status nicht. Daher werden alle Genehmigungen, die noch als **Ausstehend** gekennzeichnet sind, nach dem Upgrade nicht verarbeitet.

## <a name="after-you-upgrade"></a>Nach dem Upgrade

Nach dem Upgrade auf moderne Genehmigungen muss ein Administrator validieren, dass der Cloud-Flow, der Genehmigungen verarbeitet, aktiviert wurde.

1. Melden Sie sich bei [flow.microsoft.com](https://flow.microsoft.com) an
2. Wechseln Sie oben rechts auf der Seite von Ihrer Umgebung zu der Umgebung, die Sie aktualisiert haben.
3. Wählen Sie **Lösungen** aus, um die Lösungen aufzuführen, die in der Umgebung installiert sind.
4. Wählen Sie in der Lösungsliste **Project Operations** oder **Project Service**.
5. Ändern Sie den Filter von **Alle** in **Cloud-Flows**.
6. Überprüfen Sie, ob die **Project Service – Projektgenehmigungssätze regelmäßig planen**-Option au f **Ein** eingestellt. Wenn dies nicht der Fall ist, wählen Sie den Flow aus, und wählen Sie dann **Aktivieren** aus.
7. Überprüfen Sie, ob die Verarbeitung alle fünf Minuten erfolgt, indem Sie die **Systemaufträge**-Liste im **Einstellungen**-Bereich überprüfen.

## <a name="short-term-rollback"></a>Kurzzeitiger Rollback

Wenn Sie die Änderungen nicht übernehmen können oder ein schwerwiegendes Problem mit dieser Funktion auftritt, können Sie vorübergehend zum ursprünglichen Genehmigungsablauf zurückkehren, indem Sie die folgenden Schritte ausführen:
1. Melden Sie sich bei Ihrer Umgebung an und vergewissern Sie sich, dass keine Genehmigungen ausstehen.
2. Gehen Sie zu **Einstellungen** > **Projektparameter**.
3. Wählen Sie **Funktionssteuerung** und dann **Moderne Genehmigungen** aus, um die Funktion auszuschalten.

## <a name="removing-the-feature-flag"></a>Entfernen des Funktionskennzeichens

Im Zyklus 2-Update vom Oktober 2022 wird die Möglichkeit zum Deaktivieren dieser Funktion entfernt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
