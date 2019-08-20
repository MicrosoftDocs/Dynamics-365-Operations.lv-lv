---
title: Izpēte/izņēmumu novēršana
description: Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835410"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="f373c-103">Izpēte/izņēmumu novēršana</span><span class="sxs-lookup"><span data-stu-id="f373c-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f373c-104">Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.</span><span class="sxs-lookup"><span data-stu-id="f373c-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="f373c-105">Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="f373c-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="f373c-106">Kreditoru rēķinu ierobežojumi neattiecas uz rēķiniem, kas tika izveidoti rēķinu reģistrā vai rēķinu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="f373c-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="f373c-107">Rēķinu salīdzināšanas pārbaudes neizmanto kreditoru rēķinu ierobežojumus, bet tā vietā ir iestatītas lapā Kreditoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="f373c-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="f373c-108">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="f373c-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="f373c-109">Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="f373c-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="f373c-110">Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="f373c-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="f373c-111">Sagatavoties kreditoru rēķinu ierobežojumu izveidošanai</span><span class="sxs-lookup"><span data-stu-id="f373c-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="f373c-112">Pārejiet uz sadaļu Kreditori > Iestatījumi > Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="f373c-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="f373c-113">Noklikšķiniet uz cilnes Rēķinu validēšana.</span><span class="sxs-lookup"><span data-stu-id="f373c-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="f373c-114">Atzīmējiet vai notīriet izvēles rūtiņu Automātiski atjaunināt rēķina virsraksta statusu.</span><span class="sxs-lookup"><span data-stu-id="f373c-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="f373c-115">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f373c-115">Click OK.</span></span>
5. <span data-ttu-id="f373c-116">Laukā Grāmatot rēķinu ar neatbilstībām atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="f373c-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="f373c-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-117">Close the page.</span></span>
7. <span data-ttu-id="f373c-118">Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="f373c-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="f373c-119">Noklikšķiniet uz Parametri.</span><span class="sxs-lookup"><span data-stu-id="f373c-119">Click Parameters.</span></span>
9. <span data-ttu-id="f373c-120">Noklikšķiniet uz btnAdd.</span><span class="sxs-lookup"><span data-stu-id="f373c-120">Click btnAdd.</span></span>
10. <span data-ttu-id="f373c-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="f373c-122">Izveidot ierobežojuma nosacījumu tipus kreditora rēķiniem</span><span class="sxs-lookup"><span data-stu-id="f373c-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="f373c-123">Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumu nosacījumu veidi.</span><span class="sxs-lookup"><span data-stu-id="f373c-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="f373c-124">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f373c-124">Click New.</span></span>
3. <span data-ttu-id="f373c-125">Laukā Kārtulas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="f373c-126">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f373c-127">Laukā Vaicājuma nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f373c-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f373c-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f373c-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f373c-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f373c-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f373c-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f373c-130">Click Save.</span></span>
9. <span data-ttu-id="f373c-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="f373c-132">Definēt kreditora rēķina ierobežojumu</span><span class="sxs-lookup"><span data-stu-id="f373c-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="f373c-133">Pārejiet uz sadaļu Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="f373c-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="f373c-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f373c-134">Click New.</span></span>
3. <span data-ttu-id="f373c-135">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f373c-136">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f373c-137">Izvērsiet vai sakļaujiet sadaļu Politikas organizācijas.</span><span class="sxs-lookup"><span data-stu-id="f373c-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="f373c-138">Koka struktūrā atlasiet “Contoso Entertainment System USA”.</span><span class="sxs-lookup"><span data-stu-id="f373c-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="f373c-139">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="f373c-139">Click Add.</span></span>
8. <span data-ttu-id="f373c-140">Izvērsiet vai sakļaujiet sadaļu Ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="f373c-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="f373c-141">Noklikšķiniet uz Izveidot politikas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="f373c-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="f373c-142">Laukā Ierobežojuma nosacījumi ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="f373c-143">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="f373c-143">Click Filter.</span></span>
12. <span data-ttu-id="f373c-144">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="f373c-144">Click Add.</span></span>
13. <span data-ttu-id="f373c-145">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f373c-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f373c-146">Laukā Tabula noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f373c-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f373c-147">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f373c-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f373c-148">Laukā Atveidotā tabula noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f373c-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f373c-149">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f373c-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f373c-150">Laukā Lauks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f373c-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="f373c-151">Laukā Lauks ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="f373c-152">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-152">Close the page.</span></span>
21. <span data-ttu-id="f373c-153">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f373c-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="f373c-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f373c-154">Click OK.</span></span>
23. <span data-ttu-id="f373c-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f373c-155">Click OK.</span></span>
24. <span data-ttu-id="f373c-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-156">Close the page.</span></span>
25. <span data-ttu-id="f373c-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f373c-157">Close the page.</span></span>

