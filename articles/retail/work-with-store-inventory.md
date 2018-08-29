---
title: "Veikala krājumu vadība"
description: "Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="store-inventory-management"></a><span data-ttu-id="6e3ba-103">Veikala krājumu vadība</span><span class="sxs-lookup"><span data-stu-id="6e3ba-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e3ba-104">Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="6e3ba-105">Lai pārvaldītu savas organizācija krājumus, varat izmantot tālāk uzskaitītos dokumentu tipus.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="6e3ba-106">Pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="6e3ba-106">Purchase orders</span></span>
<span data-ttu-id="6e3ba-107">Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="6e3ba-108">Ja pirkšanas pasūtījuma virsrakstā ir iekļauta mazumtirdzniecības noliktava, pasūtījumu var saņemt veikalā, izmantojot programmu Modern POS (MPOS) vai Cloud POS programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="6e3ba-109">Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="6e3ba-110">Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="6e3ba-111">Veikalā saņemtie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pirkšanas pasūtījuma laukā **Saņemt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="6e3ba-112">Pārsūtīšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="6e3ba-112">Transfer orders</span></span>
<span data-ttu-id="6e3ba-113">Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, no kura krājumus var sūtīt.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="6e3ba-114">Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā izdošanas pieprasījums programmā MPOS vai Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="6e3ba-115">Pēc pieprasīto daudzumu izdošanas tie tiek fiksēti un nosūtīti uz centrālo biroju.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="6e3ba-116">Veikalā izdotie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pārsūtīšanas pasūtījuma laukā **Nosūtīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="6e3ba-117">Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, uz kuru krājumus var sūtīt.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="6e3ba-118">Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā saņemšanas pieprasījums programmā MPOS vai Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="6e3ba-119">Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="6e3ba-120">Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="6e3ba-121">Veikalā saņemtie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pārsūtīšanas pasūtījuma laukā **Saņemt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="6e3ba-122">Krājumu uzskaite</span><span class="sxs-lookup"><span data-stu-id="6e3ba-122">Stock counts</span></span>
<span data-ttu-id="6e3ba-123">Krājumu uzskaites var būt plānotas vai neplānotas.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="6e3ba-124">Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="6e3ba-125">Galvenajā birojā tiek izveidots uzskaites dokuments, ko var saņemt veikalā, kurā faktisko rīcībā esošo krājumu daudzumi ir ievadīto programmā MPOS vai Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="6e3ba-126">Veikalā tiek sākta neplānota krājumu uzskaite, programmā MPOS vai Cloud POS tiek atjaunināti faktisko rīcībā esošo krājumu daudzumi.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="6e3ba-127">Atšķirībā no ieplānotās krājumu uzskaites neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="6e3ba-128">Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="6e3ba-129">Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="6e3ba-130">Krājumu pārlūkošana</span><span class="sxs-lookup"><span data-stu-id="6e3ba-130">Inventory lookup</span></span>
<span data-ttu-id="6e3ba-131">Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā Krājumu uzmeklēšana.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="6e3ba-132">Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="6e3ba-133">Lai to izdarītu, atlasiet veikalu, kuram vēlaties skatīt ATP, un pēc tam noklikšķiniet uz **Rādīt veikala pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="6e3ba-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





