---
title: Nomas grupas izveide
description: Šajā tēmā ir paskaidrots, kā iestatīt nomas grupas. Nomas grupas ir vajadzīgas, lai izveidotu jaunas nomas.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8512a59d0e9935090f97a0f0237bfefc8473955
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445789"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="62ddb-104">Nomas grupas izveide</span><span class="sxs-lookup"><span data-stu-id="62ddb-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62ddb-105">Šajā tēmā ir paskaidrots, kā iestatīt nomas grupas.</span><span class="sxs-lookup"><span data-stu-id="62ddb-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="62ddb-106">Nomas grupas ir vajadzīgas, lai izveidotu jaunas nomas.</span><span class="sxs-lookup"><span data-stu-id="62ddb-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="62ddb-107">Nomas grāmatas ir saistītas ar katru nomas grupu.</span><span class="sxs-lookup"><span data-stu-id="62ddb-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="62ddb-108">Nomas grāmatas nosaka noklusējuma grāmatas, kas jāizveido katrai nomai.</span><span class="sxs-lookup"><span data-stu-id="62ddb-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="62ddb-109">Varat piešķirt konkrētus kontus nomas grupai lapā **Nomas grāmatošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="62ddb-110">Nomas grāmatas izveide un nomas grupas pievienošana</span><span class="sxs-lookup"><span data-stu-id="62ddb-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="62ddb-111">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grupas**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="62ddb-112">Lai pievienotu nomas grupu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="62ddb-113">Režģim tiek pievienota rinda.</span><span class="sxs-lookup"><span data-stu-id="62ddb-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="62ddb-114">Jaunās rindas laukā **Nomas grupa** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="62ddb-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="62ddb-115">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="62ddb-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="62ddb-116">Tikko ievadītā informācija tiek pievienota laukam **Nomas grupa** lapā **Pievienot nomu**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="62ddb-117">Grāmatas saistīšana ar nomas grupu</span><span class="sxs-lookup"><span data-stu-id="62ddb-117">Associate a book with a lease group</span></span>

<span data-ttu-id="62ddb-118">Pēc nomas grupu izveides varat piešķirt grāmatas katrai grupai.</span><span class="sxs-lookup"><span data-stu-id="62ddb-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="62ddb-119">Izveidojot nomu un piešķirot to nomas grupai, sistēma izveido grafiku kopu katrai grāmatai, kas saistīta ar nomas grupu.</span><span class="sxs-lookup"><span data-stu-id="62ddb-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="62ddb-120">Grāmatas ir jāiestata pirms tās var piešķirt nomas grupai.</span><span class="sxs-lookup"><span data-stu-id="62ddb-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="62ddb-121">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grupa**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="62ddb-122">Atlasiet nomas grupu un pēc tam atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="62ddb-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="62ddb-123">Atlasiet **Jauns** un pēc tam laukā **Grāmatas veids** atlasiet grāmatu, ko piešķirt nomas grupai.</span><span class="sxs-lookup"><span data-stu-id="62ddb-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="62ddb-124">Nomas grupai varat piešķirt vairākas grāmatas, ja noma jāuzskaita dažādos veidos.</span><span class="sxs-lookup"><span data-stu-id="62ddb-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
