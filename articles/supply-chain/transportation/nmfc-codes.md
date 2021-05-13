---
title: Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi
description: Šajā tēmā aprakstīts, kā strādāt ar Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodiem programmā Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941886"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="5980c-103">Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi</span><span class="sxs-lookup"><span data-stu-id="5980c-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5980c-104">Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi palīdz klasificēt krājumus, ko var nosūtīt.</span><span class="sxs-lookup"><span data-stu-id="5980c-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="5980c-105">NMFC kods ir apzīmējums, ko izmanto, lai grupētu preces.</span><span class="sxs-lookup"><span data-stu-id="5980c-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="5980c-106">Tas ļauj transporta uzņēmumiem novērtēt preces nosūtīšanai, klasificējot krājumus, balstoties uz tādiem apsvērumiem kā kravas automašīnas iederība, iekraušanas problēmas, apstrādes problēmas un bīstamība.</span><span class="sxs-lookup"><span data-stu-id="5980c-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="5980c-107">Preces ir grupētas vienā no 18 kravas klasēm, izmantojot skaitļu diapazonu no 50 līdz 500.</span><span class="sxs-lookup"><span data-stu-id="5980c-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="5980c-108">Klase, kurā prece ir grupēta, ir balstīta uz novērtējumu, kas norāda četras transportēšanas īpašības: blīvums, kraušanas iespēja, apstrādes un atbildība.</span><span class="sxs-lookup"><span data-stu-id="5980c-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="5980c-109">Kopā šīs īpašības veido preču transportējamību.</span><span class="sxs-lookup"><span data-stu-id="5980c-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="5980c-110">NMFC kods ir saistīts ar katru no māzāk par krāvu (LTL) piegādes krājumu.</span><span class="sxs-lookup"><span data-stu-id="5980c-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="5980c-111">Piemēram, klēpjdatoram var piešķirt NMFC, kas ir klasificēta kā 2,5, bet elektriskās instalācijas var piešķirt NMFC, kas ir klasificēta kā 65.</span><span class="sxs-lookup"><span data-stu-id="5980c-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="5980c-112">Šis līdzeklis palīdzēs darbiniekiem izmantot NMFC kodus LTL nosūtīšanas krājumu klasificēšanai.</span><span class="sxs-lookup"><span data-stu-id="5980c-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="5980c-113">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="5980c-113">Here are some examples:</span></span>

- <span data-ttu-id="5980c-114">Ja jūsu uzņēmumā ietilpst preču transporta pavadzīmes (bill of lading - BOL) kravas apraksts, pārvadātājam būs kaut kāda nojausma, par kravu.</span><span class="sxs-lookup"><span data-stu-id="5980c-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="5980c-115">Krava ir svarīga klasifikācija, jo daudzi transporta uzņēmumi izmanto visu savu biznesa modeli uz kravas tipiem, ko tie nosūta.</span><span class="sxs-lookup"><span data-stu-id="5980c-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="5980c-116">Šī klasifikācija var būt būtiska uzņēmumam, jo tā tiek izmantota, lai noteiktu dotās kravas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="5980c-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="5980c-117">Jūsu uzņēmums var noteikt LTL loģistikas un transportēšanas uzņēmuma rentabilitāti.</span><span class="sxs-lookup"><span data-stu-id="5980c-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="5980c-118">Šajā tēmā ir aprakstīts, kā strādāt ar NMFC kodiem programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5980c-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5980c-119">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5980c-119">Prerequisites</span></span>

<span data-ttu-id="5980c-120">Pirms izveidīt NMFC kodus, jāiestata visas LTL kravas klases, kas tiem ir jākartē.</span><span class="sxs-lookup"><span data-stu-id="5980c-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="5980c-121">LTL kravas klases pārstāv preču kategorijas, turpretim NMFC kodi ir saistīti ar konkrētām precēm katrā no 18 kravas kategorijām.</span><span class="sxs-lookup"><span data-stu-id="5980c-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="5980c-122">Papildinformāciju par to, kā strādāt ar LTL klasēm, skatiet sadaļā [Mazāk par kravu (LTL) klases](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="5980c-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="5980c-123">Izveidot NMFC kodu</span><span class="sxs-lookup"><span data-stu-id="5980c-123">Create an NMFC code</span></span>

<span data-ttu-id="5980c-124">Lai izveidotu NMFC kodu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5980c-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="5980c-125">Izpildiet kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="5980c-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="5980c-126">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> NMFC kodi**.</span><span class="sxs-lookup"><span data-stu-id="5980c-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="5980c-127">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas standarti \> NMFC kodi**.</span><span class="sxs-lookup"><span data-stu-id="5980c-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="5980c-128">Atlasiet **Jauns**, lai izveidotu NMFC kodu.</span><span class="sxs-lookup"><span data-stu-id="5980c-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="5980c-129">Pēc tam iestatiet tālāk minētos laukus.</span><span class="sxs-lookup"><span data-stu-id="5980c-129">Then set the following fields:</span></span>

    - <span data-ttu-id="5980c-130">**NMFC kods** - ievadiet NMFC kodu preces veidam.</span><span class="sxs-lookup"><span data-stu-id="5980c-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="5980c-131">**Nosaukums** - ievadiet elementa NMFC kodu.</span><span class="sxs-lookup"><span data-stu-id="5980c-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="5980c-132">**Par LTL klasi** — atlasiet LTL klasi, kas ir saistīta ar NMFC kodu.</span><span class="sxs-lookup"><span data-stu-id="5980c-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="5980c-133">**BOL materiālu apstrādes vienība** - definējiet noklusējuma kravas apstrādes veidu.</span><span class="sxs-lookup"><span data-stu-id="5980c-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="5980c-134">Piemērs: NMFC kodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5980c-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="5980c-135">Šajā piemērā parādīts, kā iestatīt divus dažādus NMFC kodus, ko var lietot ar dažādiem produktiem.</span><span class="sxs-lookup"><span data-stu-id="5980c-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="5980c-136">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> NMFC kodi**.</span><span class="sxs-lookup"><span data-stu-id="5980c-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="5980c-137">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5980c-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5980c-138">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="5980c-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5980c-139">**NMFC kods:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="5980c-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="5980c-140">**Nosaukums:** *Dators*</span><span class="sxs-lookup"><span data-stu-id="5980c-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="5980c-141">**LTL klase:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="5980c-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="5980c-142">**BOL materiālu apstrādes vienība:** *Vienība*</span><span class="sxs-lookup"><span data-stu-id="5980c-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="5980c-143">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5980c-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5980c-144">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5980c-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5980c-145">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="5980c-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5980c-146">**NMFC kods:** *125*</span><span class="sxs-lookup"><span data-stu-id="5980c-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="5980c-147">**Nosaukums:** *Tālruņi*</span><span class="sxs-lookup"><span data-stu-id="5980c-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="5980c-148">**LTL klase:** *125*</span><span class="sxs-lookup"><span data-stu-id="5980c-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="5980c-149">**BOL materiālu apstrādes vienība:** *Vienība*</span><span class="sxs-lookup"><span data-stu-id="5980c-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="5980c-150">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5980c-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5980c-151">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5980c-151">Additional resources</span></span>

- [<span data-ttu-id="5980c-152">Mazāk par autokravu (LTL) klases</span><span class="sxs-lookup"><span data-stu-id="5980c-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="5980c-153">Preču transporta pavadzīmes izveide</span><span class="sxs-lookup"><span data-stu-id="5980c-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
