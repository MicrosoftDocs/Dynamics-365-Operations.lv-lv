---
title: Budžeta plānošanas integrācija ar citiem moduļiem
description: Budžeta plānus var ģenerēt no vairākiem atšķirīgiem resursiem. Periodiskā procesa pamatelementi ir vienādi visiem resursiem.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c497f6ff4588ab1fd334f98ea822006006f16e4e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971232"
---
# <a name="budget-planning-integration-with-other-modules"></a>Budžeta plānošanas integrācija ar citiem moduļiem

[!include [banner](../includes/banner.md)]

 Budžeta plānus var ģenerēt no vairākiem atšķirīgiem resursiem. Periodiskā procesa pamatelementi ir vienādi visiem resursiem. 



<a name="periodic-processes-for-generating-budget-plans"></a>Periodiskie procesi budžeta plānu ģenerēšanai
----------------------------------------------

Budžeta plānus var ģenerēt no šādiem resursiem:

-   Virsgrāmatas transakcijas
-   Pamatlīdzekļi
-   Prognožu pozīcijas
-   Projektu budžeti
-   Piegādes apjoma prognozes
-   Pieprasījuma apjoma prognozes
-   Budžeta reģistra ieraksti
-   Citi budžeta plāni

Periodiskā procesa pamatelementi ir vienādi visiem procesiem. Cilnes ļauj definēt datu avotu, mērķa (budžeta plāna) atribūtus un opcijas procesa veikšanai fonā pakešuzdevuma veidā. Šī raksta turpmākajās sadaļās aprakstīti elementi, kas var nebūt acīmredzami katrā procesā.

### <a name="actions"></a>Darbības

Katram ražošanas procesam ir pieejamas trīs darbības:

-   **Izveidot jaunu budžeta plānu** izveido jaunu plānu, kuram ir atribūti, kas atlasīti sadaļā **Mērķis**. Šiem atribūtiem nav jābūt unikāliem. Tāpēc diviem plāniem var būt vienāds nosaukums un citas vērtības.
-   **Aizstāt esošo budžeta plāna scenāriju** dzēš visus datus mērķa budžeta plānā atlasītajā budžeta plāna scenārijā un izveido jaunas rindas, kas lieto atlasītos avota datus.
-   **Atjaunināt esošo budžeta plāna scenāriju un pievienot jaunus datus** atjaunina esošās rindas mērķa plānā, kas atbilst avota rindām, un pievieno jaunas rindas jauniem datiem. Atbilstības pamatā ir Virsgrāmatas konts, datums, budžeta klase un dažādi citi lauki. Piemēram, ģenerējot budžeta plānus no prognozes pozīcijām, pozīcijas numurs ir svarīgs lauks. Visas rindas, kurām ir pozīcijas numurs, kas atbilst avota pozīcijas numuram, tiek aizstātas ar jaunām rindām no avota.

### <a name="source"></a>Avots

Visiem procesiem cilne **Avots** jums ļauj filtrēt datus, izmantojot pogu **Filtrs**. Pēc noklusējuma katram procesam filtram tiek pievienoti noteikti lauki. Piemēram, procesam **Budžeta plāna ģenerēšana no virsgrāmatas** ir pieejamas un tiek rādītas ģenerēšanas lapā kategorijas **Virsgrāmatas konts** un **Galvenais konts**. Visi filtram pievienotie lauki tiek pievienoti arī lapai kopā ar visiem pievienotajiem kritērijiem.

### <a name="target"></a>Adresāts

Opcija **Vēsturiskais** cilnē **Mērķis** ļauj jums izmantot datumus no datu avota kā spēkā stāšanās datumus budžeta plānā. Parasti spēkā stāšanās datumam ir jābūt plāna budžeta ciklā. Ja iestatāt opciju **Vēsturiskais** uz **Jā**, avota datums (pat gads) tiek izmantots, lai jūs varētu izmantot agrākos datus kā pamatu salīdzināšanai. Vēsturiskos datus budžeta plānā nevar modificēt un plāns ir iestatīts uz apstiprināto darbplūsmas statusu. Tomēr, var atiestatīt statusu, ja tas ir nepieciešams, ja citi scenāriji plānā pieprasa izmaiņas.

