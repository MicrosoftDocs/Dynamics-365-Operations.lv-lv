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


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="20120-103">Uzlabota preču un kategorijas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="20120-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="20120-104">Šajā tēmā ir aprakstīts uzlabotais veids, kā risinājumā Dynamics 365 for Retail pārvaldīt Retail preču kategorijas un preces.</span><span class="sxs-lookup"><span data-stu-id="20120-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="20120-105">Šie uzlabojumi preču pārvaldniekiem ļauj skatīt preces rekvizītu pamata struktūru starp Retail preču hierarhiju un izlaisto preču detalizēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="20120-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="20120-106">Lai uzzinātu vairāk par Retail preču kategoriju pārvaldību, dodieties uz **Mazumtirdzniecības preču hierarhija** no darbvietas **Kategorijas un preču pārvaldība** un skatiet lapu **Mazumtirdzniecības preču kategorija** uzlaboto struktūru.</span><span class="sxs-lookup"><span data-stu-id="20120-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Darbvieta Kategorijas un preču pārvaldība](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="20120-108">Iepriekšējās versijās preču rekvizīti bija iedalīti **Pamata preces rekvizīti** un **Mazumtirdzniecības preces rekvizīti**, pamatojoties uz to piemērojamību.</span><span class="sxs-lookup"><span data-stu-id="20120-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="20120-109">**Mazumtirdzniecības preču rekvizīti** ir *globāli* atkarībā no piemērojamības jomas, kas nozīmē, ka konkrēta **mazumtirdzniecības preces rekvizīta** vērtība tika koplietota visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="20120-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="20120-110">**Pamata preces rekvizīti** tiek lietoti tikai konkrētai *juridiskajai personai*.</span><span class="sxs-lookup"><span data-stu-id="20120-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="20120-111">Citiem vārdiem sakot — attiecīgā **Pamata preces rekvizīta** vērtība dažādām juridiskajām personām var atšķirties, pamatojoties uz atsevišķajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="20120-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="20120-112">Uzlabotajā Retail preču kategorijas struktūrā preču rekvizīti tiek loģiski sadalīti, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.</span><span class="sxs-lookup"><span data-stu-id="20120-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Lauku grupēšana, pamatojoties uz to piemērojamības jomu](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="20120-114">Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanas visās juridiskajās juridiskās personās, uz varat tos pārvaldīt konkrētai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="20120-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="20120-115">Lai to izdarītu, atlasiet **Skatīt/rediģēt visām juridiskajām personām** vai **Skatīt/rediģēt konkrētai juridiskajai personai**.</span><span class="sxs-lookup"><span data-stu-id="20120-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Skata pārslēgšana starp privātpersonu un visām juridiskajām personām](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Skata pārslēgšana starp privātpersonu un visām juridiskajām personām](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="20120-118">Salīdzinājumā ar iepriekšējām versijām jaunajā Retail preču kategorijas struktūrā preču pārvaldnieks var definēt arī noklusējuma vērtības papildu preču rekvizītu kopai atsevišķu kategoriju līmenī.</span><span class="sxs-lookup"><span data-stu-id="20120-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="20120-119">Preces izveides laikā prece pārmanto šī noklusējuma preču rekvizīta vērtības, ņemot vērā to saistību ar atsevišķu kategoriju no Retail preču hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="20120-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="20120-120">Šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="20120-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="20120-121">Atlasīt rekvizītus, lai atjauninātu preces no mazumtirdzniecības preču kategorijas formas</span><span class="sxs-lookup"><span data-stu-id="20120-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="20120-122">Šo jauno uzlaboto preču rekvizītu struktūru var izmantot, lai atlasītu, kuri atjauninātie preču rekvizīti ir jāpārceļ pie saistītajām precēm.</span><span class="sxs-lookup"><span data-stu-id="20120-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Jaunais uzlabotais atjaunināto preču skats](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="20120-124">Preču pārvaldnieki šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="20120-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


