--- 
title: "EUR-00015 Kreditora PVN ID reģistrēšana"
description: "Šajā procedūrā parādīts, kā pievienot PVN reģistrācijas ID un nodokli, izņemot numuru kreditora kontam."
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d9788a35e768a4a289742e9cd864b3ca185a0407
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="d6d87-103">EUR-00015 Kreditora PVN ID reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="d6d87-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6d87-104">Šajā procedūrā parādīts, kā pievienot PVN reģistrācijas ID un nodokli, izņemot numuru kreditora kontam.</span><span class="sxs-lookup"><span data-stu-id="d6d87-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="d6d87-105">Šis process ir līdzīgs juridiskām personām un debitoriem.</span><span class="sxs-lookup"><span data-stu-id="d6d87-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="d6d87-106">Lai veiktu šo procedūru, jums ir jāiestata PVN ID.</span><span class="sxs-lookup"><span data-stu-id="d6d87-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="d6d87-107">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="d6d87-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="d6d87-108">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Vācijā.</span><span class="sxs-lookup"><span data-stu-id="d6d87-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="d6d87-109">Šī procedūra ir paredzēta datu pārvaldības administratoram, kreditoriem maksājamo parādu vadītājam vai debitoru parādu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="d6d87-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="d6d87-110">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="d6d87-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d6d87-111">Pārejiet uz sadaļu Kreditori > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="d6d87-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d6d87-112">Sarakstā atrodiet un atlasiet kreditoru DE-01001</span><span class="sxs-lookup"><span data-stu-id="d6d87-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="d6d87-113">Noklikšķiniet uz Reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="d6d87-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="d6d87-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d6d87-114">Click Add.</span></span>
5. <span data-ttu-id="d6d87-115">Atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="d6d87-115">Select VAT ID.</span></span>
6. <span data-ttu-id="d6d87-116">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="d6d87-117">Norādiet PVN ID Vācijā atlasītajam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="d6d87-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="d6d87-118">ID ir jāatbilst reģistrācijas tipā norādītajam formātam.</span><span class="sxs-lookup"><span data-stu-id="d6d87-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="d6d87-119">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="d6d87-119">Click the General tab.</span></span>
8. <span data-ttu-id="d6d87-120">Laukā Ir spēkā ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="d6d87-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="d6d87-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d6d87-121">Click Save.</span></span>
10. <span data-ttu-id="d6d87-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d6d87-122">Click New.</span></span>
11. <span data-ttu-id="d6d87-123">Laukā Nosaukums vai apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="d6d87-124">Piemēram, ievadiet ITA.</span><span class="sxs-lookup"><span data-stu-id="d6d87-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="d6d87-125">Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="d6d87-126">Piemēram, atlasiet ITA.</span><span class="sxs-lookup"><span data-stu-id="d6d87-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="d6d87-127">Atlasiet Jā laukā Primārais valstij.</span><span class="sxs-lookup"><span data-stu-id="d6d87-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="d6d87-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d6d87-128">Click Save.</span></span>
15. <span data-ttu-id="d6d87-129">Noklikšķiniet uz cilnes Apskats.</span><span class="sxs-lookup"><span data-stu-id="d6d87-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="d6d87-130">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="d6d87-130">Click Add.</span></span>
17. <span data-ttu-id="d6d87-131">Laukā Reģistrācijas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="d6d87-132">Piemēram, atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="d6d87-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="d6d87-133">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="d6d87-134">Piemēram, norādiet PVN ID Itālijā.</span><span class="sxs-lookup"><span data-stu-id="d6d87-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="d6d87-135">ID ir tāds pats formāts kā reģistrācijas tipam.</span><span class="sxs-lookup"><span data-stu-id="d6d87-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="d6d87-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d6d87-136">Click Save.</span></span>
20. <span data-ttu-id="d6d87-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d6d87-137">Close the page.</span></span>
21. <span data-ttu-id="d6d87-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d6d87-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6d87-139">Piemēram, atlasiet DE-01001.</span><span class="sxs-lookup"><span data-stu-id="d6d87-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="d6d87-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d6d87-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="d6d87-141">Izvērsiet sadaļu Rēķins un piegāde.</span><span class="sxs-lookup"><span data-stu-id="d6d87-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="d6d87-142">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d6d87-142">Click Edit.</span></span>
25. <span data-ttu-id="d6d87-143">Laukā PVN reģistrācijas numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d6d87-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="d6d87-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d6d87-144">Click Save.</span></span>


