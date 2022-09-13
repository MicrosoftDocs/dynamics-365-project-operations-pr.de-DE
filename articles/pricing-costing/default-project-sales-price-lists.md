---
title: Standardpreislisten
description: Dieser Artikel enthält Informationen über Standardverkaufs- und Selbstkostenpreislisten in Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410261"
---
# <a name="default-price-lists"></a>Standardpreislisten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="sales-price-lists"></a>Verkaufspreislisten

Jedes Projektangebot und jeder Vertrag in Dynamics 365 Project Operations enthält eine Standardvertriebspreisliste. 

### <a name="price-list-default-on-project-quotes"></a>Standardpreislisten in Projektangeboten
Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für ein Projektangebot standardmäßig verwendet werden soll:

1. Das System überprüft die Preislisten, die den Projektpreislisten des Kontos beigefügt sind. 
1. Wenn dem Firmendatensatz keine Projektpreislisten beigefügt sind, überprüft das System die Verkaufspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektangebots übereinstimmen.
1. Als Nächstes überprüft das System die Datumseffektivität der Preislisten, die dem Datumsbereich des Projektangebots entsprechen. Speziell das Datum, an dem das Angebot erstellt wurde.
1. Wenn es mehrere Preislisten gibt, die für das Datum des Projektangebots gültig sind, werden alle Preislisten standardmäßig im Projektangebot verwendet.
1. Wenn für das Datum des Projektangebots keine Preislisten gültig sind, enthält das Projektangebot keine Standardprojektpreisliste. Im Projektangebot wird eine Warnmeldung angezeigt. In der Meldung heißt es, dass Istwerte und Vorkalkulationen im Projekt nicht bewertet werden, da keine Projektpreislisten angefügt sind.

### <a name="price-list-default-on-project-contracts"></a>Standardpreislisten in Projektverträgen 
Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für einen Projektvertrag standardmäßig verwendet werden soll:

1. Wenn der Vertrag aus einem Angebot erstellt wird, werden die Projektpreislisten auf dem Angebot separat kopiert und dem Projektvertrag beigefügt.
1. Wenn der Vertrag von Grund auf neu erstellt wird, überprüft das System die Preislisten, die den Projektpreislisten des Kontos beigefügt sind. Wenn dem Firmendatensatz keine Projektpreislisten beigefügt sind, überprüft das System die Verkaufspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektvertrags übereinstimmen.
1. Als Nächstes überprüft das System die Datumseffektivität der Preislisten, die dem Datumsbereich des Projektvertrags entsprechen. Speziell das Datum, an dem der Vertrag erstellt wurde.
1. Wenn es mehrere Preislisten gibt, die für das Datum des Vertrags gültig sind, werden alle Preislisten standardmäßig im Vertrag verwendet.
1. Wenn für das Datum des Vertrags keine Preislisten gültig sind, enthält der Vertrag keine Standardprojektpreislisten. Im Projektvertrag wird eine Warnmeldung angezeigt. In der Meldung heißt es, dass Istwerte und Vorkalkulationen im Projekt nicht bewertet werden, da keine Projektpreislisten angefügt sind.

## <a name="cost-price-lists"></a>Einstandspreislisten

Einstandspreislisten sind standardmäßig keine Entität in Project Operations. Die Ermittlung der Einstandspreise für die Projektkosten erfolgt immer auf entsprechender Vor-Transaktions-Basis. Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für Projektkosten verwendet werden soll:

1. Das System prüft zunächst die Preislisten, die der Vertragsorganisationseinheit des Projekts beigefügt sind.
1. Das System prüft als Nächstes die Datumseffektivität der Preislisten, die mit dem Datum der eingehenden Vorkalkulation oder der tatsächlichen Transaktionen übereinstimmen.

    - *Kalkulationskontext* bezieht sich auf alle drei Vorkalkulationen in Project Operations:

        - Projektvorkalkulationsposition
        - Detailinformationen zur Angebotsposition
        - Vertragszeilendetail

    - *Tatsächlicher Kontext* bezieht sich auf eine der drei Quellen für die Kalkulation in Project Operations:

       - Erfassungszeilen, die manuell erstellt werden, oder Korrekturbuchungszeilen, die in einer Korrekturbuchung erstellt werden
       - Journalzeilen, die während der Übermittlung von Zeit-, Ausgaben- oder Materialverbrauchsprotokollen erstellt werden
       - Rechnungsposition

    Wenn Project Operations mit der Datumsgültigkeit der eingehenden Buchungszeilen- oder Rechnungszeilendetails im *tatsächlichen Kontext* übereinstimmt, wir das Feld **Transaktionsdatum** verwendet.

    - Wenn mehrere Preislisten vorhanden sind, die für das Datum des eingehenden Vorkalkulationskontext oder des tatsächlichen Kontexts gültig sind, wird die zuletzt erstellte Preisliste ausgewählt.
    - Wenn der Vertragsorganisationseinheit des Projekts keine Projektpreislisten beigefügt sind, überprüft das System die Einstandspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektangebots übereinstimmen.

## <a name="enable-multi-currency-cost-price-list"></a>Einstandspreisliste mit Mehrfachwährung aktivieren

Diese Einstellung finden Sie unter **Einstellungen** \> **Parameter**. Der Standardwert ist **Nein**.

Wenn diese Einstellung aktiviert ist (d. h. der Wert auf **Ja**) festgelegt ist, verhält sich das System wie folgt:

- Es lässt zu, dass Preislisten in einer beliebigen Währung aktualisiert werden, nachdem sie einer Organisationseinheit zugeordnet wurden. Beispielsweise kann eine Selbstkostenpreisliste in der Währung EUR an eine Organisationseinheit in der Währung USD angehängt werden. Das System überprüft weiterhin, ob Einstandspreislisten, die einer Organisationseinheit zugeordnet sind, keine sich überschneidende Datumsgültigkeit haben.
- Es validiert, dass Einstandspreislisten, die an Projektparameter angehängt sind, keine sich überschneidende Datumsgültigkeit haben, selbst wenn sie unterschiedliche Währungen haben. Dieses Verhalten unterscheidet sich vom Standardverhalten (d. h. dem Verhalten, wenn der Wert auf **Nein**) festgelegt ist. Im Standardverhalten werden nur Einstandspreislisten, die die **gleiche** Währung haben, auf nicht überlappende Datumsgültigkeit validiert.
- Für einen eingehenden Transaktionskontext bestimmt es die Einstandspreisliste nur basierend auf der Datumsgültigkeit. Dieses Verhalten unterscheidet sich vom Standardverhalten, bei dem das System die Einstandspreisliste auswählt, die sowohl der Währung des Projekts als auch der Datumsgültigkeit entspricht.

Aufgrund dieser Verhaltensänderungen können Project Operations-Kunden eine globale Kostenpreisliste führen, die für das gesamte Unternehmen relevant ist. Sie müssen keine Preislisten in jeder Betriebswährung haben. Die globale Preisliste hat Datumsgültigkeit und ermöglicht die Einrichtung von Kostensätzen in jeder Währung für eine bestimmte Kombination von Preisdimensionswerten. Die Währung der Einstandspreisliste wird nur zur Eingabe von Vorschlagswerten verwendet, wenn **Rollenpreise**, **Kategoriepreise**, und **Preisliste** Artikeldatensätze erstellt werden. Sie wird nicht zur Ermittlung der Preisliste herangezogen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
