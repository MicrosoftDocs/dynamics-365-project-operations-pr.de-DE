---
title: Leads verwalten – Lite
description: Dieses Thema enthält Informationen zur Verwaltung projekbasierter Leads (Pro).
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67480459478ffb8a157a2943af919dc63721b779
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994720"
---
# <a name="manage-leads---lite"></a>Leads verwalten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektbasierte Leads können in Project Operations verwaltet und qualifiziert werden. Der Prozess des Lead-Managements umfasst das Erstellen arbeitsbezogener Leads und das Qualifizieren dieser Leads. 

## <a name="list-of-project-sales-leads"></a>Liste der Projektvertriebsleads

Im **Vertrieb**-Abschnitt öffnen Sie im linken Navigationsbereich die **Leads**-Listenseite, um eine Liste aller Lead-Datensätze im System anzuzeigen. Die Leads in der Liste sind arbeitsbasiert sowie andere Arten von Leads, die erstellt werden können, wenn Sie auch über Dynamics 365 Sales- oder Dynamics 365 Field Service-Anwendungen verfügen.

Sie können eine gefilterte Ansicht erstellen, um nur projektbasierte Leads anzuzeigen, indem Sie einen Filter für den Wert **Typ** erstellen. Sie können beispielsweise festlegen, dass nur arbeitsbezogene Leads angezeigt werden.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Erstellen eines neuen Leads für einen projektbasierten Deal

Wenn ein projektbasierter Lead qualifiziert ist, werden eine Verkaufschance und ein Konto erstellt. Eine projektbasierte Gelegenheit ist der Ausgangspunkt für Vertriebsaktivitäten in der Phase Verkaufschance. Projektbasierte Verkaufschancen verfügen über einzigartige Funktionen, die für den Verkauf von Projektarbeit erforderlich sind. Diese Fähigkeiten umfassen Folgendes:

- Abrechnungsmethoden Zeit und Material und Festpreis
- Mehrere datumsabhängige Preislisten für Personal, Ausgaben und Material sind für Projekte angefallen.

Damit ein qualifizierter Lead automatisch eine Verkaufschance erstellt, legen Sie die Option **Typ** auf **Arbeitsbezogen** fest, wenn Sie den Lead erstellen. Wenn Sie einen anderen Typ auswählen, erstellt der Lead keine projektbasierte Verkaufschance, wenn er qualifiziert ist. Wenn die projektbasierte Verkaufschance nicht erstellt wird, sind die projektspezifischen Funktionen in den nachgelagerten Verkaufsprozessen nicht verfügbar.

Die folgende Tabelle enthält wichtige Feldinformationen für einen Lead und die nachgelagerten Auswirkungen dieser Felder.

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Thema | Registerkarte „Allgemein“ | Dieses Textfeld sollte eine kurze Beschreibung des Geschäfts enthalten. | Das Thema des Leads wird standardmäßig als Thema der Verkaufschance und als Name des Angebots- und Projektvertrags verwendet. |
| Art | Registerkarte „Allgemein“ | Dieses Optionssatzfeld enthält die folgenden Optionen:</br>- Arbeitsbasiert (nur bei Installation von Project Operations verfügbar)</br>- Positionsbasiert (nur verfügbar, wenn Project Operations und Sales installiert sind)</br>- Servicewartungsbasiert (verfügbar, wenn Field Service installiert ist) | Wenn der Wert dieses Feldes beim Lead auf **Arbeitsbasiert** festgelegt ist, ist der Lead qualifiziert, eine projektbasierte Verkaufschance zu erstellen. Eine projektbasierte Verkaufschance ist erforderlich, um alle projektspezifischen Erweiterungen und Funktionen im nachgelagerten Verkaufsprozess für dieses Geschäft zu aktivieren. |
| Vorname | Registerkarte „Allgemein“ | Vorname des Interessentenkontakts | Wenn der Lead qualifiziert ist, werden ein Konto, ein Kontakt und eine Verkaufschance erstellt. Der Vorname des Kontakts ist der hier festgelegte Wert. |
| Nachname | Registerkarte „Allgemein“ | Nachname des Interessentenkontakts | Wenn der Lead qualifiziert ist, werden ein Konto, ein Kontakt und eine Verkaufschance erstellt. Der Nachname des Kontakts ist der hier festgelegte Wert. |
| Firma | Registerkarte „Allgemein“ | Name des Unternehmens des Interessentenkontakts | Wenn der Lead qualifiziert ist, werden ein Konto, ein Kontakt und eine Verkaufschance erstellt. Der Name des erstellten Kontos ist der hier festgelegte Wert. |
| Währung | Details-Registerkarte | Währung des Interessentenkunden | Wenn der Lead qualifiziert ist, werden ein Konto, ein Kontakt und eine Verkaufschance erstellt. Die Währung des erstellten Kontos ist der hier festgelegte Wert. |

## <a name="qualify-a-new-project-based-lead"></a>Qualifizieren eines neuen projektbasierten Leads

Leads, die den **Typ**-Wert auf **Arbeitsbasiert** festgelegt haben, werden projektbasierte Leads genannt. Wenn ein projektbasierter Lead qualifiziert ist, wird Folgendes erstellt:

- Ein Konto, das das **Unternehmen**-Feld vom Lead verwendet.
- Ein dem Konto zugeordneter Kontaktdatensatz basierend auf den Werten in den **Vorname**- und **Nachname**-Feldern zum Lead.
- Eine projektbasierte Verkaufschance, bei der das Feld **Typ** auf **Arbeitsbezogen** festgelegt ist.

Weitere Informationen zum Qualifizieren von Leads finden Sie unter [Leads qualifizieren oder konvertieren](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Geschäftsprozessfluss für projektbasierte Deals

Die folgenden Geschäftsprozessflüsse werden für projektbasierte Transaktionen im Project Operations unterstützt:

- Lead-zu-Verkaufschancen-Geschäftsprozess
- Vertriebsprozess Verkaufschance

Der Lead-zu-Verkaufschance-Geschäftsprozess unterstützt die folgenden Phasen:

| Name der Phase | Zugeordnete Entität | Funktionalität |
| --- | --- | --- |
| Qualifizieren | Lead | Qualifizieren des Leads, um eine Firma, einen Kontakt und eine Verkaufschance zu erstellen. |
| Entwickeln | Verkaufschance | Entwickeln Sie die Möglichkeit, weitere Informationen über die Arbeit, die wichtigsten Interessengruppen und den Wettbewerb hinzuzufügen. |
| Vorschlagen | Verkaufschance | Entwickeln Sie den Vorschlag und holen Sie sich vom internen Überprüfungsteam eine Genehmigung. |
| Schließen | Verkaufschance | Gewinnen Sie die Verkaufschance, um den Deal zu schließen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]