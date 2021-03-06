---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909333"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.6. (2019. gada novembris)

[!include [banner](../includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.6. Šai versijai ir būvējuma numurs 10.0.234. Kamēr vispārējais pieejamības datums ir novembrī, jaunie līdzekļi ir pieejami pirmstermiņa izlaišanai oktobrī. Plašāku informāciju par versiju 10.0.6 skatiet [Papildu resursi](whats-new-scm-10-0-6.md#additional-resources).

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

Tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) apraksta līdzekļus, kas ir vai ir ieplānots noņemšanai no Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda funkcija tiek noņemta no preces, izslēgšanas paziņojums tiks izziņota tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mēnešu laikā pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]