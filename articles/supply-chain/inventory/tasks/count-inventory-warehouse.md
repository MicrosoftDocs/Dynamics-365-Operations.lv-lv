---
title: Krājumu skaitīšana noliktavā
description: Šajā tēmā aprakstīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204175"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="cda85-103">Krājumu skaitīšana noliktavā</span><span class="sxs-lookup"><span data-stu-id="cda85-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cda85-104">Šajā tēmā aprakstīts krājumu inventarizācijas žurnāla izveides un grāmatošanas process, lai saskaitītu noteiktu krājumu novietojumā attiecīgajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="cda85-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="cda85-105">Procedūra attiecas uz "pamata noliktavas" funkcionalitāti, kas pieejama krājumu vadības modulī, nevis uz noliktavas funkcionalitāti, kas ir pieejama noliktavas vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="cda85-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="cda85-106">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="cda85-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="cda85-107">Ja izmantojat savus datus, pārliecinieties, ka ir izveidoti produkti un novietojumi un ka esat izveidojis krājumu žurnāla nosaukumu inventarizācijas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="cda85-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="cda85-108">Krājumu inventarizāciju parasti veic noliktavas darbinieks.</span><span class="sxs-lookup"><span data-stu-id="cda85-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="cda85-109">Izveidojiet krājumu inventarizācijas žurnālu</span><span class="sxs-lookup"><span data-stu-id="cda85-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="cda85-110">Dodieties uz sadaļu **Navigācijas rūts > Moduļi > Krājumu pārvaldība > Žurnāla ieraksti > Krājumu inventarizācija > Inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="cda85-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="cda85-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cda85-111">Select **New**.</span></span>
3. <span data-ttu-id="cda85-112">Laukā **Nosaukums** atlasiet krājumu inventarizācijas žurnāla nosaukumu, kuru vēlaties izmantot no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="cda85-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="cda85-113">Daži citi lauki tiks aizpildīti, pamatojoties uz atlasītajiem krājumu inventarizācijas žurnāla nosaukuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="cda85-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="cda85-114">Laukā **Darbinieks** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cda85-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cda85-115">Sarakstā **Aylasiet** darbinieku, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="cda85-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="cda85-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cda85-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="cda85-117">Izveidot žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="cda85-117">Create journal lines</span></span>
1. <span data-ttu-id="cda85-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cda85-118">Select **New**.</span></span>
2. <span data-ttu-id="cda85-119">Laukā **Krājuma kods** nolaižamamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cda85-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="cda85-120">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet **A0001**.</span><span class="sxs-lookup"><span data-stu-id="cda85-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="cda85-121">Laukā **Vieta** nolaižamamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cda85-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="cda85-122">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet vietu **2**.</span><span class="sxs-lookup"><span data-stu-id="cda85-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="cda85-123">Laukā **Noliktava** nolaižamamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cda85-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="cda85-124">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet noliktavu **24**.</span><span class="sxs-lookup"><span data-stu-id="cda85-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="cda85-125">Laukā **Atrašanās vieta** nolaižamamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cda85-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="cda85-126">Ja izmantojat uzņēmuma USMF demonstrācijas datus, atlasiet atrašanās vietu **Lielapjoma-001**.</span><span class="sxs-lookup"><span data-stu-id="cda85-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="cda85-127">Laukā Saskaitīts ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cda85-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="cda85-128">Ja ievadāt saskaitīto skaitu, kas atšķiras no laukā **Rīcībā esošs** parādītā skaita, lauks **Daudzums** tiek atjaunināts, lai parādītu neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="cda85-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="cda85-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cda85-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="cda85-130">Krājumu inventarizācijas žurnāla grāmatošana</span><span class="sxs-lookup"><span data-stu-id="cda85-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="cda85-131">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="cda85-131">Select **Post**.</span></span> <span data-ttu-id="cda85-132">Grāmatojot krājumu inventarizācijas žurnālu, ja saskaitītais skaits atšķiras no skaita, kas norādīts laukā **Rīcībā esošs**, tiek grāmatota krājumu ieejas plūsma vai izejas plūsma, tiek mainīts krājumu līmenis un vērtība un tiek ģenerētas virsgrāmatas darbības.</span><span class="sxs-lookup"><span data-stu-id="cda85-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="cda85-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cda85-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="cda85-134">Skatiet krājumu darbības</span><span class="sxs-lookup"><span data-stu-id="cda85-134">View inventory transactions</span></span>
1. <span data-ttu-id="cda85-135">Atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="cda85-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="cda85-136">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="cda85-136">Select **Transactions**.</span></span> <span data-ttu-id="cda85-137">Šeit varat redzēt saistītās darbības, kas tiks izveidotas, grāmatojot krājumu inventarizācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="cda85-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

