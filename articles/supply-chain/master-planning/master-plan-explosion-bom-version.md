---
title: "MK versijas izvēršana"
description: "Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="7a3ad-103">MK versijas izvēršana</span><span class="sxs-lookup"><span data-stu-id="7a3ad-103">Explosion of a BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7a3ad-104">Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="7a3ad-105">Izvēršanas pieprasīšana materiālu komplekta (MK) versijas izveido pieprasījuma katram MK rindas krājumam noteiktā vietā, un, iespējams, konkrētajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="7a3ad-106">Vietai specifisku MK noteiktā noliktavā var definēt katrai MK rindai.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="7a3ad-107">Turklāt par katru MK rindu, krājuma dimensiju iestatījumi nosaka, vai noliktava ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="7a3ad-108">Iegūtais pieprasījums par katru MK rindas vienību tad kļūst par papildu pieprasījuma izvēršana sākumpunktu.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="7a3ad-109">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="7a3ad-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="7a3ad-110">Vietas dimensija ir obligāta un tā ir jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="7a3ad-111">Vietas dimensija ir saskaņota.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-111">The site dimension is consistent.</span></span> <span data-ttu-id="7a3ad-112">Tādēļ vieta zemāka līmeņa prasībai ir tāda pati kā vietai sākotnējā prasības darbībā.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="7a3ad-113">Šis grafiks ilustrē, kā turpinās vispārējās plānošanas prasības izvēršana.</span><span class="sxs-lookup"><span data-stu-id="7a3ad-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Pieprasīt izvēršanu, lietojot MK versiju](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="7a3ad-115">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7a3ad-115">See also</span></span>
--------

[<span data-ttu-id="7a3ad-116">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="7a3ad-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="7a3ad-117">Vispārējā plānošana un vairākvietu funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="7a3ad-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




