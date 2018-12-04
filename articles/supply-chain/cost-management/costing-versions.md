---
title: Cenu versijas
description: "Šajā rakstā ir sniegta informācija par izmaksu aprēķināšanas versijām, par to uzturēšanu un datu tipiem, kurus tajās varat iekļaut. Izmaksu aprēķināšanas versijas galvenais mērķis ir iekļaut izmaksu ierakstus par krājumiem, izmaksu kategorijas un netiešo izmaksu aprēķinu formulas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb8e8193b3312a63042a44cb082a33a196cbc1be
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="costing-versions"></a>Cenu versijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par izmaksu aprēķināšanas versijām, par to uzturēšanu un datu tipiem, kurus tajās varat iekļaut. Izmaksu aprēķināšanas versijas galvenais mērķis ir iekļaut izmaksu ierakstus par krājumiem, izmaksu kategorijas un netiešo izmaksu aprēķinu formulas.

Izmaksu aprēķināšanas versija var kalpot vienam vai vairākiem nolūkiem, atkarībā no datiem, ko šī izmaksu aprēķināšanas versija ietver. Izmaksu aprēķināšanas versijas galvenais mērķis ir iekļaut izmaksu ierakstus par krājumiem, izmaksu kategorijas un netiešo izmaksu aprēķinu formulas. Izmaksu versijā var būt iekļauta standarta izmaksu ierakstu kopa vai plānoto izmaksu ierakstu kopa, kuru pamatā ir izmaksu veids, kas piešķirts izmaksu versijai.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Izmaksu aprēķināšanas versijas standarta vai plānotajām izmaksām
### <a name="standard-costs"></a>Standarta izmaksas

Izmaksu aprēķināšanas versija var atbalstīt standarta izmaksu krājuma modeli tiem krājumiem, kuru izmaksu aprēķināšanas versija satur standarta izmaksu ierakstu kopu par krājumiem un ražošanas procesiem. Izmaksu dati par ražošanas procesu tiek izteikti izmaksu kategorijās maršrutēšanas operācijām un aprēķinu formulās ražošanas papildu atbalstam.

### <a name="planned-costs"></a>Plānotās izmaksas

Izmaksu aprēķināšanas versija var ietvert plānoto izmaksu ierakstu kopu par krājumiem un ražošanas procesiem. Izmaksu aprēķināšanas versija, kas ietver plānotās izmaksas, bieži tiek lietota, lai atbalstītu izmaksu aprēķināšanas simulācijas, piemēram, simulācijas par to, kā iegādāto materiālu vai ražošanas procesu izmaksu izmaiņas ietekmē saražoto krājumu aprēķinātās maksas. Krājumu izmaksu ierakstus plānotajām izmaksām iespējams arī izmantot, lai atbalstītu faktisko izmaksu krājumu modeli, nodrošinot krājumu izmaksām sākotnējās vērtības. Šīs vērtības iekļaut plānoto izmaksu aprēķinu saražotajiem krājumiem.

## <a name="entering-costs"></a>Izmaksu ievadīšana
Izmaksu ierakstu datu pārvaldība izmaksu aprēķināšanas versijā iekļauj izmaksu ievadīšanu par iegādātajiem krājumiem un par krājumiem, kas ir pārsūtīti starp vietām. Papildu datu uzturēšana ražotājiem ietver izmaksu ievadīšanu izmaksu kategorijām, kuras ir saistītas ar maršrutēšanas operācijām, aprēķinu formulu ievadīšanu netiešajām izmaksām, kuras atspoguļo ražošanas pieskaitāmās izmaksas, kā arī izmaksu aprēķināšanu saražotajiem krājumiem. 

Krājuma izmaksu dati izmaksu versijā sastāv no viena vai vairākiem izmaksu ierakstiem katram krājumam. Kad krājuma izmaksu ieraksts tiek ievadīts pirmo reizi, tā statuss ir **Gaidošs** un tam ir plānotais spēkā stāšanās datums. Kad aktivizējat krājuma izmaksu ierakstu, šis statuss tiek atjaunināts uz **Aktīvs** un spēka stāšanās datums tiek atjaunināts uz aktivizēšanas datumu. Dažādi krājumu izmaksu ieraksti var atspoguļot dažādas vietas, spēkā stāšanās datumus vai statusus. Kad aprēķināt izmaksas saražotajiem krājumiem kādam turpmākam datumam, materiālu komplekta (MK) aprēķins izmanto izmaksu ierakstus, kuriem ir saistītais spēka stāšanās datums, neatkarīgi no tā, vai statuss ir **Gaidošs** vai **Aktīvs**. Krājuma pašreizējais aktīvais izmaksu ieraksts tiek izmantots, lai novērtētu ražošanas pasūtījuma izmaksas un novērtētu krājumu transakcijas atbilstoši standarta izmaksu aprēķināšanas krājumu modelim. Izmaksu kategoriju izmaksu ierakstu un netiešo izmaksu aprēķina formulu uzturēšana atgādina krājumu izmaksu ierakstu uzturēšanu. 

