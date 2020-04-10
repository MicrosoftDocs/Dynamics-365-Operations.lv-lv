---
title: Kreditoru rēķinu politiku iestatīšana
description: Šajā tēmā ir izskaidrots, kā iestatīt kreditora rēķina politiku.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143365"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="d4f0b-103">Kreditoru rēķinu politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4f0b-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4f0b-104">Šajā tēmā ir izskaidrots, kā iestatīt kreditora rēķina politiku.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="d4f0b-105">Kreditoru rēķinu politikas tiek palaistas, kad kreditora rēķinu grāmatojat, izmantojot lapu Kreditora rēķins un kad atverat kreditora rēķinu lapu Ierobežojumu pārkāpumi.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="d4f0b-106">Varat arī konfigurēt kreditora rēķina darbplūsmu, lai kreditoru rēķinu ierobežojumi tiktu palaisti katru reizi, kad darbplūsmā iesniedzat kādu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="d4f0b-107">Kreditoru rēķinu ierobežojumi neattiecas uz rēķiniem, kas tika izveidoti rēķinu reģistrā vai rēķinu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="d4f0b-108">Rēķinu salīdzināšanas pārbaudes neizmanto kreditoru rēķinu ierobežojumus, bet tā vietā ir iestatītas lapā Kreditoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="d4f0b-109">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="d4f0b-110">Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="d4f0b-111">Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="d4f0b-112">Sagatavoties kreditoru rēķinu ierobežojumu izveidošanai</span><span class="sxs-lookup"><span data-stu-id="d4f0b-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="d4f0b-113">Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Kreditori > Iestatīšana > Kreditoru parametri**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="d4f0b-114">Atlasiet cilni **Rēķinu validēšana**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="d4f0b-115">Atzīmējiet vai notīriet izvēles rūtiņu **Automātiski atjaunināt rēķina virsraksta statusu**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="d4f0b-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-116">Select **OK**.</span></span>
5. <span data-ttu-id="d4f0b-117">Laukā **Grāmatot rēķinu ar neatbilstībām** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="d4f0b-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-118">Close the page.</span></span>
7. <span data-ttu-id="d4f0b-119">Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina politikas**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="d4f0b-120">Atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="d4f0b-121">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-121">Select **Add**.</span></span>
10. <span data-ttu-id="d4f0b-122">Aizveriet lapu, lai atgrieztos lapā sākuma lapā.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="d4f0b-123">Izveidot ierobežojuma nosacījumu tipus kreditora rēķiniem</span><span class="sxs-lookup"><span data-stu-id="d4f0b-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="d4f0b-124">Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina ierobežojuma nosacījumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="d4f0b-125">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-125">Select **New**.</span></span>
3. <span data-ttu-id="d4f0b-126">Ievadiet vērtības laukos **Noteikumu nosaukums** un **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d4f0b-127">Laukā **Vaicājuma nosaukums** atlasiet nolaižamo pogu, lai atvērtu uzmeklēšanu, pēc tam atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="d4f0b-128">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-128">Select **Save**.</span></span>
6. <span data-ttu-id="d4f0b-129">Aizveriet lapu, lai atgrieztos lapā sākuma lapā.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="d4f0b-130">Definēt kreditora rēķina ierobežojumu</span><span class="sxs-lookup"><span data-stu-id="d4f0b-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="d4f0b-131">Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Politikas iestatīšana > Kreditora rēķina politikas**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="d4f0b-132">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-132">Select **New**.</span></span>
3. <span data-ttu-id="d4f0b-133">Ievadiet vērtības laukos **Nosaukums** un **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="d4f0b-134">Izvērsiet vai sakļaujiet sadaļu **Politikas organizācijas**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="d4f0b-135">Koka struktūrā atlasiet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="d4f0b-136">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-136">Select **Add**.</span></span>
7. <span data-ttu-id="d4f0b-137">Izvērsiet vai sakļaujiet sadaļu **Ierobežojuma nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="d4f0b-138">Atlasiet **Izveidot ierobežojuma nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="d4f0b-139">Laukā **Ierobežojuma nosacījumu apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="d4f0b-140">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-140">Select **Filter**.</span></span>
11. <span data-ttu-id="d4f0b-141">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-141">Select **Add**.</span></span> <span data-ttu-id="d4f0b-142">Atlasīt vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-142">Select the desired record.</span></span>
12. <span data-ttu-id="d4f0b-143">Laukā **Tabula**, **Atvasinātāstabula** un **Lauks** atlasiet vai ievadiet opcijas no nolaižamajām izvēlnēm.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="d4f0b-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-144">Close the page.</span></span>
14. <span data-ttu-id="d4f0b-145">Laukā **Kritēriji** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="d4f0b-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-146">Select **OK**.</span></span>
16. <span data-ttu-id="d4f0b-147">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-147">Select **OK**.</span></span>
17. <span data-ttu-id="d4f0b-148">Aizveriet lapas, lai atgrieztos lapā sākuma lapā.</span><span class="sxs-lookup"><span data-stu-id="d4f0b-148">Close the pages to return to the home page.</span></span>

