---
title: Anketu projektēšana
description: Šajā rakstā ir aprakstīts anketas izveidošanas process. Pirmā darbība anketas plānošana. Kad plānojat anketu, jūs ne tikai rakstāt jautājumus un atbildes, bet arī izveidojat struktūru, kas atbildes ļauj ierakstīt uz sakārtot.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: da4250b281438c29c82150af8db9cb8cca41c6c9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429570"
---
# <a name="design-questionnaires"></a>Anketu projektēšana

Šajā rakstā ir aprakstīts anketas izveidošanas process. Pirmā darbība anketas plānošana. Kad plānojat anketu, jūs ne tikai rakstāt jautājumus un atbildes, bet arī izveidojat struktūru, kas atbildes ļauj ierakstīt uz sakārtot. 

Rūpīgi plānota anketa var palīdzēt paaugstināt iegūto datu kvalitāti. Veicot rūpīgu plānošanu, anketai varat labāk atlasīt atbilstošajā laikā atbilstošās opcijas. Nākamie punkti jums var palīdzēt plānot efektīvu anketu:

-   Skaidri definējiet anketas mērķi, lai palīdzētu garantēt, ka jautājumi palīdz to sasniegt.
-   Nosakiet atsevišķu personu vai personu grupu, kam ir jāizpilda šī anketa.
-   Uzrakstiet jautājumus, kas būs redzami anketā, un iekļaujiet atbilžu variantus, ja piemērojams.
-   Pārliecinieties, ka anketai ir loģiska plūsma, lai respondenti saglabātu interesi.
-   Izkārtojiet jautājumus un atbildes tādā secībā, kādā tie ir jāsniedz respondentiem.
-   Izlemiet, kā ir jānovērtē rezultāti, ja piemērojams.
-   Izlemiet, vai ir nepieciešami papildu līdzekļi. Piemēram, nosakiet, vai un kā rezultāti ir jādala kategorijās, vai ir nepieciešams laika ierobežojums un vai visi jautājumi ir obligāti.

Šī izstrādes fāze ietver četras uzdevumu kategorijas, kas ir jāizpilda šādā secībā:

1.  Iestatiet priekšnosacījumus, ja nepieciešams.
2.  Iestatiet atbilžu grupas un atbildes, ja piemērojams.
3.  Iestatiet jautājumus un to saistību ar atbilžu grupām.
4.  Iestatiet pašu anketu un pievienojiet tai jautājumus.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu izveidot anketas, atbildes un jautājumus, ir nepieciešami noteikti priekšnosacījumi. Taču ne visi priekšnosacījumi ir obligāti pilnai funkcionalitātei.

### <a name="required"></a>Obligāts

| Priekšnosacījums        | Apraksts                |
|---------------------|----------------------------|
| Anketu tipi | Iedaliet anketas kategorijās. |
| Jautājumu tipi      | Iedaliet jautājumus kategorijās.      |

### <a name="optional"></a>Neobligāts

| Priekšnosacījums             | Apraksts                                                    |
|--------------------------|----------------------------------------------------------------|
| Anketas parametri | Modificējiet anketām pamata vadīklas un noklusējuma iestatījumus. |

### <a name="questionnaire-types"></a>Anketu tipi

Anketu tipi ir obligāti, un tie ir jāpiešķir, kad veidojat anketu. Anketu tipi jums palīdz vienkāršāk pārvaldīt anketas un klasificēt tās. Lietojiet anketu tipus, lai klasificētu anketas un atšķirtu tās vienu no otras. Piemēram, ja jums ir vairākas anketas, no kurām izvēlēties, varat tās filtrēt pēc tipa, lai vienkāršotu konkrētas anketas atrašanu. Šeit ir norādīti daži anketu tipu piemēri:

-   Cilvēkresursu attīstība
-   Debitoru aptaujas
-   Pārskatīšanas process

### <a name="question-types"></a>Jautājumu tipi

Jautājumu tipi ir obligāti, un tie ir jāpiešķir, kad veidojat jautājumu. 

Lietojiet jautājumu tipus, lai jautājumus dalītu kategorijās atskaišu nolūkiem. Jautājumu tipi vienkāršo arī jautājumu atrašanu, jo tipus varat izmantot kā filtrus lapā **Jautājumi**. Šeit ir norādīti daži jautājumu tipu piemēri:

-   Personāla vadība
-   Biznesa pārvaldība
-   Kursa novērtējums

### <a name="questionnaire-parameters"></a>Anketas parametri

