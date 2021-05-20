---
title: Intercompany-Transaktionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Intercompany-Transaktionen.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b8b35e8875ac4aff1ae9690c4d4afabe25af8dc9
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880447"
---
# <a name="create-intercompany-transactions"></a>Intercompany-Transaktionen erstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Intercompany-Transaktionen sind Zeit- und Kostentransaktionen aus einem Projektvertrag, die zu einem Unternehmen oder einer Organisationseinheit gehören, während die Ressourcen im Projektvertrag Teil eines anderen Unternehmens oder einer anderen Organisationseinheit sind.

Wenn eine Intercompany-Transaktion genehmigt wird, werden die folgenden tatsächlichen Transaktionen erstellt

| **Transaktionstyp** | **Angewendete Preisliste** | **Buchungswährung** |
| --- | --- | --- |
| Kosten | Preisliste für Vertragsstückkosten | Währung auf der Preisposition |
| Nicht fakturierte Umsätze Diese werden nur für Istdaten erstellt, die einer Vertragszeile mit Abrechnungsart, Uhrzeit und Material zugeordnet sind. | Vertriebspreisliste für Vertragsprojekt | Vertragswährung |
| Kosten der Ressourcenzuordnungseinheit | Preisliste für Ressourceneinheitskosten | Währung auf der Preisposition |
| Organisationsübergreifende Einheitenverkäufe | Preisliste für Vertragsstückkosten | Währung auf der Preisposition |

Kosten, die Beschaffungskosten für Einheiten sowie die Preise und die Währung für Verkaufstransaktionen zwischen Organisationen werden durch die **Organisationseinheit** bestimmt. Dies ist wichtig, wenn Sie entscheiden, wie Unternehmen und Organisationseinheiten in Ihrer Implementierung strukturiert werden sollen.

Wenn Sie Opportunity-, Angebots-, Projektvertrags- und Projektaufzeichnungen erstellen, überprüft das System, ob die Währung der Vertragseinheit mit der Buchhaltungswährung des Vertragsunternehmens übereinstimmt. Wenn sie nicht identisch sind, können diese Datensätze nicht erstellt werden. Die Währung der Organisationseinheit wird in Dynamics 365 Project Operations definiert, indem Sie zu **Dataverse** > **Einstellungen** > **Organisationseinheiten** gehen. Die Rechnungswährung eines Unternehmens wird in Dynamics 365 Finance definiert, indem Sie zu **Finanzbuchhaltung** > **Sachkonto-Einstellungen** > **Sachkonto** gehen. Die Währung wird mit Ihrer Dataverse-Umgebung mit der Zuordnung für duales Schreiben des Sachkontos synchronisiert.

Das System erstellt in den folgenden Situationen Ressourcen-Stückkosten und Ist-Verkaufszahlen zwischen Organisationen:

  - Wenn sich die Beschaffungseinheit von der Vertragseinheit unterscheidet
  - Wenn sich das Beschaffungsunternehmen vom Vertragsunternehmen unterscheidet

Es werden jedoch nur Transaktionen an die Dynamics 365 Finance-Umgebung zur zusätzlichen Buchhaltung übertragen, die ein anderes Resourcing-Unternehmen als das Vertragsunternehmen haben.

Die Bilanzierung von Projekt-Istdaten wird im Project Operations-Integrationsjournal in Finance erfasst. Das System erstellt die folgenden Journalzeilen.

| **Transaktionstyp** | **Juristische Person** | **Erstellt eine Projekttransaktion beim Buchen** | **Finanzdimensions-Standardeinstellungen an** | **Standard-Fakturierungs-Mehrwertsteuergruppe und Fakturierungs-Artikel-Mehrwertsteuergruppe** |
| --- | --- | --- | --- | --- |
| Kosten | Wird nicht zum Integrationsjournal hinzugefügt | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend |
| Nicht fakturierte Umsätze | Das Integrationsjournal für leihende juristische Personen | Ja | Project | **Abrechnungs-Umsatzsteuergruppe**: Basierend auf **Vertragskunde** <br/> **Abrechnungsposten-Umsatzsteuergruppe**: Aus der aktuellen Projektkategorie für juristische Personen in der Journalzeile |
| Kosten der Ressourcenzuordnungseinheit | Das Integrationsjournal für ausleihende juristische Personen | Nr. | Konzerninterner Kunde | **Abrechnungs-Umsatzsteuergruppe**: Basierend auf **Intercompany-Kunde** <br/> **Abrechnungsposten-Umsatzsteuergruppe**: Aus der aktuellen Projektkategorie für juristische Personen in der Journalzeile |
| Organisationsübergreifender Umsatz | Das Integrationsjournal für ausleihende juristische Personen | Nr. | Konzerninterner Kunde | **Abrechnungs-Umsatzsteuergruppe**: Basierend auf **Intercompany-Kunde** <br/> **Abrechnungsposten-Umsatzsteuergruppe**: Aus der aktuellen Projektkategorie für juristische Personen in der Journalzeile |

### <a name="example-intercompany-transactions"></a>Beispiel: Intercompany-Transaktionen

Molly Clark, Entwicklerin bei GBPM, verzeichnet 10 Stunden Arbeit für ein USPM Adventure Works-Projekt, das vom Projektmanager genehmigt wurde. Die Entwicklerkosten in GBPM betragen 88 GBP pro Stunde. GBPM berechnet USPM 120 USD pro Entwicklerstunde. USPM stellt dem Kunden Adventure Works 200 USD für die von der GBPM-Ressource geleistete Arbeit in Rechnung. Weitere Informationen finden Sie unter [Intercompany-Rechnungsstellung konfigurieren](configure-intercompany-invoicing.md).

