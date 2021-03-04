---
title: Vertriebsprozesse
description: Dieses Thema enthält Informationen zu den grundlegenden Vertriebsprozessen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145177"
---
# <a name="sales-processes"></a>Vertriebsprozesse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die Vertriebsprozesse, die in einer projektbasierten Organisation verwendet werden, unterscheiden sich von jenen, die in einer produktbasierten Organisation verwendet werden. Der Grund für diesen Unterschied ist, dass die Vertriebszyklen für projektbasierte Organisationen länger sind und zum Analysieren und Erstellen von Angeboten für jeden Auftrag benutzerdefinierter Schätzungstechniken bedürfen. Dynamics 365 Project Service Automation verwendet zum Teil die gleichen Funktionen, die im Vertriebsprozess für Dynamics 365 Sales verwendet werden. Im Folgenden finden Sie einige Beispiele hierfür:

- Eine Lead-Entität wird zur Nachverfolgung des Vertriebsprozesses verwendet.
- Qualifizierte Leads werden als Verkaufschancen nachverfolgt. Der Vertriebsprozess kann auch mit einer Verkaufschance beginnen.
- Es wird auf alle zugehörigen Artefakte einer Verkaufschance zugegriffen. Diese Artefakte umfassen das Vertriebsteam, die Stakeholder, die Wahrscheinlichkeit, die Bewertung, die Vertriebsphasen und Geschäftsprozesse.
- Für eine Verkaufschance werden mehrere Angebote erstellt.
- Ein Angebot wird als **Als gewonnen geschlossen** markiert, um einen Vertriebsauftrag zu erstellen. In PSA wird der Vertriebsauftrag angepasst und als Projektvertrag bezeichnet.

Die folgende Abbildung zeigt einen typischen Vertriebsprozess in einer projektbasierten Organisation.

