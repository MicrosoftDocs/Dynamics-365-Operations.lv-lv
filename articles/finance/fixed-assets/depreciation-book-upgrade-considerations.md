---
title: Nolietojuma grāmatas jaunināšanas pārskats
description: Šajā tēmā aprakstīta pašreizējā pamatlīdzekļu grāmatas funkcionalitāte. Šī funkcionalitāte ir balstīta uz iepriekšējās vērtības modeļa funkcionalitāti, bet ietver arī visas funkcionalitātes, kas iepriekš tika nodrošinātas tikai nolietojuma grāmatām.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c36e0ab53f8a10e81e1bed207417861066dd6917
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675156"
---
# <a name="depreciation-book-upgrade-overview"></a>Nolietojuma grāmatas jaunināšanas pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta pašreizējā pamatlīdzekļu grāmatas funkcionalitāte. Šī funkcionalitāte ir balstīta uz iepriekšējās vērtības modeļa funkcionalitāti, bet ietver arī visas funkcionalitātes, kas iepriekš tika nodrošinātas tikai nolietojuma grāmatām. Vērtības modeļa funkcionalitāte un nolietojuma grāmatas funkcionalitāte ir apvienotas vienā jēdzienā, kas tiek saukts par grāmatu. Grāmatas funkcionalitāte ļauj jums izmantot vienu lapu, pieprasījumu un pārskatu kopu visiem jūsu organizācijas pamatlīdzekļu procesiem. Šajā tēmā ir sniegtas dažas lietas, kas jāņem vērā pirms jaunināšanas. 

Jaunināšanas process jūsu esošos iestatījumus un visas pastāvošās transakcijas pārvietos uz jaunās grāmatas struktūru. Vērtību modeļi saglabāsies pašreizējā stāvokli, kā grāmata, kas grāmato Virsgrāmatā. Nolietojuma grāmatas tiks pārvietotas uz grāmatu, kurai opcija Grāmatot virsgrāmatā ir iestatīta uz Nē. Nolietojuma grāmatas žurnāla nosaukumi tiks pārvietoti uz virsgrāmatas žurnāla nosaukumu, kura grāmatošanas slānis ir iestatīts uz Nav. Nolietojuma grāmatas transakcijas tiks pārvietotas uz pamatlīdzekļu transakcijām.

Pirms palaižat datu jaunināšanu, jums ir jāsaprot abas opcijas, kas ir pieejamas nolietojuma grāmatas žurnālu rindu jaunināšanai uz transakciju dokumentiem, un numuru sēriju, kas tiks izmantota dokumentu sērijai.

1. opcija:  **Sistēmas definēta numuru sērija** — šī ir noklusējuma opcija jauninājuma veiktspējas optimizēšanai. Jauninājums neizmantos numuru sēriju struktūru, bet tās vietā dokumentiem izmantos no kopas atkarīgu pieeju. Pēc jaunināšanas tiks veidota jaunā numuru sērija, kuras **Nākamā skaitļu kopa** attiecīgi būs pamatota uz jauninātajām transakcijām. Pēc noklusējuma izmantotā numuru sērija būs formātā FADBUpgr\#\#\#\#\#\#\#\#\#. Kad izmantojot šo pieeju, formāta pielāgošanai jums ir pieejami vairāki tālāk aprakstītie parametri.

-   **Numuru sērijas kods** — kods šīs numuru sērijas identificēšanai. Šis numuru sērijas kods nevar pastāvēt, jo tas tiks izveidots ar jaunināšanu.
    -   Konstantes nosaukums: **NumberSequenceDefaultCode**
    -   Noklusējuma vērtība: “FADBUpgr”
-   **Prefikss** — konstanta virknes vērtība, kas tiks izmantota kā prefikss dokumentu numuriem.
    -   Konstantes nosaukums: **NumberSequenceDefaultParameterPrefix**
    -   Noklusējuma vērtība: “FADBUpgr”
-   **Burtciparu garums** — numuru sērijas burtciparu segmenta garums.
    -   Konstantes nosaukums: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Noklusējuma vērtība: 9
-   **Sākuma numurs** — pirmais šajā numuru sērijā izmantojamais numurs.
    -   Konstantes nosaukums: **NumberSequenceDefaultParameterStartNumber**
    -   Noklusējuma vērtība: 1

