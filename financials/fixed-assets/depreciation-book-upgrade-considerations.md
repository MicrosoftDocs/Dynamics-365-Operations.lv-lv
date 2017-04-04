---
title: "Nolietojuma grāmatu jaunināšanas pārskats"
description: "Iepriekšējos laidienos, pastāvēja divi vērtēšanas jēdzieni - vērtību modeļus un nolietojuma grāmatas pamatlīdzekļiem. Programmas Microsoft Dynamics 365 for Operations versijā 1611 vērtības modeļa funkcionalitāte un nolietojuma grāmatas funkcionalitāte ir apvienotas vienā jēdzienā, kas tiek saukts par grāmatu. Šajā tēmā ir norādīts uz dažiem faktoriem, kas ir jāņem vērā, veicot jaunināšanu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Nolietojuma grāmatu jaunināšanas pārskats

Iepriekšējos laidienos, pastāvēja divi vērtēšanas jēdzieni - vērtību modeļus un nolietojuma grāmatas pamatlīdzekļiem. Programmas Microsoft Dynamics 365 for Operations versijā 1611 vērtības modeļa funkcionalitāte un nolietojuma grāmatas funkcionalitāte ir apvienotas vienā jēdzienā, kas tiek saukts par grāmatu. Šajā tēmā ir norādīts uz dažiem faktoriem, kas ir jāņem vērā, veicot jaunināšanu. 

Jaunināšanas process jūsu esošos iestatījumus un visas pastāvošās transakcijas pārvietos uz jaunās grāmatas struktūru. Vērtību modeļi saglabāsies pašreizējā stāvokli, kā grāmata, kas grāmato Virsgrāmatā. Nolietojuma grāmatas tiks pārvietotas uz grāmatu, kurai opcija **Grāmatot virsgrāmatā** ir iestatīta uz **Nē**. Nolietojuma grāmatas žurnāla nosaukumus tiks pārvietots uz Virsgrāmatas žurnāla nosaukumu ar grāmatošanas līmeni, kas iestatīts uz **nav**. Nolietojuma grāmatu darbības tiek pārvietots uz pamatlīdzekļu darbībām. 

Pirms palaižat datu jaunināšanu, jums ir jāsaprot abas opcijas, kas ir pieejamas nolietojuma grāmatas žurnālu rindu jaunināšanai uz transakciju dokumentiem, un numuru sēriju, kas tiks izmantota dokumentu sērijai. 

1. opcija: **Sistēmas definēta numuru sērija** — šī ir noklusējuma opcija jauninājuma veiktspējas optimizēšanai. Jauninājums neizmantos numuru sēriju struktūru, bet tās vietā dokumentiem izmantos no kopas atkarīgu pieeju. Pēc jaunināšanas, tiks veidots jauns numuru sērijas **nākamo skaitļu kopas** attiecīgi pamatojoties uz modernizētām darbībām. Pēc noklusējuma numuru sērija, kuru izmanto tiks FADBUpgr\#\#\#\#\#\#\#\#\# formātā. Daži parametri ir pieejami, lai pielāgotu formātu, izmantojot šo pieeju:

-   **Numuru secības kodu** – identifikācijas numuru sērijas kodu. Šo numuru sēriju nevar pastāvēt, jo tas tiks izveidots pēc jaunināšanas.
    -   Konstantes nosaukums: **NumberSequenceDefaultCode**
    -   Noklusējuma vērtība: “FADBUpgr”
-   **Prefikss** — konstanta virknes vērtība, kas tiks izmantota kā prefikss dokumentu numuriem.
    -   Konstantes nosaukums: **NumberSequenceDefaultParameterPrefix**
    -   Noklusējuma vērtība: “FADBUpgr”
-   **Burtciparu garums** — numuru sērijas burtciparu segmenta garums.
    -   Pastāvīga nosaukums: * * NumberSequenceDefaultParameterAlpanumericLength * *
    -   Noklusējuma vērtība: 9
-   **Sākuma numurs** — pirmais šajā numuru sērijā izmantojamais numurs.
    -   Pastāvīga nosaukums: * * NumberSequenceDefaultParameterStartNumber * *
    -   Noklusējuma vērtība: 1

2. variants: **esošā lietotāja definētu numuru secības** -šī iespēja ļauj definēt numuru secību, kas jāizmanto par atjaunināšanas. Apsveriet, izmantojot šo opciju, ja jums nepieciešama papildu numuru secības konfigurācijas. Lietot numuru sērijas, ir jāmodificē jaunināšanas klases ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans ar šādu informāciju:

