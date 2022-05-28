---
title: Mehrere Kunden in Projektverträgen verwalten
description: Dieses Thema enthält Informationen zum Verwalten von mehreren Kunden für einen Projektvertrag.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bf8b0d313b2b07924d730fe8923b05559bbcc244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591311"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Mehrere Kunden in Projektverträgen verwalten

Dieses Thema enthält Informationen zum Verwalten von mehreren Kunden für einen Projektvertrag. Sie können einen Projektvertrag verwenden, wenn eine vertragliche Vereinbarung für mehrere Kunden zur Finanzierung eines Geschäfts erforderlich ist. Auf der **Projektvertrag**-Seite enthält die **Zusammenfassung**-Registerkarte Informationen zum Hauptkunden für ein Geschäft. Andere Kunden, die an dem Geschäft teilnehmen, können der **Kunden**-Registerkarte hinzugefügt werden.

Alle Vertragskunden, die auf der **Kunden**-Registerkarte im Projektvertrag aufgeführt sind, werden standardmäßig als Vertragszeilenkunden in allen neuen projektbasierten Vertragszeilen aufgeführt, die für den Projektvertrag erstellt wurden. Alle bestehenden projektbasierten Vertragszeilen erben keine neuen Vertragskunden, die zu einem späteren Zeitpunkt erstellt wurden.

Sie können Vertragskunden und Vertragszeilenkunden jederzeit hinzugefügen, aktualisieren oder löschen, bevor der Vertrag gewonnen wird. Ein Kunde im Projektvertrag muss als Kunde in der Eigentümergesellschaft oder juristischen Person auf der **Kunden**-Seite eingerichtet sein. Juristische Personen sind im **Projektmanagement und Buchhaltung**-Modul von Dynamics 365 Project Operations festgelegt und sind als Unternehmen in den Modulen **Projektvertrieb** und **Lieferung** Module von Project Operations verfügbar.

## <a name="primary-customers"></a>Primäre Kunden

Der potenzielle Kunde auf der **Zusammenfassung**-Registerkarte des Projektvertrags ist der primäre Kunde des Vertrags. Sie können den Hauptkunden nicht aus der Liste des Vertragskunden aktualisieren. Wenn Sie versuchen, den Hauptkunden aus der Kundenliste des Vertrags zu löschen, wird eine Fehlermeldung angezeigt, dass ein Hauptkundendatensatz eines Vertrags nicht gelöscht werden kann. Stattdennen ändern Sie den Kunden im Feld **Potenzieller Kunde** auf der **Zusammenfassung**-Registerkarte des Projektvertrags. Wenn Sie dieses Feld aktualisieren, wird der neue Kunde als neuer Vertragskunde mit dem gesetzten **Primär**-Flag auf **Ja** hinzugefügt. Der vorherige Hauptkunde ist weiterhin ein Kunde im Vertrag, er ist jedoch nicht mehr der Hauptkunde.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Erstellen, aktualisieren oder löschen Sie einen Vertragskundendatensatz

Ein Vertragskunde kann über die **Vertragskunden**-Registerkarte auf der **Vertrag**-Seite erstellt, aktualisiert oder gelöscht werden. Die folgenden Felder sind im Vertragskundendatensatz der projektbasierten Vertragszeilen enthalten.

