---
title: Bereitstellungstypen
description: Dieses Thema enthält Informationen, die Ihnen helfen, den korrekten Bereitstellungstyp von Projekt Operations für Ihr Unternehmen zu bestimmen.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948868"
---
# <a name="deployment-types"></a>Bereitstellungstypen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

> [!IMPORTANT]
> Nachdem Sie die Lizenz gekauft haben, beginnen Sie hier, um das beste Bereitstellungsmodell für Dynamics 365 Project Operations mithilfe des [geführten Installationsablaufs](https://aka.ms/provisionprojectoperations) zu ermitteln.
> Nachdem Sie den geführten Installationsablauf abgeschlossen haben, werden Sie zum richtigen Verwaltungsportal weitergeleitet, um Ihre Installation abzuschließen. Weitere Informationen zum Abschluss der Installation finden Sie in den folgenden Bereitstellungsdetails.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Vorhandene Kunden von Dynamics, die Dynamics 365 Project Service Automation nutzen
Project Operations umfasst die Funktionen, die mit Project Service Automation geliefert werden. Für diese Kunden wird in Zukunft ein Upgrade-Pfad freigegeben.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Vorhandene Kunden von Dynamics 365 Finance, die Projektmanagement und -buchhaltung verwenden 

Vorhandene Finanzkunden, die die Projektmanagement- und -buchhaltungsfunktion verwenden, können diese weiterhin verwenden. Weitere Informationen finden Sie unter [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma).

Project Operations unterstützt mehrere Bereitstellungsoptionen, die Ihren Anforderungen entsprechen. Unabhängig davon, ob Sie ein neuer oder vorhandener Dynamics 365-Kunde sind, kann Project Operations Ihre Anforderungen unterstützen.

Unsere [Bereitstellungsfragebogen](https://aka.ms/provisionprojectoperations) hilft Ihnen bei der Ermittlung der richtigen Bereitstellung. Die Ergebnisse führen Sie zu einem der folgenden Bereitstellungstypen:

- [Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung](#lite)
- [Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen](#integrated)
- [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma)

Project Operations unterstützt Lager-/Produktionsauftragsszenarien und nicht lagernde/ressourcenbasierte Szenarien in derselben Umgebung durch Konfigurationen auf der Ebene der juristischen Person. Beispielsweise kann Contoso die Lagerbestands-/Produktionsauftragsfunktionen in seiner US-Produktionsstätte (juristische Person = Contoso Manufacturing USA) und die nicht vorrätigen/ressourcenbasierten Funktionen in seiner Contoso Robotics Arms-Serviceeinrichtung in Großbritannien (juristische Person = Contoso Robotics Vereintes Königreich) nutzen.

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung
Die Lite-Bereitstellung umfasst die folgenden Funktionen:

- Projektplanung mit Microsoft Project für das Web
- Mehrdimensionale Preisberechnung
- Vereinheitlichte Ressourcenverwaltung
- Zeitnachverfolgung
- Grundkosten
- Rechnungsvorschlag

### <a name="deployment-steps"></a>Bereitstellungsschritte:
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](lite-preview-subscription-sign-up.md) und [Neue Umgebung bereitstellen](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen
Der Projektbetrieb für Ressourcen-/nicht vorrätige Szenarien umfasst die folgenden Funktionen:
  
- Projektplanung mit Microsoft Project für das Web
- Mehrdimensionale Preisberechnung
- Vereinheitlichte Ressourcenverwaltung
- Zeitnachverfolgung
- Grundkosten
- Volle Ausgaben
- Zugangs-OCR
- Volle Rechnungsstellung
- Umsatzrealisierung

### <a name="deployment-steps"></a>Bereitstellungsschritte:
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](resource-sign-up-preview-subscription.md) und [Neue Umgebung bereitstellen](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen

- Projektplanung mit WBS
- Ressourcenverwaltung
- Zeitnachverfolgung
- Volle Ausgaben
- Zugangs-OCR
- Volle Rechnungsstellung
- Umsatzrealisierung
- Produktionsaufträge
- Materialienunterstützung

### <a name="deployment-steps"></a>Bereitstellungsschritte:
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) und [Neue Umgebung bereitstellen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



