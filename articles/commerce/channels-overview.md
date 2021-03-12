---
title: Kanālu apskats
description: Šajā tēmā sniegts pārskats par kanāliem programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e060fe2a578296f079653244ed4d5676313e5ea8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963064"
---
# <a name="channels-overview"></a><span data-ttu-id="65924-103">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="65924-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="65924-104">Šajā tēmā sniegts pārskats par kanāliem programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65924-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="65924-105">Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc katra kanāla iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="65924-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="65924-106">Kanālu veidi</span><span class="sxs-lookup"><span data-stu-id="65924-106">Types of Channels</span></span>

<span data-ttu-id="65924-107">Dynamics 365 Commerce atbalsta trīs dažādus kanālu veidus: mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.</span><span class="sxs-lookup"><span data-stu-id="65924-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="65924-108">Mazumtirdzniecības kanāli</span><span class="sxs-lookup"><span data-stu-id="65924-108">Retail channels</span></span>

<span data-ttu-id="65924-109">Mazumtirdzniecības kanāli ir standarta fiziskie veikali.</span><span class="sxs-lookup"><span data-stu-id="65924-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="65924-110">Katram veikalam var būt savas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="65924-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="65924-111">Zvanu centra kanāli</span><span class="sxs-lookup"><span data-stu-id="65924-111">Call center channels</span></span>

<span data-ttu-id="65924-112">Zvanu centra kanāli attēlo zvanu centra kārtību un debitoru pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="65924-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="65924-113">Tiešsaistes kanāli</span><span class="sxs-lookup"><span data-stu-id="65924-113">Online channels</span></span>

<span data-ttu-id="65924-114">Tiešsaistes kanāli ir tiešsaistes e-Commerce veikali.</span><span class="sxs-lookup"><span data-stu-id="65924-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="65924-115">Kad tiešsaistes kanāls ir izveidots, vietne ir jāizveido, izmantojot Microsoft Dynamics 365 Commerce vietnes veidošanas rīku vai citu trešās puses e-Commerce risinājumu.</span><span class="sxs-lookup"><span data-stu-id="65924-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="65924-116">Kanāla iestatīšanas pamati</span><span class="sxs-lookup"><span data-stu-id="65924-116">Channel setup basics</span></span>

<span data-ttu-id="65924-117">Kanāla iestatījumi tiek veikti Commerce rīkā.</span><span class="sxs-lookup"><span data-stu-id="65924-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="65924-118">Katram kanālam var būt savas maksājuma metodes, cenu grupas, preču hierarhijas, preču klāsts un preču kopa.</span><span class="sxs-lookup"><span data-stu-id="65924-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="65924-119">Pēc kanāla izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā pārdot.</span><span class="sxs-lookup"><span data-stu-id="65924-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="65924-120">Katram kanāla veidam ir unikāls funkciju kopums, ko var būt nepieciešams konfigurēt.</span><span class="sxs-lookup"><span data-stu-id="65924-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="65924-121">Piemēram, mazumtirdzniecības kanālam ir jāpiešķir darbinieki, reģistri un debitori.</span><span class="sxs-lookup"><span data-stu-id="65924-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="65924-122">Kad jauns kanāls ir izveidots, tas ir jāpiešķir organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="65924-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="65924-123">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="65924-123">Channel setup prerequisites</span></span>

<span data-ttu-id="65924-124">Pirms kanāla iestatīšanas ir jāpabeidz daži priekšnosacījumu uzdevumi, pamatojoties uz kanāla veidu.</span><span class="sxs-lookup"><span data-stu-id="65924-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="65924-125">Plašāku informāciju skatiet sadaļā [Kanāla iestatīšanas priekšnosacījumi](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="65924-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="65924-126">Kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-126">Set up a channel</span></span>

<span data-ttu-id="65924-127">Kad esat pabeidzis priekšnosacījumu uzdevumus, papildu iestatīšanas instrukcijām izmantojiet tālāk norādītās saites.</span><span class="sxs-lookup"><span data-stu-id="65924-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="65924-128">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="65924-129">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="65924-130">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="65924-131">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="65924-131">Additional resources</span></span>

[<span data-ttu-id="65924-132">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="65924-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="65924-133">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="65924-134">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="65924-135">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="65924-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="65924-136">Iestatīt organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="65924-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
