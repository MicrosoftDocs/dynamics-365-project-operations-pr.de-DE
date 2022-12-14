---
title: Project Operations bereitstellen Lite
description: Dieser Artikel informiert Sie darüber, wie Sie die Lite-Bereitstellung von Project Operations - Deal zur Proforma-Fakturierung installieren können.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810977"
---
# <a name="deploy-project-operations-lite"></a>Project Operations bereitstellen Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_



Project Operations unterstützt mehrere Bereitstellungsmodelle. Informationen zum Ermitteln des besten Bereitstellungsmodells finden Sie unter [Bereitstellungstypen](determine-deployment-type.md).


> [!IMPORTANT]
> Diese Bereitstellung, Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung führt zu einer reinen **Dataverse-Bereitstellung von Project Operations**.

- [Project Operations in einer neuen Dataverse-Umgebung installieren](#new)
- [In einer vorhandenen Dataverse-Umgebung installieren](#existing)
- [Installation in einer vorhandenen Dataverse Umgebung mit Dual-Write-Komponenten](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Lite in einer neuen Dataverse-Umgebung installieren

1. Als der [Globale oder Power Platform-Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz erstellen Sie eine neue Dataverse-Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com). Stellen Sie sicher, dass **Datenbank für diese Umgebung erstellen** und **Dynamics 365-Apps** aktiviert sind. Weitere Informationen finden Sie unter [Erstellen und Verwalten von Umgebungen im Power Platform-Admin Center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Wählen Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Lite in einer vorhandenen Dataverse-Umgebung installieren 
1. Als der [globale oder Power Platform-Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz suchen Sie die Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com), wo Sie Project Operations installieren möchten.
1. Installieren Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps. Weitere Informationen finden Sie unter [Verwalten von Dynamics 365-Apps](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installieren Sie Project Operations Lite in einer vorhandenen Dataverse Umgebung, in der bereits duale Schreiblösungen vorhanden sind

Wenn Sie Project Operations weiterhin im Lite-Bereitstellungsmodus ausführen möchten, sollten Sie die folgenden Schritte ausführen:

1. Als der [globale oder Power Platform-Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz suchen Sie die Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com), wo Sie Project Operations installieren möchten.
1. Installieren Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps. Weitere Informationen finden Sie unter [Verwalten von Dynamics 365-Apps](/power-platform/admin/manage-apps).
1. Da in Ihrer Umgebung duale Schreibkomponenten vorhanden sind, die bei der Integration in Finanz- und Betriebs-Apps helfen, installiert die Installation von Project Operations auch die Funktionen und Erweiterungen, die zum Integrieren von projektbezogenen Daten in Finanz- und Betriebs-Apps erforderlich sind. Da Sie Project Operations in einer Lite-Bereitstellung ausführen möchten, sollten diese Integrationskomponenten entfernt werden, da sie Einschränkungen und Mehraufwand für Lite-Bereitstellungsszenarien verursachen. Deinstallieren Sie die Lösungen **Dynamics 365 Project Operations Duales Schreiben** und **Dynamics 365 Project Operations Duales Schreiben Entitäskarten** manuell, um diese Komponenten zu entfernen.
1. Gehen Sie zu **Project Operations -> Einstellungen -> Parameter**. Öffnen Sie die Detailseite **Projektparameter** und setzen Sie das Feld **Lösungs-Upgrade-Verhalten** auf **Lite Nur**. Dadurch wird sichergestellt, dass nachfolgende Upgrades von Project Operations die Integrationskomponenten nicht wieder in Project Operations zurückbringen.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
