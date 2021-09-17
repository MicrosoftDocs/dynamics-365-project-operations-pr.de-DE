---
title: Ressourcen für Fremdarbeitsposition
description: In diesem Thema wird erläutert, wie Sie die dedizierten Ressourcen angeben, die vom Lieferanten für eine bestimmte Fremdarbeitsposition zeitlich festgelegt werden.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323370"
---
# <a name="subcontract-line-resources"></a>Ressourcen für Fremdarbeitsposition

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations kann ein Lieferant Ressourcen angeben, die verwendet werden, um die Ressourcenkapazität zu liefern, die auf der Fremdarbeitsposition auf Zeit gekauft wird.

## <a name="create-subcontract-line-resources"></a>Ressourcen für Fremdarbeitsposition erstellen

Gehen Sie wie folgt vor, um Ressourcen für eine Fremdarbeitsposition zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus, und öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten.
2. Öffnen Sie die Fremdarbeitsposition für die Zeit, für die Sie Lieferantenressourcen angeben möchten.
3. Auf der **Ressourcen für die Fremdarbeitsposition**-Registerkarte wählen Sie im Unterraster **+ Neue Ressource für die Fremdarbeitsposition**.
4. Auf der **Neuer Meilenstein für die Fremdarbeitsposition**-Seite geben Sie die erforderlichen Informationen ein und wählen dann **Speichern und schließen** aus.

In der folgenden Tabelle werden die Felder der Ressourcen für die Fremdbearbeitungsposition erläutert.

| Feld |  Beschreibung |
| ----- | ------------ |
| Buchbare Ressource | Wählen Sie eine buchbare Ressource vom Typ „Fremdarbeiter“ aus, die Sie als Ressource in der Fremdarbeitsposition verwenden möchten. Wenn Sie noch keine buchbare Ressource für den Fremdarbeiter angelegt haben, lassen Sie dieses Feld leer. Beim Speichern des Datensatzes wird eine buchbare Ressource erstellt.  |
| Kontakt | Wenn das **Buchbare Ressource**-Feld leer ist, können Sie Ihre Fremdarbeitsressource aus einem vorhandenen Kontakt erstellen. Verwenden Sie die Suche, um die Liste der aktiven Kontakte im System anzuzeigen. Wählen Sie einen Ansprechpartner für den Lieferanten dieses Fremdarbeiters aus. Der ausgewählte Kontakt wird beim Speichern des Datensatzes validiert. Wenn der von Ihnen ausgewählte Kontakt kein gültiger Kontakt ist, wird Ihr Datensatz nicht gespeichert. Wenn für den ausgewählten Kontakt keine buchbare Ressource vorhanden ist, erstellt das System eine buchbare Ressource für den ausgewählten Kontakt, bevor die Ressource für die Fremdarbeitsposition erstellt wird. |
| User | Wenn das **Buchbare Ressource**-Feld leer ist, können Sie eine Fremdarbeitsressource erstellen, indem Sie einen aktiven Benutzer auswählen. Verwenden Sie die Suche, um die Liste der aktiven Benutzer im System anzuzeigen. Wenn für den ausgewählten Benutzer keine buchbare Ressource vorhanden ist, erstellt das System eine buchbare Ressource für den ausgewählten Benutzer, bevor die Ressource für die Fremdarbeitsposition erstellt wird. |
| Startdatum | Das Datum, an dem der Einsatz des Fremdarbeiters beginnt. Wenn diese Ressource für einen Zeitraum gebucht wird, der vor diesem Datumsbereich liegt, wird eine Warnung ausgegeben. |
| Enddatum | Das Datum, an dem der Einsatz des Fremdarbeiters beendet ist. Wenn diese Ressource für einen Zeitraum gebucht wird, der nach diesem Datumsbereich liegt, wird eine Warnung ausgegeben. |
| Aufwand | Die Gesamtzahl der Arbeitsstunden, die die Fremdarbeitskraft für diese Fremdarbeitsposition aufwenden wird. Wenn diese Ressource über den Aufwand hinaus gebucht wird, der ihr in dieser Fremdarbeit zugewiesen ist, wird eine Warnung ausgegeben. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
