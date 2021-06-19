---
title: Mehrfachwährungsszenarien (Version 3.x)
description: Dieses Thema enthält Informationen zu Mehrfachwährungsszenarien.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 70f27d29c74a82f0307bd0724347960e5755e3a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014790"
---
# <a name="multiple-currency-scenarios"></a>Mehrfachwährungsszenarien

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 bietet zwei Konzepte für Währungen:

- **Transaktionswährung** – Die Währung, in der eine Transaktion stattfindet. 
- **Basiswährung** – Die Währung der Dynamics 365-Instanz. Diese Währung wird bei der Bereitstellung einer Dynamics 365-Instanz eingerichtet. Es kann nicht geändert werden.

Beispielsweise verkaufte Contoso USA 100 T-Shirts für jeweils 15 Pfund Sterling (GBP) an einen Kunden im Vereinigten Königreich. Die folgende Tabelle gibt Aufschluss darüber, wie diese Transaktion in der Entität „Auftrag (Produkt)” erfasst wird.

| Produkt | Menge | Einzelpreis | Währung | Betrag | Wechselkurs | Einzelpreis (Basis)| Betrag (Basis)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-Shirt | 100      | 15             | GBP      | 1500   | 0.94          | USD 17,25               | 1.725 USD       |

In der Spalte **Währung** wird die Transaktionswährung angezeigt, in der der Verkauf erfolgte. Die Spalte **Wechselkurs** ist der Wechselkurs zwischen der Transaktionswährung und der Basiswährung. Die Basiswährung ist US-Dollar (USD). Die Basiswährung wurde bei der Bereitstellung der Dynamics 365-Instanz eingerichtet.
Wie die Tabelle zeigt, wird jede Transaktion sowohl in der Transaktionswährung als auch in der Basiswährung erfasst. Dynamics 365 verwendet den Wechselkurs zur Berechnung der Basiswährungsbeträge.

## <a name="project-service-automation-extensions"></a>Project Service Automation-Erweiterungen

Dynamics 365 Project Service Automation wirkt sich auf die Transaktionswährung aus, da Geschäftstransaktionen normalerweise zwei Aspekte haben: Kosten und Vertrieb.

Die folgenden Entitäten gelten als Geschäftstransaktionen:

- Detailinformationen zur Angebotsposition
- Positionsdetail von Projektvertrag
- Vorkalkulationsposition
- Erfassungsposition
- Rechnungsposition
- Tatsächlich

In jeder dieser Entitäten ist ein Datensatz vorhanden, der den Kostenbetrag oder den Umsatzbetrag darstellt. Wie bei jeder Dynamics 365-Entität mit einem Feld **Betrag**, enthält jeder Datensatz Beträge sowohl in der Transaktionswährung als auch in der Basiswährung. 

PSA erweitert das Konzept der Transaktionswährung für Kosten und Umsatz folgendermaßen:

- Die Kostentransaktionswährung für Zeittransaktionen wird immer von der Währung der Organisationseinheit, die das Projekt besitzt und verwaltet, abgeleitet. Diese Organisationseinheit wird als Vertragseinheit bezeichnet.
- Die für Verkaufstransaktionswährung für Zeit- und Ausgabentransaktionen stammt immer von der Währung des Projektvertrags.
- Die Kostentransaktionswährung für Ausgaben stammt von der Währung, in welcher der Ausgabeneintrag erstellt wurde.

## <a name="multiple-currency-scenario"></a>Mehrfachwährungsszenario

In diesem Abschnitt wird ein Beispiel für ein Projekt beschrieben, das Contoso UK für einen Kunden mit dem Namen Fabrikam, Japan, liefert. Das Szenario wurde folgendermaßen eingerichtet:

