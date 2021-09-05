---
title: Žurnāla grāmatošanas kļūme neatbilstības dēļ
description: Šajā tēmā skaidrots, kādēļ debeti un kredīti dokumentu darbībās var nebūt līdzsvaroti, tādējādi darbības nevar grāmatot. Tēmā ir iekļauti arī soļi problēmas labošanai.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385727"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Žurnāla grāmatošanas kļūme neatbilstības dēļ

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kādēļ debeti un kredīti dokumentu darbībās var nebūt līdzsvaroti, tādējādi darbības nevar grāmatot. Tēmā ir iekļauti arī soļi problēmas labošanai.

## <a name="symptom"></a>Simptoms

Dažos gadījumos žurnālu nevar grāmatot, un tiek rādīts šāds ziņojums: "Konkrētā dokumenta darbības nelīdzsvaro noteiktu datumu (uzskaites valūta: 0,01 — pārskata valūta: 0,06)." Kāpēc žurnālu nevar grāmatot?

## <a name="resolution"></a>Novēršana

Grāmatojot Virsgrāmatā, katram dokumentam jābūt līdzsvarotam darbības valūtā, uzskaites valūtā un pārskata valūtā, ja šīs valūtas ir definētas **Virsgrāmatas iestatījuma** lapā. (Dokumenti tiek līdzsvaroti, ja debetu kopsumma ir vienāda ar kredītu kopsummu.)

Kopsummas tiek rādītas žurnāla rindu lapas apakšdaļā, uzskaites valūtā un pārskata valūtā. Tās **netiek** rādītas ārvalstu valūtas darbību valūtā. Turklāt kļūdas ziņojums, ko lietotāji saņem simulācijas vai grāmatošanas laikā, rāda tikai atšķirības uzskaites valūtā un pārskata valūtā. Tas nerāda tos darījuma valūtā, jo vienam dokumentam var būt vairāk nekā viena darījuma valūta, un žurnālā var būt ietverti dokumenti dažādās darbību valūtās. Tāpēc ir svarīgi pārbaudīt, vai darbības valūtas summas katram dokumentam ir līdzsvarotas.

### <a name="transaction-currency"></a>Darbības valūta

Simulācijas un grāmatošanas laikā sistēma pārbauda, vai katrs dokuments darbības valūtā ir līdzsvarots. Katram ievadītam dokumentam darbības valūtai var būt viena vai vairākas valūtas. Piemēram, dokumentam, kas ir ievadīts Virsgrāmatas žurnālā, var būt divas darbību valūtas, kad nauda tiek pārsūtīta no bankas konta, kas izmanto eiro (EUR) uz bankas kontu, kurā tiek izmantoti Kanādas dolāri (CAD).

Ja dokumentam ir tikai viena darbības valūta, debetu kopsummai ir jābūt vienādai ar šī dokumenta kredītu kopsummu. Debitori konstatēja šādus scenārijus, kuros grāmatošana neizdevās pareizi, jo netika līdzsvarotas darbību valūtas summas:

