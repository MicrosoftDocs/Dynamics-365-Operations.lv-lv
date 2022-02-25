---
title: Krājumu statusi
description: Šajā rakstā ir aprakstīts, kā varat izmantot krājumu statusus, lai krājumus sadalītu kategorijās un sekotu tiem līdzi.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103467"
---
# <a name="inventory-statuses"></a>Krājumu statusi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā varat izmantot krājumu statusus, lai krājumus sadalītu kategorijās un sekotu tiem līdzi.

## <a name="set-up-and-use-inventory-statuses"></a>Iestatiet un lietojiet krājumu statusus

Krājumu statusus var izmantot, lai kategorizētu krājumu. Pēc tam varat sākt atbilstošas darbības, piemēram, papildināšanas vai izvietošanas darbu.

Tālāk ir minēti daži piemēri, kā izmantot krājumu statusus.

- Izveidojiet krājumu statusus rīcībā esošajiem krājumiem un ienākošajām un izejošajām transakcijām.
- Norādiet noklusējuma krājuma statusu noliktavas transakcijām.
- Mainīt preču krājumu statusu pirms ierašanās, ierašanās laikā, vai tad, kad preces ir izvietotas krājumu kustības laikā.
- Izmantojiet krājumu statusu to vienību cenas noteikšanai, kas tiek atgrieztas, un plānojiet preču segšanu vispārējās plānošanas laikā.

Krājumu statuss ir viena no dimensijām noliktavas dimensiju grupā. Krājumu statusus var klasificēt kā pieejamus vai nepieejamus, un var izmantot parametru **Krājuma bloķēšana**, lai bloķētu vienības, kam krājuma statuss ir Nav pieejams. Vienības ar statusu Bloķēts tiek uzskatītas par fiziskiem krājumiem un tās nevar izmantot ražošanas pasūtījumā, pārdošanas pasūtījumā, pārsūtīšanas pasūtījumā vai izejošā transakcijā.

Ienākošam darbam varat izmantot noliktavas vienības ar statusu Pieejams vai Nav pieejams. Piemēram, izveidojiet pieejamības statusu ar nosaukumu *Gatavs*, nepieejamības statusu ar nosaukumu *Bojāts* un bloķēšanas statusu ar nosaukumu *Bloķēts*. Veidojot pirkšanas pasūtījumu saņemtām vai atgrieztām vienībām, ja kāda no vienībām ir bojāta vai sadalīta, pirkšanas pasūtījuma rindā varat mainīt šo vienību krājuma statusu uz *Bojāts*. Kad šīs vienības ir saņemtas, automātiski tiek iestatīts statuss *Bloķēts*. Ja skenējat bojātos vienumus, izmantojot mobilo ierīci, programma Supply Chain Management var izmantot vietas direktīvas un darba veidnes, lai rādītu informāciju par atbilstošo vietu vai vietu diapazonu, kur varat novietot šos vienumus. Atgrieztajām vienībām lapā *Krājumu darbības* tiek izveidots izsniegšanas veids **Rezervācija**.

Varat norādīt, kuri krājumu statusi ir aizturēšanas statusi, izmantojot parametru **Krājuma bloķēšana** lapā **Krājumu statusi**. Krājumu statusus nevar izmantot kā ražošanas pasūtījumu, pārdošanas pasūtījumu, pārsūtīšanas pasūtījumu vai projekta integrācijas aizturēšanas statusus.

Izejošam darbam jūs varat izmantot dažādus nebloķējošos krājumu statusus, lai kontrolētu, ar kuriem krājumiem veikt rezervēšanu. Ja ir vienības ar statusu *Bloķēts*, un šīm vienībām tiek palaista vispārējā plānošana, tās tiek uzskatītas par trūkstošām, un krājums tiek automātiski papildināts. Turklāt ar izejošo darbu saistīto kvalitātes pasūtījumu statusu nav iespējams atjaunināt **Krājuma statusu** kā daļu no kvalitātes pasūtījuma validācijas.

