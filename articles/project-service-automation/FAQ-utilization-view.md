---
title: Fakturierbare Nutzung für Ressourcen anzeigen
description: Dieses Thema enthält Informationen zur Ressourcennutzungsansicht.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721928"
---
# <a name="view-chargeable-utilization-for-resources"></a>Fakturierbare Nutzung für Ressourcen anzeigen
 
In der **Nutzungsansicht** auf der Seite **Project Service Ressourcennutzung** wird die fakturierbare Nutzung für jede buchbare Ressource angezeigt. Da die Ansicht auf der Zeitplanübersicht basiert, sehen Sie viele der gleichen Funktionen.

> ![Screenshot der Nutzungsansicht](media/FAQ-utilization-1.png)
 

Anrechenbare Nutzungsberechnungsverwendung funktioniert wie folgt:

   Fakturierbare Nutzung = (Fakturierbare tatsächliche Stunden) / (Ressourcenkapazität)

Die Zellen repräsentieren die berechnete fakturierbare Nutzung für den ausgewählten Zeitraum (Tage, Wochen oder Monate).

Die Farben in jeder Zelle zeigen die fakturierbare Nutzung für eine Ressource verglichen mit der Zielvorgabe der fakturierbaren Nutzung an. 

Die Zielnutzung kann auf die Standardrolle der Ressource oder auf die einzelne Ressource selbst festgelegt werden. Bei der Berechnung wird zuerst die Person für das Ziel und dann die Standardrolle der Ressource betrachtet.

## <a name="set-target-on-a-resource"></a>Festlegen des Ziels für eine Ressource

1. Navigieren Sie zu **Ressourcen** \> **Ressourcen**. 
2. Wählen Sie eine Ressource aus, um den Datensatz zu öffnen. 
3. Auf der Registerkarte **Project Service** können Sie die Zielnutzung der Ressource festlegen.

> ![Screenshot der Verwendung der Project Service Registerkarte, um die Zielnutzung festzulegen](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Festlegen der Zielnutzung für eine Rolle

1. Wechseln Sie zu **Ressourcen** \> **Ressourcenrollen**. 
2. Wählen Sie eine Rolle aus und öffnen Sie den Datensatz. 
3. Prozentsatz der Zielnutzung für die Rolle festlegen.

> ![Screenshot der Verwendung der Project Service Registerkarte, um die Zielnutzung festzulegen](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Berechnen der fakturierbaren Nutzung für eine Ressourcen

Um die fakturierbare Nutzung für eine Ressource zu berechnen, müssen Sie einige Voraussetzungen erfüllen. 

### <a name="set-default-role-for-individual-resource"></a>Festlegen der Standardrolle für einzelne Ressourcen

Zunächst muss die Zielnutzung entweder für die einzelne Ressource oder für Ressourcenrollen festgelegt werden. Wenn Sie Ressourcenrollen für Ziele verwenden, muss jede einzelne Ressource eine Standardrolle haben. 

1. Wechseln Sie dazu zu **Ressourcen** \> **Ressourcen**. 
2. Wählen Sie eine Ressource aus, öffnen Sie den Datensatz, und wählen Sie dann die Registerkarte **Project Service** aus. 
3. Stellen Sie im Raster **Ressourcenrolle** sicher, dass es eine Rolle für die Ressource gibt und dass der Wert **Ist Standard** auf **Ja** festgelegt ist.
 
### <a name="change-billing-type-for-resource-role"></a>Ändern des Rechnungstyps für die Ressourcenrolle

Die Ressourcenrollen müssen festgelegt werden, damit ein Fakturierungstyp **Fakturierbar** verfügbar ist. 

1. Wechseln Sie zu **Ressourcen** \> **Ressourcenrollen**. 
2. Öffnen Sie den Datensatz, den Sie aktualisieren möchten, und setzen Sie den Fakturierungstyp auf **Fakturierbar**.

### <a name="set-working-hours-for-resource-role"></a>Festlegen der Arbeitsstunden für die Ressourcenrolle
 
Die Ressource muss Arbeitszeit haben für die Kapazitätsberechnung. 

1. Navigieren Sie zu **Ressourcen** \> **Ressourcen**. 
2. Wählen Sie eine Ressource aus, um den Datensatz zu öffnen, und wählen Sie dann **Arbeitsstunden anzeigen** aus. 
3. Sie können auf der Ressourcenliste ein Bulk-Update durchführen, indem Sie eine **Arbeitszeitvorlage** aus der Ansicht **Ressourcenliste** anwenden.

## <a name="troubleshooting-chargeable-actual-hours"></a>Problembehandlung bei fakturierbaren tatsächlichen Stunden

Die fakturierbaren tatsächlichen Arbeitsstunden werden aus der Entität **Ist-Werte** erstellt. Ist-Werte mit dem Fakturierungstyp **Fakturierbar** werden in die Berechnung einbezogen. Aus diesem Grund müssen Projekte vorhanden sein, bei denen die Ist-Werte fakturierbar sind.

Wenn Sie keine fakturierbare Nutzung finden, sind hier einige Dinge, die Sie überprüfen können:

- Die Ressourcen mit Arbeitszeit, die für Kapazität definiert sind.
- Die Ressource hat entweder einzelne definierte Nutzungsziele oder eine zugewiesene Standardrolle. Die Rolle verfügt über ein Nutzungsziel, das dafür definiert ist.
- Ist-Werte weisen für den Zeitraum, für den Sie eine Nutzungsberechnung erwarten, den Fakturierungstyp **Fakturierbar** auf. Überprüfen Sie Folgendes, wenn Ist-Werte mit Fakturierungstypen anders als „fakturierbar” angezeigt werden:

  - Die Rolle, die für die Ist-Werte verwendet wird, hat einen Standardfakturierungstyp, der nicht anrechenbar ist.
  - Die Rolle in der Projektvertragszeile, die das Projekt unterstützen, sind auf nicht verrechenbar festgelegt.
  - Das Projekt hat keine zugewiesenen Vertragszeilen.

