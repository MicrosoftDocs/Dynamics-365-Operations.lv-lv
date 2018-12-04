--- 
title: "Kreditoru parādu rēķinu salīdzināšanas pārbaudes iestatīšana"
description: "Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7a26a057b524f162e4b288b88e8c30f7c5db7a45
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Kreditoru parādu rēķinu salīdzināšanas pārbaudes iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana. Ja jūsu juridiskā persona izseko izdevumus, piemēram, pārvadāšanas izdevumus, izmantojot maksas, pārliecinieties, vai ir atlasīta konfigurācijas atslēga Izmaksas.  Parādu kreditoriem rēķinu salīdzināšana ir kreditoru rēķinu, pirkšanas pasūtījumu un produktu ieejas plūsmu informācijas salīdzināšanas process. Atšķirības starp šiem dokumentiem tiek sauktas par salīdzināšanas neatbilstībām. Salīdzināšanas neatbilstības tiek salīdzinātas ar norādītajiem tolerances līmeņiem. Ja salīdzināšanas neatbilstība pārsniedz tolerances procentuālo daļu vai summu, kreditora rēķina veidlapā un rēķinu salīdzināšanas informācijas veidlapā tiek attēlotas salīdzināšanas neatbilstību ikonas.

1. Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.
2. Noklikšķiniet uz cilnes Rēķinu validēšana.
3. Atzīmējiet vai noņemiet atzīmi izvēles rūtiņā Iespējot rēķinu salīdzināšanas pārbaudi.
    * Atlasiet, vai nepieciešama apstiprināšana pirms tā rēķina grāmatošanas, kurā ir rēķinu salīdzināšanas neatbilstība. Ja opcija ir iestatīta uz Atļaut ar brīdinājumu, tad katru reizi, kad salīdzināšanas laikā radīsies neatbilstība, kas pārsniedz toleranci, tiks attēlota vizuāla norāde. Tomēr rēķinu būs iespējams iegrāmatot. Lai kopā ar rēķinu salīdzināšanas pārbaudi izmantotu darbplūsmas, pārliecinieties, vai laukā Grāmatot rēķinu ar neatbilstībām ir iestatīta vērtība Atļaut ar brīdinājumu, kas ļaus izvairīties no tā apstiprināšanas vairākas reizes.  
    * Laukā Automātiski atjaunināt rēķina virsraksta atbilstības statusu atlasiet, vai salīdzināšanu automātiski veiks sistēma rēķina datu ievades laikā. Ieteicamais iestatījums ir Jā, ja vien nerodas datu ierakstu veiktspējas problēmas. Atspējojot automātisko atjaunināšanu sistēmas veiktspēja var kļūt ātrāka, jo rēķinu salīdzināšanas pārbaude datu ievades laikā tiks apieta. Ja opcijas vērtība tiek pārslēgta uz Nē, datu ievades darbiniekam būs manuāli jāatjaunina rēķina atbilstības statuss, lai apskatītu rēķinu salīdzināšanas pārbaudes rezultātus.  
4. Pārslēdziet sadaļas Rēķinu kopsummu salīdzināšana paplašinājumu.
5. Lai salīdzinātu faktiskās rēķina kopsummas ar paredzamajām kopsummām vai to atceltu, atzīmējiet vai noņemiet atzīmi izvēles rūtiņā Salīdzināt rēķina kopsummas.
    * Atlasiet, vai parādīt ikonu, ja rēķinu salīdzināšanas neatbilstība pārsniedz toleranci. Varat izvēlēties parādīt ikonu, ja pozitīva neatbilstība pārsniedz toleranci vai arī pozitīva vai negatīva neatbilstība pārsniedz toleranci.  
    * Piemēram, tolerance ir 5 procenti un rēķina kopsumma pirkšanas pasūtījumā ir 100,00. Tādēļ, ja rēķina kopsumma pārsniedz 105,00, tiek parādīta cenu saskaņošanas ikona. Ja atzīmējat opciju Ja vērtība ir lielāka vai mazāka par toleranci, tad ikona tiek parādīta arī tad, ja rēķina summa ir mazāka par 95,00.  
6. Ievadiet skaitli laukā Rēķina kopsummu tolerances procentu daļa.
7. Pārslēdziet sadaļas Cenas un daudzuma salīdzināšana paplašinājumu.
    * Laukā Rindas atbilstības ierobežojumi atlasiet vērtību, kas tiks izmantota par noklusējuma ierobežojumu juridiskajai personai, ar kuru strādājat. "Nav nepieciešama" nozīmē, ka nav nepieciešama atsevišķas rēķina rindas cenas salīdzināšana ar pirkšanas pasūtījuma cenu un rēķina daudzuma salīdzināšana ar pavadzīmes daudzumiem. "Divvirzienu atbilstība" nozīmē, ka rēķina rindu pārbaude ir jāveic, bet pārbaudē iesaistīti tikai pirkšanas pasūtījuma un piegādātāja rēķina dokumenti. Produktu ieejas plūsma atbilstības pārbaudēs netiek ņemta vērā. "Trīsvirzienu atbilstība" nozīmē, ka rēķinā norādītā vienības neto cena tiks salīdzināta ar pirkšanas pasūtījuma vienības neto cenu un atbilstošās produktu ieejas plūsmas daudzums tiks salīdzināts ar rēķina daudzumu.  
    * Ja izmantojat divvirzienu atbilstības vai trīsvirzienu atbilstības rindu atbilstības ierobežojumus, krājumu cenu tolerances lapā varat iestatīt cenas toleranci procentos juridiskajai personai, krājumiem un kreditoriem. Salīdzinot kreditoru rēķinus ar pirkšanas pasūtījumu informāciju, tiek meklēta lietojamā cenas tolerances procentuālā vērtība.  
8. Atlasiet opciju laukā Rindu atbilstības ierobežojumi.
    * Lai krājumam, kreditoram, kreditora un krājuma kombinācijai vai pirkšanas pasūtījuma rindai atļautu lietot cita līmeņa salīdzināšanu, atlasiet vērtību laukā Atļaut atbilstības ierobežojumu ignorēšanu. Juridiskās personas rindu atbilstības ierobežojumus iespējams ignorēt noteiktam kreditoram, krājumam vai kreditora un krājuma kombinācijai, iestatot to lapā Atbilstības ierobežojumi.  
    * Lai saskaņotu cenu kopsummas rēķinu rindu krājumiem, atlasiet vērtību laukā Salīdzināt cenu kopsummas. Šāda veida salīdzināšana ir noderīga, ja kreditors vienai pirkšanas pasūtījuma rindai nosūta vairākus rēķinus. Varat salīdzināt informāciju par katras rēķina rindas neto summas cenu un visām gaidošo un iepriekš iegrāmatoto rēķinu rindām ar neto summu, kas atbilst pirkšanas pasūtījuma rindai.  
9. Atlasiet opciju laukā Salīdzināt cenu kopsummas.
10. Ievadiet skaitli laukā Iegādes cenas kopsummas tolerance.
11. Pārslēdziet sadaļas Izmaksu salīdzināšana paplašinājumu.
12. Lai saskaņotu faktiskās maksas ar paredzētajām maksām, pamatojoties uz informāciju pirkšanas pasūtījumā, atzīmējiet izvēles rūtiņu Salīdzināt izmaksas.
13. Aizvērt lapu.


