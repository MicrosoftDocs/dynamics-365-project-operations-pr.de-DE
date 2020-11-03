---
title: Vertriebsprozess Übersicht
description: Dieses Thema enthält Informationen zu den grundlegenden Vertriebsprozessen.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: c70760748c5faa87f6738ab7e2ab593e2df49e41
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076723"
---
# <a name="sales-processes-overview"></a>Vertriebsprozess Übersicht

Die Vertriebsprozesse, die in einer projektbasierten Organisation verwendet werden, unterscheiden sich von jenen, die in einer produktbasierten Organisation verwendet werden. Der Grund für diesen Unterschied ist, dass die Vertriebszyklen für projektbasierte Organisationen länger sind und zum Analysieren und Erstellen von Angeboten für jeden Auftrag benutzerdefinierter Schätzungstechniken erfordern. Dynamics 365 Project Operations verwendet zum Teil die gleichen Funktionen, die in einem Vertriebsprozess verwendet werden.

- Ein Lead-Datensatz wird zur Nachverfolgung des Vertriebsprozesses verwendet.
- Qualifizierte Leads werden als Verkaufschancen nachverfolgt.
- Es wird auf alle zugehörigen Artefakte von einer Verkaufschance zugegriffen. Diese Artefakte umfassen das Vertriebsteam, die Stakeholder, die Wahrscheinlichkeit, die Bewertung, die Vertriebsphasen und Geschäftsprozesse.
- Für eine Verkaufschance werden mehrere Angebote erstellt.
- Ein Angebot erhält den Status **Als gewonnen geschlossen** , um einen Vertriebsauftrag zu erstellen. In Project Operations wird der Vertriebsauftrag angepasst und als Projektvertrag bezeichnet.

## <a name="estimate-a-sale"></a>Einen Verkauf schätzen
Der Wert eines Verkaufs kann auf der Grundlage von zuvor gelieferten Projekten und der Komplexität des Projektes geschätzt werden. Für Projekte, bei denen es sich um Erweiterungen von vorherigen Projekten handelt, oder Projekte, bei denen der Zulieferer über hohe Fachkenntnisse verfügt und bekannte Arbeitsvorlagen verwendet werden, können Sie einen einfacheren Schätzungsprozess verwenden. Komplexere Projekte haben normalerweise einen längeren Kaufvorgang. Daher gibt es mehr Phasen in der Vertriebsvorkalkulation. Zu Beginn des Prozesses verwendet das Vertriebsteam die Beiträge von Account Managern und Fachleuten (SMEs), um eine allgemeine Schätzung für jede einzelne angebotene Arbeitskomponente zu erstellen. Diese Arbeitskomponenten werden durch Angebotszeilen dargestellt. 

Sie können eine allgemeine Schätzung des Angebots erstellen. Anschließend wird diese allgemeine Schätzung durch eine detailliertere Schätzung ersetzt, die auf einem Projektplan beruht, den Sie mithilfe der standardisierten Projektvorlagen erstellen. Mithilfe dieser Vorlagen können Sie einen Zeitplan erstellen und Geldbeträge für das Angebot und seine Komponenten (Angebotszeilen) ermitteln. 

Sie können für ein Projekt mehrere Angebote erstellen und sie unter einem Verkaufschancen-Datensatz gruppieren. Schließlich wird ein Angebot als **Als gewonnen geschlossen** markiert, und ein Projektvertrag oder eine Leistungsbeschreibung (SOW) wird erstellt. Ein Projektvertrag enthält den vertraglich vereinbarten Wert für jede Komponente (Vertragszeile), die vom Kunden zur Lieferung angenommen wird. Eine Leistungsbeschreibung wird normalerweise in der Form eines Microsoft Word-Dokuments erstellt. Alle Rechnungen, die dem Kunden im Laufe der Projektlieferung gesendet werden, verweisen auf den Projektvertrag oder die Leistungsbeschreibung.

Sie können auch andere Angebote unter einem Verkaufschancen-Datensatz erstellen oder das System so konfigurieren, dass ein Projektvertrag erstellt wird, wenn ein Angebot gewonnen wird. In diesem Fall können Sie dem Projektvertragsdatensatz ein Word-Dokument anfügen, das die Leistungsbeschreibung darstellt.

