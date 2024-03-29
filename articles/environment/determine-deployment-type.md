---
title: Bereitstellungstyp festlegen
description: Dieser Artikel liefert Informationen, die Ihnen helfen, die richtige Einsatzart von Project Operations für Ihre Firma zu bestimmen.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912193"
---
# <a name="determine-your-deployment-type"></a>Bereitstellungstyp festlegen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

> [!IMPORTANT]
> Beginnen Sie nach dem Kauf der Lizenz hier, um das beste Bereitstellungsmodell für Dynamics 365 Project Operations mithilfe des [ Geführten Installationsflows](https://aka.ms/provisionprojectoperations) zu ermitteln.
> Nachdem Sie den geführten Installationsablauf abgeschlossen haben, werden Sie zum richtigen Verwaltungsportal weitergeleitet, um Ihre Installation abzuschließen. Weitere Informationen zum Abschluss der Installation finden Sie in den Bereitstellungsdetails.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Vorhandene Kunden von Dynamics, die Dynamics 365 Project Service Automation nutzen
Project Operations umfasst die Funktionen, die mit Project Service Automation geliefert werden. Für diese Kunden wird in der Veröffentlichungswelle 1 2021 ein Upgrade-Pfad freigegeben.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Vorhandene Kunden von Dynamics 365 Finance, die Projektmanagement und Buchhaltung verwenden 

Bestehende Finance-Kunden, die die Projektmanagement- und Buchhaltungsfunktion verwenden, können sie weiterhin unverändert verwenden. Weitere Informationen finden Sie unter [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma).


## <a name="deployment-regions"></a>Bereitstellungsregionen
Informationen dazu, welche Regionen die Bereitstellung von Project Operations unterstützen, finden Sie unter [Geografische Verfügbarkeit für Dynamics 365- und Power Platform-Berichte](https://dynamics.microsoft.com/en-us/geographic-availability/). Wählen Sie **Bericht anzeigen** aus, und erweitern Sie **Dynamics 365 > Operations-Apps > Dynamics 365 Project Operations**, um sich die unterstützten Regionen anzeigen zu lassen.

## <a name="deployment-types"></a>Bereitstellungstypen
Project Operations unterstützt mehrere Bereitstellungsoptionen, die Ihren Anforderungen entsprechen. Unabhängig davon, ob Sie ein neuer oder vorhandener Dynamics 365-Kunde sind, kann Project Operations Ihre Anforderungen unterstützen.

Unsere [Bereitstellungsfragebogen](https://aka.ms/provisionprojectoperations) hilft Ihnen bei der Ermittlung der richtigen Bereitstellung. Die Ergebnisse führen Sie zu einem der folgenden Bereitstellungstypen:

- [Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung](#lite)
- [Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen](#integrated)
- [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma)

Project Operations unterstützt Lager-/Produktionsauftragsszenarien und nicht lagernde/ressourcenbasierte Szenarien in derselben Umgebung durch Konfigurationen auf der Ebene der juristischen Person. Beispielsweise kann Contoso die Lagerbestands-/Produktionsauftragsfunktionen in seiner US-Produktionsstätte nutzen (juristische Person = Contoso Manufacturing United States). Contoso kann die nicht vorrätigen/ressourcenbasierten Funktionen in seiner Contoso Robotics Arms-Serviceeinrichtung im Vereinigten Königreich (juristische Person = Contoso Robotics, Vereinigtes Königreich) verwenden.

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung

Die Lite-Bereitstellung umfasst die folgenden Funktionen:

- Verkaufsprozess für Projekte, der die Anwendungserfahrung von Dynamics 365 Sales erweitert
- Projektplanung mit Microsoft Project für das Web
- Mehrdimensionale Preisberechnung
- Einheitliche Ressourcenverwaltung
- Zeiterfassung
- Grundkosten
- Proforma-Rechnungsstellung für die Überprüfung und Bearbeitung durch den Projektmanager 

#### <a name="deployment-steps"></a>Bereitstellungsschritte
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](lite-preview-subscription-sign-up.md) und [Neue Umgebung bereitstellen](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen
Der Projektbetrieb für Ressourcen-/nicht vorrätige Szenarien umfasst die folgenden Funktionen:
 
- Verkaufsprozess für Projekte, der die Anwendung von Dynamics 365 Sales erweitert
- Projektplanung mit Microsoft Project für das Web
- Mehrdimensionale Preisberechnung
- Vereinheitlichte Ressourcenverwaltung
- Zeitnachverfolgung
- Grundkosten
- Volle Ausgaben
- Zugangs-OCR
- Proforma und kundenorientierte Rechnungsstellung 
- Umsatzerkennung für Projekte

#### <a name="deployment-steps"></a>Bereitstellungsschritte
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](resource-sign-up-preview-subscription.md) und [Neue Umgebung bereitstellen](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen

- Projektplanung mit WBS
- Ressourcenverwaltung
- Zeiterfassung
- Volle Ausgaben
- Zugangs-OCR
- Volle Rechnungsstellung
- Umsatzrealisierung
- Fertigungsaufträge
- Lagerbestandsunterstützung mit Inventar

#### <a name="deployment-steps"></a>Bereitstellungsschritte
Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).

Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) und [Neue Umgebung bereitstellen](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]