---
title: Plāna tipa apskats
description: Plāna tips programmā Microsoft Dynamics 365 Human Resources ir noteikta tipa atvieglojumu augsta līmeņa grupēšana.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337304"
---
# <a name="plan-type-overview"></a>Plānot veidu pārskatu

[!include [banner](../includes/preview-banner.md)]

Plāna veids ir noteikta veida atvieglojumu augsta līmeņa grupēšana. Katram plāna tipam ir plāna tipa kods, kas nosaka plāna tipa kārtulas. Piemēram, plāna tipam **Pamata dzīve** būtu plāna tipa kods **Dzīve**, jo tas ir sava veida dzīvības apdrošināšanas plāna tips, un tam jāatbilst kārtulām, kas noteiktas plāna tipa kodam **Dzīve**. Cits plāna tips varētu būt **Papildu dzīve**. Šim plāna tipam būs arī plāna tipa **Dzīve** kods.

Katrs plāna tips norāda, vai nodarbinātais var pieteikties vienā sava tipa plānā vai vairākos. Piemēram, darbinieks varētu reģistrēties plāna tipa "Dzīve" politikai **Pamata dzīve** un **Papildu dzīve**. Nodarbinātajam visticamāk būs atļauts reģistrēties tikai vienā tipa Medicīna politikā.

Ja plāna tips ietver kontaktus, plāna tips norāda, vai kontaktpersonas ir saņēmēji vai pakārtotie. Piemēram, plāna tipam **Pamata dzīve** būtu saņēmēji, bet Pamata medicīniskā plāna tipam būtu pakārtotie. Dažos gadījumos plānam var nebūt personīgu kontaktpersonu. Piemēram, elastīgu izdevumu konts vai autostāvvietas atļauja.


Plāna tips var definēt vajadzību opcijas. Vajadzības opcijas ir definētas lapā **Vajadzības opcijas**. Vajadzības opcija var norādīt atvieglojumu summu vai kontaktpersonas, kas ir tiesīgas uz plāna tipu. Piemēram, ja kontaktpersonas tips ir **Saņēmējs**, vajadzības opcijai vajadzētu definēt nosacījumus par to, ko saņēmējs var saņemt, lietojot atvieglojumu. Ja kontaktpersonas veids ir **Pakārtota**, vajadzības opcijai vajadzētu definēt relāciju starp pakārtoto un darbinieku. 

> [!IMPORTANT]
> Lapā **Plānu veidi** tiek iekļauti galvenie dati, kuri ietekmē opcijas, kuras ir pieejamas jauna ieguvumu plāna izveidnes laikā:
>
> - **Plāna tipa kods** – šis lauks ietekmē to, kas tiek rādīts cilnē **Konfigurācija**, kad tiek iestatīti faktiskie atvieglojumi.  
> - **Vienlaicīga reģistrācija** – šis lauks nosaka, vai vairākas reģistrācijas ir atļautas. (Medicīniskām plānam šis lauks parasti ir iestatīts kā **Viena reģistrācija**.)
> - **Kontaktpersonas tips** – šis lauks aktivizē pakārtoto vai saņēmēju pievienošanai plānam. Ja iestatījums ir **Nav**, darbiniekiem, kuri reģistrē atvieglojumus, nav iespējas atlasīt saņēmēju vai apgādājamo.
> - **Vajadzības opcijas** – izmantojiet šo lauku, lai saistītu vajadzību opcijas ar plāna tipiem. Tas definē vai nu personas, kuras tiks segtas ar šo plāna tipu, vai nodrošinājuma summas, kas ir pieejamas šim plāna tipam. Piemēram, varat norādīt, ka nodrošinājums medicīniskā plāna tipam būs pieejams tikai darbiniekam, darbiniekam un vienai citai personai, darbiniekam un viņu saimei.

## <a name="create-plan-types"></a>Izveidot plānu tipus

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Plānu veidi**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Plāna tips** | Unikāls nosaukums, kas identificē plāna tipu. |
   | **Apraksts** | Plāna veida apraksts. |
   | **Plāna veida kods** | No vērtību nolaižamā saraksta atlasiet plāna veida kodu. Plāna veidu kodu saraksts parāda visus plāna veidus, kurus atbalsta pašreizējā versijā. |
   | **Vienlaicīga reģistrācija** | Norāda, vai darbinieks var reģistrēties vairākos viena plāna veida atvieglojumu plānos vai tikai vienā noteikta plāna veida atvieglojumu plānā. |
   | **Kontakta tips** | Norāda personiskās kontaktpersonas lomu. Vērtības ir tukša, Pakārtotais un Saņēmējs. **Kontaktpersonas tipu** var atstāt tukšu, ja plāna veids neprasa pakārtoto vai saņēmēju, pamatojoties uz vajadzības opciju. |

4. Lai konfigurētu dzīves notikuma opcijas, izvēlieties **Darbības** un pēc tam atlasiet **Dzīves notikuma opcijas**. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Plāna tips** | Plāna veids, kuram konfigurēt dzīves notikuma opcijas. |
   | **Dzīves notikuma veida ID** | Dzīves notikuma veida ID. |
   | **Mainīt vajadzības opciju** | Norāda, vai darbinieks var mainīt vajadzību opcijas dzīves notikuma laikā. |
   | **Mainīt uz jaunu plānu** | Norāda, vai darbinieks var mainīt plānus dzīves notikuma laikā. |
   | **Automātiski atkārtoti atvērt piemērotības pārbaudi** | Norāda, vai dzīves notikuma laikā automātiski atkārtoti jāatver atvieglojumu reģistrācijas atbilstības pārbaude. |
   | **Dzīves notikuma reģistrācijas periods** | Norāda dzīves notikuma pārskata veidošanas logu dienās. **Piezīme**: Ja neievadāt summu, sistēma pieņem, ka pārskata logs ir nulle un dzīves notikumu neapstrādās. |
   | **Rediģējams tikai administratori** | Norāda, vai administratori var atcelt vai rediģēt plānu dzīves notikuma laikā. Darbinieku pašapkalpošanās darbvietā **darbinieks nevar veikt izmaiņas**. |
   | **Automātiski atcelt plānu** | Norāda, vai dzīves notikuma laikā plāns ir jāatceļ automātiski. Kad dzīves notikumu izmaiņas ir apstrādātas, **automātiskā atcelšanas plāna** opcija saglabās plāna atlasi. Tiks noņemts **tikai** statuss **Apstiprināts** vai Paņemts. Plāns paliek atlasīts. Tāpēc darbinieki, kuri neplāno plāna atlases dzīves notikuma reģistrēšanas periodā, zaudēs plāna atlasi. 

5. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
