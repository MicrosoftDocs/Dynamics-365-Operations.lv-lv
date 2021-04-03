---
title: " Preču virzīšana no sadales centra uz veikalu, izmantojot sagādes sadali"
description: Šajā procedūrā parādīts, kā izveidot un apstrādāt sagādes sadali, lai izplatītu preces no vienas vietas uz vienu vai vairākiem veikaliem.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf5dc0320e16bb53dbebc9e0bea689e0125b9827
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232838"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="37101-103"> Preču virzīšana no sadales centra uz veikalu, izmantojot sagādes sadali</span><span class="sxs-lookup"><span data-stu-id="37101-103">Push products from distribution center to store using buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37101-104">Šajā procedūrā parādīts, kā izveidot un apstrādāt sagādes sadali, lai izplatītu preces no vienas vietas uz vienu vai vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="37101-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="37101-105">Lietotājs var norādīt vairākas konfigurācijas, un sistēma ieteiks, kā sadalīt preces vai manuāli ievadīt veikalu, kur preces tiek sadalītas un kādu daudzumu sadalīt katrā veikalā.</span><span class="sxs-lookup"><span data-stu-id="37101-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="37101-106">Procedūras laikā netiek iestatīti dati, ko var izmantot sagādes sadalē, piemēram, papildināšanas kārtulas, organizācijas hierarhijas un preču svari veikalam.</span><span class="sxs-lookup"><span data-stu-id="37101-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="37101-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="37101-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="37101-108">Dodieties uz cilni Sagādes sadale.</span><span class="sxs-lookup"><span data-stu-id="37101-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="37101-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="37101-109">Click New.</span></span>
3. <span data-ttu-id="37101-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37101-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="37101-111">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="37101-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="37101-112">Laukā Noliktava ievadiet vai atlasiet noliktavu, kur ir preces ar rīcībā esošiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="37101-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="37101-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="37101-113">Click Add.</span></span>
7. <span data-ttu-id="37101-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="37101-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="37101-115">Laukā Krājuma kods ievadiet vai atlasiet preci.</span><span class="sxs-lookup"><span data-stu-id="37101-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="37101-116">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="37101-116">Click Add.</span></span>
10. <span data-ttu-id="37101-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="37101-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="37101-118">Laukā Krājuma kods ievadiet vai atlasiet preces variantu.</span><span class="sxs-lookup"><span data-stu-id="37101-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="37101-119">Ievadot preces variantus, rindas tiks izveidotas katram variantam.</span><span class="sxs-lookup"><span data-stu-id="37101-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="37101-120">Sarakstā atzīmējiet rindu.</span><span class="sxs-lookup"><span data-stu-id="37101-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="37101-121">Laukā Sadalītais daudzums ierakstiet, cik daudz atlasītās preces vēlaties sadalīt.</span><span class="sxs-lookup"><span data-stu-id="37101-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="37101-122">Laukā Papildu sadalāmais daudzums ievadiet to preču daudzumu, kurām ir pieejams sadalei nepieciešamais daudzums.</span><span class="sxs-lookup"><span data-stu-id="37101-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="37101-123">Laukā Sadale ievadiet Vietas īpatsvars.</span><span class="sxs-lookup"><span data-stu-id="37101-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="37101-124">Varat atlasīt citus veidus, kam lietot citādas sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="37101-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="37101-125">Laukā Papildināšanas hierarhija atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="37101-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="37101-126">Laukā Atbilstošie preču klāsti atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="37101-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="37101-127">Noklikšķiniet uz Aprēķināt daudzumus un pārskatiet daudzumus, kas tiek pievienoti sadaļas Noliktavas rindām.</span><span class="sxs-lookup"><span data-stu-id="37101-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="37101-128">Noklikšķiniet uz Izveidot pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="37101-128">Click Create order.</span></span>
20. <span data-ttu-id="37101-129">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="37101-129">Click Yes.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]