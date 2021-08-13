---
title: Ein Projekt kopieren
description: Dieses Thema enthält Informationen zum Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007190"
---
# <a name="copy-a-project"></a>Ein Projekt kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mithilfe von Dynamics 365 Project Operations können Sie schnell neue Projekte erstellen, indem Sie **Projekt kopieren** im Formular **Projekte** auswählen. Um ein Projekt zu kopieren, öffnen Sie das zu kopierende Projekt, und wählen Sie dann **Projekt kopieren** aus. Die Aktion kopiert Folgendes:

- Projekteigenschaften 
- Projektstrukturplan
- Projektteammitglieder
- Projektschätzungen
- Projektausgabenschätzungen
- Materialschätzungen Projekte

## <a name="project-properties"></a>Projekteigenschaften

Beim Kopieren des Projekts werden die Werte in den folgenden Feldern kopiert:

- Name des Dataflows
- Beschreibung des Dataflows
- Kunde
- Kalendervorlage
- Währung
- Vertragseinheit
- Projektmanager
- Status
- Gesamtprojektstatus
- Kommentare
- Schätzungen
- Geschätztes Startdatum: Dies ist das Datum, an dem das Projekt aus der Kopie erstellt wird.
- Voraussichtliches Enddatum: Dieses Datum wird basierend auf dem Startdatum des neuen Projekts angepasst, das aus der Kopie erstellt wurde.
- Aufwand (Stunden)
- Geschätzte Arbeitskosten
- Geschätzte Ausgabenkosten
- Geschätzte Materialkosten

> [!NOTE]
> Projekt kopieren ist ein lang andauernder Vorgang. Projektdatensätze, ihre relevanten Attribute und viele zugehörige Entitäten werden ebenfalls kopiert. Aufgrund der langen Laufzeit des Vorgangs wird die Zielprojektseite nach dem Start des Kopiervorgangs für die Bearbeitung gesperrt, bis der Kopiervorgang abgeschlossen ist.

## <a name="work-breakdown-structure"></a>Projektstrukturplan

Beim Kopieren des Projekts wird die gesamte ressourcenintensive Projektstrukturplan kopiert. Benannte Ressourcen werden durch generische Ressourcen ersetzt. Wenn die benannten Ressourcen nicht die gleichen Arbeitszeiten wie die generische Ressource haben, wird der Zeitplan neu berechnet und die Aufgabendauer kann sich ändern.

## <a name="project-team-members"></a>Projektteammitglieder

Wenn ein Projektteam aus dem Quellprojekt kopiert wird, werden die generischen Ressourcen kopiert. Generische Ressourcenzuweisungen werden wie im Quellprojekt verwaltet. Benannte Ressourcen werden in generische Teammitglieder konvertiert.

## <a name="estimates"></a>Schätzungen

Beim Kopieren des Projekts werden Ressourcen-, Aufwands- und Materialkalkulationszeilen aus dem Quellprojekt kopiert. 

Informationen zum programmgesteuerten Zugriff auf „Projekt kopieren“ finden Sie unter [Projektvorlagen mit „Projekt kopieren“ entwickeln](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