Lauks **Apkopot kopsummu pēc** lapas augšdaļā arī nosaka izmantoto datumu. Šajā laukā aprēķina kopsummas, un pēc izvēles iestata spēkā stāšanās datumu uz finanšu gadu vai finanšu perioda pirmo dienu. 

Daudzi no laukiem cilnē <strong>Mērķis</strong> kļūst rediģējami vai tikai lasāmi atkarībā no atlasītās darbības. Pārejot no jauna budžeta plāna izveides uz esošā plāna atjaunināšanu, lauks **Budžeta plāna nosaukums** kļūst nepieejams, un kļūst pieejami lauki, kas ir saistīti ar esošā plāna atlasi. Cilnē **Mērķis** un cilnē **Avots** lauks **Virsgrāmata** nekad nav pieejams, jo vērtība tiek noteikta pēc atlasītā budžeta plānošanas procesa. 

Lauks **Budžeta klase** var iestatīt budžeta plāna rindas kā izdevumu transakcijas vai ieņēmumu transakcijas. Parasti, ieņēmumu transakcijas ir kredīti Virsgrāmatas kontā un tādējādi saglabātas kā negatīvas summas. Parasti šīs transakcijas parādās arī kā negatīvas summas budžeta plānā. Tomēr, pievienojot budžeta klasi kā lauku plāna izkārtojumā, varat iespējot opciju, lai ieņēmumi tiktu rādīti kā pozitīvas summas.

### <a name="generation-rules"></a>Ģenerēšanas kārtulas

Trīs lauki nodrošina papildu funkcionalitāti: **Faktors**, **Minimums** un **Noapaļošanas** **nosacījumi**. 

Vērtība laukā **Faktors** tiek reizināta ar avota summu, lai iestatītu daudzumu budžeta plānā. Pielāgojumus var veikt pēc budžeta plāna rindu izveides. Piemēram, jūs varat ievadīt **1,03** 3 procentu pieaugumam. Šim koeficientam jābūt pozitīvam skaitlim. 

Lauks **Minimums** ļauj iestatīt sliekšņa summu budžeta plāna rindu veidošanai. Ja avota summa ir mazāka par šo skaitli, budžeta plāna rinda netiek izveidota. Vērtība **0,00** ļauj izmantot visas summas, bet neierobežo rindas uz pasīvajām summām. (Neviena vērtība rindas neierobežo uz pasīvajām summām. Negatīvas summas vienmēr ir iekļautas, un parasti tās apzīmē kredīta ierakstus.)

Lauks **Noapaļošanas nosacījumi** ļauj iestatīt izveidoto budžeta plāna rindu precizitāti. Var noapaļot summas līdz valūtas tuvākajai vērtībai 1,00, 10,00, 100,00 utt.

## <a name="notes-for-specific-processes"></a>Piezīmes par konkrētiem procesiem
### <a name="generate-budget-plan-from-general-ledger"></a>Budžeta plāna ģenerēšana no virsgrāmatas

Veidojot budžeta plānu no Virsgrāmatas datiem, lauks **Apkopot kopsummu pēc** ir jāiestata uz **Finanšu gads**, ja opcija **Vēsturiskais** ir iestatīta uz **Nē**. Periodi un datumi avotā var neatbilst mērķa datumu periodiem. Tā kā procesā nav uzticama veida, kā kartēt šīs vērtības, process ir jāierobežo ar gada pirmo. 

Mērķī lauks **Budžeta klase** ir iestatīts uz **Izdevumi** vai **Ieņēmumi**. Šis iestatījums tiek izmantots, lai atlasītu atribūtu **Budžeta tips** rindām, kas tiek izveidotas, kad galvenajam kontam rindā nav tips **Ieņēmumi** vai **Izdevumi**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Budžeta plāna ģenerēšana no pamatlīdzekļiem

Procesam **Budžeta plāna ģenerēšana no pamatlīdzekļiem** nav opcijas apvienošanai pēc perioda vai dienas. Nav arī nevienas opcijas plāna iestatīšanai par vēsturisku. Šo periodisko procesu varat izmantot, lai budžeta plānošanā iekļautu prognozētās pamatlīdzekļu transakcijas.

