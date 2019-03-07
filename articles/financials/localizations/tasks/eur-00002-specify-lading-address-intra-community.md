---
title: EUR-00002 EK iekšējo darbību iekraušanas adreses norādīšana
description: Šajā procedūrā parādīts kā norādīt iekraušanas adresi EK tirdzniecības darbībai.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db22444bee1590770a47ca5946941b530ae85ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "371289"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="b643f-103">EUR-00002 EK iekšējo darbību iekraušanas adreses norādīšana</span><span class="sxs-lookup"><span data-stu-id="b643f-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b643f-104">Šajā procedūrā parādīts kā norādīt iekraušanas adresi EK tirdzniecības darbībai.</span><span class="sxs-lookup"><span data-stu-id="b643f-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="b643f-105">Piemēram, Vācijas uzņēmums pasūta krājumus no kreditora ar vācu uzņēmuma adresi.</span><span class="sxs-lookup"><span data-stu-id="b643f-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="b643f-106">Šim kreditoram ir noliktava Itālijā, un krājumi tiek piegādāti no turienes.</span><span class="sxs-lookup"><span data-stu-id="b643f-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="b643f-107">Pārskats par šo piegādi jāsaglabā Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b643f-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="b643f-108">Tāda pati situācija ir derīga debitora atgrieztajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="b643f-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="b643f-109">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="b643f-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="b643f-110">Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā primārās adreses valsti.</span><span class="sxs-lookup"><span data-stu-id="b643f-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="b643f-111">Lai varētu veikt šo procedūru, ir jākonfigurē Intrastat pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="b643f-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="b643f-112">Šī procedūra ir paredzēta grāmatvežiem.</span><span class="sxs-lookup"><span data-stu-id="b643f-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="b643f-113">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="b643f-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b643f-114">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b643f-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b643f-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b643f-115">Click New.</span></span>
3. <span data-ttu-id="b643f-116">Ievadiet vai atlasiet kādu vērtību</span><span class="sxs-lookup"><span data-stu-id="b643f-116">Enter or select a value</span></span>
    * <span data-ttu-id="b643f-117">Piemēram, atlasiet DE-001.</span><span class="sxs-lookup"><span data-stu-id="b643f-117">For example, select DE-001.</span></span> <span data-ttu-id="b643f-118">Šis kreditoram ir Vācijas uzņēmuma adrese.</span><span class="sxs-lookup"><span data-stu-id="b643f-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="b643f-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b643f-119">Click OK.</span></span>
5. <span data-ttu-id="b643f-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b643f-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b643f-121">Laukā Krājuma kods ievadiet vai atlasiet vērtību D0001.</span><span class="sxs-lookup"><span data-stu-id="b643f-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="b643f-122">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b643f-122">Click Save.</span></span>
8. <span data-ttu-id="b643f-123">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="b643f-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="b643f-124">Noklikšķiniet uz Transportēšanas dati.</span><span class="sxs-lookup"><span data-stu-id="b643f-124">Click Transportation details.</span></span>
10. <span data-ttu-id="b643f-125">Laukā Iekraušanas datums un laiks ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="b643f-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="b643f-126">Noklikšķiniet uz Pievienot adresi.</span><span class="sxs-lookup"><span data-stu-id="b643f-126">Click Add address.</span></span>
12. <span data-ttu-id="b643f-127">Noklikšķiniet uz Jauns un izveidojiet jaunu adresi ar nolūku Iekraušana.</span><span class="sxs-lookup"><span data-stu-id="b643f-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="b643f-128">Laukā Nosaukums vai apraksts ierakstiet 'Itālijas'.</span><span class="sxs-lookup"><span data-stu-id="b643f-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="b643f-129">Atlasiet Iekraušana kā vērtību.</span><span class="sxs-lookup"><span data-stu-id="b643f-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="b643f-130">Ņemiet vērā, ka adreses nolūkam ir jābūt Iekraušana.</span><span class="sxs-lookup"><span data-stu-id="b643f-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="b643f-131">Laukā Valsts/reģions ievadiet vai atlasiet vērtību ITA.</span><span class="sxs-lookup"><span data-stu-id="b643f-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="b643f-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b643f-132">Click Save.</span></span>
17. <span data-ttu-id="b643f-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b643f-133">Close the page.</span></span>
18. <span data-ttu-id="b643f-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b643f-134">Click Save.</span></span>
    * <span data-ttu-id="b643f-135">Pārbaudiet vai iekraušanas adrese ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="b643f-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="b643f-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b643f-136">Close the page.</span></span>
20. <span data-ttu-id="b643f-137">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="b643f-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="b643f-138">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="b643f-138">Click Confirm.</span></span>
22. <span data-ttu-id="b643f-139">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="b643f-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="b643f-140">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="b643f-140">Click Invoice.</span></span>
24. <span data-ttu-id="b643f-141">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b643f-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="b643f-142">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="b643f-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="b643f-143">Noklikšķiniet uz Noklusējums no: Produktu ieejas plūsmu daudzums, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b643f-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="b643f-144">Laukā Noklusējuma daudzums rindām atlasiet opciju 'Pasūtītais daudzums'.</span><span class="sxs-lookup"><span data-stu-id="b643f-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="b643f-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b643f-145">Click OK.</span></span>
29. <span data-ttu-id="b643f-146">Noklikšķiniet uz Transportēšanas dati.</span><span class="sxs-lookup"><span data-stu-id="b643f-146">Click Transportation details.</span></span>
    * <span data-ttu-id="b643f-147">Pārbaudiet vai preces tika nosūtītas no Itālijas.</span><span class="sxs-lookup"><span data-stu-id="b643f-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="b643f-148">Ja nepieciešams, varat rediģēt iekraušanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="b643f-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="b643f-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b643f-149">Close the page.</span></span>
31. <span data-ttu-id="b643f-150">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="b643f-150">Click Post.</span></span>
32. <span data-ttu-id="b643f-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b643f-151">Close the page.</span></span>
33. <span data-ttu-id="b643f-152">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b643f-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="b643f-153">Noklikšķiniet uz Pārvest.</span><span class="sxs-lookup"><span data-stu-id="b643f-153">Click Transfer.</span></span>
35. <span data-ttu-id="b643f-154">Atlasiet Jā laukā Kreditora rēķins.</span><span class="sxs-lookup"><span data-stu-id="b643f-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="b643f-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b643f-155">Click OK.</span></span>
37. <span data-ttu-id="b643f-156">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="b643f-156">Click the General tab.</span></span>
    * <span data-ttu-id="b643f-157">Atrodiet jaunizveidoto rindu un pārbaudiet, vai sūtītājs nosūtīja preces no Itālijas.</span><span class="sxs-lookup"><span data-stu-id="b643f-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  

