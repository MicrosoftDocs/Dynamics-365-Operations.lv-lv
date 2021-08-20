---
title: Ieņēmumu atzīšanas atkārtota sadale — 2. scenārijs
description: Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kurā ir ievadīti divi pārdošanas pasūtījumi, un pēc tam debitors pievieno līgumam krājumu, kad pirmais pārdošanas pasūtījums ir iekļauts rēķinā. Kad līgumam tiek pievienots jauns krājums, to var pievienot jaunam pārdošanas pasūtījumam vai esošajam pārdošanas pasūtījumam.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1fe195f171e8e343e9ce01b2ca0d4980d193a6fd3d9aa6f95efed66a29aa7d6d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770693"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Ieņēmumu atzīšanas atkārtota sadale — 2. scenārijs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kurā ir ievadīti divi pārdošanas pasūtījumi, un pēc tam debitors pievieno līgumam krājumu, kad pirmais pārdošanas pasūtījums ir iekļauts rēķinā. Kad līgumam tiek pievienots jauns krājums, to var pievienot jaunam pārdošanas pasūtījumam vai esošajam pārdošanas pasūtījumam.

Šim scenārijam **virsgrāmatas parametru** lapas cilnē **Ieņēmumu atzīšana** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Nē**(**Ieņēmumu atzīšana \> iestatīšana \> Virsgrāmatas parametri**).

