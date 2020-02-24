---
title: Preču kategoriju un preču pārvaldība
description: Šajā tēmā ir aprakstīts, kā preču pārvaldnieki var izmantot mazumtirdzniecības preču kategorijas, lai pārvaldītu attiecības starp Commerce preču hierarhiju un izlaisto preču detalizētu informāciju.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6e0c6a8048b5a2ef9a48495cd5e2609a1324a6e2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023252"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="18853-103">Preču kategoriju un preču pārvaldība</span><span class="sxs-lookup"><span data-stu-id="18853-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="18853-104">Šajā tēmā ir aprakstīts uzlabots veids, kā pārvaldīt preču kategorijas un preces programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18853-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="18853-105">Šie uzlabojumi preču pārvaldniekiem ļauj skatīt preces rekvizītu pamata struktūru, kas ir kopīga preču hierarhijai un izlaisto preču detalizētajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="18853-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="18853-106">Lai uzzinātu vairāk par preču kategoriju pārvaldību, darbvietā **Kategoriju un preču pārvaldība**, atlasiet elementu **Commerce preču hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="18853-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="18853-107">Pievērsiet uzmanību parādītās lapas **Commerce preču hierarhija** uzlabotajai struktūrai.</span><span class="sxs-lookup"><span data-stu-id="18853-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="18853-108">Iepriekšējās programmas versijās preču rekvizīti bija iedalīti *Pamata preces rekvizītos* un *Mazumtirdzniecības preces rekvizītos*, pamatojoties uz to piemērojamību.</span><span class="sxs-lookup"><span data-stu-id="18853-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="18853-109">Mazumtirdzniecības preču rekvizītu piemērojamības joma ir *globāla*.</span><span class="sxs-lookup"><span data-stu-id="18853-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="18853-110">Citiem vārdiem sakot — katram attiecīgajam preces rekvizītam viena un tā pati vērtība tiek koplietota visās juridiskajās personās.</span><span class="sxs-lookup"><span data-stu-id="18853-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="18853-111">Turpretim pamata preces rekvizīti tiek lietoti tikai *konkrētai juridiskajai personai*.</span><span class="sxs-lookup"><span data-stu-id="18853-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="18853-112">Citiem vārdiem sakot — attiecīgā pamata preces rekvizīta vērtība dažādām juridiskajām personām var atšķirties atkarībā no katras juridiskās personas atsevišķajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="18853-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="18853-113">Uzlabotajā preču kategoriju struktūrā preču rekvizīti tiek loģiski sadalīti, pamatojoties uz to piemērojamību grupas ietvaros, tādējādi atspoguļojot izlaisto preču detalizētās informācijas formas struktūru.</span><span class="sxs-lookup"><span data-stu-id="18853-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Lauki, kas grupēti, pamatojoties uz rekvizītu piemērojamības jomu](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="18853-115">Varat pārslēgties starp juridiskajai personai specifisku rekvizītu pārvaldīšanu visās juridiskās personās, un varat tos pārvaldīt konkrētai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="18853-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="18853-116">Lai pārvaldītu rekvizītus visām juridiskajām personām, atlasiet **Skatīt visām juridiskajām personām** (vai **Rediģēt visām juridiskajām personām**).</span><span class="sxs-lookup"><span data-stu-id="18853-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Skatīt/rediģēt visām juridiskajām personām](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="18853-118">Lai pārvaldītu rekvizītus konkrētai juridiskajai personai, atlasiet **Skatīt konkrētai juridiskajai personai** (vai **Rediģēt konkrētai juridiskajai personai**).</span><span class="sxs-lookup"><span data-stu-id="18853-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Skatīt/rediģēt konkrētai juridiskajai personai](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="18853-120">Turklāt uzlabotajā preču kategorijas struktūrā preču pārvaldnieks var definēt noklusējuma vērtības papildu preču rekvizītu kopai atsevišķu kategoriju līmenī.</span><span class="sxs-lookup"><span data-stu-id="18853-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="18853-121">Pēc tam, izveidojot preces, tās pārmanto preču rekvizītu noklusējuma vērtības, ņemot vērā attiecīgo rekvizītu saistību ar atsevišķu kategoriju no preču hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="18853-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="18853-122">Šos pārmantotos preču rekvizītus katrai precei var modificēt, lai tie atbilstu konkrētajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="18853-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="18853-123">Rekvizītu atlasīšana, lai atjauninātu preces lapā Commerce preču hierarhija</span><span class="sxs-lookup"><span data-stu-id="18853-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="18853-124">Šo jauno uzlaboto preču rekvizītu struktūru var izmantot, lai atlasītu atjauninātos preču rekvizītus, kuri jāpārceļ pie saistītajām precēm.</span><span class="sxs-lookup"><span data-stu-id="18853-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="18853-125">Lapas **Commerce preču hierarhija** darbību rūtī atlasiet **Kategorija** un pēc tam atlasiet **Atjaunināt preces**, lai atvērtu dialoglodziņu **Atjaunināt preces**.</span><span class="sxs-lookup"><span data-stu-id="18853-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialoglodziņš Atjaunināt preces](media/NewUpdateProductsEnhancedView.PNG)
