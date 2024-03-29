---
title: Buchhaltung für interne Projekte konfigurieren
description: In diesem Artikel erfahren Sie, wie Sie in Project Operations die Abrechnungsmodalitäten für interne Projekte festlegen.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919461"
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
