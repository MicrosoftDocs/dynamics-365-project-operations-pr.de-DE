---
title: Währungskonfliktfehler
description: Dieses Thema bietet Informationen zur Fehlerbehebung bei einem Währungskonfliktfehler, der beim Speichern bestimmter Datensatztypen auftritt.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903426"
---
# <a name="currency-mismatch-error"></a>Währungskonfliktfehler 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn Sie ein Projekt, einen Vertrag, ein Angebot oder eine buchbare Ressource speichern, erhalten Sie ggf. den Fehler **Das Angebot, das die Unternehmenswährung besitzt, stimmt nicht mit der Währung der Vertragseinheit überein. Wählen Sie zum Fortsetzen ein anderes Unternehmen oder eine Vertragspartei aus**. Dies liegt daran, dass eine Währungsinkongruenz zwischen der Währung der Vertragseinheit für den Datensatz und der Währung des Eigentümerunternehmens besteht.


## <a name="resolution"></a>Lösung

Führen Sie die folgenden Schritte aus, um dieses Problem zu umgehen:
- Überprüfen Sie die Währung der Vertragseinheit für diesen Datensatz. Sie können die Währung sehen, indem Sie den Datensatz der Organisationseinheit öffnen und den Wert auf der **Allgemein**-Registerkarte im **Währung**-Feld überprüfen.
- Überprüfen Sie die Währung der Eigentümergesellschaft. Sie können die Währung sehen, indem Sie auf **Verwandt** > **Sachkonten** im Firmendatensatz gehen. Doppelklicken Sie auf den mit der Firma verknüpften Sachkonto-Datensatz und überprüfen Sie den Wert auf der **Allgemein**-Registerkarte im **Buchhaltungswährung**-Feld.

Wenn die in der Vertragseinheit eingestellte Währung und der Sachkonto-Datensatz nicht übereinstimmen, passen Sie die Konfiguration an oder wählen Sie beim Sichern des Datensatzes andere Werte aus. Das System erfordert, dass diese Datensätze übereinstimmen, um korrekte konzerninterne Rechnungsflüsse sicherzustellen. Weitere Informationen zu Intercompany-Konfigurationen finden Sie unter [Intercompany-Transaktionen erstellen](../../project-accounting/create-intercompany-transactions.md).

Wenn dem Firmendatensatz kein zugehöriger Sachkontodatensatz zugeordnet ist, weist dies darauf hin, dass beim Einrichten der Umgebung eine Konfiguration fehlt. Der Systemadministrator muss die Konfiguration korrigieren. Der Systemadministrator muss zu **Konfigurationen für duales Schreiben** gehen und **Sachkonto-Zuordnung für duales Schreiben** mit der Erstsynchronisierung dieser Zuordnung und ihrer Voraussetzungen stoppen und neu starten. Weitere Informationen finden Sie unter [Project Operations-Zuordnungsversionen für duales Schreiben](../../environment/resource-dual-write-maps.md).
