---
title: Mazāk par autokravu (LTL) klases
description: Šajā tēmā skaidrots, kas ir mazāk par autokravu (LTL) klases, un apraksta, kā to iestatīt sistēmā Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941814"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="77f39-103">Mazāk par autokravu (LTL) klases</span><span class="sxs-lookup"><span data-stu-id="77f39-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77f39-104">Mazāk par autokravu (LTL) klase, ir kravas pārvadāšanas klase, ko izmanto, lai klasificētu krājumus, ko var nosūtīt.</span><span class="sxs-lookup"><span data-stu-id="77f39-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="77f39-105">Parasti katram preces veidam ir Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kods, kas atbilst noteiktam kravas klases numuram par LTL sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="77f39-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="77f39-106">LTL kravas klases pārstāv preču kategorijas, turpretim NMFC kodi ir saistīti ar konkrētām precēm katrā no 18 kravas kategorijām.</span><span class="sxs-lookup"><span data-stu-id="77f39-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="77f39-107">Šis līdzeklis ļauj izmantot sistēmu, lai veiktu šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="77f39-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="77f39-108">Nosakiet LTL kravas klases, kas tiek izmantotas jūsu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="77f39-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="77f39-109">Piešķiriet katru LTL klasi NMFC kodam lapā **NMFC kodi**.</span><span class="sxs-lookup"><span data-stu-id="77f39-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="77f39-110">Papildinformāciju skatiet [Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC)](nmfc-codes.md) kodi.</span><span class="sxs-lookup"><span data-stu-id="77f39-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="77f39-111">Piešķiriet NMFC kodu (un tādēļ tas ir saistīts ar LTL kodu) katrai precei lapā **Preces**.</span><span class="sxs-lookup"><span data-stu-id="77f39-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="77f39-112">Precīzi novērtējiet LTL klasi katrai precei, pie kuras ir piešķirts NMFC kods.</span><span class="sxs-lookup"><span data-stu-id="77f39-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="77f39-113">Nosakiet iepakojuma prasības katrai LTL klasei, pārbaudot starptautiskos LTL standartus.</span><span class="sxs-lookup"><span data-stu-id="77f39-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="77f39-114">Šādā veidā tiek nodrošināts, ka preces ir labi aizsargātas un droši nosūtītas.</span><span class="sxs-lookup"><span data-stu-id="77f39-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="77f39-115">Iegūstiet precīzus nosūtīšanas novērtējumus, balstoties uz LTL kravas klasi katrai precei.</span><span class="sxs-lookup"><span data-stu-id="77f39-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="77f39-116">Šajā tēmā aprakstīts, kā izveidot LTL klasi programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="77f39-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="77f39-117">Izveidot LTL klasi</span><span class="sxs-lookup"><span data-stu-id="77f39-117">Create an LTL class</span></span>

<span data-ttu-id="77f39-118">Lai izveidotu LTL klasi, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="77f39-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="77f39-119">Izpildiet kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="77f39-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="77f39-120">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> LTL klases**.</span><span class="sxs-lookup"><span data-stu-id="77f39-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="77f39-121">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas standarti \> LTL klases**.</span><span class="sxs-lookup"><span data-stu-id="77f39-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="77f39-122">Lai izveidotu LTL klasi, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77f39-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="77f39-123">Pēc tam iestatiet tālāk minētos laukus.</span><span class="sxs-lookup"><span data-stu-id="77f39-123">Then set the following fields:</span></span>

    - <span data-ttu-id="77f39-124">**LTL klase** – ievadiet uzņēmuma iekšējo LTL klases identifikatoru (ID) preču tipam.</span><span class="sxs-lookup"><span data-stu-id="77f39-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="77f39-125">Lielākā daļa uzņēmumu izmanto starptautisko standartu.</span><span class="sxs-lookup"><span data-stu-id="77f39-125">Most companies use the international standard.</span></span> <span data-ttu-id="77f39-126">Šādā gadījumā šī lauka vērtība atbilst lauka **Klase** vērtībai.</span><span class="sxs-lookup"><span data-stu-id="77f39-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="77f39-127">Tomēr, ja jūsu uzņēmums izmanto savu standartu, ievadiet kodu, kas atbilst standartam.</span><span class="sxs-lookup"><span data-stu-id="77f39-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="77f39-128">**Nosaukums** – ievadiet aprakstošu nosaukumu, kas jums un citiem lietotājiem palīdzēs izvēlēties pareizo LTL klasi katram NMFC kodam.</span><span class="sxs-lookup"><span data-stu-id="77f39-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="77f39-129">**Klase** – ievadiet starptautisko standarta LTL klases ID preču tipam.</span><span class="sxs-lookup"><span data-stu-id="77f39-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="77f39-130">Kodam, kuru šeit ievadāt, jāatbilst oficiālajam standartam.</span><span class="sxs-lookup"><span data-stu-id="77f39-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="77f39-131">Piemērs: LTL klašu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="77f39-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="77f39-132">Šajā piemērā parādīts, kā iestatīt divas dažādas LTL klases, ko var lietot ar dažādiem produktu tipiem.</span><span class="sxs-lookup"><span data-stu-id="77f39-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="77f39-133">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> LTL klases**.</span><span class="sxs-lookup"><span data-stu-id="77f39-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="77f39-134">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77f39-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77f39-135">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77f39-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77f39-136">**LTL klase:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="77f39-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="77f39-137">**Nosaukums:** *Datori, monitori, ledusskapji*</span><span class="sxs-lookup"><span data-stu-id="77f39-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="77f39-138">**Klase:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="77f39-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="77f39-139">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="77f39-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="77f39-140">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77f39-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77f39-141">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77f39-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77f39-142">**LTL klase:** *125*</span><span class="sxs-lookup"><span data-stu-id="77f39-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="77f39-143">**Nosaukums:** *Mazās mājsaimniecības ierīces*</span><span class="sxs-lookup"><span data-stu-id="77f39-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="77f39-144">**Klase:** *125*</span><span class="sxs-lookup"><span data-stu-id="77f39-144">**Class:** *125*</span></span>

1. <span data-ttu-id="77f39-145">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="77f39-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77f39-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="77f39-146">Additional resources</span></span>

- [<span data-ttu-id="77f39-147">Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi</span><span class="sxs-lookup"><span data-stu-id="77f39-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="77f39-148">Preču transporta pavadzīmes izveide</span><span class="sxs-lookup"><span data-stu-id="77f39-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
