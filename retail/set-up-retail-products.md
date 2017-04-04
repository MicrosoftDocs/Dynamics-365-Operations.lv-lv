---
title: "Iestatīt mazumtirdzniecības preces"
description: "Šajā rakstā aprakstīts, kā iestatīt mazumtirdzniecības produktos Microsoft Dynamics 365 operācijām - mazumtirdzniecības."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Iestatīt mazumtirdzniecības preces

Šajā rakstā aprakstīts, kā iestatīt mazumtirdzniecības produktos Microsoft Dynamics 365 operācijām - mazumtirdzniecības.

Pirms jūs varat piedāvāt produktus tālākai pārdošanai mazumtirdzniecības kanāliem, ir jāizveido un jākonfigurē produktu programmā Dynamics 365 par operācijas AX - mazumtirdzniecības. Mazumtirdzniecības izmanto produkta līdzekļus Dynamics 365 operācijām produkta pamata izveidot uzņēmuma produktiem. Varat izveidot preces, definēt preču rekvizītus un atribūtus un piešķirt preces mazumtirdzniecības kategoriju hierarhijām. Lai padarītu preces pieejamas mazumtirdzniecības kanālos un pievienotu tās aktīvajam klāstam, preces ir jāizlaiž juridiskajām personām, ja tās ir pieejamas. Lai iestatītu preces, ko pārdodat, izmantojot mazumtirdzniecības kanālus, veiciet tālāk norādītos uzdevumus.

1.  Definējiet mazumtirdzniecības preču hierarhiju. Izmantojot kategorijas hierarhijas līdzekļus Dynamics 365 operācijām, var definēt mazumtirdzniecības kategorijas hierarhijas grupu un kategoriju produktiem, kas tiek izplatīta mazumtirdzniecības kanāliem. Kategorijas līmenī var definēt lietotāja definētos un sistēmas atribūtus. Pēc tam visas ar kategoriju saistītās preces pārmanto šos atribūtus. Var definēt vairākas kategoriju hierarhijas, un katru preci var piešķirt vairākām hierarhijām. Taču vienā hierarhijā katru preci var piešķirt tikai vienai kategorijai.
2.  Pievienojiet preces un preču variantus preces šablonam. Preces šablonam pievienotās preces veido globālu preču sarakstu. Varat manuāli pievienot preces pa vienai vai importēt preču datus no kreditoriem.
3.  Izlaidiet preci juridiskajam personām. Mazumtirdzniecības kanālos var padarīt pieejamas tikai tās preces, kas ir izdotas juridiskām personām. Pirmo reizi definējot preci, tā tiek definēta organizācijas līmenī. Pēc tam varat atlasīt vienu vai vairākas juridiskas personas, kam izlaist preci. Pēc tam prece kļūst pieejama vairākos mazumtirdzniecības kanālos jūsu organizācijā. Varat izmantot šo funkcionalitāti, lai vienreiz izveidotu preci, vienuviet pievienotu un atjauninātu preces atribūtus un rekvizītus un pēc tam izplatītu preci savas organizācijas mazumtirdzniecības kanālos, kur tā ir pieejama.
4.  Pievienojiet preces klāstiem. Klāsts ir preču kopa, ko piedāvājat savos mazumtirdzniecības kanālos. Varat definēt vienu vai vairākus klāstus un katru preci varat piešķirt vienam vai vairākiem klāstiem. Lai piešķirtu preces mazumtirdzniecības kanāliem, jūs piešķirat klāstus šiem mazumtirdzniecības kanāliem. Kad izveidojat klāstu, varat pievienot preces, kas vēl nav izlaistas juridiskai personai. Taču, lai preces varētu padarīt pieejamas mazumtirdzniecības kanālos, šīs preces vispirms ir jāizlaiž juridiskai personai.
5.  Pievienot produktu navigācijas hierarhijām. Pirms produktu var pārlūkot tiešsaistē vai attiecībā uz pārdošanu (POS), tie ir kategorizēta mazumtirdzniecības navigācijas hierarhijā.
6.  Pievienot produktu katalogos. Kaut arī šis solis nav obligāts attiecībā uz POS, tiešsaistes veikali prasa produkti jāiekļauj vismaz vienu katalogu.



