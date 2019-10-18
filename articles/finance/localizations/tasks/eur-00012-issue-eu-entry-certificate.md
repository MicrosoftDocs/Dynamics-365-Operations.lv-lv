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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 735331fd399ba9501031084e236b88c0e11bb179
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183784"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="70c27-103">EUR-00012 ES ieraksta sertifikāta izsniegšana</span><span class="sxs-lookup"><span data-stu-id="70c27-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70c27-104">Šajā procedūrā ir izklāstīts, kā iespējot ES ieraksta sertifikātu, konfigurēt debitora kontu ierakstu sertifikātu izmantošanai un sertifikātu izsniegšanai.</span><span class="sxs-lookup"><span data-stu-id="70c27-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="70c27-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.</span><span class="sxs-lookup"><span data-stu-id="70c27-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="70c27-106">Iespējot ieraksta sertifikāta pārvaldību</span><span class="sxs-lookup"><span data-stu-id="70c27-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="70c27-107">Pārejiet uz sadaļu Debitori > Iestatījumi > Debitoru parametri.</span><span class="sxs-lookup"><span data-stu-id="70c27-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="70c27-108">Noklikšķiniet uz cilnes Sūtījumi.</span><span class="sxs-lookup"><span data-stu-id="70c27-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="70c27-109">Izvērsiet sadaļu Ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="70c27-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="70c27-110">Atlasiet Jā laukā Iespējot ieraksta sertifikāta pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="70c27-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="70c27-111">Atlasiet Jā laukā Iespējot ieraksta sertifikāta izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="70c27-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="70c27-112">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="70c27-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="70c27-113">Sarakstā atrodiet un atlasiet rindu Ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="70c27-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="70c27-114">Laukā Numuru sērijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="70c27-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="70c27-115">Debitora iestatīšana</span><span class="sxs-lookup"><span data-stu-id="70c27-115">Set up a customer</span></span>
1. <span data-ttu-id="70c27-116">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="70c27-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="70c27-117">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="70c27-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="70c27-118">Piemēram, filtrējiet pēc lauka Konts vērtības DE-015.</span><span class="sxs-lookup"><span data-stu-id="70c27-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="70c27-119">Atveriet debitora konta detaļas.</span><span class="sxs-lookup"><span data-stu-id="70c27-119">Open customer account details.</span></span>
4. <span data-ttu-id="70c27-120">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="70c27-120">Click Edit.</span></span>
5. <span data-ttu-id="70c27-121">Izvērsiet sadaļu Rēķins un piegāde.</span><span class="sxs-lookup"><span data-stu-id="70c27-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="70c27-122">Atlasiet Jā laukā Nepieciešams ieraksta sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="70c27-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="70c27-123">Atlasiet Jā laukā Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="70c27-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="70c27-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="70c27-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="70c27-125">ES ieraksta sertifikāta automātiskā izveide</span><span class="sxs-lookup"><span data-stu-id="70c27-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="70c27-126">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="70c27-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="70c27-127">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="70c27-127">Click New.</span></span>
3. <span data-ttu-id="70c27-128">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="70c27-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="70c27-129">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="70c27-129">Click OK.</span></span>
5. <span data-ttu-id="70c27-130">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="70c27-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="70c27-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="70c27-131">Click Save.</span></span>
7. <span data-ttu-id="70c27-132">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="70c27-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="70c27-133">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="70c27-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="70c27-134">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="70c27-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="70c27-135">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="70c27-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="70c27-136">Notīriet izvēles rūtiņu Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="70c27-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="70c27-137">Ieraksta sertifikātu var izsniegt pavadzīmes grāmatošanas laikā vai pasūtījuma rēķina izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="70c27-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="70c27-138">Neatzīmējiet izvēles rūtiņu Izsniegt ieraksta sertifikātu, lai to izsniegtu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="70c27-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="70c27-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70c27-139">Click OK.</span></span>
13. <span data-ttu-id="70c27-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70c27-140">Click OK.</span></span>
14. <span data-ttu-id="70c27-141">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="70c27-142">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-142">Click Invoice.</span></span>
    * <span data-ttu-id="70c27-143">Pārbaudiet, vai sadaļā Pārskats ir atzīmētas izvēles rūtiņas Nepieciešams ieraksta sertifikāts un Izsniegt ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="70c27-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="70c27-144">Var arī atzīmēt izvēles rūtiņu Drukāt ieraksta sertifikātu, lai atļautu veikt sertifikāta izdrukas.</span><span class="sxs-lookup"><span data-stu-id="70c27-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="70c27-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70c27-145">Click OK.</span></span>
17. <span data-ttu-id="70c27-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70c27-146">Click OK.</span></span>
18. <span data-ttu-id="70c27-147">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="70c27-148">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-148">Click Invoice.</span></span>
20. <span data-ttu-id="70c27-149">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="70c27-150">Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="70c27-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="70c27-151">Klikšķiniet Drukāt.</span><span class="sxs-lookup"><span data-stu-id="70c27-151">Click Print.</span></span>
23. <span data-ttu-id="70c27-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="70c27-152">Close the page.</span></span>
24. <span data-ttu-id="70c27-153">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="70c27-153">Click Change status.</span></span>
25. <span data-ttu-id="70c27-154">Laukā Jauns statuss atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="70c27-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="70c27-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="70c27-155">Click OK.</span></span>
27. <span data-ttu-id="70c27-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="70c27-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="70c27-157">ES ieraksta sertifikāta manuālā izveide</span><span class="sxs-lookup"><span data-stu-id="70c27-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="70c27-158">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="70c27-159">Noklikšķiniet uz Izveidot ieraksta sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="70c27-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="70c27-160">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="70c27-160">Click OK.</span></span>
4. <span data-ttu-id="70c27-161">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="70c27-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="70c27-162">Noklikšķiniet uz Skatīt izsniegtos ierakstu sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="70c27-162">Click View issued entry certificates.</span></span>

