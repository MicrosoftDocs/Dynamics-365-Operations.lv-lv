---
title: Iemeslu kodi krājumu inventarizācijai
description: Šajā tēmā ir aprakstīts, kā iestatīt un lietot iemeslu kodus inventarizācijas uzdevumiem.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "320838"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="0f79e-103">Iemeslu kodi krājumu inventarizācijai</span><span class="sxs-lookup"><span data-stu-id="0f79e-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f79e-104">Iemeslu kodi jums ļauj analizēt inventarizācijas procesa rezultātus un visas šajā procesā radušās neatbildības.</span><span class="sxs-lookup"><span data-stu-id="0f79e-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="0f79e-105">Varat norādīt iemeslu inventarizācijas veikšanai, piemēram, bojāta palete vai krājumu korekcija, kas ir balstīta uz krājumu paraugiem.</span><span class="sxs-lookup"><span data-stu-id="0f79e-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="0f79e-106">Rekomendācija</span><span class="sxs-lookup"><span data-stu-id="0f79e-106">Recommendation</span></span>

<span data-ttu-id="0f79e-107">Pirms šīs sistēmas iestatīšanas iesakām definēt stratēģiju darbam ar iemeslu kodiem.</span><span class="sxs-lookup"><span data-stu-id="0f79e-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="0f79e-108">Piemēram, mēģiniet atbildēt uz tālāk norādītajiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="0f79e-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="0f79e-109">Vai iemeslu kodiem noliktavās ir jābūt obligātiem?</span><span class="sxs-lookup"><span data-stu-id="0f79e-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="0f79e-110">Vai noteiktu vienumu iemeslu kodiem ir jābūt obligātiem vai neobligātiem?</span><span class="sxs-lookup"><span data-stu-id="0f79e-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="0f79e-111">Cik iemeslu kodu jums ir nepieciešams?</span><span class="sxs-lookup"><span data-stu-id="0f79e-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="0f79e-112">Kādā veidā iemeslu kodi ir jāizmanto svītrkoda skeneru lietotājiem?</span><span class="sxs-lookup"><span data-stu-id="0f79e-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="0f79e-113">Vai iemeslu kodiem ir jābūt sākotnēji atlasītiem, obligātiem vai nerediģējamiem?</span><span class="sxs-lookup"><span data-stu-id="0f79e-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="0f79e-114">Vai noliktavas darbiniekiem mobilajos skeneros ir nepieciešama citāda iemeslu kodu uzvedība?</span><span class="sxs-lookup"><span data-stu-id="0f79e-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="0f79e-115">Ja atbilde ir Jā, varat izveidot vairākus izvēlnes vienumus un tos piešķirt dažādām personām.</span><span class="sxs-lookup"><span data-stu-id="0f79e-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="0f79e-116">Kur tiek lietoti iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="0f79e-116">Where reason codes apply</span></span>

<span data-ttu-id="0f79e-117">Varat izveidot vairākas iemeslu kodu politikas, un katrai iemeslu kodu politikai var būt divas inventarizācijas iemesla koda politikas.</span><span class="sxs-lookup"><span data-stu-id="0f79e-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="0f79e-118">Inventarizācijas iemeslu kodu politikas var lietot noliktavas līmenī vai krājumu līmenī.</span><span class="sxs-lookup"><span data-stu-id="0f79e-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="0f79e-119">Iemeslu kodu politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0f79e-119">Set up reason code policies</span></span>

