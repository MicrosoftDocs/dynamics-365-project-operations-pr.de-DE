---
title: Sicherheitsmodell
description: Dieses Thema enthält Informationen zum Sicherheitsmodell in Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642902"
---
# <a name="security-model"></a>Sicherheitsmodell

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations enthält ein einzigartiges Sicherheitsmodell, das ein rollenbasiertes Geschäftssicherheitsmodell ermöglicht, mit dem in Microsoft Office-Gruppen zusammengearbeitet wird. 


## <a name="security-roles"></a>Sicherheitsrollen
Die Front-End-Funktionen von Project Operations umfassen die folgenden Rollen:

| Rolle                          | Beschreibung des Dataflows                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Practice Manager              | Unterstützt projektübergreifende Berichte                                                                                                            | Geschäftseinheit              |
| Projektgenehmiger              | Genehmigt Zeit und Ausgaben für ein Projekt                                                                                                                              | Geschäftseinheit |
| Projektabrechnungsadministrator | Erstellt den Rechnungsvorschlag                                                                                                                                                 | Geschäftseinheit |
| Projektmanager               | Erstellt den Projektplan und fordert Ressourcen an                                                                                                                              | Geschäftseinheit |
| Projektressource              | Teammitglieder, die gebucht werden können und Zeit melden                                                                                                          | Geschäftseinheit|
| Resource Manager              | Alle Ressourcenverwaltungsfunktionen, z. B. die Erfüllung von Ressourcenanforderungen und Buchungen, sind getrennt, um eine hybride Projektmanager- und Resource Manager-Konfiguration und eine einzelne und zentralisierte Resource Manager-Rolle zu unterstützen. | Geschäftseinheit |


Microsoft Project for the Web enthält die folgenden Rollen:

| Rolle           | Beschreibung des Dataflows                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projektbenutzer   | Kollaborativer Benutzer von Project   , der in der Lage ist, eigene Projekte zu erstellen und alle für ihn freigegebenen Projekte anzuzeigen | User   |
| Projektsystem | Rolle, die für den Kontext der Anwendung   verwendet wird Kunden sollten diese Systemrolle nicht verwenden.                                    | Global |

## <a name="security-enforcement"></a>Sicherheitsdurchsetzung
Aktionen, die auf Projektebene ausgeführt werden, werden im Kontext des angemeldeten Benutzers ausgeführt. Dies bedeutet, dass der Benutzer zum Erstellen, Öffnen oder Löschen eines Projekts Zugriff auf CDS haben muss. Der Zugriff auf CDS kann über einen der in der Plattform enthaltenen möglichen Mechanismen gewährt werden. Beispielsweise kann ein Benutzer mit einem größeren Bereich auf das Projekt zugreifen oder wenn eine explizite Projektfreigabeaktion ausgeführt wurde, die dem Benutzer Zugriff gewährt.

Es ist wichtig, dies beim Erstellen von Projekten in Project Operations zu berücksichtigen.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderne Gruppenzusammenarbeit mit Project Operations
Project for the Web und Project Operations unterstützen moderne Gruppen für die Zusammenarbeit. Benutzer, die über eine Gruppe zum Projekt hinzugefügt wurden, können den Projektplan bearbeiten.

Project for the Web fügt Benutzer bei der Zuweisung automatisch zur Gruppe hinzu.

Mithilfe von Gruppen können die Berechtigungen des Projekts und unterstützende Artefakte für die Zusammenarbeit gemeinsam bearbeitet werden. Das folgende Diagramm zeigt die Ereignisse und Statusänderungen, die während des Gruppenzuweisungsprozesses auftreten.

Project Operations erstellt keine Gruppe durch implizite Aktion und nur durch die explizite Aktion dringlicher Gruppen.

Die Suche nach Gruppenmitgliedern im Dialogfeld **Gruppenverwaltung** ist auf diejenigen beschränkt, die als Teil der Sicherheitsgruppe der Umgebung festgelegt sind. Weitere Informationen unter [Benutzerzugriff auf Umgebungen steuern: Sicherheitsgruppen und Lizenzen](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Gruppenmodus](./media/groupsmode.png)

1. Das Projekt wird erstellt und gehört dem erstellenden Benutzer.
2. Der Projektbesitzer wird für das Team aktualisiert.
3. Das Besitzerteam ist der angegebenen oder erstellten Office-Gruppe zugeordnet.
4. Der ursprüngliche Besitzer des Projekts wird der Office-Gruppe hinzugefügt.

## <a name="deployment-recommendation"></a>Bereitstellungsempfehlung
Im Zuge der Weiterentwicklung des Modells für die Zusammenarbeit mit Office-Gruppen werden Funktionen hinzugefügt, um eine detailliertere Kontrolle über die Zeit zu ermöglichen. Kunden, die Project Operations heute bereitstellen, werden aufgefordert, sich auf ein traditionelles Microsoft Dynamics 365-Sicherheitsmodell zu konzentrieren.

Weitere Informationen finden Sie unter [Sicherheit in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations- und Microsoft Dynamics 365 Finance-Sicherheit
Project Operations umfasst die folgenden Rollen:

- Projektmanager
- Projektbuchhaltung

Weitere Informationen zur Sicherheit in Finance finden Sie unter [Rollenbasierte Sicherheit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


