---
title: Neuigkeiten Oktober 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom Oktober 2021 der Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen.
author: sigitac
ms.date: 10/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 078869ad01a23bac1108629c5f532ba57a2967e9
ms.sourcegitcommit: f37502a50cabdaf736aeba149feb5f8288e23df7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7753291"
---
# <a name="whats-new-october-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten Oktober 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

   - Project Operations in der Microsoft Dataverse-Umgebung Version 4.25.0.91
   - Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.21

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- [Projektbestellungen](../procurement/non-stocked-materials-project-purchase-orders.md) kann jetzt für die von der Beschaffungsabteilung verwaltete/zentrale Beschaffung für Projekte verwendet werden.
- [Lieferantenbindung](../procurement/vendor-retention-overview.md) können Sie einen Teil der Zahlungen an Lieferanten einbehalten.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Die aktive Version der Zuordnung können Sie auf der Seite Dual-write in der Spalte Version sehen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie Tabellenzuordnungsversionen auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2209402 | Die Validierungen wurden korrigiert, die verhinderten, dass Einbehaltungsbeträge in Rechnung gestellt wurden, wenn ein Projektvertrag bestätigt wurde. |
| Verkaufschancenmanagement | 2227414 | Die Felder **Produkt**, **Manueller Eintrag**, und **IsProductOverriden** werden in die Angebotszeilendetails und Vertragszeilendetails kopiert. |
| Preise und Abrechnung | 2338357 | Die Währung im Materialverwendungsprotokoll muss der Projektwährung entsprechen, wenn das Projekt ausgewählt wird. |
| Zeit und Ausgaben | 2414777 | Das Stornieren einer Genehmigung, wenn der Aufwands- oder Zeitbuchung mehr als eine Projektgenehmigung zugeordnet ist, muss möglich sein. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [412077](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D412077&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020681298%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JT2OvagELTPqep4rOiFTwGYF80KkgSHgBJmd%2BHBBgA8%3D&amp;reserved=0) | Wenn Sie der Einkaufsmanagerrolle Zugriff auf eine juristische Person gewähren, wird auch der Zugriff auf alle Projekte in allen juristischen Personen gefiltert. |
| Projektmanagement und -buchhaltung | [555604](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D555604&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=NGAT/5r0sezqdisYP%2BDzyFDDi5f9gyrr5ZhJZaDLV0k%3D&amp;reserved=0) | Die Eliminierung der Schätzung schlägt fehl, wenn die Funktion **Projektvertragswährung für Schätzungsberechnung aktivieren** aktiviert ist. |
| Projektmanagement und -buchhaltung | [564701](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564701&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IyhrFb59YBXjNpJdtPhlEDxoYiFCTrqzQtKZsBZk2DM%3D&amp;reserved=0) | [FRA] Die bedingte Steuer wird für die letzte Zahlung nicht korrekt berechnet, wenn der Kreditoreneinbehalt und die Vorauszahlung auf eine Bestellrechnung angewendet wurden. |
| Projektmanagement und -buchhaltung | [569250](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569250&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020741035%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YcB6z9MvvtiyT9d8g2GkHXDUcNfnPdxlYsHblbk%2BCXs%3D&amp;reserved=0) | WIP-Buchungen ins Hauptbuch werden mit einem falschen Betrag gebucht. |
| Projektmanagement und -buchhaltung | [581167](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D581167&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020989941%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=9UjX3lX/DOJOPiz%2BlYVge5F3Tpbb%2BUBaN7PVXkpwYJE%3D&amp;reserved=0) | Der Projektrechnungsbericht überspringt Zeilen. |
| Projektmanagement und -buchhaltung | [598810](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598810&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021408104%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=f2oJYnmjpfUiIKvF6qfLsBcfTjoSOq955%2B87%2BSIh0Io%3D&amp;reserved=0) | Beim Post-Batch der Projektrechnung gibt es ein Problem, bei dem der Rechnungsvorschlag verarbeitet und gebucht wird, auch wenn die Rechnungsposten nicht generiert wurden. |
| Projektmanagement und -buchhaltung | [578970](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D578970&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021876048%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JMg%2BIRbLiSKeIXN/JArWC3hSGFhNhabERbuKzGBKCC8%3D&amp;reserved=0) | Aktualisieren Sie die Erstellung eines Batch-Jobs für die Projektschätzung, um die Ausführung mehrerer Unteraufgaben zu unterstützen. |
| Projektmanagement und -buchhaltung | [586034](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586034&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021895962%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MRGsdBRM5spFKDJZ/IjrAoWy%2BGTyFVyUU7SCfFJSj6g%3D&amp;reserved=0) | Gutscheintransaktionen werden nicht als „XX/XX/XXXX“ bilanziert (Buchungswährung: 0,00 – Berichtswährung: 0,01). |
| Projektmanagement und -buchhaltung | [596669](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D596669&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021955698%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IpJrV7LW0CegdNrRXfDqBhLEsy8tlSvlaipvZBQFZVg%3D&amp;reserved=0) | Die Steuerbefreiungsnummer für eine juristische Person wird nicht auf einer gedruckten Projektrechnung angezeigt. |
| Projektmanagement und -buchhaltung | [598109](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598109&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021975611%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=erjkqXSdKwjU62xNiVEJomzc5JoiiC9U7f6ofrv4KGE%3D&amp;reserved=0) | Die Einrichtung einer fortlaufenden Nummernreihenfolge beim Posten einer Schätzung wird nach der Anwendung von KB 4619395 nicht unterstützt. |
| Projektmanagement und -buchhaltung | [602677](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602677&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4TBJC6dKbgZxWQTlyDkTm%2BzHpL%2BJx5ZcueNWkMJfUK4%3D&amp;reserved=0) | Der WIP-Stornowert aus der Rechnungsbuchung weicht vom ursprünglich gebuchten WIP-Wert aus der Zeiterfassung ab. |
| Projektmanagement und -buchhaltung | [602728](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Ux5tLxoBzA%2BJtbf5MhLB63/GNJqYcBg8PH4tncXLTsM%3D&amp;reserved=0) | Gutscheintransaktionen werden aufgrund eines Buchungsproblems mit vom Projekt in Rechnung gestellten Einnahmen in angewendeten Einbehaltungsfällen nicht korrekt ausgeglichen. |
| Projektmanagement und -buchhaltung | [607324](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D607324&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022065219%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=I/SwbTsPpFvMkxLIK7JpligW%2B4nlObh3nCCSppVGvhE%3D&amp;reserved=0) | Projektschätzungen werden nur für eine Periode erstellt. |
| Reisekosten und Ausgaben | [551911](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D551911&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=fDFL3GM5jXJAzIzxwRlOIaq3/ytSHXnpIzGsC4Jjphg%3D&amp;reserved=0) | Richtlinien für Reiseanforderungen werden ignoriert, um den Workflow fehlerfrei zu genehmigen. |
| Reisekosten und Ausgaben | [563752](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D563752&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SVrkNdniaVfhOjc3Brf1gtrFv3SJpPNQ4JYOGnCOxlQ%3D&amp;reserved=0) | Die Kostenstellen-Projekt-ID, die abrechenbare und die Aktivitätsnummer werden nicht in der mobilen Spesen-App gespeichert. |
| Reisekosten und Ausgaben | [569458](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569458&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020750990%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=cC33gCOlM8aa3jR5Hy1Hubf5bszsu2YWwraLLrIYCYk%3D&amp;reserved=0) | Das Feld **Beigefügte Quittung** ist auf **Ja** gesetzt, auch wenn der Spesenzeile keine Quittung beigefügt ist. |
| Reisekosten und Ausgaben | [571334](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D571334&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020760950%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Y6dd19CzWyWPa%2BItpWXBEgUuSx8evJxth6VslSRMYsg%3D&amp;reserved=0) | Wenn Sie versuchen, die Ausgabenkategorie in **Persönlich** zu ändern, wird eine Fehlermeldung angezeigt. |
| Reisekosten und Ausgaben | [572783](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D572783&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020770904%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=nugD/4Rj3d8CNanZf%2BY3vNm9aRqHoh5vF/bHFZD9UxE%3D&amp;reserved=0) | Nachdem eine Kreditkartentransaktion in einer Spesenabrechnung aufgeteilt wurde, können Sie die übergeordnete Ausgabe weder bearbeiten noch einen Beleg anhängen. |
| Reisekosten und Ausgaben | [574252](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574252&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020790818%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=uKYIlgBpKju4jBH%2BK8GXVKCgi6kxSG1AxXVvF75WsbA%3D&amp;reserved=0) | Die Spesenrichtlinie für konzerninterne Transaktionen mit einer Projekt-ID funktioniert nicht richtig. |
| Reisekosten und Ausgaben | [574489](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574489&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=ErBwfDvDtWWzEJP3STHd5kzPjTe7%2B4nCeG02kH64dWU%3D&amp;reserved=0) | Bei gebuchten Spesenabrechnungen fehlt das gebuchte Datum. |
| Reisekosten und Ausgaben | [574504](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574504&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SeW6L68CNpJ86TJ2aNqLZoTMq5PHRfu3542mNkKqf%2Bg%3D&amp;reserved=0) | Es gibt Probleme mit der Zahlungsmethode in der mobilen Spesen-App. |
| Reisekosten und Ausgaben | [584799](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D584799&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021129331%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4Q%2B/R9wPra2P/%2BEk63qgSenyNoJMa5OJsBv2Nn9s%2B%2Bo%3D&amp;reserved=0) | Eine Reiseanforderung, die für eine Arbeitskraft erstellt wurde, kann für die Spesenabrechnung einer anderen Arbeitskraft verwendet werden und kann die Reiseanforderung vor dem Delegiertendatum verwenden. |
| Reisekosten und Ausgaben | [586023](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586023&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021169156%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=d9Kmf1ng415Uw0U4aQ5N%2B0RboRmjDW1S2lt91rG9ofc%3D&amp;reserved=0) | Wenn ein Aufwand erstellt wird, werden sich ändernde Finanzdimensionswerte auf der Buchhaltungsverteilungsebene im Arbeitsplatz **Spesenmanagement**. |
| Reisekosten und Ausgaben | [586081](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586081&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021179116%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=LlWjcIANIl1gudmiD4WIsluKkF21w9EgVC5uDvBOzg4%3D&amp;reserved=0) | Der Genehmigungsstatus der Hauptausgabenzeile wird nicht mit dem Genehmigungsstatus des Einzelposten-Workflows synchronisiert. |
| Reisekosten und Ausgaben | [590544](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D590544&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021318495%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MolkGywocB%2BG404npaOv7fcfunnlDUGgAYFOcw8OlKg%3D&amp;reserved=0) | Beim Buchen einer Spesenabrechnung tritt ein Fehler auf, wenn **Steuerrückerstattung** in den Kostenverwaltungsparametern aktiviert ist. |
| Reisekosten und Ausgaben | [564851](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564851&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021856138%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YBsBJdzH%2BqbGzq07u7WILEs%2Bi5Ap6WYzqWnpGWcI4Ac%3D&amp;reserved=0) | Ein Delegierter kann keine Spesendokumente für einen gekündigten Mitarbeiter löschen. |
| Reisekosten und Ausgaben | [587306](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D587306&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021905919%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=TbWDuK1sHY//jTw%2BmehJG3M3N3feEl2oRkTMTkqWOVE%3D&amp;reserved=0) | Das Löschen einer Kostenzeile dauert lange und beeinträchtigt die Leistung. |
| Reisekosten und Ausgaben | [600455](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D600455&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021995524%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MH0sIRbAKhNNyAgYZzO9NovWHM7ZWKsoZYqXCIVHJ5A%3D&amp;reserved=0) | **TrvExpTrans** verursacht einen verwaisten **TaxUncommitted**-Datensatz nur durch Löschen von **SourceDocumentLine**. |