### <a name="generate-budget-plan-from-forecast-positions"></a>Budžeta plāna ģenerēšana no prognozes pozīcijām

Process **Budžeta plāna ģenerēšana no prognozes pozīcijām** piešķir avota prognozes pozīciju budžeta plāna rindai. Pozīciju var skatīt, pievienojot prognozes pozīciju kā rindu budžeta plāna izkārtojumā vai izmantojot pieprasījumu **Budžeta plāna rindas**. Ja nevēlaties piešķirt prognozes pozīciju budžeta plāna rindām, iestatiet opciju **Ietvert pozīciju budžeta plāna rindā** uz **Nē**.

Budžeta plāna rindas ir apkopotas pēc virsgrāmatas konta un pozīcijas. Taču pozīcijas numuru varat izslēgt, lai rindas tiktu apkopotas tikai pēc virsgrāmatas konta. Cilnē **Mērķis** iestatiet opciju **Ietvert pozīciju budžeta plānā** uz **Nē**.

Laukā **budžeta plāna FTE scenārijs** var atlasīt scenāriju, lai ietvertu pilnas slodzes ekvivalentu (FTE) skaitu budžeta plānā. Šis lauks ir ierobežots ar daudzuma tipa scenārijiem, kas ir iekļauti mērķa budžeta plāna izkārtojumā. Ja atlasāt FTE scenāriju, jāatlasa arī FTE galvenais konts. Šis konts tiek izmantots, lai izveidotu daudzuma budžeta plāna rindas. 

Budžeta plānošanas process un budžeta plāna scenārijs, kas atlasīti avotā, iestata mērķa scenārija budžeta plānošanas procesu un scenāriju. Tā kā šie atribūti ir piešķirti prognožu pozīcijām, tiem ir jāatbilst budžeta plānam. Tāpēc šos atribūtus nevar modificēt mērķī.

### <a name="generate-budget-plan-from-project-forecasts"></a>Ģenerēt budžeta plānu no projektu prognozēm

Procesam **Budžeta plāna ģenerēšana no projektu prognozēm** tāpat kā procesam **Budžeta plāna ģenerēšana no prognozes pozīcijām** ir iespēja iekļaut projekta daudzumus (stundas, izdevumus un krājumus) daudzumu scenārijā. Šiem diviem procesiem ir arī līdzīgi filtri budžeta plāna izkārtojuma kolonnās. 

Cilnē **Avots** trīs opcijas sadaļā **Iekļaut pārskatu** nosaka, kuras budžeta plāna rindas tiek izveidotas. Šīs opcijas ir tādas pašas kā opcijas, kas pieejamas, kad izveidojat budžeta reģistra ierakstus tieši no projekta prognozēm. Iestatiet opciju **Peļņa un zaudējumi** uz **Jā** , lai izveidotu rindas izmaksām un ieņēmumiem. Iestatiet opciju **NP** uz **Jā**, lai izveidotu nepabeigtās ražošanas ierakstus. Iestatiet opciju **Algu sadalījums** uz **Jā**, lai izveidotu rindas algu korespondējošiem kontiem stundu transakcijām. 

Lauka **Budžeta klase** nav, jo budžeta klasi (**Izdevumus** vai **Ieņēmumus**) nosaka avots. 

Projekta budžetus var izmantot kā avotu, atlasot budžeta modeli, kas ietver projekta budžeta summas. Atcerieties, ka projektu budžeti izveido projekta budžeta ierakstus, kad tie tiek apstiprināti.

Lai atlasītu tikai budžeta plāna rindu izmaksas vai ieņēmumus, izmantojiet filtru, lai atlasītu <strong>Budžeta labojumi: Summas tips = Izmaksas</strong>. Lai atlasītu tikai viena tipa prognozes, izmantojiet filtru, lai atlasītu <strong>Budžeta labojumi: Transakcijas tips = *xxx</strong>*. 

