---
title: Konsolidēt sūtījumus, kravu plānošanas rīkā, pārvietojot tos uz noliktavu
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā noslodzē un pēc tam tiek automātiski apvienoti sūtījumos.
author: GarmMSFT
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
ms.openlocfilehash: b724b3f040a1b277d99dd067525dfda2b47ca73b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577892"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a>Konsolidēt sūtījumus, kravu plānošanas rīkā, pārvietojot tos uz noliktavu

[!include [banner](../includes/banner.md)]

Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā noslodzē un pēc tam tiek automātiski apvienoti sūtījumos.

## <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Iestatīt sūtījumu konsolidācijas politikas un preču filtrus

Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus. Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.

## <a name="create-the-sales-orders-for-this-scenario"></a>Izveidot pārdošanas pasūtījumus šim scenārijam

Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt. Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem. Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.

Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.

### <a name="create-order-set-1"></a>Izveidot 1. pasūtījuma kopu

#### <a name="sales-order-1-1"></a>Pārdošanas pasūtījums 1-1

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Piegādes veids:** *Airwa-Air*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-order-1-2"></a>Pārdošanas pasūtījums 1-2

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Piegādes veids:** *Airwa-Air*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-order-1-3"></a>Pārdošanas pasūtījums 1-3

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Piegādes veids:** *10*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.
1. Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*
    - **Piegādes veids:** *Airwa-Air*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.

### <a name="create-order-set-2"></a>Izveidot 2. pasūtījuma kopu

#### <a name="sales-orders-2-1-and-2-2"></a>Pārdošanas pasūtījumi 2-1 un 2-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-002*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.
1. Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)
    - **Daudzums:** *1.00*
    - **Piegādes veids:** *Airwa-Air*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu otro pasūtījuma rindu.

### <a name="create-order-set-3"></a>Izveidot 3. pasūtījuma kopu

#### <a name="sales-orders-3-1-and-3-2"></a>Pārdošanas pasūtījumi 3-1 un 3-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-001*
    - **Debitora pieprasījums:** *1*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-orders-3-3-and-3-4"></a>Pārdošanas pasūtījumi 3-3 un 3-4

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-001*
    - **Debitora pieprasījums:** *2*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

### <a name="create-order-set-4"></a>Izveidot 4. pasūtījuma kopu

#### <a name="sales-orders-4-1-and-4-2"></a>Pārdošanas pasūtījumi 4-1 un 4-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-003*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-orders-4-3-and-4-4"></a>Pārdošanas pasūtījumi 4-3 un 4-4

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-004*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-orders-4-5-and-4-6"></a>Pārdošanas pasūtījumi 4-5 un 4-6

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Vieta:** *6*
    - **Noliktava:** *61*
    - **Kopa:** *ShipCons*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

#### <a name="sales-orders-4-7-and-4-8"></a>Pārdošanas pasūtījumi 4-7 un 4-8

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Vieta:** *6*
    - **Noliktava:** *61*
    - **Kopa:** atstājiet šo lauku tukšu.

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Atlasiet **Krājums \> Rezervācija** un pēc tam darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu pasūtījuma rindu.

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Izmantojiet noslodzes plānošanas darbvietu, lai izveidotu noslodzes un nodotu tās noliktavā

Sekojiet šiem soļiem, lai izveidotu noslodzi katrai pasūtījuma kopai, ko izveidojāt šim scenārijam, un tad to nodotu noliktavai.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Cilnē **Pārdošanas rindas** meklējiet un atlasiet visas pārdošanas pasūtījuma rindas vienā no šim scenārijam izveidotajām pasūtījumu kopām.
1. Darbības rūtī cilnē **Piedāvājums un pieprasījums** atlasiet **Pievienot \> Jaunajai noslodzei**, lai pievienotu atlasītās pasūtījuma rindas jaunai noslodzei.
1. Dialoglodziņā **Noslodzes veidnes piešķire** laukā **Noslodzes veidnes ID** atlasiet noslodzes veidni, piemēram, *Stnd noslodzes veidne*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu. 
1. Sadaļā **Noslodzes** meklējiet un atlasiet tikko izveidoto noslodzi.
1. Atlasiet opciju **Pārvietot \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto noslodzi uz noliktavu.
1. Atkārtojiet šo procedūru pārējām trim pasūtījumu kopām, ko izveidojāt šim scenārijam.

## <a name="verify-the-shipments"></a>Pārbaudīt sūtījumus

Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju. Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atrast un atlasīt nepieciešamo sūtījumu.
1. Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.

### <a name="release-order-set-1-in-one-load"></a>Nodot 1. pasūtījuma kopu vienā noslodzē

Ir jābūt izveidotiem diviem sūtījumiem:

- Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.
- Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.

### <a name="release-order-set-2-in-one-load"></a>Nodot 2. pasūtījuma kopu vienā noslodzē

Ir jābūt izveidotiem trīs sūtījumiem:

- Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.
- Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.

### <a name="release-order-set-3-in-one-load"></a>Nodot pasūtījuma kopu 3 vienā noslodzē

Ir jābūt izveidotiem diviem sūtījumiem:

- Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.
- Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.

### <a name="release-order-set-4-in-one-load"></a>Nodot 4. pasūtījuma kopu vienā noslodzē

Ir jābūt izveidotiem četriem sūtījumiem:

- Rindas no diviem pasūtījumiem debitoru kontam *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no diviem pasūtījumiem debitoru kontam *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru kontam *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.

## <a name="additional-resources"></a>Papildu resursi

- [Sūtījumu konsolidācijas politikas](about-shipment-consolidation-policies.md)
- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]