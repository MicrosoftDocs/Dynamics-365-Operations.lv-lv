---
title: Iestatīt vēlamos uzturēšanas speciālistus
description: Šajā tēmā paskaidrots, kā uzstādīt vēlamos uzturēšanas speciālistus programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 327cda12a05ad54b310e472a652f1c822ad97142
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215336"
---
# <a name="set-up-preferred-maintenance-workers"></a>Iestatīt vēlamos uzturēšanas speciālistus

[!include [banner](../../includes/banner.md)]

 

Darba pasūtījuma plānošanas laikā jūs varat dot priekšroku tam, kuri uzturēšanas speciālisti vai speciālistu grupa ir piešķirti, lai izpildītu darba pasūtījumus. Šīs funkcionalitātes lietošana nav obligāta, taču tā var jums palīdzēt izvēlēties kvalificētāko uzturēšanas speciālistu, kurš pabeigtu darbu, pamatojoties uz speciālista prasmēm un kompetenci. Ieplānoti tiks vienīgi tie uzturēšanas speciālisti, kuri ir pieejami plānošanas laikā. Ja vēlamā uzturēšanas speciālista uzstādījums plānošanas laikā atbilst darba pasūtījumam, taču uzturēšanas speciālists ir piešķirts citiem darbiem, darba pasūtījums tiks ieplānots citam pieejamajam uzturēšanas speciālistam.

Iekams jūs varat uzstādīt vēlamos uzturēšanas speciālistus, jums ir vispirms jāuzstāda tie uzturēšanas speciālisti un speciālistu grupas. Lai uzzinātu, kā uzstādīt uzturēšanas speciālistus un speciālistu grupas, skatiet sadaļu [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Vēlamo speciālistu uzstādīšana.

Vēlamais uzturēšanas speciālists vai speciālistu grupa var būt saistīti ar vienu vai vairākiem no šiem:

- tirdzniecība  
- uzturēšanas darba tipa variantu  
- uzturēšanas darba tipu  
- uzturēšanas darba tipa kategoriju  
- aktīvs  
- līdzekļa tipu  

Jo vairāk atlašu veicat vienam un tam pašam ierakstam, jo konkrētāks būs jūsu iestatījums.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Speciālisti** > **Vēlamie uzturēšanas speciālisti**.

2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu ierakstu.

3. Sāciet ar "noklusējuma" uzturēšanas speciālista vai speciālistu grupas izveidi. Tas nozīmē, ka jūs varat izdarīt atlasi vienīgi laukos **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**. Ekrānuzņēmumā zemāk ir redzams piemērs pirmajam ierakstam, kurā kā **Vēlamā uzturēšanas speciālistu grupa** ir atlasīta "Pieprasījumi".

    [!NOTE] Noklusējuma iestatījums tiks izmantots darba pasūtījuma plānošanā, ja neviena cita specifiska kombinācija neatbilst darba pasūtījuma saturam.

4. Atkārtojiet 2. darbību, lai izveidotu jaunu ierakstu. Veiciet nepieciešamo atlasi atkarībā no vēlamā speciālista vai speciālistu grupas detalizācijas līmeņa. 

    *Piemērs:* Ekrānuzņēmumā zemāk sestais ieraksts - uzturēšanas speciālists Šons Ričardsons - ir atlasīts kā vēlamais speciālists. Viņš tiks automātiski atlasīts darba pasūtījuma plānošanas laikā, kura ietver līdzekli "CH-BP1-03-02" un uzturēšanas darba veidu "Iekārtu novērtējums", ja viņš būs pieejams plānotajā laikā.

    [!NOTE] Parasti, kad darba pasūtījuma plānošanas laikā tiek atlasīts vēlamais uzturēšanas speciālists, programma Asset Management iziet cauri visiem ierakstiem **Vēlamie uzturēšanas speciālisti**, lai pārbaudītu, vai nav iespējamas atbilstības, vienmēr pārbaudot viskonkrētāko kombināciju. Tas nozīmē, ka, ja nav atrasta atbilstība, tiek izmantots "noklusējuma" ieraksts ar atlasi vai nu laukā **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.

![1. attēls](media/02-work-order-scheduling.png)

Jūs varat arī uzstādīt *atbildīgos* uzturēšanas speciālistus, kurus var atlasīt, kad tiek izveidots uzturēšanas pieprasījums vai darba pasūtījums. Jūs varat rediģēt atlasi laukos **Visi darba pasūtījumi** un **Visi uzturēšanas pieprasījumi**, ja nepieciešams. Papildinformāciju skatiet lapā [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).

Darba pasūtījuma plānošanas laikā, tiek aprēķināti dažādi rezultāti, lai noteiktu, kuriem speciālistiem vajadzētu pabeigt darbus, kas saistīti ar darba pasūtījumu (šie rezultāti tiek uzstādīti, dodoties uz **Līdzekļu pārvaldības parametri** > **Darba pasūtījumu plānošanas** saiti). Ja divi vai vairāk vēlamie uzturēšanas speciālisti vai atbildīgie uzturēšanas speciālisti darba pasūtījuma plānošanas laikā saņem vienādu rezultātu, viens speciālists tiek atlasīts nejauši. Pretējā gadījumā darba pasūtījuma pabeigšanai vienmēr tiek piešķirts speciālists ar augstāko rezultātu.