2. opcija: **Pastāvoša lietotāja definēta numuru sērija** — šī opcija jums ļauj definēt numuru sēriju, ko lietot jauninājumam. Apsveriet iespēju lietot šo opciju, ja ir nepieciešama detalizēta numuru sērijas konfigurēšana. Lai lietotu numuru sēriju, jums ir nepieciešams jauninājuma klasi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans modificēt ar tālāk norādīto informāciju.

-   **Numuru sērijas kods** — šīs numuru sērijas kods.
    -   Konstantes nosaukums: **NumberSequenceExistingCode**
    -   Noklusējuma vērtība: noklusējuma vērtības nav, tā ir jāatjaunina uz numuru sērijas kodu.
-   **Kopīga numuru sērija** — Būla vērtība, lai identificētu numuru sērijas tvērumu. Lietojiet “true” visos uzņēmumos kopīgām numuru sērijām, un lietojiet “false” no uzņēmuma atkarīgam tvērumam. Kad lietojat “false”, tad numuru sērijai ar norādīto nosaukumu ir jāpastāv ikvienā uzņēmumā, kas ietver nolietojuma grāmatas transakcijas. Kopīgās numuru sērijas pastāv katrā nodalījumā, kas ietver nolietojuma grāmatas transakcijas.
    -   Konstantes nosaukums: **NumberSequenceExistingIsShared**
    -   Noklusējuma vērtība: true

Šie parametri atrodas klases ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans sākumā. 

*// Norādiet ieteicamo dokumentu sadalījuma metodi* 
 *// true, ja vēlaties lietot pastāvošu numuru sērijas kodu* 
 *// false, ja plānojat lietot sistēmas definētu numuru sēriju (noklusējums)* const boolean NumberSequenceUseExistingCode = false;  

*// Ja lietojat metodi ar sistēmas definētu numuru sēriju, norādiet numuru sērijas parametrus.*
 *// Tiks izveidota jauna numuru sērija ar šiem parametriem.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Ja lietojat metodi ar pastāvošu numuru sēriju, norādiet pastāvošās numuru sērijas kodu.* 
 *// Pastāvošajām numuru sērijām dokumentu sadalījums darbosies pa vienai rindai.* const str NumberSequenceExistingCode = ''; *// Norādiet pastāvošās numuru sērijas koda tvērumu* 
 *// true, ja norādītā numuru sērija ir kopīga* 
 *// false, ja norādītā numuru sērija ir katram uzņēmumam sava* 
 *// Noklusējuma sistēmas definētā numuru sērija tiek izmantota, ja netiek atrasts numuru sērijas kods ar norādīto tvērumu.* const boolean NumberSequenceExistingIsShared = true; 

Kad konstantes ir modificētas, atjaunojiet projektu, kas satur šo klasi. 

Kad lietojat metodi ar sistēmas ģenerēto numuru sēriju (1. opcija), jaunināšana izmantos no kopas atkarīgo apstrādi, lai piešķirtu dokumentu numurus, kā norādīts jaunināšanas skripta parametros. Pēc piešķiršanas tiek arī izveidota jauna numuru sērija ar norādītajiem parametriem. 

Kad lietojat metodi ar lietotāja definētu pastāvošu numuru sēriju (2. opcija), tad datu jaunināšana pārbauda, vai datu bāzē katram nodalījumam un uzņēmumam ar nolietojuma grāmatas transakcijām pastāv numuru sērija ar norādīto tvērumu. Ja tā pastāv, jaunināšana izmantos apstrādi pa vienai rindai, lai piešķirtu dokumentu numurus, kā norādīts ar numuru sēriju, izmantojot numuru sērijas struktūru. Ja šī numuru sērija norādītajā tvērumā nepastāv, tad jaunināšana izmantos noklusējuma sistēmas definētas numuru sērijas metodi, lai piešķirtu dokumentu numurus, un pēc sadales izveidos jaunu numuru sēriju ar norādītajiem noklusējuma parametriem.

Ar jebkuru no šīm metodēm datu jaunināšanas skripts izmantos arī numuru sēriju laukam **Dokumentu sērija** jaunajos virsgrāmatas žurnālu nosaukumos, kas tiek izveidoti iepriekšējiem nolietojuma grāmatas žurnāla nosaukumiem.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
