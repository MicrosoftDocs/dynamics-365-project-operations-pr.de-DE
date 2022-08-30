---
title: Synchronisieren Sie den Projektstatus, um den Eintrag für geschlossene Projekte zu verhindern
description: In diesem Artikel wird erläutert, wie Sie den Projektstatus synchronisieren, um den Zugriff auf inaktive oder geschlossene Projekte zu verhindern.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348020"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synchronisieren Sie den Projektstatus, um den Eintrag für geschlossene Projekte zu verhindern

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

## <a name="scenario"></a>Szenario

Contoso wird mit Microsoft Dynamics 365 Project Operations für Szenarios mit Ressourcen/nicht auf Lager live geschaltet. Im Rahmen der normalen Geschäftstätigkeit können Projekte abgeschlossen oder ausgesetzt werden. Sie können das Projekt deaktivieren, um sicherzustellen, dass keine Ausgaben oder Rechnungen generiert werden.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Anforderungen

-   Microsoft Dynamics 365 Finance 10.0.29 oder höher muss installiert sein.
-   Dual Write Map 1.0.0.3 für Projects V2 (msdyn\_projects) müssen wie unten beschrieben installiert oder manuell konfiguriert werden.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Eine aktualisierte Version der Zuordnung für duales Schreiben für Project V2 Project Operations-Integrationsvertragsposition erstellen

Aktualisieren der Project Operations Projects V2 Zuordnung für duales Schreiben:

1. Gehen Sie zu **duales Schreiben** im Arbeitsbereich und wählen Sie **Datenverwaltung** aus.
2. Wählen Sie die Kachel **Duales Schreiben** aus.
3. Aus der Spalte **Tabellenzuordnung** suchen und auswählen **Projekt V2 (msdyn\_projects)**, und wählen Sie dann Stopp aus.
4. Wählen Sie den Kartennamen aus, um die Karte zu öffnen, und wählen Sie dann **[Keiner]** aus.
5. Wählen Sie im Dialogfeld Spalte **satecode \[Projekt Status\]** und wählen Sie dann OK. Sie können tippen **Status** im Filterwert, um die Liste einzugrenzen.
6.  Wählen Sie **Transformation hinzufügen oder bearbeiten** in der Spalte **Kartentyp**, um die Transformation zu bearbeiten.
7.  Wählen Sie aus **Transformationstyp** **ValueMap** aus.
8.  Wählen Sie **Wertzuordnung hinzufügen**, und fügen Sie dann folgende **Schlüssel** und **Werte** hinzu:

   Key       | Wert 
   ----------|-------
   InProcess | 0     
   abgeschlossen | 1     

![Screenshot der Dual Write-Zuordnung](media/projectstage-dw-mapping.png)

9. Wählen Sie **Save** (Speichern).
10. Wählen Sie oben auf der Seite **Duales Schreiben > Projekte V2 (msdyn_projects)** die Option **Speichern als** aus.
11. Wählen Sie im Bereich **Tabelle hinzufügen** im Feld **Verleger** **CSD-Standardherausgeber**.
12. Setzen Sie das Feld **Version** auf 1.0.0.3.
13. Geben Sie eine **Beschreibung** ein und wählen Sie dann **Speichern**.
14. Wählen Sie oben auf der Seite **Duales Schreiben > Projekte V2 (msdyn_projects)** die Option **Ausführen** aus, um die Karte zu starten, und wählen Sie dann **Ja** wenn Sie vor dem Lauf zur Bestätigung aufgefordert werden. 

### <a name="close-a-newly-completed-project"></a>Schließen Sie ein neu abgeschlossenes Projekt ab

Dynamics 365 Finance verwendet das Feld **Projektphase**, um zwischen Projekten in **in Bearbeitung** oder **fertig** zu unterscheiden. **Fertige** Projekte können keine Kosten verursachen oder Kunden in Rechnung gestellt werden.

1. Öffnen Sie ein Projekt, um es zu deaktivieren.
2. Wählen Sie aus dem Menüband **Deaktivieren**.

> [!NOTE]
> Sie können ein Projekt entweder deaktivieren oder schließen, da sich beide im Finanzkontext gleich verhalten.

3. Öffnen Sie in Finance die Seite **Liste aller Projekte**.
4. Bestätigen Sie, dass das deaktivierte Projekt nicht in der Liste erscheint.
5. Ändern Sie im Filter über der Liste **Projekte zeigen** den Wert von **Aktiv** zu **Alle**.
6. Sie sehen nun das deaktivierte Projekt.

Wenn Sie versuchen, Zeit oder Ausgaben für dieses Projekt in Finance zu protokollieren, sollten Sie das Projekt nicht zur Auswahl sehen. Wenn Sie die Projektnummer bei einer Ausgabe manuell eingeben, wird eine Meldung wie „Projektphase abgeschlossen erlaubt keine Aufzeichnung im Projekt“ angezeigt. Rechnungsstellung und andere Abrechnungsfunktionen sollten deaktiviert werden, da sie im Kontext eines abgeschlossenen Projekts sein werden.

