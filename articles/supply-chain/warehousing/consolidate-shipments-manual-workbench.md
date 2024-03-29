---
title: Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku
description: Šajā rakstā ir scenārijs, kurā vairāki pasūtījumi ir izlaisti nosūtīšanai uz noliktavu un pēc tam konsolidēti kravās vēlāk, izmantojot piegādes konsolidācijas pakalpojumu.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: eed484cd37b02e58831e0041c3e0625091283b65
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428122"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku

[!include [banner](../includes/banner.md)]

Šajā rakstā ir scenārijs, kurā vairāki pasūtījumi ir izlaisti nosūtīšanai uz noliktavu un pēc tam konsolidēti kravās vēlāk, izmantojot piegādes konsolidācijas pakalpojumu.

## <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šī raksta scenārijā ir atsauces uz vērtībām un ierakstiem, kas iekļauti standarta demonstrācijas datos, kas tiek nodrošināti korporācijai Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Iestatīt sūtījumu konsolidācijas politikas un preču filtrus

Šeit aprakstītajā scenārijā tiek pieņemts, ka esat jau ieslēdzis līdzekli, paveicis vingrinājumus, lai [Konfigurētu sūtījumu konsolidācijas politikas](configure-shipment-consolidation-policies.md) un izveidotu politikas un citus tur aprakstītos ierakstus. Pirms turpināt šo scenāriju, noteikti veiciet šos vingrinājumus.

## <a name="turn-the-manual-shipment-consolidation-feature-on-or-off"></a>Ieslēgt vai izslēgt manuālas piegādes konsolidācijas līdzekli

Lai izmantotu manuālu piegādes konsolidāciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot manuālas piegādes *konsolidācijas* līdzekli līdzekļu pārvaldības [darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lai izveidotu politikas *(no Piegādes* ķēdes pārvaldības versijas 10.0.29), jums ir arī jāslēdz piegādes konsolidācijas funkcija, un to nevar izslēgt. Papildinformāciju skatiet kravas konsolidācijas [politiku konfigurēšana](configure-shipment-consolidation-policies.md).

## <a name="create-the-sales-orders-for-this-scenario"></a>Izveidot pārdošanas pasūtījumus šim scenārijam

Sāciet ar pārdošanas pasūtījumu kolekcijas izveidošanu, ar kuru varat strādāt. Jums ir jāstrādā ar noliktavu, kas ir aktivizēta papildu noliktavas (WMS) procesiem. Ja nav skaidri minēta cita noliktava, tai pašai noliktavai ir jābūt izmantotai katrai no šīm pasūtījumu kopām.

Dodieties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi** un izveidojiet pārdošanas pasūtījumu kolekciju, kam ir iestatījumi, kas aprakstīti šādās apakšsadaļās.

### <a name="create-order-set-1"></a>Izveidot 1. pasūtījuma kopu

#### <a name="sales-orders-1-1-and-1-2"></a>Pārdošanas pasūtījumi 1-1 un 1-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

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
    - **Piegādes veids:** *Airwa-Air*

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

## <a name="release-the-orders-to-the-warehouse"></a>Pasūtījumu izlaišana noliktavā

Sekojiet šiem soļiem, lai izlaistu pārdošanas pasūtījumu, ko izveidojāt šim scenārijam noliktavā.

1. Doties uz **Debitoru parādi \> Pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atrodiet un atlasiet izlaižamo pārdošanas pasūtījumu.
1. Darbību rūtī cilnē **Noliktava**, atlasiet **Darbības \> Pārvietot uz noliktavu**, lai pārvietotu atlasīto pārdošanas pasūtījumu.
1. Atkārtojiet šo procedūru katram otrajam pārdošanas pasūtījumam, ko izveidojāt šim scenārijam.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku

1. Dodieties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Sūtījumu konsolidācijas rīks**.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:

    - **Tabula:** *Pārdošanas pasūtījumi*
    - **Lauks:** *Pārdošanas pasūtījums*
    - **Kritēriji:** ievadiet ar komatu atdalītu pārdošanas pasūtījumu numuru sarakstu katrai pasūtījumu kopai, ko izveidojāt šim scenārijam.

1. Atlasiet **Labi**, lai saglabātu jūsu vaicājumu un aizvērtu dialoglodziņu.
1. Darbību rūtī atlasiet **Konsolidēt sūtījumus**.
1. Atlasiet visus sūtījumus un pēc tam Darbību rūtī atlasiet **Konsolidēt**.

## <a name="verify-the-shipments"></a>Pārbaudīt sūtījumus

Šī procedūra ļauj pārbaudīt sūtījumus, kas ir izveidoti vai atjaunināti, veicot sūtījuma konsolidāciju. Izmantojiet to, lai pārskatītu katru pasūtījuma kopu, ko izveidojāt šim scenārijam, un tad pārskatītu sekojošās apakšsadaļas, lai pārliecinātos, ka esat ieguvis plānotos rezultātus.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atrast un atlasīt nepieciešamo sūtījumu.
1. Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.

### <a name="related-shipments-for-order-set-1"></a>1. pasūtījumu kopas saistītie sūtījumi

Ir jābūt izveidotiem diviem sūtījumiem:

- Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.
- Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.

### <a name="related-shipments-for-order-set-2"></a>2. pasūtījumu kopas saistītie sūtījumi

Ir jābūt izveidotiem trīs sūtījumiem:

- Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.
- Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.

### <a name="related-shipments-for-order-set-3"></a>3. pasūtījumu kopas saistītie sūtījumi

Ir jābūt izveidotiem diviem sūtījumiem:

- Pirmajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*.
- Otrajā sūtījumā ir pasūtījuma rindas no pārdošanas pasūtījuma, kur **Debitora pieprasījuma** lauks ir iestatīts uz *2*.

### <a name="related-shipments-for-order-set-4"></a>4. pasūtījumu kopas saistītie sūtījumi

Ir jābūt izveidotiem četriem sūtījumiem:

- Rindas no diviem pasūtījumiem debitoram *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no diviem pasūtījumiem debitoram *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 4-5 un 4-6 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 4-7 un 4-8 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.

## <a name="additional-resources"></a>Papildu resursi

- [Kravu konsolidācijas politikas pārskats](about-shipment-consolidation-policies.md)
- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]