Anketas parametri nav obligāti. Varat tos nelietot, atkarībā no jūsu uzņēmuma prasībām. 

Anketas parametri nosaka anketas anonimitāti, numuru sēriju kodus un atsauču tipus. Kad organizācija izplata kādu anketu, var būt svarīga opcija, vai respondentiem ļaut palikt anonīmiem. 

Numuru sēriju kodi tiek izmantoti, lai kārtotu jautājumus un atbildes. Pamatojoties uz šiem numuru sēriju kodiem, vērtības krājumiem tiek piešķirtas automātiski. 

Lai varētu izveidot savus datus, jums ir jādefinē visi parametri. Anketas parametru iestatījumus varat modificēt jebkurā laikā.

## <a name="questionnaire-components"></a>Anketas komponenti
Anketas ietver trīs galvenos elementus: atbilžu grupas, kas ietver atbildes uz jautājumiem ar atbilžu variantiem, jautājumus un pašu anketu. Pēc izvēles varat grupēt aptaujas jautājumus rezultātu grupās. Rezultātu grupas jums ļauj jautājumus dalīt kategorijās un sniegt papildu analīzi par anketu. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Atbilžu grupas un atbildes

Atkarībā no jautājuma tēmas respondenti uz jautājumu var atbildēt divējādi:

-   Atvērtajiem jautājumiem nav nepieciešamas noteikta formāta atbildes. Respondenti atbildi var ierakstīt kā tekstu, skaitli, datumu vai laiku. Šiem jautājumiem parasti ir nepieciešams, lai respondenti atbildēs sniegtu subjektīvu informāciju, piemēram, viedokli, aprakstu, novērtējumu vai prognozi.
-   Slēgtajiem jautājumiem ir nepieciešams, lai respondents atlasa kādu atbildi no iespējamajām pareizajām atbildēm.

Lai nodrošinātu sarakstu ar iespējamajām atbildēm uz slēgtajiem jautājumiem, varat izveidot atbildes lapā **Atbilžu grupas**. 

Atbilžu grupas un atbildes ir komponenti, kas veido informācijas pamatu, no kā tiek veidoti jautājumi. Kad izveidojat atbilžu grupu, šo atbilžu grupu varat saistīt ar kādu jautājumu laukā **Atbilžu grupa**, lapā **Jautājumi**. 

Atbilžu grupu var izmantot vairākiem jautājumiem tajā pašā aptaujā, kā arī vairākās aptaujās. 

> [!NOTE]
> Ja modificējat atbildes tekstu atbilžu grupās, kas jau ir izmantotas aizpildītās anketās, šo datu novērtēšana var kļūt apgrūtināta un anketu rezultāti var kļūt nederīgi. Ja ir nepieciešams mainīt kādu atbilžu grupu, apsveriet iespēju izveidot jaunu atbilžu grupu, nevis mainīt jau esošo. Nevar dzēst atbilžu grupas, kas ir pievienotas jautājumam vai atbildei vai kas ir atbildētas.

### <a name="questions"></a>Jautājumi

Anketā ir jābūt jautājumiem. Jautājumi var būt atvērti vai slēgti.

-   Atbildes uz atvērtajiem jautājumiem netiek kontrolētas, un respondenti var ierakstīt savas atbildes.
-   Slēgtajiem jautājumiem ir nepieciešams saraksts ar iepriekš definētiem atbilžu variantiem, un jautājumi var būt strukturēti tā, lai respondentam ļautu izvēlēties vairākas atbildes. Jautājumi ir jāveido tā, lai tie no respondenta izvilinātu noteiktu informāciju, un tiem ir jābūt saistītiem ar atbilžu grupu, kas katram slēgtajam jautājumam nodrošina atbilžu variantus. 

    > [!NOTE]
    > Lai varētu iestatīt slēgtus jautājumus, ir jāizveido atbilžu grupas un atbildes.

Jautājumus var sakārtot nosacījuma jautājumu hierarhijā, lai sekundārie jautājumi būtu atkarīgi no atbildes, ko respondents atlasa iepriekšējam jautājumam. Varat vispirms uzrakstīt jautājumus un vēlāk tos sakārtot hierarhijā.

## <a name="setting-up-questionnaires"></a>Anketu iestatīšana

> [!NOTE]
> Lai varētu iestatīt anketu, jums ir jāiestata atbildes, jautājumi un priekšnosacījumi. 

Katrai anketai varat definēt tālāk minēto informāciju.