## <a name="configure-the-sales-process"></a>Konfigurieren des Vertriebsprozesses
Sie können Geschäftsprozessflüsse verwenden, um Ihren Vertriebsprozess zu konfigurieren. Diese Abläufe bieten eine geführte visuelle Schnittstelle, um Geschäfte durch die Phasen des Vertriebsprozesses voranzutreiben.

Beispielsweise verfügt Ihr Unternehmen über die folgenden sechs Phasen im Vertriebsprozess:

1. Qualifizieren
2. Schätzung
3. Interne Prüfung
4. Vertrag
5. Bereitstellen
6. Schließen
 
Ihre Organisation verwendet möglicherweise verschiedene Entitäten zur Darstellung des gleichen Auftrags, wie er sich entwickelt. Zu Beginn des Vertriebsprozesses wird ein Auftrag durch die Verkaufschancenentität dargestellt. Im Laufe der Zeit und wenn weitere Details bekannt werden, können Sie allgemeine Schätzungen verwenden, um ein oder mehrere Angebote zu erstellen. Wenn eines dieser Angebote von den internen und kundenseitigen Stakeholdern überprüft wird, stellt die Angebotsentität den Auftrag dar. Nachdem der Kunde das Angebot angenommen hat, wird der Auftrag durch einen Projektvertrag oder eine Leistungsbeschreibung repräsentiert. Um dieses Verhalten zu unterstützen, sind BPFs so strukturiert, dass jede Phase des Prozesses mit einer anderen Datenbanktabelle verknüpft ist.

Die Phase **Qualifizieren** im Vertriebsprozess kann durch eine Verkaufschancenentität unterstützt werden. Die Phasen **Schätzung** und **Interne Prüfung** können von einer Angebotsentität unterstützt werden. Die Phasen **Vertrag** , **Lieferung** und **Schließen** können über eine Projektvertragsentität unterstützt werden.

Beim Vorantreiben der Geschäfte durch die Phasen werden Sie aufgefordert, den entsprechenden Entitätsdatensatz zu erstellen, der Sie durch den Prozess führt und unterstützt. Die Phasen können bedingt sein. Wenn Sie beispielsweise nur dann eine interne Überprüfung eines Angebots benötigen, wenn im Angebot eine benutzerdefinierte Preisliste verwendet wird, können Sie diese Bedingung in der entsprechenden Phase des Geschäftsprozesses konfigurieren. Die Phase **Interne Prüfung** wird dann nur für Angebote angezeigt, in denen eine benutzerdefinierte Preisliste verwendet wird. Bei allen anderen Geschäftsabschlüssen und Angeboten folgt auf die Phase **Schätzung** die Phase **Vertrag**.

> [!NOTE]
> Project Operations verfügt über bestimmte Seiten für Verkaufschance, Angebots-, Bestell- und Rechnungsentitätsdatensätze. Sie müssen diese Datensätze mithilfe der Projektinformationsseiten für diese Entitäten erstellen. Andernfalls können Sie die Datensätze nicht über die Seite **Projektinformation** öffnen. Wenn Sie einen Datensatz aus der Seite **Projektinformation** öffnen, müssen Sie den Datensatz löschen und mit der neu erstellen Seite **Projektinformation** neu erstellen, auf der die Geschäftslogik für jeden dieser Entitätstypen sicherstellt, dass das Feld **Art** des Datensatzes korrekt eingestellt ist, und alle obligatorischen Konzepte ordnungsgemäß initialisiert werden.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Nachverfolgen von Überarbeitungen von Angeboten und Projektplänen im Verkaufszyklus
In Project Operations ist es nicht möglich, Überarbeitungen an einem Angebot nachzuverfolgen. Stattdessen müssen Sie das vorhandene Angebot als **Als verloren geschlossen** markieren und dann ein neues Angebot erstellen. Sie können ein Angebot kopieren oder ein projektbasiertes Angebot klonen.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Nachverfolgungskommentare und Genehmigungen von Angeboten und Projektverträgen
Sie können die Überprüfung und Genehmigung von Angeboten und Projektverträgen mithilfe der Datensatzpinnwand und Beiträge verwalten. Ihre Organisation kann benutzerdefinierte Workflows und Plug-Ins erstellen, um die Benachrichtigungen zu Überprüfungs- und Genehmigungsarbeitselementen zuzuweisen, umzuleiten, zu eskalieren und zu verwalten.
