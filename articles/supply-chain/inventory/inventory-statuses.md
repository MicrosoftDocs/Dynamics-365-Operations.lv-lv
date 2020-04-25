---
title: Krājumu statusi
description: Šajā rakstā ir aprakstīts, kā varat izmantot krājumu statusus, lai krājumus sadalītu kategorijās un sekotu tiem līdzi.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96ed6d01e22ee2cbc5b3b2be8168fbb43904c89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212714"
---
# <a name="inventory-statuses"></a>Krājumu statusi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā varat izmantot krājumu statusus, lai krājumus sadalītu kategorijās un sekotu tiem līdzi.

Krājumu statusus var izmantot, lai kategorizētu krājumu. Pēc tam varat sākt atbilstošas darbības, piemēram, papildināšanas vai izvietošanas darbu.

Tālāk ir minēti daži piemēri, kā izmantot krājumu statusus.

-   Izveidojiet krājumu statusus rīcībā esošajiem krājumiem un ienākošajām un izejošajām transakcijām.
-   Norādiet noklusējuma krājuma statusu noliktavas transakcijām.
-   Mainīt preču krājumu statusu pirms ierašanās, ierašanās laikā, vai tad, kad preces ir izvietotas krājumu kustības laikā.
-   Izmantojiet krājumu statusu to vienību cenas noteikšanai, kas tiek atgrieztas, un plānojiet preču segšanu vispārējās plānošanas laikā.

Krājumu statuss ir viena no dimensijām noliktavas dimensiju grupā. Krājumu statusus var klasificēt kā pieejamus vai nepieejamus, un var izmantot parametru **Krājuma bloķēšana**, lai bloķētu vienības, kam krājuma statuss ir Nav pieejams. Vienības ar statusu Bloķēts tiek uzskatītas par fiziskiem krājumiem un tās nevar izmantot ražošanas pasūtījumā, pārdošanas pasūtījumā, pārsūtīšanas pasūtījumā vai izejošā transakcijā.

Ienākošam darbam varat izmantot noliktavas vienības ar statusu Pieejams vai Nav pieejams. Piemēram, izveidojiet pieejamības statusu ar nosaukumu **Gatavs**, nepieejamības statusu ar nosaukumu **Bojāts** un bloķēšanas statusu ar nosaukumu **Bloķēts**. Veidojot pirkšanas pasūtījumu saņemtām vai atgrieztām vienībām, ja kāda no vienībām ir bojāta vai sadalīta, pirkšanas pasūtījuma rindā varat mainīt šo vienību krājuma statusu uz **Bojāts**. Kad šīs vienības ir saņemtas, automātiski tiek iestatīts statuss **Bloķēts**. Ja skenējat bojātos vienumus, izmantojot mobilo ierīci, programma Supply Chain Management var izmantot vietas direktīvas un darba veidnes, lai rādītu informāciju par atbilstošo vietu vai vietu diapazonu, kur varat novietot šos vienumus. Atgrieztajām vienībām lapā **Krājumu darbības** tiek izveidots izsniegšanas veids **Rezervācija**.

Izejošam darbam izmantojiet vienības, kam krājuma statuss ir Pieejams. Ja ir vienības ar statusu **Bojāts**, un šīm vienībām tiek palaista vispārējā plānošana, tās tiek uzskatītas par trūkstošām, un krājums tiek automātiski papildināts.

Kad krājumu statusi ir iestatīti, varat iestatīt noklusējuma krājumu statusu vietai, vienībai un noliktavai. Varat arī iestatīt noklusējuma statusu pārdošanas, pārsūtīšanas un pirkšanas pasūtījumiem. Noklusējuma pārdošanas pasūtījumu un izejošo pārsūtīšanas pasūtījumu statusam opcija **Krājuma bloķēšana** nevar būt iestatīta uz **Jā**. Krājuma statusu, kas tiek mantots no vietas, noliktavas, vienības, pirkšanas pasūtījuma, pārsūtīšanas pasūtījuma vai pārdošanas pasūtījuma noklusējuma iestatījumiem, var mainīt, izmantojot mobilo ierīci, pirkšanas un pārdošanas pasūtījumu vai pārsūtīšanas pasūtījuma rindu.

Lai plānotu to vienību segumu, kam krājuma statuss ir Pieejams, lapā **Noliktavas dimensiju grupas** noliktavas dimensijai atlasiet opciju **Vajadzības plāns pa dimensijām**. Atverot vedni **Vienības vajadzības**, vienības, kurām statuss ir Pieejams, tiks parādītas lapā **Statuss**. Lai izveidotu šo preču segšanas iestatījumus, atlasiet krājumu statusa ID pieejamo krājumu statusiem. Pamatojoties uz segšanas iestatījumiem, varat aprēķināt preču vajadzības un prognozēt pieejamo preču piegādi un piedāvājumu vispārējās plānošanas laikā. Vienības vajadzības iestatījumus nevar izveidot, ja krājuma statuss ir Bloķēts. Tā vietā izmantojiet lapu **Vienības vajadzības**, lai izveidotu vai modificētu vienības vajadzības parametrus.
