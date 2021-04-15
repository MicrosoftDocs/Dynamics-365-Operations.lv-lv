---
title: Sveiciena ziņojuma pievienošana
description: Šajā tēmā aprakstīts, kā pievienot sagaidīšanas ziņojumu savai Microsoft Dynamics 365 Commerce vietnei.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797387"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="3d11a-103">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="3d11a-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d11a-104">Šajā tēmā aprakstīts, kā pievienot sagaidīšanas ziņojumu savai Microsoft Dynamics 365 Commerce vietnei.</span><span class="sxs-lookup"><span data-stu-id="3d11a-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="3d11a-105">Sveiciena ziņojums jūsu E-komercijas tīmekļa vietnē var informēt apmeklētājus par notiekošo pārdošanu, vietnes atjauninājumiem vai sezonālo kolekciju pieejamību.</span><span class="sxs-lookup"><span data-stu-id="3d11a-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="3d11a-106">Sveiciena ziņojums tiek iestatīts, izmantojot brīdinājuma moduli.</span><span class="sxs-lookup"><span data-stu-id="3d11a-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="3d11a-107">Brīdinājuma modulis ir jāpievieno galvenes fragmenta slotam **Kļūdas/informācijas ziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="3d11a-108">Brīdinājuma modulis ļauj norādīt parādāmo tekstu, teksta krāsu un līdzinājumu.</span><span class="sxs-lookup"><span data-stu-id="3d11a-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="3d11a-109">Tas arī ļauj norādīt, vai vietnes apmeklētāji var noraidīt šo ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="3d11a-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="3d11a-110">Kad koplietojamam galvenes fragmentam tiek pievienots sveiciena ziņojums, tas tiks parādīts katrā lapā, kas lieto veidni, kurā tiek izmantots šis koplietojamais galvenes fragments.</span><span class="sxs-lookup"><span data-stu-id="3d11a-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="3d11a-111">Lai vietnei pievienotu sveiciena ziņojumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="3d11a-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="3d11a-112">Dodieties uz savu vietni Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="3d11a-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="3d11a-113">Atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="3d11a-114">Atlasiet galvenes fragmentu, kam pievienot ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="3d11a-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="3d11a-115">Strukturējuma kokā izvērsiet **Kļūdas/informācijas ziņojumus**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="3d11a-116">Atlasiet brīdinājuma moduli un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="3d11a-117">Ja brīdinājuma modulis vēl nav izveidots, vispirms atlasiet daudzpunktes pogu (**...**) blakus **Kļūdas/informācijas ziņojumi** un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="3d11a-118">Rekvizītu rūtī labajā pusē cilnē **Dati** atlasiet **Pievienot datu avotu** un pēc tam atlasiet **Saturs**.</span><span class="sxs-lookup"><span data-stu-id="3d11a-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="3d11a-119">Laukā **Ievades teksts** norādiet sveiciena ziņojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="3d11a-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="3d11a-120">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu galvenes fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="3d11a-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="3d11a-121">Tagad sveiciena ziņojums tiks parādīts katras vietnes lapas, kura izmanto atlasīto galvenes fragmentu, augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="3d11a-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d11a-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3d11a-122">Additional resources</span></span>

[<span data-ttu-id="3d11a-123">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="3d11a-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3d11a-124">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="3d11a-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3d11a-125">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="3d11a-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3d11a-126">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="3d11a-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3d11a-127">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="3d11a-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3d11a-128">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="3d11a-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3d11a-129">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="3d11a-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
