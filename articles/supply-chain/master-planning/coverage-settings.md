---
title: "Vajadzības iestatījumi"
description: "Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="99555-103">Vajadzības iestatījumi</span><span class="sxs-lookup"><span data-stu-id="99555-103">Coverage settings</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="99555-104">Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="99555-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="99555-105">Jūs varat norādīt vajadzības iestatījumus vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="99555-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="99555-106">Norādiet vajadzību grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="99555-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="99555-107">Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu.</span><span class="sxs-lookup"><span data-stu-id="99555-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="99555-108">Lai izveidotu vajadzību grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**.</span><span class="sxs-lookup"><span data-stu-id="99555-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="99555-109">Vajadzību grupu varat saistīt ar preci.</span><span class="sxs-lookup"><span data-stu-id="99555-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="99555-110">Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="99555-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="99555-111">Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** kopsavilkuma cilnē **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="99555-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="99555-112">Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota lauka **Vispārējā vajadzību grupa** vērtība, kas ir norādīta lapā **Vispārējās plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="99555-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="99555-113">Norādiet preces vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="99555-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="99555-114">Varat izveidot vajadzību iestatījumus noteiktai precei.</span><span class="sxs-lookup"><span data-stu-id="99555-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="99555-115">Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="99555-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="99555-116">Atlasiet preci lapas sadaļā **Darbību rūts**, cilnē **Plāns**, **Vajadzības grupa** un noklikšķiniet uz **Krājumu vajadzība**, lai atvērtu lapu **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="99555-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="99555-117">Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**.</span><span class="sxs-lookup"><span data-stu-id="99555-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="99555-118">Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.</span><span class="sxs-lookup"><span data-stu-id="99555-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="99555-119">Norādiet preces vajadzības iestatījumus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="99555-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="99555-120">Vednis ir pakāpeniska palīdzība primārās preces vajadzību parametru iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="99555-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="99555-121">Lapā **Krājumu vajadzība** noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību ceļvedis**.</span><span class="sxs-lookup"><span data-stu-id="99555-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="99555-122">Norādiet dimensiju grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="99555-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="99555-123">Noklikšķiniet uz <strong>Preču informācijas pārvaldība &gt; Vispārīgi &gt; Izlaistās preces</strong>.</span><span class="sxs-lookup"><span data-stu-id="99555-123">Click <strong>Product information management &gt; Common &gt; Released products</strong>.</span></span> <span data-ttu-id="99555-124">Lapas <strong>Detalizēta informācija par izlaistajām precēm **cilnes **Vispārīgi</strong> grupā <strong>Administrēšana</strong> noklikšķiniet uz saites <strong>Noliktavas dimensiju grupa</strong>.</span><span class="sxs-lookup"><span data-stu-id="99555-124">On the <strong>Released product detail **page, on the **General</strong> tab, in the <strong>Administration</strong> group, click the <strong>Storage dimension group</strong> link.</span></span> <span data-ttu-id="99555-125">Lapā <strong>Noliktavas dimensiju grupa</strong> atlasiet lauku <strong>Vajadzības plāns pa dimensijām</strong>, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā.</span><span class="sxs-lookup"><span data-stu-id="99555-125">On the <strong>Storage dimension group</strong> page, select the <strong>Coverage plan by dimension</strong> field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="99555-126">Lauks <strong>Vajadzības plāns pa dimensijām</strong> ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.</span><span class="sxs-lookup"><span data-stu-id="99555-126">All product dimensions, such as configuration, color, size, style, must have the <strong>Coverage plan by dimension</strong> field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="99555-127">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="99555-127">See also</span></span>
--------

[<span data-ttu-id="99555-128">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="99555-128">Master plans</span></span>](master-plans.md)




