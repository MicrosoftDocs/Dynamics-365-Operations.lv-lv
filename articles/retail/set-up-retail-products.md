---
title: "Iestatīt mazumtirdzniecības preces"
description: "Šajā rakstā ir aprakstīts, kā veikt mazumtirdzniecības preču iestatīšanu programmatūrā Microsoft Dynamics 365 for Retail"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 2be44e0000e9730aa93076f21a4204f5d56f6aac
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017

---

# <a name="set-up-retail-products"></a>Iestatīt mazumtirdzniecības preces

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīts, kā veikt mazumtirdzniecības preču iestatīšanu programmatūrā Microsoft Dynamics 365 for Retail

Lai preces varētu piedāvāt tālākpārdošanai savos mazumtirdzniecības kanālos, šīs preces ir jāizveido un jākonfigurē programmā Dynamics 365 for Retail. Modulī Mazumtirdzniecība tiek izmantotas sistēmā Dynamics 365 for Retail norādītas preces īpašības, lai preces šablonā izveidotu organizācijas līmeņa preces. Varat izveidot preces, definēt preču rekvizītus un atribūtus un piešķirt preces mazumtirdzniecības kategoriju hierarhijām. Lai padarītu preces pieejamas mazumtirdzniecības kanālos un pievienotu tās aktīvajam klāstam, preces ir jāizlaiž juridiskajām personām, ja tās ir pieejamas. Lai iestatītu preces, ko pārdodat, izmantojot mazumtirdzniecības kanālus, veiciet tālāk norādītos uzdevumus.

1.  Definējiet mazumtirdzniecības preču hierarhiju. Izmantojot kategoriju hierarhijas līdzekļus sistēmā Dynamics 365 for Retail, varat definēt mazumtirdzniecības kategoriju hierarhijas, lai grupētu un kategorizētu preces, ko izplatāt mazumtirdzniecības kanālos. Kategorijas līmenī var definēt lietotāja definētos un sistēmas atribūtus. Pēc tam visas ar kategoriju saistītās preces pārmanto šos atribūtus. Var definēt vairākas kategoriju hierarhijas, un katru preci var piešķirt vairākām hierarhijām. Taču vienā hierarhijā katru preci var piešķirt tikai vienai kategorijai.
2.  Pievienojiet preces un preču variantus preces šablonam. Preces šablonam pievienotās preces veido globālu preču sarakstu. Varat manuāli pievienot preces pa vienai vai importēt preču datus no kreditoriem.
3.  Izlaidiet preci juridiskajam personām. Mazumtirdzniecības kanālos var padarīt pieejamas tikai tās preces, kas ir izdotas juridiskām personām. Pirmo reizi definējot preci, tā tiek definēta organizācijas līmenī. Pēc tam varat atlasīt vienu vai vairākas juridiskas personas, kam izlaist preci. Pēc tam prece kļūst pieejama vairākos mazumtirdzniecības kanālos jūsu organizācijā. Varat izmantot šo funkcionalitāti, lai vienreiz izveidotu preci, vienuviet pievienotu un atjauninātu preces atribūtus un rekvizītus un pēc tam izplatītu preci savas organizācijas mazumtirdzniecības kanālos, kur tā ir pieejama.
4.  Pievienojiet preces klāstiem. Klāsts ir preču kopa, ko piedāvājat savos mazumtirdzniecības kanālos. Varat definēt vienu vai vairākus klāstus un katru preci varat piešķirt vienam vai vairākiem klāstiem. Lai piešķirtu preces mazumtirdzniecības kanāliem, jūs piešķirat klāstus šiem mazumtirdzniecības kanāliem. Kad izveidojat klāstu, varat pievienot preces, kas vēl nav izlaistas juridiskai personai. Taču, lai preces varētu padarīt pieejamas mazumtirdzniecības kanālos, šīs preces vispirms ir jāizlaiž juridiskai personai.
5.  Pievienojiet preces navigācijas hierarhijām. Lai preces varētu pārlūkot tiešsaistē vai pārdošanas punktā (POS), vispirms tās ir jākategorizē mazumtirdzniecības navigācijas hierarhijā.
6.  Pievienojiet preces katalogiem. Lai gan šī darbība nav obligāta, ja izmantojat POS, lai izmantotu tiešsaistes veikalus, precēm ir jābūt iekļautām vismaz vienā katalogā.




