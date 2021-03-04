---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 14. februāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461886"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 14. februāris)

Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli kļūdu labojumi.

## <a name="changes-in-onboarding"></a>Izmaiņas pievienošanas procesā
Šajā laidienā ir ietverti nelieli kļūdu labojumi.
 
## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR 
**8.1.2146 būvējums**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Elements Darbinieka fiksētā atlīdzība nenodrošina visu ierakstu eksportēšanu
Šīs izmaiņas nodrošina, ka tagad elements **Darbinieka fiksētā atlīdzība** nodrošina visu ierakstu eksportēšanu. Šo elementu var izmantot, lai izveidotu jaunus un atjauninātu esošos darbinieku fiksētās atlīdzības ierakstus. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Darbinieka vēlamās laika zonas iestatījuma neņemšana vērā, nosakot nodarbinātības beigu datumu
Tagad, brīdī, kad darbinieks sāk vai beidz strādāt uzņēmumā, nosakot nodarbinātības beigu datumu, tiek ņemts vērā lietotāja vēlamās laika joslas iestatījums.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Lielbritānijā esošu adrešu rādīšana kā Austrumšveicē esošu programmā Analytics
Šajā laidienā ir veiktas izmaiņas, lai novērstu adrešu neatbilstību darbvietas **Personāla vadība** pārskatā Darbinieku skaits pēc atrašanās vietas.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Darba attiecību pārtraukšanas koda nenorādīšana nodarbinātā amata piešķires ierakstā, kad tiek beigta amata piešķire
Ir veiktas izmaiņas, lai brīdī, kad tiek beigta amata piešķire darbiniekam, tiktu norādīta koda Darba attiecību pārtraukšanas pamatojums noklusējuma vērtība.

### <a name="new-entity-created-for-job-compensation-levels"></a>Jauna darba atlīdzības līmeņu elementa izveide
Ir izveidots jauns datu pārvaldības struktūras (data management framework — DMF) elements. Šis elements sniedz iespēju izveidot un atjaunināt katra sistēmā definētā darba atlīdzības līmeņus, tirgus vērtības un aptauju informāciju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]