1. Gehen Sie in Project Operations zu **Ressourcen** und wählen Sie **Molly Clark** aus der Liste. Auf der Registerkarte **Zeitplanung** wählen Sie im Feld **Firma** **GBPM** aus.
2. Gehen Sie zu **Vertrieb** > **Debitoren** und wählen Sie **Neu**, um einen neuen Kundendatensatz für Adventure Works zu erstellen.
    1. Legen Sie die Firma auf **USPM** fest:
    2. Legen Sie den **Beziehungstyp** auf **Debitor** fest.
    3. Wählen Sie **Kundengruppe 10 – Inland** aus.
    4. Legen Sie die Währung auf **USD** fest.
    5. Speichern Sie den Datensatz.
3. Gehen Sie zu **Vertrieb** > **Projektverträge** und erstellen Sie einen neuen Projektvertrag für Adventure Works.
    1. Setzen Sie die Eigentümerfirma auf **USPM** und die Vertragseinheit auf **Contoso Robotics US**.
    2. Wählen Sie Adventure Works als Debitor aus.
    3. Wählen Sie eine Produktpreisliste und speichern Sie den Datensatz.
    4. Auf der Registerkarte **Vertragspositionen** erstellen Sie eine neue Vertragsposition. Stellen Sie einen beliebigen Namen ein und wählen Sie **Zeit und Materialien** als Abrechnungsmethode.
    5. Erstellen Sie ein neues Projekt und ordnen Sie es dieser Vertragslinie zu.
4. Als Ressource **Molly Clark** anmelden. Gehen Sie zu **Projekte** > **Zeiteinträge** und erstellen Sie einen Zeiteintrag für das Adventure Works-Projekt.
5. Melden Sie sich als Projektmanager an. Gehen Sie zu **Projekte** > **Genehmigungen** und genehmigen Sie die von Molly Clark protokollierte Zeiteintragstransaktion.
6. Navigieren Sie zum Adventure Works-Projekt, und wählen Sie **Verknüpft** > **Ist-Werte** aus. Die folgenden tatsächlichen Transaktionen werden erstellt.

| **Transaktionstyp** | **Preis** | **Buchungswährung** | **Betrag** |
| --- | --- | --- | --- |
| Kosten | 120 | USD | 1200 |
| Nicht fakturierte Umsätze | 200 | USD | 2000 |
| Kosten der Ressourcenzuordnungseinheit | 88 | GBP | 880 |
| Organisationsübergreifende Einheitenverkäufe | 120 | USD | 1200 |

7. Melden Sie sich als USPM-Buchhalter an. Öffnen Sie die Finance-Instanz von Project Operations und wählen Sie das Unternehmen **USPM**. 
8. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Periodisch** > **Project Operations on Customer Engagement** > **Aus Staging importieren** und wählen Sie, um den periodischen Prozess auszuführen. Dieser periodische Prozess füllt das Project Operations-Integrations-Journal aus.
9. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Journale** > **Project Operations-Integrationsjournal** und überprüfen Sie die Journalzeilen. Das System erstellt die folgende Position.

    | **Transaktionstyp** | **Preis** | **Buchungswährung** | **Betrag** |
    | --- | --- | --- | --- |
    | Nicht fakturierte Umsätze | 200 | USD | 2000 |

    Wenn das System so eingerichtet ist, dass Einnahmen für dieses Projekt anfallen, wird Folgendes gebucht:

    - Lastschrift: Projekt – WIP-Verkaufswert 200 USD
    - Gutschrift: Projekt – Aufgelaufene Einnahmen 200 USD

    Dieser nicht in Rechnung gestellte Verkauf ist jetzt zur Rechnungsstellung bereit. Die Rechnung für den Kunden Adventure Works kann bei Bedarf finanziell gebucht werden.

10. Melden Sie sich als **GBPM**-Buchhalter an. Öffnen Sie die Finance-Instanz von Project Operations und öffnen Sie das Unternehmen **GBPM**. 
11. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Periodisch** > **Project Operations-Integration** > **Import aus Staging-Tabelle** und führen Sie den periodischen Prozess aus, um das Project Operations Integrationsjournal auszufüllen.
12. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Journale** > **Project Operations-Integrationsjournal** und überprüfen Sie die Positionen. Das System erstellt die folgende Positionen.

    | **Transaktionstyp** | **Preis** | **Buchungswährung** | **Betrag** |
    | --- | --- | --- | --- |
    | Kosten der Ressourcenzuordnungseinheit | 88 | GBP | 880 |
    | Organisationsübergreifende Einheitenverkäufe | 120 | USD | 1200 |

    Das Buchen dieser Datensätze führt zu folgenden Gutscheintransaktionen:

    - Lastschrift: Projektkosten 88 GBP
    - Gutschrift: Lohnzuweisung 88 GBP

    Wenn das System so eingerichtet ist, dass Intercompany-Einnahmen für dieses Projekt anfallen, wird Folgendes gebucht:

    - Lastschrift: Projekt – WIP-Verkaufswert 120 USD
    - Gutschrift: Projekt – Aufgelaufene Einnahmen 120 USD

    Das System ist jetzt bereit, eine Intercompany-Debitorenrechnung zu erstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
