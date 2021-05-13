---
title: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
description: Nevar apstiprināt sūtījumu, jo nav izdoti krājumi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938511"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Nevar apstiprināt sūtījumu, jo nav izdoti krājumi

Kļūdas kods: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Daļa noslodzei %1 nepieciešamo krājumu vēl nav izdoti un pārvietoti uz galīgo nosūtīšanas novietojumu.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravu vai sūtījumu nevar apstiprināt tās pašreizējā stāvoklī, jo var pastāvēt viens no tālāk norādītajiem nosacījumiem:

- Saistītais darbs vēl nav izdots un pārvietots uz beigu nosūtīšanas vietu.
- Izdotais darba daudzums nesaskan ar kravas rindā izveidoto darba daudzumu.

## <a name="resolution"></a>Novēršana

Pārbaudiet ar kravu vai sūtījumu saistītos pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus. Pārliecinieties, ka visi saistītie darbi ir pabeigti galīgā nosūtīšanas vietā un ka daudzumi sakrīt.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Noslodzes rindas** atlasiet kravas rindas.
1. Atzīmējiet lauka **Darba izveidotais daudzums** vērtību.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet, vai darbs ir pabeigts galīgās nosūtīšanas vietā un vai izdotais darba daudzums sakrīt ar izveidoto darba daudzumu kravas rindā.
1. Atkārtojiet šo procedūru visām kravas rindām, lai nodrošinātu visu kritēriju izpildi.
