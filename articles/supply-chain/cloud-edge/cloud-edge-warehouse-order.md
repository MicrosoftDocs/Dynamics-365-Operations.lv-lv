---
title: Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par noliktavas pasūtījuma iespēju, kas tiek izmantota kā daļa no noliktavas mēroga vienības darba noslodzes.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105718"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne visas biznesa funkcionalitātes tiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas. Izmantojot malas mēroga mērvienības, noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītus.

## <a name="what-are-warehouse-orders"></a>Kas ir noliktavas pasūtījumi?

*Noliktavas pasūtījumi* ir pasūtījuma veids, kas tika izveidots, lai atbalstītu pārkraušanas centra un mēroga vienību noliktavas izvietošanu. Tie ļauj saņemt krājumus, veicot noliktavas darba noslodzi mēroga vienībā. Ties pašlaik tiek lietoti tikai pirkšanas pasūtījumos.

Noliktavas pasūtījumi tiek izmantoti kā daļa no noliktavas pārvaldības apstrādes, piemēram, kad noliktavas programma tiek izmantota, lai reģistrētu fiziskos rīcībā esošos krājumus ienākošā pirkšanas pasūtījuma apstrādes laikā. Noliktavas pasūtījumi tiek izveidoti kā daļa no *Pārsūtīšanas uz noliktavu* procesa, kas ir pieejams pirkšanas pasūtījumiem, kuros norādīta mēroga vienības noliktava un krājumi, kas ir iespējoti noliktavas pārvaldības procesu izmantošanai.

> [!IMPORTANT]
> Noliktavas pasūtījumi ir pieejami tikai izvietošanās, kas izmanto noliktavas [pārvaldības darba noslodzes mākoņa un malas mēroga vienībām](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Pirkšanas pasūtījuma izveide

Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.

1. Piesakieties Microsoft Dynamics 365 Supply Chain Management instancei, kas ir palaista centrmezglā. (Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā.)
1. Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.
1. Lai skatītu saistītās noliktavas pasūtījuma rindas, atveriet atbilstošo pirkšanas pasūtījumu, atlasiet rindu sadaļā **Pirkšanas pasūtījuma rindas** un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas pasūtījuma rindas**. Lai skatītu visas rindas, dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.

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

**Noliktavas pasūtījuma rindu** skatā varat pārraudzīt ienākošās saņemšanas progresu, pārskatot kolonnas **Saņemamais daudzums** vērtības. Lai skatītu detaļas, kas saistītas ar darbu, kas paveikts, izmantojot noliktavas programmu, veiciet vienu no šīm darbībām.

- Pārejiet uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas** un izmantojiet filtru, lai atrastu meklētās rindas.
- Dodieties uz **Sagāde un avoti \> Pirkšanas pieprasījumi \> Visi pirkšanas pieprasījumi**, un atveriet attiecīgo pirkšanas pasūtījumu. Sadaļā **Pirkšanas pasūtījuma rindas** atlasiet vienu vai vairākas rindas un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas ieejas plūsmas ieraksti**.
