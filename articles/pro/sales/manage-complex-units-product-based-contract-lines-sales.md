---
title: Komplexe Einheiten für produktbasierte Vertragszeilen verwalten – Lite
description: Dieser Artikel enthält Informationen über die Unterstützung des Verkaufs von Produkten im Abonnement.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f48ac31778e34ace79dbce74cff752343484e5a5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919921"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Komplexe Einheiten für produktbasierte Vertragszeilen verwalten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verwendet Mengenfaktoren, um den Verkauf von Abonnement-basierten Produkten zu unterstützen. Für Abonnement-basierte Produkte wird die Menge im Vertrag oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.

Der Preis der Abonnement-Software im Katalog wird als Preis pro Benutzer pro Monat gespeichert. Während des Vertriebsprozesses wird der Preis in der Vertragszeile in der Regel als Preis pro Benutzer pro Monat angegeben, der vom Vertriebsmitarbeiter verhandelt und diskontiert wurde. Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate. Die Menge, die verwendet wird, um die Menge der Vertragszeile zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.

Um diese Art des Verkaufs zu unterstützen, unterstützt Project Operations das Konzept der *Mengenfaktoren*. Mengenfaktoren basieren auf den Produktattributen. Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, können Sie eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren markieren.

Project Operations stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden. Wenn ein Produkt mit konfigurierten Mengenfaktoren zu einer Vertragszeile hinzugefügt wird, wird das **Menge**-Feld schreibgeschützt. Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, berechnet Project Operations die Menge der Vertragszeile.

Beispielsweise kann Dynamics 365 Sales die folgenden Eigenschaften aufweisen:

- **Anzahl der Benutzer**: Die Anzahl der Benutzer.
- **Anzahl der Monate**: Die Anzahl der Abonnementmonate.
- **Produkt-SKU**: Die Lagereinheit (SKU) für das Produkt.

Die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** können durch Bearbeitung der Produktposition als Mengenfaktoren gekennzeichnet werden.

Führen Sie die folgenden Schritte aus, um Mengenfaktoren aus Produkteigenschaften zu erstellen.

1. Wählen Sie in **Project Operations** **Vertriebsprodukte** aus.
2. Öffnen Sie das Produkt, für das Sie Mengenfaktoren einrichten müssen. Stellen Sie sicher, dass für das Produkt bereits Eigenschaften eingerichtet sind.
3. Auf der **Projektinformations**-Seite wählen Sie die **Mengenfaktoren**-Registerkarte.
4. Wählen Sie im Unterraster **+Neue Feldermittlung** aus.
5. Geben Sie den Namen des **Mengenfaktors** ein, und wählen Sie den Eigenschaftswert aus, der der Feldermittlung zugeordnet ist.
6. Speichert und schließt das Formular.
7. Wiederholen Sie die Schritte 2 bis 6 für alle Eigenschaften, die zusammen die Menge für die produktbasierte Vertragszeile bilden.

Wenn Mengenfaktoren eingerichtet sind und der Benutzer eine Vertragszeile für dieses Produkt erstellt, wird die Menge der Vertragszeile gesperrt. Die Menge wird dann als Produkt der Eigenschaftswerte für diese Vertragszeile berechnet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]