---
title: Manuelles Bereitstellen der App Project Operations Dataverse mit Dual-Write-Unterstützung
description: In diesem Thema wird erklärt, wie Sie die App Project Operations Dataverse manuell bereitstellen, sodass sie Dual-Write unterstützt.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986445"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Manuelles Bereitstellen der App Project Operations Dataverse mit Dual-Write-Unterstützung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In diesem Thema wird erklärt, wie Sie Microsoft Dynamics 365 Project Operations in Microsoft Dataverse manuell bereitstellen, sodass es Dual-Write unterstützt. Project Operations erkennt die Konfiguration der Umgebung und fügt zusätzliche Unterstützung für Dual-Write hinzu, wenn die Voraussetzungen dafür erfüllt sind.

Wenn Sie beim Bereitstellen über Microsoft Dynamics Lifecycle Services (LCS) die Anweisungen in diesem Thema befolgt haben, können Sie das Bereitstellen der Microsoft Power Platform-Integration (früher als Common Data Service-Umgebung bezeichnet) überspringen.

Der Prozess des Bereitstellens von Project Operations in Dataverse, sodass es Dual-Write unterstützt, hat vier Hauptschritte:

1. [Erstellen Sie eine neue Umgebung in Dataverse, die Dual-Write unterstützt](#create).
2. [Hinzufügen von Dual-Write-Voraussetzungen zur Umgebung](#prerequisites).
3. [Fügen Sie die App Project Operations Dataverse hinzu](#dataverse).
4. [Verknüpfen Sie Ihre Umgebungen](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Erstellen Sie eine neue Umgebung in Dataverse, die Dual-Write unterstützt

Um diesen Vorgang abzuschließen, müssen Sie sich als Administrator anmelden.

1. Öffnen Sie das [Power Platform Admin-Center](https://admin.powerplatform.com), und melden Sie sich als Administrator an.
2. Erstellen Sie eine neue Umgebung, und benennen Sie sie.
3. Wählen Sie den Typ der Umgebung. Wenn Sie sich für das Test-Angebot angemeldet haben, wählen Sie **Test (abonnementbasiert)**.
4. Bestätigen Sie die Bereitstellungsregion.
5. Aktivieren Sie die Option **Erstellen Sie eine Datenbank für diese Umgebung**. 
6. Bestätigen Sie die Sprache, und bestätigen Sie, dass die Währung mit der Währung für Ihre Finance and Operations-Apps übereinstimmt.
7. Aktivieren Sie die Option **Dynamics 365 Apps** und bestätigen Sie, dass das Feld **Automatisch diese Apps bereitstellen** auf **Keine** festgelegt ist.
8. Fügen Sie eine Sicherheitsgruppe hinzu, wenn eine Sicherheitsgruppe erforderlich ist.
9. Wählen Sie **Speichern** aus, um die Umgebung zu erstellen.
10. Warten Sie, bis die Bereitstellung abgeschlossen ist und die Umgebung den Status **Bereit** erreicht.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Hinzufügen von Dual-Write-Voraussetzungen zur Umgebung

Die Dual-Write-Unterstützung umfasst zusätzliche Felder, die zu wichtigen Entitäten hinzugefügt werden, wie z. B. die Entität **Firma**. Wenn Sie die Dual-Write-Unterstützung zu einer bestehenden Umgebung hinzufügen, müssen Sie möglicherweise die Daten aktualisieren, um die Unterstützung zu aktivieren. Informationen darüber, wie Sie die Daten booten können, finden Sie unter [Bootstrap-Firmendaten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Weitere Informationen über Dual-Write finden Sie unter [Systemanforderungen für Dual-Write](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Führen Sie dieses Verfahren aus, um die Dual-Write-Voraussetzungen zu Ihrer Umgebung hinzuzufügen.

1. Öffnen Sie die Umgebung, die Sie gerade erstellt haben, und gehen Sie dann zu **Ressourcen** \> **Dynamics 365 Apps**.
2. Wählen Sie **Dual-write Kernlösung** in der App-Liste und installieren Sie sie.
3. Warten Sie, bis die Installation abgeschlossen ist. Wählen Sie dann **Dual-write Orchestrierungslösung für die Anwendung** in der App-Liste und installieren Sie sie.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Hinzufügen der Project Operations Dataverse-App

Sie können diesen Vorgang nur abschließen, wenn Sie die vorherigen Vorgänge abgeschlossen haben, bevor Sie Project Operations installiert haben. Während der Installation analysiert das System die Umgebungskonfiguration und fügt Unterstützung für Dual-Write hinzu, wenn dies erforderlich ist.

1. Öffnen Sie die Umgebung, die Sie zuvor erstellt haben, und gehen Sie dann zu **Ressource** \> **Dynamics 365 Apps**.
2. Wählen Sie **Microsoft Dynamics 365 Project Operations** in der App-Liste und installieren Sie sie.

## <a name="link-your-environments"></a><a name="link"></a>Verknüpfen Sie Ihre Umgebungen

Nachdem die Dataverse-Umgebung bereitgestellt ist, können Sie die Verknüpfung in Ihren Finance and Operations-Apps festlegen. Führen Sie die Schritte unter [Verwenden Sie den Assistenten zum Verknüpfen Ihrer Umgebungen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment) aus.
