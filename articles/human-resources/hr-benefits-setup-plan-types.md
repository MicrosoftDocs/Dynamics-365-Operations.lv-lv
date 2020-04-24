---
title: Izveidot plānu tipus
description: Plāna tips programmā Microsoft Dynamics 365 Human Resources ir noteikta tipa atvieglojumu augsta līmeņa grupēšana. Katram plāna tipam ir plāna tipa kods, kas nosaka plāna tipa kārtulas.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06a36f9f3fef54e7e06d616c9179374db4ce7115
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229698"
---
# <a name="create-plan-types"></a>Izveidot plānu tipus

Plāna tips programmā Microsoft Dynamics 365 Human Resources ir noteikta tipa atvieglojumu augsta līmeņa grupēšana. Katram plāna tipam ir plāna tipa kods, kas nosaka plāna tipa kārtulas. Piemēram, plāna tipa Pamata dzīve būtu plāna tipa kods Life, jo tas ir sava veida dzīvības apdrošināšanas plāns, un tam jāatbilst kārtulām, kas noteiktas plāna tipa kodam Life. Cits plāna tips var būt Papildu dzīve, arī ar plāna tipa kodu Life.

Katrs plāna tips norāda, vai nodarbinātais var pieteikties vienā sava tipa plānā vai vairākos. Piemēram, nodarbinātais varētu pieteikties plāna tipa Dzīve politikām Pamata dzīve un Papildu dzīve. Nodarbinātajam visticamāk būs atļauts reģistrēties tikai vienā tipa Medicīna politikā.

Ja plāna tips ietver kontaktus, plāna tips norāda, vai kontaktpersonas ir saņēmēji vai pakārtotie. Piemēram, Pamata dzīves plāna veidam būtu saņēmēji, bet Pamata medicīniskā plāna veidam ir pakārtotie. Dažos gadījumos plānam var nebūt personīgu kontaktpersonu. Piemēram, elastīgu izdevumu konts vai autostāvvietas atļauja.

Plāna tips var definēt vajadzību opcijas. Vajadzību opcijas ir definētas veidlapā Vajadzības opcija. Vajadzības opcija var norādīt atvieglojumu summu vai kontaktpersonas, kas ir tiesīgas uz plāna tipu. Piemēram, ja kontaktpersonas tips ir Saņēmējs, vajadzības opcijai ir jādefinē nosacījumi, ko saņēmējs var saņemt, kad tiek izmantoti atvieglojumi. Ja kontaktpersonas tips ir Pakārtotais, vajadzības opcijai jādefinē attiecības starp pakārtoto un darbinieku. 

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

4. Lai konfigurētu dzīves notikuma opcijas, izvēlieties **Darbības**un pēc tam atlasiet **Dzīves notikuma opcijas**. Norādiet vērtības tālāk minētajos laukos.

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