1. <span data-ttu-id="0f79e-120">Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Krājumi** \> **Inventarizācijas iemeslu kodu politikas** un izveidojiet jaunu iemeslu kodu politiku.</span><span class="sxs-lookup"><span data-stu-id="0f79e-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="0f79e-121">Laukā **Inventarizācijas iemesla koda tips** atlasiet vienumu **Obligāts** vai **Neobligāts**, lai norādītu, vai iemeslu koda atlasīšanai ir jābūt neobligātai vai obligātai darbībai vienā no tālāk norādītajiem inventarizācijas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="0f79e-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="0f79e-122">Cikla inventarizācija (mobilā ierīce)</span><span class="sxs-lookup"><span data-stu-id="0f79e-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="0f79e-123">Skaits uz vietas (mobilā ierīce)</span><span class="sxs-lookup"><span data-stu-id="0f79e-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="0f79e-124">Sliekšņa skaits (mobilā ierīce)</span><span class="sxs-lookup"><span data-stu-id="0f79e-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="0f79e-125">Ienākošās korekcijas (mobilā ierīce)</span><span class="sxs-lookup"><span data-stu-id="0f79e-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="0f79e-126">Izejošās korekcijas (mobilā ierīce)</span><span class="sxs-lookup"><span data-stu-id="0f79e-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="0f79e-127">Inventarizācijas žurnāls (bagātināts klients)</span><span class="sxs-lookup"><span data-stu-id="0f79e-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="0f79e-128">Iemeslu kodus varat iestatīt arī atsevišķām noliktavām un precēm.</span><span class="sxs-lookup"><span data-stu-id="0f79e-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="0f79e-129">Iemeslu kodu iestatīšana precēm var ignorēt iestatījumus noliktavām.</span><span class="sxs-lookup"><span data-stu-id="0f79e-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="0f79e-130">Obligātie iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="0f79e-130">Mandatory reason codes</span></span>

<span data-ttu-id="0f79e-131">Ja noliktavām vai krājumiem iemeslu kodu konfigurācijā ir iestatīts parametrs **Obligāts**, uzskaites inventarizācijas nevar pabeigt un noslēgt, kamēr nav norādīts iemesla kods.</span><span class="sxs-lookup"><span data-stu-id="0f79e-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="0f79e-132">Iemeslu kodu iestatīšana noliktavām</span><span class="sxs-lookup"><span data-stu-id="0f79e-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="0f79e-133">Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Krājumu sadalījums** \> **Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="0f79e-134">Cilnes **Noliktava** laukā **Inventarizācijas iemeslu kodu politika** atlasiet vienu no tālāk aprakstītajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="0f79e-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="0f79e-135">**Tukšs** — lai noteiktu, vai inventarizācijas žurnāli šai precei ir obligāti, tiek izmantots krājumam iestatītais parametrs.</span><span class="sxs-lookup"><span data-stu-id="0f79e-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0f79e-136">**Obligāts** — noliktavas inventarizācijas žurnāliem iemesla kods ir nepieciešams vienmēr.</span><span class="sxs-lookup"><span data-stu-id="0f79e-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="0f79e-137">**Neobligāts** — noliktavas inventarizācijas žurnāliem iemesla kods nav nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="0f79e-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="0f79e-138">Iemeslu kodu iestatīšana precēm</span><span class="sxs-lookup"><span data-stu-id="0f79e-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="0f79e-139">Atlasiet **Preču informācijas pārvaldība** \> **Preces** \> **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="0f79e-140">Cilnē **Prece** atlasiet **Inventarizācijas iemeslu kodu politika** un pēc tam atlasiet vienu no tālāk aprakstītajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="0f79e-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="0f79e-141">**Tukšs** — lai noteiktu, vai inventarizācijas žurnāli šai precei ir obligāti, tiek izmantots noliktavai iestatītais parametrs.</span><span class="sxs-lookup"><span data-stu-id="0f79e-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0f79e-142">**Obligāts** — preces inventarizācijas žurnāliem iemesla kods ir nepieciešams vienmēr.</span><span class="sxs-lookup"><span data-stu-id="0f79e-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="0f79e-143">Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.</span><span class="sxs-lookup"><span data-stu-id="0f79e-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="0f79e-144">**Neobligāts** — preces inventarizācijas žurnāliem iemesla kods nav nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="0f79e-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="0f79e-145">Šis iestatījums ignorē visus iemeslu kodu iestatījumus noliktavas līmenī.</span><span class="sxs-lookup"><span data-stu-id="0f79e-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="0f79e-146">Iemeslu kodu izmantošana inventarizācijas žurnālos</span><span class="sxs-lookup"><span data-stu-id="0f79e-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="0f79e-147">Inventarizācijas žurnālā varat pievienot iemeslu kodus tālāk uzskaitīto tipu inventarizācijām.</span><span class="sxs-lookup"><span data-stu-id="0f79e-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="0f79e-148">Cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="0f79e-148">Cycle Count</span></span>
- <span data-ttu-id="0f79e-149">Inventarizācija uz vietas</span><span class="sxs-lookup"><span data-stu-id="0f79e-149">Spot Count</span></span>
- <span data-ttu-id="0f79e-150">Sliekšņa inventarizācija</span><span class="sxs-lookup"><span data-stu-id="0f79e-150">Threshold Count</span></span>
- <span data-ttu-id="0f79e-151">Ienākošā korekcija</span><span class="sxs-lookup"><span data-stu-id="0f79e-151">Adjustment In</span></span>
- <span data-ttu-id="0f79e-152">Izejošā korekcija</span><span class="sxs-lookup"><span data-stu-id="0f79e-152">Adjustment Out</span></span>

