---
title: Organisationseinheiten
description: Dieser Artikel beschreibt das Konzept der organisatorischen Einheiten und erläutert, wie Sie organisatorische Einheiten in Microsoft Dynamics 365 Project Operations erstellen und pflegen.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921623"
---
# <a name="organizational-units-overview"></a>Übersicht über Organisationseinheiten

In Microsoft Dynamics 365 Project Operations ist eine *Organisationseinheit* eine eigene Gruppe oder ein eigener Geschäftsbereich in einem Unternehmen für professionelle Dienstleistungen, die abrechenbare Ressourcen mit Kostenraten einsetzt.

Bei Unternehmen für professionelle Dienstleistungen, die technische Ressourcen in verschiedenen Praxisbereichen oder Geschäftszweigen verwenden, können sich die Kosten je nach dem Praxisbereich oder dem Geschäftszweig, in dem die Rolle ausgefüllt wird, unterscheiden. In diesem Szenario hilft das Konzept der Organisationseinheiten, indem es eine Möglichkeit bereitstellt, einen Satz von abrechenbaren Rollen in einem Geschäftsbereich eines Unternehmens zu gruppieren, das eine eindeutige Kostenstruktur für diese Rollen hat.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Das Konzept der Organisationseinheiten im Project Operations

In Project Operations hat eine Organisationseinheit eine bestimmte Währung und spezielle Einstandspreislisten.

Die Währung einer Organisationseinheit ist die primäre Währung, die für die Nachverfolgung von Kosten verwendet wird.

Mindestens eine Einstandspreisliste kann jeder Organisationseinheit angefügt werden. Project Operations legt die folgenden Einschränkungen für die Preislisten fest, die einer Organisationseinheit angefügt werden können:

- Die Preislisten müssen in der Währung der Organisationseinheit vorliegen.
- Die Preislisten müssen aus Einstandspreislisten bestehen.

Darüber hinaus enthält die Resource-Entität ein Attribut für die Organisationseinheit. Jeder Ressource kann einer Organisationseinheit zugewiesen werden.

### <a name="roles-of-organizational-units"></a>Rollen von Organisationseinheiten

Die Organisationseinheit hat in Project Operations zwei Rollen:

- **Vertragseinheit** – Die Organisationseinheit, die die Unternehmensgruppe oder den Geschäftsbereich darstellt, die bzw. der hauptsächlich für den Verkaufsabschluss und die Verwaltung der Lieferung von Arbeit und Services an den Kunden verantwortlich ist. Die Vertragseinheit wird anhand des Felds **Vertragseinheit** im Kopfzeilenabschnitt der Seiten **Verkaufschance**, **Angebot**, **Projektvertrag** und **Projekt** ermittelt.
- **Ressourceneinheit** – Die Organisationseinheit, zu der eine Ressource gehört oder der sie zugewiesen ist. Die Organisationseinheit kann ihre Ressourcen für bestimmte Rollen bei Leistungsbeschreibungen und Projekten bereitstellen, die der Vertragseinheit gehören.

