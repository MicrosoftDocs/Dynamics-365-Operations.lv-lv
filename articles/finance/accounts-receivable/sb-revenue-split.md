---
title: Ieņēmumu sadalīšanas veidnes abonementa norēķinos
description: Šajā tēmā skaidrots, kā iestatīt ieņēmumu sadalīšanas veidnes krājumiem, kas tiek pārdoti kā komplekti.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660516"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Ieņēmumu sadalīšanas veidnes abonementa norēķinos

Izmantojiet ieņēmumu **sadalīšanas veidnes lapu**, lai iestatītu veidnes ieņēmumu sadalīšanai. Ieņēmumu sadalīšana sastāv no pamatvienības, kam ir pakārtotie krājumi. Šis krājuma tips bieži tiek pārdots debitoriem kā atsevišķs krājums vai saišķis.

Piemēram, datora krājumu var veidot šādā veidā:

- **Pamatelements: abonementa** sudraba
- **Rindas (pakārtotie) vienumi:**

    - Atbalsts
    - Uzturēšana
    - Licence

Veidojot pamatelementu, ņemiet vērā šādus ierobežojumus:

- Krājumu kā pamatobjektu var norādīt tikai vienu reizi.
- Tajā pašā veidnē vecākelementu var atlasīt kā pakārtotu krājumu.
- Derīgai veidnei ir nepieciešams vismaz viens pakārtots krājums.
- Krājumu var norādīt kā atvasinātu krājumu vairāk nekā vienam saistītajam krājumam.
- Katrai pamata-pakārtotā relācijai jābūt unikālai.

## <a name="create-a-parent-item-that-has-child-items"></a>Izveidot pamatelementu, kam ir apakšelementi

Izpildiet šīs darbības, lai izveidotu pamatobjektu, kam ir apakšelementi.

1. **Ieņēmumu sadalīšanas veidnes** lapā atlasiet **Jauns**.
1. Laukā **Pamata krājums** atlasiet pamatelementu. Varianta **numura** lauks tiek atjaunināts automātiski. Vērtību var mainīt pēc jūsu pieprasītā.
1. Laukā **Sadalījuma** metode atlasiet sadalījuma metodi.
1. Sarakstā Komponenta **krājumi atlasiet** Pievienot, lai **pievienotu** atvasinātos krājumus.
1. Ja laukā **Sadalījuma** metode atlasījāt **Procentus**, laukā Procenti norādiet **procentus**.

    - Ja laukā Sadalījuma **metode atlasīta** Vienāda **summa**, lauks **Procenti** tiek automātiski atjaunināts tā, lai katram krājumam būtu vienādi procenti.
    - Ja laukā **Sadalījums atlasījāt Mainīgā summa,** **·** **·** **Nulles pamatsumma vai Nulles summa,** **lauka** Procenti vērtība paliek 0 **(nulle) un to nevar mainīt.**

1. Atlasiet **Saglabāt**.

## <a name="fields"></a>Lauki

Ieņēmumu **sadalīšanas veidnes** lapā ir šādi lauki.

