---
title: Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu
description: Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā automatizētajā, periodiskajā izdošanas-nodošanas procedūrā.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: dba864cd11ab9ae7a4ca4c2e2094cbdd066d9ba9a42ddd7d53eebf72955ec191
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716448"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu

[!include [banner](../includes/banner.md)]

Šī tēma iepazīstina ar scenāriju, kurā vairāki pasūtījumi tiek nodoti noliktavā tajā pašā automatizētajā, periodiskajā izdošanas-nodošanas procedūrā. Pasūtījumi automātiski tiks konsolidēti sūtījumos, pamatojoties uz noteikumiem, kas definēti kā piegādes konsolidācijas politikas.

Scenārija laikā jūs izveidosiet pārdošanas pasūtījumu kopas un izlaidīsiet katru kopu noliktavā. Pēc tam jūs pārskatīsiet sūtījumus, kas izveidoti vai atjaunināti sūtījuma konsolidācijas laikā, pamatojoties uz konfigurētajām politikām.

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

#### <a name="sales-order-1-2"></a>Pārdošanas pasūtījums 1-2

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Piegādes veids:** *Airwa-Air*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

#### <a name="sales-order-1-3"></a>Pārdošanas pasūtījums 1-3

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Piegādes veids:** *10*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

1. Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0002* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*
    - **Piegādes veids:** *Airwa-Air*

### <a name="create-order-set-2"></a>Izveidot 2. pasūtījuma kopu

#### <a name="sales-orders-2-1-and-2-2"></a>Pārdošanas pasūtījumi 2-1 un 2-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-002*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)
    - **Daudzums:** *1.00*

1. Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)
    - **Daudzums:** *1.00*
    - **Piegādes veids:** *Airwa-Air*

### <a name="create-order-set-3"></a>Izveidot 3. pasūtījuma kopu

#### <a name="sales-order-3-1"></a>Pārdošanas pasūtījums 3-1

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-002*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9200* (krājums, kur **kods 4** filtrs ir iestatīts uz *Viegli uzliesmojošs*)
    - **Daudzums:** *1.00*

1. Pievienojiet otru pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *M9201* (krājums, kur **kods 4** filtrs ir iestatīts uz *Sprādzienbīstams*)
    - **Daudzums:** *1.00*
    - **Piegādes veids:** *Airwa-Air*

> [!NOTE]
> Šis pasūtījums ir identisks diviem pasūtījumiem, kurus izveidojāt 2. pasūtījuma kopai. Tomēr tas ir norādīts kā atsevišķa pasūtījumu kopa, jo vēlāk šajā scenārijā jūs to atbrīvosit atsevišķi.

### <a name="create-order-set-4"></a>Izveidot 4. pasūtījuma kopu

#### <a name="sales-order-4-1"></a>Pārdošanas pasūtījums 4-1

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Debitora pieprasījums:** *1*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

### <a name="create-order-set-5"></a>Izveidot 5. pasūtījuma kopu

#### <a name="sales-orders-5-1-and-5-2"></a>Pārdošanas pasūtījumi 5-1 un 5-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-001*
    - **Debitora pieprasījums:** *2*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

#### <a name="sales-order-5-3"></a>Pārdošanas pasūtījums 5-3

1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Debitora pieprasījums:** *1*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

### <a name="create-order-set-6"></a>Izveidot 6. pasūtījuma kopu

#### <a name="sales-orders-6-1-and-6-2"></a>Pārdošanas pasūtījumi 6-1 un 6-2

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-003*
    - **Debitora pieprasījums:** *2*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Pārdošanas pasūtījumi 6-3 un 6-4

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-004*
    - **Debitora pieprasījums:** *1*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Pārdošanas pasūtījumi 6-5 un 6-6

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Vieta:** *6*
    - **Noliktava:** *61*
    - **Kopa:** *ShipCons*

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Pārdošanas pasūtījumi 6-7 un 6-8

1. Izveidojiet divus identiskus pārdošanas pasūtījumus, kam ir šādi iestatījumi:

    - **Debitora konts:** *US-007*
    - **Vieta:** *6*
    - **Noliktava:** *61*
    - **Kopa:** atstājiet šo lauku tukšu.

1. Pievienojiet pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *A0001* (krājums, kam nav piešķirts **kods 4** filtrs)
    - **Daudzums:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automātiska pārdošanas pasūtījumu pārvietošana uz noliktavu

