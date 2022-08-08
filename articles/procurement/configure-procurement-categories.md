---
title: Beschaffungskategorien mit Projektbestellungen und ausstehenden Kreditorenrechnungen verwenden
description: Dieser Artikel beschreibt, wie Sie Beschaffungskategorien konfigurieren, die mit Projektbestellungen und ausstehenden Lieferantenrechnungen verwendet werden können.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028609"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Beschaffungskategorien mit Projektbestellungen und ausstehenden Kreditorenrechnungen verwenden

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Professionelle Einkäufer können Kataloge von Artikeln und Dienstleistungen erstellen und verwalten, die in Projektbestellungen und ausstehenden Kreditorenrechnungen verwendet werden können. [Beschaffungskataloge](/dynamics365/supply-chain/procurement/procurement-catalogs) bieten Ihnen eine einfache Möglichkeit, Einkäufe zu kategorisieren, ohne einen freigegebenen Produktkatalog konfigurieren und verwenden zu müssen. Jede Beschaffungskategorie kann einer Projektkategorie für Zeit-, Ausgaben- oder Artikeltransaktionen zugeordnet werden. Nachdem eine ausstehende Kreditorenrechnung gebucht wurde, die eine Beschaffungskategorie verwendet, erstellt das System Zeit-, Ausgaben- oder Materialprojekt-Ist-Werte, Projekttransaktionen und Nebenbucheinträge.

## <a name="minimum-version-requirements"></a>Mindestens erforderliche Anforderungen

Die folgenden Versionen sind erforderlich, um Beschaffungskategorien mit Projektbestellungen für Microsoft Dynamics 365 Project Operations nicht lagerhaltige/ressourcenbasierte Szenarien zu verwenden:

- Project Operations Dataverse-Lösungsversion 4.41.0.45 oder höher
- Version der Finanz- und Betriebs-App-Umgebung 10.0.26 oder höher

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Zuordnungen für duales Schreiben zur Unterstützung von Beschaffungskategorien ausführen

Stellen Sie sicher, dass die Zuordnung für die **Project Operations-Integrationsprojektreditorenrechnungen-Exportentität msdyn\_projectvendorinvoicelines** Version 1.0.0.4 oder höher verwendet.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Den Funktionsschlüssel für Beschaffungskategorien aktivieren

Befolgen Sie diese Schritte, um die Funktionalität für die Verwendung von Beschaffungskategorien mit Projektbestellungen zu aktivieren.

1. Öffnen Sie in Dynamics 365 Finance den Arbeitsberiech **Funktionsverwaltung**.
1. Suchen Sie in der Funktionsliste die Funktion **Beschaffungskategorien in Project Operations für ressourcenbasierte/nicht vorrätige Szenarien verwenden**, und wählen Sie **Aktivieren** aus.

> [!IMPORTANT]
> Als Voraussetzung müssen Sie auch die **Ausstehende Kreditorenrechnungen in Project Operations für ressourcenbasierte/nicht gelagerte Szenarien aktivieren**-Funktion aktivieren.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektkategorien in der Beschaffungskategoriehierarchie zuordnen

Befolgen Sie diese Schritte, um in der **Beschaffungskategorie**-Hierarchie Projektkategorien den Beschaffungskategorien zuzuordnen:

1. Wechseln Sie zu **Beschaffung \> Beschaffungskategorien**.
1. Wählen Sie **Kategoriehierarchie bearbeiten** aus.
1. Wählen Sie den gewünschten Knoten der Kategorienhierarchie aus und ordnen Sie dann auf der Registerkarte **Projektkategorien zuordnen** den Knoten der Projektkategorie aus der Kategorie **Zeit**, **Aufwand** oder **Element-Projekt** zu (d.h. der Kategorie **Standard-Zeit** oder **Standard-Aufwand**).
1. Wählen Sie **Save** (Speichern).
1. Schließen Sie die Seite.

> [!NOTE]
> Die Zuordnung einer Beschaffungskategorie zu einer Projektkategorie ist optional. Wenn keine Beschaffungskategorie zugeordnet ist, verwendet das System den Wert, der im **Artikel**-Feld im **Standardwerte für Projektkategorien**-Abschnitt auf der Registerkarte **Project Operations bei Dynamics 365 Customer Engagement** auf der Seite **Projektmanagement und Abrechnungsparameter** festgelegt ist.
