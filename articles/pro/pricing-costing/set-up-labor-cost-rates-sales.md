---
title: Arbeitskostensätze einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen für Arbeit in Project Operations.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 01e3b41ca5c8fcc9146186873e0f44daad020c6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575671"
---
# <a name="set-up-labor-cost-rates---lite"></a>Arbeitskostensätze einrichten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Jede Preisliste enthält eine Reihe von Arbeitssätzen (Rollenpreisen), die mit dem Inhalt und der Datumseffektivität der Preisliste übereinstimmen.

1. Erstellen Sie eine Preisliste und auf der **Rollenpreis**-Registerkarte wählen Sie im Unterraster die Registerkarte **Neue Rolle**.
2. Wählen Sie auf der Seite **Schnellerfassung** die Rolle und die Organisationseinheit aus.
3. Geben Sie alle erforderlichen Feldinformationen ein.

Die folgende Tabelle enthält einige der Felder, die beim Erstellen von Arbeitssätzen auf einer Einstandspreisliste wichtig sind.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Rolle | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Wählen Sie die Rolle aus, für die der Kostensatz gilt. | Die Rolle in der eingehenden Vorkalkulation oder der Istwerte wird mit dieser Zeile abgeglichen, um die Kosten der Rolle als Standard festzulegen. |
| Ressourcenzuordnungseinheit | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Wählen Sie die Organisationseinheit oder die Abteilung des Unternehmens aus, von der aus diese Rolle verwendet werden soll. Zum Beispiel ein Entwickler aus der Robotics-Abteilung von Fabrikam India oder ein Entwickler aus der Software-Abteilung von Fabrikam USA. | Die Ressourcenzuordnungseinheit in der eingehenden Vorkalkulation oder den Istwerten wird mit dieser Zeile abgeglichen, um den Kostensatz der Rolle als Standard festzulegen. |
| Preis | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Richten Sie den Kostensatz für die Kombination aus Rolle, Ressourcenzuordnungsunternehmen und Ressourcenzuordnungseinheit ein. Beispielsweise wird für einen Entwickler von Fabrikam India 1.000 INR oder für einen Entwickler aus Fabrikam Kosten von 150 USD berechnet. | Der Preis ist der Kostensatz, der standardmäßig auf den Einzelpreis der eingehenden Vorkalkulation oder der tatsächlichen Zeile für die Transaktionsklasse **Zeit** basiert. |
| Währung | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Standardmäßig stammt der Währungswert aus der Währung in der Kopfzeile der Einstandspreisliste, kann jedoch überschrieben werden. Zum Beispiel wird für einen Entwickler von Fabrikam India 1000 INR berechnet. Ein Entwickler aus Fabrikam USA kostet 150 USD. | Diese Währung basiert standardmäßig auf dem Einzelpreis der eingehenden Istwert-Zeile der Transaktionsklasse **Zeit**. Bei einer Projektvorkalkulation wird der Währungswert in die Projektwährung umgerechnet und in der zeitgesteuerten Ansicht der Vorkalkulation angezeigt. |
| Einheitenzeitplan | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Der Einheitenzeitplan ist standardmäßig auf Zeit eingestellt und kann für die Rollenpreisentität nicht geändert werden, da er verwendet wird, um Sätze nach Zeiteinheiten darzustellen. | Dabei gibt es keine nachgelagerten Auswirkungen. |
| Einheit | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Standardmäßig stammt dieser Wert aus dem Feld **Zeiteinheit** im Header der Einstandspreisliste. Der Wert kann überschrieben werden. Zum Beispiel wird für einen Entwickler von Fabrikam India 1.000 INR pro **Tag in Indien** berechnet. Ein Entwickler aus Fabrikam USA kostet 150 USD pro **Tag in den USA**. | Das System verwendet das Einheitensystem und die Umrechnung in Basiseinheiten, um den Einzelpreis zu berechnen und den Standardpreis pro Einheit für eine eingehende Vorkalkulations- oder Istwertzeile zu berechnen. Zum Beispiel entspricht eine Vorkalkulation für die Arbeit eines Entwicklers aus Indien 10 **Tage in Indien**, und die Einheit **Tag in Indien** ist als 10 Stunden definiert. Bei der Kalkulation dieser Vorkalkulationszeile berechnet die Anwendung die Stückkosten für die Vorkalkulation wie folgt: 1000 INR/10 Stunden = 100 INR pro Stunde, die in USD umgerechnet und als Stückkosten auf der Seite **Projektvorkalkulationen** angezeigt wird. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Verrechnungspreise und Kosten für Ressourcen außerhalb Ihres Geschäftsbereichs oder Ihrer juristischen Person

