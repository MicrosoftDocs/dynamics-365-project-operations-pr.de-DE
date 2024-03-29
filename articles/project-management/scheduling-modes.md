---
title: Planungsmodi
description: Dieser Artikel enthält Informationen über Terminplanungsmodi.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923647"
---
# <a name="scheduling-modes"></a>Planungsmodi

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dynamics 365 Project Operations bietet Organisationen die Möglichkeit zu definieren, wie sie Änderungen an Schlüsselvariablen in Aufgaben innerhalb der Projektstrukturplan verwalten. Basierend auf den spezifischen Anforderungen der Organisation können Projektmanager Änderungen am Planungsmodus vornehmen, wenn ein Projekt erstellt wird.

In Project Operations stehen drei Planungsmodi zur Verfügung:

  - Feste Dauer (dies ist der Standardmodus)
  - Fester Aufwand (*Arbeit)*
  - Feste Einheiten

Die Werte, die von der Definition eines bestimmten Planungsmodus betroffen sind, werden durch die folgende Formel bestimmt:

  Anstrengung = Dauer x Einheiten

Wenn Sie den Planungsmodus eines Projekts definieren, legen Sie einen dieser Werte fest, der dann nicht geändert werden kann. Wenn Sie diesen Wert als Konstante halten, wird diesem Wert Priorität eingeräumt. Dadurch wird das System benachrichtigt, ihn nicht zu ändern, wenn sich die beiden anderen Werte ändern. Die folgende Tabelle enthält Informationen zu den Auswirkungen der Auswahl eines bestimmten Modus.

| **In dieser Aufgabe**             | **Wenn Sie Einheiten überarbeiten**   | **Wenn Sie Dauer überarbeiten** | **Wenn Sie Aufwand überarbeiten**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Feste Einheiten-Aufgabe     | Die Dauer wird neu berechnet. | Der Aufwand wird neu berechnet.    | Die Dauer wird neu berechnet. |
| Fester Aufwand - Aufgabe    | Die Dauer wird neu berechnet. | Einheiten werden neu berechnet.    | Die Dauer wird neu berechnet. |
| Feste Dauer - Aufgabe  | Der Aufwand wird neu berechnet.   | Der Aufwand wird neu berechnet.    | Einheiten werden neu berechnet.   |

Weitere Informationen zu den Auswirkungen eines bestimmten Modus finden Sie unter [ Ändern des Aufgabentyps für eine genauere Planung](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). In dem Artikel wird der Begriff **Arbeit** anstelle von **Aufwand** verwendet.

## <a name="change-the-organizations-scheduling-mode"></a>Ändern Sie den Planungsmodus der Organisation

Führen Sie die folgenden Schritte aus, um den Planungsmodus einer Organisation zu definieren.

1. Gehen Sie zu **Einstellungen**\> **Allgemein** \>**Parameter** und wählen Sie dann den Projektparameter aus. 
2. Auf der Seite **Projektparameter** wählen Sie den Standardplanungsmodus für die Organisation aus und definieren Sie dann die Fähigkeit des Projektmanagers, die Einstellung beim Erstellen eines neuen Projekts zu überschreiben.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Ändern Sie die Planungsmoduseinstellung für ein Projekt

Wenn eine Organisation dem Projektmanager erlaubt, den Standardplanungsmodus zu überschreiben, kann der Projektmanager diese Änderung vornehmen, wenn er ein neues Projekt erstellt. Nachdem das Projekt gespeichert wurde, kann der Planungsmodus jedoch nicht mehr geändert werden.

## <a name="copied-projects"></a>Kopierte Projekte

Da beim Ausführen der Aktion "Projekt kopieren" ein Projekt erstellt wird, kann der Projektmanager den Planungsmodus nicht festlegen. Das Zielprojekt verwendet standardmäßig immer den auf Organisationsebene definierten Modus.

## <a name="copied-tasks"></a>Kopierte Aufgaben

Wenn eine Aufgabe von einem Projekt in ein anderes kopiert wird, erbt die Aufgabe den Planungsmodus des Zielprojekts.
