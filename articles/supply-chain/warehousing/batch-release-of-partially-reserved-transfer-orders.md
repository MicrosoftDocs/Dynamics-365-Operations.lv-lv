---
title: "Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un lietot daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišanu no mobilās ierīces."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="44c28-103">Daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišana</span><span class="sxs-lookup"><span data-stu-id="44c28-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="44c28-104">Funkcionalitāte daļēji rezervētu pārsūtīšanas pasūtījumu partijas izlaišanai jums ļauj uz noliktavu daļēji pārvietot pārsūtīšanas pasūtījumus, izmantojot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="44c28-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="44c28-105">Tā kā jums ir iespēja izlaist daļēju daudzumu, tad pirms pasūtījuma izlaišanas jums nav jāgaida, līdz noliktavā ir pieejams viss pasūtījuma daudzums.</span><span class="sxs-lookup"><span data-stu-id="44c28-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="44c28-106">Pasūtījumu pārvietošana uz noliktavu ir papildu noliktavas vadības process.</span><span class="sxs-lookup"><span data-stu-id="44c28-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="44c28-107">Šis process ietver tādas aktivitātes kā izdošana, iepakošana un nosūtīšana, kuras noliktavas darbinieks var veikt, izmantojot mobilo ierīci.</span><span class="sxs-lookup"><span data-stu-id="44c28-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="44c28-108">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="44c28-108">Where it applies</span></span>

<span data-ttu-id="44c28-109">Šai funkcionalitātei pārsūtīšanas pasūtījumi uz noliktavu tiek pārvietoti, izmantojot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="44c28-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="44c28-110">Šī funkcionalitāte ir noderīga, ja jums noliktavā nav pietiekami daudz krājumu, bet jūs tik un tā vēlaties krājumus no vienas noliktavas pārsūtīt uz citu.</span><span class="sxs-lookup"><span data-stu-id="44c28-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="44c28-111">Kā to iestatīt</span><span class="sxs-lookup"><span data-stu-id="44c28-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="44c28-112">Norādīt izpildes kritērijus pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="44c28-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="44c28-113">Lai pasūtījumu varētu daļēji pārvietot uz noliktavu pakešveidā, ir jābūt izpildītiem izpildes kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="44c28-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="44c28-114">Šos izpildes kritērijus nosaka izpildes politika.</span><span class="sxs-lookup"><span data-stu-id="44c28-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="44c28-115">Izpildes politikas attiecībā uz pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem tiek norādītas uzņēmuma līmenī.</span><span class="sxs-lookup"><span data-stu-id="44c28-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="44c28-116">Atkarībā no izpildes politikas iestatījumiem pasūtījumu izlaišana pakešveidā tiks pieņemta vai noraidīta.</span><span class="sxs-lookup"><span data-stu-id="44c28-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="44c28-117">Pēc tam pasūtījumi tiks atbilstoši apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="44c28-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="44c28-118">Lai izveidotu izpildes politikas pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Pārvietot uz noliktavu** \> **Izpildes politika**, un pēc tam izveidojiet izpildes politiku, ievadot nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="44c28-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="44c28-119">Lai norādītu izpildes koeficientu, vērtības tipu un ziņojumu, kas tiek rādīts, ja izpildes politika tiek pārkāpta, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Pārvietot uz noliktavu** \> **Izpildes politika** un pēc tam iestatiet laukus **Izpildes koeficients**, **Vērtības tips** un **Izpildes pārkāpumu ziņojums**.</span><span class="sxs-lookup"><span data-stu-id="44c28-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="44c28-120">Iestatīt izpildes politikas pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="44c28-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="44c28-121">Lai izpildes politikas iestatītu pārsūtīšanas pasūtījumiem, noklikšķiniet uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** \> **Pārsūtīšanas pasūtījumi** \> **Noliktavas vadība** un pēc tam atlasiet pārsūtīšanas pasūtījumu izpildes politiku.</span><span class="sxs-lookup"><span data-stu-id="44c28-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="44c28-122">Lai izpildes politikas iestatītu pārdošanas pasūtījumiem, noklikšķiniet uz **Debitoru parādi** \> **Iestatījumi** \> **Debitoru parādu parametri** \> **Noliktavas vadība** un pēc tam atlasiet pārdošanas pasūtījumu izpildes politiku.</span><span class="sxs-lookup"><span data-stu-id="44c28-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="44c28-123">Atļaut izlaišanu pakešveidā un norādīt daudzumu, kas ir jāizlaiž pakešveidā</span><span class="sxs-lookup"><span data-stu-id="44c28-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="44c28-124">Pakešuzdevums tiek izmantots pasūtījumu pārvietošanai uz noliktavu pakešveidā.</span><span class="sxs-lookup"><span data-stu-id="44c28-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="44c28-125">Parametri, kas norāda pasūtījumus, kuri ir jāpalaiž pakešuzdevumā, tiek iestatīti pašā pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="44c28-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="44c28-126">Parametrs **Daudzums** norāda, vai paketē ir jāizlaiž viss daudzums vai fiziski rezervētais daudzums.</span><span class="sxs-lookup"><span data-stu-id="44c28-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="44c28-127">Parametrs **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** nosaka, vai pasūtījumi paketē ir jāpieņem vai jānoraida, ja tie iepriekš bija izlaisti daļēji.</span><span class="sxs-lookup"><span data-stu-id="44c28-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="44c28-128">Lai parametru **Daudzums** un **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** iestatītu pārsūtīšanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Pārvietot uz noliktavu** \> **Pārsūtīšanas pasūtījumu automātiska pārvietošana**.</span><span class="sxs-lookup"><span data-stu-id="44c28-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="44c28-129">Lai parametru **Daudzums** un **Atļaut daļēji pārvietotu pasūtījumu pārvietošanu** iestatītu pārdošanas pasūtījumiem, noklikšķiniet uz **Noliktavas vadība** \> **Pārvietot uz noliktavu** \> **Pārdošanas pasūtījumu automātiska pārvietošana**.</span><span class="sxs-lookup"><span data-stu-id="44c28-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

