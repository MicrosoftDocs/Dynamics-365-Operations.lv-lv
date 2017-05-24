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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 208fa88153adeca029f347f240c112ee156d1a7d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="coverage-settings"></a>Vajadzības iestatījumi

[!include[banner](../includes/banner.md)]


Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības. 

Jūs varat norādīt vajadzības iestatījumus vairākos veidos:

-   Norādiet vajadzību grupas vajadzības iestatījumus. Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu. Lai izveidotu vajadzību grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**. Vajadzību grupu varat saistīt ar preci. Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**. Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** kopsavilkuma cilnē **Plāns**. Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota lauka **Vispārējā vajadzību grupa** vērtība, kas ir norādīta lapā **Vispārējās plānošanas parametri**.

-   Norādiet preces vajadzības iestatījumus. Varat izveidot vajadzību iestatījumus noteiktai precei. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Atlasiet preci lapas sadaļā **Darbību rūts**, cilnē **Plāns**, **Vajadzības grupa** un noklikšķiniet uz **Krājumu vajadzība**, lai atvērtu lapu **Krājumu vajadzība**. Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**. Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.

<!-- -->

-   Norādiet preces vajadzības iestatījumus, izmantojot vedni. Vednis ir pakāpeniska palīdzība primārās preces vajadzību parametru iestatīšanai. Lapā **Krājumu vajadzība** noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību ceļvedis**.

<!-- -->

-   Norādiet dimensiju grupas vajadzības iestatījumus. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Vispārīgi &gt; Izlaistās preces**. Lapas **Detalizēta informācija par izlaistajām precēm** cilnes **Vispārīgi**, grupā **Administrēšana** noklikšķiniet uz saites **Noliktavas dimensiju grupa**. Lapā **Noliktavas dimensiju grupa** atlasiet lauku **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā. Lauks **Vajadzības plāns pa dimensijām** ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.



<a name="see-also"></a>Skatiet arī
--------

[Vispārējie plāni](master-plans.md)



