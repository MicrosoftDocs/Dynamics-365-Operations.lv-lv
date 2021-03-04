---
title: Ieņēmumu atzīšanas atkārtota sadale — 3. scenārijs
description: Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur jauna rinda tiek pievienota esošam, rēķinā iekļautam pārdošanas pasūtījumam. Kad līgumam tiek pievienots jauns krājums, to var pievienot jaunam pārdošanas pasūtījumam vai esošajam pārdošanas pasūtījumam.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51646d27fe8c343c99360815d22949ffe0757979
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003358"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Ieņēmumu atzīšanas atkārtota sadale — 3. scenārijs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur jauna rinda tiek pievienota esošam, rēķinā iekļautam pārdošanas pasūtījumam. Kad līgumam tiek pievienots jauns krājums, to var pievienot jaunam pārdošanas pasūtījumam vai esošajam pārdošanas pasūtījumam. Šajā scenārijā ir parādīts arī tas, kas notiek, ja tiek atjaunināti debitoru parādi atkārtotas sadales dēļ.

Šim scenārijam **virsgrāmatas parametru** lapas cilnē **Ieņēmumu atzīšana** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Jā**(**Ieņēmumu atzīšana \> Iestatīšana \> Virsgrāmatas parametri**).

[![Opcija Grāmatot rēķinu labojumus debitoru parādos ir iestatīta uz Jā](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir izveidots debitoram US\_SI\_0003. Debitors iegādājas klēpjdatoru (krājuma numurs S0012) un tam paredzētu atbalsta plānu (krājuma numurs S0008, "Nepārtraukts inženierijas pakalpojums"). Klēpjdatora ieņēmumi tiek nekavējoties atpazīti. Atbalsta plāna ieņēmumi tiks atlikti un atzīti 12 mēnešu laikā, kā definēts saskaņā ar līguma laika periodu.

[![Klēpjdatora un atbalsta plāna pārdošanas pasūtījuma rindas](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir apstiprināts. Tā kā abi krājumi ir iestatīti ieņēmumu cenas sadalījumam, ieņēmumu cena tiek aprēķināta, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumus, kas tiks atpazīti, var apskatīt **ieņēmumu cenas sadalījuma** lapā (**pārdošanas pasūtījuma** lapas darbību rūts cilnes **Pārvaldīt** grupā **Ieņēmumu atzīšana** atlasiet **Ieņēmumu cenas sadalījums**). Klēpjdatora ieņēmumi tiks grāmatoti ieņēmumu kontā 1008,01 $ summas apmērā. Atbalsta plāna ieņēmumi tiks grāmatoti atlikto ieņēmumu kontā 190,99 $ summas apmērā. Ieņēmumu cenu summai jābūt vienādai ar to rindu summu, kas tika iestatītas ieņēmumu cenu sadalījuma tveršanai (1199,00 $).

[![Ieņēmumu cenas sadalījuma lapa](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir pilnībā iekļauts rēķinā. Šajā ilustrācijā parādīts rēķinam grāmatotais uzskaites ieraksts.

[![Uzskaites ieraksts pārdošanas pasūtījumam, kas pilnībā iekļauts rēķinā](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Tiek izveidots arī ieņēmumu atzīšanas grafiks. Pēc kāda laika diviem mēnešiem ir atpazīti ieņēmumi atbalsta plānam.

[![Ieņēmumu atzīšanas grafika lapa pēc divu mēnešu beigām](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Pašlaik debitors izlemj pievienot instalēšanas pakalpojumus (krājuma numurs S0001). Šis krājums tiek pievienots esošajam pārdošanas pasūtījumam. Debitoram tiek aicināts apstiprināt, ka vēlas modificēt pilnībā rēķinā iekļauto pārdošanas pasūtījumu, un tas viņš atlasa **Jā**.

[![Pārdošanas pasūtījums pēc instalēšanas pakalpojumu rindas pievienošanas](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Ja šis jaunais krājums ir vienīgās izmaiņas debitora līgumā, tagad var palaist atkārtotas sadales procesu. Pārdošanas pasūtījumā atlasiet **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, lai atvērtu lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Atlasiet visas šī pārdošanas pasūtījuma rindas un pēc tam atlasiet **Atjaunināt atkārtoto sadali**. Kolonna **Atkārtoti sadalītā summa** parāda jauno ieņēmumu cenu katrai pārdošanas pasūtījuma rindai.

[![Jaunas ieņēmumu cenas lapā Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Pēc tam atlasiet **Paredzētais dokuments**, lai skatītu uzskaites ierakstus. Tā kā lapas **Virsgrāmatas parametri** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Jā** , šie uzskaites ieraksti tiks grāmatoti virsgrāmatā, izmantojot kredīta dokumentu, un jaunais rēķins tiks izveidots debitoru parādos.

[![Uzskaites ieraksti lapā Paredzētais dokuments](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Lapā **Paredzētais dokuments** pēdējās četras rindas stornēja sākotnējo uzskaites ierakstu no grāmatotā rēķina. Pirmās piecas rindas veido jaunos uzskaites ierakstus, kas tiek grāmatoti rēķinam. Ir svarīgi, ka saprotat, ka debitoram netiek piedāvāts jauns rēķins. Pēc atkārtotās sadales debitors vēl ir parādā 1276,94 $, kas ir summa, kas jaunajā uzskaites ierakstā ir jāgrāmato debitoru parādos. Korespondējošais nodoklis un ieņēmumi vai atliktie ieņēmumi ir šādi: 995,83 $ + 188,69 $ + 77,94 $ = 1.262,46 $. Ieņēmumu un atlikto ieņēmumu summa ir mainīta atkārtotās sadales dēļ. Starpība -14,48 $ tiek iegrāmatota daļējo rēķina ieņēmumu klīringa kontā. Šī bilance tiks klīrēta, kad rēķins tiks iegrāmatots jaunajam krājumam, kas tika iekļauts pārdošanas pasūtījumā.

Lai pabeigtu atkārtoto sadali, atlasiet **Apstrādāt**. Ir ievadīts grāmatošanas datums. Kad atkārtotā sadale ir pabeigta, **ieņēmumu cenas sadalījuma** lapa rāda cenas atkārtoto sadali visiem trim krājumiem.

[![Cenas atkārtotā sadale visiem trim krājumiem ieņēmumu cenu sadalījuma lapā](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Tika atjaunināts arī ieņēmumu atzīšanas grafiks, ņemot vērā jauno ieņēmumu atkārtotās sadales cenu. Pārdošanas pasūtījumā atveriet lapu **Ieņēmumu atzīšanas grafiks**. Iepriekš krājumam S0008 bija 13 rindas (šim krājumam tika piešķirts 12 mēnešu grafiks). Tagad ir 39 rindas: 13 oriģinālās grafika rindas, 13 stornēšanas grafika rindas un 13 rindas, kas balstītas uz jauno ieņēmumu cenu.

[![Atjaunināta ieņēmumu atzīšanas grafika lapa ar 39 rindām krājumam S0008](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Ja tiek atlasīts **Dokuments**, rēķinu žurnālā tiek rādīts sākotnējais uzskaites ieraksts. Lai pārdošanas pasūtījumā skatītu storno ierakstu un jauno uzskaites ierakstu, darbību rūtī atlasiet **Ieņēmumu korekcijas** un pēc tam atlasiet **Dokuments**.

Pēc tam atveriet lapu **Visi debitori** (**Debitoru parādi \> Debitori \> Visi debitori**), atlasiet debitoru **US\_SI\_0003** un pēc tam atlasiet **Transakcijas**. **Debitora transakciju** lapa rāda oriģinālo rēķinu (000006), stornējamo dokumentu (000006-1) un jauno rēķinu (000006-2). Oriģinālais rēķins un stornējamais dokuments tiek segti viens pret otru un to bilance ir 0 (nulle). Apskatiet katru dokumentu, lai redzētu ietekmi virsgrāmatā.

[![Oriģinālais rēķins, stornējamais dokuments un jaunais rēķins debitora transakciju lapā](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Par pievienoto krājumu vēlreiz tiek izrakstīts rēķins pārdošanas pasūtījumam. Kopējais debitoram iesniegtais rēķins ir šāds: 300,00 $ + 19,50 $ nodoklis= 319,50 $. Šajā ilustrācijā parādīts grāmatotais uzskaites ieraksts.

[![Dokumenta transakciju lapa ar grāmatoto uzskaites ierakstu](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Tā kā ieņēmumu un pārdošanas summa ir lielāka par 319,50 $, iegrāmatotā starpība ir 14,48 $. Šī summa notīra bilanci no daļējā rēķina ieņēmumu klīringa konta. Šī bilance tiek atjaunināta jaunajā uzskaites ierakstā, kas tika grāmatots pēc atkārtotās sadales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]