---
title: Projektpreislisten in Projektangeboten verwalten
description: Dieses Thema bietet Informationen zur Arbeit mit Projektpreislisten in Angeboten.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7fcc7feaa9fc8d53046f54576e20989318dc3ec939569ea3844b18097512a24b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001610"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Projektpreislisten in Projektangeboten verwalten 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektangebote unterstützen effektive Verkaufspreislisten mit mehreren Daten. Mit Dynamics 365 Project Operations wird eine neue zugeordnete Entität namens **Projektpreislisten** ergänzt. Diese Entität hat eine 1:n-Beziehung zu einem Projektangebot.

Projektpreislisten werden verwendet, um Zeit-, Material- und Aufwandsvorgänge für ein Projekt zu bewerten. Wenn ein Angebot eine oder mehrere Projektpreislisten enthält, werden diese Preislisten verwendet, um Zeit, Material, Kostenvorkalkulationen und Istwerte für Projekte zu bewerten, die dem Angebot über die Angebotszeile zugeordnet sind.

Wenn ein Projektangebot keine Projektpreislisten enthält, erhalten Sie eine Warnmeldung. In der Meldung heißt es, dass Ihre geschätzten und tatsächlichen Projektarbeiten und -kosten nicht bewertet werden, da keine Projektpreislisten vorhanden sind. Stattdessen haben sie einen Preis von Null (0) für Verkaufswerte.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Eine Projektpreisliste in einem Projektangebot verknüpfen oder trennen

Führen Sie die folgenden Schritte aus, um eine bestimmte Preisliste für die Schätzung der projektbezogenen Arbeit und Ausgaben zu erstellen oder auszuwählen.

1. Wählen Sie im Angebot die Registerkarte **Projektpreis** und im Unterraster **+ Neue Projektpreisliste hinzufügen** aus.
2. Wählen Sie auf der Seite „Schnellerfassung“ eine Preisliste aus. In der Dropdownliste werden alle Preislisten angezeigt, für die der Kontext **Vertrieb** festgelegt ist und die Währung mit der Währung im Angebot übereinstimmt.
4. Geben Sie eine Beschreibung für die Projektpreislistenzuordnung ein, und wählen Sie **Speichern und schließen** aus.

Eine Projektpreislistenzuordnung wird erstellt.

Sie können diesen Prozess wiederholen, wenn Sie dem Projektangebot mehr als eine Projektpreisliste zuordnen müssen. Erstellen Sie nur dann mehrere Projektpreislisten, wenn Sie für jede der zugehörigen Projektpreislisten unterschiedliche Gültigkeitsdaten haben.

> [!NOTE]
> Project Operations unterstützt keine überlappende Datumseffektivität der Projektpreislisten. Wenn für eine Transaktion mit einem bestimmten Datum mehrere Projektpreislisten vorhanden sind, wird der Preis für diese Transaktion standardmäßig auf Null (0) gesetzt.
Um eine Projektpreislistenzuordnung zu entfernen, wählen Sie die Projektpreisliste und dann **Angebotsprojektpreisliste löschen** aus. Die Preisliste wird aus den Projektpreislisten des Angebots entfernt, die Preisliste selbst wird jedoch nicht gelöscht. Nur die Zuordnung zum Angebot wird gelöscht.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Standardprojektpreislisten für ein Angebot einrichten

Projektpreislisten können standardmäßig für ein Projektangebot eingerichtet werden. Diese Einrichtung stellt sicher, dass alle Angebote in Ihrer Organisation immer mit einer Standardpreisliste für diesen Preiszeitraum beginnen.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Organisationsstandard für Projektpreislisten einrichten

1. Navigieren Sie zu **Einstellungen** > **Allgemein** > **Parameter**.
2. Suchen Sie auf der Listenseite **Aktive Parameter** den Datensatz, und doppelklicken Sie, um ihn zu öffnen. 
3. Wählen Sie auf der Seite **Parameter** die Registerkarte **Preisliste** aus. Sie können sehen, dass die Liste der Standardpreislisten angezeigt wird. Dies ist eine Liste der Standardkosten- und Verkaufspreislisten. Wenn für jede Währung, in der Sie verkaufen, eine Verkaufspreisliste zugeordnet ist, wird sichergestellt, dass diese Verkaufspreisliste für alle Angebote, die Sie für Kunden erstellen, die in dieser Währung Transaktionen durchführen, standardmäßig verwendet wird.

### <a name="set-up-customer-specific-project-price-lists"></a>Kundenspezifische Projektpreislisten einrichten

Kundenspezifische Projektpreislisten können auch erstellt werden, wenn Sie mit Ihren Kunden eine Rahmenpreisvereinbarung ausgehandelt haben.

Führen Sie die folgenden Schritte aus, um eine kundenspezifische Projektpreisliste einzurichten.

1. Wählen Sie im Bereich **Vertrieb** die Option **Kunden** aus.
2. Wählen Sie in der Liste Ihrer aktiven Konten den Kundendatensatz aus, und öffnen Sie den Datensatz, für den Sie eine spezielle Preisliste haben.
3. Auf der Registerkarte **Projektpreislisten** können Sie eine neue Preislistenzuordnung erstellen, um die Projektpreisliste zu erhalten, die für diesen Kunden spezifisch ist.

## <a name="create-custom-pricing-on-a-project-quote"></a>Benutzerdefinierte Preise für ein Projektangebot erstellen

Nachdem Sie organisatorische und kundenspezifische Standard-Projektpreislisten erstellt haben, werden Ihre Projektangebote automatisch mit diesen Projektpreislistenzuordnungen erstellt. In bestimmten Fällen müssen Sie jedoch möglicherweise benutzerdefinierte Preise für ein bestimmtes Projektangebot erstellen. 

1. Stellen Sie unter **Projektangebot** auf der **Projektpreisliste** im Unterraster sicher, dass kein bestimmter Preislistendatensatz ausgewählt ist.
2. Wählen Sie **Benutzerdefinierte Preisberechnung erstellen** aus. Dadurch werden Kopien aller Standardpreislisten erstellt, die derzeit dem Angebot zugeordnet sind, und diese Kopien werden dem Angebot zugeordnet. Die bestehenden Verknüpfungen zu Standardpreislisten werden entfernt. Der Vertriebsmitarbeiter kann dann beginnen, die Preise für diese Kopien zu ändern. Diese geänderten Preise gelten nur für dieses Projektangebot.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
