---
title: Nomas korekcija
description: Tēmā paskaidrots, kā koriģēt nomu. Korekcija var būt nepieciešama, ja tiek izmainīti nomas noteikumi, noma tiek pagarināta vai mainās citi apstākļi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445802"
---
# <a name="adjust-leases"></a>Nomas korekcija

[!include [banner](../includes/banner.md)]

Tēmā paskaidrots, kā koriģēt nomu. Korekcija var būt nepieciešama, ja tiek izmainīti nomas noteikumi, noma tiek pagarināta vai mainās citi apstākļi. Līdzekļu noma atbilst vadlīnijām, ko par nomas izmaiņu sniedz Grāmatvedības standartu kodifikācijas temats 842 (ASC 842) un Starptautiskais finanšu pārskatu standarts 16 (IFRS 16). ASC 842-20-15-1 definē izmaiņas nomā kā jebkādas līguma noteikumu un nosacījumu izmaiņas, kas izraisa izmaiņas nomas apjomā vai atlīdzībā. IFRS 16 39. pants nosaka, ka nomniekam jāpārvērtē nomas saistības, lai tās atspoguļotu izmaiņās nomas maksājumos.

Organizācijām, kas ievēro ASC 842 vai IFRS 16, noma tiek pārvērtēta, lai atspoguļotu pašreizējās vērtības izmaiņas nākotnes minimālajos nomas maksājumos (PVFMLP). Ja PVFMLP palielinās, izveidotais žurnāla ieraksts būs debets lietojuma tiesību līdzeklim (LLT) un kredīts nomas saistībām par starpību starp jauno PVFMLP un iepriekšējo PVFMLP. Ja PVFMLP samazinās, žurnāla ieraksts būs debets nomas saistībām un kredīts LLT par starpību.

Ja korekcija samazina LLT zem 0 (nulles), atlikums tiks kreditēts, lai gūtu ienākumus nomas izmaiņu grāmatošanas kontā, kas norādīts lapā **Nomas grāmatošanas konti**. Sistēma uzskaita šos darījumus un citus korekcijas ierakstus, piemēram, izmaiņas klasifikācijā, sākotnējās tiešās izmaksas, nomas stimulus, priekšapmaksas un demontāžas izmaksas, kas rodas no izmaiņām nomā.

Lai iepazītos ar konkrētām nomas korekcijas darījumu vadlīnijām, iesakām skatīt IFRS 16 un ASC 842.

Lai koriģētu nomu, veiciet tālāk aprakstītās darbības. Izmainītie dati atjauninās nomas grafikus pēc grafika izveides procesa palaišanas.

1. Dodieties uz **Līdzekļu noma \> Noma \> Nomas kopsavilkums**.
2. Lapā **Nomas kopsavilkums** atlasiet nomu, ko koriģēt, un pēc tam atlasiet **Koriģēt nomu**.
3. Lapā **Koriģēt nomu** ievadiet jauno informāciju koriģētajai nomai.

    Ievērojiet, ka lapa **Koriģēt nomu** līdzinās lapai **Pievienot nomu**. Turklāt, tāpat kā sākuma datums, ko norādāt, kad pievienojat nomu, nosaka, kad tiek sākta jauna noma, lauks **Izmaiņu datums** lapā **Koriģēt nomu** nosaka, kad sākas izmainītā noma. Šis datums nevar būt vēlāks nekā sākuma datums maksājumu grafika rindās.

    > [!NOTE]
    > Lauku **LLT apsvērumi** attiecas uz nomas korekciju. Ja ar izmainīto nomu nav saistītas sākotnējās tiešās izmaksas, nomas stimuli, priekšapmaksas vai demontāžas izmaksas, atstājiet šos laukus tukšus. Sākotnējie daudzumi neattieksies uz atjaunināto nomu. Visas papildu izmaksas, kas rodas, izmainoties nomai, ir jāievada lapā **Koriģēt nomu**.
    > 
    > Piemēram, iznomātājs nodrošina $ 1000 stimulu par piekrišanu nomas pagarināšanai. Šādā gadījumā, kad tiek koriģējat nomu, pagarināšanas konta laukā ievadiet **1000** laukā **Nomas stimuli**. Ja ar nomas korekciju nav saistīti nekādi stimuli, dzēsiet jebkuras vērtības, kas iepriekš ievadītas šajā laukā. Šī pati loģika piemērojama citiem LLT apsvērumiem.

    Koriģētās nomas maksājumu grafika rindas jāizveido uz paredzamā bāzes. Maksājumu grafika rindas, kas ir izveidotas uz paredzamā bāzes, nevar sākt darboties, pirms nomas izmaiņas stājas spēkā.

    Tālāk norādītās darbības ir gandrīz identiskas darbībām sākotnējai nomas atzīšanai.

