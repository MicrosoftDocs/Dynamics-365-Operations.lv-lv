---
title: "Preču kategorijas pārvaldība"
description: "Šajā tēmā ir aprakstīts, kā preču pārvaldnieki var izmantot Retail preču kategorijas, lai pārvaldītu attiecības starp Retail preču hierarhiju un izlaisto preču detalizētu informāciju."
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
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: lv-lv
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Uzlabota preču un kategorijas pārvaldība

[!include[banner](./includes/banner.md)]

Šajā tēmā ir aprakstīts uzlabotais veids, kā risinājumā Dynamics 365 for Retail pārvaldīt Retail preču kategorijas un preces. Šie uzlabojumi preču pārvaldniekiem ļauj skatīt preces rekvizītu pamata struktūru starp Retail preču hierarhiju un izlaisto preču detalizēto informāciju.

Lai uzzinātu vairāk par Retail preču kategoriju pārvaldību, dodieties uz **Mazumtirdzniecības preču hierarhija** no darbvietas **Kategorijas un preču pārvaldība** un skatiet lapu **Mazumtirdzniecības preču kategorija** uzlaboto struktūru.

![Darbvieta Kategorijas un preču pārvaldība](media/LaunchRetailProductHierarchy.png)

Iepriekšējās versijās preču rekvizīti bija iedalīti **Pamata preces rekvizīti** un **Mazumtirdzniecības preces rekvizīti**, pamatojoties uz to piemērojamību. **Mazumtirdzniecības preču rekvizīti** ir *globāli* atkarībā no piemērojamības jomas, kas nozīmē, ka konkrēta **mazumtirdzniecības preces rekvizīta** vērtība tika koplietota visām juridiskajām personām. **Pamata preces rekvizīti** tiek lietoti tikai konkrētai *juridiskajai personai*. Citiem vārdiem sakot — attiecīgā **Pamata preces rekvizīta** vērtība dažādām juridiskajām personām var atšķirties, pamatojoties uz atsevišķajām biznesa prasībām.

Uzlabotajā Retail preču kategorijas struktūrā preču rekvizīti tiek loģiski sadalīti, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.

![Lauku grupēšana, pamatojoties uz to piemērojamības jomu](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanas visās juridiskajās juridiskās personās, uz varat tos pārvaldīt konkrētai juridiskajai personai. Lai to izdarītu, atlasiet **Skatīt/rediģēt visām juridiskajām personām** vai **Skatīt/rediģēt konkrētai juridiskajai personai**.

![Skata pārslēgšana starp privātpersonu un visām juridiskajām personām](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Skata pārslēgšana starp privātpersonu un visām juridiskajām personām](media/ToggleToEditForAllLegalEntities.PNG)  

Salīdzinājumā ar iepriekšējām versijām jaunajā Retail preču kategorijas struktūrā preču pārvaldnieks var definēt arī noklusējuma vērtības papildu preču rekvizītu kopai atsevišķu kategoriju līmenī. Preces izveides laikā prece pārmanto šī noklusējuma preču rekvizīta vērtības, ņemot vērā to saistību ar atsevišķu kategoriju no Retail preču hierarhijas. Šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Atlasīt rekvizītus, lai atjauninātu preces no mazumtirdzniecības preču kategorijas formas 
 
Šo jauno uzlaboto preču rekvizītu struktūru var izmantot, lai atlasītu, kuri atjauninātie preču rekvizīti ir jāpārceļ pie saistītajām precēm. 

![Jaunais uzlabotais atjaunināto preču skats](media/NewUpdateProductsEnhancedView.PNG) 

Preču pārvaldnieki šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.


