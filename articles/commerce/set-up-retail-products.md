---
title: Mazumtirdzniecības preču iestatīšana
description: Šajā rakstā ir aprakstīts, kā iestatīt preces programmā Dynamics 365 Commerce.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5c8ae2f385e2e3a4d08412d9da4ab68d50496211
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795505"
---
# <a name="set-up-retail-products"></a>Mazumtirdzniecības preču iestatīšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt preces programmā Dynamics 365 Commerce.

Lai preces varētu piedāvāt atkārtošanai pārdošanai savos komercijas kanālos, šīs preces ir jāizveido un jākonfigurē. Commerce izveido organizācijas līmeņa preces preču šablonā. Varat izveidot preces, definēt preču rekvizītus un atribūtus, un piešķirt šīs preces komercijas kategoriju hierarhijām. Lai preces padarītu pieejamas saviem kanāliem un tās pievienotu aktīvam preču klāstam, šīs preces ir jāizlaiž juridiskajām personām, kurās tās ir pieejamas. Lai iestatītu preces, ko pārdodat, izmantojot kanālus, veiciet tālāk norādītos uzdevumus.

1. **Definējiet preču hierarhiju.** Izmantojot programmā Commerce pieejamos kategoriju hierarhijas līdzekļus, varat definēt mazumtirdzniecības kategoriju hierarhijas, lai grupētu un kategorizētu preces, ko izplatāt mazumtirdzniecības kanālos. Kategorijas līmenī var definēt lietotāja definētos un sistēmas atribūtus. Pēc tam visas ar kategoriju saistītās preces pārmanto šos atribūtus. Var definēt vairākas kategoriju hierarhijas, un katru preci var piešķirt vairākām hierarhijām. Taču vienā hierarhijā katru preci var piešķirt tikai vienai kategorijai.
2. **Pievienojiet preces un preču variantus preces šablonam.** Preces šablonam pievienotās preces veido globālu preču sarakstu. Varat manuāli pievienot preces pa vienai vai importēt preču datus no kreditoriem.
3. **Izlaidiet preci juridiskajam personām.** Jūsu kanālos var padarīt pieejamas tikai tās preces, kas ir izdotas juridiskām personām. Pirmo reizi definējot preci, tā tiek definēta organizācijas līmenī. Pēc tam varat atlasīt vienu vai vairākas juridiskas personas, kam izlaist preci. Pēc tam prece kļūst pieejama vairākos kanālos jūsu organizācijā. Varat izmantot šo funkcionalitāti, lai vienreiz izveidotu preci, vienuviet pievienotu un atjauninātu preces atribūtus un rekvizītus un pēc tam izplatītu preci savas organizācijas kanālos, kur tā ir pieejama.
4. **Pievienojiet preces klāstiem.** Klāsts ir preču kopa, ko piedāvājat savos kanālos. Varat definēt vienu vai vairākus klāstus un katru preci varat piešķirt vienam vai vairākiem klāstiem. Lai piešķirtu preces kanāliem, jūs piešķirat klāstus šiem kanāliem. Kad izveidojat klāstu, varat pievienot preces, kas vēl nav izlaistas juridiskai personai. Taču, lai preces varētu padarīt pieejamas kanālos, šīs preces vispirms ir jāizlaiž juridiskai personai.
5. **Pievienojiet preces navigācijas hierarhijām.** Lai preces varētu pārlūkot tiešsaistē vai pārdošanas punktā (POS), vispirms tās ir jākategorizē Commerce navigācijas hierarhijā.
6. **Pievienojiet preces katalogiem.** Lai gan šī darbība nav obligāta, ja izmantojat POS, lai izmantotu tiešsaistes veikalus, precēm ir jābūt iekļautām vismaz vienā katalogā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]