Divas bloķēšanas politikas aprēķinu versijai nosaka, vai izmaksas var tikt saglabātas un vai nepabeigtās izmaksas var tikt aktivizētas. Izmantojiet bloķēšanas politikas, lai ļautu datu uzturēšanu, un pēc tam izmantojiet tās, lai novērstu datu uzturēšanu izmaksu ierakstiem izmaksu versijā. 

Izmaksu versijā MK aprēķinu nolūkos var arī būt iekļauti dati par krājumu pārdošanas vai pirkšanas cenām.

## <a name="item-sales-prices-for-bom-calculations"></a>Krājumu pārdošanas cenas MK aprēķiniem
Galvenais iemesls, kāpēc iekļaut datus par pārdošanas cenām, ir paturēt saražoto krājumu aprēķināto pārdošanas cenu. Pēc tam aprēķināto pārdošanas cenu var analizēt, lai noteiktu, kā komponenti, maršrutēšanas operācijas un pieskaitāmās izmaksas ietekmē izmaksas un pārdošanas cenu. 

Otrs iemesls, kāpēc iekļaut datus par pārdošanas cenām, ir noteikt pārdošanas cenas ierakstus komponentu krājumiem. Pēc tam šos ierakstus var izmantot, lai aprēķinātu saražoto krājumu pārdošanas cenu. Jums vispirms ir jānosaka pārdošanas cenas modelis, kas ir iegults MK aprēķinu grupā, un šī MK aprēķinu grupa ir jāpiešķir iegādātajiem krājumiem. Pēc tam, kad veicat MK aprēķinus, kas izmanto plānotās izmaksas, atlasiet MK aprēķinu grupas izmaksu cenu modeli. 

Pretējā gadījumā pārdošanas cenu ieraksti par krājumiem tiek lietoti tikai kā atsauces informācija, neatkarīgi no tā, vai ieraksti tiek ievadīti manuāli vai aprēķināti. Aktivizējot krājuma pārdošanas cenas ierakstu, varat atjaunināt krājuma pārdošanas pamatcenu. Taču pārdošanas pamatcena nav atkarīga no vietas, un to var manuāli pārrakstīt. Krājuma pārdošanas pamatcena tiek lietota kā noklusējuma pārdošanas cena pārdošanas pasūtījumos un pārdošanas piedāvājumos.

## <a name="item-purchase-prices-for-bom-calculations"></a>Krājumu pirkšanas cenas MK aprēķiniem
Galvenais iemesls, kāpēc iespējot pirkšanas cenas datus, ir definēt pirkšanas cenas ierakstus komponentu krājumiem, lai saražoto krājumu izmaksu aprēķināšanai varētu izmantot visus ierakstus. Krājuma pirkšanas cenas ierakstus jāievada manuāli. 

Lai iespējotu pirkšanas cenas saturu, jums vispirms ir jādefinē MK aprēķinu grupa, kas ietver izmaksu cenu modeli krājuma pirkšanas cenai, un jāpiešķir MK aprēķinu grupa iegādātajiem krājumiem. Pēc tam jums ir jāizmanto izmaksu cenu modelis MK aprēķinu grupai, kad veicat MK aprēķinus, kuros tiek izmantotas plānotās izmaksas, lai aprēķinātu saražoto krājumu pārdošanas cenu. 

Pirkšanas cenu ieraksti krājumiem tiek izmantoti arī kā uzziņu informācija. Krājuma pirkšanas cenas ieraksta statusu mainot no **Gaidošs** uz **Aktīvs**, varat atjaunināt krājuma bāzes pirkšanas cenu. Taču pirkšanas pamatcena nav atkarīga no vietas, un to var manuāli pārrakstīt. Krājuma pirkšanas pamatcena tiek izmantota kā pirkšanas pasūtījumu noklusējuma pirkšanas cena.




