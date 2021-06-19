---
title: Projektpreislisten in Projektverträgen verwalten
description: Dieses Thema enthält Informationen zum Verwalten von Projektpreislisten für Projektverträge.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010380"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projektpreislisten in Projektverträgen verwalten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektverträge in Dynamics 365 Project Operations unterstützen effektive Verkaufspreislisten mit mehreren Daten für einen Vertrag. In Project Operations gibt es eine neue zugeordnete Entität mit dem Namen **Projektpreislisten**. Diese Entität hat eine 1:n-Beziehung zu einem Projektvertrag.

Projektpreislisten werden verwendet, um Zeit-, Material- und Aufwandsvorgänge für ein Projekt zu bewerten. Wenn ein Vertrag eine oder mehrere Projektpreislisten enthält, werden diese Preislisten verwendet, um Zeit, Material, Kostenschätzungen und Istwerte für Projekte zu bewerten, die dem Vertrag über die Vertragszeile zugeordnet sind.

Wenn ein Projektvertrag keine Projektpreislisten enthält, wird eine Warnmeldung angezeigt, dass keine Projektpreislisten vorhanden sind und Ihre Schätzungen, die tatsächliche Projektarbeit, das Material und die aufgezeichneten Kosten nicht bewertet werden. Für Verkaufswerte gibt es keinen Preis.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Verknüpfen oder Aufheben der Zuordnung einer Projektpreisliste zu einem Projektvertrag

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Erstellen oder verknüpfen Sie eine bestimmte Preisliste zur Schätzung der projektbasierten Arbeit, des Materials und der Kosten

1. Wählen Sie im Projektvertrag die Registerkarte **Projektpreislisten**.
2. Wählen Sie im Unterraster **+ Neue Projektpreisliste hinzufügen** aus.
3. Auf dem **Schnellerfassung**-Schieberegler wählen Sie eine Preisliste. 

  In der Dropdown-Liste werden alle Preislisten angezeigt, für die der Kontext **Vertrieb** festgelegt ist, wobei die Währung auf der Preisliste mit der Währung auf dem Vertrag übereinstimmt.
  
4. Geben Sie eine Beschreibung für die Projektpreislistenzuordnung ein und wählen Sie **Speichern** und schließen Sie dann den **Schnellerfassung**-Schieberegler.

   Eine Projektpreislistenzuordnung wird erstellt.
   
5. Wiederholen Sie die Schritte 1 bis 4, um dem Projektvertrag mehr als eine Projektpreisliste zuzuordnen. Erstellen Sie nur dann mehrere Projektpreislisten, wenn Sie für jede der zugehörigen Projektpreislisten unterschiedliche Datumseffektivität haben.

> [!NOTE]
> Project Operations unterstützt keine Überlappung der Datumseffektivität der Projektpreislisten. Wenn für eine Transaktion mit einem bestimmten Datum mehrere Projektpreislisten vorhanden sind, wird der Preis für diese Transaktion standardmäßig auf null gesetzt.

### <a name="remove-a-project-price-list-association"></a>Projektpreislistenzuordnung entfernen

- Wählen Sie die Projektpreisliste aus und wählen Sie dann **Preisliste für Vertragsprojekt löschen** auf dem Unterraster. 

  Die Preisliste wird aus den Projektpreislisten im Vertrag entfernt. Die Preisliste selbst wird nicht gelöscht. Nur die Zuordnung zum Vertrag wird gelöscht.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Richten Sie die automatische Standardisierung von Projektpreislisten für einen Vertrag ein

Eine Projektpreisliste kann als Standardprojektpreisliste eingerichtet werden. Dieses Setup stellt sicher, dass alle Verträge in Ihrer Organisation immer mit einer Standardprojektpreisliste für diesen Preiszeitraum beginnen.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Richten Sie den organisatorischen Standard für Projektpreislisten ein

1. Wechseln Sie zu **Einstellungen** > **Allgemein**, und wählen Sie dann **Parameter** aus.
2. Auf der Listenseite **Aktive Parameter** wählen Sie den Datensatz und doppelklicken Sie darauf, um ihn zu öffnen. Stellen Sie beim Doppelklicken sicher, dass Sie nicht auf einen Feldwert klicken, der ein Hyperlink ist. 
3. Auf der **Aktive Parameter**-Seite wählen Sie die **Preisliste**-Registerkarte. Ein Unterraster zeigt eine Liste der Standardpreislisten. Dies ist eine Liste der Standardkosten- und Verkaufspreislisten. Eine hier zugeordnete **Vertrieb**-Preisliste für jede Währung, in der Sie verkaufen, stellt sicher, dass die Verkaufspreisliste der Standard für jeden Vertrag ist, den Sie für Kunden erstellen, die in dieser Währung Transaktionen durchführen.

### <a name="set-up-a-customer-specific-project-price-list"></a>Richten Sie eine kundenspezifische Projektpreisliste ein

Sie können auch kundenspezifische Projektpreislisten einrichten, wenn Sie mit Ihren Kunden eine Rahmenpreisvereinbarung ausgehandelt haben.

1. Gehen Sie zu **Vertrieb** > **Kunden**.
2. Wählen Sie aus der Liste der aktiven Konten den Kunden aus, für den eine spezielle Preisliste vorliegt.
3. Wählen Sie den Kundendatensatz aus, um ihn zu öffnen, und wählen Sie dann die **Projektpreislisten**-Registerkarte. Ein Unterraster zeigt eine Liste der für diesen Kunden spezifischen Projektpreislisten. 
4. Erstellen Sie hier eine neue Preislistenzuordnung, um eine für diesen Kunden spezifische Projektpreisliste zu erhalten.

## <a name="custom-pricing-on-a-project-contract"></a>Benutzerdefinierte Preisgestaltung für einen Projektvertrag

Nachdem Sie organisatorische und kundenspezifische Standardprojektpreislisten erstellt haben, werden Ihre Projektverträge mit diesen Projektpreislistenzuordnungen automatisch erstellt. Projektpreislisten auf einem Projektvertrag werden jedoch immer mit dem Datum und dem Vertragsnamen kopiert, die an sie angehängt sind. Die Konto- und Projektmanager können dann beginnen, die Preise für diese Kopien zu ändern. Diese geänderten Preise gelten nur für diesen Projektvertrag.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
