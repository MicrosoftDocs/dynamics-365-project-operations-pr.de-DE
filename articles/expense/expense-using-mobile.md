---
title: Mobile Ausgaben-App
description: Dieses Thema bietet Informationen über die Ausgabenverwaltung im mobilen Arbeitsbereich.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 01df30bf48fa9118771b87363d0418eb6b49ecea
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499895"
---
# <a name="mobile-expense-app"></a>Mobile Ausgaben-App

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dieses Thema bietet Informationen über die **Ausgabenverwaltung** im mobilen Arbeitsbereich. Mit diesem Arbeitsbereich können Benutzer einen Beleg erfassen und hochladen, um ihn später zu einem Spesenbericht hinzuzufügen. Benutzer können mithilfe einer angehängten Quittung auch schnell eine Ausgabenzeile erstellen und ihre Spesenabrechnungen erstellen und verwalten. Darüber hinaus können Genehmigende den mobilen Arbeitsbereich **Ausgabenmanagement** nutzen zum Anzeigen der ihnen zugewiesenen Spesenabrechnungen und zum Genehmigen oder Ablehnen dieser Spesenabrechnungen.

Dieser mobile Arbeitsbereich soll zusammen mit der Dynamics 365 Unified Ops mobile App verwendet werden.

Viele Organisationen verlangen, dass eine Kopie einer Quittung einer reisebezogenen oder geschäftlichen Ausgabenabrechnung beigefügt wird, die ein Mitarbeiter zur Erstattung einreicht. Mit dem mobilen Arbeitsbereich **Ausgabenmanagement** können Benutzer schnell neue Spesenabrechnungen auf dem mobilen Gerät ihrer Wahl erstellen, indem sie ein beigefügtes Foto einer Quittung verwenden. Alternativ können Benutzer ein Foto einer Quittung aufnehmen und später an eine Ausgabenabrechnung anhängen. Mitarbeiter können auch ihre Ausgabenabrechnungen erstellen und verwalten und sie dann mithilfe ihres Mobilgeräts zur Genehmigung und Erstattung einreichen.

Insbesondere der mobile Arbeitsbereich **Ausgabenmanagement** lässt Benutzer folgende Aufgaben ausführen:

- Machen Sie ein Foto von einer Quittung. Laden Sie das Belegfoto hoch und fügen Sie es später einer Ausgabenabrechnung bei.
- Laden Sie eine Datei als erfasste Quittung hoch. Sie können diese Datei später an eine Ausgabenabrechnung anhängen.
- Erstellen Sie eine neue Ausgabenzeile mithilfe einer beigefügten Quittung. Sie können die Position später zu einer Ausgabenabrechnung hinzufügen und zur Genehmigung und Erstattung einreichen.

Sie können diese Funktionem auch für folgende Aufgaben verwenden:

- Erstellen eines neuen Ausgabenberichts.
- Fügen Sie Kreditkartentransaktionen und andere zuvor erstellte Ausgaben einer Spesenabrechnung hinzu.
- Erstellen Sie neue Ausgaben für eine Spesenabrechnung.
- Fügen Sie einer Ausgabenabrechnung eine Quittung bei, indem Sie entweder ein Foto der Quittung aufnehmen oder eine Datei als erfasste Quittung hochladen.
- Fügen Sie abhängig von der Ausgabenrichtlinie des Unternehmens die Liste der Gäste zu einer Ausgabe hinzu.
- Führen Sie die Ausgaben abhängig von der Ausgabenrichtlinie des Unternehmens auf.
- Senden Sie eine Ausgabenabrechnung zur Genehmigung und Erstattung.
- Genehmigen oder lehnen Sie Ausgabenabrechnungen ab, für die Sie ein zugeordneter Genehmiger sind.

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen variieren je nach Version, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Voraussetzungen, wenn Sie Dynamics 365 Finance verwenden 
Wenn Finance für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich der **Ausgabenverwaltung** veröffentlichen. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Version 1611 mit Plattform Update 3 oder höher verwenden
Wenn Version 1611 mit Plattform Update 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator auch die folgenden Voraussetzungen erfüllen. 

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung des Dataflows</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wissensdatenbank 4019015 implementieren.</td>
<td>Systemadministrator</td>
<td>Wissensdatenbank 4019015 ist ein X ++ – Update oder ein Metadaten-Hotfix, der den mobilen Arbeitsbereich <strong>Ausgabenverwaltung</strong> enthält. Um Wissensdatenbank 4019015 zu implementieren, muss Ihr Systemadministrator diese Schritte ausführen.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laden Sie Updates von Lifecycle Services herunter</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadaten-Hotfix</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Erstellen Sie ein bereitstellbares Paket</a>, das die Modelle <strong>ApplicationSuite</strong> und <strong>ExpenseMobile</strong> enthält und laden Sie dann das bereitstellbare Paket auf LCS hoch.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Bereitstellbares Paket anwenden</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Veröffentlichen Sie den mobilen Arbeitsbereich <strong>Ausgabenmanagement</strong>.</td>
<td>Systemadministrator</td>
<td>Anweisungen finden Sie unter <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Laden Sie die Dynamics 365 Unified Ops mobile App herunter und installieren Sie sie
Laden Sie die Dynamics 365 Unified Ops mobile App herunter und installieren Sie sie:

