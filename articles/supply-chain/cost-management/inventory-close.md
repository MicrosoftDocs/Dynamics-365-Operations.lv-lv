---
title: Krājumu slēgšana
description: Izsniegšanas transakciju nosegšanas ar saņemšanas transakcijām procesa gaitā var arī noteikt, ka ir jāatjaunina galvenā virsgrāmata, lai varētu redzēt veiktās korekcijas.
author: AndersGirke
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25db42351529fafbc68313c992f873918cd5e8638d9dc9417cb04f1ba5698f3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711933"
---
# <a name="inventory-close"></a>Krājumu slēgšana

[!include [banner](../includes/banner.md)]

Izsniegšanas transakciju nosegšanas ar saņemšanas transakcijām procesa gaitā var arī noteikt, ka ir jāatjaunina galvenā virsgrāmata, lai varētu redzēt veiktās korekcijas.

Krājumu slēgšanas procesa laikā saņemšanas darbības tiek segtas ar izdošanas darbībām, pamatojoties uz krājumu novērtēšanas metodi, kas ir atlasīta vienības krājumu modeļa grupā. Segšanas procesa gaitā var norādīt, ka virsgrāmata ir jāatjaunina, lai tajā ir redzamas veiktās korekcijas. Tomēr pirms krājumu slēgšanas vai pārrēķina izpildes izdošanas transakcijas tiek grāmatotas pēc aprēķinātās aktīvās vidējās izmaksu cenas. 

Pēc krājumu slēgšanas to vairs nevar iegrāmatot periodos pirms iestatītā krājumu slēgšanas datuma, ja vien pabeigtais krājumu slēgšanas process netiek atsākts. Piemēram, ja krājumu slēgšana tiek izpildīta par periodu, kas beidzas 31. janvārī, nevar grāmatot transakcijas, kuru datums ir pirms 31. janvāra. 

Krājumu vienības tiek piešķirtas vienam no diviem krājumu veidiem: krājums vai pakalpojums. Krājumu slēgšanas procesā vienādas funkcijas tiek veiktas attiecībā uz abiem tipiem. Tomēr pakalpojumu krājumu gadījumā krājumu slēgšanas procesā joprojām sedz izdošanas darbības ar saņemšanas darbībām. 

Krājumu slēgšanas procesa izpildes biežums ir atkarīgs no uzņēmuma. Tomēr transakciju apjoms var palīdzēt noteikt, cik bieži jāizpilda krājumu slēgšanas procedūra. Vairums uzņēmumu parasti veic krājumu slēgšanu mēneša beigu slēgšanas un saskaņošanas procedūru ietvaros.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Krājumu pārrēķināšana un virsgrāmata
Ja mēneša vai cita krājumu periodā ir jāveic krājumu un virsgrāmatas korekcijas, krājumu slēgšanas vietā varat veikt krājumu pārrēķināšanu. Krājumu pārrēķināšana ļauj veikt korekcijas, bet tā nenodrošina krājumu transakciju nosegšanu. 

Krājumu pārrēķināšanas laikā tiek koriģēti rīcībā esošie krājumi, tiek pielāgotas krājumu transakcijas un tiek izpildīti krājumu pārrēķini un krājumu slēgšanas. Šie uzdevumi ietekmē visus virsgrāmatas kontus, kas ir saistīti ar sākotnējo krājumu transakciju. 

**Piemērs** 

Kad izveidojat pirkšanas pasūtījumu no pārdošanas pasūtījuma, tiek atjaunināti virsgrāmatas konti, kas tika izmantoti sākotnējam pārdošanas pasūtījumam. Pat ja virsgrāmatas konti krājumu grupai, kas ir piešķirta šim krājumam, tika mainīti pēc tam, kad pārdošanas pasūtījums tika grāmatots, un krājumu pārrēķināšana izveidoja korekciju summu, šī korekciju summa tiek grāmatota sākotnējos virsgrāmatas kontos. Koriģētā summa netiek grāmatota krājumam piešķirtajos jaunajos virsgrāmatas kontos. 

Kad atjaunināšana ir pabeigta, varat pārskatīt virsgrāmatas dokumentu, kura grāmatošanu izraisīja viens no šiem uzdevumiem.

1.  Lapas **Slēgšana un pielāgošana** cilnē **Pārskats** atlasiet pārskatāmo atjauninājumu.
2.  Noklikšķiniet uz **Detalizēta informācija** un pēc tam atlasiet vienumu **Dokuments**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Krājumu slēgšanas procesa ietekme uz virsgrāmata ierakstiem
Vairāki uzdevumi, kuri tiek veikti lapā **Slēgšana un pielāgošana**, izraisa virsgrāmatas atjaunināšanu. Piemēram, virsgrāmata tiek atjaunināta, kad tiek veikta rīcībā esošo krājumu iestatīšana, krājumu transakciju koriģēšana, krājuma pārrēķināšana un krājuma slēgšana. 