Katrai iepriekš izveidoto pārdošanas pasūtījumu kopai jūs veiksit automātiskas izlaišanas procedūru noliktavā. Katrā gadījumā jums būs jāstrādā, izmantojot [pamata nodošana uz noliktavu procedūru](#release-procedure), kas tiek sniegta šeit.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Pamata nodošana uz noliktavu procedūra

Katrai iepriekš izveidotajai pārdošanas pasūtījumu kopai tiks izpildītas trīs procedūras, kas norādītas šādās apakšsadaļās.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Atjaunināt kopuma veidni, kas tiks izmantota izlaišanas laikā

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
1. Iestatiet lauku **Kopuma veidnes veids** uz *Sūtīšana*.
1. Meklējiet un atlasiet kopuma veidni, kas ir saistīta ar noliktavu, ko izmantojāt pasūtījuma kopās, ko izveidojāt šim scenārijam. Piemēram, ja izmantojāt noliktavu *24*, atlasiet **24 nosūtīšanas noklusējuma** kopuma veidni. Ja izmantojāt noliktavu *61*, atlasiet **61 nosūtīšanas noklusējuma** kopuma veidni.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz *Nē*.

#### <a name="release-to-the-warehouse"></a>Nodot izpildei noliktavā

1. Doties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Automātiska pārdošanas pasūtījumu nodošana**.
1. Iestatiet lauku **Nododamais daudzums** uz *Visi*.
1. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu vaicājuma dialoglodziņu.
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:

    - **Tabula:** *Pārdošanas pasūtījums*
    - **Atveidotā tabula:** *Pārdošanas pasūtījums*
    - **Lauks:** *Pārdošanas pasūtījums*
    - **Kritēriji:** Ievadiet ar komatu atdalītu pārdošanas pasūtījumu numuru sarakstu no vēlamā pasūtījuma komplekta.

1. Atlasiet **Labi**, lai saglabātu vaicājumu.
1. Atlasiet **Labi**, lai sāktu procedūru *Automātiski pārvietot uz noliktavu*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Pārskatiet izveidoto vai atjaunināto sūtījumu

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atrast un atlasīt nepieciešamo sūtījumu.
1. Ja sūtījuma izveides vai atjaunināšanas laikā tika izmantota konsolidācijas politika, jums to vajadzētu ieraudzīt laukā **Sūtījuma konsolidācijas politika**.

### <a name="release-sales-orders-from-order-set-1"></a>Izlaist pārdošanas pasūtījumus no 1. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 1. pasūtījumu kopas.

Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti divi sūtījumi:

- Pirmajā sūtījumā ir trīs rindas, un tās tika izveidotas, izmantojot *CustomerMode* sūtījumu konsolidācijas politiku.
- Otrais sūtījums, kas neizmanto *Gaisa* pārvadājumu transportēšanas veidu, tika izveidots, izmantojot *CustomerOrderNo* sūtījumu konsolidācijas politiku.

### <a name="release-sales-orders-from-order-set-2"></a>Izlaist pārdošanas pasūtījumus no 2. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 2. pasūtījumu kopas.

Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti trīs sūtījumi:

- Pirmajā sūtījumā ir *Viegli uzliesmojoši* krājumi.
- Abi pārējie sūtījumi satur vienu rindu, kurā ir *Sprādzienbīstams* krājums.

### <a name="release-sales-orders-from-order-set-3"></a>Izlaist pārdošanas pasūtījumus no 3. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 3. pasūtījumu kopas.

Kad esat pabeidzis, jums vajadzētu redzēt, ka ir notikušas šādas darbības:

- Tika atjaunināts viens esošais sūtījums (sūtījums, kas tika izveidots, kad tika nodota 2. pasūtījuma kopa). Tika pievienota rinda ar viegli *Uzliesmojošu* krājumu.
- Tika izveidots viens jauns sūtījums, kas satur *sprādzienbīstamu* krājumu.

### <a name="release-sales-orders-from-order-set-4"></a>Izlaist pārdošanas pasūtījumus no 4. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 4. pasūtījumu kopas.

Kad esat pabeidzis, jums būtu jāredz, ka ir atjaunināts viens esošais sūtījums (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*). Tai tika pievienota viena jauna rinda.

### <a name="release-sales-orders-from-order-set-5"></a>Izlaist pārdošanas pasūtījumus no 5. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 5. pasūtījumu kopas.

Kad esat pabeidzis, jums vajadzētu redzēt, ka ir notikušas šādas darbības:

- Tika atjaunināts viens esošais sūtījums (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*). Tai tika pievienota rinda no pārdošanas pasūtījuma 5-3 (kur **Debitora pieprasījuma** lauks ir iestatīts uz *1*).
- Tika izveidots viens jauns sūtījums, kur pārdošanas pasūtījumu 5-1 un 5-2 rindas tiek grupētas vienā sūtījumā.

### <a name="release-sales-orders-from-order-set-6"></a>Izlaist pārdošanas pasūtījumus no 6. pasūtījumu kopas

Sekojiet [pamata nodošanas uz noliktavu procedūrai](#release-procedure), lai nodotu pārdošanas pasūtījumus no 6. pasūtījumu kopas.

Kad esat pabeidzis, jums būtu jāredz, ka ir izveidoti četri sūtījumi:

- Rindas no diviem pasūtījumiem debitoram *US-003* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no diviem pasūtījumiem debitoram *US-004* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 6-5 un 6-6 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Pasūtījumu kopas* sūtījuma konsolidācijas politiku.
- Rindas no pārdošanas pasūtījumiem 6-7 un 6-8 debitoru *US-007* tika grupētas vienā sūtījumā, izmantojot *Savstarpēja pasūtījuma* sūtījuma konsolidācijas politiku.

## <a name="additional-resources"></a>Papildu resursi

- [Sūtījumu konsolidācijas politikas](about-shipment-consolidation-policies.md)
- [Sūtījumu konsolidācijas politiku konfigurēšana](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]