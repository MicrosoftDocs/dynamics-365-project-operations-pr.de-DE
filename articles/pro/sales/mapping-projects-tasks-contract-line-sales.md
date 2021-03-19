---
title: Projekte und Aufgaben einer projektbasierten Vertragszeile zuordnen – Lite
description: Dieses Thema enthält Informationen zum Hinzufügen und Entfernen von Projekten und Aufgaben zu einer Vertragszeile.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c29872ef3d62780eea3c0eda48c8fd2a9af4b1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272792"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Projekte und Aufgaben einer projektbasierten Vertragszeile zuordnen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In projektbasierten Vertragszeilen können Sie der Vertragszeile bestimmte Aufgaben in einem Projekt zuordnen.

Wenn Sie einer Vertragszeile bestimmte Aufgaben zuordnen, gelten die Abrechnungsmethode, die Gebührenoptionen, die nicht zu überschreitenden Grenzwerte und die in der Vertragszeile definierten Kunden nur für diese bestimmten Aufgaben.

Wenn Sie ein Szenario haben, in dem eine Phase eines Projekts, z. B. die Prototypphase, ein Festpreis ist und alle anderen Phasen Zeit und Material sind, können Sie die Prototypphase und alle zugehörigen untergeordneten Aufgaben der Vertragszeile zuordnen für diese Phase mit einer Festpreisabrechnungsmethode.

Alle anderen Phasen Ihres Projektstrukturplans (PSP) können der zeit- und materialbasierten Vertragszeile zugeordnet werden.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Aufgaben projektbasierten Vertragszeilen zuweisen

Aufgaben können Vertragszeilen aus der **Fakturierbare Aufgaben**-Registerkarte auf der **Vertragszeile**-Seite oder der **Aufgabenabrechnung**-Registerkarte auf der **Projekt**-Seite zugeordnet werden.

### <a name="from-the-contract-line-page"></a>Von der Vertragszeilenseite

Führen Sie die folgenden Schritte aus, um Projektaufgaben der Vertragszeile von der **Fakturierbare Aufgaben**-Registerkarte der **Vertragszeile**-Seite zu verknüpfen.

1. Überprüfen Sie auf der **Allgemein**-Registerkarte auf einer projektbasierten Vertragszeile, ob das **Projekt**-Feld ausgefüllt ist.
2. Im feld **Enthaltene Aufgaben** wählen Sie das Feld **Nur ausgewählte Aufgaben** aus.
3. Speichern Sie Ihre Änderungen. Das Formular wird aktualisiert und die **Fakturierbare Aufgaben**-Registerkarte wird angezeigt.
4. Wählen Sie die **Fakturierbare Aufgaben**-Registerkarte und dann im Unterraster die Option **Eine Vertragszeilenaufgabe hinzufügen** aus.
5. Wählen Sie auf der **Vertragszeilenaufgaben**-Seite im **Aufgaben**-Dropdownmenü die Aufgabe aus. 
6. Geben Sie Informationen in das Feld **Fakturierungstyp** ein und wählen Sie dann **Speichern und schließen**. Die ausgewählte Aufgabe ist der Vertragszeile zugeordnet.

> [!NOTE]
> Dies ist nicht die optimalste Erfahrung, um Projektaufgaben Vertragszeilen zuzuordnen. Jedes Projekt muss in dieser Erfahrung manuell zugeordnet werden. Der bevorzugte Weg ist über die **Aufgabenfakturierung**-Registerkarte auf der **Projekt**-Seite.

### <a name="from-the-project-page"></a>Über die Seite „Projekt“

Dies ist die optimale Methode, um Aufgaben Vertragszeilen zuzuordnen. Sie können mehrere Aufgaben auswählen und all diese und ihre untergeordneten Aufgaben der ausgewählten Vertragszeile zuordnen. Führen Sie die folgenden Schritte aus, um Aufgaben der Vertragszeile über die **Projekt**-Seite zu verknüpfen.

