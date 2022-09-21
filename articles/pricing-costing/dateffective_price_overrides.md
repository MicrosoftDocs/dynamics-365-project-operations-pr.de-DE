---
title: Preisüberschreibungen mit Gültigkeitsdatum
description: In diesem Artikel wird erläutert, wie Sie Preisüberschreibungen für bestimmte Preise in der Preisliste einrichten.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445968"
---
# <a name="date-effective-price-overrides"></a>Preisüberschreibungen mit Gültigkeitsdatum 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

*Datumswirksame Preisüberschreibungen* bieten eine Möglichkeit, bestimmte Preise in der Preisliste zu überschreiben oder zu ändern. Beispiel: Sie haben eine Standardpreisliste, die vom 1. Januar 2022 bis zum 31. Dezember 2022 gültig ist. Diese Preisliste enthält Preise für viele Rollen. Der festgelegte Preis für die **Netzwerktechniker** Rolle beträgt 100 US-Dollar (USD) pro Stunde. Wenn ein Netzwerktechniker zwischen dem 1. Januar 2022 und dem 31. Dezember 2022 Zeit protokolliert, wird die Zeit mit 100 USD berechnet. Am 1. Oktober 2022 müssen Sie den Preis *nur* für die **Netzwerktechniker** Rolle anpassen, von 100 USD pro Stunde bis 110 USD pro Stunde. Mit der Funktion **Datum gültige Preisüberschreibungen** können Sie diese Änderung als Überschreibung der Zeile für diesen spezifischen Rollenpreis einrichten. Daher müssen Sie nicht die gesamte Preisliste kopieren und den Preis nur dieser einen Zeile ändern.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datumswirksame Preisüberschreibungen für Arbeitspreise

Der Prozess zum Einrichten datumswirksamer Preisüberschreibungen für die Arbeitszeit in einem Projekt besteht aus zwei grundlegenden Schritten.

1. **Preisüberschreibungen mit Gültigkeitsdatum** aktivieren.
1. Preisüberschreibungen mit Gültigkeitsdatum einrichten.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Die Funktion Preisüberschreibungen mit Gültigkeitsdatum aktivieren

> [!NOTE]
> Nachdem die Funktion **Preisüberschreibungen mit Gültigkeitsdatum** aktiviert wurde, kann sie nicht mehr deaktiviert werden.

Um die Funktion **Datumswirksame Preisüberschreibungen** zu aktivieren, folgen Sie diesen Schritten.

1. Gehen Sie zu **Einstellungen** \> **Parameter**.
1. Datensatz **Parameter** öffnen.
1. Klicken Sie im Aktionsbereich auf die Registerkarte **Funktionssteuerung** und wählen **Preisüberschreibungen nach Datum aktivieren**.
1. Wählen Sie im Bestätigungsdialogfeld **OK**.
1. Aktualisieren Sie nach einigen Augenblicken Ihren Browser. Überschreibungsfunktionen für datumswirksame Preise sollten jetzt verfügbar sein. Sie werden wissen, dass diese Funktionen aktiviert wurden, wenn die Schaltfläche **Aktivieren und Überarbeiten von Angeboten aktivieren** nicht mehr im Aktivitätsbereich angezeigt wird.

### <a name="set-up-a-date-effective-price-override"></a>Preisüberschreibungen mit Gültigkeitsdatum einrichten

Preisüberschreibungen zum Gültigkeitsdatum können nur in Preislisten mit den Modulen **Kosten**, **Vertrieb** oder **Kauf** eingerichtet werden.

> [!NOTE]
>Das Verhalten **Datum gültige Preisüberschreibungen** hat derzeit folgende Einschränkungen:
>
> - Nur Rollenpreise und Rollenpreisaufschläge unterstützen die **Datum gültige Preisüberschreibungen** Funktion uin Project Operations.
> - Beim Kopieren einer Preisliste mit der **Kopieren** Aktion auf der Seite **Details der Preisliste** und wenn Sie während der Vertragserstellung eine Projektpreisliste aus einer Standard- oder benutzerdefinierten Preisliste erstellen, werden datumswirksame Preisüberschreibungen **nicht** aus der Quellpreisliste kopiert.

Führen Sie die folgenden Schritte aus, um eine datumswirksame Preisüberschreibung für einen Rollenpreis oder einen Rollenpreisaufschlag einzurichten.

