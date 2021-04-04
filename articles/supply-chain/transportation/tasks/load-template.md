---
title: Kravas veidnes
description: Šajā tēmā ir aprakstīts, kā iestatīt kravas veidnes un kā kravas veidni saistīt ar jaunu kravu.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 80004b5d22e1cf81c1ffa9f74c2c479e1561df72
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247218"
---
# <a name="load-templates"></a><span data-ttu-id="bc112-103">Kravas veidnes</span><span class="sxs-lookup"><span data-stu-id="bc112-103">Load templates</span></span>

<span data-ttu-id="bc112-104">Kad izveidojat jaunu kravu, varat piešķirt kravas veidni.</span><span class="sxs-lookup"><span data-stu-id="bc112-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="bc112-105">Kravas veidnē ir ietverta informācija par aprīkojumu un par tādiem mērījumiem kā, piemēram, kravas augstums, platums, dziļums un tilpums.</span><span class="sxs-lookup"><span data-stu-id="bc112-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="bc112-106">Šajā tēmā ir aprakstīts, kā iestatīt kravas veidnes un kā kravas veidni saistīt ar jaunu kravu.</span><span class="sxs-lookup"><span data-stu-id="bc112-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="bc112-107">Kravas veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="bc112-107">Set up a load template</span></span>

1. <span data-ttu-id="bc112-108">Doties uz **Transportēšanas pārvaldība \> Uzstādīšana \> Kravas plānošana \> Kravas veidne**.</span><span class="sxs-lookup"><span data-stu-id="bc112-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="bc112-109">Darbības rūtī atlasiet **Jauns**, lai pievienotu jaunu veidni vai **Rediģēt**, lai rediģētu esošo veidni.</span><span class="sxs-lookup"><span data-stu-id="bc112-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="bc112-110">Jaunās vai esošās veidnes rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="bc112-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="bc112-111">**Kravas veidnes ID** - ievadiet unikālu kravas veidnes identifikatoru (ID).</span><span class="sxs-lookup"><span data-stu-id="bc112-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="bc112-112">**Aprīkojums** - atlasiet aprīkojumu, kas jāizmanto kravas nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="bc112-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="bc112-113">**Kravas augstums**, **Kravas platums** un **Kravas dziļums** - ievadiet kravas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bc112-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="bc112-114">**Maks. atļautais kravas tilpums** un **Maks. atļautais kravas svars** - ievadiet maksimālo atļauto kravas apjomu un svaru.</span><span class="sxs-lookup"><span data-stu-id="bc112-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="bc112-115">**Maksimālais atļautais bruto svars** - ievadiet maksimālo atļauto kravas bruto svaru.</span><span class="sxs-lookup"><span data-stu-id="bc112-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="bc112-116">Kravas bruto svars ietver gan kravas taras svaru, gan kravas noslodzes svaru.</span><span class="sxs-lookup"><span data-stu-id="bc112-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="bc112-117">**Maksimālais atļautais kravas vienību skaits** - ievadiet maksimālo kravas vienību skaitu, ko var saturēt krava.</span><span class="sxs-lookup"><span data-stu-id="bc112-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="bc112-118">**Kravas noslodze uz grīdas** — atzīmējiet šo izvēles rūtiņu, lai lietotu grīdas noslodzi.</span><span class="sxs-lookup"><span data-stu-id="bc112-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="bc112-119">Grīdas nestspējas gadījumā kastes konteinerā tiek sakrautas no grīdas līdz griestiem un no vienas sienas līdz otrai, maksimizējot iekšējo ietilpību.</span><span class="sxs-lookup"><span data-stu-id="bc112-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="bc112-120">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bc112-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="bc112-121">Kravas veidnes saistīšana ar jaunu kravu</span><span class="sxs-lookup"><span data-stu-id="bc112-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="bc112-122">Dodieties uz **Transportēšanas pārvaldība \> Plānošana \> Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="bc112-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="bc112-123">Lapas augšdaļā atlasiet vienu no šīm cilnēm atkarībā no pirmdokumenta tipa, kuram tiek veidota krava: **Sūtījumi**, **Pārdošanas rindas**, **Pārsūtīšanas rindas** vai **Pirkšanas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="bc112-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="bc112-124">Atlasiet konkrētu dokumentu, kam plānot kravu.</span><span class="sxs-lookup"><span data-stu-id="bc112-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="bc112-125">Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**.</span><span class="sxs-lookup"><span data-stu-id="bc112-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="bc112-126">Dialoglodziņā **Kravas veidne** laukā **Kravas veidnes ID** atlasiet veidni, ko piemērot.</span><span class="sxs-lookup"><span data-stu-id="bc112-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="bc112-127">Atlasiet **Labi**, lai pielietotu veidni.</span><span class="sxs-lookup"><span data-stu-id="bc112-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]