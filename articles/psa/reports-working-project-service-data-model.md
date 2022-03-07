---
title: Arbeiten mit dem Project Service Automation-Datenmodell
description: In diesem Thema finden Sie Informationen dazu, wie Sie mit dem Datenmodell arbeiten.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9bceb96153f0e9f5c0d40478baf691220de95f27
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642677"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Arbeiten mit dem Project Service Automation-Datenmodell

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation erweitert andere App-Entitäten und führt eigene Entitäten im Common Data Service Datenmodell ein. In diesem Kapitel werden einige der Entitäten behandelt, die in typischen PSA-Berichterstellungsszenarien vorkommen.

## <a name="reporting-on-opportunities"></a>Berichte zu Verkaufschancen

Project Service Automation erweitert die Dynamics 365 Sales **Verkaufschance**-Entität, indem Felder hinzugefügt werden, die projektbasierte Szenarien ermöglichen. Diese Felder werden von einem Schemanamen mit vorangestelltem **msdyn\_** erkannt. Ein neues Feld, das für die Berichterstellung in PSA-Verkaufschancen wichtig ist, ist **Auftragstyp**. Ein Wert von **Arbeitsbasiert** für dieses Feld zeigt, dass die Verkaufschance eine PSA-Verkaufschance ist. Die anderen Felder, die der Entität hinzugefügt wurden, sind **Vertragsorganisation**, um die Organisation zu erfassen, die die Verkaufschance hat, und **Konto-Manager**, um den Namen des Kundenbetreuers zu erfassen, der für die Verkaufschance zuständig ist.

Die Entität **Verkaufschancenzeile** enthält auch Felder, die mit Project Service verknüpft sind. **Fakturierungsmethode** zeigt an, dass die Verkaufschancenzeile auf Zeit- und Materialgrundlage oder Festpreisgrundlage berechnet werden soll, und **Projekt** erfasst den Namen des Projekts, das die Verkaufschance unterstützt. Die anderen Felder, für die Sie Berichte zu Erfassungskosten und Kundenbudgetbeträgen für die Positionsartikel erstellen können.

## <a name="reporting-on-quotes"></a>Berichte in Angeboten

PSA erweitert die Vertriebs-**Angebot**-Entität, indem projektbezogene Felder hinzugefügt werden. **Auftragstyp** unterscheidet PSA-Angebote von Angeboten außerhalb von PSA. Ein Wert von **Arbeitsbasiert** für dieses Feld zeigt, dass das Angebot ein PSA-Angebot ist. Die anderen Felder, die für Berichte zu PSA-Angeboten relevant sein können, umfassen Betragsfelder, wie **Fakturierbare Kosten**, **Nichtfakturierbare Kosten**, **Bruttogewinn**, **Schätzungen** und **Budget**. Weitere hilfreiche Felder geben an, ob das Angebot rentabel ist, planmäßig abgeschlossen wird und ob es den Budgeterwartungen des Kunden entspricht.

PSA erweitert auch die Vertriebsentität **Angebotsposition**. Ein Feld, das in PSA hinzugefügt wurde, ist **Fakturierungsmethode**, das angibt, wie die Angebotsposition berechnet wird (Zeit und Materialien oder Festpreis). Die anderen Felder, die der Entitätserfassung für das zugehörige Projekt hinzugefügt wurden, das die Angebotsposition, die Rechnungsstellung, die Kosten und das Budget unterstützt.

PSA fügt auch neue Entitäten in Verbindung mit Angeboten zum Dynamics 365-Datenmodell hinzu. Im Folgenden finden Sie einige Beispiele hierfür:

- **Detailinformationen zur Angebotsposition** – Diese Entität enthält die Projektschätzungsdetails der Angebotsposition. Sie hat zwei Datensätze pro Angebotsposition. Ein Datensatz speichert die Kosten und die Kostendetails der Angebotsposition, und der andere Datensatz speichert die Umsatz- und Vertriebsdetails der Angebotsposition.
- **Rechnungszeitplan der Angebotsposition** – Diese Entität enthält den Fakturierungszeitplan der Angebotsposition. Der Zeitplan wird anhand der Fakturierungshäufigkeit generiert, die der Angebotsposition zugewiesen ist.
- **Meilenstein der Angebotsposition** – Diese Entität enthält die Fakturierungsmeilensteine für Festpreisangebotspositionen.
- **Angebotsposition-Analyseaufschlüsselung** – Diese Entität enthält die Finanzdetails der Angebotsposition. Diese Details können nützlich für Berichte zu angebotenen Verkäufen und geschätzten Kostenbeträgen nach verschiedenen Dimensionen sein.

Andere Entitäten, die PSA zu Angeboten hinzufügt, sind **Projektpreisliste der Angebotsposition**, **Ressourcenkategorie für die Angebotsposition** und **Transaktionskategorie der Angebotsposition**.

