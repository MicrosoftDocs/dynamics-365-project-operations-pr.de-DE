---
title: Projektvorlagen mit Projekt kopieren erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Projektvorlagen mithilfe der benutzerdefinierten Aktion „Projekt kopieren“.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989251"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektvorlagen mit Projekt kopieren erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations unterstützt die Möglichkeit, ein Projekt zu kopieren und alle Zuweisungen auf die allgemeinen Ressourcen zurückzusetzen, die die Rolle darstellen. Kunden können diese Funktionalität verwenden, um grundlegende Projektvorlagen zu erstellen.

Wenn Sie **Projekt kopieren** auswählen, wird der Status des Zielprojekts aktualisiert. Verwenden Sie **Statusgrund**, um festzustellen, wann die Kopieraktion abgeschlossen ist. Durch Auswahl von **Projekt kopieren** wird auch das Startdatum des Projekts auf das aktuelle Startdatum aktualisiert, wenn in der Zielprojektentität kein Zieldatum erkannt wird.

## <a name="copy-project-custom-action"></a>Benutzerdefinierte Aktion „Projekt kopieren“ 

### <a name="name"></a>Name des Dataflows 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Eingabeparameter
Es gibt drei Eingabeparameter:

| Parameter          | Art   | Werte                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** oder **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitätsreferenz | Quellprojekt |
| Zielsprache             | Entitätsreferenz | Zielprojekt |


- **{"clearTeamsAndAssignments":true}**: Das Standardverhalten für Project für das Web. Dadurch werden alle Arbeitsaufträge und Teammitglieder entfernt.
- **{"removeNamedResources":true}** Das Standardverhalten für Project Operations, bei dem Zuweisungen zu generischen Ressourcen zurückgesetzt werden.

Weitere Standardinformationen über Aktionen finden Sie unter [Nutzen von Web-API-Aktionen](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

## <a name="specify-fields-to-copy"></a>Zu kopierende Felder angeben 
Wenn die Aktion aufgerufen wird, wird mit **Projekt kopieren** die Ansicht **Projektspalten kopieren** betrachtet, um zu bestimmen, welche Felder kopiert werden sollen, wenn das Projekt kopiert wird.


### <a name="example"></a>Beispiel
Das folgende Beispiel zeigt, wie Sie die benutzerdefiniert Aktion **Projekt kopieren** mit dem Parametersatz **removeNamedResources** aufrufen können.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]