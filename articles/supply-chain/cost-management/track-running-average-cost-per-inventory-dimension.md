---
title: "Pašreizējās vidējās izmaksu cenas izsekošana pēc krājumu dimensijas"
description: "Katrai krājumu vienībai ir piesaistīta krājumu dimensiju grupa. Tāpēc krājuma kārtējo vidējo izmaksu cena tiek aprēķināta, pamatojoties uz atlasītajām krājumu dimensijām, kas tiek finansiāli izsekotas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f8ade2981056e9e4f49726a8c01c45f77b8e151b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="abc58-104">Pašreizējās vidējās izmaksu cenas izsekošana pēc krājumu dimensijas</span><span class="sxs-lookup"><span data-stu-id="abc58-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="abc58-105">Katrai krājumu vienībai ir piesaistīta krājumu dimensiju grupa.</span><span class="sxs-lookup"><span data-stu-id="abc58-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="abc58-106">Tāpēc krājuma kārtējo vidējo izmaksu cena tiek aprēķināta, pamatojoties uz atlasītajām krājumu dimensijām, kas tiek finansiāli izsekotas.</span><span class="sxs-lookup"><span data-stu-id="abc58-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="abc58-107">Ir pieejami trīs krājumu dimensiju veidi: preces, uzglabāšanas un izsekošanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="abc58-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="abc58-108">Krājumu dimensijas ietver konfigurāciju, izmēru un krāsu.</span><span class="sxs-lookup"><span data-stu-id="abc58-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="abc58-109">Krājumu dimensijas vienmēr tiek izsekotas finansiāli.</span><span class="sxs-lookup"><span data-stu-id="abc58-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="abc58-110">Uzglabāšanas un izsekošanas dimensijas ietver vietu, noliktavu, novietojumu, krājumu statusu, noliktavas vienību, partijas numur un sērijas numuru.</span><span class="sxs-lookup"><span data-stu-id="abc58-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="abc58-111">Varat izvēlēties, kuras uzglabāšanas un izsekošanas dimensijas tiek izsekotas finansiāli.</span><span class="sxs-lookup"><span data-stu-id="abc58-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="abc58-112">**1. piemērs**</span><span class="sxs-lookup"><span data-stu-id="abc58-112">**Example 1**</span></span> 

<span data-ttu-id="abc58-113">Ja krājumu dimensiju grupa, kas ir piesaistīta krājumam, tiek finansiāli izsekota pēc noliktavas, tad kārtējo vidējo izmaksu cena tiek aprēķināta katrai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="abc58-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="abc58-114">Rēķinā ir iekļauti šādi pirkšanas pasūtījumi:</span><span class="sxs-lookup"><span data-stu-id="abc58-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="abc58-115">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 10,00 noliktavai GW.</span><span class="sxs-lookup"><span data-stu-id="abc58-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="abc58-116">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 3 un izmaksu cenu USD 12,00 noliktavai GW.</span><span class="sxs-lookup"><span data-stu-id="abc58-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="abc58-117">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 5 un izmaksu cenu USD 15,00 noliktavai MW.</span><span class="sxs-lookup"><span data-stu-id="abc58-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="abc58-118">Kārtējo vidējo izmaksu cena noliktavai GW ir USD 11,20, bet noliktavai MW tā ir USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="abc58-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="abc58-119">Tiek grāmatots pārdošanas pasūtījuma rēķins noliktavai GW.</span><span class="sxs-lookup"><span data-stu-id="abc58-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="abc58-120">Krājumu vērtība un pārdoto preču pašizmaksa (pirms krājumu slēgšanas un noliktavas iezīmēšanas) ir USD 11,20.</span><span class="sxs-lookup"><span data-stu-id="abc58-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="abc58-121">Tiek grāmatots cits pārdošanas pasūtījums noliktavai MW.</span><span class="sxs-lookup"><span data-stu-id="abc58-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="abc58-122">Krājumu vērtība un pārdoto preču pašizmaksa (pirms krājumu slēgšanas un noliktavas iezīmēšanas) ir USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="abc58-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="abc58-123">**2. piemērs.** Ja noliktavas dimensiju grupa, kas ir piesaistīta krājumam, tiek finansiāli izsekota pēc noliktavas un izsekošanas dimensiju grupa tiek finansiāli izsekota pēc partijas numura, kārtējo vidējo izmaksu cena tiek aprēķināta katrai partijai.</span><span class="sxs-lookup"><span data-stu-id="abc58-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="abc58-124">**Piezīme.** Ir ieteicams vienmēr skatīt izmaksu cenu visām izsekotajām finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="abc58-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="abc58-125">Rēķinā ir iekļauti šādi pirkšanas pasūtījumi:</span><span class="sxs-lookup"><span data-stu-id="abc58-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="abc58-126">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 10,00 noliktavai GW un partijai AAA.</span><span class="sxs-lookup"><span data-stu-id="abc58-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="abc58-127">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 3 un izmaksu cenu USD 12,00 noliktavai GW un partijai AAA.</span><span class="sxs-lookup"><span data-stu-id="abc58-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="abc58-128">Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 15,00 noliktavai GW un partijai BBB.</span><span class="sxs-lookup"><span data-stu-id="abc58-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="abc58-129">Kārtējo vidējo izmaksu cena noliktavai GW un partijai AAA ir USD 11,20, bet noliktavai MW un partijai BBB tā ir USD 15,00.</span><span class="sxs-lookup"><span data-stu-id="abc58-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




