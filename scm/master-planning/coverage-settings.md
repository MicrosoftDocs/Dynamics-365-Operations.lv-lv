---
title: "Vajadzības iestatījumi"
description: "Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Vajadzības iestatījumi

Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības. 

Jūs varat norādīt vajadzības iestatījumus vairākos veidos:

-   Norādiet vajadzību grupas vajadzības iestatījumus. Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu. Noklikšķiniet uz **vispārējā plānošana &gt;Setup &gt;vajadzību &gt;Coverage groups**, lai izveidotu vajadzību grupu. Vajadzību grupu varat saistīt ar preci. Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**. Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** kopsavilkuma cilnē **Plāns**. Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota lauka **Vispārējā vajadzību grupa** vērtība, kas ir norādīta lapā **Vispārējās plānošanas parametri**.

-   Norādiet preces vajadzības iestatījumus. Varat izveidot vajadzību iestatījumus noteiktai precei. Noklikšķiniet uz **produkta informācijas pārvaldības &gt;produkti &gt;atbrīvo produktus**. Izvēlēties produktu, par **darbību rūti**, **plāns** cilni, jo **vajadzību grupu**, noklikšķiniet uz **krājumu vajadzība** atvērt **krājumu vajadzība** lapu. Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**. Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.

<!-- -->

-   Norādiet preces vajadzības iestatījumus, izmantojot vedni. Vednis ir pakāpeniska palīdzība primārās preces vajadzību parametru iestatīšanai. Lapā **Krājumu vajadzība** noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību ceļvedis**.

<!-- -->

-   Norādiet dimensiju grupas vajadzības iestatījumus. Noklikšķiniet uz **produkta informācijas pārvaldības &gt;kopējo &gt;atbrīvo produktus**. Uz * * atbrīvo produkta detaļas * * lapa, no **vispārējā** cilni, jo **administrācija** grupu, noklikšķiniet uz **glabāšanas dimensiju grupu** saiti. Lapā **Noliktavas dimensiju grupa** atlasiet lauku **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā. Visu produktu dimensijas, piemēram, konfigurācijas, krāsu, izmērus, stilu, ir jābūt **vajadzības plāns pa dimensijām** atlasītais lauks.



<a name="see-also"></a>Skatiet arī
--------

[Master plans](master-plans.md)