- Debetu un kopējo kredītu kopsumma **netika** līdzsvarota darbības valūtā, bet tie tika līdzsvaroti attiecībā uz uzskaites valūtu un pārskata valūtu. Debitors ir pieņemts, ka dokuments joprojām tiks grāmatots. Tomēr šis pieņēmums bija nepareizs. **Darbības valūtas summām dokumentā vienmēr jābūt līdzsvarotām, kad visām dokumenta rindām ir viena valūta.**
- Dokuments tika importēts Microsoft Excel, un lietotājs domāja, ka darbības valūtas summas tika līdzsvarotas. Excel darbgrāmatā importētās summas tika iestatītas kā **Skaitliskās** vērtības, nevis **Valūtas** vērtības. Šajā scenārijā skaitliskās summas darbgrāmatā bija vairāk nekā divas decimāldaļas vietas, un vairāk nekā divas decimāldaļas vietas tika iekļautas, kad summas tika importētas. Tāpēc debeti nav vienādi ar kredītiem, jo tie tika noņemti pēc sīknaudas daļas. Žurnāls neatspoguļo šo starpību dokumenta rindās, jo parādītajām summām ir tikai divas decimāldaļas vietas.
- Dokuments tika importēts Excel, un lietotājs domāja, ka darbības valūtas summas tika līdzsvarotas. Lai gan dokuments tika līdzsvarots, dažām dokumenta rindām bija dažādi darbības datumi. Ja pievienojat kopējos debetus un kopējos kredītus dokumenta un darbības datumam, tie netika līdzsvaroti. Sistēma tagad nepieļauj šādu scenāriju. Dokumentam var būt tikai viens darbības datums. Šī prasība tiek īstenota, ievadot dokumentu caur Virsgrāmatas žurnālu sistēmā. Tomēr tā sākotnēji netika ieviesta, kad dokuments tika importēts, izmantojot Excel.

Vienā atbalstītajā scenārijā dokumentam var būt vairākas darbības valūtas. Šajā gadījumā sistēma **nepārbauda**, vai debeti ir vienādi ar kredītiem darbības valūtā, jo valūtas nesakrīt. Tā vietā sistēma pārbauda, vai uzskaites valūtas summas ir līdzsvarotas.

### <a name="accounting-currency"></a>Uzskaites valūta

Ja visām dokumenta rindām ir viena un tā pati darbības valūta un ja darbības valūtas summas ir līdzsvarotas, sistēma pārbauda, vai uzskaites valūtas summas ir līdzsvarotas. Ja dokuments ir ievadīts ārzemju valūtā, maiņas kurss dokumenta rindās tiek izmantots, lai darbības valūtas summas pārveidotu uzskaites valūtā. Vispirms katra dokumenta rinda tiek tulkota. Pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kredītus. Tā kā katra rinda tiek tulkota, debetu un kredītu kopsumma var nebūt līdzsvarota. Tomēr, ja starpība ir **Maksimālās sīknaudas starpības** vērtībā, kas definēta **Virsgrāmatas parametru** lapā, dokuments tiks grāmatots un starpība automātiski tiks grāmatota Sīknaudas starpības kontā.

Ja dokumentam ir vairāk nekā viena darbības valūta, katra dokumenta rinda tiek tulkota uzskaites valūtā, un pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kopējos kredītus. Lai tā tiktu uzskatīta par līdzsvarotu, debetiem un kredītiem jābūt līdzsvarotiem, un nedrīkst būt sīknaudas noapaļošanas starpība.

### <a name="reporting-currency"></a>Pārskata valūta

Ja visām dokumenta rindām ir viena un tā pati darbības valūta un ja darbības valūtas summas ir līdzsvarotas, sistēma pārbauda, vai uzskaites valūtas summas ir līdzsvarotas. Ja dokuments ir ievadīts ārzemju valūtā, maiņas kurss dokumenta rindās tiek izmantots, lai darbības valūtas summas pārveidotu uzskaites valūtā. Vispirms katra dokumenta rinda tiek tulkota. Pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kredītus. Tā kā katra rinda tiek tulkota, debetu un kredītu kopsumma var nebūt līdzsvarota. Tomēr, ja starpība ir **Maksimālās sīknaudas starpības** vērtībā, kas definēta **Virsgrāmatas parametru** lapā, dokuments tiks grāmatots un starpība automātiski tiks grāmatota Sīknaudas starpības kontā.

Ja dokumentam ir vairāk nekā viena darbības valūta, katra dokumenta rinda tiek tulkota uzskaites valūtā, un pēc tam rindas tiek summētas, lai noteiktu kopējos debetus un kopējos kredītus. Lai tā tiktu uzskatīta par līdzsvarotu, debetiem un kredītiem jābūt līdzsvarotiem, un nedrīkst būt sīknaudas noapaļošanas starpība.