4. Atlasiet **Izveidot grafikus**, lai ģenerētu pielāgoto maksājumu grafiku. Jūs saņemat ziņojumu, kurā norādīts, ka nomai ir izveidots maksājumu grafiks.

    > [!IMPORTANT]
    > Pirms atlasāt **Izveidot grafikus**, pārliecinieties, ka izmaiņu datums un maksājumu grafika rindas ir pareizas. Tāpat pārliecinieties, vai visas sākotnējās tiešās izmaksas, nomas stimuli, priekšapmaksas vai demontāžas izmaksas atbilst tikai tām izmaksām, kas rodas no korekcijas.

5. Lai skatītu tikko izveidoto maksājumu grafiku, atlasiet **Grāmatas** un atveriet lapu **Maksājumu grafiks**.
6. Lapā **Maksājumu grafiks** varat rediģēt koriģētās maksājuma summas pirms maksājuma grafika apstiprināšanas. Lai apstiprinātu grafiku, atlasiet **Apstiprināt grafiku**.

    Kad maksājumu grafiks ir apstiprināts, tiek izveidoti jauni līdzekļu nolietojuma un nomas saistību grafiki.

7. Lai skatītu jauno nomas saistību amortizācijas grafiku, kas ir ģenerēts no jaunajām ievadēm, aizveriet lapu **Maksājumu grafiks** un atveriet lapu **Saistību amortizācijas grafiks**.
8. Lai skatītu tikko ģenerēto līdzekļu nolietojuma grafiku, atveriet lapu **Līdzekļu nolietojuma grafiks** no lapas **Detalizēta informācija par grāmatu**.
9. Lai ģenerētu korekcijas žurnāla ierakstu, atlasiet **Funkcija \> Nomas korekcija**. Jūs saņemat ziņojumu, kurā teikts, ka izveidots korekcijas žurnāla ieraksts. 
10. Lai skatītu žurnāla ierakstu, atlasiet **Žurnāls \> Līdzekļu nomas žurnāls**.
11. Lai grāmatotu žurnāla ierakstu, atlasiet rindu un pēc tam atlasiet **Grāmatot**.

## <a name="view-lease-versions"></a>Nomas versiju skatīšana

Ja noma ir izmanīta, varat apskatīt dažādas tās versijas. Varat arī skatīt vēsturiskos grafikus un iepriekšējo informāciju par nomu.

1. Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam darbību rūtī atlasiet **Nomas versiju vēsture**.

    Ja atlasītā noma ir tikusi koriģēta, lapā **Nomas versiju vēsture** tiks parādītas dažādas tās versijas. Sākotnējā noma ir apzīmēta ar **1** un turpmākās versijas ir numurētas augošā secībā.

    Atlasītajai nomas versijai varat apskatīt finanšu dimensijas, detalizētu informāciju par līgumu, atrašanās vietu un maksājumu grafika rindas.

2. Lai skatītu vēsturiskos grafikus, atveriet izmanīto nomu no lapas **Nomas kopsavilkums**, atlasiet vajadzīgo grāmatu un pēc tam darbību rūtī atlasiet **Grāmatas versijas vēsture**.
3. Lapā **Grāmatas versija** atlasiet vēlamo versiju un vēlamo grafiku, lai to skatītu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]