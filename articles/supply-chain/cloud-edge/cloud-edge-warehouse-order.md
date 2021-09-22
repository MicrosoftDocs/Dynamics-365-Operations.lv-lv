---
title: Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par noliktavas pasūtījuma iespēju, kas tiek izmantota kā daļa no noliktavas mēroga vienības darba noslodzes.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bd3c72f2c008b936ceda53a3fcdde79df1e6b1b7
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471696"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ne visas biznesa funkcionalitātes tiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas. Izmantojot malas mēroga mērvienības, noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītus.

## <a name="what-are-warehouse-orders"></a>Kas ir noliktavas pasūtījumi?

*Noliktavas pasūtījumi* ir pasūtījumi, kurus izmanto, lai sekmētu centrmezgla un mēroga vienības noliktavas izvietošanu. Ar tiem var saņemt un sūtīt krājumu, kad esat palaiduši noliktavas darba slodzi mēroga vienībā.

Noliktavas pasūtījumi tiek izmantoti kā daļa gan no ienākošās, gan izejošās noliktavu pārvaldības apstrādes. Tie tiek izveidoti kā daļa no *Izlaišanas uz noliktavu* procesa, kas tiek inicializēts centrmezglā.
Ienākošajai apstrādei tiek izmantota noliktavas mobilā lietojumprogramma, lai reģistrētu fizisko rīcībā esošo krājumu ienākošo pasūtījumu apstrādes laikā; tas ir pieejams pirkuma un ražošanas pasūtījumiem, kuri konkretizē mēroga vienības noliktavu un elementus, kuri ir iespējoti, lai lietotu noliktavas pārvaldības procesus.
Izejošie noliktavas pasūtījumi tiek lietoti kā daļa no sūtījuma kopuma procesa pārsūtīšanas un pārdošanas pasūtījumiem.

> [!IMPORTANT]
> Noliktavas pasūtījumi ir pieejami tikai izvietošanās, kas izmanto noliktavas [pārvaldības darba noslodzes mākoņa un malas mēroga vienībām](cloud-edge-workload-warehousing.md).

## <a name="create-an-inbound-warehouse-order"></a>Ienākošā noliktavas pasūtījuma izveidne

Lai izveidotu pirkuma pasūtījuma apstrādes ienākošo noliktavas pasūtījumu, izpildiet tālāk norādītās darbības.

1. Piesakieties Microsoft Dynamics 365 Supply Chain Management instancei, kas ir palaista centrmezglā. (Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā.)
1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.
1. Lai skatītu saistītās noliktavas pasūtījuma rindas, atveriet atbilstošo pirkšanas pasūtījumu, atlasiet rindu sadaļā **Pirkšanas pasūtījuma rindas** un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas pasūtījuma rindas**. Lai skatītu visas rindas, dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.

Jūs variet arī izraisīt *Palaišanas uz noliktavu* procesu no pakešuzdevuma, ejot uz **Noliktavas pārvaldība > Nodot uz noliktavu > Automātiska pirkšanas pasūtījumu izlaišana**. Iestatot pakešuzdevumu, var atlasīt specifiskas pirkšanas pasūtījuma rindas, pamatojoties uz vaicājumu. Tipisks scenārijs būtu iestatīt periodisku pakešuzdevumu, kas atbrīvo visas apstiprinātās pirkšanas pasūtījuma rindas, kam paredzēts saņemt nākamo dienu.

## <a name="cancel-a-warehouse-order"></a>Atgriešanas pasūtījuma atcelšana

Kā daļa no *Pārsūtīšanas uz noliktavu* procesa, pirkšanas pasūtījuma krājumu darbības ir saistītas ar noliktavas pasūtījumiem un bloķētas no atjaunināšanas ar pārkraušanas vietu. Ja kļūdainā gadījumā izlaista noliktavai, vai arī ja ir kāds cits iemesls atsaukt noliktavas pasūtījuma rindu izveidošanu, varat pieprasīt atcelt noliktavas pasūtījuma rindas.

Lai atceltu pārdošanas pasūtījumu, veiciet šādas darbības.

1. Piesakieties Supply Chain Management instancei, kas ir palaista centrmezglā.
1. Dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.
1. Atlasiet saistīto rindu.
1. Darbību rūtī atlasiet **Atcelt noliktavas pasūtījuma rindas**.

> [!NOTE]
> Pieprasījums atcelt rindas tiks noraidīts visām rindām, kas jau gaida atcelšanu vai kas aktīvi tiek apstrādātas noliktavā, kas palaiž tās darba slodzi mēroga vienībā.

## <a name="monitor-a-warehouse-order"></a>Noliktavas pasūtījuma uzraudzīšana

**Noliktavas pasūtījuma rindu** skatā varat pārraudzīt ienākošās saņemšanas progresu, pārskatot kolonnas **Saņemamais daudzums** vērtības. Lai skatītu detaļas, kas saistītas ar darbu, kas paveikts, izmantojot Warehouse Management mobile programmu, veiciet vienu no šīm darbībām.

- Pārejiet uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas** un izmantojiet filtru, lai atrastu meklētās rindas.
- Dodieties uz **Sagāde un avoti \> Pirkšanas pieprasījumi \> Visi pirkšanas pieprasījumi**, un atveriet attiecīgo pirkšanas pasūtījumu. Sadaļā **Pirkšanas pasūtījuma rindas** atlasiet vienu vai vairākas rindas un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas ieejas plūsmas ieraksti**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