> ![Vertriebsprozess in einer projektbasierten Organisation](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Einschätzung eines Verkaufs
Der Wert eines Verkaufs kann auf der Grundlage von zuvor gelieferten Projekten und der Komplexität von Projekten geschätzt werden. Für Projekte, bei denen es sich um Erweiterungen von vorherigen Projekten handelt, oder Projekte, bei denen der Zulieferer über hohe Fachkenntnisse verfügt und bekannte Arbeitsvorlagen verwendet werden, können Sie einen einfacheren Schätzungsprozess verwenden. Komplexere Projekte haben normalerweise einen längeren Kaufvorgang. Daher gibt es mehr Phasen in der Vertriebsvorkalkulation. Zu Beginn des Prozesses verwendet das Vertriebsteam die Beiträge von Account Managern und Fachleuten (SMEs – Subject Matter Experts), um eine allgemeine Schätzung für jede einzelne angebotene Arbeitskomponente zu erstellen. Diese Arbeitskomponenten werden durch Angebotszeilen dargestellt. 

Sie können eine allgemeine Schätzung des Angebots erstellen. Anschließend wird diese allgemeine Schätzung durch eine detailliertere Schätzung ersetzt, die auf einem Projektplan beruht, den Sie mithilfe der standardisierten Projektvorlagen erstellen. Mithilfe dieser Vorlagen können Sie einen Zeitplan erstellen und Geldbeträge für das Angebot und seine Komponenten (Angebotszeilen) ermitteln. 

Sie können für ein Projekt mehrere Angebote erstellen und sie unter einem Verkaufschancen-Entitätstyp gruppieren. Schließlich wird eines dieser Angebote als **Als gewonnen geschlossen** markiert, und ein Projektvertrag oder eine Leistungsbeschreibung (SOW, Statement of Work) wird erstellt. Ein Projektvertrag enthält den vertraglich vereinbarten Wert für jede Komponente (Vertragszeile), die vom Kunden zur Lieferung angenommen wird. Eine Leistungsbeschreibung wird normalerweise in der Form eines Microsoft Word-Dokuments erstellt. Alle Rechnungen, die dem Kunden im Laufe der Projektlieferung gesendet werden, verweisen auf den Projektvertrag oder die Leistungsbeschreibung.

Sie können auch andere Angebote unter einem Verkaufschancen-Entitätstyp erstellen oder das System so konfigurieren, dass ein Projektvertrag erstellt wird, wenn ein Angebot gewonnen wird. In diesem Fall können Sie dem Projektvertragsdatensatz ein Word-Dokument anfügen, das die Leistungsbeschreibung darstellt.

![Schließen eines Angebots, um einen Projektvertrag zu erstellen](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurieren des Vertriebsprozesses
Sie können Geschäftsprozessflüsse (BPFs, Business Process Flows) in Microsoft Dynamics 365 verwenden, um Ihren Vertriebsprozess zu konfigurieren. BPFs bieten dem Vertriebspersonal eine intuitive visuelle Sichtschnittstelle, mit der sie Geschäftsabschlüsse durch die für Ihr Unternehmen typischen Phasen vorantreiben können.

Beispielsweise verfügt Ihr Unternehmen über die folgenden sechs Phasen im Vertriebsprozess:

1. Qualifizieren
2. Schätzung
3. Interne Prüfung
4. Vertrag
5. Bereitstellen
6. Schließen

Diese sechs Phasen werden durch Doppelpfeile (\>) dargestellt, die Sie auswählen, um sie in jedem von Ihnen erstellten Verkaufschancen-Entitätstyp zu erweitern.

![Konfigurieren eines Geschäftsprozesses in Dynamics 365](media/basic-guide-3.png)
 
Ihre Organisation verwendet möglicherweise verschiedene Entitäten zur Darstellung des gleichen Auftrags, wie er sich entwickelt. Zu Beginn des Vertriebsprozesses wird ein Auftrag durch die Verkaufschancenentität dargestellt. Im Laufe der Zeit und wenn weitere Details bekannt werden, können Sie allgemeine Schätzungen verwenden, um ein oder mehrere Angebote zu erstellen. Wenn eines dieser Angebote von den internen und kundenseitigen Stakeholdern überprüft wird, stellt die Angebotsentität den Auftrag dar. Nachdem der Kunde das Angebot angenommen hat, wird der Auftrag durch einen Projektvertrag oder eine Leistungsbeschreibung repräsentiert. Um dieses Verhalten zu unterstützen, sind BPFs so strukturiert, dass jede Phase des Prozesses mit einer anderen Datenbanktabelle verknüpft ist.

Die Phase **Qualifizieren** im Vertriebsprozess kann durch eine Verkaufschancenentität unterstützt werden. Die Phasen **Schätzung** und **Interne Prüfung** können von einer Angebotsentität unterstützt werden. Die Phasen **Vertrag**, **Lieferung** und **Schließen** können über eine Projektvertragsentität unterstützt werden.

Beim Vorantreiben der Geschäfte durch die Phasen werden Sie aufgefordert, den entsprechenden Entitätsdatensatz zu erstellen, der Sie durch den Prozess führt und unterstützt. Die Phasen können bedingt sein. Wenn Sie beispielsweise nur dann eine interne Überprüfung eines Angebots benötigen, wenn im Angebot eine benutzerdefinierte Preisliste verwendet wird, können Sie diese Bedingung in der entsprechenden Phase des Geschäftsprozesses konfigurieren. Die Phase **Interne Prüfung** wird dann nur für Angebote angezeigt, in denen eine benutzerdefinierte Preisliste verwendet wird. Bei allen anderen Geschäftsabschlüssen und Angeboten folgt auf die Phase **Schätzung** die Phase **Vertrag**.

> [!NOTE]
> PSA bietet spezifische Seiten für die Entitäten Verkaufschance, Angebot, Auftrag und Rechnung. Sie müssen für diese Entitäten mithilfe der Projektinformationsseiten Project Service-Verkaufschancen, Angebote, Aufträge und Rechnungen erstellen. Wenn Sie zum Erstellen eines Datensatzes eine andere Seite verwenden, können Sie den Datensatz nicht über die Seite **Projektinformationen** öffnen. Wenn Sie einen Datensatz über die Seite **Projektinformationen** öffnen möchten, müssen Sie den Datensatz löschen und über die Seite **Projektinformationen** neu erstellen. Auf der Seite **Projektinformationen** sorgt die Geschäftslogik für jeden dieser Entitätstypen dafür, dass das Feld **Typ** des Datensatzes korrekt festgelegt ist und alle erforderlichen Konzepte ordnungsgemäß initialisiert werden.

> ![Projektinformationen für einen neuen Auftrag](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Unterschiede zwischen Project Service Automation und Vertrieb
Der Vertriebsprozess in PSA nutzt zwar die grundlegenden Funktionen des Vertriebsprozesses in Sales, weist jedoch einige wesentliche Unterschiede auf, da die Geschäftspraktiken projektbasierter Organisationen unterschiedlich sind. Im Folgenden finden Sie einige Beispiele hierfür:

- **Projektangebote** – In Project Service Automation wird ein Angebot geschlossen, nachdem ein Projektvertrag aus einem Angebot erstellt wurde. In Sales können Sie ein Angebot offen halten, nachdem Sie es gewonnen haben. Der Grund für diesen Unterschied ist, dass eine Übereinstimmung zwischen einem Angebot und einem Projektvertrag für projektbasierte Organisationen besser ist. 
- **Aktivierung und Überarbeitungen** – In PSA werden die Aktivierung und Überarbeitung von Projektangeboten nicht unterstützt. In Sales kann ein Angebot gesperrt werden, um weitere Bearbeitungen zu verhindern.
- **Schließen eines Angebots als verloren oder gewonnen** – Wenn in PSA ein Projektangebot als gewonnen oder verloren geschlossen wird, bleibt die Verkaufschance offen. Alle anderen Angebote für die Verkaufschance werden als verloren geschlossen. Wenn in Sales ein Angebot als gewonnen oder verloren geschlossen wird, wird der Benutzer aufgefordert, bei der Verkaufschance eine Aktion zu ergreifen. Je nach Benutzereingabe kann die zugrundeliegende Verkaufschance geschlossen oder offen gelassen werden.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Nachverfolgen von Überarbeitungen von Angeboten und Projektplänen im Verkaufszyklus
In PSA ist es nicht möglich, Überarbeitungen an einem Angebot nachzuverfolgen. Stattdessen müssen Sie das vorhandene Angebot als **Als verloren geschlossen** markieren und dann ein neues Angebot erstellen. Mit PSA können Sie ein Angebot kopieren oder ein projektbasiertes Angebot klonen.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Nachverfolgungskommentare und Genehmigungen von Angeboten und Projektverträgen
Sie können die Überprüfung und Genehmigung von Angeboten und Projektverträgen mithilfe der Datensatzpinnwand und Beiträge verwalten. Ihre Organisation kann benutzerdefinierte Workflows und Plug-Ins erstellen, um Benachrichtigungen zu Überprüfungs- und Genehmigungsarbeitselementen zuzuweisen, umzuleiten, zu eskalieren und zu verwalten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]