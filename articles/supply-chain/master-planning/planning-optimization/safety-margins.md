---
title: Drošības rezerves
description: Šajā tēmā aprakstīts, kā drošības rezerves var izmantot ar Plānošanas optimizācijas pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4a15b1c3df5de1dc5a55cfaa08686ee85ed50ba3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236031"
---
# <a name="safety-margins"></a><span data-ttu-id="9d8f7-103">Drošības rezerves</span><span class="sxs-lookup"><span data-stu-id="9d8f7-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d8f7-104">Šajā tēmā aprakstīts, kā drošības rezerves var izmantot ar Plānošanas optimizācijas pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="9d8f7-105">Drošības rezervju apskats</span><span class="sxs-lookup"><span data-stu-id="9d8f7-105">Safety margins overview</span></span>

<span data-ttu-id="9d8f7-106">Drošības rezervju nolūks ir iespējot iestatījumu, kas nodrošina zināmu bufera laiku pēc parastā izpildes laika.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="9d8f7-107">Piemēram, ja materiālam jābūt izsaiņotam vai pārbaudītam pēc tā saņemšanas no kreditora, jūs nevarat vienkārši pievienot papildu laiku pirkšanas izpildes laikam, jo šī pieeja piegādātājam dos papildu bufera laiku.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="9d8f7-108">Šajā piemērā ieejas plūsmas rezerve var tikt izmantota, lai nodrošinātu, ka piegādātājs piegādā agrāk.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="9d8f7-109">Šī pieeja nodrošina bufera laiku, lai preces varētu apstrādāt iekšēji.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="9d8f7-110">Ir pieejami trīs drošības rezervju veidi.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="9d8f7-111">**Pasūtījuma rezerve** – bufera laiks piegādes pasūtījuma izvietošanai</span><span class="sxs-lookup"><span data-stu-id="9d8f7-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="9d8f7-112">**Ieejas plūsmas rezerve** – bufera laiks ienākošās piegādes apstrādei</span><span class="sxs-lookup"><span data-stu-id="9d8f7-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="9d8f7-113">**Izejas plūsmas rezerve** – kravu apstrādes bufera laiks</span><span class="sxs-lookup"><span data-stu-id="9d8f7-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="9d8f7-114">Šajā attēlā parādīts, kā šīs drošības rezerves tiek piemērotas laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-114">The following illustration shows how these safety margins apply over time.</span></span>

![Drošības rezerves](media/safety-margins-1.png)

<span data-ttu-id="9d8f7-116">Visas rezerves ir definētas dienās.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-116">All margins are defined in days.</span></span> <span data-ttu-id="9d8f7-117">Noklusējuma vērtība, *0* (nulle), norāda, ka rezerve netiek lietota.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="9d8f7-118">Iestatot vairākas vezerves, tās visas pievieno kopējam laikam no piegādes *pasūtījuma datuma* līdz pieprasījuma *vajadzības datumam* .</span><span class="sxs-lookup"><span data-stu-id="9d8f7-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="9d8f7-119">Piemēram, iestatījumam nav izpildes laika, un visi trīs vezervju veidi ir iestatīti uz vienu dienu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="9d8f7-120">Šādā gadījumā starp piegādes pasūtījuma datumu un pieprasījuma vajadzības datumu būs trīs dienas, tātad, ja pasūtījuma datums ir 1. jūlijs, vajadzības datums ir 4. jūlijs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="9d8f7-121">Ieejas plūsmas rezerve</span><span class="sxs-lookup"><span data-stu-id="9d8f7-121">Receipt margin</span></span>

<span data-ttu-id="9d8f7-122">Ieejas plūsmas rezerve visticamāk tiek izmantota trijās drošības rezervēs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="9d8f7-123">Tā ir piemērota *izpildes datumam* un pretēji no *pieprasījuma datuma*.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="9d8f7-124">Citiem vārdiem, preces jāsaņem pirms norādītā saņemšanas uzcenojuma dienu skaita no tās dienas, kad tās tiek pieprasītas.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="9d8f7-125">Sekojošajā attēlā ir parādīta ieejas plūsmas rezerve.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-125">The following illustration highlights the receipt margin.</span></span>

