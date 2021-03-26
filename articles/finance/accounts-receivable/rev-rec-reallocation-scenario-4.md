---
title: Ieņēmumu atzīšanas atkārtota sadale — 4. scenārijs
description: Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur jauna rinda tiek noņemta no esoša, daļēji rēķinā iekļauta pārdošanas pasūtījuma. Šis scenārijs rada vienu un to pašu rezultātu neatkarīgi no tā, vai rinda ir noņemta no pārdošanas pasūtījuma vai iestatīta uz statusu Atcelts.
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
ms.openlocfilehash: 50a2d0d2ca28d9b62713502700f2c4bd2e42751e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238308"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Ieņēmumu atzīšanas atkārtota sadale — 4. scenārijs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur jauna rinda tiek noņemta no esoša, daļēji rēķinā iekļauta pārdošanas pasūtījuma. Šis scenārijs rada vienu un to pašu rezultātu neatkarīgi no tā, vai rinda ir noņemta no pārdošanas pasūtījuma vai iestatīta uz statusu Atcelts.

Šim scenārijam **virsgrāmatas parametru** lapas cilnē **Ieņēmumu atzīšana** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Nē**(**Ieņēmumu atzīšana \> iestatīšana \> Virsgrāmatas parametri**).

[![Opcija Grāmatot rēķinu labojumus debitoru parādos ir iestatīta uz Nē](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir izveidots debitoram US\_SI\_0003. Debitors iegādājas klēpjdatoru (krājuma numurs S0012), instalēšanas pakalpojumus (krājuma numurs S0001) un atbalsta plānu klēpjdatoram (krājuma numurs S0008, “Nepārtraukts inženierijas pakalpojums”). Klēpjdatora un instalēšanas pakalpojumu ieņēmumi tiek nekavējoties atpazīti. Atbalsta plāna ieņēmumi tiks atlikti un atzīti 12 mēnešu laikā, kā definēts saskaņā ar līguma laika periodu.

[![Klēpjdatora, instalēšanas pakalpojumu un atbalsta plāna pārdošanas pasūtījuma rindas](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir apstiprināts. Tā kā visi trīs krājumi ir iestatīti ieņēmumu cenas sadalījumam, ieņēmumu cena tiek aprēķināta, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumus, kas tiks atpazīti, var apskatīt **ieņēmumu cenas sadalījuma** lapā (**pārdošanas pasūtījuma** lapas darbību rūts cilnes **Pārvaldīt** grupā **Ieņēmumu atzīšana** atlasiet **Ieņēmumu cenas sadalījums**). Klēpjdatora ieņēmumi tiks grāmatoti ieņēmumu kontā 995,84 $ summas apmērā. Instalēšanas pakalpojumu ieņēmumi arī tiks grāmatoti ieņēmumu kontā 314,47 $ summas apmērā. Atbalsta plāna ieņēmumi tiks grāmatoti atlikto ieņēmumu kontā 188,69 $ summas apmērā. Ieņēmumu cenu summai jābūt vienādai ar to rindu summu, kas tika iestatītas ieņēmumu cenu sadalījuma tveršanai (1.499,00 $).

[![Ieņēmumu cenas sadalījuma lapa](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Debitoram tiek izrakstīts rēķins par klēpjdatoru un atbalsta plānu, bet ne instalēšanas pakalpojumiem. Šajā ilustrācijā parādīts rēķinam grāmatotais uzskaites ieraksts.

[![Uzskaites ieraksts pārdošanas pasūtījumam, kas iekļauts rēķinā](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Uzskaites ieraksts debitoru parādos iegrāmato 1276,94 $. Tomēr, tā kā šis rēķins ir daļējs rēķins, ieņēmumi vai atliktie ieņēmumi plus nodoklis nav vienādi ar debitoru parādu summu. Starpība -14,47 $ tiek iegrāmatota daļējo rēķina ieņēmumu klīringa kontā.

Tiek izveidots arī ieņēmumu atzīšanas grafiks.

[![Ieņēmumu atzīšanas grafika lapa daļējam rēķinam](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Vēlāk debitors izlemj neiegādāties instalēšanas pakalpojumus. Tāpēc šī rinda tiek izņemta no pārdošanas pasūtījuma. Ņemiet vērā, ka pārdošanas pasūtījumu nevar apstiprināt atkārtoti, jo pārdošanas pasūtījumā paliek tikai rēķinā iekļautās rindas.

[![Pārdošanas pasūtījums pēc instalēšanas pakalpojumu rindas noņemšanas](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Kaut arī pārdošanas pasūtījumu nevar apstiprināt, to var atkārtoti sadalīt. Pārdošanas pasūtījumā atlasiet **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, lai atvērtu lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Atlasiet divas atlikušās pārdošanas pasūtījuma rindas un pēc tam atlasiet **Atjaunināt atkārtoto sadali**. Kolonna **Atkārtoti sadalītā summa** parāda jauno ieņēmumu cenu katrai atlikušajai pārdošanas pasūtījuma rindai.

[![Jaunas ieņēmumu cenas lapā Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Pēc tam atlasiet **Paredzētais dokuments**, lai skatītu uzskaites ierakstus.

[![Uzskaites ieraksti lapā Paredzētais dokuments](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Lapā **Paredzētais dokuments** pēdējās piecas rindas stornēja sākotnējo uzskaites ierakstu no grāmatotā rēķina. Pirmās četras rindas veido jaunos uzskaites ierakstus, kas tiek grāmatoti rēķinam. Ir svarīgi, ka saprotat, ka debitoram netiek piedāvāts jauns rēķins. Pēc atkārtotās sadales debitors vēl ir parādā 1276,94 $, kas ir summa, kas jaunajā uzskaites ierakstā ir jāgrāmato debitoru parādos. Jaunie ieņēmumi vai atliktie ieņēmumi plus nodokļi ir 1276,94 $. Tādēļ jums nav jāgrāmato daļējā rēķina ieņēmumu klīringa kontā.

Lai pabeigtu atkārtoto sadali, atlasiet **Apstrādāt**. Ir ievadīts grāmatošanas datums. Kad atkārtotā sadale ir pabeigta, **ieņēmumu cenas sadalījuma** lapa rāda cenas atkārtoto sadali diviem atlikušajiem krājumiem.

[![Cenas atkārtotā sadale atlikušajiem krājumiem ieņēmumu cenu sadalījuma lapā](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Tika atjaunināts arī ieņēmumu atzīšanas grafiks, ņemot vērā jauno ieņēmumu atkārtotās sadales cenu. Pārdošanas pasūtījumā atveriet lapu **Ieņēmumu atzīšanas grafiks**. Iepriekš krājumam S0008 bija 13 rindas (šim krājumam tika piešķirts 12 mēnešu grafiks). Tagad ir 39 rindas: 13 oriģinālās grafika rindas, 13 stornēšanas grafika rindas un 13 rindas, kas balstītas uz jauno ieņēmumu cenu.

[![Atjaunināta ieņēmumu atzīšanas grafika lapa ar 39 rindām krājumam S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Ja tiek atlasīts **Dokuments**, rēķinu žurnālā tiek rādīts sākotnējais uzskaites ieraksts. Lai pārdošanas pasūtījumā skatītu storno ierakstu un jauno uzskaites ierakstu, darbību rūtī atlasiet **Ieņēmumu korekcijas** un pēc tam atlasiet **Dokuments**.

Pēc tam atveriet lapu **Visi debitori** (**Debitoru parādi \> Debitori \> Visi debitori**), atlasiet debitoru **US\_SI\_0003** un pēc tam atlasiet **Transakcijas**. **Debitora transakciju** lapa rāda tikai oriģinālo rēķinu (000008) kopā ar sākotnējo uzskaites ierakstu. Tā kā lapā **Virsgrāmatas parametri** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Nē**, tiek atjaunināta tikai virsgrāmata. Tāpēc nav parādīti storno un atjauninātie uzskaites ieraksti. Ņemiet vērā, ka tiek parādītas ieņēmumu korekcijas darbības, kas tika izveidotas [3. scenārijā ](rev-rec-reallocation-scenario-3.md).

[![Sākotnējais uzskaites ieraksts debitora transakciju lapā](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]