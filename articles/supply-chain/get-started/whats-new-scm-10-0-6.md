---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Dynamics 365 Supply Chain Management 10.0.6.
author: kamaybac
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8c97e4e5544c49d2e6a13b34061abfbf50e2932a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844443"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.6. Šai versijai ir būvējuma numurs 10.0.234. Kamēr vispārējais pieejamības datums ir novembrī, jaunie līdzekļi ir pieejami pirmstermiņa izlaišanai oktobrī. Plašāku informāciju par versiju 10.0.6 skatiet [Papildu resursi](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Preču konfigurācijas modeļi V2 datu elements

Tiek izlaista "preču konfigurācijas modeļu" datu elementa otrā versija (saukta par ¨preces konfigurācijas modeļiem v2¨). Noklusējuma veidne "418 — preču konfigurācijas modeļi" ir jāiestata tā, lai tā izmantotu jauno "produktu konfigurācijas modeļu v2" datu elementu importēšanas/eksportēšanas struktūras veidnēs. Veidne netiks automātiski atjaunināta, tāpēc jums būs manuāli jāielādē veidne no noklusējuma. V2 elements eksportē vienu rindu kā atsevišķu failu pielikumā, atrisinot V1 elementa lieluma ierobežojumus. 
 
Kas ir jādara, lai veiktu šīs izmaiņas?
-    Tā kā V1 elements ir novecojis, jums vajadzētu sākt migrēt no V1 uz v2. Ja tiek izmantota veidne "418 — preču konfigurācijas modeļi", varat noklikšķināt uz pogas "ielādēt noklusējuma veidnes" un atkārtoti ielādēt veidni "418 — preču konfigurācijas modeļi"
-    Ja ir nepieciešams saglabāt saderību ar esošajām sistēmām, tagad varat turpināt lietot esošo veidni un (novecojušo) V1 elementu, līdz pārvietojat savas integrācijas uz jauno veidni. 

## <a name="feature-management-enhancements"></a>Līdzekļu pārvaldības uzlabojumi
Funkciju pārvaldība tagad ļauj pēc noklusējuma iespējot visus jaunos līdzekļus, pieprasīt apstiprinājumu, lai iespējotu līdzekli, un iespējot visus līdzekļus, kas vēl nav iespējoti. 


## <a name="purchase-agreement-responsible-party"></a>Par pirkšanas līgumu atbildīgā puse
Tagad jums ir iespēja definēt primārās un sekundārās atbildīgās personas pirkšanas līguma klasifikācijas veidlapā un iegūtajos pirkšanas līgumos.  Tas nodrošina lietotājam piekļuvi PVO, kas pārrauga līgumus.

## <a name="rfq-link-on-the-purchase-order-line"></a>RFQ saite pirkšanas pasūtījuma rindā
Varat pievienot atsauces saiti no pirkšanas pasūtījuma rindām uz atbilstošajām RFQ rindām, ko tās ir izveidojušas, ļaujot lietotājam viegli tikt nodrošinātam ar piedāvājuma pieprasījuma dokumenta pamatojumu.

## <a name="additional-resources"></a>Papildu resursi

### <a name="bug-fixes"></a>Kļūdu labojumi
Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.6, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platformas update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 ietver platformas atjauninājumu 30. Lai uzzinātu vairāk par platformas atjauninājumu 30, skatiet [Jaunumi vai izmaiņas platformas atjauninājumos 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019. gada 2. kopuma plāns
Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Pārbaudiet [Dynamics 365: 2019. gada 2. kopuma plānu](/dynamics365-release-plan/2019wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Noņemtie [vai novecojušie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) rakstā apraksta funkcijas, kas ir noņemtas vai ieplānotas izņemšanai vai nolietojumam Piegādes ķēžu pārvaldībai.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]