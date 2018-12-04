---
title: "Iepakojuma materiāli un papildmaksas"
description: "Iepakojuma materiālu papildmaksas pārstrādes uzņēmumam tiek maksātas zināmos laika intervālos. Apmaksa tiek veikta par smaguma mērvienību katram iepakojuma vienības sastāvā esošajam materiālam. Iepakojuma materiālu papildmaksas tiek aprēķinātas un iekļautas atskaitēs, bet netiek grāmatotas virsgrāmatas transakcijas, jo papildmaksas netiek uzskatītas par valsts iestādei maksājamiem nodokļiem."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b131cdfa2f0e3b6a8f116464323d49eaa4584634
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="packing-materials-and-fees"></a>Iepakojuma materiāli un papildmaksas

[!include [banner](../includes/banner.md)]

Iepakojuma materiālu papildmaksas pārstrādes uzņēmumam tiek maksātas zināmos laika intervālos. Apmaksa tiek veikta par smaguma mērvienību katram iepakojuma vienības sastāvā esošajam materiālam. Iepakojuma materiālu papildmaksas tiek aprēķinātas un iekļautas atskaitēs, bet netiek grāmatotas virsgrāmatas transakcijas, jo papildmaksas netiek uzskatītas par valsts iestādei maksājamiem nodokļiem.

Iepakojuma materiālu svars un maksa tiek aprēķināti pārdošanas pasūtījumu rindām un pirkšanas pasūtījumu rindām.

Vienu vai vairākas iepakojuma vienības varat definēt krājumam, krājumu grupas iepakojumam vai visiem krājumiem. Iepakojuma vienība sastāv no iepakojuma materiāliem, to svara un no iepakojuma vienībā ietilpstošo krājumu skaita. Iepakojuma materiāla kods tiek piešķirts katram definētajam iepakojuma materiālu tipam. Pamatojoties uz iepakojuma materiāla kodu, noteiktam periodam varat norādīt cenu. Iepakojuma materiāla maksa tiek aprēķināta, pamatojoties uz šo informāciju.

| **Piezīme.**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pat ja uzņēmumam nav jāsedz iepakojuma materiālu maksas, šo funkcionalitāti varat izmantot, lai aprēķinātu iepakojuma materiālu svara statistisko informāciju. |

## <a name="setup-requirements-for-packing-material-fees"></a>Iepakojuma materiālu maksu iestatīšanas prasības
Pirms iepakojuma materiālu svara vai iepakojuma materiālu maksu, vai to abu aprēķināšanas, jums ir jāizveido šādi pamatdati:

-   Iepakojuma grupas — izveidojiet iepakojuma grupas, ko piešķirt krājumiem.
-   Iepakojuma materiālu kodi — izveidojiet iepakojuma materiālu kodus katram definētajam iepakojuma materiālu tipam.
-   Iepakojuma vienības — norādiet iepakojuma vienību krājumam, iepakojuma grupai vai visiem krājumiem. Katrai iepakojuma vienībai definējiet, kādi iepakojuma materiāli tajā ietilpst, piešķiriet svarus un laukā Iepakojuma vienības koeficients ievadiet pārveidošanas koeficientu pārrēķināšanai no krājuma vienības.
-   Iepakojuma materiālu maksas — norādiet iepakojuma materiālu maksas pēc iepakojuma materiāla koda. Katram materiālu veidam definējiet derīguma periodu, cenu pēc materiāla, valūtu un vienību.

## <a name="packing-units-on-sales-order-lines"></a>Iepakojuma vienības pārdošanas pasūtījuma rindās
Kad veidojat pārdošanas pasūtījuma rindu, sistēma pārbauda, vai šim krājumam ir norādītas iepakojuma vienības. Ja iepakojuma vienības ir norādītas, tad pārdošanas pasūtījuma rindu sistēma atjaunina ar norādīto iepakojuma vienību un iepakojuma vienības daudzumu. Iepakojuma vienības daudzums ir balstīts uz pasūtīto daudzumu, dalītu ar atlasītajā iepakojuma vienībā ietilpstošo krājumu skaitu. Ja iepakojuma vienības nav norādītas, iepakojuma vienību un iepakojuma vienību skaitu varat manuāli ievadīt pārdošanas pasūtījuma rindā. Iepakojuma vienību un iepakojuma vienību daudzumu varat arī mainīt, kad grāmatojat pārdošanas pasūtījuma rindu. Tas ir svarīgi, ja pārdošanas pasūtījuma rinda ir tikai daļēji piegādāta vai daļēji iekļauta rēķinā. Kad izrakstāt rēķinu par pārdošanas pasūtījumu, tiek izveidotas iepakojuma materiālu transakcijas. Iepakojuma materiālu transakcijas ietver iepakojuma materiālu svaru attiecīgajai pārdošanas rindai. Šīs transakcijas varat labot arī pēc to iekļaušanas rēķinā un pēc tam izveidot jaunas transakcijas.

## <a name="packing-units-on-purchase-order-lines"></a>Iepakojuma vienības pirkšanas pasūtījuma rindās
Sistēma neveido iepakojuma materiālu transakcijas pirkšanas pasūtījuma rindai. Rēķinā iekļautajām pirkšanas pasūtījuma rindām jūs manuāli izveidojat transakcijas lapā **Iepakojuma materiālu transakcijas**.

## <a name="set-up-customer-packaging-material-fee-license-numbers"></a>Debitora iepakojuma materiāla maksas licenču numuru iestatīšana
Ja debitori maksā iepakojuma materiālu maksas, tad lapā **Debitori** norādiet debitora iepakojuma materiālu maksu licenču numurus. Kad licences numurs debitoram piešķirts, iepakojuma materiāla maksas tiek aprēķinātas automātiski, iekļaujot rēķinā pārdošanas pasūtījumus. Pēc rēķina izrakstīšanas lapā **Iepakojuma materiālu transakcijas** tiek notīrīta izvēles rūtiņas **Aprēķināt maksu** atzīme, jo jums nav jāaprēķina un jādrukā atskaite. Iepakojuma materiālu svaru varat drukāt rēķinā un informēt debitorus, ka viņi maksā šīs maksas. 

Ja jūsu uzņēmums maksā iepakojuma materiālu maksas, nenorādiet debitora licenču numurus. Pēc rēķina izrakstīšanas lapā **Iepakojuma materiālu transakcijas** ir atzīmēta izvēles rūtiņa **Aprēķināt maksu**. Tas norāda, ka maksas tiek aprēķinātas, kad tiek veidota atskaite. Šo svaru varat drukāt rēķinā un norādīt, ka jūsu uzņēmums maksā šīs maksas.

## <a name="print-packaging-material-weights-on-invoices"></a>Iepakojuma materiāla svaru drukāšana rēķinos
Iepakojuma materiālu svaru varat drukāt rēķinā un norādīt, kurš maksā iepakojuma materiāla maksu. Svars tiek summēts pēc iepakojuma koda.






