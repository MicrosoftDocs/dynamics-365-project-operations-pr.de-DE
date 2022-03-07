---
title: Lohnkostensätze einrichten
description: Dieses Thema enthält Informationen zum Einrichten und Anwenden von Lohnkostensätzen in Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7d2dd7b6001ddb475d381d35a4863dcc4b322214
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004665"
---
# <a name="set-up-labor-bill-rates"></a>Lohnkostensätze einrichten

_ **Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen

Jede Preisliste enthält einen Satz von Rollenpreisen oder Arbeitssätzen, die für den Kontext und die Datumseffektivität gelten, die im Preislistenheader enthalten sind. Rechnungssätze für Zeit können in Dynamics 365 Project Operations nur in der Währung eingerichtet werden, die die Währung in der Kopfzeile der Preisliste ist.

1. Um die Lohnkosten für eine Verkaufspreisliste festzulegen, gehen Sie zu **Vertrieb** > **Kunden** > **Preislisten** und wählen **Neu** aus, um eine neue Preisliste zu erstellen. 
2. Wählen Sie auf der Registerkarte **Rollenpreise** im Unterregister die Option **Neuer Rollenpreis** aus. 
3. Geben Sie im Bereich **Schnellerfassung** die Kombination aus Rolle und Organisationseinheit ein, für die Sie den Fakturierungssatz einrichten müssen.

   In der folgenden Tabelle sind die Felder auf der Registerkarte **Allgemein** und der Bereich **Schnellerfassung** einer Rollenpreiszeile aufgeführt, die Sie beim Erstellen von Rollenpreisen in einer Verkaufspreisliste berücksichtigen sollten.

    | Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
    | --- | --- | --- | --- |
    | Rolle | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Wählen Sie die Rolle aus, für die Sie den Fakturierungssatz festlegen. | Die Rolle in der eingehenden Vorkalkulation oder der Istwerte wird mit dieser Zeile abgeglichen, um den Fakturierungssatz der Rolle als Standard festzulegen. |
    | Ressourcenzuordnungsunternehmen | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Wählen Sie das Unternehmen oder die juristische Person aus, von der die Rolle stammt. Zum Beispiel ein Entwickler von Fabrikam India oder ein Entwickler von Fabrikam USA. | Das Ressourcenzuordnungsunternehmen in der eingehenden Vorkalkulation oder den Istwerten wird mit dieser Zeile abgeglichen, um den Fakturierungssatz der Rolle als Standard festzulegen. |
    | Ressourcenzuordnungseinheit | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Wählen Sie die Organisationseinheit oder die Abteilung des Unternehmens aus, von dem die Rolle stammt. Zum Beispiel ein Entwickler aus der Robotics-Abteilung von Fabrikam India oder ein Entwickler aus der Software-Abteilung von Fabrikam USA. | Die Ressourcenzuordnungseinheit in der eingehenden Vorkalkulation oder den Istwerten wird mit dieser Zeile abgeglichen, um den Fakturierungssatz der Rolle als Standard festzulegen. |
    | Preis | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Richten Sie den Fakturierungssatz für die Kombination aus Rolle, Ressourcenzuordnungsunternehmen und Ressourcenzuordnungseinheit ein. Beispielsweise hat ein Entwickler aus Fabrikam India eine Fakturierungsrate von 100 USD oder ein Entwickler aus Fabrikam USA eine Fakturierungsrate von 150 USD. | Der Preis ist der Standard-Fakturierungssatz für den Preis pro Einheit der eingehenden Vorkalkulations- oder Istwertzeile für die Zeittransaktionsklasse. |
    | Währung | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung**| Standardmäßig stammt dieser Währungswert aus der Währung in der Kopfzeile der Verkaufspreisliste. In einer Verkaufspreisliste kann die Währung nicht überschrieben werden. | Diese Währung ist die Standardwährung für den Einzelpreis der eingehenden Istwert-Umsatzzeile für die Zeittransaktionsklasse. |
    | Einheitenzeitplan | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Dieser Einheitenzeitplan ist standardmäßig auf Zeit eingestellt und kann für die Rollenpreisentität nicht geändert werden, da er verwendet wird, um Sätze nach Zeiteinheiten darzustellen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
    | Einheit | Die Registerkarte **Allgemein** und der Bereich **Schnellerfassung** | Der Einheitenwert stammt aus dem Feld **Zeiteinheit** im Vetriebspreislisten-Header. Der Wert kann aber überschrieben werden. Zum Beispiel wird für einen Entwickler von Fabrikam India eine Fakturierungsrate von 1.000 USD pro **Tag in Indien** berechnet. Ein Entwickler aus Fabrikam USA hat eine Fakturierungsrate von 1.500 USD pro **Tag in den USA**. | Wenn der Preis pro Einheit standardmäßig in einer eingehenden Vorkalkulations- oder Istwert-Zeile angegeben wird, verwendet das System die Einheiten und Umrechnung in Basiseinheiten, um den Preis pro Einheit zu berechnen. Zum Beispiel entspricht eine Vorkalkulation für die Arbeit eines Entwicklers aus Indien 10 **Tage in Indien**, und die Einheit „Tag in Indien“ ist als 10 Stunden definiert. Bei der Preisberechnung dieser Vorkalkulationszeile berechnet die Anwendung den Einheitspreis für die Vorkalkulation als 1.000 USD/10 Stunden = 100 USD pro Stunde. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Verrechnungspreise oder Fakturierungssätze für Ressourcen aus anderen Organisationseinheiten oder -abteilungen einrichten 