Virsgrāmatas konti, kas tiek atjaunināti saistībā ar šo uzdevumu izpildi, tiek saistīti ar sākotnējām krājumu transakcijām. Piemēram, ja pārdošanas pasūtījums ir segts ar pirkšanas pasūtījumu, tiek koriģēti virsgrāmatas konti, kas tika izmantoti sākotnējam pārdošanas pasūtījumam. Tas notiek arī tad, ja šim krājumam piešķirtās krājumu grupas virsgrāmatas konti kopš pārdošanas pasūtījuma grāmatošanas ir mainījušies. Kad pēc krājumu slēgšanas tiek veidota nosegšanas summa, tā joprojām tiek grāmatota sākotnējos virsgrāmatas kontos nevis jaunajos krājumam piešķirtajos virsgrāmatas kontos. Virsgrāmatu var atjaunināt arī, atsaucot krājumu slēgšanu. 

> [!NOTE] 
> - Krājumu slēgšana ir obligāts solis mēneša beigu slēgšanas procedūrā visiem krājumu modeļiem, izņemot vidējās vērtības pārvietošanu.  Jūs tiksiet brīdināts, ja mēģināsiet aizvērt finanšu periodu, vispirms neveicot krājumu slēgšanu no perioda beigu datuma.
> - Pirms slēgšanas procedūras izpildes var skatīt to krājumu sarakstu, kuru atjaunināšanas laikā nevar nosegt.
> - Krājumu slēgšanu ir ieteicams veikt zemas darba slodzes laikā, lai vienmērīgāk sadalītu skaitļošanas resursus.

## <a name="the-inventory-close-log"></a>Krājumu slēgšanas žurnāls
Kad krājumu slēgšanas process ir pabeigts, iespējams, ka ziņojumu centrā tiek parādīts ziņojums ar informāciju, ka vienības pašizmaksa var būt nepareiza, jo transakciju nevar pilnībā nosegt. 

Pirms šī ziņojuma parādīšanas sistēmā tiek parādīts krājuma numurs un ietekmētā transakcija. Ziņojumā ir iekļauta informācija, ka šajā transakcijā izmantotais izmaksu apjoms nav atjaunināts krājumu slēgšanas dēļ. Ziņojums tiek parādīts, ja nevar nosegt izejas plūsmas veida transakciju. 

Krājuma slēgšanas procesa laikā sistēma pārbauda visas finanšu dimensijas, lai pārliecinātos, vai līdz noteiktajam slēgšanas datumam pastāv vairāk izsniegšanas nekā saņemšanas transakciju. Šī nesakritība var rasties tad, ja krājumu transakcija no pirkšanas pasūtījuma nav pilnībā finansiāli iegrāmatota, jo kreditora rēķins nav saņemts vai materiālu komplekta (MK) komponenti, kas ir iekļauti ražošanā augstākā līmenī, nav finansiāli iegrāmatoti. (Apakšražošanas izmaksas netiek aprēķinātas.) Šādā gadījumā vēlāk veiktas slēgšanas laikā netiek veikta visu izsniegšanu korekcija uz pareizo izmaksu cenu, jo nav pietiekami daudz informācijas par ieejas plūsmu. 

Katras slēgšanas procedūras izpildes gaitā sistēmā tiek norādīts, vai ir saglabāts žurnāls, kurā ir iekļauti brīdinājumi, un vai to var skatīt. 

Ja ziņojumā tiek parādīts daudz brīdinājumu, ieteicams veikt tālāk aprakstītās darbības.

-   Finansiāli atjauniniet saņemšanas transakcijas.
-   pavirziet uz priekšu slēgšanas datumu;
-   Vēlreiz novērtējiet biznesa procedūras.

Dažos gadījumos brīdinājumiem nav atbilstošu darbību. Piemēram, ja tiek izmantots marķējums un marķētā pirkšanas pasūtījuma finanšu datums ir pēc slēgšanas datuma, slēgšanas datumu nevar mainīt.

## <a name="reversing-a-completed-inventory-close"></a>Pabeigtas krājumu slēgšanas anulēšana
Iespējams, ka reizēm ir jāanulē pabeigta krājumu slēgšana, lai atgrieztu segšanas transakcijas tādā stāvoklī, kādā tās bija pirms korekciju veikšanas. Kad anulējat pabeigtu krājumu slēgšanu, krājums tiek atvērts no jauna, lai varētu iegrāmatot periodā, uz ko šī krājumu slēgšana attiecas. Saistītās izmaiņas var veikt arī virsgrāmatā. Kad koriģēšanas darbības ir pabeigtas, var vēlreiz izpildīt apstrādātā perioda krājumu slēgšanas procedūru. 

> [!NOTE] 
> Vēlreiz atvērt var tikai pēdējo slēgto krājumu periodu. Lai atsauktu vecāku krājumu slēgšanu, pa vienai ir jāatsauc visas turpmākās krājumu slēgšanas, sākot ar pēdējo slēgšanu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]