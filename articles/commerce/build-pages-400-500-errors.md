---
title: Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām
description: Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697110"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="ab79c-103">Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām</span><span class="sxs-lookup"><span data-stu-id="ab79c-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ab79c-104">Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab79c-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab79c-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ab79c-105">Overview</span></span>

<span data-ttu-id="ab79c-106">Ja pieprasījums ir neveiksmīgs, serveris izdod HTTP statusa koda kļūdas atbildes.</span><span class="sxs-lookup"><span data-stu-id="ab79c-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="ab79c-107">404 statusa kods tiek iegūts un atgriezts, ja lapa netiek atrasta, un 500 statusa kods tiek iegūts un atgriezts servera kļūdas gadījumā.</span><span class="sxs-lookup"><span data-stu-id="ab79c-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="ab79c-108">Lietojumprogrammā Dynamics 365 Commerce lietotāji var izveidot pielāgotas statusa koda kļūdas atbilžu lapas, kas tiek rādītas lietotājiem saistībā ar šīm statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="ab79c-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="ab79c-109">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="ab79c-109">Build a status code error response page</span></span>

<span data-ttu-id="ab79c-110">Lai sāktu statusa koda kļūdas atbildes lapas izveidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ab79c-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ab79c-111">Vēlamajā tīmekļa pārlūkā pierakstieties programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ab79c-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="ab79c-112">Atlasiet vietni, kurai vēlaties izveidot 4xx/5xx statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="ab79c-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="ab79c-113">Veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="ab79c-113">Build the template</span></span>

<span data-ttu-id="ab79c-114">Lai izveidotu veidni statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ab79c-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ab79c-115">Dodieties uz **Veidnes \>Jauna veidne**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="ab79c-116">Nosauciet jauno veidni.</span><span class="sxs-lookup"><span data-stu-id="ab79c-116">Name the new template.</span></span>
1. <span data-ttu-id="ab79c-117">Izveidojiet veidni, pamatojoties uz struktūru, ko vēlaties izmantot statusa koda kļūdas atbildes lapā.</span><span class="sxs-lookup"><span data-stu-id="ab79c-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="ab79c-118">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="ab79c-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="ab79c-119">Statusa koda kļūdas atbildes lapas izveide</span><span class="sxs-lookup"><span data-stu-id="ab79c-119">Build the status code error response page</span></span>

<span data-ttu-id="ab79c-120">Lai izveidotu statusa koda kļūdas atbildes lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ab79c-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ab79c-121">Dodieties uz **Lapas \>Jauna lapa**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="ab79c-122">Norādiet nosaukumu statusa koda kļūdas atbildes lapai, bet **neiestatiet** vietrāža **URL** lauku.</span><span class="sxs-lookup"><span data-stu-id="ab79c-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="ab79c-123">Veidojiet lapu.</span><span class="sxs-lookup"><span data-stu-id="ab79c-123">Build the page.</span></span>
1. <span data-ttu-id="ab79c-124">Pārbaudiet lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="ab79c-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ab79c-125">Varat izveidot atsevišķas statusa koda kļūdas atbildes lapas 4xx un 5xx statusa koda kļūdām.</span><span class="sxs-lookup"><span data-stu-id="ab79c-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="ab79c-126">Alternatīvi varat izmantot vienu un to pašu vispārīgā statusa koda kļūdas atbildes lapu abām kļūdu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="ab79c-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="ab79c-127">Novirzīšanas iestatīšana statusa koda kļūdas atbildes lapai</span><span class="sxs-lookup"><span data-stu-id="ab79c-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="ab79c-128">Lai iestatītu novirzīšanu statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ab79c-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ab79c-129">Dodieties uz **vietrāži URL \> Jauns \> Jauns aizstājvārds** un atlasiet iepriekš izveidoto statusa koda kļūdas atbildes lapu.</span><span class="sxs-lookup"><span data-stu-id="ab79c-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="ab79c-130">Laukā **Aizstājvārds** ievadiet vai nu**default-4xx**, vai **default-5xx**, atkarībā no statusa koda kļūdas atbildes lapas, kam iestatāt novirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="ab79c-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="ab79c-131">Šie aizstājvārdi ir jāpublicē.</span><span class="sxs-lookup"><span data-stu-id="ab79c-131">These aliases must be published.</span></span> <span data-ttu-id="ab79c-132">Pretējā gadījumā novirzīšana nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="ab79c-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="ab79c-133">Atlasiet **Labi**, lai izpildītu saistīšanu.</span><span class="sxs-lookup"><span data-stu-id="ab79c-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="ab79c-134">Ja izmantojat vienu statusa koda kļūdas atbildes lapu abām kļūdu kategorijām, atkārtojiet šo procedūru, lai ar to pašu lapu saistītu aizstājvārdu citai kļūdas kategorijai.</span><span class="sxs-lookup"><span data-stu-id="ab79c-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab79c-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ab79c-135">Additional resources</span></span>

[<span data-ttu-id="ab79c-136">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="ab79c-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ab79c-137">Jaunas vietnes lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="ab79c-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ab79c-138">Lapas vietrāža URL izveide</span><span class="sxs-lookup"><span data-stu-id="ab79c-138">Create a page URL</span></span>](create-page-url.md)
