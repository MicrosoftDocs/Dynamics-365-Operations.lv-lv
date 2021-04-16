---
title: Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām
description: Šajā tēmā aprakstīts, kā veidot klientu atbildes lapas statusa koda kļūdām 4xx un 5xx, izmantojot autorēšanas rīkus risinājumā Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799655"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="d1978-103">Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām</span><span class="sxs-lookup"><span data-stu-id="d1978-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1978-104">Šajā tēmā aprakstīts, kā veidot klientu atbildes lapas statusa koda kļūdām 4xx un 5xx, izmantojot autorēšanas rīkus risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1978-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d1978-105">Ja pieprasījums ir neveiksmīgs, serveris izdod HTTP statusa koda kļūdas atbildes.</span><span class="sxs-lookup"><span data-stu-id="d1978-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="d1978-106">404 statusa kods tiek iegūts un atgriezts, ja lapa netiek atrasta, un 500 statusa kods tiek iegūts un atgriezts servera kļūdas gadījumā.</span><span class="sxs-lookup"><span data-stu-id="d1978-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="d1978-107">Lietojumprogrammā Dynamics 365 Commerce lietotāji var izveidot pielāgotas statusa koda kļūdas atbilžu lapas, kas tiek rādītas lietotājiem saistībā ar šīm statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="d1978-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="d1978-108">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="d1978-108">Build a status code error response page</span></span>

<span data-ttu-id="d1978-109">Lai sāktu statusa koda kļūdas atbildes lapas izveidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1978-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d1978-110">Vēlamajā tīmekļa pārlūkā pierakstieties programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d1978-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="d1978-111">Atlasiet vietni, kurai vēlaties izveidot 4xx/5xx statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="d1978-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="d1978-112">Veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="d1978-112">Build the template</span></span>

<span data-ttu-id="d1978-113">Lai izveidotu veidni statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1978-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d1978-114">Dodieties uz **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="d1978-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="d1978-115">Atlasiet **Jauns**, lai izveidotu lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="d1978-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="d1978-116">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet jaunās veidnes nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d1978-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="d1978-117">Izveidojiet veidni, pamatojoties uz struktūru, ko vēlaties izmantot statusa koda kļūdas atbildes lapā.</span><span class="sxs-lookup"><span data-stu-id="d1978-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="d1978-118">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d1978-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="d1978-119">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="d1978-119">Build the status code error response page</span></span>

<span data-ttu-id="d1978-120">Lai izveidotu statusa koda kļūdas atbildes lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1978-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d1978-121">Doties uz **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="d1978-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="d1978-122">Atlasiet **Jauns**, lai izveidotu lapu.</span><span class="sxs-lookup"><span data-stu-id="d1978-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="d1978-123">Dialoglodziņā **Izvēlēties veidni** atlasiet veidni un pēc tam sadaļā **Lapas nosaukums** ievadiet nosaukumu statusa koda kļūdas atbildei.</span><span class="sxs-lookup"><span data-stu-id="d1978-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="d1978-124">Atstājiet lauku **Lapas vietrādis URL** tukšu.</span><span class="sxs-lookup"><span data-stu-id="d1978-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="d1978-125">Veidojiet lapu.</span><span class="sxs-lookup"><span data-stu-id="d1978-125">Build the page.</span></span>
1. <span data-ttu-id="d1978-126">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d1978-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="d1978-127">Varat izveidot atsevišķas statusa koda kļūdas atbildes lapas 4xx un 5xx statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="d1978-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="d1978-128">Alternatīvi varat izmantot vienu un to pašu vispārīgā statusa koda kļūdas atbildes lapu abām kļūdu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="d1978-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="d1978-129">Novirzīšanas iestatīšana statusa koda kļūdas atbildes lapai</span><span class="sxs-lookup"><span data-stu-id="d1978-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="d1978-130">Lai iestatītu novirzīšanu statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1978-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d1978-131">Dodieties uz **vietrāži URL \> Jauns \> Jauns aizstājvārds** un atlasiet iepriekš izveidoto statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="d1978-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="d1978-132">Laukā **Aizstājvārds** ievadiet vai nu **default-4xx**, vai **default-5xx**, atkarībā no statusa koda kļūdas atbildes lapas, kam iestatāt novirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="d1978-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="d1978-133">Šie aizstājvārdi ir jāpublicē.</span><span class="sxs-lookup"><span data-stu-id="d1978-133">These aliases must be published.</span></span> <span data-ttu-id="d1978-134">Pretējā gadījumā novirzīšana nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="d1978-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="d1978-135">Atlasiet **Labi**, lai izpildītu saistīšanu.</span><span class="sxs-lookup"><span data-stu-id="d1978-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="d1978-136">Ja izmantojat vienu statusa koda kļūdas atbildes lapu abām kļūdu kategorijām, atkārtojiet šo procedūru, lai ar to pašu lapu saistītu aizstājvārdu citai kļūdas kategorijai.</span><span class="sxs-lookup"><span data-stu-id="d1978-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1978-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d1978-137">Additional resources</span></span>

[<span data-ttu-id="d1978-138">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="d1978-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d1978-139">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="d1978-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d1978-140">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="d1978-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
