---
title: "Preču kategorijas pārvaldība"
description: "Šajā tēmā ir aprakstīts, kā preču pārvaldnieki var izmantot mazumtirdzniecības preču kategorijas, lai pārvaldītu attiecības starp mazumtirdzniecības preču hierarhiju un izlaisto preču detalizētu informāciju."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2246024d7d70947690173f3d0768292abe43efd7
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="manage-retail-product-categories-and-products"></a>Mazumtirdzniecības preču kategoriju un preču pārvaldība

[!include [banner](./includes/banner.md)]

Šajā tēmā ir aprakstīts uzlabotais veids, kā risinājumā Microsoft Dynamics 365 for Retail pārvaldīt mazumtirdzniecības preču kategorijas un preces. Šie uzlabojumi preču pārvaldniekiem ļauj skatīt preces rekvizītu pamata struktūru, kas ir kopīga mazumtirdzniecības preču hierarhijai un izlaisto preču detalizētajai informācijai.

Lai uzzinātu vairāk par mazumtirdzniecības preču kategoriju pārvaldību, darbvietā **Kategoriju un preču pārvaldība**, atlasiet elementu **Mazumtirdzniecības preču hierarhija**.

Pievērsiet uzmanību parādītās lapas **Mazumtirdzniecības preču hierarhija** uzlabotajai struktūrai. Iepriekšējās Retail versijās preču rekvizīti bija iedalīti *Pamata preces rekvizītos* un *Mazumtirdzniecības preces rekvizītos*, pamatojoties uz to piemērojamību. Mazumtirdzniecības preču rekvizītu piemērojamības joma ir *globāla*. Citiem vārdiem sakot — katram attiecīgajam mazumtirdzniecības preces rekvizītam viena un tā pati vērtība tiek koplietota visās juridiskajās personās. Turpretim pamata preces rekvizīti tiek lietoti tikai *konkrētai juridiskajai personai*. Citiem vārdiem sakot — attiecīgā pamata preces rekvizīta vērtība dažādām juridiskajām personām var atšķirties atkarībā no katras juridiskās personas atsevišķajām biznesa prasībām.

Uzlabotajā mazumtirdzniecības preču kategoriju struktūrā preču rekvizīti tiek loģiski sadalīti, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.

![Lauki, kas grupēti, pamatojoties uz rekvizītu piemērojamības jomu](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanu visās juridiskās personās, un varat tos pārvaldīt konkrētai juridiskajai personai.

Lai pārvaldītu rekvizītus visām juridiskajām personām, atlasiet **Skatīt visām juridiskajām personām** (vai **Rediģēt visām juridiskajām personām**).

![Skatīt/rediģēt visām juridiskajām personām](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Lai pārvaldītu rekvizītus konkrētai juridiskajai personai, atlasiet **Skatīt konkrētai juridiskajai personai** (vai **Rediģēt konkrētai juridiskajai personai**).

![Skatīt/rediģēt konkrētai juridiskajai personai](media/ToggleToEditForAllLegalEntities.PNG)

Turklāt uzlabotajā mazumtirdzniecības preču kategorijas struktūrā preču pārvaldnieks var definēt noklusējuma vērtības papildu preču rekvizītu kopai atsevišķu kategoriju līmenī. Pēc tam, izveidojot preces, tās pārmanto preču rekvizītu noklusējuma vērtības, ņemot vērā attiecīgo rekvizītu saistību ar atsevišķu kategoriju no mazumtirdzniecības preču hierarhijas. Šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Rekvizītu atlasīšana, lai atjauninātu preces lapā Mazumtirdzniecības preču hierarhija

Šo jauno uzlaboto preču rekvizītu struktūru var izmantot, lai atlasītu atjauninātos preču rekvizītus, kuri jāpārceļ pie saistītajām precēm. Lapas **Mazumtirdzniecības preču hierarhija** darbību rūtī atlasiet **Kategorija** un pēc tam atlasiet **Atjaunināt preces**, lai atvērtu dialoglodziņu **Atjaunināt preces**.

![Dialoglodziņš Atjaunināt preces](media/NewUpdateProductsEnhancedView.PNG)


