---
title: Finanzdimensions-Standardeinstellungen
description: Dieses Thema enthält Informationen zum Einrichten von Standardeinstellungen für Finanzdimensionen.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579489"
---
# <a name="financial-dimension-defaults"></a>Finanzdimensions-Standardeinstellungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_



Dynamics 365 Project Operations verwendet das [Framework für Finanzdimensionen](/dynamics365/finance/general-ledger/financial-dimensions) in Dynamics 365 Finance, um zusätzliche Einblicke in Projekttransaktionen in untergeordneten Sachkonten und in der Finanzbuchhaltung bereitzustellen.

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
3. Erweitern Sie **Zugehörige Informationen**, und wählen Sie die Registerkarte **Finanzierungsquellen** aus.
4. Richten Sie die Standardeinstellungen für die Finanzdimension ein. Beachten Sie, dass die finanziellen Dimensionen standardmäßig vom Kundenkonto ausgehen.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Legen Sie finanzielle Dimensionen für eine Vertragszeile fest

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektverträge**.
2. Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Projektvertrag**-Registerkarte **Standardabrechnung anzeigen** aus.
3. Erweitern Sie **Zugehörige Informationen**, und wählen Sie die Registerkarte **Vertragszeilen** aus.
4. Richten Sie die Standardeinstellungen für die Finanzdimension ein. Die Standardeinstellungen für die finanzielle Dimension gelten und können nur mit Festpreisvertragszeilen (Meilenstein) verwendet werden.

Diese Standardeinstellungen werden für zugehörige Projekttransaktionen und Rechnungsposten verwendet.

## <a name="define-default-financial-dimensions-for-projects"></a>Definieren Sie Standardfinanzdimensionen für Projekte

Projekte werden in CDS erstellt und gepflegt. Buchhaltungsattribute für Projekte werden im **Projektmanagement und Buchhaltung**-Modul in Finance festgelegt.

1. Wechseln Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Alle Projekte**.
2. Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Vertrag**-Registerkarte **Standardabrechnung anzeigen** aus.
3. Erweitern Sie **Zugehörige Informationen**, und wählen Sie die Registerkarte **Einrichtung** aus.
4. Richten Sie die Standardeinstellungen für die Finanzdimension ein. Beachten Sie, dass Finanzdimensionen standardmäßig vom Debitorenkonto ausgehen. Wenn das Projekt einer Vertragszeile mehreren Projektvertragsdebitoren zugeordnet ist, wird der primäre Debitor verwendet, um Finanzdimensionen als Standard festzulegen.

Die standardmäßigen Finanzdimensionen des Projekts werden verwendet, um die Standardeinstellungen für Buch.-Blattzeilen für Zeit‑, Spesen‑ und Gebührentransaktionen in der **Project Operations-Integrationserfassung** und auf verwandten Projektrechnungszeilen festzulegen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
