---
title: Seguma iestatījumi
description: Šajā tēmā ir sniegta informācija par vajadzību iestatījumiem, kurus vispārējā plānošana izmanto, lai aprēķinātu krājumu vajadzības.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538898"
---
# <a name="coverage-settings"></a><span data-ttu-id="0adb6-103">Seguma iestatījumi</span><span class="sxs-lookup"><span data-stu-id="0adb6-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0adb6-104">Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="0adb6-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="0adb6-105">Jūs varat norādīt vajadzības iestatījumus vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="0adb6-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="0adb6-106">Norādiet vajadzību grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="0adb6-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="0adb6-107">Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu.</span><span class="sxs-lookup"><span data-stu-id="0adb6-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="0adb6-108">Lai izveidotu seguma grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="0adb6-109">Vajadzību grupu varat saistīt ar preci.</span><span class="sxs-lookup"><span data-stu-id="0adb6-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="0adb6-110">Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="0adb6-111">Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** FastTab cilnē **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="0adb6-112">Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota vispārējā vajadzību grupa, kas ir norādīta lapā **Vispārējās plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="0adb6-113">Norādiet preces vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="0adb6-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="0adb6-114">Varat izveidot vajadzību iestatījumus noteiktai precei.</span><span class="sxs-lookup"><span data-stu-id="0adb6-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="0adb6-115">Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="0adb6-116">Atlasiet preci un pēc tam lapas sadaļā Darbību rūts, cilnē **Plāns**, grupā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība** , lai atvērtu lapu **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="0adb6-117">Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="0adb6-118">Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="0adb6-119">Norādiet preces vajadzības iestatījumus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="0adb6-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="0adb6-120">Vednī soli pa solim ir izskaidrots primāro krājumu vajadzību parametru iestatīšanas process.</span><span class="sxs-lookup"><span data-stu-id="0adb6-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="0adb6-121">Lapas **Krājumu vajadzība** darbību rūtī noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību vednis**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="0adb6-122">Norādiet dimensiju grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="0adb6-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="0adb6-123">Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="0adb6-124">Lapas **Detalizēta informācija par izlaistajām precēm** FasTab cilnes **Vispārīgi** sadaļā **Administrēšana** atlasiet saiti laukā **Noliktavas izmēru grupa**.</span><span class="sxs-lookup"><span data-stu-id="0adb6-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="0adb6-125">Lapā **Noliktavas dimensiju grupas** atlasiet izvēles rūtiņu **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā.</span><span class="sxs-lookup"><span data-stu-id="0adb6-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="0adb6-126">Lauks **Vajadzības plāns pa dimensijām** ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.</span><span class="sxs-lookup"><span data-stu-id="0adb6-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0adb6-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0adb6-127">Additional resources</span></span>

[<span data-ttu-id="0adb6-128">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="0adb6-128">Master plans</span></span>](master-plans.md)