| Lauks | Apraksts |
|-------|-------------|
| Pamatkrājums | Atlasiet krājuma kodu. Šis krājums kļūst par pamata krājumu izveidotam saistītam krājumam. |
| Preces nosaukums | Preces nosaukums. |
| Sadalījuma metode | <p>Atlasiet sadalījuma metodi:</p><ul><li>**Vienāda summa** – sadalījuma procenti tiek automātiski aprēķināti un vienādi sadalīti starp visiem veidnes krājumiem.</li><li>**Procenti** – sadalījumam varat norādīt procentuālo summu. Visu procentu summai ir jābūt vienādai ar 100.</li><li>**Mainīgā summa** – pakārtotie krājumi, kuriem neto summa ir 0 (nulle). Pakārtoto krājumu cena jānorāda darbību līmenī.</li><li>**Nulles** summa – pamatelements saglabā savu vienības cenu un neto summu. Visu pakārtoto krājumu neto summa ir 0 (nulle).</li><li>**Nulles pamatsumma** – pamatelementa fiksēta neto summa ir 0 (nulle). Visi pakārtotie krājumi tiek apstrādāti kā standarta krājumi. Lai pārbaudītu, vai pakārtoto krājumu summu summa ir vienāda ar pamatelementa summu, nav veikta pārbaude.</li></ul> |
| **Komponenta krājumi** | |
| Komponenta krājums | Atlasiet krājuma kodu. Šis krājums ir pakārtots krājums. |
| Varianta numurs | Atlasiet krājuma varianta numuru. |
| Preces nosaukums | Preces nosaukums. |
| Procentuālā vērtība | <p>Atskaites punkta sadalījuma procenti:</p><ul><li>Ja Sadalījuma **metodes lauks** ir iestatīts uz **Procenti**, varat norādīt procentus.</li><li>Ja Sadalījuma **metodes lauks** ir iestatīts **uz Vienāda summa**, procenti tiek automātiski aprēķināti tā, lai katram krājumam veidnē ir vienādi procenti.</li><li>**Ja laukā Sadalījuma** metode **ir** iestatīta vērtība Mainīgais daudzums, **Nulles** pamatsumma vai Nulles summa, **procenti** ir 0 (nulle) un to nevar rediģēt.</li></ul><p>Šī lauka vērtība var būt jebkurš pozitīvs skaitlis no 0 (nulle) līdz 100. Visu procentu summai ir jābūt vienādai ar 100.</p> |
| Kopējais procentuālais daudzums | <p>Vērtību summa kolonnā **Procenti**.</p><ul><li>Ja sadalījuma **metodes lauks** ir iestatīts uz **Vienāda summa** **vai** Procenti, visu procentu summai ir jābūt vienādai ar 100.</li><li>Ja Sadalījuma **metodes lauks** ir iestatīts uz **Mainīgā summa**, **Nulle** **pamatsumma** vai Nulle, kopējā procentu likme ir 0 (nulle).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Ieņēmumi, kas sadalīti pārdošanas pasūtījumā

Lai izveidotu pārdošanas pasūtījumu, kam ir krājums, kas ir iestatīts ieņēmumu sadalīšanai, sekojiet šiem soļiem.

1. **Pārdošanas pasūtījuma lapā** izveidojiet pārdošanas pasūtījumu.
2. Rindā katram krājumam, kas ir iestatīts ieņēmumu sadalīšanai, atzīmējiet izvēles **rūtiņu Ieņēmumu** sadalīšana. Šis krājums kļūst par pamatelementu. Ja veidne jau ir iestatīta, sarakstā automātiski tiek parādīti pakārtotie krājumi.
3. Lai pievienotu vairāk pakārtoto krājumu, atlasiet Pievienot **ieņēmumu sadalīšanas bērnelementu** un atlasiet pakārtoto krājumu, ko vēlaties pievienot.
4. Saglabājiet pasūtījumu.

## <a name="revenue-split-with-billing-schedules"></a>Ieņēmumi sadalīti ar norēķinu grafikiem

Lai izveidotu norēķinu grafiku, kurā ir vienība, kas ir iestatīta ieņēmumu sadalīšanai, sekojiet šiem soļiem.

1. Lapā Visi **/Aktīvie norēķinu grafiki** izveidojiet norēķinu grafiku.
2. Rindā katram krājumam, kas ir iestatīts ieņēmumu sadalīšanai, atzīmējiet izvēles **rūtiņu Ieņēmumu** sadalīšana. Šis krājums kļūst par pamatelementu. Ja veidne jau ir iestatīta, sarakstā automātiski tiek parādīti pakārtotie krājumi.
3. Lai pievienotu vairāk pakārtoto krājumu, atlasiet Pievienot **ieņēmumu sadalīšanas bērnelementu** un atlasiet pakārtoto krājumu, ko vēlaties pievienot.
4. Turpiniet ar soļiem darbam ar norēķinu grafiku.

> [!NOTE]
> Ja opcija **Automātiski izveidot ieņēmumu sadali** ir iestatīta uz Jā **lapā** **Periodiskie līguma norēķinu parametri**, tiek veiktas šādas darbības:
>
> - Ja rindas krājums ieņēmumu sadalīšanas veidnē ir iestatīts kā pamatelements, automātiski tiek **atzīmēta** izvēles rūtiņa Ieņēmumu sadalīšana.
> - Pakārtotie krājumi tiek automātiski ievadīti pārdošanas pasūtījuma vai norēķinu grafika rindā.
>
> Ja opcija **Automātiski izveidot ieņēmumu sadalījumu ir** iestatīta uz **Nē**, funkcionalitāte tiek paskaidrota iepriekš.
