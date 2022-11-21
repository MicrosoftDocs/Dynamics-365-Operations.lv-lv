---
title: Kreditoru moduļa rēķinu salīdzināšanas pārbaudes iestatīšana
description: Šajā rakstā ir sniegta informācija par to, kā iestatīt kreditoru parādu rēķinu salīdzināšanas validāciju.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c93ba4a13dee32427f33fe9f33fda5d783501a7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775331"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Iestatīt kreditoru rēķinu salīdzināšanas pārbaudi

[!include [banner](../../includes/banner.md)]

Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana. Ja jūsu juridiskā persona izseko izdevumus, piemēram, pārvadāšanas izdevumus, izmantojot maksas, pārliecinieties, vai ir atlasīta konfigurācijas atslēga Izmaksas. Parādu kreditoriem rēķinu salīdzināšana ir kreditoru rēķinu, pirkšanas pasūtījumu un produktu ieejas plūsmu informācijas salīdzināšanas process. Atšķirības starp šiem dokumentiem tiek sauktas par salīdzināšanas neatbilstībām. Salīdzināšanas neatbilstības tiek salīdzinātas ar norādītajiem tolerances līmeņiem. Ja salīdzināšanas neatbilstība pārsniedz tolerances procentuālo lielumu vai summu, lapā **Kreditora rēķins** un lapā **Rēķinu salīdzināšanas detalizēta informācija** tiek rādītas salīdzināšanas novirzes ikonas.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Noteikšana, kuru rēķinu salīdzināšanas validācija lietot
Ir pieejami četri dažādi salīdzināšanas validācijas tipi. 

- **Rindas līmeņa salīdzināšana** — visbiežāk izmantotais salīdzināšanas tips ir rindu salīdzināšana. Rindas līmeņa salīdzināšana var būt divvirzienu vai trīsvirzienu salīdzināšana. Noklusējuma rindas līmeņa salīdzināšanu juridiskajai personai var norādīt lapā **Parādu kreditoriem parametri**. Ar divvirzienu salīdzināšanu rēķinā norādītā vienības cena tiek salīdzināta ar vienības cenu pirkšanas pasūtījumā. Ar trīsvirzienu salīdzināšanu rēķinā norādītais daudzums tiek papildus salīdzināts ar atbilstošo produktu ieejas plūsmas daudzumu.
- **Rēķina kopsummu salīdzināšana** — rēķina kopsummas salīdzināt ar kopsummām pirkšanas pasūtījumā. Šis rēķinu salīdzināšanas veids ietver vismazāko detalizētību, tāpēc šo opciju varat izmantot, lai iestatītu kontroles, kas samazina laiku, kurš darbiniekiem ir nepieciešams, lai pārskatītu rēķinu salīdzināšanas informāciju. Tiek salīdzinātas sešas kopsummas, tostarp Apakšsumma, Beigu atlaide, Maksas, PVN, Noapaļošana un Rēķina summa. Sistēma validēs, vai kāda no šīm vērtībām rēķinā atšķiras no prognozētajām summām par vairāk nekā pieļaujamo novirzi.
- **Maksu salīdzināšana** — maksu informāciju (summas) rēķinā salīdzināt ar maksu informāciju (summām) pirkšanas pasūtījumā.
- **Cenu kopsummu salīdzināšana rindas vienumam** — šī tipa salīdzināšana ir noderīga uzņēmumiem, kas parasti saņem vairākus rēķinus vienai pirkšanas pasūtījuma rindai. Ja parasti saņemat tikai vienu rēķinu par katru pirkšanas pasūtījuma rindu, šī tipa salīdzināšana nav nepieciešama. Lai veiktu šo salīdzināšanu, ir jābūt iespējotai divvirzienu vai trīsvirzienu salīdzināšanai, un tā darbojas kā nepārsniedzamās neto summas validācija, pamatojoties uz tolerances procentuālajiem daudzumiem un summām. Ar šo salīdzināšanas tipu cenas informācija neto summai katrā rēķina rindā un visās gaidošajās un iepriekš iegrāmatotajās rēķinu rindās tiek salīdzināta ar neto summu atbilstošajā pirkšanas pasūtījuma rindā. Neto summa tiek noteikta ar šādu formulu: (Vienības cena * Rindas daudzums) + Rindas maksas - Rindas atlaides. Saskaņojot cenu kopsummas procentos, vērtības tiks salīdzinātas, izmantojot darījuma valūtu. Nosakot cenas kopsummu atbilstību pēc summas, sistēma salīdzina vērtības, izmantojot uzskaites valūtu.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Parametru iestatīšana rēķinu salīdzināšanas validācijas iespējošanai
1. Dodieties uz **Parādi kreditoriem > Iestatīšana > Kreditoru moduļa parametri**.
2. Atlasiet cilni **Rēķinu validēšana**.
3. Atzīmējiet izvēles rūtiņu **Iespējot rēķinu salīdzināšanas validāciju** vai noņemiet tās atzīmi.
    * Atlasiet, vai nepieciešama apstiprināšana pirms tā rēķina grāmatošanas, kurā ir rēķinu salīdzināšanas neatbilstība. Ja šī opcija ir iestatīta uz **Atļaut ar brīdinājumu**, tad katru reizi, kad rēķinu salīdzināšanas laikā neatbilstība pārsniedz toleranci, tiek parādīta vizuāla norāde. Tomēr rēķinu būs iespējams iegrāmatot. Lai kopā ar rēķinu salīdzināšanas validāciju izmantotu darbplūsmas, pārliecinieties, vai laukā **Grāmatot rēķinu ar neatbilstībām** ir iestatīta vērtība **Atļaut ar brīdinājumu**, kas ļaus izvairīties no nepieciešamības apstiprināšanu veikt vairākas reizes.  
    * **Laukā Automātiski atjaunināt rēķina galvenes atbilstības statusu** atlasiet, vai rēķina datu ievades laikā automātiski tiks veikta atbilstība. Ieteicamais iestatījums ir **Jā**, ja vien nerodas datu ierakstu veiktspējas problēmas. Atspējojot automātisko atjaunināšanu sistēmas veiktspēja var kļūt ātrāka, jo rēķinu salīdzināšanas pārbaude datu ievades laikā tiks apieta. Ja šīs opcijas vērtība ir iestatīta uz **Nē**, datu ievades darbiniekam ir manuāli jāatjaunina rēķina atbilstības statuss, lai redzētu rēķinu salīdzināšanas validācijas rezultātus.  
