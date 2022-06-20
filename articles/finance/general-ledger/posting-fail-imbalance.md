---
title: Žurnāla grāmatošanas kļūme neatbilstības dēļ
description: Šajā rakstā skaidrots, kādēļ debeti un kredīti dokumentu darbībās var nebūt līdzsvaroti, tādējādi darbības nevar grāmatot. Rakstā ir iekļautas arī problēmas labošanas darbības.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f5afded3d5c42f8dab465b668e4c1fcdaed8c215
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861334"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Žurnāla grāmatošanas kļūme neatbilstības dēļ

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kādēļ debeti un kredīti dokumentu darbībās var nebūt līdzsvaroti, tādējādi darbības nevar grāmatot. Rakstā ir iekļautas arī problēmas labošanas darbības.

## <a name="symptom"></a>Simptoms

Dažos gadījumos žurnālu nevar grāmatot, un tiek rādīts šāds ziņojums: “Konkrētā dokumenta darījums nav sabalansēts noteiktam datumam (uzskaites valūta: 0,01 — pārskata valūta: 0,06).” Kāpēc žurnālu nevar grāmatot?

## <a name="resolution"></a>Novēršana

Grāmatojot Virsgrāmatā, katram dokumentam jābūt sabalansētam darījuma valūtā, uzskaites valūtā un pārskata valūtā, ja šīs valūtas ir definētas **Virsgrāmatas iestatījuma** lapā. (Dokumenti tiek sabalansēti, ja debetu kopsumma ir vienāda ar kredītu kopsummu.)

Kopsummas tiek rādītas žurnāla rindu lapas apakšdaļā, uzskaites valūtā un pārskata valūtā. Tās **netiek** rādītas ārvalstu valūtas darījumu valūtā. Turklāt kļūdas ziņojums, ko lietotāji saņem simulācijas vai grāmatošanas laikā, rāda tikai atšķirības uzskaites valūtā un pārskata valūtā. Tas nerāda tos darījuma valūtā, jo vienam dokumentam var būt vairāk nekā viena darījuma valūta, un žurnālā var būt ietverti dokumenti dažādās darījumu valūtās. Tāpēc ir svarīgi manuāli pārbaudīt, vai darījuma valūtas summas katram dokumentam, kuram ir tikai viena darījuma valūta, ir sabalansētas.

### <a name="transaction-currency"></a>Darījuma valūta

Simulācijas un grāmatošanas laikā sistēma pārbauda, vai katrs dokuments, kuram ir tikai viena darījuma valūta, ir sabalansēts darījuma valūtā. Katram ievadītam dokumentam var būt viena vai vairākas valūtas, kas tiek uzskatītas par darījuma valūtām. Piemēram, dokumentam, kas ir ievadīts Virsgrāmatas žurnālā, var būt divas darījuma valūtas, kad nauda tiek pārsūtīta no bankas konta, kas izmanto eiro (EUR) uz bankas kontu, kurā tiek izmantoti Kanādas dolāri (CAD).

Ja dokumentam ir tikai viena darījuma valūta, debetu kopsummai ir jābūt vienādai ar šī dokumenta kredītu kopsummu darījuma valūtā. Debitori konstatēja šādus scenārijus, kuros grāmatošana neizdevās pareizi, jo netika sabalansētas darījuma valūtas summas:

- Debetu un kopējo kredītu kopsumma **netika** sabalansēta darījuma valūtā, bet tie tika sabalansēti attiecībā uz uzskaites valūtu un pārskata valūtu. Debitors ir pieņemts, ka dokuments joprojām tiks grāmatots. Tomēr šis pieņēmums bija nepareizs. **Darījuma valūtas summām dokumentā vienmēr jābūt sabalansētām, kad visām dokumenta rindām ir viena darījuma valūta.**
- Dokuments tika importēts ar datu elementu, izmantojot Datu pārvaldības struktūru (DMF), un lietotājs domā, ka darījumu valūtas summas tika sabalansētas. Importētajā failā dažām summām bija vairāk nekā divas decimāldaļas vietas, un vairāk nekā divas decimāldaļas vietas tika iekļautas, kad summas tika importētas. Tāpēc debeti nav vienādi ar kredītiem, jo tie tika noņemti pēc sīknaudas daļas. Žurnāls neatspoguļo šo starpību dokumenta rindās, jo parādītajām summām ir tikai divas decimāldaļas vietas.
- Dokuments tika importēts ar datu elementu, izmantojot DMF, un lietotājs domāja, ka darījuma valūtas summas tika sabalansētas. Lai gan **dokuments** tika sabalansēts, dažām dokumenta rindām bija dažādi darījuma datumi. Ja pievienojat kopējos debetus un kopējos kredītus darījuma valūtai katrā **dokumenta un darījuma datumā**, tie netika sabalansēti. Šī prasība tiek īstenota, ievadot dokumentu caur Virsgrāmatas žurnālu sistēmā. Tomēr šī opcija netiek ieviesta, kad dokuments tiek importēts ar datu elementu, izmantojot DMF.