-   Kopējais laiks vai laika ierobežojums obligāto jautājumu atbildēšanai.
-   Vai visi jautājumi ir obligāti.
-   Vai aprēķināt anketas punktu skaitu.
-   Kā kategorizēt rezultātus.
-   Vai anketa būs pieejama ierobežotai respondentu kopai.
-   Vai formas veidne ir jārāda kā fons katras anketas lapas aizmugurē.
-   Vai ir nepieciešamas papildu piezīmes, lai respondentiem paskaidrotu anketas mērķi.
-   Vai jautājumi ir jārāda fiksētā secībā vai nejauši jāatlasa no kopas.
-   Vai jautājumi tiks uzdoti tikai gadījumā, ja iepriekšējām atbildēm ir sniegtas konkrētas atbildes.

### <a name="set-up-a-questionnaire"></a>Anketas iestatīšana

Primārā lapa, ko izmantojat anketu iestatīšanai, ir lapa **Anketas**. Lai iestatītu anketu, izpildiet tālāk uzskaitītos uzdevumus šādā secībā:

1.  Izveidojiet anketu.
2.  Lai anketai pievienotu jautājumus, izpildiet vienu no šīm darbībām:
    -   Ja izmantojat rezultātu grupas, jautājumus anketai varat pievienot, izmantojot rezultātu grupas. Vispirms iestatiet anketas rezultātu grupas un pēc tam pievienojiet jautājumus šīm rezultātu grupām.
    -   Ja neizmantojat rezultātu grupas, jautājumus varat tieši pievienot anketai.

3.  Iestatiet nosacījuma jautājumu hierarhiju, ja nepieciešams.
4.  Testējiet anketu.

Lapā **Anketas** noklikšķiniet uz **Validēt**, lai testētu, vai anketa ir salikta pareizi. Taču pirms anketas izplatīšanas ieteicams to aizpildīt un testēt pašam.

### <a name="modify-a-questionnaire"></a>Anketas modificēšana

Lapā **Anketas** varat izpildīt tālāk norādītos uzdevumus.

-   Modificējiet anketā ietverto informāciju, piemēram, rezultātu grupas un jautājumus.
-   Dzēsiet un pievienojiet jautājumus.
-   Veiciet izmaiņas rezultātu grupās un kārtas numurā. 

> [!CAUTION]
> Uzmanieties, kad maināt jau aizpildītas anketas. Šādas izmaiņas var mazināt statistikas precizitāti, līdz ar to šo statistiku padarot par sliktu novērtējuma pamatu. Tā vietā apsveriet iespēju izveidot jaunu jautājumu, nevis mainīt jau atbildētu jautājumu.

Anketā nevar dzēst šādu tipu jautājumus:

-   Jautājumi, kas ir pievienoti kādai anketai
-   Jautājumi, kas jau ir atbildēti un tāpēc ir redzami dialoglodziņā **Atbildes**.

### <a name="result-groups"></a>Rezultātu grupas

Kad anketai pievienojat jautājumus, rezultātu grupas nav obligātas. 

Rezultātu grupa tiek lietota, lai aprēķinātu punktu skaitu un anketas rezultātus sadalītu kategorijās. Ja izmantojat rezultātu grupas, varat veikt šādus uzdevumus:

-   Novērtējiet anketas rezultātus, pamatojoties uz punktu statistiku.
-   Novērtējiet respondenta punktu skaitu katrai iestatītajai rezultātu grupai.
-   Ģenerējiet statistiku katrai rezultātu grupai, lai atvieglotu rezultātu analizēšanu.
-   Drukājiet atskaiti, kurā ir parādīti rezultāti par katru rezultātu grupu, kā arī papildu punktus/tekstus, kuru pamatā ir katrā rezultātu grupā iegūtais punktu skaits.

> [!NOTE]
> Lai varētu iestatīt rezultātu grupas, jums ir jāizpilda šādi uzdevumi:

-   Iestatiet slēgtos jautājumus. Slēgtam jautājumam ievades tipam lapā **Jautājumi** ir jābūt **Izvēles rūtiņa**, **Alternatīvā poga** vai **Kombinētais lodziņš**.
-   Definējiet punktu skaitu atbildēm tajās atbilžu grupās, kuras ir piešķirtas katram jautājumam.
-   Iestatiet anketu.

Lai anketai pievienotu jautājumus, izmantojot rezultātu grupas, vispirms iestatiet anketas rezultātu grupas un pēc tam šīm rezultātu grupām pievienojiet jautājumus. Ja jūs neizmantojat rezultātu grupas, jautājumus varat pievienot tieši anketai. 

