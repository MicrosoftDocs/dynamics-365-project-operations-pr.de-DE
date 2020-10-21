---
title: Verwalten komplexer Einheiten für produktbasierte Angebotspositionen, z. B. pro Benutzer und Monat
description: Dieses Thema enthält Informationen zur Verwaltung komplexer Einheiten für produktbasierte Angebotspositionen.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965786"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Verwalten komplexer Einheiten für produktbasierte Angebotspositionen, z. B. pro Benutzer und Monat

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verwendet Mengenfaktoren, um den Verkauf von Abonnement-basierten Produkten zu unterstützen. Für Abonnement-basierte Produkte wird die Menge im Angebot oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.

Normalerweise wird der Preis der Abonnement-Software im Katalog als Preis pro Benutzer pro Monat gespeichert. Während des Vertriebsprozesses wird der Preis in der Angebotsposition in der Regel als Preis pro Benutzer pro Monat angegeben, der vom IT-Vertriebsmitarbeiter verhandelt und diskontiert wurde. Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate. Die Menge, die verwendet wird, um die Menge der Angebotsposition zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.

Um diese Art des Verkaufs zu unterstützen, hat Project Operations das Konzept der Mengenfaktoren eingeführt. Mengenfaktoren basieren auf den Produktattributen in Dynamics 365. Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, kennzeichnet Project Operations eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren.

Project Operations stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden. Wenn Sie einer Angebotsposition ein Produkt mit Mengenfaktoren hinzufügen, wird das Feld **Menge** schreibgeschützt. Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, berechnet Project Operations die Menge der Angebotsposition.

Beispielsweise kann Dynamics 365 Sales die folgenden Eigenschaften aufweisen:

- **Anzahl der Benutzer**: Die Anzahl der Benutzer
- **Anzahl der Monate**: Die Anzahl der Abonnementmonate
- **Produkt-SKU**

Sie können die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** durch Bearbeitung der Produktposition als Mengenfaktoren kennzeichnen.

Gehen Sie folgendermaßen vor, um Mengenfaktoren aus Produkteigenschaften zu erstellen:

1. Navigieren Sie im linken Navigationsbereich von Project Operations zu **Vertrieb** > **Produkte**.
2. Öffnen Sie das Produkt, für das Sie Mengenfaktoren konfigurieren müssen. Stellen Sie sicher, dass für das Produkt bereits Eigenschaften konfiguriert sind.
3. Wählen Sie auf der Seite **Projektinformationen** für das Produkt die Registerkarte **Mengenfaktoren** aus.
4. Wählen Sie im Unterraster **+Neue Feldermittlung** aus.
5. Geben Sie den Namen des Mengenfaktors ein, und wählen Sie den Eigenschaftswert aus, der der Feldermittlung zugeordnet ist.
6. Speichert und schließt das Formular. Wiederholen Sie diese Schritte für alle Eigenschaften, die zur Berechnung der Menge für die produktbasierte Angebotsposition verwendet werden sollen.

Wenn Sie eine produktbasierte Angebotsposition für ein Produkt erstellen, wird die Menge der Angebotsposition gesperrt. Die Menge wird als Produkt der Eigenschaftswerte berechnet, die Sie für diese Angebotsposition eingeben.
