---
title: Preču kategoriju un preču pārvaldība
description: Šajā tēmā ir aprakstīts, kā preču pārvaldnieki var izmantot mazumtirdzniecības preču kategorijas, lai pārvaldītu attiecības starp Commerce preču hierarhiju un izlaisto preču detalizētu informāciju.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 89237c830109e8cb304b2547230484f15b90d875
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351301"
---
# <a name="manage-product-categories-and-products"></a>Preču kategoriju un preču pārvaldība

[!include [banner](./includes/banner.md)]

Šajā tēmā ir aprakstīts uzlabots veids, kā pārvaldīt preču kategorijas un preces programmā Dynamics 365 Commerce. Šie uzlabojumi preču pārvaldniekiem ļauj skatīt preces rekvizītu pamata struktūru, kas ir kopīga preču hierarhijai un izlaisto preču detalizētajai informācijai.

Lai uzzinātu vairāk par preču kategoriju pārvaldību, darbvietā **Kategoriju un preču pārvaldība**, atlasiet elementu **Commerce preču hierarhija**.

Pievērsiet uzmanību parādītās lapas **Commerce preču hierarhija** uzlabotajai struktūrai. Iepriekšējās programmas versijās preču rekvizīti bija iedalīti *Pamata preces rekvizītos* un *Mazumtirdzniecības preces rekvizītos*, pamatojoties uz to piemērojamību. Mazumtirdzniecības preču rekvizītu piemērojamības joma ir *globāla*. Citiem vārdiem sakot — katram attiecīgajam preces rekvizītam viena un tā pati vērtība tiek koplietota visās juridiskajās personās. Turpretim pamata preces rekvizīti tiek lietoti tikai *konkrētai juridiskajai personai*. Citiem vārdiem sakot — attiecīgā pamata preces rekvizīta vērtība dažādām juridiskajām personām var atšķirties atkarībā no katras juridiskās personas atsevišķajām biznesa prasībām.

Uzlabotajā preču kategoriju struktūrā preču rekvizīti tiek loģiski sadalīti, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.

![Lauki, kas grupēti, pamatojoties uz rekvizītu piemērojamības jomu.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanu visās juridiskās personās, un varat tos pārvaldīt konkrētai juridiskajai personai.

Lai pārvaldītu rekvizītus visām juridiskajām personām, atlasiet **Skatīt visām juridiskajām personām** (vai **Rediģēt visām juridiskajām personām**).

![Skatīt/rediģēt visām juridiskajām personām.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Lai pārvaldītu rekvizītus konkrētai juridiskajai personai, atlasiet **Skatīt konkrētai juridiskajai personai** (vai **Rediģēt konkrētai juridiskajai personai**).

![Skatīt/rediģēt konkrētai juridiskajai personai.](media/ToggleToEditForAllLegalEntities.PNG)

Turklāt uzlabotajā preču kategorijas struktūrā preču pārvaldnieks var definēt noklusējuma vērtības papildu preču rekvizītu kopai atsevišķu kategoriju līmenī. Pēc tam, izveidojot preces, tās pārmanto preču rekvizītu noklusējuma vērtības, ņemot vērā attiecīgo rekvizītu saistību ar atsevišķu kategoriju no preču hierarhijas. Šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Rekvizītu atlasīšana, lai atjauninātu preces lapā Commerce preču hierarhija

Šo jauno uzlaboto preču rekvizītu struktūru var izmantot, lai atlasītu atjauninātos preču rekvizītus, kuri jāpārceļ pie saistītajām precēm. Lapas **Commerce preču hierarhija** darbību rūtī atlasiet **Kategorija** un pēc tam atlasiet **Atjaunināt preces**, lai atvērtu dialoglodziņu **Atjaunināt preces**.

![Dialoglodziņš Atjaunināt preces.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]