> [!NOTE]
> To vietu krājumu statusu, kuros pastāv atvērts darbs, nevar mainīt. Piemēram, ja pirkāt krājuma saņemšanu, bet nepaveicāt izvietošanas soli, saņemšanas vietai būtu atvērts darbs, un, mēģinot mainīt krājumu statusu šajā vietā, rodas kļūda. Saistītā darba pabeigšana vai atcelšana ļautu mainīt statusu.
>
> Parasti rīcībā esošo krājumu statusu, kas saistīts ar atvērto noliktavas darbu, maina tikai darbinieki, kuri izmanto mobilo programmu Noliktavas pārvaldība, piemēram, veicot kustības procesu.

Kad krājumu statusi ir iestatīti, varat iestatīt noklusējuma krājumu statusu vietai, vienībai un noliktavai. Varat arī iestatīt noklusējuma statusu pārdošanas, pārsūtīšanas un pirkšanas pasūtījumiem. Noklusējuma pārdošanas pasūtījumu un izejošo pārsūtīšanas pasūtījumu statusam opcija **Krājuma bloķēšana** nevar būt iestatīta uz *Jā*. Krājuma statusu, kas tiek mantots no vietas, noliktavas, vienības, pirkšanas pasūtījuma, pārsūtīšanas pasūtījuma vai pārdošanas pasūtījuma noklusējuma iestatījumiem, var mainīt, izmantojot mobilo ierīci, pirkšanas un pārdošanas pasūtījumu vai pārsūtīšanas pasūtījuma rindu.

Lai plānotu to vienību segumu, kam krājuma statuss ir Pieejams, lapā **Noliktavas dimensiju grupas** noliktavas dimensijai atlasiet opciju **Vajadzības plāns pa dimensijām**. Atverot vedni **Vienības vajadzības**, vienības, kurām statuss ir Pieejams, tiks parādītas lapā **Statuss**. Lai izveidotu šo preču segšanas iestatījumus, atlasiet krājumu statusa ID pieejamo krājumu statusiem. Pamatojoties uz segšanas iestatījumiem, varat aprēķināt preču vajadzības un prognozēt pieejamo preču piegādi un piedāvājumu vispārējās plānošanas laikā. Vienības vajadzības iestatījumus nevar izveidot, ja krājuma statuss ir Bloķēts. Tā vietā izmantojiet lapu **Vienības vajadzības**, lai izveidotu vai modificētu vienības vajadzības parametrus.

## <a name="change-inventory-statuses"></a>Mainīt krājuma statusus

Varat mainīt krājumu statusus, izmantojot lapu **Rīcībā esošs pēc novietojuma** vai izmantojot *Krājumu statusa izmaiņu* periodisko uzdevumu.

- Lietojot *Krājumu statusa izmaiņu* periodisko uzdevumu, varat atlasīt, kurus ierakstus iekļaut un iestatīt uzdevumu, kas jāpalaiž partijā vēlamajā intervālā.
- Lai mainītu krājumu statusu kā speciālu procesu, atveriet lapu **Rīcībā esošs pēc novietojuma**, izvēlieties atbilstošos ierakstus un pēc tam atlasiet pogu **Krājumu statusa maiņa**.

> [!NOTE]
> *Mainīt krājumu statusu vienumiem, kurus kontrolē izsekošanas dimensijas* funkcija ļauj jums mainīt krājumu statusu vienumiem, kas ir kontrolēti ar izsekošanas dimensijām, ieskaitot spēju atjaunināt tikai atlasītos ierakstus. Tāpat kā Piegādes ķēdes pārvaldībai 10.0.25 šī funkcija ir obligāta un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.25, administratori šo funkcionalitāti var ieslēgt vai izslēgt, meklējot vienumu statusa izmaiņas, ko kontrolē *izsekošanas*[dimensiju](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) līdzeklis līdzekļu pārvaldības darbvietā. Ja šī funkcija ir iespējota, varat veikt šādas darbības:
>
> - Lapā **Rīcībā esošs pēc atrašanās vietas** varat grupēt rindas, pamatojoties uz parādītajām dimensijām, izmantojot pogu **Parādīt dimensijas** un mainīt atlasīto rindu statusu.
> - Lapā **Rīcībā esošs pēc atrašanās vietas** varat atlasīt vairākus ierakstus un tad izmantot pogu **Krājumu statusa maiņa**, lai tos visus uzreiz mainītu.
> - **Krājumu statusa maiņa** periodiskajā uzdevumā būs iespējams filtrēt pēc izsekošanas dimensijām.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