![Diagramm mit Angebot, Angebotzeile und Projekt-Beziehungen](media/PS-Reporting-image2.png "Diagramm mit Angebot, Angebotzeile und Projekt-Beziehungen")

## <a name="reporting-on-project-contracts"></a>Berichte zu Projektverträgen

PSA erweitert die Vertriebs-**Auftrags**-Entität, die verwendet wird, wenn Projektverträge erfasst werden. Hierdurch wird ein wichtiges neues Feld **Auftragstyp** hinzugefügt, das den Vertrag als PSA-Projektvertrag anstelle eines Vertriebsauftrags identifiziert. Ein Wert von **Arbeitsbasiert** für dieses Feld zeigt, dass der Auftrag ein PSA-Projektauftrag ist. Andere neue Felder, die zu den **Auftrags**-Entitätserfassungsdetails über Kosten, PSA-Vertragsstatus und über die Organisation hinzugefügt wurden, der der Vertrag gehört.

PSA erweitert auch die Entität **Vertriebsauftragspositionen**. Die hinzugefügten Felder umfassen Felder, die die Fakturierungsmethode (Zeit und Materialien oder Festpreis), die Kundenbudgetbeträge und das zugrundeliegende Projekt erfassen.

PSA fügt auch neue Entitäten hinzu, die für Projektverträge verwendet werden. Im Folgenden finden Sie einige Beispiele hierfür:

- **Projektvertragsposition** – Diese Entität enthält die Informationen auf Positionsebene, die im Vertragszeilenbetrag zusammengerechnet werden. Diese Informationen können so ausführlich wie Positionsartikel sein, die von einem Projektzeitplan auf der Aufgabenebene generiert werden.
- **Rechnungszeitplan für die Vertragszeile** – Diese Entität enthält den Fakturierungszeitplan, der auf Basis der Rechnungshäufigkeit generiert wird, die der Vertragszeile zugeordnet wurde.
- **Vertragsmeilenstein** – Diese Entität enthält die Fakturierungsmeilensteine für Vertragszeilen, die eine Festpreisfakturierungsbedingung haben.

Andere Entitäten, die PSA zu Verträgen hinzufügt, sind **Projektpreisliste der Projektvertragsposition**, **Ressourcenkategorie für die Projektvertragsposition** und **Transaktionskategorie der Projektvertragsposition**.

![Diagramm mit Bestellung, Bestellungszeile und Projekt-Beziehungen](media/PS-Reporting-image3.png "Diagramm mit Bestellung, Bestellungszeile und Projekt-Beziehungen")

## <a name="reporting-on-projects"></a>Berichte zu Projekten

Die **Projekte**-Entität und verknüpfte Entitäten sind für PSA exklusiv. **Projekt** ist die Entität auf oberster Ebene, die verwendet wird, um die Arbeits- und Kostenseite von Aktivitäten aufzuzeichnen. Hier finden Sie eine Liste der zugeordneten Entitäten:

- **Projektteammitglied** – Diese Entität enthält Details zu buchbaren Ressourcen, die dem Projekt zugewiesen werden. Diese Ressourcen können allgemeine buchbare Ressourcen sein, oder sie können buchbare Ressourcen benannt werden, die entweder vom Projektmanager eingegeben werden oder im Projektzeitplan generiert werden.
- **Projektaufgabe** – Diese Entität enthält die Aufgaben, die den Projektplan oder den Zeitplan bilden.
- **Ressourcenzuweisung** – Diese Entität enthält die Aufgabenzuordnung für die Projektressourcenrolle.
- **Ressourcenanforderung** – Diese Entität enthält die Voraussetzungen für alle allgemeinen Ressourcenteammitglieder.
- **Schätzung** und **Vorkalkulationsposition** – Diese Entitäten besitzen eine Kopfzeilen-/Positionsbeziehung und enthalten Ausgabenschätzungen für das Projekt. Aufgabenschätzungen werden in der **Ressourcenbasierten Schätzung** gespeichert.

![Diagramm mit Ressourcenanforderung und Projekt-Beziehungen](media/PS-Reporting-image4.png "Diagramm mit Ressourcenanforderung und Projekt-Beziehungen")

## <a name="reporting-on-resources"></a>Berichte zu Ressourcen

Projektressourcen verwenden die Entität **Buchbare Ressource** aus der Universal Resource Scheduling (URS), die mit anderen Apps verwendet werden, wie Microsoft Dynamics 365 Field Service. Hier finden Sie eine Liste der Entitäten, die Sie möglicherweise verwenden müssen, wenn Sie Berichte zu Projektressourcen erstellen:

