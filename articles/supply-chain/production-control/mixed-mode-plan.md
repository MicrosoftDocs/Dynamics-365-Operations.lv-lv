---
title: Jaukta režīma plānošana — atsevišķu avotu, procesa avotu un racionālo avotu apvienošana
description: Šajā tēmā ir sniegta informācija par jaukta režīma plānošanu.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c16cf5bf1346cad7d5310a74b84c199ae2c71a4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986892"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Jaukta režīma plānošana — atsevišķu avotu, procesa avotu un racionālo avotu apvienošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par jaukta režīma plānošanu. Jaukta režīma plānošanā savu piegādes ķēdi varat modelēt, pamatojoties uz materiālu plūsmu. Dynamics 365 Supply Chain Management nodrošina materiālu plūsmas atbilstību jūsu modeļiem neatkarīgi no atlasītās piegādes politikas (Kanban, ražošanas pasūtījumi, pirkšanas pasūtījumi, partijas pasūtījumi vai pārsūtīšanas pasūtījumi). 

Varat atlasīt vispārējo stratēģiju preces piegādei, neatkarīgi no preces struktūras.  

Piemēram, var būt Kanban kontrole komplektācijā, kur materiāli ir ņemti komplektēšanas zonai atbilstoši ražošanas pasūtījumiem, Kanban, pārsūtīšanām, partijas pasūtījumiem, vai jebkurai kombinācijai, kas ir lietderīga piegādes ķēdes raksturlielumiem, bet jums joprojām var būt visu piegāžu pilna redzamība. Šī iespēja noved pie optimizētiem piegādes ķēdes procesiem un uzlabotas redzamības piegādes ķēdē.  

Vispārējā plānošanā izmantojamo piegādes politiku granularitāte ir atkarīga no noliktavas dimensijām, kas ir iespējotas kā vajadzības dimensijas. Lai iespējotu vispārējo plānošanu, lai kontrolētu papildināšanu un piegādes dažādu tipu novietojumos (piemēram, atdalot dažādu ražošanas vienību ražošanas stāvus vai atdalot dažādu tipu materiālu un pabeigto preču noliktavas), ieteicams iespējot vietu un noliktavu kā vajadzības dimensijas. Alternatīvi, noliktavu kā nodrošinājuma dimensiju var izlaist. Šajā gadījumā, kad izmantojat papildu noliktavas vadību, visas kustības noliktavā tiek kontrolētas ar noliktavas darbu, bet visas kustības starp noliktavām var kontrolēt ar atvilkumu Kanban.

## <a name="supply-policies"></a>Piedāvājuma politikas
Režīma plānošana nodrošina preces piedāvājuma veida kontroli un atvasināto pieprasījumu (krājumu patēriņš no materiālu komplekta \[MK\]) izsniegšanas kontroli, pamatojoties uz piedāvājumu. Pamatojoties uz pasūtījuma tipu, sistēma automātiski izvēlas materiālus, kas atbilst prasībām.  

Piedāvājuma politikas var noteikt preču līmenī vai jebkurā granularitātē, kas atbalsta jūsu prasības. Piedāvājuma politiku granularitāte tiek definēta lapā **Pasūtījuma noklusējuma iestatījumi**.  

Piedāvājuma politikas var kontrolēt ar preču, krājumu dimensijām (konfigurāciju, krāsu un lielumu), vietu un noliktavu. Šis iestatījums tiek veikts lapā **Krājumu vajadzība**.  

Noklusējuma pasūtījuma tips kontrolē, kādu pasūtījumu ģenerē vispārējā plānošana.  

Neatkarīgi no tā, kā tiek modelēta piegādes ķēde, Supply Chain Management atbalsta dažādu piedāvājuma politiku lietošanu. Jums var būt ražošanas pasūtījumi, kas tiek iegūti no Kanban. Alternatīvi, jums var būt partijas pasūtījums, kam nepieciešama prece, ko piedāvā ar pārsūtīšanām vai Kanban.  

Supply Chain Management nodrošina materiālu plūsmas atbilstību modelim.  

Noliktava materiālu izdošanai tiek piešķirta dinamiski izpildes laikā, pēc piegādes politiku definēšanas.  

Parasti Kanban netiek izveidoti nākotnes datumiem, jo Kanban ir īss dzīves cikls. Lai saglabātu pilnu redzamību piegādes ķēdē, esam ieviesuši jaunu plānošanas jēdzienu "plānotais Kanban", kas tiek izmantots, lai aprēķinātu atvasinātās vajadzības, un palīdz garantēt, ka vajadzības tiek nodrošinātas, pamatojoties uz to pašu loģiku, kas tiek izmantota, veidojot faktisko Kanban.  

Tāda pati loģika pastāv visiem citiem piedāvājuma politiku tipiem. Tāpēc ilgtermiņa materiālu plānošanas pamatā ir tāda pati loģika, kura gaidāma faktisko pasūtījumu gadījumā, pēc tam, kad ražošana un piegāde ir apstiprināta.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Materiālu sadalījuma šķērspiedāvājumu politika — resursu patēriņš uz MK
Resursu patēriņš ir svarīga funkcionalitāte. Resursu patēriņš ļauj materiālu izdošanas noliktavai būt atlasītai dinamiski, pamatojoties uz piedāvājumu politiku (pasūtījuma tipu), un arī atvieglo pamatdatu uzturēšanu.  

Resursu patēriņš pieprasa, lai noliktava, no kuras tiek izdoti materiāli, tiktu piešķirta, pamatojoties uz to, kādā veidā prece tiek piedāvāta. Citiem vārdiem sakot, izpildes laikā sistēma atrod resursus, kas ir jāizmanto ražošanā. Pamatojoties uz šiem resursiem, sistēma atrod izdošanas noliktavu.  

Darbam, kas nav atkarīgs no piedāvājuma politikas, nav jāmaina informācija par MK, ja piedāvājums mainās. Ekspromta izmaiņu gadījumā Supply Chain Management nodrošina materiālu ņemšanu no nepieciešamās noliktavas.

## <a name="process-manufacturing--the-production-type"></a>Ražošanas process — ražošanas veids
Lai nodrošinātu pilnīgu pielāgojamību jauktajā režīmā, ir ieteicams visām precēm lietot ražošanas veida MK. Šādā gadījumā preces piedāvājuma nodrošināšanai varat izmantot ražošanas pasūtījumus, Kanban, pārsūtīšanas pasūtījumus vai pirkšanas pasūtījumus. Ražošanas procesam ir jāizmanto ražošanas veids **Formula**, **Līdzprodukts**, **Blakusprodukts** vai **Plānošanas krājums**. Šiem ražošanas veidiem nevar izmantot Kanban un ražošanas pasūtījumus.