Varat iestatīt vairākas rezultātu grupas, lai novērtētu punktu skaitu, ko respondents nopelna katrā kategorijā. Kad anketa ir aizpildīta, varat apskatīt punktu skaitu, kas ir iegūti katrai rezultātu grupai. 

> [!TIP]
> Lai novērtētu anketu, izmantojot punktu skaitu, bet ne atsevišķas kategorijas, visus jautājumus varat pievienot vienai rezultātu grupai. 

Katrai rezultātu grupai varat arī iestatīt vienu vai vairākus no punktu skaita atkarīgus ziņojumus, ko respondenti saņem pēc anketas aizpildīšanas. Rādītais teksts var atšķirties atkarībā no punktu skaita, ko respondents saņem rezultātu grupā. Lai izmantotu no punktu skaita atkarīgus ziņojumus, jums ir jādefinē punktu intervāli un katra intervāla apraksts. Kad respondents iegūst punktu skaitu noteiktā intervālā, rezultātu atskaitē tiek iekļauts teksts šim intervālam. 

Tā kā rezultātu grupa ir saistīta ar punktu skaitu, kas ir saistīti ar konkrētu jautājumu kopu anketā, anketai varat izmantot tikai noteiktu rezultātu grupu.

#### <a name="example-pointstexts-for-result-group-3"></a>Piemērs. Punktu skaits/teksti rezultātu grupai 3

Jūs izmantojat anketu vadības testam, kurā ir 15 jautājumi trīs kategorijās. Jūs izveidojat trīs rezultātu grupas un katrai rezultātu grupai pievienojat piecus jautājumus. Pēc tam punkti tiek summēti šajās trīs grupās. Šīs trīs rezultātu grupas ir šādas:

-   radošās spējas;
-   vadības spējas;
-   tehniskās spējas.

Lai lietotu no punktu skaita atkarīgos ziņojumus, jūs iestatāt teksta intervālus katrai rezultātu grupai. Katram jautājumam tiek piešķirti divi punkti. Tāpēc maksimālā punktu kopsumma katrā rezultātu grupā ir 10. 

Nākamajā tabulā ir parādīti no punktiem atkarīgi ziņojumi, kurus jūs definējat rezultātu grupai "vadības spējas".

| Punktu intervāls | Teksts                                       |
|----------------|--------------------------------------------|
| 1 līdz 3         | Jums ir vidējas vadības spējas.     |
| 4 līdz 7         | Jums ir labas vadības spējas.        |
| 8 līdz 10        | Jums ir izcilas vadības spējas. |

Punktu intervālus un tekstus varat iestatīt katrai rezultātu grupai anketā. Katrai rezultātu grupai tiek rādīts teksts, kas atbilst katra respondenta punktu skaitam. 

> [!NOTE]
> Intervālus un tekstus varat mainīt. Taču, ja anketa ir aizpildīta, šādas izmaiņas var izraisīt atšķirības starp iepriekšējām un jaunajām rezultātu atskaitēm.

### <a name="conditional-question-hierarchies"></a>Nosacījuma jautājumu hierarhijas

Kad iestatāt anketu, nosacījuma jautājumu hierarhijas nav obligātas. 

> [!NOTE]
> Lai varētu iestatīt nosacījuma jautājumu hierarhiju, jums anketai ir jāpievieno jautājumi, kuriem ir piešķirtas atbilžu grupas. 

Lai anketas jautājumu hierarhijas izveidošanai izmantotu nosacījuma jautājumus, varat norādīt, lai jautājumu rādīšanas secība būtu atkarīga no atbildes, kādu respondents atlasa katram jautājumam. Jautājumu secību pamatojot uz respondenta atbildi, varat modificēt aptauju, kamēr respondents to aizpilda.

#### <a name="examples"></a>Piemēri

Juridiskā persona saviem klientiem piedāvā gan preces, gan pakalpojumus. Kā parasti notiek šādos gadījumos, daži klienti iegādājas tikai preces, daži iegādājas tikai pakalpojumus, un daži iegādājas gan preces, gan pakalpojumus. Līdz ar to, kad juridiskā persona izplata klientu apmierinātības aptauju, tā anketai lieto nosacījuma struktūru, lai klientiem, kas iegādājas tikai pakalpojumus, nevajadzētu atbildēt uz jautājumiem par precēm. 

Alternatīvi varat iestatīt anketu tā, lai gadījumā, ja respondents 1. jautājumam atlasa atbildi A, tad anketas secībā nākamais ir 2. jautājums. Taču, ja respondents 1. jautājumam atlasa atbildi B, nākamais tiek rādīts 5. jautājums.