Vienā atbalstītajā scenārijā dokumentam var būt vairākas darījuma valūtas. Šajā gadījumā sistēma **nepārbauda**, vai debeti ir vienādi ar kredītiem darījuma valūtā, jo valūtas nesakrīt. Tā vietā sistēma pārbauda, vai uzskaites valūtas un pārskata valūtas summas ir sabalansētas.

### <a name="accounting-currency"></a>Uzskaites valūta

Ja visām dokumenta rindām ir viena un tā pati darījuma valūta un ja darījuma valūtas summas ir sabalansētas, sistēma pārbauda, vai uzskaites valūtas summas ir sabalansētas. Ja dokuments ir ievadīts ārzemju valūtā, maiņas kurss dokumenta rindās tiek izmantots, lai darījuma valūtas summas pārveidotu uzskaites valūtā. Vispirms katra dokumenta rinda tiek tulkota un noapaļota līdz divām decimālzīmēm aiz komata. Pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kredītus. Tā kā katra rinda tiek tulkota, debetu un kredītu kopsumma var nebūt līdzsvarota. Tomēr, ja starpības absolūtā vērtība ir **Maksimālās sīknaudas starpības** vērtībā, kas definēta **Virsgrāmatas parametru** lapā, dokuments tiks grāmatots un starpība automātiski tiks grāmatota Sīknaudas starpības kontā.

Ja dokumentam ir vairāk nekā viena darījuma valūta, katra dokumenta rinda tiek tulkota uzskaites valūtā un noapaļota līdz divām decimālzīmēm aiz komata, un pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kopējos kredītus. Lai tiktu uzskatīts par līdzsvarotu, debetiem un kredītiem ir jābūt līdzsvarotiem uzskaites valūtā.  Sīknaudas starpības konts nekad nav pievienots dokumentam uzskaites valūtā, lai debeti un kredīti pārvērstu bilancē. 

### <a name="reporting-currency"></a>Pārskata valūta

Ja visām dokumenta rindām ir viena un tā pati darījuma valūta un ja darījuma valūtas summas ir sabalansētas, sistēma pārbauda, vai uzskaites valūtas summas ir sabalansētas. Ja dokuments ir ievadīts ārzemju valūtā, maiņas kurss dokumenta rindās tiek izmantots, lai darījuma valūtas summas pārveidotu uzskaites valūtā. Vispirms katra dokumenta rinda tiek tulkota un noapaļota līdz divām decimālzīmēm aiz komata. Pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kredītus. Tā kā katra rinda tiek tulkota, debetu un kredītu kopsumma var nebūt sabalansētas. Tomēr, ja starpība ir **Maksimālās sīknaudas starpības** vērtībā, kas definēta **Virsgrāmatas parametru** lapā, dokuments tiks grāmatots un starpība automātiski tiks grāmatota Sīknaudas starpības kontā.

Ja dokumentam ir vairāk nekā viena darījuma valūta, katra dokumenta rinda tiek tulkota pārskata valūtā un noapaļota līdz divām decimālzīmēm aiz komata, un pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kopējos kredītus. Lai tiktu uzskatīts par līdzsvarotu, debetiem un kredītiem ir jābūt līdzsvarotiem pārskata valūtā.  Sīknaudas starpības konts nekad nav pievienots dokumentam pārskata valūtā, lai debeti un kredīti pārvērstu bilancē.

### <a name="example-for-an-accounting-currency-imbalance"></a>Piemērs, kad uzskaites valūtas neatbilst

> [!NOTE]
> Pārskata valūtas summa tiek aprēķināta no darījuma valūtas summas tādā pašā veidā kā uzskaites valūtas summa.

Maiņas kurss: 1,5

| Rinda | Dokuments | Konts | Valūta | Debets (transakcija) | Kredīts (transakcija) | Debets (uzskaite) | Kredīts (uzskaite) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3,33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3,33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3,34 | | 5,01 | |
| 4 | 001 | 4101- | EUR | | 10,00 | | 15,00 |
| **Summa** | | | | **10,00** | **10,00** | **15,01** | **15,00** |

Uzskaites valūtai ir neatbilstība par 0,01. Tomēr, kamēr maksimālā sīknaudas noapaļošana uzskaites valūtā ir vismaz 0,01, starpība automātiski tiks grāmatota Sīknaudas starpības kontā, un dokuments tiks sekmīgi grāmatots.
