---
title: Plāna tipa apskats
description: Plāna tips programmā Microsoft Dynamics 365 Human Resources ir noteikta tipa atvieglojumu augsta līmeņa grupēšana.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5d66d205d2a987310cd592a00feb10ad0dcd90e
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423348"
---
# <a name="plan-type-overview"></a>Plānot veidu pārskatu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Plāna veids ir noteikta veida atvieglojumu augsta līmeņa grupēšana. Katram plāna tipam ir plāna tipa kods, kas nosaka plāna tipa kārtulas. Piemēram, plāna tipam **Pamata dzīve** būtu plāna tipa kods **Dzīve**, jo tas ir sava veida dzīvības apdrošināšanas plāna tips, un tam jāatbilst kārtulām, kas noteiktas plāna tipa kodam **Dzīve**. Cits plāna tips varētu būt **Papildu dzīve**. Šim plāna tipam būs arī plāna tipa **Dzīve** kods.

Katrs plāna tips norāda, vai nodarbinātais var pieteikties vienā sava tipa plānā vai vairākos. Piemēram, nodarbinātais varētu pieteikties plāna tipa Dzīve politikām Pamata dzīve un Papildu dzīve. Nodarbinātajam visticamāk būs atļauts reģistrēties tikai vienā tipa Medicīna politikā.

Ja plāna tips ietver kontaktus, plāna tips norāda, vai kontaktpersonas ir saņēmēji vai pakārtotie. Piemēram, Pamata dzīves plāna veidam būtu saņēmēji, bet Pamata medicīniskā plāna veidam ir pakārtotie. Dažos gadījumos plānam var nebūt personīgu kontaktpersonu. Piemēram, elastīgu izdevumu konts vai autostāvvietas atļauja.

Plāna tips var definēt vajadzību opcijas. Vajadzību opcijas ir definētas lapā **Vajadzības opcija**. Vajadzības opcija var norādīt atvieglojumu summu vai kontaktpersonas, kas ir tiesīgas uz plāna tipu. Piemēram, ja kontaktpersonas tips ir Saņēmējs, vajadzības opcijai ir jādefinē nosacījumi, ko saņēmējs var saņemt, kad tiek izmantoti atvieglojumi. Ja kontaktpersonas tips ir Pakārtotais, vajadzības opcijai jādefinē attiecības starp pakārtoto un darbinieku. 

> [!IMPORTANT]
> Lapā ir ietverti galvenie dati, kas ietekmē opcijas, kas ir pieejamas, izveidojot jaunu atvieglojumu plānu:
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
   | **Atļaut atcelšanu** | Norāda, vai darbinieks var atcelt atvieglojumu plānu dzīves notikuma laikā. |
   | **Mainīt vajadzības opciju** | Norāda, vai darbinieks var mainīt vajadzību opcijas dzīves notikuma laikā. |
   | **Mainīt uz jaunu plānu** | Norāda, vai darbinieks var mainīt plānus dzīves notikuma laikā. |
   | **Automātiski atcelt plānu** | Tiek norādīts, vai automātiski atcelt plānu dzīves notikuma laikā. |
   | **Automātiski atkārtoti atvērt piemērotības pārbaudi** | Norāda, vai dzīves notikuma laikā automātiski atkārtoti jāatver atvieglojumu reģistrācijas atbilstības pārbaude. |
   | **Pārskata veidošanas logs** | Norāda dzīves notikuma pārskata veidošanas logu dienās. **Piezīme**: Ja neievadāt summu, sistēma pieņem, ka pārskata logs ir nulle un dzīves notikumu neapstrādās. |

5. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
