--- 
title: "Preču virzīšana no sadales centriem uz veikaliem, izmantojot sagādes sadali"
description: "Šajā procedūrā ir parādīts, kā izveidot un apstrādāt sagādes sadali, lai preces no vienas vietas izplatītu uz vienu vai vairākiem veikaliem."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ed47b4f052dab99dec058910e4b8558481b34e59
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="push-products-from-distribution-centers-to-stores-via-buyers-push"></a><span data-ttu-id="1d86f-103">Preču virzīšana no sadales centriem uz veikaliem, izmantojot sagādes sadali</span><span class="sxs-lookup"><span data-stu-id="1d86f-103">Push products from distribution centers to stores via buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1d86f-104">Šajā procedūrā ir parādīts, kā izveidot un apstrādāt sagādes sadali, lai preces no vienas vietas izplatītu uz vienu vai vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="1d86f-104">This procedure walks through the steps to create and process a Buyer's push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="1d86f-105">Lietotājs var norādīt vairākas konfigurācijas, un sistēma ieteiks, kā sadalīt preces vai manuāli ievadīt veikalu, kur preces tiek sadalītas un kādu daudzumu sadalīt katrā veikalā.</span><span class="sxs-lookup"><span data-stu-id="1d86f-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="1d86f-106">Šajā procedūrā neietilpst sagādes sadalē izmantojamo datu iestatīšana, piemēram, papildināšanas kārtulu, organizācijas hierarhiju un preču svaru veikalam iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="1d86f-106">This procedure doesn't include setup of data that can be used in the Buyer's push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="1d86f-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="1d86f-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1d86f-108">Dodieties uz cilni Sagādes sadale.</span><span class="sxs-lookup"><span data-stu-id="1d86f-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="1d86f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1d86f-109">Click New.</span></span>
3. <span data-ttu-id="1d86f-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1d86f-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="1d86f-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1d86f-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="1d86f-112">Laukā Noliktava ievadiet vai atlasiet noliktavu, kur ir preces ar rīcībā esošiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="1d86f-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="1d86f-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1d86f-113">Click Add.</span></span>
7. <span data-ttu-id="1d86f-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1d86f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1d86f-115">Laukā Krājuma kods ievadiet vai atlasiet preci.</span><span class="sxs-lookup"><span data-stu-id="1d86f-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="1d86f-116">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1d86f-116">Click Add.</span></span>
10. <span data-ttu-id="1d86f-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1d86f-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="1d86f-118">Laukā Krājuma kods ievadiet vai atlasiet preces variantu.</span><span class="sxs-lookup"><span data-stu-id="1d86f-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="1d86f-119">Ievadot preces variantus, rindas tiks izveidotas katram variantam.</span><span class="sxs-lookup"><span data-stu-id="1d86f-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="1d86f-120">Sarakstā atzīmējiet rindu.</span><span class="sxs-lookup"><span data-stu-id="1d86f-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="1d86f-121">Laukā Sadalītais daudzums ierakstiet, cik daudz atlasītās preces vēlaties sadalīt.</span><span class="sxs-lookup"><span data-stu-id="1d86f-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="1d86f-122">Laukā Papildu sadalāmais daudzums ievadiet to preču daudzumu, kurām ir pieejams sadalei nepieciešamais daudzums.</span><span class="sxs-lookup"><span data-stu-id="1d86f-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="1d86f-123">Laukā Sadale ievadiet Vietas īpatsvars.</span><span class="sxs-lookup"><span data-stu-id="1d86f-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="1d86f-124">Varat atlasīt citus veidus, kam lietot citādas sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="1d86f-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="1d86f-125">Laukā Papildināšanas hierarhija atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1d86f-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="1d86f-126">Laukā Atbilstošie preču klāsti atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="1d86f-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="1d86f-127">Noklikšķiniet uz Aprēķināt daudzumus un pārskatiet daudzumus, kas tiek pievienoti sadaļas Noliktavas rindām.</span><span class="sxs-lookup"><span data-stu-id="1d86f-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="1d86f-128">Noklikšķiniet uz Izveidot pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="1d86f-128">Click Create order.</span></span>
20. <span data-ttu-id="1d86f-129">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1d86f-129">Click Yes.</span></span>