![Ieejas plūsmas rezerve](media/safety-margins-2.png)

<span data-ttu-id="9d8f7-127">Parasti ieejas plūsmas rezerve tiek izmantota kā buferis, lai nodrošinātu noliktavas reģistrācijas laiku vai citus laikietilpīgus procesus, kas netiek uztverti kā daļa no vispārējā izpildes laika sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="9d8f7-128">Pirkumiem viena priekšrocība ir tāda, ka pirkšanas pasūtījuma *piegādes datums* tiek attiecīgi pārvietots uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="9d8f7-129">Palielinot izpildes laiku tā vietā, lai izmantotu drošības rezervi, kreditoram joprojām tiks lūgts veikt piegādi pēdējā minūtē.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="9d8f7-130">Ievērojiet, ka ieejas plūsmas rezerve nemaina piegādes *vajadzības datumu*.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="9d8f7-131">Tāpēc ieejas plūsmas rezerve nav tieši redzama, ja tiek salīdzināti pieprasījuma un piedāvājuma vajadzības datumi (piemēram, lapā **Neto vajadzības** ).</span><span class="sxs-lookup"><span data-stu-id="9d8f7-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="9d8f7-132">Piemēram, ja ieejas plūsmas rezerve ir iestatīta uz četrām dienam un pirkšanas pasūtījuma rinda ir plānota saņemšanai mēneša piecpadsmitajā datumā, vispārējā plānošana par koriģēto saņemšanas datumu aprēķina mēneša deviņpadsmito datumu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="9d8f7-133">Ņemiet vērā, ka ieejas plūsmas rezerve netiek lietota, kad piegādei tiek izmantots rīcībā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="9d8f7-134">Visi rīcībā esošie krājumi tiek uzskatīti par pieejamiem nekavējoties, neskatoties uz to, kad tie tika faktiski saņemti.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="9d8f7-135">Pasūtījuma rezerve</span><span class="sxs-lookup"><span data-stu-id="9d8f7-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="9d8f7-136">**Drīzumā:** Šis līdzeklis vēl nav atbalstīts Plānošanas optimizācijai.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="9d8f7-137">Kamēr tas netiek atbalstīts, visas vērtības, kas ir ievadītas **Pasūtījuma rezervei, kas pievienota krājumu izpildes laikam** tiks traktētas kā *0* (nulle).</span><span class="sxs-lookup"><span data-stu-id="9d8f7-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="9d8f7-138">Sekojošajā attēlā ir parādīta pasūtījuma rezerve.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-138">The following illustration highlights the reorder margin.</span></span>

![Pasūtījuma rezerve](media/safety-margins-3.png)

<span data-ttu-id="9d8f7-140">Pasūtījuma rezerve tiek pievienota pirms krājuma izpildes laika visiem plānotajiem pasūtījumiem vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="9d8f7-141">Tāpēc tā nodrošina papildu laiku piegādes pasūtījuma ievietošanai.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="9d8f7-142">Šī rezerve parasti tiek izmantota kā buferis, lai nodrošinātu laiku apstiprināšanas procesiem vai citiem iekšējiem procesiem, kas ir nepieciešami piegādes pasūtījumu izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="9d8f7-143">Pasūtījuma rezerve tiek novietota starp piegādes *pasūtījuma datumam* un *sākuma datumam*.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="9d8f7-144">Izejas plūsmas rezerve</span><span class="sxs-lookup"><span data-stu-id="9d8f7-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="9d8f7-145">**Drīzumā:** Šis līdzeklis vēl nav atbalstīts Plānošanas optimizācijai.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="9d8f7-146">Kamēr tā netiek atbalstīta, visas vērtības, kas ir ievadītas **Izejas plūsmas rezervei, kas atskaitīta no vajadzības datuma** tiks traktētas kā *0* (nulle).</span><span class="sxs-lookup"><span data-stu-id="9d8f7-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="9d8f7-147">Sekojošajā attēlā ir parādīta izejas plūsmas rezerve.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-147">The following illustration highlights the issue margin.</span></span>

