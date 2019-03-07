---
title: EUR-00012 ES ieraksta sertifikāta izsniegšana
description: Šajā procedūrā ir izklāstīts, kā iespējot ES ieraksta sertifikātu, konfigurēt debitora kontu ierakstu sertifikātu izmantošanai un sertifikātu izsniegšanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a566b1d25064e3fccc8953dc883aa63bd16a301
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "371300"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="05b98-103">EUR-00012 ES ieraksta sertifikāta izsniegšana</span><span class="sxs-lookup"><span data-stu-id="05b98-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05b98-104">Šajā procedūrā ir izklāstīts, kā iespējot ES ieraksta sertifikātu, konfigurēt debitora kontu ierakstu sertifikātu izmantošanai un sertifikātu izsniegšanai.</span><span class="sxs-lookup"><span data-stu-id="05b98-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="05b98-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.</span><span class="sxs-lookup"><span data-stu-id="05b98-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="05b98-106">Iespējot ieraksta sertifikāta pārvaldību</span><span class="sxs-lookup"><span data-stu-id="05b98-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="05b98-107">Pārejiet uz sadaļu Debitori > Iestatījumi > Debitoru parametri.</span><span class="sxs-lookup"><span data-stu-id="05b98-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="05b98-108">Noklikšķiniet uz cilnes Sūtījumi.</span><span class="sxs-lookup"><span data-stu-id="05b98-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="05b98-109">Izvērsiet sadaļu Ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="05b98-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="05b98-110">Atlasiet Jā laukā Iespējot ieraksta sertifikāta pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="05b98-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="05b98-111">Atlasiet Jā laukā Iespējot ieraksta sertifikāta izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="05b98-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="05b98-112">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="05b98-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="05b98-113">Sarakstā atrodiet un atlasiet rindu Ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="05b98-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="05b98-114">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="05b98-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="05b98-115">Debitora iestatīšana</span><span class="sxs-lookup"><span data-stu-id="05b98-115">Set up a customer</span></span>
1. <span data-ttu-id="05b98-116">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="05b98-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="05b98-117">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="05b98-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="05b98-118">Piemēram, filtrējiet pēc lauka Konts vērtības DE-015.</span><span class="sxs-lookup"><span data-stu-id="05b98-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="05b98-119">Atveriet debitora konta detaļas.</span><span class="sxs-lookup"><span data-stu-id="05b98-119">Open customer account details.</span></span>
4. <span data-ttu-id="05b98-120">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="05b98-120">Click Edit.</span></span>
5. <span data-ttu-id="05b98-121">Izvērsiet sadaļu Rēķins un piegāde.</span><span class="sxs-lookup"><span data-stu-id="05b98-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="05b98-122">Atlasiet Jā laukā Nepieciešams ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="05b98-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="05b98-123">Atlasiet Jā laukā Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="05b98-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="05b98-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="05b98-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="05b98-125">ES ieraksta sertifikāta automātiskā izveide</span><span class="sxs-lookup"><span data-stu-id="05b98-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="05b98-126">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="05b98-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="05b98-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="05b98-127">Click New.</span></span>
3. <span data-ttu-id="05b98-128">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="05b98-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="05b98-129">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="05b98-129">Click OK.</span></span>
5. <span data-ttu-id="05b98-130">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="05b98-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="05b98-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="05b98-131">Click Save.</span></span>
7. <span data-ttu-id="05b98-132">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="05b98-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="05b98-133">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="05b98-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="05b98-134">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="05b98-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="05b98-135">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="05b98-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="05b98-136">Notīriet izvēles rūtiņu Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="05b98-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="05b98-137">Ieraksta sertifikātu var izsniegt pavadzīmes grāmatošanas laikā vai pasūtījuma rēķina izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="05b98-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="05b98-138">Neatzīmējiet izvēles rūtiņu Izsniegt ieraksta sertifikātu, lai to izsniegtu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="05b98-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="05b98-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05b98-139">Click OK.</span></span>
13. <span data-ttu-id="05b98-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05b98-140">Click OK.</span></span>
14. <span data-ttu-id="05b98-141">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="05b98-142">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-142">Click Invoice.</span></span>
    * <span data-ttu-id="05b98-143">Pārbaudiet, vai sadaļā Pārskats ir atzīmētas izvēles rūtiņas Nepieciešams ieraksta sertifikāts un Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="05b98-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="05b98-144">Var arī atzīmēt izvēles rūtiņu Drukāt ieraksta sertifikātu, lai atļautu veikt sertifikāta izdrukas.</span><span class="sxs-lookup"><span data-stu-id="05b98-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="05b98-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05b98-145">Click OK.</span></span>
17. <span data-ttu-id="05b98-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05b98-146">Click OK.</span></span>
18. <span data-ttu-id="05b98-147">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="05b98-148">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-148">Click Invoice.</span></span>
20. <span data-ttu-id="05b98-149">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="05b98-150">Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="05b98-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="05b98-151">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="05b98-151">Click Print.</span></span>
23. <span data-ttu-id="05b98-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="05b98-152">Close the page.</span></span>
24. <span data-ttu-id="05b98-153">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="05b98-153">Click Change status.</span></span>
25. <span data-ttu-id="05b98-154">Laukā Jauns statuss atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="05b98-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="05b98-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="05b98-155">Click OK.</span></span>
27. <span data-ttu-id="05b98-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="05b98-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="05b98-157">ES ieraksta sertifikāta manuālā izveide</span><span class="sxs-lookup"><span data-stu-id="05b98-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="05b98-158">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="05b98-159">Noklikšķiniet uz Izveidot ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="05b98-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="05b98-160">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="05b98-160">Click OK.</span></span>
4. <span data-ttu-id="05b98-161">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="05b98-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="05b98-162">Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="05b98-162">Click View issued entry certificates.</span></span>