Projektbasierte Unternehmen setzen häufig Mitarbeiter verschiedener juristischer Personen und Abteilungen innerhalb der juristischen Person ein, um an Projekten zu arbeiten. Projekte können von einer bestimmten juristischen Person und Abteilung ausgeführt werden, während die Mitarbeiter oder Berater, die an den Projekten arbeiten, von derselben juristischen Person oder Abteilung oder aus einer anderen stammen können. Das Projekt könnte auch aus einer Kombination von Personen aus verschiedenen juristischen Personen oder Abteilungen bestehen. In Project Operations ist die juristische Person, die für die Bereitstellung des Projekts verantwortlich ist, das **zuständige Unternehmen** und die Abteilung, die für die Bereitstellung verantwortlich ist, wird **Vertragseinheit** genannt. Alle anderen juristischen Personen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungsunternehmen** und Abteilungen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungseinheiten**. Aufgrund der unterschiedlichen Arbeitskosten in verschiedenen Regionen und Arbeitsmärkten auf der ganzen Welt werden die Fakturierungssätze für Arbeitskräfte auch für verschiedene Regionen unterschiedlich festgelegt.

Beispielsweise wird für einen Entwickler aus der Robotics-Abteilung von Fabrikam India, der an einem US-Projekt arbeitet, eine Rate von 100 USD pro Stunde in Rechnung gestellt. Für einen Entwickler aus der Robotics-Abteilung von Fabrikam US, der an einem US-Projekt arbeitet, wird 150 USD pro Stunde berechnet. 

### <a name="example-set-up-a-bill-rate"></a>Beispiel: Einen Fakturierungssatz einrichten 

1. Erstellen Sie eine Verkaufspreisliste mit dem Namen *Fabrikam US-Fakturierungssätze*, und legen Sie die Datumseffektivität fest.
2. Geben Sie in der Verkaufspreisliste die folgenden Rateninformationen ein:

    | Rolle | Ressourcenzuordnungsunternehmen | Ressourcenzuordnungseinheit | Fakturierungsrate |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India – Robotics | 100 € |
    | Developer | Fabrikam Philippinen | Fabrikam Philippines – Robotics | 90 USD |
    | Developer | Fabrikam US | Fabrikam US - Robotics | 150 USD |

3. Fügen Sie die Verkaufspreisliste, **Fabrikam US-Fakturierungssätze**, zur Projektpreisliste des Projektvertrags oder einem bestimmten Konto hinzu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
