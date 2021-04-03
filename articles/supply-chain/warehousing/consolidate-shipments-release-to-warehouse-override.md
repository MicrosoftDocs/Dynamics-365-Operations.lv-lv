---
title: Konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”
description: Šī tēma piedāvā scenāriju, kur viena vai vairākas pārdošanas rindas ir manuāli jāpārvieto uz noliktavu no lapas Pārvietot uz noliktavu, un sistēmas definētā sūtījumu konsolidācijas politika ir jāignorē pirms pārvietošanas.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: be573f3a137fbd74ba2f5d8bb346e4bb9f9116c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237111"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>Konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”

[!include [banner](../includes/banner.md)]

Šī tēma piedāvā scenāriju, kur viena vai vairākas pārdošanas rindas ir manuāli jāpārvieto uz noliktavu no lapas **Pārvietot uz noliktavu**, un sistēmas definētā sūtījumu konsolidācijas politika ir jāignorē pirms pārvietošanas. Sūtījuma konsolidācijas politikas ignorēšana var būt nepieciešama, ja, piemēram, pasūtījums, kas parasti netiek konsolidēts ar atvērtiem sūtījumiem, ir jākonsolidē ar atvērtiem sūtījumiem.

Scenārija laikā jūs izveidosiet pārdošanas pasūtījumu kopu un pēc tam ignorēsiet noklusējuma sūtījumu konsolidācijas politiku pirms pasūtījumu nodošanas noliktavā.

## <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Iestatīt sūtījumu konsolidācijas politikas un preču filtrus

Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus. Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.

## <a name="create-the-sales-orders-for-this-scenario"></a>Izveidot pārdošanas pasūtījumus šim scenārijam

1. Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet trīs identiskus pārdošanas pasūtījumus, kuriem ir šādi iestatījumi:

    - **Debitora konts:** *US-002*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Pārvietot pārdošanas pasūtījumus no lapas Pārvietot uz noliktavu

Sekojiet šiem soļiem, lai ignorētu sūtījuma konsolidācijas politiku izlaišanas noliktavā laikā.

1. Dodieties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Pārvietot uz noliktavu**.
1. Augšējā rūtī atlasiet pirmo pārdošanas pasūtījumu, ko izveidojāt šim scenārijam.
1. Atlasiet **Pievienot**, lai pievienotu rindu izlaišanai noliktavā. Ievērojiet, ka apakšējā rūtī tiek lietota *Noklusējuma* sūtījumu konsolidācijas politika.
1. Apakšējā rūtī atlasiet **Atlasīt jaunu sūtījumu konsolidācijas politiku**.
1. Atlasiet politiku, kas ļauj veikt konsolidāciju ar citiem tās pašas politikas atvērtajiem sūtījumiem. Piemēram, atlasiet *CustomerOrderNo* politiku.
1. Atlasiet **Pārvietot uz noliktavu**.
1. Atlasiet otro un trešo pārdošanas pasūtījumu, ko izveidojāt šim scenārijam.
1. Atlasiet **Pievienot**, lai pievienotu rindas izlaišanai noliktavā. Ievērojiet, ka apakšējā rūtī tiek lietota *Noklusējuma* politika.
1. Atlasiet otro rindu un pēc tam laukā **Atlasīt jaunu sūtījumu konsolidācijas politiku** atlasiet *CustomerOrderNo* politiku.
1. Atlasiet **Pārvietot uz noliktavu** abām rindām.

## <a name="verify-the-shipments"></a>Pārbaudīt sūtījumus

Ir jābūt izveidotiem diviem sūtījumiem:

- Pirmajā sūtījumā ir divas rindas, un tās tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.
- Otrajā sūtījumā ir viena rinda, un tā tika izveidota, izmantojot *Noklusējuma* sūtījumu konsolidācijas politiku.

Sekojiet šiem soļiem, lai pārskatītu izveidotos sūtījumus.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atrast un atlasīt nepieciešamo sūtījumu.
1. Laukā **Sūtījuma konsolidācijas politika** pārskatiet izveidoto konsolidācijas politiku, izveidojot sūtījumu.

## <a name="additional-resources"></a>Papildu resursi

- [Sūtījumu konsolidācijas politikas](about-shipment-consolidation-policies.md)
- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]