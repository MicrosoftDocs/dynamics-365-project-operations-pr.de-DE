---
title: Ressourcen für Fremdarbeitsposition
description: Dieser Artikel erklärt, wie Sie die dedizierten Ressourcen festlegen, die der Lieferant für eine bestimmte Zeile eines Unterauftrags auf Zeit bereitstellt.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d440201fde26e835b407db0b8ee1de8d663311a0
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261463"
---
# <a name="subcontract-line-resources"></a>Ressourcen für Fremdarbeitsposition

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations kann ein Lieferant Ressourcen angeben, die verwendet werden, um die Ressourcenkapazität zu liefern, die auf der Fremdarbeitsposition auf Zeit gekauft wird.

## <a name="create-subcontract-line-resources"></a>Ressourcen für Fremdarbeitsposition erstellen

Gehen Sie wie folgt vor, um Ressourcen für eine Fremdarbeitsposition zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus, und öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten.
2. Öffnen Sie die Fremdarbeitsposition für die Zeit, für die Sie Lieferantenressourcen angeben möchten.
3. Auf der **Ressourcen für die Fremdarbeitsposition**-Registerkarte wählen Sie im Unterraster **+ Neue Ressource für die Fremdarbeitsposition**.
4. Geben Sie auf der Seite **Neue Ressource für Fremdarbeitsposition** die erforderlichen Speseninformationen ein, und wählen Sie dann **Speichern und schließen** aus.

In der folgenden Tabelle werden die Felder der Ressourcen für die Fremdbearbeitungsposition erläutert.

| Feld | Beschreibung | Funktionsauswirkung |
| ----- | ----------- | ----------------- |
| Buchbare Ressource | Wählen Sie eine buchbare Ressource vom Typ **Fremdarbeiter** aus, die Sie als Ressource in der Fremdarbeitsposition verwenden möchten.| Wenn Sie keine buchbare Ressource für den Leiharbeiter angelegt haben, lassen Sie dieses Feld leer. Beim Speichern des Datensatzes wird eine buchbare Ressource erstellt.  |
| Kontakt | Sie können Ihre Fremdauftragszeilenressource aus einem vorhandenen Kontakt erstellen. Verwenden Sie die Suche, um die Liste der aktiven Kontakte im System anzuzeigen. Wählen Sie einen Ansprechpartner für den Lieferanten dieses Fremdarbeiters aus. Wenn der von Ihnen ausgewählte Kontakt kein gültiger Kontakt für den Kreditor im Unterauftrag ist, wird der Ressourcendatensatz der Fremdauftragsposition nicht gespeichert.| Wenn für den ausgewählten Kontakt keine buchbare Ressource vorhanden ist, erstellt das System eine buchbare Ressource für den ausgewählten Kontakt, bevor die Ressource für die Fremdarbeitsposition erstellt wird. |
| User | Sie können eine Fremdauftragszeilenressource erstellen, indem Sie einen aktiven Benutzer auswählen. Verwenden Sie die Suche, um die Liste der aktiven Benutzer im System anzuzeigen.| Wenn für den ausgewählten Benutzer keine buchbare Ressource vorhanden ist, erstellt das System eine buchbare Ressource für den ausgewählten Benutzer, bevor die Ressource für die Fremdarbeitsposition erstellt wird. |
| Startdatum | Das Datum, an dem der Einsatz des Fremdarbeiters beginnt.| Wenn diese Ressource für einen Zeitraum gebucht wird, der vor diesem Datumsbereich liegt, wird eine Warnung ausgegeben. |
| Enddatum | Das Datum, an dem der Einsatz des Fremdarbeiters beendet ist.| Wenn diese Ressource für einen Zeitraum gebucht wird, der nach diesem Datumsbereich liegt, wird eine Warnung ausgegeben. |
| Aufwand | Die Gesamtzahl der Arbeitsstunden, die die Vertragsarbeitskraft für diese Unterauftragsposition aufwenden wird.| Wenn diese Ressource über den Aufwand hinaus gebucht wird, der diesem Unterauftrag zugeordnet ist, erfolgt eine Warnung. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
