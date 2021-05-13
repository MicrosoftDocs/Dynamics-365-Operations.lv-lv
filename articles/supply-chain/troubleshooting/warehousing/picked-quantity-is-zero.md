---
title: Nevar apstiprināt kravu, jo daudzums ir nulle
description: Nevar apstiprināt kravu, jo daudzums ir nulle
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938510"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Nevar apstiprināt kravu, jo daudzums ir nulle

Kļūdas kods: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Noslodzes rinda krājumam %1 un sūtījumam %2 tika atjaunināta uz nulli nepilnas piegādes iestatījuma dēļ, kurš šim krājumam neļauj nosūtīt nekādu daudzumu.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Sistēma novērtē, vai izdotais daudzums atbilst paredzamajiem ierobežojumiem, balstoties uz izdoto daudzumu, noslodzes rindas daudzumu un nepilnā pasūtījuma procentuālo vērtību. Ja sistēma konstatē, ka kravas rindā izdotais daudzums ir 0 (nulle), sūtījumu nevar apstiprināt. Piemēram, šī problēma var rasties, ja darbs ir atcelts un kravas rindas nepilnā pasūtījuma procentuālā vērtība ir 100 procenti.

## <a name="resolution"></a>Novēršana

Pārbaudiet kravas rindas, lai nodrošinātu, ka nepilnā pasūtījuma procentuālā vērtība un daudzumi ir saskaņoti ar izdoto darbu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz nepilnā pasūtījuma procentus.
1. Pēc vajadzības koriģējiet lauka **Nepilns pasūtījums** vērtību vai lauku **Daudzums**.

> [!TIP]
> Ja problēma vēl nav fiksēta, iespējams, būs jāpabeidz vairāk izdošanas darbu saistītajiem pārdošanas pasūtījumiem vai pārsūtīšanas pasūtījumiem, līdz pieejamais daudzums ir saskaņots ar kravu vai sūtījumu.
