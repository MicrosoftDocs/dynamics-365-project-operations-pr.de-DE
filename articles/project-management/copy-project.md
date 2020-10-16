---
title: Ein Projekt kopieren
description: Dieses Thema enthält Informationen zum Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908143"
---
# <a name="copy-a-project"></a>Ein Projekt kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mit Dynamics 365 Project Operations können Sie mithilfe der **Projekt kopieren**-Aktion auf dem **Projekte**-Formular schnell neue Projekte erstellen. Um ein Projekt zu kopieren, wählen Sie ein Projekt aus und wählen Sie dann **Kopieren**. Die Aktion kopiert:

- Projekteigenschaften
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