---
title: Projektvorlagen mit Projekt kopieren erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Projektvorlagen mithilfe der benutzerdefinierten Aktion „Projekt kopieren“.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590897"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektvorlagen mit Projekt kopieren erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt die Möglichkeit, ein Projekt zu kopieren und alle Zuweisungen auf die allgemeinen Ressourcen zurückzusetzen, die die Rolle darstellen. Kunden können diese Funktionalität verwenden, um grundlegende Projektvorlagen zu erstellen.

Wenn Sie **Projekt kopieren** auswählen, wird der Status des Zielprojekts aktualisiert. Verwenden Sie **Statusgrund**, um festzustellen, wann die Kopieraktion abgeschlossen ist. Durch Auswahl von **Projekt kopieren** wird auch das Startdatum des Projekts auf das aktuelle Startdatum aktualisiert, wenn in der Zielprojektentität kein Zieldatum erkannt wird.

## <a name="copy-project-custom-action"></a>Benutzerdefinierte Aktion „Projekt kopieren“

### <a name="name"></a>Name des Dataflows 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Eingabeparameter

Es gibt drei Eingabeparameter:

- **ReplaceNamedResources** oder **ClearTeamsAndAssignments** – Stellen Sie nur eine der Optionen ein. Stellen Sie nicht beide ein.

    - **\{"ReplaceNamedResources":true\}** – Das Standardverhalten für Project Operations. Alle benannten Ressourcen werden durch generische Ressourcen ersetzt.
    - **\{"ClearTeamsAndAssignments":true\}** – Das Standardverhalten für Project for the Web. Alle Zuweisungen und Teammitglieder werden entfernt.

- **SourceProject** – Die Entitätsreferenz des Quellprojekts, aus dem kopiert werden soll. Dieser Parameter darf nicht sein.
- **Target** – Die Entitätsreferenz des Zielprojekts, in das kopiert werden soll. Dieser Parameter darf nicht sein.

Die folgende Tabelle enthält eine Übersicht über die drei Parameter.

| Parameter                | Type             | Wert                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolesch          | **True** oder **False** |
| ClearTeamsAndAssignments | Boolesch          | **True** oder **False** |
| SourceProject            | Entitätsreferenz | Das Quellprojekt    |
| Zielsprache                   | Entitätsreferenz | Die Zielprojekt    |

Weitere Standardinformationen über Aktionen finden Sie unter [Nutzen von Web-API-Aktionen](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Prüfungen

Die folgenden Validierungen werden durchgeführt.

1. Null überprüft und ruft die Quell- und Zielprojekte ab, um das Vorhandensein beider Projekte in der Organisation zu bestätigen.
2. Das System validiert, dass das Zielprojekt zum Kopieren gültig ist, indem es die folgenden Bedingungen überprüft:

    - Es gibt keine vorherige Aktivität für das Projekt (einschließlich der Auswahl der **Aufgaben**-Registerkarte), und das Projekt wird neu erstellt.
    - Es gibt keine vorherige Kopie, für dieses Projekt wurde kein Import angefordert, und das Projekt hat keinen **Fehler**-Status.

3. Der Vorgang wird nicht über HTTP aufgerufen.

## <a name="specify-fields-to-copy"></a>Zu kopierende Felder angeben

Wenn die Aktion aufgerufen wird, wird mit **Projekt kopieren** die Ansicht **Projektspalten kopieren** betrachtet, um zu bestimmen, welche Felder kopiert werden sollen, wenn das Projekt kopiert wird.

### <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie die benutzerdefinierte Aktion **CopyProjectV3** mit dem **removeNamedResources**-Parametersatz aufgerufen wird.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
