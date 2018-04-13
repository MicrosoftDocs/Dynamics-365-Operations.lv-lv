---
title: "Atjaunināt jaunas ražošanas vienības standarta izmaksas"
description: "Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt jauna ražojamā krājuma standarta izmaksas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1cfb04a98f7d01f7766bea97157ca3c44c51e326
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Atjaunināt jaunas ražošanas vienības standarta izmaksas

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt jauna ražojamā krājuma standarta izmaksas. 

Norādījumi tālāk tiek sniegti, pieņemot, ka standarta izmaksu atjaunināšanai tiek izmantota divu versiju pieeja. Izmantojot šo pieeju, viena izmaksu aprēķināšanas versija ietver standarta izmaksas, kas sākotnēji ir noteiktas uz fiksētu periodu, un otra izmaksu aprēķināšanas versija ietver inkrementālos atjauninājumus, kas attiecas uz jauniem ražojamiem krājumiem. Inkrementālie atjauninājumi tiek ievadīti kā izmaksu ieraksti otrajā izmaksu aprēķināšanas versijā, kas pēc tam tiek aktivizēti. Lai varētu izmantot divu versiju pieeju, jādefinē otra izmaksu aprēķināšanas versija. Tālāk ir sniegtas norādes, ka definēt šo izmaksu aprēķināšanas versiju.

-   Piešķiriet instancei **Standarta izmaksas** izmaksu aprēķināšanas veidu.
-   Piešķiriet nozīmīgu identifikatoru, kas norāda izmaksu aprēķināšanas versijas komponentus, piemēram, **2016-ATJAUNINĀJUMI**.
-   Lauka grupā **Atļaut cenu veidus** pārbaudiet, vai ir iestatīta vienuma **Izmaksu cena** opcija **Jā**.
-   Atļaujiet veikt izmaksu ierakstus visām vietām (t.i., atstājiet lauku **Vieta**tukšu). Ja vieta ir ievadīta, izmaksu ierakstus var ievadīt tikai šai vietai.
-   Izmantojiet regresa principu **Aktīvs**.

Lai pievienotu jaunus ražošanas krājumus iesaldētajā periodā, veiciet tālāk norādītās darbības.

1.  Izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatījumi**, lai iespējotu otrajā izmaksu aprēķināšanas versijā ievadāmos izmaksu ierakstus, kuros iekļauti inkrementāli atjauninājumi. Nepieļaujiet neapstiprināto izmaksu aktivizāciju, kur aktivizācija ir atļauta pēc tam, kad neapstiprinātās izmaksas tiek pabeigtas un precīzi definētas. Norādiet veidlapas sākuma datumu, kā politiku aprēķina versijā, un pēc tam ievadiet sākuma datumu, kad jūs ievadiet katru izmaksu ierakstu. Sākuma datumam ir jānorāda datums, kas ir pirms jaunie krājumi tiek pārdoti vai saražoti.
2.  Izmantojiet lapu **Krājuma cena**, lai ievadītu jauno iepirkto krājumu izmaksu ierakstus. Katrā izmaksu ierakstā ievadiet izmaksu aprēķināšanas versiju, kas ietver inkrementālos atjauninājumus, un izmantojiet sākuma datumu, kas ir pirms jauno ražojamo krājumu paredzētā ražošanas datuma.
3.  Lai aprēķinātu jauno ražojamo krājumu izmaksas, izmantojiet lapu **Aprēķins**. Izmantojot lapu **Izmaksu aprēķināšanas versijas uzturēšana**, atveriet lapu **Aprēķins** un pēc tam atlasiet izmaksu aprēķināšanas versiju, kas ietver inkrementālos atjauninājumus. Izmantojiet atlases kritērijus, lai noteiktu jauno ražojamo krājumu un visus tā ražojamos komponentus. Iespējams, ka vairāku līmeņu produktu struktūrā ir arī jānorāda visi pamata krājumi, kas ietver jaunos ražojamos krājumus ar komponenta statusu. Ievadiet materiālu komplekta (MK) aprēķinu sākuma datumu, kas atbilst jauno ražojamo krājumu ražošanas sākumam. Sākuma datumam ir jābūt krājuma MK un maršruta versijas spēkā esošo datumu robežās. **Piezīme.** Trūkstošs izmaksu ieraksts var norādīt uz jaunu ražojamo krājumu. MK aprēķinu veikšana var būt ierobežota krājumiem ar trūkstošām izmaksām.
4.  Pārbaudiet jauno ražojamo krājumu aprēķināto izmaksu pilnīgumu un precizitāti. Izmantojiet lapu **Pabeigt**, lai pārskatītu gan visus krājumu izmaksu ierakstu aprēķinātās izmaksas, gan visus brīdinājuma ziņojumus informācijas žurnālā. Papildus var izmantot lapu **Aprēķins**, lai pārskatītu aprēķinātās izmaksas.
5.  Izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatījumi**, lai mainītu bloķējošo karodziņu un tādējādi atļautu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto izmaksu ierakstu aktivizēšanu.
6.  Izmantojiet lapu **Aktivizēt cenas** (ko var atvērt, izmantojot lapu **Izmaksu aprēķināšanas versijas uzturēšana**), lai iespējotu visu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto krājumu izmaksu ierakstu aktivizēšanu. Var iespējot arī atsevišķu krājumu neapstiprināto izmaksu ierakstus, lapā **Krājuma cena** noklikšķinot uz pogas **Aktivizēt neapstiprinātās cenas**.
7.  Lai nepieļautu papildu datu uzturēšanu un mainītu bloķējošos karodziņus, kas ir iekļauti otrajā izmaksu aprēķināšanas versijā, izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatīšana**. Bloķēšanas politika nepieļauj jaunu neapstiprinātu izmaksu ievadi un aktivizāciju.





