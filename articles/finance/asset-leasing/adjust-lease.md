---
title: Nomas korekcija
description: Tēmā paskaidrots, kā koriģēt nomu. Korekcija var būt nepieciešama, ja tiek izmainīti nomas noteikumi, noma tiek pagarināta vai mainās citi apstākļi.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1016b69fd59bbe90924996f5c931cb5d0f779253de66f5f3821a8c3001d3313b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729658"
---
# <a name="adjust-leases"></a>Nomas korekcija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tēmā paskaidrots, kā koriģēt nomu. Korekcija var būt nepieciešama, ja tiek izmainīti nomas noteikumi, noma tiek pagarināta vai mainās citi apstākļi. Līdzekļu noma atbilst vadlīnijām, ko par nomas izmaiņu sniedz Grāmatvedības standartu kodifikācijas temats 842 (ASC 842) un Starptautiskais finanšu pārskatu standarts 16 (IFRS 16). ASC 842-20-15-1 definē izmaiņas nomā kā jebkādas līguma noteikumu un nosacījumu izmaiņas, kas izraisa izmaiņas nomas apjomā vai atlīdzībā. IFRS 16 39. pants nosaka, ka nomniekam jāpārvērtē nomas saistības, lai tās atspoguļotu izmaiņās nomas maksājumos.

Organizācijām, kas ievēro ASC 842 vai IFRS 16, noma tiek pārvērtēta, lai atspoguļotu pašreizējās vērtības izmaiņas nākotnes minimālajos nomas maksājumos (PVFMLP). Ja PVFMLP palielinās, izveidotais žurnāla ieraksts būs debets lietojuma tiesību līdzekļu kontam (LLT) un kredīts nomas saistību kontam par starpību starp jauno PVFMLP un iepriekšējo PVFMLP. Ja PVFMLP samazinās, žurnāla ieraksts būs debets nomas saistību kontam un kredīts LLT kontam par starpību.

Ja korekcija samazina LLT zem 0 (nulles), atlikums tiks kreditēts, lai gūtu ienākumus nomas izmaiņu grāmatošanas kontā, kas norādīts lapā **Nomas grāmatošanas konti**. Sistēma uzskaita šos darījumus un citus korekcijas ierakstus, piemēram, izmaiņas klasifikācijā, sākotnējās tiešās izmaksas, nomas stimulus, priekšapmaksas un demontāžas izmaksas, kas rodas no izmaiņām nomā.

Lai iepazītos ar konkrētām nomas korekcijas darījumu vadlīnijām, iesakām skatīt IFRS 16 un ASC 842.

## <a name="lease-adjustment-wizard"></a>Nomas korekciju vednis

Lai koriģētu nomu, veiciet tālāk norādītās darbības. Modificētie dati atjauninās nomas grafikus pēc grāmatošanas no **Nomas korekcijas** vedņa. Varat saglabāt savu darbu un aizvērt vedni jebkurā laikā un atgriezties vēlāk, lai atsāktu darbu.

Lai atvērtu **Nomas korekcijas** vedni no nomas kopsavilkuma, izpildiet šīs darbības.

1. Dodieties uz **Līdzekļu noma \> Noma \> Nomas kopsavilkums**. 
2. Atlasiet nomu koriģēšanai un pēc tam atlasiet **Nomas vednis**.
3. Sekojiet vedņa uzvednēm, lai ievadītu nepieciešamās izmaiņas.

Lai atvērtu **Nomas korekcijas** vedni no **Nomas korekcijas** lapas pielāgojumiem, kas jau ir darbībā, sekojiet šiem soļiem.

1.  Dodieties uz **Noma \> Nomas \> Nomas korekcijas**.
2.  Atlasiet nomu, kuras korekcijas statuss ir **Notiek**, un pēc tam atlasiet **Pielāgošanas vednis**.
3.  Laukos **Modifikācijas sākuma datums** un **Grāmatošanas datums** ievadiet atbilstošus datumus.
4.  Atlasiet **Nākamais**.

    Tagad noma ir pievienota **Nomas korekciju** lapai, kur varat ievadīt jaunu informāciju par to.

    Kad noma ir koriģēta, uz to attiecas lietošanas tiesību apsvērumu lauki. Ja ar izmainīto nomu nav saistītas sākotnējās tiešās izmaksas, nomas stimuli, priekšapmaksas vai demontāžas izmaksas, atstājiet attiecīgos laukus tukšus. Sākotnējie daudzumi neattieksies uz atjaunināto nomu. 

    Piemēram, iznomātājs nodrošina $ 1000 stimulu par piekrišanu nomas pagarināšanai. Šādā gadījumā, kad tiek koriģējat nomu, pagarināšanas konta laukā ievadiet **1000** laukā **Nomas stimuli, kas izriet no korekcijas**.

    Maksājumu grafika rindās tagad tiek rādīti visi maksājumi, kas veikti, sākot no mēneša, un vēlākiem mēnešiem, laukā **Modifikācijas sākuma datums**. Tā kā modifikācijas ir potenciālas, maksājumu grafika rindas nevar sākt pirms modificēšanas sākuma. Lai skatītu maksājumu grafika rindas no pirms modifikācijas sākuma datuma, dodieties uz **Nomas versijas vēstures** lapu.

