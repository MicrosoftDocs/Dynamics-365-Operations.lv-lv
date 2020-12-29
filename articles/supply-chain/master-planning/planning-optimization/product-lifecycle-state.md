---
title: Neiekļaut preces, kurām ir noteikti preces dzīves cikla stāvokļi
description: Šajā tēmā skaidrots, kā izslēgt preces, pamatojoties uz to dzīves cikla stāvokli, kad tiek izmantota plānošanas optimizācijas funkcionalitāte.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645096"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="9f2c0-103">Neiekļaut preces, kurām ir noteikti preces dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="9f2c0-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f2c0-104">Izlaistās preces un izlaistās preces versijas iekļauj lauku **Preces dzīves cikla stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="9f2c0-105">Šis lauks ļauj jums cita starpā kontrolēt, kuras preces ir iekļautas vispārējā plānošanā.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="9f2c0-106">Varat pievienot, noņemt un rediģēt dzīves cikla stāvokļus, kā nepieciešams, ejot uz **Preces informācijas pārvaldība \> Iestatīšana \> Preces dzīves cikla stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="9f2c0-107">Katram preču dzīves cikla stāvoklim iestatiet opciju **Ir aktīvs plānošanai** uz *Jā*, ja preces, kurām ir šis stāvoklis, ir jāiekļauj vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="9f2c0-108">Kad opcija ir iestatīta uz *Nē*, saistītās preces un varianti tiks izslēgti no visas vispārējās plānošanas un visiem aprēķiniem materiālu komplekta (MK) līmenī.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="9f2c0-109">Izlaistās preces un varianti, kuros **Preču dzīves cikla stāvokļa** lauks ir atstāts tukšs, tiek apstrādāti tā, it kā tiem būtu preces dzīves cikla stāvoklis, kurā opcija **Ir aktīvs plānošanai** ir iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="9f2c0-110">Citiem vārdiem sakot, tās tiks iekļautas vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="9f2c0-111">Lai izvairītos no nevajadzīgiem piedāvājuma ieteikumiem, mēs iesakām jums saistīt visas novecojušās izlaistās preces un variantus ar prešu dzīves cikla stāvokli, kur opcija **Ir aktīvs plānošanai** ir iestatīta uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="9f2c0-112">Šī pieeja ir īpaši svarīga, kad strādājat ar preču konfigurācijas variantiem, kas nav atkārtoti izmantojami, jo tas palīdzēs novērst zaudējumu rašanos.</span><span class="sxs-lookup"><span data-stu-id="9f2c0-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9f2c0-113">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="9f2c0-113">Related resources</span></span>

<span data-ttu-id="9f2c0-114">Lai iegūtu vairāk informācijas par preču dzīves cikliem, skatiet [Preču dzīves cikla pārskats](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="9f2c0-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="9f2c0-115">Lai iegūtu detalizētu informāciju, kas iekļauj darbības preču dzīves ciklu izmantošanai, lai izslēgtu preces no vispārējās plānošanas un MK līmeņa aprēķiniem, skatiet [Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9f2c0-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
