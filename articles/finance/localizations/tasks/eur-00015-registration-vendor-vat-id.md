---
title: EUR-00015 Kreditora PVN ID reģistrēšana
description: Šajā procedūrā parādīts, kā pievienot PVN reģistrācijas ID un nodokli, izņemot numuru kreditora kontam.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb72a5f187afe9ebe1081acd6fe0b039c370718e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227908"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="0b7b2-103">EUR-00015 Kreditora PVN ID reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="0b7b2-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b7b2-104">Šajā procedūrā parādīts, kā pievienot PVN reģistrācijas ID un nodokli, izņemot numuru kreditora kontam.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="0b7b2-105">Šis process ir līdzīgs juridiskām personām un debitoriem.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="0b7b2-106">Lai veiktu šo procedūru, jums ir jāiestata PVN ID.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="0b7b2-107">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="0b7b2-108">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Vācijā.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="0b7b2-109">Šī procedūra ir paredzēta datu pārvaldības administratoram, kreditoriem maksājamo parādu vadītājam vai debitoru parādu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="0b7b2-110">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0b7b2-111">Pārejiet uz sadaļu Kreditori > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="0b7b2-112">Sarakstā atrodiet un atlasiet kreditoru DE-01001</span><span class="sxs-lookup"><span data-stu-id="0b7b2-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="0b7b2-113">Noklikšķiniet uz Reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="0b7b2-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-114">Click Add.</span></span>
5. <span data-ttu-id="0b7b2-115">Atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-115">Select VAT ID.</span></span>
6. <span data-ttu-id="0b7b2-116">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="0b7b2-117">Norādiet PVN ID Vācijā atlasītajam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="0b7b2-118">ID ir jāatbilst reģistrācijas tipā norādītajam formātam.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="0b7b2-119">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-119">Click the General tab.</span></span>
8. <span data-ttu-id="0b7b2-120">Laukā Ir spēkā ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="0b7b2-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-121">Click Save.</span></span>
10. <span data-ttu-id="0b7b2-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-122">Click New.</span></span>
11. <span data-ttu-id="0b7b2-123">Laukā Nosaukums vai apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="0b7b2-124">Piemēram, ievadiet ITA.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="0b7b2-125">Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="0b7b2-126">Piemēram, atlasiet ITA.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="0b7b2-127">Atlasiet Jā laukā Primārais valstij.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="0b7b2-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-128">Click Save.</span></span>
15. <span data-ttu-id="0b7b2-129">Noklikšķiniet uz cilnes Apskats.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="0b7b2-130">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-130">Click Add.</span></span>
17. <span data-ttu-id="0b7b2-131">Laukā Reģistrācijas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="0b7b2-132">Piemēram, atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="0b7b2-133">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="0b7b2-134">Piemēram, norādiet PVN ID Itālijā.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="0b7b2-135">ID ir tāds pats formāts kā reģistrācijas tipam.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="0b7b2-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-136">Click Save.</span></span>
20. <span data-ttu-id="0b7b2-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-137">Close the page.</span></span>
21. <span data-ttu-id="0b7b2-138">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0b7b2-139">Piemēram, atlasiet DE-01001.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="0b7b2-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="0b7b2-141">Izvērsiet sadaļu Rēķins un piegāde.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="0b7b2-142">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-142">Click Edit.</span></span>
25. <span data-ttu-id="0b7b2-143">Laukā PVN reģistrācijas numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="0b7b2-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0b7b2-144">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]