<span data-ttu-id="0f79e-153">Iemeslu kodi tiek pievienoti žurnāla rindām inventarizācijas žurnālos ar tipu **Inventarizācijas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="0f79e-154">Atlasiet **Krājumu pārvaldība** \> **Žurnālu ieraksti** \> **Krājumu inventarizācija** \> **Inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="0f79e-155">Inventarizācijas žurnāla rindas informācijas laukā **Inventarizācijas iemesla kods** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="0f79e-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="0f79e-156">Inventarizācijas vēstures skatīšana, to ierakstot pēc iemeslu kodiem</span><span class="sxs-lookup"><span data-stu-id="0f79e-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="0f79e-157">Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Inventarizācijas vēsture** un pēc tam laukā **Inventarizācijas iemesla kods** apskatiet inventarizācijas vēsturi, kas ir ierakstīta, izmantojot kādu iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="0f79e-158">Iemesla koda izmantošana daudzuma korekcijai</span><span class="sxs-lookup"><span data-stu-id="0f79e-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="0f79e-159">Lapā **Rīcībā esošie krājumi** atlasiet **Koriģēt daudzumu**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="0f79e-160">Lapu **Rīcībā esošie krājumi** var atvērt vairākos veidos.</span><span class="sxs-lookup"><span data-stu-id="0f79e-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="0f79e-161">Piemēram, atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="0f79e-162">Atlasiet **Koriģēt daudzumu** un pēc tam laukā **Inventarizācijas iemesla kods** atlasiet kādu iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="0f79e-163">Iemeslu kodu konfigurēšana mobilās ierīces izvēlnes vienumiem</span><span class="sxs-lookup"><span data-stu-id="0f79e-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="0f79e-164">Iemeslu kodus varat konfigurēt jebkura tipa inventarizācijai mobilās ierīces izvēlnes vienumā.</span><span class="sxs-lookup"><span data-stu-id="0f79e-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="0f79e-165">Mobilās ierīces izvēlnes vienuma konfigurācija ietver tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="0f79e-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="0f79e-166">Vai iemesla kods tiek rādīts mobilās ierīces darbiniekam inventarizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="0f79e-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="0f79e-167">Noklusējuma iemesla kods, kas tiek rādīts mobilās ierīces izvēlnes vienumā.</span><span class="sxs-lookup"><span data-stu-id="0f79e-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="0f79e-168">Vai lietotājs var rediģēt šo iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="0f79e-169">Iemeslu kodu iestatīšana mobilajā ierīcē</span><span class="sxs-lookup"><span data-stu-id="0f79e-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="0f79e-170">Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes elementi**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="0f79e-171">Cilnē **Cikla inventarizācija** atlasiet **Cikla inventarizācija**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="0f79e-172">Laukā **Noklusējuma inventarizācijas iemesla kods** iestatiet noklusējuma iemesla kodu, kas ir jāieraksta, kad inventarizācija tiek veikta, izmantojot šo mobilās ierīces izvēlnes vienumu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="0f79e-173">Laukā **Rādīt inventarizācijas iemesla kodu** atlasiet **Rinda**, lai iemesla kodu rādītu pēc katras novirzes ierakstīšanas.</span><span class="sxs-lookup"><span data-stu-id="0f79e-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="0f79e-174">Vai arī — atlasiet **Slēpt**, ja iemesla kods nav jārāda.</span><span class="sxs-lookup"><span data-stu-id="0f79e-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="0f79e-175">Opciju **Rediģēt inventarizācijas iemesla kodu** iestatiet uz **Jā** vai **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="0f79e-176">Ja šo opciju iestatāt uz **Jā**, darbinieks iemesla kodu var rediģēt, kad inventarizācijas laikā tas tiek rādīts mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="0f79e-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="0f79e-177">Poga **Cikla inventarizācija** var būt iespējota jebkuram mobilās ierīces izvēlnes vienumam, kur var veikt inventarizāciju.</span><span class="sxs-lookup"><span data-stu-id="0f79e-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="0f79e-178">Piemēri tostarp ir izvēlnes vienumi inventarizācijai uz vietas, lietotāja noteiktam darbam un sistēmas noteiktam darbam.</span><span class="sxs-lookup"><span data-stu-id="0f79e-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="0f79e-179">Cikla inventarizācijas apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="0f79e-179">Cycle count approvals</span></span>

