---
title: Project Operations bereitstellen – Lite
description: Dieser Artikel informiert Sie darüber, wie Sie die Lite-Bereitstellung von Project Operations - Deal zur Proforma-Fakturierung installieren können.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930317"
---
# <a name="deploy-project-operations---lite"></a>Project Operations bereitstellen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_



Project Operations unterstützt mehrere Bereitstellungsmodelle. Informationen zum Ermitteln des besten Bereitstellungsmodells finden Sie unter [Bereitstellungstypen](determine-deployment-type.md).


> [!IMPORTANT]
> Diese Bereitstellung, Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung führt zu einer reinen **Dataverse-Bereitstellung von Project Operations**.

- [Project Operations in einer neuen Dataverse-Umgebung installieren](#new)
- [In einer vorhandenen Dataverse-Umgebung installieren](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations in einer neuen Dataverse-Umgebung installieren

1. Als der [Globale oder Power Platform-Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz erstellen Sie eine neue Dataverse-Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com). Stellen Sie sicher, dass **Datenbank für diese Umgebung erstellen** und **Dynamics 365-Apps** aktiviert sind. Weitere Informationen finden Sie unter [Erstellen und Verwalten von Umgebungen im Power Platform-Admin Center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Wählen Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations in einer vorhandenen Dataverse-Umgebung installieren
1. Stellen Sie sicher, dass die Umgebung nicht mit [duales Schreiben](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) konfiguriert wurde, da die Installation dann die Funktionen [Project Operations für ressourcen-/nicht lagerbasierte Szenarien](project-operations-integrated-deployment-overview.md) installiert.
2. Als der [globale oder Power Platform-Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz suchen Sie die Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com), wo Sie Project Operations installieren möchten.
3. Installieren Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps. Weitere Informationen finden Sie unter [Verwalten von Dynamics 365-Apps](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