Tikai vienu budžeta modeli var izmantot, lai ģenerētu budžeta plāna scenāriju. Ja veicat procesu vienam budžeta modelim, un pēc tam veicat atjauninājumu un mēģināt norādīt citu modeli, pirmais modelis tiks pārrakstīts, ja lieto vienu un to pašu projektu un Virsgrāmatas konus. Lai ģenerētu budžeta plāna scenāriju no vairāk nekā viena budžeta modeļa, ģenerējiet citos budžeta plāna scenārijos un izmantojiet sadalījuma opcijas, lai tās pievienotu kopā citā scenārijā. 

Process **Budžeta plāna ģenerēšana no projektu prognozēm** piešķir arī avota projektu budžeta plāna rindai.

### <a name="generate-budget-plan-from-supply-forecast"></a>Ģenerēt budžeta plānu no piegādes apjoma prognozes

Avota filtra opcijas procesā **Budžeta plānu ģenerēšana no piegādes apjoma prognozes** tika modelētas pēc opcijām funkcijā **Pārsūtīt pirkšanas budžetu uz Virsgrāmatu**, jo process un funkcija ir līdzīgi.

### <a name="generate-budget-plan-from-demand-forecast"></a>Budžeta plāna ģenerēšana no pieprasījuma apjoma prognozes

Procesam **Budžeta plāna ģenerēšana no pieprasījuma apjoma prognozes** var iestatīt opciju **Pārdošanas pasūtījums** uz **Jā**, lai ģenerētu ieņēmumu rindas budžeta plānā, iestatiet opciju **Patēriņš** uz **Jā**, lai izveidotu izdevumu rindas, vai iestatiet abas opcijas uz **Jā**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Ģenerēt budžeta plānu no budžeta reģistra ierakstiem

Procesā **Budžeta plāna ģenerēšana no budžeta reģistra ierakstiem** avotam jānorāda viens apakšmodelis, viens budžeta kods un viens ieraksta numurs. Citiem vārdiem sakot, budžeta plāna rindas var vienā reizē izveidot tikai vienam budžeta reģistra ierakstam. Varat izmantot papildu ierakstus vienā un tajā pašā budžeta plānā, palaižot procesu vienu reizi katram avota ierakstam.

### <a name="generate-budget-plan-from-budget-plan"></a>Budžeta plāna ģenerēšana no budžeta plāna

Procesā **Budžeta plāna ģenerēšana no budžeta plāna** papildu opciju kopa cilnē **Mērķis** ļauj piešķirt jaunas finanšu dimensijas. Ja ir atlasīta finanšu dimensija, šī vērtība tiks izmantota visām budžeta plāna rindām. Tāpēc jūs varat izmantot vienu budžeta plānu kā pamatu citiem budžeta plāniem, bet varat arī piešķirt, piemēram, citu departamentu vai izmaksu centru jauniem budžeta plāniem.

## <a name="looking-back-from-the-budget-plan"></a>Skatoties atpakaļ no budžeta plāna
### <a name="budget-plans-by-dimension-set-inquiry"></a>Budžeta plāni pēc dimensiju kopas pieprasījuma

Pieprasījums **Budžeta plāni pēc dimensiju kopas** ietver vairākas opcijas, kas ļauj palaist vaicājumu, lai palīdzētu identificēt budžeta plāna datu avotu. 

Atlasiet rindu un noklikšķiniet uz pogas **Budžeta plāna rindas**, lai izpildītu vaicājumu **Budžeta plāna rindas**. Rezultāti tiek filtrēti atlasītās rindas dimensijas vērtībām. Pēc tam varat izmantot papildu parametrus. 

Izmantojiet pogas **Piegādes apjoma prognoze** un **Pieprasījuma apjoma prognoze**, lai izpildītu šos vaicājumus. Abos gadījumos vaicājums meklē budžeta rindas, kuras varētu izveidot budžeta plāna rindas. 

Pieejamie papildu pārskati ietver pārskatu **Prognozes pozīcijas pēc budžeta plāna**. Šis pārskats ir īpaši noderīgs, ja vēlaties noskaidrot, vai pozīcija ir pareizi piešķirta budžeta plāniem.



