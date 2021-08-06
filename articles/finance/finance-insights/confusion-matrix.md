---
title: Algoritmiskās mācīšanās modeļu rezultāti (priekšskatījums)
description: Šajā tēmā ir apspriestas algoritmiskās mācīšanās (AM) modeļu neskaidrību matricas, klasifikācijas problēmas un precizitāte. Mērķis ir uzlabot izpratni par AM prognozēšanas rezultātu precizitāti.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f766303f0592dec917a23339511a957fcdc940d6
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638684"
---
# <a name="results-of-machine-learning-models-preview"></a>Algoritmiskās mācīšanās modeļu rezultāti (priekšskatījums)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir apspriestas algoritmiskās mācīšanās (AM) modeļu neskaidrību matricas, klasifikācijas problēmas un precizitāte. Mērķis ir uzlabot izpratni par AM prognozēšanas rezultātu precizitāti. Mērķauditorija ietver inženierus, analītiķus un vadītājus, kuri vēlas apgūt zināšanas un prasmes datu zinātnē.

## <a name="confusion-matrix"></a>Neskaidrību matrica
Pēc tam, kad ir pārraudzīta AM problēma ir apmācīta, izmantojot vēsturiskos datus, tā tiek testēta, izmantojot datus, kas netiek izmantoti apmācību procesā. Šādā veidā varat salīdzināt apmācītā modeļa prognozes ar faktiskajām vērtībām. Neskaidrību matrica sniedz līdzekļus, lai novērtētu to, cik veiksmīga ir klasifikācijas problēma, un kur tā kļūdās (tas ir, kur tai ir "neskaidrības").

Piemēram, jūsu mērķis ir prognozēt, vai mājdzīvnieks ir suns vai kaķis, pamatojoties uz dažām fiziskajām un uzvedības pazīmēm. Ja jums ir testa datu kopa, kas satur 30 suņus un 20 kaķus, neskaidrību matrica var izskatīties līdzīgi tālāk redzamajam attēlam.

![Sugas prognozēšanas piemērs.](media/species-prediction-matrix.png)

Skaitļi zaļajās šūnās attēlo pareizās prognozes. Kā redzat, modelis pareizi prognozēja lielāku procentuālo daļu faktisko kaķu. Modeļa vispārējo precizitāti ir viegli aprēķināt. Šādā gadījumā tā ir 42 ÷ 50 vai 0,84.

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>Vairāku klašu klasifikatori neskaidrību matricā

Lielākā daļa diskusiju par neskaidrību matricu fokusēja uz binārajiem klasifikatoriem, kā tas ir iepriekšējā piemērā. Šis ir īpašs gadījums, kad var tikt apsvērtas citas metrikas, piemēram, jutība un atsaukšana.

Pēc tam tiks apsvērta klasifikācijas problēma finanšu scenārijam, kam ir trīs stāvokļi. Modelis prognozē, vai debitora rēķins tiks apmaksāts savlaicīgi, novēloti vai ļoti novēloti. Piemēram, no 100 testa rēķiniem 50 tiek apmaksāti savlaicīgi, 35 tiek apmaksāti novēloti, un 15 tiek apmaksāti ļoti novēloti. Šādā gadījumā modelis var radīt neskaidrību matricu, kas līdzinās tālāk redzamajam attēlam.

![1. modelis.](media/payment-prediction-matrix.png)]

Neskaidrību matrica sniedz ievērojami vairāk informācijas, nekā vienkārša precizitātes metrika. Tomēr to joprojām ir samērā viegli saprast. Neskaidrību matrica norāda, vai jums ir sabalansēta datu kopa, kur izvades klasēm ir līdzīgs skaits. Vairāku klašu scenārijā tā norāda, cik tālu var atšķirties prognoze, ja izvades klases ir kārtas, kā iepriekšējā piemērā par debitoru maksājumiem.

## <a name="model-accuracy"></a>Modeļa precizitāte 
Dažādām precizitātes metrikām ir priekšrocības, nosakot modeļa kvalitātes lielumu. 

Tā kā precizitāte ir vienkārša metrika, ko saprast, tā ir labs sākumpunkts, lai izskaidrotu modeli citiem cilvēkiem, it īpaši modeļa lietotājiem, kuri nav datu zinātnieki. Nav nepieciešama statistikas izpratne, lai saprastu modeļa precizitāti. Ja ir pieejama neskaidrību matrica, tā sniedz papildu ieskatu modeļa veiktspējā.