1. Überprüfen Sie auf der **Allgemein**-Registerkarte auf einer projektbasierten Vertragszeile, ob das **Projekt**-Feld ausgefüllt ist.
2. Im Feld **Enthaltene Aufgaben** wählen Sie das Feld **Nur ausgewählte Aufgaben** aus.
3. Speichern Sie die projektbasierte Vertragszeile. Das Formular wird aktualisiert und die **Fakturierbare Aufgaben**-Registerkarte wird angezeigt. Das dient lediglich zu Überprüfungszwecken.
4. Wählen Sie auf der **Allgemein**-Registerkarte auf einer projektbasierten Vertragszeile im **Projekt**-Feld den Projektlink.
5. Auf der **Projekt**-Seite wählen Sie die **Einrichtung der Aufgabenfakturierung**-Registerkarte.
6. Es gibt zwei Raster. Ein Raster ist für Vertragszeilen vorgesehen, die für das gesamte Projekt gelten. Das zweite Raster gilt für die aufgabenspezifische Abrechnungskonfiguration. Wählen Sie im zweiten Raster eine oder mehrere Aufgaben aus und wählen Sie dann **Vertragszeilen verknüpfen**.
7. Wählen Sie auf der sich öffnenden Dialogseite eine Vertragszeile aus der Dropdown-Liste aus.
8. Verwenden Sie die **Fakturierungstyp**-Dropdown-Liste, um die Aufgaben als kostenpflichtig oder nicht kostenpflichtig zu markieren.
9. Aktivieren Sie das Kontrollkästchen, um anzugeben, ob die Zuordnung auch untergeordnete Aufgaben der ausgewählten Aufgaben enthalten soll. Durch Aktivieren des Kontrollkästchens werden auch die untergeordneten Aufgaben der ausgewählten Aufgaben der Vertragszeile zugeordnet.
10. Schließen Sie das Dialogfenster mit **OK**.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Zuweisung von Aufgaben zu projektbasierten Vertragszeilen aufheben

### <a name="from-the-contract-line-page"></a>Von der Vertragszeilenseite

Führen Sie die folgenden Schritte aus, um die Zuweisung von Projektaufgaben zur Vertragszeile von der **Fakturierbare Aufgaben**-Registerkarte der **Vertragszeile**-Seite aufzuheben.

1. Wählen Sie auf der **Fakturierbare Aufgaben**-Registerkarte die Option **Eine Vertragszeilenaufgabe löschen**.
2. Eine Warnmeldung zeigt an, dass das Entfernen dieser Zuordnung zur Umkehrung aller zuvor in der Aufgabe aufgezeichneten Istwerte führen kann. Wählen Sie **OK** im Dialogfeld aus, um die Zuordnung zwischen der Aufgabe und der projektbasierten Vertragszeile zu entfernen. 

> [!NOTE]
> Dadurch wird die Aufgabe nicht aus dem Projekt gelöscht. Stattdessen wird die Aufgabenzuordnung aus der projektbasierten Vertragszeile entfernt.

### <a name="from-the-project-page"></a>Über die Seite „Projekt“

Dies ist die optimalere Erfahrung, um die Zuordnung von Projektaufgaben zu Vertragszeilen aufzuheben. Sie können mehrere Aufgaben auswählen und die Zuordnung all dieser und der untergeordneten Aufgaben der ausgewählten Vertragszeile aufheben. Führen Sie die folgenden Schritte aus, um die Zuordnung der Aufgaben von der Vertragszeile über die Projekt-Seite zu entfernen.

1. Wählen Sie auf der **Allgemein**-Registerkarte auf einer projektbasierten Vertragszeile im **Projekt**-Feld den Projektlink.
2. Auf der **Projekt**-Seite wählen Sie die **Einrichtung der Aufgabenfakturierung**-Registerkarte.
3. Auf der Seite befinden sich zwei Raster. Ein Raster gilt für Vertragszeilen, die für das gesamte Projekt gelten, und das zweite für aufgabenspezifische Abrechnungskonfigurationen. Wählen Sie im zweiten Raster eine oder mehrere Aufgaben aus und wählen Sie dann **Zuordnung von Vertragszeilen aufheben**.
4. Wählen Sie auf der sich öffnenden Dialogseite eine Vertragszeile aus der Dropdown-Liste aus.
5. Aktivieren Sie das Kontrollkästchen, um anzugeben, ob die Zuordnung auch aus untergeordneten Aufgaben der ausgewählten Aufgaben entfernt werden soll. Durch Aktivieren des Kontrollkästchens werden auch die untergeordneten Aufgaben der ausgewählten Aufgaben aus der Vertragszeile entfernt.
6. Klicken Sie auf **OK**. Eine Warnmeldung zeigt an, dass das Entfernen dieser Zuordnung zur Umkehrung aller zuvor in der Aufgabe aufgezeichneten Istwerte führen kann. Wählen Sie **OK** im Warnungsdialogfeld aus, um die Zuordnung zwischen der Aufgabe und der projektbasierten Vertragszeile zu entfernen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]