---
title: Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām
description: Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269548"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="068d3-103">Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām</span><span class="sxs-lookup"><span data-stu-id="068d3-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="068d3-104">Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="068d3-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="068d3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="068d3-105">Overview</span></span>

<span data-ttu-id="068d3-106">Ja pieprasījums ir neveiksmīgs, serveris izdod HTTP statusa koda kļūdas atbildes.</span><span class="sxs-lookup"><span data-stu-id="068d3-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="068d3-107">404 statusa kods tiek iegūts un atgriezts, ja lapa netiek atrasta, un 500 statusa kods tiek iegūts un atgriezts servera kļūdas gadījumā.</span><span class="sxs-lookup"><span data-stu-id="068d3-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="068d3-108">Lietojumprogrammā Dynamics 365 Commerce lietotāji var izveidot pielāgotas statusa koda kļūdas atbilžu lapas, kas tiek rādītas lietotājiem saistībā ar šīm statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="068d3-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="068d3-109">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="068d3-109">Build a status code error response page</span></span>

<span data-ttu-id="068d3-110">Lai sāktu statusa koda kļūdas atbildes lapas izveidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="068d3-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="068d3-111">Vēlamajā tīmekļa pārlūkā pierakstieties programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="068d3-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="068d3-112">Atlasiet vietni, kurai vēlaties izveidot 4xx/5xx statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="068d3-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="068d3-113">Veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="068d3-113">Build the template</span></span>

<span data-ttu-id="068d3-114">Lai izveidotu veidni statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="068d3-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="068d3-115">Dodieties uz **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="068d3-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="068d3-116">Atlasiet **Jauns**, lai izveidotu lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="068d3-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="068d3-117">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet jaunās veidnes nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="068d3-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="068d3-118">Izveidojiet veidni, pamatojoties uz struktūru, ko vēlaties izmantot statusa koda kļūdas atbildes lapā.</span><span class="sxs-lookup"><span data-stu-id="068d3-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="068d3-119">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="068d3-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="068d3-120">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="068d3-120">Build the status code error response page</span></span>

<span data-ttu-id="068d3-121">Lai izveidotu statusa koda kļūdas atbildes lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="068d3-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="068d3-122">Doties uz **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="068d3-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="068d3-123">Atlasiet **Jauns**, lai izveidotu lapu.</span><span class="sxs-lookup"><span data-stu-id="068d3-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="068d3-124">Dialoglodziņā **Izvēlēties veidni** atlasiet veidni un pēc tam sadaļā **Lapas nosaukums** ievadiet nosaukumu statusa koda kļūdas atbildei.</span><span class="sxs-lookup"><span data-stu-id="068d3-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="068d3-125">Atstājiet lauku **Lapas vietrādis URL** tukšu.</span><span class="sxs-lookup"><span data-stu-id="068d3-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="068d3-126">Veidojiet lapu.</span><span class="sxs-lookup"><span data-stu-id="068d3-126">Build the page.</span></span>
1. <span data-ttu-id="068d3-127">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="068d3-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="068d3-128">Varat izveidot atsevišķas statusa koda kļūdas atbildes lapas 4xx un 5xx statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="068d3-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="068d3-129">Alternatīvi varat izmantot vienu un to pašu vispārīgā statusa koda kļūdas atbildes lapu abām kļūdu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="068d3-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="068d3-130">Novirzīšanas iestatīšana statusa koda kļūdas atbildes lapai</span><span class="sxs-lookup"><span data-stu-id="068d3-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="068d3-131">Lai iestatītu novirzīšanu statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="068d3-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="068d3-132">Dodieties uz **vietrāži URL \> Jauns \> Jauns aizstājvārds** un atlasiet iepriekš izveidoto statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="068d3-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="068d3-133">Laukā **Aizstājvārds** ievadiet vai nu**default-4xx**, vai **default-5xx**, atkarībā no statusa koda kļūdas atbildes lapas, kam iestatāt novirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="068d3-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="068d3-134">Šie aizstājvārdi ir jāpublicē.</span><span class="sxs-lookup"><span data-stu-id="068d3-134">These aliases must be published.</span></span> <span data-ttu-id="068d3-135">Pretējā gadījumā novirzīšana nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="068d3-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="068d3-136">Atlasiet **Labi**, lai izpildītu saistīšanu.</span><span class="sxs-lookup"><span data-stu-id="068d3-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="068d3-137">Ja izmantojat vienu statusa koda kļūdas atbildes lapu abām kļūdu kategorijām, atkārtojiet šo procedūru, lai ar to pašu lapu saistītu aizstājvārdu citai kļūdas kategorijai.</span><span class="sxs-lookup"><span data-stu-id="068d3-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="068d3-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="068d3-138">Additional resources</span></span>

[<span data-ttu-id="068d3-139">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="068d3-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="068d3-140">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="068d3-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="068d3-141">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="068d3-141">Create a page URL</span></span>](create-page-url.md)