Tomēr, lai iegūtu pilnīgāku izpratni, ir jāatzīmē vairākas problēmas, kas saistītas ar precizitāti. Metrikas lietderība ir atkarīga no problēmas konteksta. Saistībā ar modeļa veiktspēju bieži rodas jautājums: "Cik labs ir modelis?" Tomēr atbilde uz šo jautājumu ne vienmēr ir vienkārša. Aplūkojiet tālāk redzamo neskaidrību matricu (2. modelis).

![Maksājuma prognozes piemērs ar lielāku paraugu.](media/payment-prediction-matrix-2.png)

Ātrs aprēķins parāda, ka šī modeļa precizitāte ir (70 + 10 + 3) ÷ 100 vai 0,83. Virspusēji šis rezultāts šķiet labāks, nekā iepriekšējā vairāku klašu modeļa (1. modeļa) rezultāts, kura precizitāte ir 0,73. Bet vai tas ir labāks?

Lai sāktu apskatīt šo jautājumu, apsveriet naiva minējuma precizitāti. Klasifikācijas problēmai vienkāršs minējums vienmēr prognozēs visbiežāko klasi. 1. modelī, šis minējums būs "savlaicīgi", un tas radīs precizitāti 0,50. Minējums 2. modelim arī būs "savlaicīgi", un tas radīs precizitāti 0,80. Tā kā naivs minējums uzlabo 1. modeli par 0,73 – 0,50 = 0,23, turpretī naivs minējums uzlabo 2. modeli par 0,83 – 0,80 = 0,03, 1. modelis ir labāks, pat ja tam ir mazāka precizitāte. Aprēķins parāda, ka efektīvam modeļa kvalitātes novērtējumam nepieciešams vairāk konteksta, nekā precizitātes vērtība.

Ir vērts pieminēt vēl vienu aspektu. Apsveriet scenāriju, kur tiek izmantots medicīnisks tests, lai noteiktu pacienta slimību. Šī ir bināras klasifikācijas problēma, kad pozitīvs rezultāts norāda, ka pacientam ir slimība. Šajā scenārijā ir jādomā par tālāk norādīto kļūdu ietekmi.

- Viltus pozitīvs, kad tests saka, ka pacientam ir slimība, bet patiesībā tā viņam nav.
- Viltus negatīvs, kad tests saka, ka pacientam nav slimības, bet patiesībā tā viņam ir.

Protams, abi kļūdu veidi ir nevēlami, bet kurš ir sliktāks? Atkal, tas ir atkarīgs no apstākļiem. Gadījumos, kad dzīvībai bīstamai slimībai nepieciešama ātra ārstēšana, prioritāte ir viltus negatīvu rezultātu samazināšanai (kam, cerams, seko papildu testi). Citās, mazāk kritiskās situācijās modeļa veidotāji tā vietā varētu samazināt viltus pozitīvos testus. Jebkurā gadījumā saprātīgs secinājums ir tāds, ka efektīvai modeļa kvalitātes noteikšanai ir jābūt pieejamai vairāk informācijai, nekā sniedz precizitātes metrika.

### <a name="recommendations"></a>Ieteikumi

Precizitāte ir svarīgs rīks saziņai ar domēna ekspertiem, kuri nepārzina statistiku. Tomēr, lai informācija būtu noderīga, ir svarīgi kopā ar precizitātes vērtību nodrošināt papildu kontekstu.

Maksājumu prognozēšanas scenārijam varat iestatīt mērķi AM modelim, kas ietver dažādas maksāšanas uzvedības faktorus. Mērķis ir tāds, ka modelim ir jāuzlabojas ar naivo minējumu, samazinot nepareizo atbilžu skaitu par vismaz 50 procentiem. Citiem vārdiem sakot, jūs vēlaties mērķa precizitāti, kas sadala atšķirības starp naivā minējuma precizitāti un 100 procentiem.

Tālāk redzamajā tabulā ir apkopoti šīs tēmas neskaidrību matricu principi.

| Modelis   | Naivais minējums | Adresāts | Modeļa precizitāte | Vai mērķis ir sasniegts?                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| 1. modelis | 0.50        | 0.75   | 0.73           | Gandrīz. Šis modelis ievērojami uzlabojas ar naivo minējumu. |
| 2. modelis | 0.80        | 0.90   | 0.83           | Nr.p.k. Ir nepieciešams uzlabojums.                              |

## <a name="classification-f1-accuracy"></a>F1 klasifikācijas precizitāte

Šīs tēmas pēdējais apsvērums ir daudz plašāks klasifikācijas AM veiktspējas mērs, kas pazīstams kā F1 precizitāte.

