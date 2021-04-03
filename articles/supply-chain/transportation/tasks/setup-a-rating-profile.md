---
title: Novērtējuma profili
description: Šajā tēmā ir aprakstīts, kā iestatīt datus novērtējuma profiliem.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f754a8b86b0d369af03812a831d77a8a6fa8154
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233515"
---
# <a name="rating-profiles"></a><span data-ttu-id="50eea-103">Novērtējuma profili</span><span class="sxs-lookup"><span data-stu-id="50eea-103">Rating profiles</span></span>

<span data-ttu-id="50eea-104">Novērtējuma profils atgādina loģistikas līgumu (bet ne juridisku līgumu).</span><span class="sxs-lookup"><span data-stu-id="50eea-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="50eea-105">Tas tiek izmantots, lai noteiktu transportēšanas tarifus kravām.</span><span class="sxs-lookup"><span data-stu-id="50eea-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="50eea-106">Katrs novērtējuma profils sūtījumu pārvadātājam ir unikāls.</span><span class="sxs-lookup"><span data-stu-id="50eea-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="50eea-107">Novērtējuma profilā jūs saistāt sūtījumu pārvadātāju saistītu ar likmes šablonu.</span><span class="sxs-lookup"><span data-stu-id="50eea-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="50eea-108">Likmes šablons definē likmes bāzes piešķiri un likmes bāzi.</span><span class="sxs-lookup"><span data-stu-id="50eea-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="50eea-109">Likmes bāze nosaka pārvadātāja likmi.</span><span class="sxs-lookup"><span data-stu-id="50eea-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="50eea-110">Novērtējuma profilu varat iestatīt, izmantojot vispārīgo lapu, kas parāda pārskatu par visiem esošajiem novērtējuma profiliem.</span><span class="sxs-lookup"><span data-stu-id="50eea-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="50eea-111">Alternatīvi, novērtējuma profilu varat arī iestatīt tieši no sūtījumu pārvadātāja.</span><span class="sxs-lookup"><span data-stu-id="50eea-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="50eea-112">Abos gadījumos novērtējuma profilam iestatītā informācija ir tāda pati.</span><span class="sxs-lookup"><span data-stu-id="50eea-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="50eea-113">Izveidot vai rediģēt novērtējuma profilu lapā Novērtējuma profili</span><span class="sxs-lookup"><span data-stu-id="50eea-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="50eea-114">Lapā **Novērtējuma profili** varat pārskatīt visus pieejamos novērtējuma profilus.</span><span class="sxs-lookup"><span data-stu-id="50eea-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="50eea-115">Varat arī rediģēt esošos profilus un izveidot jaunus profilus.</span><span class="sxs-lookup"><span data-stu-id="50eea-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="50eea-116">Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Novērtējuma profils**.</span><span class="sxs-lookup"><span data-stu-id="50eea-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="50eea-117">Darbības rūtī atlasiet **Jauns**, lai pievienotu jaunu novērtējuma profilu režģī vai atlasiet **Rediģēt**, lai rediģētu esošu profilu.</span><span class="sxs-lookup"><span data-stu-id="50eea-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="50eea-118">Jaunā vai esošā novērtējuma profila rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="50eea-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="50eea-119">**Novērtējuma profils** – ievadiet unikālu novērtējuma profila identifikatoru (ID) un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="50eea-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="50eea-120">**Nosaukums** - Ievadiet novērtējuma profila aprakstošu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="50eea-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="50eea-121">**Nosūtīšanas pārvadātājs** - atlasiet nosūtīšanas pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="50eea-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="50eea-122">Novērtējuma profils, kuru iestatāt, tiks norādīts arī izvēlētā pārvadātāja lapā **Nosūtīšanas pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="50eea-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="50eea-123">**Vietne** un **Noliktava** - atlasiet vietni un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="50eea-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="50eea-124">**Likmes noteikšanas programma** - atlasiet likmes noteikšanas programmu novērtējuma profilam.</span><span class="sxs-lookup"><span data-stu-id="50eea-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="50eea-125">**Likmes šablons** - atlasiet likmes šablonu novērtējuma profilam.</span><span class="sxs-lookup"><span data-stu-id="50eea-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="50eea-126">Varat izmantot šo likmes šablonu, lai definētu likmes bāzes tipu un likmes bāzi.</span><span class="sxs-lookup"><span data-stu-id="50eea-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="50eea-127">Plašāku informāciju skatiet [Likmes šablonu iestatīšana](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="50eea-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="50eea-128">**Pārvadājumu ilguma noteikšanas programma** - atlasiet pārvadājumu ilguma noteikšanas programmu novērtējuma profilam.</span><span class="sxs-lookup"><span data-stu-id="50eea-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="50eea-129">**Pārvadātāja degvielas rādītājs** – šim novērtējuma profilam atlasiet pārvadātāja degvielas rādītāju.</span><span class="sxs-lookup"><span data-stu-id="50eea-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="50eea-130">**Spēkā sākšanās datums un laiks**, kā arī **Derīguma beigu datums un laiks** - definējiet periodu, kad novērtējuma profilam ir jābūt aktīvam.</span><span class="sxs-lookup"><span data-stu-id="50eea-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="50eea-131">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="50eea-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="50eea-132">Izveidot novērtējuma profilu tieši lapā Nosūtīšanas pārvadātāji</span><span class="sxs-lookup"><span data-stu-id="50eea-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="50eea-133">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="50eea-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="50eea-134">Sarakstā atlasiet nosūtīšanas pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="50eea-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="50eea-135">Kopsavilkuma cilnē **Novērtējuma profili** noklikšķiniet uz **Jauns**, lai izveidotu novērtējuma profilu.</span><span class="sxs-lookup"><span data-stu-id="50eea-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="50eea-136">Iestatiet laukus jaunajam novērtējuma profilam.</span><span class="sxs-lookup"><span data-stu-id="50eea-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="50eea-137">Šie lauki atbilst lapas **Novērtējuma profilu** laukiem, kā aprakstīts iepriekšējā šīs tēmas sadaļā.</span><span class="sxs-lookup"><span data-stu-id="50eea-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="50eea-138">Lapā **Nosūtīšanas pārvadātāji** izveidotie profili tiek parādīti arī lapā **Novērtējuma profili**.</span><span class="sxs-lookup"><span data-stu-id="50eea-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]