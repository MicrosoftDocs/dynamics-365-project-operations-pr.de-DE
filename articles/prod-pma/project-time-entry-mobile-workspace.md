---
title: Mobiler Arbeitsbereich für die Projektzeiteingabe
description: Dieses Thema bietet Informationen über die Projektzeiteingabe im mobilen Arbeitsbereich. In diesem Arbeitsbereich können Benutzer mithilfe ihrem mobilen Gerät ein Projekt eingeben und Zeit sparen.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 04024cc005b67b8f4e5821b22be65cfd1822b2414c85e1fbb75c3b2ac4339dc4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989550"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobiler Arbeitsbereich für die Projektzeiteingabe

[!include [banner](../includes/banner.md)]

Dieses Thema bietet Informationen über die **Projektzeiteingabe** im mobilen Arbeitsbereich. In diesem Arbeitsbereich können Benutzer mithilfe ihrem mobilen Gerät ein Projekt eingeben und Zeit sparen.

Dieser mobile Arbeitsbereich soll zusammen mit der Dynamics 365 Unified Ops mobile App verwendet werden. 

## <a name="overview"></a>Überblick
Im Rahmen ihrer täglichen Arbeit sind Projektressourcen häufig vor Ort oder auf Reisen. Mit dem mobilen Arbeitsbereich **Projektzeiteintrag** können Benutzer ihre abrechnungsfähige oder nicht abrechnungsfähige Zeit für ein Projekt auf einem mobilen Gerät ihrer Wahl eingeben. Daher können Projektressourcen jederzeit und überall Zeiteinträge aufzeichnen. Sie können auch bereits aufgezeichnete Zeiteinträge anzeigen. 

Insbesondere im mobilen Arbeitsbereich **Projektzeiteintrag** können Benutzer folgende Aufgaben ausführen:

-   Geben Sie für ein ausgewähltes Datum die Anzahl der Stunden ein, die Sie für eine bestimmte Aufgabe aufgewendet haben.
-   Suchen Sie nach dem Projektnamen oder Kunden, um das Projekt zu finden, für das Sie die Zeit eintragen möchten.
-   Geben Sie die Kategorie und Aktivität für die Zeit an, die Sie aufgewendet haben.
-   Notieren Sie die Zeit als abrechnungsfähig oder nicht abrechnungsfähig für das Projekt.
-   Optional geben Sie externe und interne Kommentare für die Stunden ein.

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen variieren je nach Version von Microsoft Dynamics 365, das für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Voraussetzungen, wenn Sie Dynamics 365 Finance verwenden
Wenn Finance  für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich der **Projektzeiteingabe** veröffentlichen. Anweisungen finden Sie unter [Mobile nArbeitsbereiche veröffentlichen](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Version 1611 mit Platform Update 3 oder höher verwenden
Wenn Version 1611 mit Plattform Update 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Wissensdatenbank 4018050 implementieren.</td>
<td>Systemadministrator</td>
<td>Wissensdatenbank 4018050 ist ein X ++ – Update oder ein Metadaten-Hotfix, der den mobilen Arbeitsbereich <strong>Projektzeiteintrag</strong> enthält. Um Wissensdatenbank 4018050 zu implementieren, muss Ihr Systemadministrator diese Schritte ausführen.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laden Sie den Metadaten-Hotfix von Microsoft Dynamics Lifecycle Services (LCS)</a> herunter.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadaten-Hotfix</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Erstellen Sie ein bereitstellbares Paket</a>, das die Modelle <strong>ApplicationSuite</strong> und <strong>ProjectMobile</strong> enthält und laden Sie dann das bereitstellbare Paket auf LCS hoch.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Bereitstellbares Paket anwenden</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Veröffentlichen Sie den mobilen Arbeitsbereich <strong>Projektzeiteintrag</strong>.</td>
<td>Systemadministrator</td>
<td>Anweisungen finden Sie unter <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Die mobile App herunterladen und installieren

Die mobile App Finance and Operations herunterladen und installieren:

-   [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobilen App anmelden
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie Ihre Dynamics 365-URL ein.
3.  Wenn Sie sich zum ersten Mal anmelden, werden Sie dazu aufgefordert, Ihren Benutzernamen und Ihr Passwort einzugeben. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden die verfügbaren Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass wenn Ihr Systemadministrator zu irgendeinem Zeitpunkt einen neuen Arbeitsbereich veröffentlicht, Sie die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

[![Zum Aktualisieren nach unten ziehen.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Geben Sie die Zeit über den mobilen Arbeitsbereich für die Projektzeiterfassung ein
1.  Wählen Sie auf Ihrem Mobilgerät den Arbeitsbereich **Projektzeiteintrag** aus.
2.  Wählen Sie **Zeiteintrag**. Die Kalenderdaten für die aktuelle Woche werden angezeigt.
3.  Wählen Sie für ein ausgewähltes Datum **Aktionen** &gt; **Neuer Eintrag**.
4.  Geben Sie die Anzahl der aufzunehmenden Stunden ein.
5.  Wählen Sie das Projekt für den Zeiteintrag. Eine Liste zeigt die Projekte an, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Wenn Ihr Projekt nicht in der Liste enthalten ist, wählen Sie **Suchen**. Suchen Sie nach Namen oder wechseln Sie zur Suche nach Projektnamen oder Kunde.
7.  Eine Kategorie  auswählen. Eine Liste zeigt die Kategorien an, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Wenn Ihre Kategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**. Nach Kategorie suchen oder zur Suche nach Kategorienamen wechseln.
9.  Wählen Sie eine Aktivität aus. Eine Liste zeigt die Aktivitäten an, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Wenn Ihre Aktivität nicht in der Liste enthalten ist, wählen Sie **Suchen**. Suchen Sie nach Aktivitätsnummer oder wechseln Sie zur Suche nach Zweck.

11. Wählen Sie die Eigenschaft Zeile aus.
12. Optional: geben Sie externe und interne Kommentare ein.
13. Wählen Sie **Fertig** aus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]