In projektbasierten Unternehmen ist es üblich, Mitarbeiter aus unterschiedlichen legalen Entitäten oder Abteilungen in Projekten einzusetzen. Ein Projekt kann von einer juristischen Person ausgeführt werden, aber die Mitarbeiter oder Berater, die an dem Projekt arbeiten, können von derselben oder einer anderen juristischen Person stammen, oder es kann eine Kombination aus beiden geben. In Dynamics 365 Project Operations ist die juristische Person, der die Lieferung des Projekts obliegt, das **Zuständige Unternehmen** und die Abteilung, der die Lieferung obliegt, die **Vertragseinheit**. Andere juristische Personen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungsunternehmen** und Abteilungen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungseinheiten**. In den meisten Ländern müssen Unternehmen sicherstellen, dass die juristische Person oder Abteilung das zuständige Unternehmen und die Vertragseinheit für die Verwendung der Ressourcen belasten.

Beispielsweise muss die Fabrikam Corporation sicherstellen, dass Fabrikam India-Robotics eine Kostensatzkarte mit Fabrikam US-Robotics oder Fabrikam UK-Robotics ausgehandelt hat.

Ein Entwickler von Fabrikam India-Robotic berechnet 100 USD bei einer Überlassung an Fabrikam US-Robotics und 150 USD bei Überlassung an Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Kosten für externe Ressourcen einrichten

1. Erstellen Sie eine Einstandspreisliste mit der Bezeichnung *Fabrikam US-Robotics-Kostensätze*, und legen Sie einen effektiven Datumsbereich fest.
2. Richten Sie in der Einstandspreisliste die Raten anhand der Informationen aus der folgenden Tabelle ein. 

| Rolle | Ressourcenzuordnungsunternehmen | Ressourcenzuordnungseinheit | Kostenrate |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | 100 € |
| Developer | Fabrikam Philippinen | Fabrikam Philippines-Robotics | 90 USD |
| Developer | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Fügen Sie diese Einstandspreisliste der Organisationseinheit Fabrikam US-Robotics bei.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Die Verrechnungspreise für eine Ressource in der entsprechenden Währung einrichten 

In Project Operations kann die Ressourcenpreisgestaltung in einer beliebigen Währung eingerichtet werden. Die Währung wird standardmäßig im Preislisten-Header verwendet, kann jedoch geändert werden.

Anhand des Beispiels für die Einrichtung des Transferpreises können die Informationen wie folgt geändert werden:

Die Fabrikam Corporation muss sicherstellen, dass Fabrikam India-Robotics eine Kostensatzkarte mit Fabrikam US-Robotics oder Fabrikam UK-Robotics ausgehandelt hat.

Ein Entwickler von Fabrikam India-Robotics berechnet 5.000 INR bei einer Überlassung an Fabrikam US-Robotics und 5.500 INR bei Überlassung an Fabrikam UK-Robotics.

In der Einstandspreisliste für Fabrikam US-Robotics können die Kostensätze wie folgt dargestellt werden:

| Rolle | Ressourcenzuordnungsunternehmen | Kosten |
| --- | --- | --- |
| Developer | Fabrikam India | 5.000 INR |
| Developer | Fabrikam US | 115 USD |

In der Einstandspreisliste für Fabrikam UK-Robotics können die Kostensätze wie folgt dargestellt werden:

| Rolle | Ressourcenzuordnungsunternehmen | Kosten |
| --- | --- | --- |
| Developer | Fabrikam India | 5.500 INR |
| Developer | Fabrikam UK | 115 GBP |

Die Einstandspreisliste kann Arbeitssätze in mehreren Währungen enthalten. Bei der Erstellung eines Kostenvoranschlags für das Projekt konvertiert Project Operations diese Kostensätze in die Projektwährung und zeigt sie dem Benutzer an. Wenn ein Zeiteintrag genehmigt und ein tatsächlicher Kostenaufwand erstellt wird, werden die tatsächlichen Kosten in der Währung der entsprechenden Preiszeile für die Rolle in der Einstandspreisliste berechnet. Die tatsächlichen Kosten für die Zeit eines einzelnen Projekts können in mehreren Währungen erfasst werden. Wenn Sie jedoch die tatsächlichen Arbeitskosten auf Projektebene zusammenfassen, konvertiert Project Operations alle Arbeitskostenbeträge in die Projektwährung, die der Benutzer anzeigen kann.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]