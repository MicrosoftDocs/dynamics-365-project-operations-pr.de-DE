---
title: Finanzdimensions-Standardeinstellungen
description: Dieses Thema enthält Informationen zum Einrichten von Standardeinstellungen für Finanzdimensionen.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131882"
---
# <a name="financial-dimension-defaults"></a>Finanzdimensions-Standardeinstellungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dynamics 365 Project Operations verwendet das [Finanzdimensionen](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions)-Framework in Dynamics 365 Finance, um zusätzliche Einblicke in Projekt-Nebenbuch- und Hauptbuchtransaktionen zu erhalten.

Standardmäßige Finanzdimensionen können für einen Kunden, eine Projektfinanzierungsquelle, einen Meilenstein, eine Projektvertragszeile oder ein Projekt festgelegt werden.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definieren Sie Standardfinanzdimensionen für einen Kunden

Die Standardeinstellungen für die Kundendimension sind in Finance angegeben. Zum Festlegen der Dimensionsstandards müssen Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Debitorenkonten** > **Debitoren** > **Alle Debitoren**.
2. Legen Sie auf der **Kunden**-Seite auf der Registerkarte **Finanzielle Dimensionen** die finanziellen Dimensionswerte für einen bestimmten Kunden fest.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definieren Sie Standardfinanzdimensionen für Projektverträge

Projektverträge werden in Common Data Service (CDS) erstellt und gepflegt. Buchhaltungsattribute für Projektverträge werden im **Projektmanagement und Buchhaltung**-Modul in Finance festgelegt.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Legen Sie finanzielle Dimensionen für eine Projektfinanzierungsquelle fest

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektverträge**.
2. Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Projektvertrag**-Registerkarte **Standardabrechnung anzeigen** aus.
3. Erweitern Sie **Verwandte Informationen** und wählen Sie die **Finanzierungsquellen**-Registerkarte aus.
4. Legen Sie die Finanzdimensions-Standardeinstellungen fest. Beachten Sie, dass die finanziellen Dimensionen standardmäßig vom Kundenkonto ausgehen.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Legen Sie finanzielle Dimensionen für eine Vertragszeile fest

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektverträge**.
2. Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Projektvertrag**-Registerkarte **Standardabrechnung anzeigen** aus.
3. Erweitern Sie **Verwandte Informationen** und wählen Sie die **Vertragszeilen**-Registerkarte aus.
4. Legen Sie die Finanzdimensions-Standardeinstellungen fest. Die Standardeinstellungen für die finanzielle Dimension gelten und können nur mit Festpreisvertragszeilen (Meilenstein) verwendet werden.

Diese Standardeinstellungen werden für verwandte Projekttransaktionen und Rechnungspositionen verwendet.

## <a name="define-default-financial-dimensions-for-projects"></a>Definieren Sie Standardfinanzdimensionen für Projekte

Projekte werden in CDS erstellt und gepflegt. Buchhaltungsattribute für Projekte werden im **Projektmanagement und Buchhaltung**-Modul in Finance festgelegt.

1. Wechseln Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Alle Projekte**.
2. Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Vertrag**-Registerkarte **Standardabrechnung anzeigen** aus.
3. Erweitern Sie **Verwandte Informationen** und wählen Sie die **Einrichtung**-Registerkarte aus.
4. Legen Sie die Finanzdimensions-Standardeinstellungen fest. Beachten Sie, dass die finanziellen Dimensionen standardmäßig vom Kundenkonto ausgehen. Wenn das Projekt einer Vertragszeile mit mehreren Projektvertragskunden zugeordnet ist, wird der Hauptkunde verwendet, um finanzielle Dimensionen festzulegen.

Die finanziellen Standarddimensionen des Projekts werden verwendet, um die Standardeinstellungen für Journalzeilen für Zeit-, Kosten- und Gebührentransaktionen im **Project Operations-Integrationsjournal** und für verwandte Projektrechnungszeilen festzulegen.
