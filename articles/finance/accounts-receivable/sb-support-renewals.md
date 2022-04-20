---
title: Atbalsts un atjaunošana
description: Šajā tēmā skaidrots, kā iestatīt un izmantot atbalsta un atjaunošanas procesu pārdošanas pasūtījumiem, lai izveidotu norēķinu grafiku atjaunošanas krājumiem.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: d59eee6e858c4f0051ec103adc4e1e99e79feec9
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560513"
---
# <a name="support-and-renewals"></a>Atbalsts un atjaunošana 

Šajā tēmā skaidrots, kā ievadīt atbalsta krājumus vai atjaunot krājumus, kad ievadāt pārdošanas pasūtījumus. Šie krājumi tiek izmantoti, lai aprēķinātu maksas summu oriģinālajam atbalsta līgumam un/vai atjaunošanas summai, kas tiek izmantota, kad norēķinu grafiks tiek izveidots abonementa rēķinos. Piemēram, jūsu uzņēmums pārdod serveri debitoram, un jūs piedāvājat datu dublējuma abonementu pirmajam gadam un opciju atjaunot šo abonementu katru gadu. Atbalsta *krājums ir* pirmā gada abonements, un atjaunošanas *krājums ir* atjaunošana katram secīgam gadam.

Varat ievadīt informāciju atbalsta līgumam, atjaunošanas līgumam vai abiem. Kad ievadāt atbalsta līguma informāciju, pārdošanas pasūtījumam tiek pievienots tikai atbalsta krājums. Kad ievadāt atjaunošanas līguma informāciju, atjaunošanas krājums tiek izmantots, lai izveidotu norēķinu grafiku.

## <a name="support-and-renewal-setup"></a>Atbalsta un atjaunošanas iestatīšana

Lapā Atbalsta **un atjaunošanas līmeņi** var iestatīt dažādus atbalsta līmeņus krājumu atbalstam un atjaunošanai. Atbalsts vai atjaunošana var būt procenti no sākotnējā krājuma summas vai arī tā var būt standarta summa.

Periodisko līgumu norēķinu parametru lapā varat atlasīt **noklusējuma atbalsta līmeņus**.

Piemēram, uzņēmums var piedāvāt šādus atbalsta un atjaunošanas līmeņus.

| Atbalsta līmenis | Atbalsta procentuālā vērtība | Atjaunošanas procentuālā vērtība |
|---|---|---|
| Neierobežota | 40% | 30% |
| Zelts | 25% | 18% |
| Sudrabs | 20% | 14% |
| Bronzas | 15% | 10% |

Lai izveidotu atbalsta vai atjaunošanas līmeni, veiciet šos soļus.

1. Lapā Atbalsta **un atjaunošanas līmeņi** atlasiet **Jauns**.
2. Laukā **Atbalsta** līmenis ievadiet unikālu nosaukumu.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Atbalsta aprēķina** metode atlasiet atbalsta aprēķina metodi. Ja atlasāt **Procenti**, ievadiet atbalsta procentu likmi **laukā Atbalsta** procenti.
5. Laukā **Atjaunošanas aprēķina metode** atlasiet atjaunošanas aprēķina metodi. Ja atlasāt **Procenti**, ievadiet atjaunošanas procentuālo vērtību **laukā Atjaunošanas** procenti.
6. Atlasiet **Saglabāt**.

### <a name="fields"></a>Lauki

Lapā **Atbalsta un atjaunošanas līmeņi** ir ietverti tālāk norādīti lauki.

| Lauks | Apraksts |
|---|---|
| Atbalsta līmenis | Unikāls identifikators atbalsta vai atjaunošanas līmenim (piemēram, **Zelta vai** **Sudraba**). |
| Apraksts | Atbalsta vai atjaunošanas līmeņa apraksts. |
| Atbalsta aprēķina metode | Atlasiet atbalsta aprēķina metodi līmenim: procenti **vai** **standarta summa**. |
| Atbalsta procentuālā vērtība | Ja kā atbalsta **aprēķināšanas** metodi atlasījāt Procenti, norādiet procentuālo attiecību, kas tiek izmantota atbalsta krājuma cenas aprēķināšanai. Ja kā aprēķina **metodi atlasījāt** Standarta summu, summa tiek norādīta, veidojot darbību. |
| Atjaunošanas aprēķina metode | Atlasiet atjaunošanas aprēķina metodi līmenim: procenti **vai** standarta **summa**. |
| Atjaunošanas procentuālā vērtība | Ja kā atjaunošanas **aprēķina** metodi atlasījāt procentuālo vērtību, norādiet procentuālo vērtību, kas tiek izmantota atjaunošanas vienuma cenas aprēķināšanai. Ja kā aprēķina **metodi atlasījāt** Standarta summu, summa tiek norādīta, veidojot darbību. |