1. GBP und japanische Yen (JPY) werden unter **Einstellungen** \> **Unternehmensmanagement** \> **Währungen** eingerichtet. 
2. Ein Kundenkonto namens **Fabrikam - Japan** wird eingerichtet, und JPY wird als Währung für das Konto ausgewählt.
3. Eine Organisationseinheit mit dem Namen **Contoso UK** wird eingerichtet, und GBP wird als Währung ausgewählt.
4. Ein Projektvertrag wird erstellt, wobei **Contoso UK** als Vertragseinheit und **Fabrikam - Japan** als Kunde angegeben ist.
5. Projektvertragszeilen werden auf Grundlage der Fakturierungsanordnungen für die verschiedenen Transaktionsklassen für das Projekt – wie etwa Abrechnung von Zeit und Abrechnung von Ausgaben – erstellt.
6. Ein Projekt wird erstellt, wobei **Contoso UK** als Vertragseinheit angegeben ist. Dieses Projekt wird erstellt und den Projektvertragszeilen zugeordnet.


Während der Vorkalkulation, die das Angebotspositionsdetail, das Projektvertragszeilendetail bzw. die Vorkalkulationsposition des Zeitplans verwendet, werden in der Entität immer zwei Datensätze erstellt. Ein Datensatz ist für Kosten und der andere Datensatz ist für den Vertrieb.

- Standardmäßig ist die Transaktionswährung im Kostensatz auf die Währung der Vertragseinheit des Projekts eingestellt. In diesem Beispiel ist die Währung GBP.
- Standardmäßig ist die Transaktionswährung im Vertriebsdatensatz auf die Währung des Projektvertrags eingestellt. In diesem Beispiel ist die Währung JPY.

Wenn Ist-Werte für die Zeit mithilfe des Zeiteintrags oder der Erfassungsposition erstellt werden, tritt folgendes Verhalten auf:

- Standardmäßig ist die Transaktionswährung im Kostensatz auf die Währung der Vertragseinheit des Projekts eingestellt.
- Standardmäßig ist die Transaktionswährung im Vertriebsdatensatz auf die Währung des Projektvertrags eingestellt.

Wenn Ist-Werte für die Ausgaben mithilfe des Ausgabeneintrags oder der Erfassungsposition erstellt werden, tritt folgendes Verhalten auf:

- Sie können den Ausgabenbetrag in einer beliebigen Währung erfassen. Wählen Sie die Währung mithilfe des Währungswählers auf der Seite **Ausgabeneintrag** oder der Seite **Erfassungsposition** aus. Standardmäßig ist die Transaktionswährung im Kostensatz auf die Währung des Ausgabeneintrags eingestellt. 
- Standardmäßig ist die Transaktionswährung des Vertriebsdatensatzes die Währung des Projektvertrags. Um diese Währung festzulegen, rechnet das System zunächst den Transaktionsbetrag in der vom Benutzer eingegebenen Währung in die Basiswährung um. Anschließend wird der Betrag in die Währung des Projektvertrags umgerechnet. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Berechnen von Rollups, wenn Projekt-Ist-Werte in mehreren Transaktionswährungen erfasst werden

Dynamics 365 verarbeitet automatisch die Rollups von Beträgen in verschiedenen Währungen. Im Folgenden finden Sie ein Beispiel.

| Transaktionsklasse | Transaktionstyp| Date   | Ressource | Transaktionskategorie | Menge | Einzelpreis | Betrag      | Wechselkurs | Basisbetrag |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Nicht fakturierte Umsätze   | 14. Jun | Falk  |                      | 8 Std.    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Nicht fakturierte Umsätze   | 15. Jun | Falk  |                      | 8 Std.    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Expense           | Nicht fakturierte Umsätze   | 16. Jun | Falk  | Hotel                | 1 EA     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Expense           | Nicht fakturierte Umsätze   | 17. Jun | Falk  | Autovermietung           | 1 EA     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Um den gesamten nicht fakturierten Umsatzwert des Projekts zu berechnen, können Sie ein Rollup-Feld für das Feld **Betrag** auf allen zugehörigen nicht fakturiertem Umsatz-Ist-werten erstellen. Das Rollup-Feld ist ein Konstrukt von Dynamics 365, das bei zugehörigen Datensätzen schnelle Formeln ermöglicht.


[!INCLUDE[footer-include](../includes/footer-banner.md)]