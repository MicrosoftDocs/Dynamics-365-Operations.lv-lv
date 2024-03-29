---
title: Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu
description: Šajā rakstā ir scenārijs, kurā vairāki pasūtījumi ir izlaisti nosūtīšanai uz noliktavu un pēc tam konsolidēti vēlāk, izmantojot lapu Konsolidēt sūtījumus.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 05f094b82b3d9bf9c095bc43f404aa7159bcafba
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427909"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir scenārijs, kurā vairāki pasūtījumi ir izlaisti nosūtīšanai uz noliktavu un pēc tam konsolidēti vēlāk, izmantojot **lapu Konsolidēt sūtījumus**.

## <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šī raksta scenārijā ir atsauces uz vērtībām un ierakstiem, kas iekļauti standarta demonstrācijas datos, kas tiek nodrošināti korporācijai Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Iestatīt sūtījumu konsolidācijas politikas un preču filtrus

Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus. Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.

## <a name="create-the-sales-orders-for-this-scenario"></a>Izveidot pārdošanas pasūtījumus šim scenārijam

Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt. Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem. Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.

Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.

### <a name="create-sales-orders-1-and-2"></a>Pārdošanas pasūtījumu 1 un 2 izveide

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Kopa:** *ShipCons*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

### <a name="create-sales-orders-3-and-4"></a>Pārdošanas pasūtījumu 3 un 4 izveide

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Kopa:** atstājiet šo lauku tukšu.

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

## <a name="release-the-orders-to-the-warehouse"></a>Pasūtījumu izlaišana noliktavā

Sekojiet šiem soļiem, lai izlaistu pārdošanas pasūtījumu, ko izveidojāt šim scenārijam noliktavā.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atrodiet un atlasiet izlaižamo pārdošanas pasūtījumu.
1. Darbību rūtī cilnē **Noliktava**, atlasiet **Darbības \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto pārdošanas pasūtījumu.
1. Atkārtojiet šo procedūru katram otrajam pārdošanas pasūtījumam, ko izveidojāt šim scenārijam.

## <a name="consolidate-shipments"></a>Konsolidēt sūtījumus

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Meklējiet un atlasiet sūtījumu, kas tika izveidots, kad pārdošanas pasūtījums 1 tika nodots noliktavā. (Tā **Sūtījuma konsolidācijas politikas** laukam jābūt iestatītam uz *Pasūtījuma kopa* .)
1. Darbību rūts cilnē **Sūtījumi** atlasiet **Sūtījumi \> Konsolidēt sūtījumus**.
1. Pārbaudiet konsolidācijai ieteiktos sūtījumus. Konsolidācijai jāierosina tikai viens sūtījums, kam ir tāda pati politika.
1. Aizveriet lapu **Sūtījuma konsolidācija**.
1. Meklējiet un atlasiet sūtījumu, kas tika izveidots, kad pārdošanas pasūtījums 3 tika nodots noliktavā. (Tā **Sūtījuma konsolidācijas politikas** laukam jābūt iestatītam uz *Noklusējums* .)
1. Darbību rūts cilnē **Sūtījumi** atlasiet **Sūtījumi \> Konsolidēt sūtījumus**.
1. Pārbaudiet, lai neviens sūtījums netiek ieteikts konsolidācijai.
1. Atlasiet **Rādīt filtrus**.
1. Rūtī **Filtri** noņemiet **Pasūtījuma numura** filtru un pēc tam atlasiet **Lietot**.
1. Pārbaudiet konsolidācijai ieteiktos sūtījumus. Konsolidācijai jāierosina tikai viens sūtījums, kam ir tāda pati politika.

## <a name="additional-resources"></a>Papildu resursi

- [Kravu konsolidācijas politikas pārskats](about-shipment-consolidation-policies.md)
- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]