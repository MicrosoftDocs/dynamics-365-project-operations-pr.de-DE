---
title: Ein Projekt kopieren
description: Dieses Thema enthält Informationen zum Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479518"
---
# <a name="copy-a-project"></a>Ein Projekt kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mithilfe von Dynamics 365 Project Operations können Sie schnell neue Projekte erstellen, indem Sie **Projekt kopieren** im Formular **Projekte** auswählen. Um ein Projekt zu kopieren, öffnen Sie das zu kopierende Projekt, und wählen Sie dann **Projekt kopieren** aus. Die Aktion kopiert:

- Projekteigenschaften (das geschätzte Startdatum wird aus dem Quellprojekt übernommen)
- Die Projektstrukturplan
- Projektteammitglieder
- Projektschätzungen
- Projektausgabenschätzungen

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
- Voraussichtliches Startdatum
- Fertigstellungsdatum
- Aufwand (Stunden)
- Geschätzte Arbeitskosten
- Geschätzte Ausgabenkosten

## <a name="work-breakdown-structure"></a>Projektstrukturplan

Beim Kopieren des Projekts wird die gesamte ressourcenintensive Projektstrukturplan kopiert. Benannte Ressourcen werden durch generische Ressourcen ersetzt. Wenn die benannten Ressourcen nicht die gleichen Arbeitszeiten wie die generische Ressource haben, wird der Zeitplan neu berechnet und die Aufgabendauer kann sich ändern.

## <a name="project-team-members"></a>Projektteammitglieder

Wenn ein Projektteam aus dem Quellprojekt kopiert wird, werden die generischen Ressourcen kopiert. Generische Ressourcenzuweisungen werden wie im Quellprojekt verwaltet. Benannte Ressourcen werden in generische Teammitglieder konvertiert.

## <a name="estimates"></a>Schätzungen

Wenn das Projekt kopiert wird, werden sowohl Ressourcen- als auch Ausgabenschätzungszeilen aus dem Quellprojekt kopiert. 

Informationen zum programmgesteuerten Zugriff auf „Projekt kopieren“ finden Sie unter [Projektvorlagen mit „Projekt kopieren“ entwickeln](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
