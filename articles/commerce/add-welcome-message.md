---
title: Sveiciena ziņojuma pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697386"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="ae77c-103">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="ae77c-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ae77c-104">Šajā tēmā ir aprakstīts, kā pievienot sveiciena ziņojumu savai Microsoft Dynamics 365 Commerce tīmekļa vietnei.</span><span class="sxs-lookup"><span data-stu-id="ae77c-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="ae77c-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ae77c-105">Overview</span></span>

<span data-ttu-id="ae77c-106">Sveiciena ziņojums jūsu E-komercijas tīmekļa vietnē var informēt apmeklētājus par notiekošo pārdošanu, vietnes atjauninājumiem vai sezonālo kolekciju pieejamību.</span><span class="sxs-lookup"><span data-stu-id="ae77c-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="ae77c-107">Sveiciena ziņojums tiek iestatīts, izmantojot brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="ae77c-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="ae77c-108">Brīdinājuma modulis ir jāpievieno galvenes fragmenta slotam **Kļūdas/informācijas ziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="ae77c-109">Brīdinājuma modulis ļauj norādīt parādāmo tekstu, teksta krāsu un līdzinājumu.</span><span class="sxs-lookup"><span data-stu-id="ae77c-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="ae77c-110">Tas arī ļauj norādīt, vai vietnes apmeklētāji var noraidīt šo ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="ae77c-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="ae77c-111">Kad koplietojamam galvenes fragmentam tiek pievienots sveiciena ziņojums, tas tiks parādīts katrā lapā, kas lieto veidni, kurā tiek izmantots šis koplietojamais galvenes fragments.</span><span class="sxs-lookup"><span data-stu-id="ae77c-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="ae77c-112">Lai vietnei pievienotu sveiciena ziņojumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae77c-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="ae77c-113">Programmā Dynamics 365 Commerce dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="ae77c-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="ae77c-114">Atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="ae77c-115">Atlasiet galvenes fragmentu, kam pievienot ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="ae77c-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="ae77c-116">Strukturējuma kokā izvērsiet **Kļūdas/informācijas ziņojumus**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="ae77c-117">Atlasiet brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="ae77c-117">Select the alert module.</span></span>

    <span data-ttu-id="ae77c-118">Ja brīdinājuma modulis vēl nav izveidots, atlasiet daudzpunktes pogu (**...**) blakus **Kļūdas/informācijas ziņojumi** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="ae77c-119">Atlasiet brīdinājuma moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="ae77c-120">Rekvizītu rūtī labajā pusē cilnē **Dati** atlasiet **Pievienot datu avotu** un pēc tam atlasiet **Saturs**.</span><span class="sxs-lookup"><span data-stu-id="ae77c-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="ae77c-121">Laukā **Ievades teksts** norādiet sveiciena ziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="ae77c-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="ae77c-122">Saglabājiet galvenes fragmentu, pārbaudiet un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="ae77c-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="ae77c-123">Tagad sveiciena ziņojums tiks parādīts katras vietnes lapas, kura izmanto atlasīto galvenes fragmentu, augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="ae77c-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae77c-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ae77c-124">Additional resources</span></span>

[<span data-ttu-id="ae77c-125">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="ae77c-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ae77c-126">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="ae77c-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ae77c-127">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="ae77c-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ae77c-128">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="ae77c-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="ae77c-129">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="ae77c-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ae77c-130">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="ae77c-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