[![Opcija Grāmatot rēķinu labojumus debitoru parādos ir iestatīta pozīcijā Nē.](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir izveidots debitoram US\_SI\_0003. Debitors iegādājas instalēšanas pakalpojumus (krājuma numurs S0001) un atbalsta plānu (krājuma numurs S0008) klēpjdatoram, taču vēl nav izvēlējies klēpjdatoru. Ieņēmumi par instalēšanas pakalpojumiem tiks atlikti līdz klēpjdatora iegādes datumam. Atbalsta plāna ieņēmumi tiks atlikti un atzīti 12 mēnešu laikā, kā definēts saskaņā ar līguma laika periodu.

[![Instalēšanas pakalpojumu un atbalsta plāna pārdošanas pasūtījuma rindas.](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir apstiprināts. Tā kā abi krājumi ir iestatīti ieņēmumu cenas sadalījumam, ieņēmumu cena tiek aprēķināta, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumus, kas tiks atpazīti, var apskatīt **ieņēmumu cenas sadalījuma** lapā (**pārdošanas pasūtījuma** lapas darbību rūts cilnes **Pārvaldīt** grupā **Ieņēmumu atzīšana** atlasiet **Ieņēmumu cenas sadalījums**). Instalēšanas pakalpojumu ieņēmumi tiks grāmatoti atlikto ieņēmumu kontā 250,00 $ summas apmērā. Atbalsta plāna ieņēmumi arī tiks grāmatoti atlikto ieņēmumu kontā 150,00 $ summas apmērā. Ieņēmumu cenu summai jābūt vienādai ar to rindu summu, kas tika iestatītas ieņēmumu cenu sadalījuma tveršanai (400,00 $).

[![Ieņēmumu cenas sadalījuma lapa.](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir pilnībā iekļauts rēķinā. Šajā ilustrācijā parādīts rēķinam grāmatotais uzskaites ieraksts.

[![Uzskaites ieraksts pārdošanas pasūtījumam, kas pilnībā iekļauts rēķinā.](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Tiek izveidots arī ieņēmumu atzīšanas grafiks, bet neviens no ieņēmumiem vēl netiek atpazīts.

[![Ieņēmumu atzīšanas grafika lapa.](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Pēc dažām dienām debitors izvēlas klēpjdatoru. Debitoram tiek ievadīts otrs pārdošanas pasūtījums.

[![Klēpjdatora pārdošanas pasūtījuma rinda.](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Otrais pārdošanas pasūtījums ir apstiprināts. Tā kā šajā pārdošanas pasūtījumā ir tikai viena rinda, ieņēmumu cenas sadalījums netiek veikts, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumu cenas sadalījums notiek tikai tad, ja ir divi vai vairāki unikāli krājumi un ja šie krājumi ir iestatīti ieņēmumu cenas sadalījumam.

Ja šis jaunais pārdošanas pasūtījums ir vienīgās izmaiņas debitora līgumā, tagad var palaist atkārtotas sadales procesu. Vienā no abiem pārdošanas pasūtījumiem atlasiet **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, lai atvērtu lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Vai arī dodieties uz **Ieņēmumu atzīšana \> Periodiski uzdevumi \> Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Atlasiet divus pārdošanas pasūtījumus un atbilstošās pārdošanas pasūtījuma rindas un pēc tam atlasiet **Atjaunināt atkārtoto sadali**. Kolonna **Atkārtoti sadalītā summa** parāda jauno ieņēmumu cenu katrai pārdošanas pasūtījuma rindai.

[![Jaunas ieņēmumu cenas lapā Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām.](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Pēc tam atlasiet **Paredzētais dokuments**, lai skatītu uzskaites ierakstus, kas tiks grāmatoti tikai virsgrāmatā. Tā kā lapas **Virsgrāmatas parametri** opcija **Grāmatot rēķinu labojumus debitoru parādiem** ir iestatīta uz **Nē**, tad, apstrādājot atkārtoto sadali, debitoru parādos nekas netiks mainīts.

[![Uzskaites ieraksti lapā Paredzētais dokuments.](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Lapā **Paredzētais dokuments** pēdējās trīs rindas stornēja sākotnējo uzskaites ierakstu no grāmatotā rēķina. Pirmās četras rindas veido jaunu uzskaites ierakstu, kas tiek grāmatots rēķinam. Ir svarīgi, ka saprotat, ka debitoram netiek piedāvāts jauns rēķins. Pēc atkārtotās sadales debitors vēl ir parādā 426,00 $, kas ir summa, kas jaunajā uzskaites ierakstā ir jāgrāmato debitoru parādos. Korespondējošais nodoklis un atliktie ieņēmumi ir šādi: 188,69 $ + 314,48 $ + 26,00 $ = 529,17 $. Atlikto ieņēmumu summa ir mainīta atkārtotās sadales dēļ. Starpība 103,17 $ tiek iegrāmatota daļējo rēķina ieņēmumu klīringa kontā. Šī bilance tiks klīrēta, kad rēķins tiks iegrāmatots otrajam pārdošanas pasūtījumam, kas tika iekļauts atkārtotajā sadalē.

Lai pabeigtu atkārtoto sadali, atlasiet **Apstrādāt**. Tiek parādīts uzaicinājums ievadīt grāmatošanas datumu, pat ja nekas nav grāmatots. Kad atkārtotā sadale ir pabeigta, **ieņēmumu cenas sadalījuma** lapa katram pārdošanas pasūtījumam parāda cenu sadalījumu visiem krājumiem abos pārdošanas pasūtījumos. Citiem vārdiem sakot, **ieņēmumu cenas sadalījuma** lapa katram pārdošanas pasūtījumam ietver krājumu, kas šajā pārdošanas pasūtījumā nepastāv, jo tas ir daļa no tā paša līguma, bet no cita pārdošanas pasūtījuma.

> [!TIP]
> Lai parādītu kontekstu, kāpēc šie papildu krājumi tiek rādīti, režģim var pievienot citas kolonnas, piemēram, **Atkārtotas sadales ID** un **Pārdošanas pasūtījums**.
> 
> [![Papildu kolonnas ieņēmumu cenu sadalījumu lapā.](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Pārdošanas pasūtījumā 00036 tika atjaunināts arī ieņēmumu atzīšanas grafiks, ņemot vērā jauno ieņēmumu atkārtotās sadales cenu. Šajā pārdošanas pasūtījumā atveriet lapu **Ieņēmumu atzīšanas grafiks**. Iepriekš krājumam S0008 bija 13 rindas (šim krājumam tika piešķirts 12 mēnešu grafiks). Tagad ir 39 rindas: 13 oriģinālās grafika rindas, 13 stornēšanas grafika rindas un 13 rindas, kas balstītas uz jauno ieņēmumu cenu.

[![Atjaunināta ieņēmumu atzīšanas grafika lapa ar 39 rindām krājumam S0008.](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Tāpat krājumam S0001 iepriekš bija divas rindas, bet tagad ir sešas.

[![Atjaunināta ieņēmumu atzīšanas grafika lapa ar sešām rindām krājumam S0001.](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Ja pārdošanas pasūtījumā 000036 tiek atlasīts **Dokuments**, rēķinu žurnālā tiek rādīts sākotnējais uzskaites ieraksts. Lai pārdošanas pasūtījumā skatītu storno ierakstu un jauno uzskaites ierakstu, darbību rūtī atlasiet **Ieņēmumu korekcijas** un pēc tam atlasiet **Dokuments**.

[![Pārdošanas pasūtījums 000036.](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Pēc tam atveriet lapu **Visi debitori** (**Debitoru parādi \> Debitori \> Visi debitori**), atlasiet debitoru **US\_SI\_0003** un pēc tam atlasiet **Transakcijas**. Tiks parādīts atvērtais rēķins no pārdošanas pasūtījuma 000036. Ja atlasīsit dokumentu, tiks parādīts sākotnējais uzskaites ieraksts, nevis jaunais uzskaites ieraksts no atkārtotās sadales. Stornējamo ierakstu un jauno uzskaites ierakstu nevar skatīt debitoru parādu sadaļā.

Otrais pārdošanas pasūtījums tagad ir iekļauts rēķinā. Kopējais debitoram iesniegtais rēķins ir šāds: 1099,00 $ + 71,44 $ nodoklis= 1170,44 $. Šajā ilustrācijā parādīts grāmatotais uzskaites ieraksts.

[![Dokumenta transakciju lapa ar grāmatoto uzskaites ierakstu.](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Tā kā ieņēmumu un pārdošanas summa ir lielāka par 1170,44 $, iegrāmatotā starpība ir -130,17 $. Šī summa notīra bilanci no daļējā rēķina ieņēmumu klīringa konta. Šī bilance tiek grāmatota jaunajā uzskaites ierakstā pēc atkārtotās sadales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]