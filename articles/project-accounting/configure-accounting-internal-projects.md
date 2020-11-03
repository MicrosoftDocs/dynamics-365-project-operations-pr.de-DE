---
title: Buchhaltung für interne Projekte konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Buchhaltungspraktiken für interne Projekte in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076458"
---
# <a name="configure-accounting-for-internal-projects"></a>Buchhaltung für interne Projekte konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Interne Projekte ermöglichen es Unternehmen, Kosten im Zusammenhang mit Aktivitäten zu verfolgen, die keinem Kunden in Rechnung gestellt werden. Beispiele für interne Projekte sind:

- Entwicklung eines Produkts, z. B. einer mobilen App, und Verfolgung der mit der Entwicklung verbundenen Kosten
- Verwalten von Zeit und Ausgaben vor dem Verkauf Dieses interne Vorverkaufsprojekt kann später in ein fakturierbares Projekt umgewandelt werden, wenn das Angebot gewonnen wird.

Jedes Projekt, das in Dynamics 365 Project Operations keinem Vertrag zugeordnet ist, wird als intern behandelt. Projektkosten und Umsatzprofile werden nicht dazu verwendet, Buchhaltungsregeln für das Projekt zu bestimmen. Interne Projektkosten werden immer nach Gewinn- und Verlustprinzipien gebucht. Sachkonten für Buchungen werden auf der Seite **Sachkontobuchungseinstellungen** definiert.

- Zeittransaktionen werden durch Belastung des Kontos **Kosten** und Gutschriften für das Konto **Lohnzuweisung** gebucht.
- Ausgabentransaktionen werden durch Belastung des Kontos **Kosten** und Gutschriften für das Konto **Gegenkonto für Ausgaben** gebucht.

Nachdem Transaktionen in das Projekt gebucht wurden und das Projekt einem Projektvertrag zugeordnet ist, storniert das System alle kumulierten Transaktionen und erstellt neue fakturierbare Transaktionen. Die fakturierbaren Transaktionen folgen den Buchhaltungsregeln, die im jeweiligen Projektkosten- und Ertragsprofil definiert sind.