Pirms F1 precizitātes definēšanas, ir jāiepazīstas ar divām papildu metrikām: precizitāti un atsaukšanu. Precizitāte norāda, cik daudz no kopējā prognožu skaita, kas norādītas kā pozitīvas, ir piešķirtas pareizi. Šī metrika ir pazīstams arī kā pozitīvā prognozētā vērtība. Atsaukšana ir faktisko pozitīvo gadījumu kopskaits, kas tika prognozēti pareizi. Šī metrika ir pazīstama arī kā jutīgums.

[![Patiesie rezultāti pret nepatiesiem rezultātiem.](./media/tn-fn.png)](./media/tn-fn.png)

Neskaidrību matricā iepriekšējā attēlā šīs metrikas ir aprēķinātas tālāk norādītajā veidā.

- Precizitāte = KP ÷ (KP + VP)
- Atsaukšana = KP ÷ (KP + VN)

F1 mērs apvieno precizitāti un atsaukšanu. Rezultāts ir divu vērtību harmoniskais vidējais. Tas tiek aprēķināts tālāk norādītajā veidā.

- F1 = 2 × (precizitāte × atsaukšana) ÷ (precizitāte + atsaukšana)

Apskatīsim konkrētu piemēru. Iepriekš šajā tēmā bija piemērs ar modeli, kas prognozēja, vai dzīvnieks ir suns vai kaķis. Ilustrācija ir atkārtota šeit.

[![Sugas prognozēšanas piemērs (atkārtots).](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

Šeit ir rezultāti, ja "suns" tiek izmantots kā pozitīva atbilde.

- Precizitāte = 24 ÷ (24 + 2) = 0,9231
- Atsaukšana = 24 ÷ (24 + 6) = 0,8
- F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572

Kā redzat, F1 vērtība ir starp precizitātes un atsaukšanas vērtībām.

Lai gan F1 precizitāte nav tik viegli saprotama, tā pievieno nianses pamata precizitātes skaitlim. Tas var palīdzēt arī ar nesabalansētām datu kopām, kā tiks parādīts tālākajā diskusijā.

Šīs tēmas sadaļa [Modeļa precizitāte](#model-accuracy) salīdzināja divas tālāk norādītās neskaidrību matricas. Lai gan pirmajam modelim bija mazāka precizitāte, tas tika uzskatīts par noderīgāku, jo parādīja lielāku uzlabojumu, nekā noklusējuma minējums par savlaicīgo maksājumu.

![Maksājuma prognoze pret faktisko piemēru.](media/payment-prediction-matrix.png)

![Maksājuma prognozes piemērs ar lielāku paraugu (atkārtots).](media/payment-prediction-matrix-2.png)

Apskatīsim, kā šie divi modeļi ir salīdzināmi, ja tiek izmantots F1 rezultāts. F1 uzskaita precizitātes un atsaukšanas faktorus katram stāvoklim, un F1 makro aprēķins izrēķina vidējo aritmētisko F1 rezultātam starp stāvokļiem, lai noteiktu kopējo F1 rezultātu. Pastāv citi F1 varianti, bet vissvarīgāk ir apsvērt makro versiju, ņemot vērā vienādo apsvērumu, kas tiek dots visiem trim stāvokļiem.

Lai vienkāršotu aprēķinus, parauga datu masīvi tika veidoti, lai atbilstu faktiskajām un prognozētajām vērtībām. Šos datu masīvus izmanto sklearn metrikas bibliotēka Python, lai aprēķinātu vērtības. Rezultāts ir šāds.

| Modelis   | Naivais minējums | Precizitāte | F1 makro |
|---------|-------------|----------|----------|
| 1. modelis | 0.5         | 0.73     | 0.67     |
| 2. modelis | 0.80        | 0.83     | 0.66     |

Lai iegūtu vairāk informācijas par to, kā šis aprēķins darbojas, šeit ir sklearn.metrics klasifikācijas pārskats 1. modelim. Trīs stāvokļi: "savlaicīgi", "novēloti" un "ļoti novēloti" ir attēloti ar rindām, kas attiecīgi ir apzīmētas ar 1, 2 un 3. Vidējā makro vērtība ir tikai vidējā vērtība kolonnā "f1-rezultāts".

| &nbsp;    | precizitāte | atsaukšana   | f1-rezultāts |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

Kā liecina šie rezultāti, abiem modeļiem ir gandrīz identiski F1 makro precizitātes rādītāji. Šajā un daudzos citos gadījumos F1 precizitāte sniedz labāku modeļa iespēju indikatoru. Runājot par precizitāti, rezultātu interpretācijai nepieciešams izprast, ko ir vissvarīgāk ņemt vērā modelī.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
