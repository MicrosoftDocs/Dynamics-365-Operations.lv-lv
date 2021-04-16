---
title: Preces īpašnieki
description: Šajā tēmā ir sniegta informācija par preces īpašniekiem. Preces īpašnieks ir lietotāju grupa, kuri ir atbildīgi par noteiktām precēm. Šos produktus var izlaist tikai grupas dalībnieki. Preces īpašnieks var tikt izmantots arī apstiprināšanas darbplūsmā.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 679712b2397f220e263da3df07ecd03c99bebf3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842036"
---
# <a name="product-owners"></a><span data-ttu-id="29d4e-106">Preces īpašnieki</span><span class="sxs-lookup"><span data-stu-id="29d4e-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29d4e-107">Preces īpašnieks ir lietotāju grupa, kuri ir atbildīgi par noteiktām precēm.</span><span class="sxs-lookup"><span data-stu-id="29d4e-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="29d4e-108">Kad preces īpašnieka grupa ir piešķirta precei, tikai šīs grupas dalībnieki var izlaist šo preci.</span><span class="sxs-lookup"><span data-stu-id="29d4e-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="29d4e-109">Preces īpašnieks var tikt izmantots arī apstiprināšanas darbplūsmā. tehnisko izmaiņu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="29d4e-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="29d4e-110">Preces īpašnieki ir globāli iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="29d4e-110">Product owners are global settings.</span></span> <span data-ttu-id="29d4e-111">Tāpēc tie ir pieejami visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="29d4e-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="29d4e-112">Preces īpašnieka grupas izveide</span><span class="sxs-lookup"><span data-stu-id="29d4e-112">Create a product owner group</span></span>

<span data-ttu-id="29d4e-113">Lai izveidotu preces īpašnieka grupu un pievienotu tai dalībniekus, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="29d4e-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="29d4e-114">Dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Preces īpašnieki**.</span><span class="sxs-lookup"><span data-stu-id="29d4e-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="29d4e-115">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="29d4e-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="29d4e-116">Laukā **Preces īpašnieks** ievadiet grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="29d4e-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="29d4e-117">Laukā **Nosaukums** ievadiet grupas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="29d4e-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="29d4e-118">Kopsavilkuma cilnē **Dalībnieki** pievienojiet darbiniekus, kuriem ir jābūt grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="29d4e-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="29d4e-119">Preces īpašnieka piešķiršana precei</span><span class="sxs-lookup"><span data-stu-id="29d4e-119">Assign a product owner to a product</span></span>

<span data-ttu-id="29d4e-120">Lai precei piešķirtu preces īpašnieku, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="29d4e-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="29d4e-121">Atveriet lapu **Preces informācija** attiecīgajai precei vai preču šablonam.</span><span class="sxs-lookup"><span data-stu-id="29d4e-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="29d4e-122">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Preces īpašnieks** atbilstīgās preces īpašnieka grupas nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="29d4e-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="29d4e-123">Kamēr preces īpašnieks ir piešķirts precei, tikai preces īpašnieka grupas dalībnieki var rediģēt **Preces īpašnieka** iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="29d4e-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="29d4e-124">Preces īpašnieks ir redzams arī lapā **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="29d4e-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="29d4e-125">Preču īpašnieki un preces laidieni</span><span class="sxs-lookup"><span data-stu-id="29d4e-125">Product owners and product releases</span></span>

<span data-ttu-id="29d4e-126">Šo preci var izlaist tikai preces īpašnieka grupas lietotāji.</span><span class="sxs-lookup"><span data-stu-id="29d4e-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="29d4e-127">Tomēr ir izņēmums, kad prece ir pakārtota prece, un tās pārstāvis tiek atbrīvots no pārstāvja īpašnieka.</span><span class="sxs-lookup"><span data-stu-id="29d4e-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="29d4e-128">Citiem vārdiem sakot, ja prece ir daļa no citas preces MK, sistēma nepārbauda katra MK krājuma preces īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="29d4e-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="29d4e-129">Tas pārbauda tikai pakārtotās preces īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="29d4e-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="29d4e-130">Piemēram, prece X ir piešķirta *Dizaina skapju* preces īpašnieku grupai.</span><span class="sxs-lookup"><span data-stu-id="29d4e-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="29d4e-131">Prece X arī ir daļa no preces Y MK, kas ir piešķirts *Dizaina skaļruņu* preces īpašnieku grupai.</span><span class="sxs-lookup"><span data-stu-id="29d4e-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="29d4e-132">Ja lietotājs no *Dizaina skaļruņu* preces īpašnieku grupas atbrīvo produktu Y un tā MK, prece X tiks izlaista kopā ar preci Y.</span><span class="sxs-lookup"><span data-stu-id="29d4e-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="29d4e-133">Preces īpašnieki un apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="29d4e-133">Product owners and approvals</span></span>

<span data-ttu-id="29d4e-134">Tā kā preces īpašnieki zina, vai īpašas tehniskās izmaiņas dos labumu viņu precēm, bieži ir lietderīgi iekļaut tās kā apstiprināšanas procesa daļu tehnisko izmaiņu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="29d4e-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="29d4e-135">Varat īstenot šo pieeju, iestatot preces īpašniekus kā dalībnieku nodrošinātājus darbplūsmās, kas tiek izmantotas tehnisko izmaiņu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="29d4e-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="29d4e-136">Pēc tam sistēma piešķirs apstiprināšanas uzdevumus darbplūsmās, pamatojoties uz precēm, kas ir tehnisko izmaiņu pieprasījumos un tehnisko izmaiņu pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="29d4e-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="29d4e-137">Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="29d4e-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]