-   **Numuru sērijas kods** — šīs numuru sērijas kods.
    -   Pastāvīga nosaukums: * * NumberSequenceExistingCode * *
    -   Noklusējuma vērtība: noklusējuma vērtības nav, tā ir jāatjaunina uz numuru sērijas kodu.
-   **Kopīga numuru sērija** — Būla vērtība, lai identificētu numuru sērijas tvērumu. Lietojiet “true” visos uzņēmumos kopīgām numuru sērijām, un lietojiet “false” no uzņēmuma atkarīgam tvērumam. Lietojot "viltus", katrs uzņēmums, kas ir norādīts nolietojuma grāmatas darbībām jābūt numura sērijai ar norādīto nosaukumu. Kopīgu numuru sērijas, kas atrodas katru nodalījumu, kurā ir norādīts nolietojuma grāmatas darbībām.
    -   Pastāvīga nosaukums: * * NumberSequenceExistingIsShared * *
    -   Noklusējuma vērtība: true

Parametrus, kas atrodas pie sākumā ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans klasē. 

*Norādīt labāka pieeja dokumentiem sadales*<ph id="t1">
</ph>*/ / taisnība, ja vēlaties lietot esošās numuru sērijas kodu*<ph id="t2">
</ph>*/ / nepatiess, ja plānojat izmantot sistēmas definēta numuru sērija (noklusējums)* Būla const NumberSequenceUseExistingCode = false;  

*Ja, izmantojot numuru sērijas sistēmas definēta pieeja, norādiet parametru numuru sērijas. *<ph id="t3">
</ph>*/ / Jauno numuru sērija tiks izveidota ar šiem parametriem.* Konst = str NumberSequenceDefaultCode = 'FADBUpgr'; konst = str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; CONST int NumberSequenceDefaultParameterAlpanumericLength = 9; CONST int NumberSequenceDefaultParameterStartNumber = 1;   

*Ja lietojat esošu skaitļu secības pieeja, norādīt esošo numuru sērijas kodu. *<ph id="t4">
</ph>*/ / Dokumenta piešķiršanu dosies pa rindai, esošās numuru sērijas.* Konst = str NumberSequenceExistingCode = '; */ / Norādītu tvērumu, esošās numuru sērijas kodu*<ph id="t5">
</ph>*/ / taisnība, ja tiek koplietota norādītās numuru secības*<ph id="t6">
</ph>*/ / nepatiess, ja vienam uzņēmumam norādītās numuru secības*<ph id="t7">
</ph>*/ / noklusējuma sistēmas definēta numuru sērijas tiks izmantots, ja numuru sērijas kods norādītais jomai nav atrasts.* const boolean NumberSequenceExistingIsShared = true; 

Kad konstantes ir modificētas, atjaunojiet projektu, kas satur šo klasi. 

Lietojot sistēmas ģenerētie numuru secības pieeja (1. risinājums), jaunināšanas izmantos kopu pamatā apstrādes piešķirt dokumenta numurus, kā precizēts jauninājums skripta parametri. Tas radīs arī jaunas numuru sērijas ar norādītajiem parametriem pēc piešķiršanas. 

Kad lietojat metodi ar lietotāja definētu pastāvošu numuru sēriju (2. opcija), tad datu jaunināšana pārbauda, vai datu bāzē katram nodalījumam un uzņēmumam ar nolietojuma grāmatas transakcijām pastāv numuru sērija ar norādīto tvērumu. Ja tā nepastāv, jaunināšanas izmantotu rindu pēc rindas apstrāde piešķirt dokumenta numurus kā norādījis numuru sērija, izmantojot numuru sērijas ietvaros. Ja numuru sērijas nepastāv norādītajā apjomā, jaunināšanas izmantos noklusējuma sistēmas definēta numuru secības pieeja, lai piešķirtu dokumentu numurus un izveidos jaunu numuru sēriju ar norādīto noklusējuma parametrus pēc piešķiršanas.

Ar jebkuru no šīm metodēm datu jaunināšanas skripts izmantos arī numuru sēriju laukam **Dokumentu sērija** jaunajos virsgrāmatas žurnālu nosaukumos, kas tiek izveidoti iepriekšējiem nolietojuma grāmatas žurnāla nosaukumiem.


