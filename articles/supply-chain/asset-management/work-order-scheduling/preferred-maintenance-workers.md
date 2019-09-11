---
title: Iestatīt vēlamos uzturēšanas speciālistus
description: Šajā tēmā paskaidrots, kā uzstādīt vēlamos uzturēšanas speciālistus programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887415"
---
# <a name="preferred-maintenance-workers"></a>Vēlamie uzturēšanas speciālisti

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Jūs varat dot priekšroku uzturēšanas speciālistiem, kuri ir piešķirti, lai izpildītu darba pasūtījumus darba pasūtījuma plānošanas laikā. Šīs funkcionalitātes lietošana nav obligāta, taču tā var jums palīdzēt izvēlēties kvalificētāko uzturēšanas speciālistu, kurš pabeigtu darbu, pamatojoties uz speciālista prasmēm un kompetenci. Tādējādi darba pasūtījuma plānošanas laikā tiek izmantots uzstādījums **Vēlamie uzturēšanas speciālisti**, lai noteiktu vai konkrētu uzturēšanas speciālistu vai speciālistu grupu vajadzētu ieplānot darba pasūtījumam. Ieplānoti tiks vienīgi tie uzturēšanas speciālisti, kuri ir pieejami plānošanas laikā. Ja vēlamā uzturēšanas speciālista uzstādījums plānošanas laikā atbilst darba pasūtījumam, taču uzturēšanas speciālists ir piešķirts citiem darbiem, darba pasūtījums tiks ieplānots citam uzturēšanas speciālistam, kurš ir pieejams.

Iekams jūs varat uzstādīt vēlamos uzturēšanas speciālistus, jums ir vispirms jāuzstāda tie uzturēšanas speciālisti un speciālistu grupas, kurām vajadzētu būt pieejamām atlasei. Skatiet sadaļu [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md), kurā aprakstīts, kā uzstādīt uzturēšanas speciālistus un speciālistu grupas.

## <a name="set-up-preferred-workers"></a>Vēlamo speciālistu uzstādīšana.

Vēlamais uzturēšanas speciālists vai speciālistu grupa var būt saistīti ar konkrētu

- tirdzniecība  
- uzturēšanas darba tipa variantu  
- uzturēšanas darba tipu  
- uzturēšanas darba tipa kategoriju  
- aktīvs  
- līdzekļa tipu  

vai šo atlašu kombināciju. Jo vairāk atlašu veicat vienam un tam pašam ierakstam, jo konkrētāks būs jūsu iestatījums.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Speciālisti** > **Vēlamie uzturēšanas speciālisti**.

2. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu ierakstu.

3. Vispirms izveidojiet "noklusējuma" uzturēšanas speciālista vai speciālistu grupas uzstādījumu, kuriem nav atlašu laukos, kas augstāk norādīti aizzīmju sarakstā. Tas nozīmē, ka jūs varat izdarīt atlasi vienīgi laukos **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**. Attēlā zemāk ir redzams piemērs pirmajam ierakstam, kurā kā vēlamā uzturēšanas speciālistu grupa ir atlasīta "Pieprasījumi".

>[!NOTE]
>Darba pasūtījuma plānošanas laikā tiks izmantots noklusējuma uzstādījums, ja neviena cita konkrētāka kombinācija neatbildīs darba pasūtījuma saturam darba pasūtījuma plānošanas laikā.

4. Atkārtojiet 2. darbību, lai izveidotu jaunu ierakstu. Veiciet nepieciešamo atlasi atkarībā no vēlamā speciālista vai speciālistu grupas detalizācijas līmeņa. *Piemērs:* Attēlā zemāk sestais ieraksts - uzturēšanas speciālists Šons Ričardsons - ir atlasīts kā vēlamais speciālists. Viņš tiks automātiski atlasīts darba pasūtījuma plānošanas laikā, kura ietver līdzekli "CH-BP1-03-02" un uzturēšanas darba tipu "Iekārtu novērtējums", ja viņš būs pieejams plānotajā laikā.

>[!NOTE]
>Parasti, kad darba pasūtījuma plānošanas laikā tiek atlasīts vēlamais uzturēšanas speciālists, programma Asset Management iziet cauri visiem ierakstiem **Vēlamie uzturēšanas speciālisti**, lai pārbaudītu, vai nav iespējamas atbilstības, vienmēr pārbaudot viskonkrētāko kombināciju. Tas nozīmē, ka, ja nav atrasta atbilstība, tiek izmantots "noklusējuma" ieraksts ar atlasi vai nu laukā **Vēlamā uzturēšanas speciālistu grupa** vai **Vēlamais uzturēšanas speciālists**.


![1. attēls](media/02-work-order-scheduling.png)

Jūs varat arī uzstādīt atbildīgos uzturēšanas speciālistus, kurus var atlasīt, kad tiek izveidots uzturēšanas pieprasījums vai darba pasūtījums. Laukos **Visi darba pasūtījumi** un **Visi uzturēšanas pieprasījumi** jūs varat rediģēt atlasi, ja nepieciešams. Papildinformāciju skatiet [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).

Darba pasūtījuma plānošanas laikā, tiek aprēķināti dažādi rezultāti, lai noteiktu, kuriem speciālistiem vajadzētu pabeigt darbus, kas saistīti ar darba pasūtījumu (šie rezultāti tiek uzstādīti, dodoties uz **Līdzekļu pārvaldības parametri** > **Darba pasūtījumu plānošanas** saiti). Ja divi vai vairāk vēlamie uzturēšanas speciālisti vai atbildīgie uzturēšanas speciālisti darba pasūtījuma plānošanas laikā saņem vienādu rezultātu, viens speciālists tiek atlasīts nejauši. Pretējā gadījumā darba pasūtījuma pabeigšanai vienmēr tiek piešķirts speciālists ar augstāko rezultātu.

