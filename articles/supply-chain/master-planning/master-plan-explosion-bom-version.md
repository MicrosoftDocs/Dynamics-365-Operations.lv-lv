---
title: MK versijas izvēršana
description: Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbdfc169365cb73e13383b11efcd8983aef4bbca
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815322"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="26456-103">MK versijas izvēršana</span><span class="sxs-lookup"><span data-stu-id="26456-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26456-104">Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="26456-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="26456-105">Izvēršanas pieprasīšana materiālu komplekta (MK) versijas izveido pieprasījuma katram MK rindas krājumam noteiktā vietā, un, iespējams, konkrētajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="26456-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="26456-106">Vietai specifisku MK noteiktā noliktavā var definēt katrai MK rindai.</span><span class="sxs-lookup"><span data-stu-id="26456-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="26456-107">Turklāt par katru MK rindu, krājuma dimensiju iestatījumi nosaka, vai noliktava ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="26456-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="26456-108">Iegūtais pieprasījums par katru MK rindas vienību tad kļūst par papildu pieprasījuma izvēršana sākumpunktu.</span><span class="sxs-lookup"><span data-stu-id="26456-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="26456-109">Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="26456-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="26456-110">Vietas dimensija ir obligāta un tā ir jāievada pieprasījuma darbībā.</span><span class="sxs-lookup"><span data-stu-id="26456-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="26456-111">Vietas dimensija ir saskaņota.</span><span class="sxs-lookup"><span data-stu-id="26456-111">The site dimension is consistent.</span></span> <span data-ttu-id="26456-112">Tādēļ vieta zemāka līmeņa prasībai ir tāda pati kā vietai sākotnējā prasības darbībā.</span><span class="sxs-lookup"><span data-stu-id="26456-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="26456-113">Šis grafiks ilustrē, kā turpinās vispārējās plānošanas prasības izvēršana.</span><span class="sxs-lookup"><span data-stu-id="26456-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Pieprasīt izvēršanu, lietojot MK versiju](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="26456-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="26456-115">Additional resources</span></span>
--------

[<span data-ttu-id="26456-116">MK versijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="26456-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="26456-117">Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats</span><span class="sxs-lookup"><span data-stu-id="26456-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)