| **Feld** | **Ort** | **Beschreibung** | 
| --- | --- | --- | 
| Konto | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Führt alle aktiven Konten auf. Dieses Feld wird gesperrt, nachdem der Datensatz erstellt wurde. Um den Datensatz zu aktualisieren, löschen Sie den Datensatz und erstellen Sie ihn neu. Wenn Sie Istdaten aufgezeichnet haben oder wenn der Vertragskundendatensatz ein Hauptkunde ist, können Sie den Datensatz nicht löschen. Wenn eine Vertragszeile erstellt wird, werden Vertragskunden als Vertragszeilenkunden kopiert. |
| Abrechnungsteilungsprozentsatz | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Stellt den Prozentsatz jeder nicht in Rechnung gestellten Verkaufstransaktion dar, der diesem Vertragskunden zugeordnet wird. Wenn neue Projektvertragszeilen erstellt werden, wird der Prozentsatz der Abrechnungsaufteilung in alle neu erstellten Vertragszeilen und in Projektvertragszeilenkunden kopiert. |
| Kontaktname für Rechnungsadresse | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Dieses Textfeld sollte verwendet werden, um die Rechnungskontaktperson für den Kunden zu identifizieren. Die Werte werden standardmäßig aus dem zugehörigen Kontodatensatz verwendet. Der Kontaktname wird nach **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| Name für Rechnungsadresse | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Verwenden Sie dieses Textfeld, um die Rechnungskontaktperson für den Kunden zu identifizieren. Die Werte werden standardmäßig aus dem zugehörigen Kontodatensatz verwendet. Der Name wird in das Feld **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| Zahlungsbedingungen | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Die Werte werden standardmäßig aus dem zugehörigen Kontodatensatz verwendet. Die Bedingungen werden nach **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| Zuständiges Unternehmen | Bearbeitbares Raster auf der **Projektvertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Projektvertragskunden. | Die juristische Person, in der der Kunde im **Projektmanagement und Buchhaltung**-Modul eingerichtet ist. Dieses Feld ist schreibgeschützt und auf die Eigentümerfirma des Projektvertrags festgelegt.</br>Die Liste der Kunden, die in das **Konto**-Feld aufgenommen werden sollen, ist bereits auf die Liste des zuständigen Unternehmens im **Projektmanagement und -buchhaltung**-Modul von Project Operations gefiltert. Die Eigentümergesellschaft ist gleich der juristischen Person im **Projektmanagement und Buchhaltung**-Modul von Project Operations. Alle Kosten und Einnahmen aus diesem Projekt werden im Hauptbuch der Eigentümergesellschaft ausgewiesen. |
| Wird gerundet | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Gibt an, ob der Kunde ein Standardrundungskunde für das Geschäft ist. Es kann nur einen Rundungskunden in einem Projektvertrag geben. Wenn Kosten und nicht abgerechnete Umsatzaufteilungen nach Menge zu einer Rundungsdifferenz führen, wird diese Differenz auf die tatsächliche Differenz angewendet, die diesem Kunden zugeordnet ist. |
| Nicht zu überschreitender Grenzwert | Bearbeitbares Raster auf der **Vertragskunden**-Registerkarte und den Seiten Hauptbereich und Schnellerfassung für einen Vertragskunden. | Gibt an, ob es ein ausgehandeltes Limit oder eine Obergrenze für den Gesamtbetrag gibt, der dem Kunden für dieses Engagement in Rechnung gestellt wird. Der Nicht zu überschreitende Grenzwert, der auf Vertragskundenebene eingerichtet wurde, erhält eine Bewertung für nicht in Rechnung gestellte vertriebliche Ist-Werte, die auf diesen Vertragskunden verweisen. |

## <a name="edit-billing-split-percentages"></a>Aufteilungsprozentsätze bearbeiten

Sie können Fakturierungs-Aufteilungsprozentsätze im Raster bearbeiten. Wenn die Prozentsätze für die Aufteilung der Abrechnung nicht 100 Prozent betragen, wird eine Fehlermeldung angezeigt. Aktualisieren Sie die Seite **Projektvertrag**, nachdem Sie die Prozentsätze für die Aufteilung der Abrechnung bearbeitet haben, um den Fehler zu entfernen.

Sie können auch **Gleichmäßig verteilen** im Projektvertragskunden-Unterraster auswählen. Die Abrechnung wird gleichmäßig auf alle Kunden in der Projektvertragszeile verteilt. Wenn es einen Rundungsfaktor gibt, wird dieser dem Rundungskunden hinzugefügt. Einer der Vertragskunden hat immer das **Rundung**-Flag auf **Ja** gesetzt. Dieser Kunde ist der Rundungskunde. In der Regel ist der Rundungskunde auch der Hauptkunde des Vertrags, dies ist jedoch nicht erforderlich.


[!INCLUDE[footer-include](../includes/footer-banner.md)]