4. Iestatiet **Rēķinu kopsummu salīdzināšana**.
5. Atzīmējiet izvēles rūtiņu **Salīdzināt rēķinu kopsummas** vai noņemiet tās atzīmi, lai faktiskās rēķinu kopsummas salīdzinātu ar prognozētajām kopsummām.
    * Atlasiet, vai parādīt ikonu, ja rēķinu salīdzināšanas neatbilstība pārsniedz toleranci. Varat izvēlēties parādīt ikonu, ja pozitīva neatbilstība pārsniedz toleranci vai arī pozitīva vai negatīva neatbilstība pārsniedz toleranci.  
    * Piemēram, tolerance ir 5 procenti un rēķina kopsumma pirkšanas pasūtījumā ir 100,00. Tādēļ, ja rēķina kopsumma pārsniedz 105,00, tiek parādīta cenu saskaņošanas ikona. Ja atzīmējat opciju **Ja vērtība ir lielāka vai mazāka par toleranci**, tad ikona tiek parādīta arī tad, ja rēķina summa ir mazāka par 95,00.  
6. Laukā **Rēķinu kopsummu tolerance procentos** ievadiet pieņemamo procentuālo novirzi. Uzņēmumam šī vērtība ir noklusējuma vērtība. Šo vērtību noteiktiem kreditoriem var pārrakstīt, izmantojot lapu **Rēķinu kopsummu tolerances**. Informāciju par to, kā ignorēt rēķina kopsummas pielaides procentuālo vērtību konkrētam kreditoram, skatiet [šī raksta sadaļā Rēķinu kopsummu atbilstības pielaides iestatīšana kreditoriem](set-up-accounts-payable-invoice-matching-validation.md#set-up-invoice-totals-matching-tolerance-for-vendors).
7. Iestatiet **Cenu un daudzumu salīdzināšana**.
8. Laukā **Rindu salīdzināšanas politika** atlasiet vērtību, kas tiks izmantota kā noklusējuma politika juridiskajai personai, ar kuru strādājat. **Nav nepieciešams** nozīmē, ka atsevišķas rēķina rindas cenas nav nepieciešams verificēt ar pirkšanas pasūtījuma cenu un rēķina daudzumus nav nepieciešams verificēt ar pavadzīmes daudzumiem. **Divvirzienu atbilstība** nozīmē, ka rēķina rindu verificēšana ir jāveic, bet verifikācijā ir iesaistīti tikai pirkšanas pasūtījuma un piegādātāja rēķina dokumenti. Produktu ieejas plūsma atbilstības pārbaudēs netiek ņemta vērā. **Trīsvirzienu atbilstība** nozīmē, ka rēķinā norādītā vienības neto cena tiks salīdzināta ar pirkšanas pasūtījuma vienības neto cenu un atbilstošās produktu ieejas plūsmas daudzums tiks salīdzināts ar rēķina daudzumu.
9. Lai krājumam, kreditoram, kreditora un krājuma kombinācijai vai pirkšanas pasūtījuma rindai atļautu lietot cita līmeņa salīdzināšanu, atlasiet vērtību laukā **Atļaut salīdzināšanas politikas pārrakstīšanu**. Juridiskās personas rindu salīdzināšanas politiku var pārrakstīt noteiktam kreditoram, krājumam vai kreditora un krājuma kombinācijai, norādot to lapā **Salīdzināšanas politika**.
    * Ja izmantojat rindiņu atbilstības politiku Divvirzienu **atbilstība vai** Trīspusēja **atbilstība**, varat iestatīt cenu pielaides procentus savai juridiskajai personai, krājumiem un kreditoriem **lapā Krājumu cenas pielaide**. Juridiskās personas noklusējuma cenas tolerance divvirzienu un trīsvirzienu salīdzināšanai tiek iestatīta uz nulli procentu. Salīdzinot kreditoru rēķinus ar pirkšanas pasūtījumu informāciju, tiek meklēta lietojamā cenas tolerances procentuālā vērtība.   
10. Lai salīdzinātu cenu kopsummas rēķinu rindu krājumiem, atlasiet vērtību laukā **Salīdzināt cenu kopsummas**. Šāda veida salīdzināšana ir noderīga, ja kreditors vienai pirkšanas pasūtījuma rindai nosūta vairākus rēķinus. Varat salīdzināt informāciju par katras rēķina rindas neto summas cenu un visām gaidošo un iepriekš iegrāmatoto rēķinu rindām ar neto summu, kas atbilst pirkšanas pasūtījuma rindai. Opcijas tostarp ir **Nav**, **Procenti**, **Summa** vai **Procenti un summa**.
11. Laukā **Pirkšanas cenas kopsummas tolerances procenti** ievadiet jums pieņemamās novirzes procentuālo daudzumu. Šis lauks ir pieejams, ja laukā **Salīdzināt cenu kopsummas** ir iestatīta vērtība **Procenti** vai **Procenti un summa**.
12. Laukā **Pirkšanas cenas kopsummas tolerance** ievadiet summu uzskaites valūtā. Šis lauks ir pieejams, ja laukā **Salīdzināt cenu kopsummas** ir iestatīta vērtība **Summa** vai **Procenti un summa**.
13. Laukā **Rādīt cenu kopsummu salīdzināšanas ikonu** atlasiet, kad rādīt ikonu, ja rēķinu salīdzināšanas neatbilstība pārsniedz šo toleranci. Ikonu var parādīt, ja pozitīva neatbilstība pārsniedz toleranci vai arī pozitīva vai negatīva neatbilstība pārsniedz toleranci.
Piemēram, tolerance ir 5 procenti un rindas cenas kopsumma pirkšanas pasūtījumā ir 10,00. Tādēļ, ja rindas cenas kopsumma rēķinā pārsniedz 10,50, tiek parādīta cenu saskaņošanas ikona. Ja atzīmējat opciju **Ja vērtība ir lielāka vai mazāka par toleranci**, tad ikona tiek rādīta, ja rēķina rindas cenas kopsumma ir mazāka par 9,50.
13. Iestatiet **atbilstību** maksai.
14. Lai faktiskās maksas salīdzinātu ar prognozētajām maksām, pamatojoties uz informāciju pirkšanas pasūtījumā, atzīmējiet izvēles rūtiņu **Salīdzināt maksas**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Vienības cenas tolerances procentuālā daudzuma iestatīšana
Lai definētu atļauto cenas tolerances procentuālo vērtību, dodieties uz **Parādi kreditoriem > Iestatīšana > Rēķinu salīdzināšanas iestatīšana > Cenu tolerances**. Ja izmantojat rindu atbilstības politiku Divvirzienu **atbilstība vai** Trīspusēja **atbilstība**, varat iestatīt cenu pielaides procentus savai juridiskajai personai, krājumiem un kreditoriem. Salīdzinot kreditoru rēķinus ar pirkšanas pasūtījumu informāciju, tiek meklēta lietojamā cenas tolerances procentuālā vērtība. Tālāk ir norādīta meklēšanas noklusējuma secība.
* Tabula/tabula
* Tabula/grupa
* Tabula/visi
* Grupa/tabula
* Grupa/grupa
* Grupa/visi
* Visi/tabula
* Visi/grupa
* Visi/visi

Noklusējuma juridiskās personas cenu tolerance ir 0 procenti un šī cenu tolerance tiek lietota visiem krājumiem un visiem kontiem (Visi, Visi). Nevar izdzēst ierakstu noklusējuma juridiskās personas cenas pielaidei.

Pēc noklusējuma var ievadīt negatīvu cenu neatbilstību. Tomēr negatīvu skaitli nevar ievadīt kā cenu pielaides procentuālo vērtību. Lai izsekotu negatīvos cenu tolerances procentuālos lielumus, lapas **Kreditoru moduļa parametri** laukā **Rādīt vienības cenu salīdzināšanas ikonu** atlasiet **Ja vērtība ir lielāka vai mazāka par toleranci**. Pēc tam ievadiet cenu tolerances procentuālās vērtības lapā **Cenu tolerances**.

## <a name="set-up-matching-policy-override"></a>Salīdzināšanas politikas pārrakstīšanas iestatīšana

Pārejiet uz sadaļu **Kreditoru parādu > iestatīšana > rēķinu salīdzināšanas iestatīšana > saskaņošanas politika, lai definētu noklusējuma ierakstu laukā Saskaņošanas** politika **rindām** **lapā Pirkšanas pasūtījums**. Šī iestatīšana nav obligāta. Izmantojiet šo lapu, lai iestatītu divvirzienu atbilstību vai trīsvirzienu atbilstību krājumiem, kreditoriem vai krājumu un kreditoru kombinācijām. Šie ieraksti ļauj jums definēt detalizētākas salīdzināšanas politikas par juridiskās personas salīdzināšanas politiku, kuru definējāt lapā **Kreditoru moduļa parametri**. Noklusējuma juridiskās personas rindas salīdzināšanas politika attiecas uz visiem krājumiem un kreditoriem, izņemot tos, kuriem šajā lapā ir norādīta cita rindas salīdzināšanas politika.

Šajā lapā atlasiet **Salīdzināšanas politikas līmenis**. Salīdzināšanas politiku hierarhijā atlasiet līmeni, kuram iestatīt rindu salīdzināšanas politikas.

- **Krājums un kreditors** — norādiet salīdzināšanas politiku noteiktiem krājumiem, kas tiek iegādāti no noteiktiem kreditoriem.
- **Krājums** — norādiet salīdzināšanas politiku noteiktiem krājumiem, kas tiek iegādāti no jebkura kreditora, izņemot krājumus, kuri ir norādīti krājuma un kreditora līmenī.
- **Kreditors** — norādiet salīdzināšanas politiku visiem krājumiem, kas tiek iegādāti no noteiktiem kreditoriem, izņemot krājumus, kuri ir norādīti kreditora un krājuma līmeņos.
  
Lai noteiktu, kuru salīdzināšanas politiku lietot, tiek izmantota tālāk norādītā hierarhija.
  *  Krājums un kreditors
  *  Krājums
  *  Kreditors
  *  Juridiska persona
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Rēķinu kopsummu salīdzināšanas tolerances iestatīšana kreditoriem

Lai rēķinu kopsummu salīdzināšanai norādītu kreditoram raksturīgas tolerances, dodieties uz **Parādi kreditoriem > Iestatīšana > Rēķinu salīdzināšanas iestatīšana > Rēķinu kopsummu tolerances**. Salīdzināšanas aprēķinā tiek izmantots rēķinu kopsummu tolerances procentuālais daudzums no tā kreditora konta, kurš kreditora rēķinā ir norādīts kā pasūtījuma konts. Ja kreditora kontam nav norādīta pielaides procentuālā daļa rēķinu kopsummām, tiek izmantota rēķinu kopsummas pielaides procentuālā vērtība, kas juridiskajai personai ir norādīta **lapā Kreditoru parādu parametri**.

1. Lai atsevišķiem kreditoriem norādītu tolerances, kas pārraksta noklusējuma toleranci, atlasiet **Kreditora konts**.
2. Ievadiet novirzes procentuālo daļu, kuru pieņemsiet šim piegādātājam.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