## <a name="support-and-renewal-process"></a>Atbalsta un atjaunošanas process

Atbalsta un atjaunošanas funkcionalitāte var pielietot dažādus atbalsta līmeņus krājumiem un atjaunināt atjaunošanas informāciju abonementa norēķinos.

Pirms atbalsta un atjaunošanas funkcionalitātes lietošanas, uzdevumiem jābūt pabeigtiem.

1. Lapā Atbalsta **un atjaunošanas līmeņi** izveidojiet vismaz vienu atbalstu vai atjaunošanas līmeni.
2. Krājumu iestatīšanas **lapā saistiet** krājumu ar atbalsta un atjaunošanas krājumiem. Šis uzdevums ir nepieciešams tikai tad, ja vēlaties iestatīt noklusējuma vērtības krājumu atbalstam un/vai atjaunošanai.
3. Lapā Periodiskie **līguma norēķinu parametri norādiet** noklusējuma atbalstu un atjaunošanas iestatījumus jaunajiem norēķinu grafikiem.

Lai krājumiem lietotu dažādus atbalsta līmeņus un atjauninātu informāciju par atjaunošanu, sekojiet šiem soļiem.

1. **Lapā Visi pārdošanas pasūtījumi** izveidojiet pārdošanas pasūtījumu.
2. Kopsavilkuma cilnē **Pārdošanas pasūtījuma** rindas pievienojiet preci.
3. Cilnē Rēķins **atlasiet Atbalstu un atjaunošanu** Pievienojiet atbalstu **un atjaunošanu \>**.
4. Lapā Atbalsta **un atjaunošanas process** virsraksta sadaļa tiek atjaunināta ar iestatījumiem no periodisko **līgumu norēķinu parametru** lapas. Šīs vērtības attiecas uz visiem atbalsta un atjaunošanas krājumiem. (Piemēram, ja norēķinu biežums ir iestatīts kā **Reizi** gadā visām izveidotajām pārdošanas rindām, kurām ir atjaunošanas krājums, ir gada biežums.) Lai pārdošanas pasūtījumu saistītu ar esošu norēķinu grafiku, atlasiet vērtību laukā **Norēķinu grafika** numurs.
5. Lai mainītu atbalsta vai atjaunošanas sākuma datumu, iestatiet opciju Ignorēt **sākuma datumu** uz **Jā**.
6. Lai pievienotu vai rediģētu atbalsta krājumu, atzīmējiet **izvēles** rūtiņu Atbalsts un pēc tam laukā Atbalsta krājums ievadiet **atbalsta** vienību. Krājums ir pievienots pārdošanas pasūtījumam.
7. Lai pievienotu vai rediģētu atjaunošanas krājumu, atzīmējiet **izvēles** rūtiņu Atjaunošana un pēc tam laukā Atjaunošanas krājums ievadiet atjaunošanas **krājumu**. Kad pārdošanas pasūtījums tiek iekļauts rēķinā, tiks izveidots norēķinu grafiks, kas ietver vienību.
8. Atlasiet **Labi**.
9. **Cilnē Ģenerēt** atlasiet **Rēķins**. Kad pārdošanas pasūtījums ir iegrāmatots, tiek izveidots norēķinu grafiks. Ziņojumā ir redzams paziņojums, kas satur norēķinu grafika informāciju.
10. Lapā Visi **/aktīvie norēķinu grafiki** saraksta lapā atlasiet norēķinu grafika numuru, lai pārskatītu norēķinu grafika informāciju **norēķinu grafiku** lapā.
11. Kopsavilkuma cilnē **Norēķinu grafika rindas** atlasiet Atbalsts **un atjaunošana**, lai pārskatītu izveidoto rindu informāciju.