8.  Atlasiet **Nākamais**.

    Nākamajā lapā ir parādīta galvenā informācija par paredzēto nomas korekciju, piemēram, nomas saistību uzturēšanas vērtības pirms modificēšanas un jaunās paredzētās nomas saistības pēc modificēšanas. Lapa rāda arī žurnāla ieraksta priekšskatījumu plānotajai nomas korekcijai.

9.  Atlasiet **Iesniegt darbplūsmai**, lai iesniegtu nomas korekciju darbplūsmas sistēmai, ja nomas korekcijas darbplūsma ir aktīva un korekcija vēl nav apstiprināta. Plašāku informāciju par to, kā izmantot nomas korekcijas darbplūsmu, skatiet tēmā [Nomu korekcijas darbplūsmu izmantošana](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Šobrīd sistēma pārrēķina korekcijas mainīgos, lai pārbaudītu, vai nomas darbības nav grāmatotas, jo vispirms tika aprēķināts korekciju pārskats un korekciju žurnāla ieraksts. Ja tiek izmainītas vērtības, tiek atjaunināts pārrēķina pārskata režģis, kā arī ir iespējams pārskatīt informāciju pirms nomas pielāgojumu atkārtotas iesniegšanas darbplūsmas sistēmā.

10. Ja darbplūsma nav aktīva vai nomas korekcija ir apstiprināta, atlasiet **Pabeigt**, lai apstrādātu izmaiņas un grāmatotu korekciju žurnāla ierakstu.

    > [!NOTE] 
    > Šobrīd sistēma pārrēķina korekcijas mainīgos, lai pārbaudītu, vai nomas darbības nav grāmatotas, jo vispirms tika aprēķināts korekciju pārskats un korekciju žurnāla ieraksts. Ja mainās vērtības, korekcijas pārskata režģis tiek atjaunināts, un varat pārskatīt izmaiņas, pirms atlasāt **Pabeigt**. Ja darbplūsma ir aktīva un nomas korekcija ir apstiprināta, jebkuras korekciju pārskata izmaiņas izraisīs apstiprinājuma statusa atiešanu uz **Nav iesniegts**. Šajā gadījumā jums atkārtoti jāiesniedz nomas korekcija darbplūsmas sistēmai.

    **Nomas korekciju** lapā korekcijas statuss tagad ir iestatīts uz **Pabeigts**.

    Lapā **Nomas pielāgojumi** joprojām varat skatīt kopsavilkuma cilnes **Korekciju pārskats** un **Korekcijas ievadnes priekšskatījums**. Nomas dati un datuma informācija ir parādīta nomas versiju vēsturē.

    Tagad tiek izveidota jauna nomas versija un jauna grafiku kopa, izmantojot modificēto informāciju. 

13. Lai skatītu jaunos grafikus, dodieties uz nomu un pēc tam atlasiet **Grāmatas**.
14. Lai apskatītu jaunizveidoto maksājumu grafiku, izvēlieties **Maksājumu grafiks**.
15. Lai skatītu jauno nomas saistību amortizācijas grafiku, kas ir ģenerēts no jaunās informācijas, aizveriet lapu **Maksājumu grafiks** un atveriet lapu **Saistību amortizācijas grafiks**.
16. Lai skatītu tikko ģenerēto līdzekļu nolietojuma grafiku, atveriet lapu **Līdzekļu nolietojuma grafiks** no lapas **Detalizēta informācija par grāmatu**.
17. Lai skatītu korekcijas žurnāla ierakstu, atlasiet **Žurnāls \> Līdzekļu nomas žurnāls**.

## <a name="cancel-a-lease-adjustment"></a>Atcelt nomas korekciju

Lai dzēstu darbībā esošo nomas korekciju, sekojiet šiem soļiem.

1.  Dodieties uz **Noma \> Nomas \> Nomas korekcijas**.
2.  Atlasīt atceļamo, darbībā esošo nomas korekciju.
3.  Atlasiet **Atcelt korekciju**. 
4.  Atlasiet **Labi**.

    > [!NOTE] 
    > Ja **Nomas korekcijas** vednī atlasāt **Atcelt**, vednī tiek atritinātas pabeigtās izmaiņas, bet netiek noņemta darbībā esošā korekcija.

## <a name="use-the-lease-adjustment-workflow"></a>Izmantot nomas korekcijas darbplūsmu

Šajā sadaļā skaidrots, kā izmantot nomas korekcijas darbplūsmu. Nomas korekcijas darbplūsma palīdz pārvaldīt nomas korekcijas saskaņotā veidā, nodrošinot apstiprinājuma soļu kopu un piešķirot tos noteiktiem lietotājiem, kuri apstiprina nomas korekciju, pirms tā kļūst par galīgu. Pēc nomas korekcijas apstiprināšanas darbplūsmā, varat izmantot **Nomas korekcijas** vedni, lai pabeigtu nomas korekciju.

1.  Lai iesniegtu nomas korekciju apstiprināšanai, dodieties uz **Noma \> Nomas \> Nomas korekcijas**.
2.  Atlasiet nomu korekcijas ID un pēc tam atlasiet **Korekcijas vednis**.
3.  Vedņa pēdējā lapā atlasiet **Iesniegt apstiprināšanai**.
4.  Ievadiet komentāru par korekciju un pēc tam atlasiet **Labi**.

    Darbplūsmas statuss tiek mainīts uz **Gaida apstiprinājumu**, un visi vedņa lauki ir bloķēti labošanai.

5.  Lai apstiprinātu nomas korekciju, dodieties uz **Noma \> Nomas \> Nomas korekcijas**.
6.  Atlasiet nomas korekcijas ID and pārskatiet kopsavilkuma cilnes **Korekciju pārskats** un **Korekcijas ievadnes priekšskatījums**.
7.  Atlasiet **Darbplūsma \> Apstiprināts**.

    **Nomas korekciju** lapā darbplūsmas statuss tagad ir iestatīts uz **Apstiprināts**. Tagad nomas korekcija ir gatava grāmatošanai, izmantojot korekciju žurnāla ierakstu.

8.  Lai turpinātu apstrādāt nomas korekciju un grāmatot korekciju ierakstu, pārejiet uz sadaļu **Noma \> Nomas \> Nomas korekcijas**.
9.  Atlasiet nomu korekcijas ID un pēc tam atlasiet **Korekcijas vednis**.
10. Atlasiet **Tālāk**, līdz aizsniedzat vedņa pēdējo lapu, un pēc tam atlasiet **Pabeigt**.

Sistēma pārrēķina nomas uzturēšanas vērtības, lai nodrošinātu, ka pašreizējie korekcijas mainīgie ir apstiprināti. Ja ir izmaiņas, apstiprinājuma statuss tiek iestatīts atpakaļ uz **Melnraksts** un jums atkārtoti jāiesniedz nomas korekcija darbplūsmas sistēmā.

## <a name="view-lease-versions"></a>Nomas versiju skatīšana

Ja noma ir koriģēta, varat apskatīt dažādas tās versijas. Varat arī skatīt vēsturiskos grafikus un iepriekšējo informāciju par nomu.

1. Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam darbību rūtī atlasiet **Nomas versiju vēsture**.

    Ja atlasītā noma ir tikusi koriģēta, lapā **Nomas versiju vēsture** tiks parādītas dažādas versijas. Sākotnējā noma ir apzīmēta ar **1** un turpmākās versijas ir numurētas augošā secībā.

    Atlasītajai nomas versijai varat apskatīt finanšu dimensijas, detalizētu informāciju par līgumu, atrašanās vietu un maksājumu grafika rindas.

2. Lai skatītu vēsturiskos grafikus, atveriet izmanīto nomu no lapas **Nomas kopsavilkums**, atlasiet vajadzīgo grāmatu un pēc tam darbību rūtī atlasiet **Grāmatas versijas vēsture**.
3. Lapā **Grāmatas versija** atlasiet versiju un grafiku, lai to skatītu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]