- [Für Android-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
- [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobilen App anmelden
1. Starten Sie die App auf Ihrem mobilen Gerät.
2. Geben Sie Ihre Dynamics 365-URL ein.
4. Wenn Sie sich zum ersten Mal anmelden, werden Sie dazu aufgefordert, Ihren Benutzernamen und Ihr Passwort einzugeben. Geben Sie Ihre Anmeldeinformationen ein.
5. Nachdem Sie sich angemeldet haben, werden die verfügbaren Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass wenn Ihr Systemadministrator zu irgendeinem Zeitpunkt einen neuen Arbeitsbereich veröffentlicht, Sie die Liste der mobilen Arbeitsbereiche ebenfalls aktualisieren müssen.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Erfassen Sie eine Quittung mithilfe des mobilen Arbeitsbereichs für die Ausgabenverwaltung

1. Öffnen Sie den Arbeitsbereich der **Ausgabenverwaltung** auf Ihrem mobilen Gerät.
2. Wählen Sie **Quittung erfassen**.
3. Wählen Sie **Foto machen** oder **Bild auswählen**.
4. Folgen Sie einen der folgenden Schritte:

   - Wenn Sie **Foto machen** ausgewählt haben, folgen Sie diesen Schritten:

      1. Sie werden auf Ihrem Mobilgerät zur Kamera geführt, damit Sie ein Foto von der Quittung machen können. 
      2. Wenn Sie mit dem Aufnehmen eines Fotos fertig sind, wählen Sie **OK**, um das Foto anzunehmen.
      3. Optional: Geben Sie einen Namen für das Foto ein und geben Sie Notizen ein.

    - Wenn Sie **Bild auswählen** ausgewählt haben, folgen Sie diesen Schritten:

        1. Wählen Sie ein Bild auf der Liste aus.
        2. Optional: Geben Sie einen Namen für das Bild ein und geben Sie Notizen ein.

5. Wählen Sie **Fertig** aus.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Erfassen Sie eine Ausgabe mithilfe des mobilen Arbeitsbereichs für die Ausgabenverwaltung

1. Öffnen Sie den Arbeitsbereich der **Ausgabenverwaltung** auf Ihrem mobilen Gerät.
2. Wählen Sie **Schnelle Ausgabenerfassung**.
3. Wählen Sie die Ausgabenkategorie. Sie sehen eine Liste der Ausgabenkategorien, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihre Kategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Nach Ausgabenkategorie suchen oder zur Suche nach Ausgabentyp wechseln.
4. Geben Sie das Transaktionsdatum der Ausgabe ein.
5. Optional: Geben Sie den Händler für die Augabe ein.
6. Geben Sie den Geldbetrag für die Ausgabe ein.
7. Wählen Sie die Währung der Ausgabe. Sie sehen eine Liste der Währungscodes, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 400 Währlungen geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihre Währung nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Nach Währung suchen oder zur Suche nach Kategorienamen wechseln.
8. Wählen Sie **Foto machen** oder **Bild auswählen**.
9. Folgen Sie einen der folgenden Schritte:

    - Wenn Sie **Foto aufnehmen** ausgewählt haben, werden Sie auf Ihrem Mobilgerät zur Kamera geführt, damit Sie ein Foto von der Quittung machen können. Wenn Sie mit dem Aufnehmen eines Fotos fertig sind, wählen Sie **OK**, um das Foto anzunehmen.
    - Wenn Sie **Bild auswählen** wählen, wählen Sie ein Bild in der Liste aus.

10. Wählen Sie **Fertig** aus.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Genehmigen Sie eine Ausgabenabrechnung mithilfe des mobilen Arbeitsbereichs für die Ausgabenverwaltung (wenn Sie das Update vom Juli 2017 verwenden)

1. Öffnen Sie den Arbeitsbereich der **Ausgabenverwaltung** auf Ihrem mobilen Gerät.
2. **Ausgabengenehmigungen** zeigt die Anzahl der Ausgabenabrechnungen an, die Ihnen zur Genehmigung zugewiesen wurden. Die Nummer wird ungefähr alle 30 Minuten aktualisiert. Wählen Sie **Ausgabengenehmigungen**.

    Die Liste der Ausgabengenehmigungen zeigt die Anzahl der Ausgabenabrechnungen an, die Ihnen zur Genehmigung zugewiesen wurden.
    
3. Wählen Sie eine Ausgabenabrechnung aus, um die Ausgabemabrechnungen anzuzeigen.
4. Wählen Sie eine Ausgabe aus, um die Details anzuzeigen. Die Informationen, die für eine Ausgabe angezeigt werden, umfassen alle Beleg-, Gast- und Auflistungsdetails.
5. Zurück auf der **Ausgabenabrechnung** wählen Sie auf dieser Seite aus, ob der Ausgabenbericht genehmigt oder abgelehnt werden soll.
6. Geben Sie Kommentare für die Genehmigungsaktion ein.
7. Wählen Sie **Fertig** aus.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Erstellen Sie einen neuen Ausgabenbericht und übermitteln Sie diesen zur Genehmigung mithilfe des mobilen Arbeitsbereichs für die Ausgabenverwaltung (wenn Sie das Update vom Juli 2017 verwenden)

1. Öffnen Sie den Arbeitsbereich der **Ausgabenverwaltung** auf Ihrem mobilen Gerät.
2. Wählen Sie **Ausgabenerfassung**.
3. Wählen **Neuer Bericht** oder wählen Sie eine vorhandene Ausgabenabrechnung in der Liste aus.
4. Geben Sie für neue Ausgabenabrechnungen den Zweck und alle verfügbaren zusätzlichen Informationen ein. Diese Informationen variieren je nachdem, wie die Ausgabenverwaltung für Ihr Unternehmen konfiguriert ist.
5. Wählen Sie **Fertig** aus.
6. Wählen Sie aus, um vorhandene Ausgaben, z. B. Kreditkartentransaktionen, zur Ausgabenabrechnung hinzuzufügen und wählen Sie **Anfügen**.
7. Wählen Sie oder mehrere Ausgaben aus der Liste aus.
8. Wählen Sie **Fertig** aus.
9. Um eine neue Ausgabe dem Ausgabenbericht hinzuzufügen, wählen Sie **Neue Ausgaben**.
10. Wählen Sie die Ausgabenkategorie für die Ausgabe. Sie sehen eine Liste der Ausgabenkategorien, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihre Kategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Nach Ausgabenkategorie suchen oder zur Suche nach Ausgabentyp wechseln.
11. Optional: Geben Sie den Händler für die Augabe ein.
12. Geben Sie das Transaktionsdatum der Ausgabe ein.
13. Geben Sie den Geldbetrag für die Ausgabe ein.
14. Wählen Sie die Währung der Ausgabe. Sie sehen eine Liste der Währungscodes, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 400 Währlungen geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihre Währung nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Nach Währung suchen oder zur Suche nach Kategorienamen wechseln.
15. Wählen Sie **Fertig** aus.
16. Um weitere Details zu den Ausgaben hinzuzufügen, wählen Sie **Fügen Sie weitere Details hinzu**. Die verfügbaren Felder hängen von der Konfiguration des Ausgabenmanagements für Ihr Unternehmen ab.
17. Wenn für die Unternehmensrichtlinie eine Quittung für die Ausgaben erforderlich ist, wählen Sie **Quittungen** und befolgen Sie dann diese Schritte:

    1. Wählen Sie **Quittung erfassen** oder **Quittung beifügen**.
    2. Folgen Sie einen der folgenden Schritte:

        - Wenn Sie **Quittung erfassen** ausgewählt haben, folgen Sie diesen Schritten:

            1. Wählen Sie **Foto machen** oder **Bild auswählen**.
            2. Folgen Sie einen der folgenden Schritte:

                - Wenn Sie **Foto machen** ausgewählt haben, folgen Sie diesen Schritten:

                    1. Sie werden auf Ihrem Mobilgerät zur Kamera geführt, damit Sie ein Foto von der Quittung machen können. Wenn Sie mit dem Aufnehmen eines Fotos fertig sind, wählen Sie **OK**, um das Foto anzunehmen.
                    2. Optional: Geben Sie einen Namen für das Foto ein und geben Sie Notizen ein.

                - Wenn Sie **Bild auswählen** ausgewählt haben, folgen Sie diesen Schritten:

                    1. Wählen Sie ein Bild auf der Liste aus.
                    2. Optional: Geben Sie einen Namen für das Bild ein und geben Sie Notizen ein.

            3.  Wählen Sie **Fertig** aus.

        - Wenn Sie **Quittung anhängen** ausgewählt haben, folgen Sie diesen Schritten:

            1.  Wählen Sie in der Liste ein Bild oder mehrer Bilder aus.
            2.  Wählen Sie **Fertig** aus.

    3. Wählen Sie die Schaltfläche **Zurück**, um zu den Ausgabendetails zurückzukehren.

18. Wenn für die Unternehmensrichtlinie Gäste erforderlich sind, wählen Sie **Gäste** und befolgen Sie dann diese Schritte:

    1. Wählen Sie **Gast**, **Vorheriger Gast**, oder **Mitarbeiter**.
    2. Folgen Sie einen der folgenden Schritte:

        - Wenn Sie **Gast** und folgen Sie diesen Schritten:

            1. Geben Sie den Namen des Gastes ein.
            2. Optional: Geben Sie die Organisation und/oder das Land des Gastes ein.
            3. Optional: Geben Sie den Titel des Gastes ein.
            4. Wählen Sie **Fertig** aus.

        - Wenn Sie **Vorheriger Gast** und folgen Sie diesen Schritten:

            1. Wählen Sie in der Liste einen oder mehrere frühere Gäste aus. Sie sehen eine Liste früherer Gäste, die Sie zu früheren Spesenabrechnungen hinzugefügt haben, die zur Offline-Verwendung in Ihre App geladen wurden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihr früherer Gast nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Suchen Sie nach Namen oder wechseln Sie zur Suche nach Organisation, Land oder Titel.
            2. Wählen Sie **Fertig** aus.

        - Wenn Sie **Kollege** wählen, folgen Sie diesen Schritten:

            1. Wählen Sie in der Liste mindestens einen Kollegen aus. Sie sehen eine Liste der Kollegen, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihr Kollege nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Suchen Sie nach Namen oder wechseln Sie zur Suche nach Unternehmen, Land oder Titel.
            2. Wählen Sie **Fertig** aus.

    3. Wählen Sie die Schaltfläche **Zurück**, um zu den Ausgabendetails zurückzukehren.

19. Wenn für die Unternehmensrichtlinie eine Quittung für die Ausgaben erforderlich ist, wählen Sie **Quittungen** und folgen Sie dann diesen Schritte:

    1. Wählen Sie das erste Datum aus, das aufgelistet werden soll.
    2. Wählen Sie **Auflistung hinzufügen** aus.
    3. Wählen Sie die Unterkategorie für die Ausgabenauflistung aus. Sie sehen eine Liste der Unterkategorien, die zur Offline-Verwendung in Ihre App geladen werden. Standardmäßig werden 50 Elemente geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sehen Entwickler unter [Mobile Plattform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Wenn Ihre Unterkategorie nicht in der Liste enthalten ist, wählen Sie **Suchen**, um eine Online-Suche zu machen. Suche nach Ausgabenunterkategorienamen.
    4. Geben Sie den Transaktionsbetrag für die Auflistung ein.
    5. Bearbeiten Sie das Transaktionsdatum, falls erforderlich.
    6. Wählen Sie **Fertig** aus.
    7. Wiederholen Sie die vorherigen Schritte, bis Sie alle Elemente für das ausgewählte Datum hinzugefügt haben.
    8. Für weitere Tage können Sie **Auf den nächsten Tag kopieren** auswählen, um die Auflistungen auf den nächsten Tag zu kopieren. Alternativ können Sie das Datum für die Auflistung auswählen und dann wie beim ersten Datum Auflistungen hinzufügen.
    9. Nachdem Sie die Kosten aufgelistet haben, wählen Sie die **Zurück** Schaltfläche, um zu den Kostendetails zurückzukehren.

20. Wählen Sie die Schaltfläche **Zurück**, um zur Seite **Ausgabenbericht** zurückzukehren.
21. Wiederholen Sie die vorherigen Schritte, bis Sie alle Ausgaben hinzugefügt haben.
22. Wählen Sie **Übermitteln** aus.
23. Geben Sie Kommentare für die genehmigende Person ein.
24. Wählen Sie **Fertig** aus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