> [!NOTE]
> Ja norēķinu grafika rindas atjaunošanas sākuma datums ir jāmaina, **·** **varat rediģēt norēķinu grafika lapas rindas sākuma datuma** vērtību. Atverot rindai lapu **Skatīt norēķinu detalizētu** informāciju, lauks **Norēķinu sākuma datums** tiek atjaunināts ar jauno datumu. Norēķinu **beigu datuma vērtība** tiek pārrēķināta, pamatojoties uz norēķinu biežumu. Atjaunošanas sākuma datumu var atjaunināt tikai tad, ja nav izveidots un grāmatots pirmais atjaunošanas norēķinu grafika rēķins. Pēc pirmā rēķina izveidošanas un grāmatošanas sākuma datumu nevar rediģēt.

Atbalsta un atjaunošanas process ir pieejams tikai pārdošanas pasūtījumam. Kad pārdošanas pasūtījumam pievienojat atbalsta un atjaunošanas krājumus, varat izveidot jaunu norēķinu grafiku vai pievienot atjaunošanas krājumu esošam norēķinu grafikam.

## <a name="support-and-renewal-audit"></a>Atbalsta un atjaunošanas audits

Lapā Atbalsts **un atjaunošana audita** lapu varat pārskatīt informāciju par norēķinu grafika rindām, kas ir izveidotas no pārdošanas pasūtījuma atjaunošanas krājuma. Šī opcija ir pieejama, kad norēķinu grafika rindas vienums ir atjaunošanas krājums.

Lai rediģētu norēķinu grafika rindas atbalsta un atjaunošanas informāciju, sekojiet šiem soļiem.

1. **Lapā Visi norēķinu grafiki** atlasiet norēķinu grafika numuru.
2. Sadaļā Norēķinu **grafika rindas atlasiet** rindu un pēc tam atlasiet Atbalsts un **atjaunošana**.
3. Pārskatiet visu informāciju par atbalsta vai atjaunošanas krājumu.
4. Veiciet nepieciešamās izmaiņas atbalsta līmenī vai atjaunošanas procentu likmi vai summu un pēc tam **ievadiet vērtību laukā Izmaiņas** iemesls.
5. Atlasiet **Procesu**.

### <a name="fields"></a>Lauki

Atbalsta **un atjaunošanas audita lapa** satur tālāk norādītos laukus.

| Lauks | Apraksts |
|-------|-------------|
| Krājuma numurs | Norēķinu grafika rindas krājuma numurs. |
| Preces nosaukums | Preces nosaukums. |
| Atbalsta plāna līmenis | Skatiet vai mainiet atjaunošanas vienuma atbalsta līmeni. |
| Atjaunošanas procentuālā vērtība | Ievadiet atjaunošanas procentuālo daudzumu, kas tiek izmantots, kad norēķinu grafikā atjaunošanas krājumam tiek aprēķināta vienības cena. |
| Atjaunošanas summa | Ievadiet atjaunošanas summu, kas tiek izmantota, kad vienības cena tiek aprēķināta atjaunošanas krājumam norēķinu grafikā. |
| Izmaiņu iemesls | Ievadiet pamatojumu atbalsta un atjaunošanas informācijas mainīšanai. Jums ir jāievada pamatojums, kad maināt atjaunošanas **procentuālo daļu**, **atjaunošanas summu** vai atbalsta **plāna līmeņa** vērtību. |
| Sākotnējais pārdošanas krājums | Oriģinālais pārdošanas krājuma numurs no pārdošanas pasūtījuma. |
| Sākotnējā neto summa | Krājuma sākotnējā neto summa. |
| Sākotnējais atbalsta līmenis | Sākotnējais krājuma atbalsta līmenis. |
| Sākotnējā atjaunošanas procentuālā vērtība | Krājuma sākotnējais atjaunošanas procentuālais daudzums. |
| Sākotnējā atjaunošanas summa | Krājuma sākotnējā atjaunošanas summa. |
| **Režģis** | |
| Sākotnējais atbalsta līmenis | Iepriekšējais atbalsta līmenis. |
| Sākotnējā atjaunošanas procentuālā vērtība | Iepriekšējās atjaunošanas procenti. |
| Sākotnējā atjaunošanas summa | Iepriekšējā atjaunošanas summa. |
| Modificēja: | Izmaiņas veicis lietotāja vārds. |
| Modificēšanas datums un laiks | Datums, kad izmaiņas notika. |
| Pamatojums | Izmaiņas iemesls. |