![Izejas plūsmas rezerve](media/safety-margins-4.png)

<span data-ttu-id="9d8f7-149">Vispārējās plānošanas laikā izejas plūsmas rezerve tiek atskaitīta no pieprasījuma vajadzības datuma.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="9d8f7-150">Tas palīdz nodrošināt, ka ir laiks reaģēt un nosūtīt ienākošos pieprasījuma pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="9d8f7-151">Šo rezervi parasti izmanto kā buferi, lai nodrošinātu nosūtīšanas laiku un saistītos nosūtīšanas noliktavas procesus.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="9d8f7-152">Ievērojiet, ka tad, kad tiek lietota izejas plūsmas rezerve, saistītie piedāvājuma un pieprasījuma datumi nesakrīt.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="9d8f7-153">Tā vietā tie atšķiras ar izejas plūsmas rezervi, jo izejas plūsmas rezerve tiek pievienota starp piegādes *vajadzības datumu* un pieprasījuma *vajadzības datumu*.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="9d8f7-154">Iestatīt drošības rezerves</span><span class="sxs-lookup"><span data-stu-id="9d8f7-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="9d8f7-155">Ieslēgt drošības rezerves Līdzekļu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="9d8f7-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="9d8f7-156">Lai varētu izmantot šo līdzekli ar Plānošanas optimizāciju, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="9d8f7-157">Administratori var izmantot [Līdzekļu pārvaldības](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9d8f7-158">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="9d8f7-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9d8f7-159">**Modulis:** _Vispārējā plānošana_</span><span class="sxs-lookup"><span data-stu-id="9d8f7-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="9d8f7-160">**Līdzekļa nosaukums:** _Rezervi Plānošanas optimizācijai_</span><span class="sxs-lookup"><span data-stu-id="9d8f7-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="9d8f7-161">Definēt drošības rezerves</span><span class="sxs-lookup"><span data-stu-id="9d8f7-161">Define safety margins</span></span>

<span data-ttu-id="9d8f7-162">Drošības rezervēm ir elastīga iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="9d8f7-163">Tos var iestatīt gan *seguma grupai*, gan *vispārējam plānam* .</span><span class="sxs-lookup"><span data-stu-id="9d8f7-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="9d8f7-164">Ir svarīgi saprast, ka rezerves tiek pievienotas viena otrai virsū.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="9d8f7-165">Piemēram, ieejas plūsmas rezerve seguma grupai divām dienam un trījām dienam vispārējām plānam radīs efektīvu ieejas plūsmas rezervi piecām dienām.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="9d8f7-166">Iespēja iestatīt rezervi vispārējām plānam var būt noderīga, ja vēlaties simulēt ilgāku izpildes laiku vai nenoteiktību konkrētam plānam, bet neietekmējot ikdienas plānošanu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="9d8f7-167">Seguma grupas drošības rezerves</span><span class="sxs-lookup"><span data-stu-id="9d8f7-167">Coverage group safety margins</span></span>

<span data-ttu-id="9d8f7-168">Lai pielietotu drošības rezervi seguma grupai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="9d8f7-169">Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Seguma grupas**.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="9d8f7-170">Sarakstu rūtī atlasiet nepieciešamo seguma grupu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="9d8f7-171">Kopsavilkuma cilnē **Cits** sadaļā **Drošības rezerves dienās** izmantojiet sekojošos laukus, lai iestatītu nepieciešamās drošības rezerves (dienās):</span><span class="sxs-lookup"><span data-stu-id="9d8f7-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="9d8f7-172">Pievienotā ieejas plūsma pieprasījuma datumam</span><span class="sxs-lookup"><span data-stu-id="9d8f7-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="9d8f7-173">Atskaitītā izejas plūsma no pieprasījuma datuma</span><span class="sxs-lookup"><span data-stu-id="9d8f7-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="9d8f7-174">Pasūtījuma rezerve, kas pievienota krājumam izpildes laikā</span><span class="sxs-lookup"><span data-stu-id="9d8f7-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="9d8f7-175">Vispārējā plāna drošības rezerves</span><span class="sxs-lookup"><span data-stu-id="9d8f7-175">Master plan safety margins</span></span>

<span data-ttu-id="9d8f7-176">Lai pielietotu drošības rezervi vispārējām plānam, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="9d8f7-177">Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="9d8f7-178">Sarakstu rūtī atlasiet nepieciešamo vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="9d8f7-179">Kopsavilkuma cilnē **Drošības rezerves dienās** izmantojiet sekojošos laukus, lai iestatītu nepieciešamās drošības rezerves (dienās):</span><span class="sxs-lookup"><span data-stu-id="9d8f7-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="9d8f7-180">Pievienotā ieejas plūsma pieprasījuma datumam</span><span class="sxs-lookup"><span data-stu-id="9d8f7-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="9d8f7-181">Atskaitītā izejas plūsma no pieprasījuma datuma</span><span class="sxs-lookup"><span data-stu-id="9d8f7-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="9d8f7-182">Pasūtījuma rezerve, kas pievienota krājumam izpildes laikā</span><span class="sxs-lookup"><span data-stu-id="9d8f7-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="9d8f7-183">Definējiet, vai aprēķini ir balstīti uz kalendārajām dienām vai darba dienām</span><span class="sxs-lookup"><span data-stu-id="9d8f7-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="9d8f7-184">Varat iestatīt visas drošības rezerves tā, lai tās tiktu aprēķinātas, balstoties uz kalendāra dienām vai darba dienām.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="9d8f7-185">Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="9d8f7-186">Cilnē **Vispārīgi** sadaļā **Drošības rezerves dienās** iestatiet opciju **Darba dienas** uz *Jā*, lai aprēķinātu rezerves, balstoties uz darbdienām.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="9d8f7-187">Iestatiet opciju uz *Nē*, lai aprēķinātu rezerves, pamatojoties uz kalendārām dienām.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="9d8f7-188">Piemēram, kalendārs ir atvērts no pirmdienas līdz piektdienai un ir slēgts no sestdienas līdz svētdienai.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="9d8f7-189">Ja ir vienas dienas ieejas plūsmas rezerve, vajadzības datums pirmdien izveido piegādes datumu iepriekšējā piektdienā, jo sestdienas un svētdienas nav darba dienas.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="9d8f7-190">Kalendārs, kas tiek izmantots darba dienu noteikšanai, ir atkarīgs no iestatījuma un piegādes veida.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="9d8f7-191">To var kontrolēt seguma grupas, noliktavas un kreditora kalendāri.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="9d8f7-192">Ja *noliktava* nav daļa no seguma dimensijas (citiem vārdiem, plānošana ir balstīta tikai uz *vietnes*), noliktavas kalendārs netiek lietots.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="9d8f7-193">Sistēma var apstrādāt iestatījumu, kur ir definēti viens vai vairāki kalendāri.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="9d8f7-194">Šajās apakšsadaļās ir aprakstītas iespējamās kombinācijas, ko var izmantot, lai kontrolētu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="9d8f7-195">Kalendārs, kas tiek izmantots ilgumam</span><span class="sxs-lookup"><span data-stu-id="9d8f7-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="9d8f7-196">Definētie kalendāri kontrolē faktisko kopējās izpildes laiku kalendārās dienās no piegādes pasūtījuma datuma līdz pieprasījuma vajadzības datumam.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="9d8f7-197">Tiek izmantota šāda kalendāra prioritātes noteikšana:</span><span class="sxs-lookup"><span data-stu-id="9d8f7-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="9d8f7-198">**Pirkšanas izpildes laiks** – tiek ņemts vērā tikai seguma grupas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="9d8f7-199">**Ieejas plūsmas rezerve** – seguma grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-200">Pretējā gadījumā tiek izmantots noliktavas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="9d8f7-201">**Izejas plūsmas rezerve** – seguma grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-202">Pretējā gadījumā tiek izmantots noliktavas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="9d8f7-203">**Pasūtījuma rezerve** – tiek ņemts vērā tikai seguma grupas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="9d8f7-204">Kalendārs, kas tiek izmantots beigu datumam</span><span class="sxs-lookup"><span data-stu-id="9d8f7-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="9d8f7-205">Lai noteiktu, vai plānošanas programma konkrētajam datuma veidam var izmantot norādīto datumu, tiek piemēroti šādi noteikumi:</span><span class="sxs-lookup"><span data-stu-id="9d8f7-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="9d8f7-206">**Pirkšanas saņemšanas datums** – tiek izmantots kreditora kalendārs, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-207">Pretējā gadījumā seguma grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-208">Ja neviens no šiem kalendāriem nav definēts, tiek izmantots noliktavas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="9d8f7-209">**Pārsūtīšanas saņemšanas datums** – seguma grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-210">Pretējā gadījumā tiek izmantots noliktavas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="9d8f7-211">**Ražošanas saņemšanas datums** – seguma grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-212">Pretējā gadījumā tiek izmantots noliktavas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="9d8f7-213">**Pieprasījuma jautājuma atvēršanas diena** – noliktavas grupas kalendārs tiek lietots, ja tas ir definēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="9d8f7-214">Pretējā gadījumā tiek lietots seguma grupas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="9d8f7-215">**Pasūtījuma atvēršanas diena** – tiek izmantota seguma grupas kalendāra un kreditora kalendāra kombinācija (krustošanās).</span><span class="sxs-lookup"><span data-stu-id="9d8f7-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="9d8f7-216">Lai izmantotu šo datumu, abiem kalendāriem ir jābūt atvērtiem.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="9d8f7-217">Ja tikai viens no šiem kalendāriem ir definēts, tiek izmantots tikai tas kalendārs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="9d8f7-218">Kalendāra iestatīšanas pārskata matrica</span><span class="sxs-lookup"><span data-stu-id="9d8f7-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="9d8f7-219">Sekojošajā attēlā redzama matrica, kas apkopo, kuri kalendāri tiek lietoti, aprēķinot drošības rezerves.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="9d8f7-220">(Atlasiet attēlu, lai atvērtu augstas izšķirtspējas versiju.) Šādi saīsinājumi un krāsas tiek izmantotas, lai norādītu, kur katrs kalendāra tips ir norādīts:</span><span class="sxs-lookup"><span data-stu-id="9d8f7-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="9d8f7-221">**Seguma grupa (Coverage group - CG):** Zaļa</span><span class="sxs-lookup"><span data-stu-id="9d8f7-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="9d8f7-222">**Noliktava (Warehouse - WH):** Dzeltena</span><span class="sxs-lookup"><span data-stu-id="9d8f7-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="9d8f7-223">**Kreditors (Vendor - V):** Zila</span><span class="sxs-lookup"><span data-stu-id="9d8f7-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="9d8f7-224">[![Kalendāra iestatīšanas pārskata matrica](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="9d8f7-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="9d8f7-225">Kavējumu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="9d8f7-225">Calculating delays</span></span>

<span data-ttu-id="9d8f7-226">Visi trīs drošības rezervju veidi tiek iekļauti, kad sistēma nosaka, vai pasūtījums ir aizkavēts.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="9d8f7-227">Piemēram, krājumam ir vienas dienas izpildes laiks un trīs dienu ieejas plūsmas rezerve.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="9d8f7-228">Pārdošanas pasūtījums šim krājumam ir iestatīts kā nepieciešams šodien.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="9d8f7-229">Šādā gadījumā aizkave tiek aprēķināta kā *izpildes laiks* + *ieejas plūsmas rezerve* = četras dienas.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="9d8f7-230">Tāpēc, ja šodien ir 14. augusts, četras aizkaves dienas veido piegādi 18. augustā.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="9d8f7-231">Tālāk redzamajā attēlā parādīts šis piemērs.</span><span class="sxs-lookup"><span data-stu-id="9d8f7-231">The following illustration shows this example.</span></span>

![Kavējuma aprēķina piemērs](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="9d8f7-233">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9d8f7-233">Additional resources</span></span>

[<span data-ttu-id="9d8f7-234">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="9d8f7-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9d8f7-235">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="9d8f7-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]