---
title: Neu in 2021, Welle 2, Early Access 2021 – Bereitstellung von Project Operations lite
description: Dieses Thema enthält Informationen zu den Funktionen, die in der Version 2021 Welle 2 Early Access der Project Operations Lite-Bereitstellung verfügbar sind.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723675"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Neu in 2021, Welle 2, Early Access 2021 – Bereitstellung von Project Operations lite

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

  - Project Operations in Dataverse, Umgebungsversion 4.23.0.4

Die Version wird nur angewendet, wenn eine Umgebung [für Early Access angemeldet ist](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

[Fremdarbeitsverwaltung](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Diese Funktion bietet eine bessere Sichtbarkeit und Kontrolle über alle Aspekte der Arbeit an einem Projekt. Die Vorschau der Fremdarbeitsverwaltung umfasst die folgenden Funktionen:

  - Ein Projektmanager kann einen Fremdarbeitsvertrag mit einem Kreditor erstellen. Standardmäßig werden die an den Kreditorendatensatz angehängten Preislisten für den Fremdarbeitsvertrag verwendet. Das Kreditorenkonten hat den Beziehungstyp **Kreditor** oder **Lieferant**.
  - Ein Projektmanager kann alle Käufe als Positionen auf dem Fremdarbeitsvertrag auflisten. Fremdarbeitspositionen können Zeit, Ausgaben oder Produkte umfassen. Die Transaktionsklasse der Fremdarbeitsposition bestimmt, wofür die Position verwendet wird.
  - Der Konto-Manager des Zulieferers und der Projektmanager können den Fremdarbeitsvertrag durchlaufen. Die Preise können in den Einkaufspreislisten angepasst werden, die dem Fremdarbeitsvertrag angefügt sind.
  - Während des Prozesses kann der Konto-Manager des Zulieferers jeder Fremdarbeitsposition Zuliefererkontakte zuordnen, wenn die Fremdarbeitsposition zeitlich begrenzt ist. Diese Assoziation stellt dem Projektmanager, der an dem Fremdarbeitsvertrag arbeitet, Informationen zur Verfügung. Wenn ein Lieferantenkontakt mit einer Fremdarbeitsposition verknüpft ist, erstellt das System automatisch eine buchbare Ressource aus dem Kontakt, falls noch keine buchbare Ressource vorhanden ist.
  - Die Fakturierungsmethode für jede Fremdarbeitsposition kann Festpreis oder Zeit und Material sein. Für Fremdarbeitspositionen mit Festpreisen wird ein meilensteinbasierter Rechnungsplan eingerichtet.