<span data-ttu-id="0f79e-180">Pirms inventarizācijas apstiprināšanas lietotājs var mainīt ar attiecīgo inventarizāciju saistīto iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="0f79e-181">Kad inventarizācija ir apstiprināta, iemesla kods tiek ievadīts inventarizācijas žurnāla rindās.</span><span class="sxs-lookup"><span data-stu-id="0f79e-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="0f79e-182">Cikla inventarizācijas apstiprinājumu modificēšana</span><span class="sxs-lookup"><span data-stu-id="0f79e-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="0f79e-183">Atlasiet **Noliktavas pārvaldība** \> **Cikla inventarizācija** \> **Izskatīšanu gaidošais cikla inventarizācijas darbs**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="0f79e-184">Atlasiet **Cikla inventarizācija** un pēc tam laukā **Iemesla kods** atlasiet jaunu iemesla kodu.</span><span class="sxs-lookup"><span data-stu-id="0f79e-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="0f79e-185">Mobilās ierīces izvēlnes vienuma modificēšana ienākošajai korekcijai un izejošajai korekcijai</span><span class="sxs-lookup"><span data-stu-id="0f79e-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="0f79e-186">Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi** un pēc tam atlasiet **Ienākošā un izejošā korekcija**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="0f79e-187">Opciju **Izmantot esošo darbu** iestatiet uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="0f79e-188">Laukā **Darba izveides process** atlasiet **Ienākošā korekcija**.</span><span class="sxs-lookup"><span data-stu-id="0f79e-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="0f79e-189">Kad darba izveides procesa laikā tiek atlasīts vienums **Ienākošā korekcija** vai **Izejošā korekcija**, mobilās ierīces izvēlnes vienumam tiek pievienoti tālāk uzskaitītie lauki.</span><span class="sxs-lookup"><span data-stu-id="0f79e-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="0f79e-190">Noklusējuma inventarizācijas iemesla kods</span><span class="sxs-lookup"><span data-stu-id="0f79e-190">Default counting reason code</span></span>
- <span data-ttu-id="0f79e-191">Rādīt inventarizācijas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="0f79e-191">Display counting reason code</span></span>
- <span data-ttu-id="0f79e-192">Rediģēt inventarizācijas iemesla kodu</span><span class="sxs-lookup"><span data-stu-id="0f79e-192">Edit counting reason code</span></span>