1. Öffnen Sie die Seite für die Preisliste, für die Sie die datumswirksame Preisüberschreibung einrichten möchten.
1. Wählen Sie die Registerkarte **Rollenpreise** aus. Diese Registerkarte listet alle Datensätze **Rollenpreis** in der Preisliste auf.
1. Wählen Sie den Datensatz **Rollenpreis**, für den Sie einen neuen datumswirksamen Überschreibungspreis einrichten möchten, und doppeltippen (oder doppelklicken) Sie dann auf **Rollenpreis**, um die Seite **Details zum Rollenpreis** zu öffnen.
1. Wählen Sie die Registerkarte **Überschreibungen mit Gültigkeitsdatum**. Das Raster auf dieser Registerkarte listet alle datumswirksamen Preisüberschreibungen für den ausgewählten Datensatz **Rollenpreis** auf.
1. Wählen Sie in der Symbolleiste über dem Raster **Neue Rollenpreisüberschreibung** aus. Der Schieber **Neue Rollenpreisüberschreibung** wird geöffnet.
1. Geben Sie das Gültig-ab-Datum, die Einheit und den neuen Preis für die Preisüberschreibung an. Wählen Sie dann **Speichern** aus, und schließen Sie das Formular.

> [!NOTE]
> - Eine datumswirksame Preisüberschreibung für einen Rollenpreis oder einen Rollenpreisaufschlag gilt für dieselbe Kombination von Preisdimensionswerten, die auf der übergeordneten Zeile **Rollenpreis** oder **Rollenpreisaufschlag** vorhanden ist.
> - Das ausgewählte Datum im Feld **Gültig ab** sollte innerhalb der Gültigkeitsdaten der übergeordneten Preisliste liegen. Die Preisüberschreibung wird an dem Datum wirksam, das im Feld **Gültig ab** ausgewählt wurde und gilt bis zum Ende des Enddatums der übergeordneten Preisliste. Wenn Sie eine weitere datumswirksame Preisüberschreibung für denselben Rollenpreis einrichten, wird die erste Preisüberschreibung an dem Datum wirksam, das im Feld **Gültig ab** ausgewählt wurde und gilt bis zum Beginn der zweiten Überschreibung.

## <a name="examples"></a>Beispiele

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Beispiel 1: Bestimmen der Datumsgültigkeit für einen Rollenpreis mit Rollenpreisüberschreibungen

Das folgende Beispiel zeigt, wie die Datumsgültigkeit für einen bestimmten Rollenpreis bestimmt wird, für den Rollenpreisüberschreibungen eingerichtet sind.

**Preisliste A: 1. Januar bis 30. Juni**

*Rollenpreis*

| Rollenpreis | Einheit | Preis | Auswirkung auf die Preisgestaltung für eingehende Transaktionen |
|---|---|---|---|
| Netzwerktechniker | Stunde | 100 | Dieser Preis wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 1. Januar und dem 14. März liegt. |

*Rollenpreisüberschreibung*

| Gültig von | Einheit | Preis | Auswirkung auf die Preisgestaltung für eingehende Transaktionen |
|---|---|---|---|
| März 15 | Stunde | 110 | Dieser Preis wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 15. März und dem 30. März liegt. |
| April 1 | Stunde | 120 | Dieser Preis wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 1. April und dem 30. Juni liegt. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Beispiel 2: Bestimmen der Datumsgültigkeit für einen Rollenpreisaufschläge mit Rollenpreisaufschlagüberschreibungen

Das folgende Beispiel zeigt, wie die Datumsgültigkeit für einen bestimmten Rollenpreisaufschlag bestimmt wird, für den Rollenpreisaufschlagsüberschreibungen eingerichtet sind.

**Preisliste A: 1. Januar bis 30. Juni**

*Rollenpreis*

| Rollenpreis | Arbeitszeit | Einheit | Preis | Auswirkung auf die Preisgestaltung für eingehende Transaktionen |
|---|---|---|---|---|
| Netzwerktechniker | Regulär | Stunde | 100 | Dieser Preis wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 1. Januar und dem 14. März liegt. |

*Rollenpreisaufschlag*

| Organisationseinheit | Arbeitszeit | Aufschlag % |
|---|---|---|
| Contoso US | Überstunden | 10 % |

*Rollenpreisaufschlagüberschreibung*

| Gültig von | Preis | Auswirkung auf die Preisgestaltung für eingehende Transaktionen |
|---|---|---|
| März 15 | 20 % | Dieser Aufschlag in Prozent wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 15. März und dem 30. März liegt. |
| April 1 | 25 % | Dieser Aufschlag wird für alle Transaktionen verwendet, bei denen das Transaktionsdatum zwischen dem 1. April und dem 30. Juni liegt. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