- **Buchbare Ressource** – Diese Entität enthält den Benutzer, den Kontakt, die allgemeine Ressource, die Firma, die Gruppe oder die Arbeitsgeräte, die im Projektteam verwendet werden.
- **Merkmale der buchbaren Ressource** – Diese Entität enthält die Fähigkeiten, Zertifizierungen und Ausbildung der Ressource. Die Merkmale können Bewertungswerte haben, die vom Bewertungsmodell definiert werden.
- **Buchbare Ressourcenkategorie** – Diese Entität stellt die Rolle der buchbaren Ressource dar.
- **Buchbare Ressourcenbuchungen** – Diese Entität enthält die Uhrzeit, die für die Ressource in Projekten gebucht wird. Jede Buchung ist eine Kopfzeilenentität und Positionsentität, und jede Position enthält den Status, der den Status der Buchung darstellt.

![Diagramm mit buchbaren Ressourcenmerkmalen-Beziehungen](media/PS-Reporting-image5.png "Diagramm mit buchbaren Ressourcenmerkmalen-Beziehungen")

## <a name="reporting-on-actual-transactions"></a>Berichte zu tatsächlichen Transaktionen

Wenn Sie eine Arbeitszeittabelle oder eine Ausgabe genehmigen oder einen Vertrag mit PSA in Rechnung stellen, wird die Geschäftstransaktion in der Entität **Tatsächlich** erfasst. Die Entität kann als Grundlage für nahezu alle Finanzberichte in PSA dienen. Die Entität **Tatsächlich** erfasst die Kosten Verkaufstransaktionen für das Unternehmensereignis. Sie erfasst zudem zahlreiche relevante Attribute.

Wenn Sie die Entität **Tatsächlich** verwenden, ist es wichtig, zu verstehen, welche Transaktion oder Transaktionen in der Entität erfasst werden und wann die Transaktionen erfasst wurden. Dies ist der typische Fluss, wenn Sie mit Zeiteintragungen arbeiten (der Fluss für Ausgabeneinträge ist ähnlich):

1. Wenn die Zeiteintragung gespeichert wurde, werden keine Datensätze in der Entität **Tatsächlich** erstellt.
2. Wenn die Zeiteintragung übermittelt wurde, werden keine Datensätze in der Entität **Tatsächlich** erstellt.
3. Wenn die Zeiteintragung genehmigt wurde, wird ein Datensatz in der Entität **Tatsächlich** erstellt und es kann ein zweiter Datensatz erstellt werden. Im ersten Datensatz sind die Kosten der Zeiteintragung gespeichert. Der zweite Datensatz speichert den nicht fakturierten Umsatz der Zeiteintragung. Der zweite Datensatz ist abhängig vom Projekt und hat entweder einen Kunden, ein Angebot oder eine Vertragszeile zugeordnet.

    | Dokumentdatum | Transaktionstyp | Transaktionsklasse | Kunde         | Vertrag   | Ressource     | Ressourcenrolle | Fakturierungstyp | Menge | Einzelpreis | Betrag |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kosten             | Time              | Alpines Skihaus | Alpine CRM | Bruna Schöffer | Projektmanagerin   | Fakturierbar   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Nicht fakturierte Umsätze   | Time              | Alpines Skihaus | Alpine CRM | Bruna Schöffer | Projektmanagerin   | Fakturierbar   | 8.0      | 100.00     | 800.00 |

    Diese beiden Datensätze sind separate, jedoch verknüpfte Datensätze. Sie sind weder Soll noch Haben.

4. Falls ein Vertrag dem Projekt zugeordnet wird, wenn die Zeiteintragung in Rechnung gestellt wird, werden zwei weitere Datensätze in der Entität **Tatsächlich** erstellt. Zuerst wird ein negativer Betrag für den nicht fakturierten Vertriebsdatensatz erstellt. Dieser Datensatz kehrt im Wesentlichen den nicht fakturierten Vertrieb um. Anschließend wird eine Transaktion für den nicht fakturierten Vertrieb erstellt. Auch hier sind die Datensätze separat, jedoch verknüpft und sind weder Soll noch Haben.

    | Dokumentdatum | Transaktionstyp | Transaktionsklasse | Kunde         | Vertrag   | Ressource     | Ressourcenrolle | Fakturierungstyp | Menge | Einzelpreis | Betrag   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Nicht fakturierte Umsätze   | Time              | Alpines Skihaus | Alpine CRM | Bruna Schöffer | Projektmanagerin   | Fakturierbar   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Fakturierte Umsätze     | Time              | Alpines Skihaus | Alpine CRM | Bruna Schöffer | Projektmanagerin   | Fakturierbar   | 8.0      | 100.00     | 800.00   |

Die Entität **Transaktionsursprung** zeichnet den Ursprung des Datensatzes **Tatsächlich** und die Entität **Transaktionsverbindung** zeichnet die zugehörigen Datensätze für den Datensatz **Tatsächlich** auf. Darüber hinaus enthält der Datensatz **Tatsächlich** Verweise auf das Projekt, den Projektvertrag (Auftrag), die buchbare Ressource und den Kunden.

![Diagramm mit Transaktionsverbindung, Ursprung und tatsächlichem Beziehungen](media/PS-Reporting-image6.png "Diagramm mit Transaktionsverbindung, Ursprung und tatsächlichem Beziehungen")
