---
title: Buchhaltung für interne Projekte konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Buchhaltungspraktiken für interne Projekte in Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005525"
---
# <a name="configure-accounting-for-internal-projects"></a>Buchhaltung für interne Projekte konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Interne Projekte ermöglichen es Unternehmen, Kosten im Zusammenhang mit Aktivitäten zu verfolgen, die keinem Kunden in Rechnung gestellt werden. Beispiele für interne Projekte sind:

- Entwickeln eines Produkts, z. B. einer mobilen App, und Verfolgen der mit der Entwicklung verbundenen Kosten
- Verwalten von Zeit und Spesen vor dem Verkauf Dieses interne Vorverkaufsprojekt kann später in ein fakturierbares Projekt umgewandelt werden, wenn das Angebot gewonnen wird.

Jedes Projekt, das in Dynamics 365 Project Operations keinem Vertrag zugeordnet ist, wird als intern behandelt. Projektkosten und Umsatzprofile werden nicht dazu verwendet, Buchhaltungsregeln für das Projekt zu bestimmen. Interne Projektkosten werden immer nach Gewinn- und Verlustprinzipien gebucht. Sachkonten für Buchungen sind auf der Seite **Sachkontobuchungseinstellungen** definiert.

- Zeittransaktionen werden durch Belastung des Kontos **Kosten** und Gutschrift des **Lohnabrechnungs**-Umlagekontos gebucht.
- Ausgabentransaktionen werden durch Belastung des Kontos **Kosten** und Gutschriften für das Konto **Gegenkonto für Ausgaben** gebucht.
- Artikeltransaktionen werden durch Belastung des **Kostenkontos** und Gutschrift des **Kosten – Artikel**-Kontos gebucht.

Nachdem Transaktionen in das Projekt gebucht wurden und das Projekt einem Projektvertrag zugeordnet ist, storniert das System alle kumulierten Transaktionen und erstellt neue abrechnungsfähige Transaktionen. Die abrechnungsfähigen Transaktionen befolgen die Buchhaltungsvorschriften, die im entsprechenden Profil Projektkosten und ‑umsatz definiert sind.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