![Vertrags- und Ressourceneinheiten.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>FAQ zu Organisationseinheiten

Hier finden Sie einige der am häufigsten gestellten Fragen zu Organisationseinheiten.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Wie steht die Organisationseinheitsentität in Project Operations in Verbindung zur Organisationsentität, die bereits in Dynamics 365 vorhanden ist?

Die Organisationsentität in Dynamics 365 stellt den Namen einer globalen Dynamics 365-Instanz dar. Dieser Name ist gewöhnlich der Name des globalen Unternehmens.

Die Organisationseinheitsentität stellt eine Gruppe oder einen Geschäftsbereich im globalen Unternehmen dar. Diese Gruppe oder dieser Geschäftsbereich weist ganz Gruppe von Rollen und eine Einstandspreisliste für diesen Rollen auf. Und diese Rollen und Preislisten unterscheiden sich von den Rollen und der Preisliste anderer Gruppen oder Geschäftsbereiche im Unternehmen.

Wenn Project Operations installiert ist, wird eine Standardorganisationseinheit basierend auf der Organisation erstellt. Alle vorhandenen Ressourcen werden der Standardorganisationseinheit zugewiesen. Wenn neue Active Directory-Benutzer oder -Ressourcen in Dynamics 365 importiert werden, weist der Benutzerimportvorgang diese der Standardorganisationseinheit in Project Operations zu.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Wie unterscheidet sich die Organizational Unit-Entität von der Business Unit-Entität?

In Dynamics 365 ist die Unternehmenseinheitsentität ein Sicherheitskonstrukt. Der Zuordnung eines Benutzers mit einer Unternehmenseinheit bestimmt die Entitäten und die Entitätsdatensätze, auf die der Benutzer Zugriff hat. Er bestimmt auch die Berechtigungen (Erstellen, Lesen, Schreiben, Löschen, Anfügen, Anfügen an, Zuweisen oder Teilen), die der Benutzer für diese Entitätsdatensätze hat.

Die Organisationseinheitsentität stellt eine Unternehmensgruppe oder einen Geschäftsbereich dar, die bzw. der eigene Kostenraten für Mitarbeiter hat, der bzw. dem sie zugewiesen ist. Durch die Zuordnung einer Ressource zu einer Organisationseinheit werden die Kosten der Ressource für eine Projektarbeit bestimmt.

Wenn Sie Dynamics 365 implementieren, optimieren Sie die Sicherheitsautorisierung für die Hierarchie von Unternehmenseinheiten und die Zuweisung von Benutzern zu Unternehmenseinheiten. Weisen Sie allen Benutzern, die normalerweise auf dieselbe Datensatzgruppe in derselben Unternehmenseinheit zugreifen müssen. Die Organisationseinheit hat keine Auswirkungen auf die Sicherheitsautorisierung oder den Zugriff.

**Beispiel, das einen möglichen Unterschied in der Modellierung von Organisationseinheiten und Geschäftseinheiten zeigt**

Contoso, Ltd. hat eine florierende Microsoft-Technologiepraxis. Falk und Emilia sind beides C\#-Entwickler, aber Emilia befindet sich in den USA, während Falk sich in Indien befindet. Die meisten Projektarbeiten erfordern Ressourcen aus Contoso Indien und Contoso USA. Falk und Emilia brauchen dieselbe Sicherheitszugriffsebene für Projekte in diesem Praxisbereich. Allerdings unterscheiden sich die Kosten für Entwickler von Contoso Indien erheblich von den Kosten für Entwickler von Contoso USA.

Hier finden Sie eine optimale Methode zur Entwicklung dieses Szenarios unter Verwendung von Dynamics 365 und Project Operations.

1. Erstellen Sie die Microsoft-Technologiepraxis als Unternehmenseinheit und ordnen Sie dieser Falk und Emilia zu. Auf diese Weise können Sie sicherstellen, dass beide Mitarbeiter dieselbe Sicherheitszugriffsebene für alle Projekte in diesem Praxisbereich haben. Sie können beide den Fortschritt, die Berichtszeit, Ausgaben, Materialnutzung und Aufgabenupdates überprüfen.
2. Erstellen Sie zwei Organisationseinheiten, um sicherzustellen, dass die Kosten des Projekt ordnungsgemäß aktualisiert werden.
3. Ordnen Sie Emilia Contoso USA und Falk Contoso Indien zu.
4. Weisen Sie beiden Organisationseinheiten entsprechende Einstandspreislisten zu. Auf diese Weise können Sie sicherstellen, dass die Kosten, die im Rahmen des Projekts für Falk und Emilia erfasst werden, auch genau die Kostendifferenz zwischen Contoso USA und Contoso Indien widerspiegeln.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Hängen Organisationseinheiten mit Vertriebsgebieten in Dynamics 365 zusammen?

Es gibt keine Zuordnung oder Beziehung zwischen Vertriebsgebieten und Organisationseinheiten. Ein Vertriebsgebiet ist normalerweise ein geografischer Bereich, in dem Vertriebsaktivitäten auftreten. Eine Vertriebspreisliste kann jedem Vertriebsgebiet zugeordnet werden.

Die Organisationseinheit ist eine interne Gruppe oder ein interner Geschäftsbereich im Unternehmen, bei der bzw. bei dem Kosten für eine Gruppe von Rollen nachverfolgt werden, die an andere Geschäftsbereiche oder externe Debitoren verkauft werden.

**Beispiel, das einen möglichen Unterschied in der Modellierung von Organisationseinheiten und Vertriebsgebieten zeigt**

Contoso, Ltd. hat zwei Entwicklungszentren: Contoso USA und Contoso Indien. Die Kosten für Ressourcen variieren zwischen diesen beiden Entwicklungszentren stark. Contoso verkauft seine IT-Services in vielen internationalen Märkten, wie Lateinamerika, Nordamerika, Asien-Pazifik, Westeuropa und dem Mittleren Osten. Die Rechnungssätze für dieselben Projektrollen können in diesen Märkten stark variieren. Contoso USA und Contoso Indien sollten als Organisationseinheiten eingerichtet werden, und jede Organisationseinheit sollte ihre eigene Einstandspreisliste haben. Asien-Pazifik, Lateinamerika, Nordamerika, Westeuropa und der Mittlere Osten sollte als Vertriebsgebiete eingerichtet werden, und jedes Vertriebsgebiet sollte eine eigene Vertriebspreisliste haben.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Warum gibt es eine Einschränkung bei der Zuordnung von Preislisten zu Organisationseinheiten?

Die Vertriebspreisgestaltung ist normalerweise für die geografischen Gebiete oder Märkte einzigartig, in denen die Services verkauft werden. Interne Geschäftsbereiche eines Unternehmens haben in der Regel keine eigene Vertriebspreisgestaltung für denselben Typ von Services. Allerdings haben interne Geschäftsbereiche verschiedene Kosten der verkauften Waren (Cost Of Goods Sold, COGS), je nach den Fähigkeiten der beschäftigten Personen und den Arbeitsbedingungen der Region, in der sie tätig sind. Da Organisationseinheiten als interne Geschäftsbereiche eines Unternehmens erstellt werden, können sie nur Einstandspreislisten haben.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Warum können Vertriebspreislisten nicht Organisationseinheiten zugeordnet werden?

In Project Operations können Vertriebspreislisten Kunden und Vertriebsgebieten zugeordnet werden. Bei Transaktionsentitäten wie Verkaufschance, Angebot, Projektvertrag und Projekt werden Vertriebspreislisten verwendet, die dem Kundenkonto oder dem Vertriebsgebiet angefügt sind, um die Rechnungssätze und den potenziellen Umsatz für die Projektarbeit zu ermitteln.

Einstandspreislisten werden Organisationseinheiten zugeordnet. Transaktionsentitäten wie Verkaufschance, Angebot, Projektvertrag und Projekt verwenden Einstandspreislisten, die der Vertragseinheit angefügt werden, um die Kosten für die Projektarbeit zu ermitteln.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Sind Organisationseinheiten in Project Operations hierarchisch?

Nein. In der aktuellen Version von Project Operations sind Organisationseinheiten nicht hierarchisch. Daher können Sie die folgenden Aufgaben ausführen:

- Konfigurieren eines Musters für die Eingabe von Standardeinstandspreisen im Rahmen einer Hierarchie.
- Erfassen von Umsätzen oder Kosten, die in unterschiedlichen Ebenen der Organisationseinheitshierarchie zusammengefasst sind.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Wir sind ein großes multinationales Unternehmen mit einer komplexen, mehrstufigen Hierarchie von Kostenstellen, Abteilungen und Rechnungsstellen. Wie können wir eine optimale Verwendung des Konzepts von Organisationseinheiten in der aktuellen Version von Project Operations sicherstellen?

Wenn Sie eine komplexe Hierarchie von Kostenstellen, Geschäftsbereichen, Abrechnungsbüros usw. haben, richten Sie die Blattknoten dieser Hierarchie als einzelne Organisationseinheiten ein.

Im folgenden Beispiel wird eine typische Hierarchie dargestellt.

**Contoso Indien**

- SAP-Praxis

    - Technische Berater
    - Fachberater

- Microsoft-Technologiepraxis

    - Technische Berater
    - Funktionale Berater

**Contoso US**

- SAP-Praxis

    - Technische Berater
    - Funktionale Berater

- Microsoft-Technologiepraxis

    - Technische Berater
    - Fachberater

Wenn Ihre Hierarchie diesem Beispiel ähnlich ist, müssen Sie sie als flache Liste einrichten, wie hier angezeigt:

- Contoso Indien – SAP-Praxis – Technische Berater
- Contoso Indien – SAP-Praxis – Funktionale Berater
- Contoso Indien – Microsoft-Technologiepraxis – Funktionale Berater
- Contoso Indien – Microsoft-Technologiepraxis – Funktionale Berater
- Contoso USA – SAP-Praxis – Technische Berater
- Contoso USA – SAP-Praxis – Funktionale Berater
- Contoso USA – Microsoft-Technologiepraxis – Technische Berater
- Contoso USA – Microsoft-Technologiepraxis – Funktionale Berater

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Wir sind ein kleines Unternehmen für professionelle Dienstleistungen, das lediglich über einen Geschäftsbereich verfügt. Wie können wir eine optimale Verwendung des Konzepts von Organisationseinheiten in der aktuellen Version von Project Operations sicherstellen?

Wenn Ihr Unternehmen als eine Einheit mit einer Einstandspreisliste tätig ist, müssen Sie keine Organisationseinheiten einrichten. Während der Project Operations-Installation erstellt Dynamics 365 eine Standardorganisationseinheit mit demselben Namen wie die Organisation. Standardmäßig werden alle Benutzer dieser Organisationseinheit zugewiesen. Jedes Mal, wenn das System angibt, dass die Organisationseinheit ausgewählt werden muss, wird diese Organisationseinheit standardmäßig ausgewählt.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Wenn ein Projekt aus einem Angebot oder einer Projektvertragszeile erstellt wird, stammt die standardmäßige Vertragseinheit aus dem Angebot oder dem Projektvertrag. Was ist die Standardvertragseinheit, wenn ein Projekt vor den Vertriebsentitäten wie einem Angebot oder einem Projektvertrag erstellt wurde?

Wenn ein Projekt eigenständig erstellt wird, basiert die standardmäßige Vertragseinheit des Projekts auf dem Benutzer, der sie erstellt. Dieser Benutzer ist auch der Standardprojektmanager. Wenn das Projekt einer Vertriebsentität wie einem Angebot oder einem Projektvertrag zugeordnet ist, basiert die Vertragseinheit im Projekt stattdessen auf der Vertriebsentität. In diesem Fall werden Projektschätzungen möglicherweise neu berechnet, da die Einstandspreisliste verwendet wird, um Änderungen der Kostenschätzung zu berechnen, wenn die Vertragseinheit geändert wird. Die Vertriebspreisliste wird verwendet, um die Vertriebsschätzungen zu berechnen, die geändert werden, damit sie mit der Projektpreisliste im Angebot konsistent sind.

Die Felder **Vertragseinheit** und **Währung** im Projekt sind zum Bearbeiten gesperrt, da sie mit den Werten in der Vertriebsentität konsistent sein müssen (Angebot oder Projektvertrag), der das Projekt zugeordnet ist.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Erstellen und pflegen von Organisationseinheiten in Project Operations

Führen Sie folgende Schritte aus, um in Project Operations eine Organisationseinheit zu erstellen.

1. Wechseln Sie zu **Einstellungen \> Organisationseinheiten**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Bereich **Allgemeinen** im Feld **Name** einen Namen für die Organisationseinheit ein. Legen Sie dann die anderen Felder wie erforderlich fest.
4. Wählen Sie **Speichern** aus, um den Datensatz zu erstellen, sodass Sie es weiter bearbeiten können.
5. Unter **Kostenpreislisten** wählen Sie das Pluszeichen (**+**), um eine Preisliste hinzuzufügen. Sie können hier nur Preislisten mit dem **Kosten**-Kontext hinzufügen.
6. Wählen Sie im Feld **Name** auf die Schaltfläche **Suchen**, und wählen Sie eine Preisliste aus, die Sie für die Organisationseinheit verfügbar machen wollen. Fügen Sie dann nach Bedarf weitere Preislisten hinzu.
7. Wenn Sie das Hinzufügen von Preislisten abgeschlossen haben, wählen Sie **Speichern** unten rechts auf der Seite aus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
