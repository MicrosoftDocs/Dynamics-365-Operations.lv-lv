---
title: Skaidras naudas plūsmas prognoze (priekšskatījums)
description: Šajā tēmā aprakstīta skaidras naudas plūsmas prognozēšanas spēja.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0df58d3571b124acbd1edbc6d6acdd49479c309e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990593"
---
# <a name="cash-flow-forecast-preview"></a>Skaidras naudas plūsmas prognoze (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Skaidras naudas plūsma ir izšķiroša jebkuram uzņēmumam. Pat rentabli uzņēmumi var saskarties ar maksātnespēju, ja tie neuztur skaidras naudas plūsmu, lai apmierinātu tūlītējās vajadzības. Skaidras naudas plūsmas prognozēšanas spēja Finanšu ieskatos var palīdzēt uzņēmumiem efektīvi pārraudzīt un pārvaldīt savas skaidrās naudas bilances. Šis līdzeklis izmanto algoritmisko mācīšanos, lai palīdzētu uzņēmumiem prognozēt skaidras naudas plūsmas precīzāk kā iepriekš. Tas var arī palīdzēt vadītājiem pieņemt lēmumus, kas optimizē iespējas saistībā ar to pašreizējo skaidras naudas pozīciju. 

Lielākajai daļai uzņēmumu skaidras naudas plūsmas pārvaldība un skaidras naudas plūsmas prognozēšana ir nogurdinošs, monotons un manuāls process. Lielākā daļa uzņēmumu paļaujas uz Microsoft Excel risinājumiem, kam ir dažādas sarežģītības pakāpes. Skaidras naudas plūsmas precīzas prognozēšanas izaicinājumi ietver tālāk norādīto.

- Dati nav pieejami lēmumu pieņēmējiem, jo tie ir izkaisīti vairākās vietās, tostarp: 
  - Uzskaites vai uzņēmuma resursu plānošanas sistēmā
  - Finanšu plānošanas programmatūrā
  - Excel
  - Papildu programmatūras lietojumprogrammās 
- Prognozēšanas pamatā ir iekšējās zināšanas, kas atrodas "tvertnēs" katra domēna vai nodaļas ietvaros.
- Skaidras naudas plūsmas prognozes precizitātes mērīšana pēc realizētajām finanšu darbībām ir neskaidra un sarežģīta.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Detalizēta informācija par skaidras naudas plūsmas prognozes iespēju
Skaidras naudas plūsmas prognožu līdzeklī ir ietverta tālāk norādītā funkcionalitāte. 

- Atvieglo skaidras naudas plūsmas datu integrēšanu no ārējām sistēmām uz Dynamics 365 Finance. Skaidras naudas plūsmas prognozes var izmantot arī datu importēšanas un eksportēšanas struktūru. Šī struktūra atvieglo integrāciju ar Excel OData. Varat arī apvienot datus no vairākiem avotiem, lai izveidotu visaptverošu skaidras naudas plūsmas risinājumu. 

- Iepazīstina ar programmējamo skaidras naudas pozīciju. Skaidras naudas pozīcija ir veidota, pamatojoties uz debitora maksāšanas uzvedību, lai prognozētu, kad uzņēmums var sagaidīt skaidras naudas ienākšanu savos kontos. Tā analizē arī maksājošo pārdevēju vēsturisko uzvedības veidu, lai prognozētu, kad visticamāk tiks apmaksāti nākotnes rēķini un pasūtījumi. 

- Iepazīstina ar programmējamo skaidras naudas plūsmas prognozēšanu ilgtermiņa prognozēšanai, lietojot laika sēriju prognozēšanu, izmantojot automatizēto integrāciju ar AI Builder.

- Nodrošina spēju saglabāt specifisku skaidras naudas plūsmas pozīciju vai prognozes, rediģēt tās un pēc tam viegli salīdzināt un izmērīt prognozēto veiktspēju ar faktiskajiem finanšu rādītājiem.

- Iespējo iespēju analīzi, izmantojot momentuzņēmumu salīdzināšanu. Piemēram, varat izveidot vairākus momentuzņēmumus, kas attēlo optimistisku, pesimistisku un visreālāko jūsu skaidras naudas plūsmas skatu, un pēc tam salīdzināt un skatīt atšķirības.

- Nodrošina spēju skatīt skaidras naudas plūsmas prognozi vairākās valūtās, starp juridiskām personām, ka arī filtrēt un skatīt skaidras naudas plūsmu bankas kontā. 

- Ļauj filtrēt un skatīt bankas kontus, kas ir saistīti ar finanšu dimensijām.

Skaidras naudas plūsmas prognozēšanas funkcionalitāte Dynamics 365 Finance dos jūsu organizācijai iespēju pārveidot garlaicīgu, sarežģītu, tomēr atkārtojošos skaidras naudas plūsmas projekciju vienkāršā, automatizētā procesā. Visnogurdinošāko skaidras naudas plūsmas prognozēšanas aspektu automatizācija ļaus jums koncentrēties uz kritisku lēmumu pieņemšanu, lai varētu vadīt vēlamos biznesa rezultātus.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Skaidras naudas plūsmas prognozēšanas dimensiju iestatīšana
Jauna cilne lapā **Skaidras naudas plūsmas prognozes iestatīšana** ļauj kontrolēt, kādas finanšu dimensijas izmantot filtrēšanai darbvietā **Skaidras naudas plūsmas prognozēšana**. Šī cilne parādīsies tikai tad, ja ir iespējots skaidras naudas plūsmas prognozēšanas līdzeklis. 

Cilnē **Dimensijas** izvēlieties no dimensiju saraksta, ko izmantot filtrēšanai, un izmantojiet bulttaustiņus, lai pārvietotu tās uz kolonnu labajā pusē. Skaidras naudas plūsmas prognozēšanas datu filtrēšanai varat atlasīt tikai divas dimensijas. 

#### <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]