---
title: Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus
description: Šajā tēmā ir aprakstīts, kā izveidot Excel darbgrāmatu, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459518"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="151ce-103">Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="151ce-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="151ce-104">Šajā tēmā ir aprakstīts, kā izveidot Excel darbgrāmatu, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.</span><span class="sxs-lookup"><span data-stu-id="151ce-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="151ce-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="151ce-105">Overview</span></span>

<span data-ttu-id="151ce-106">Ir pieejama iepriekš definēta Excel veidne, kurai klienti var piekļūt no dažādām sistēmas daļām un kuru var izmantot, lai rediģētu un auditētu mazumtirdzniecības darījumus.</span><span class="sxs-lookup"><span data-stu-id="151ce-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="151ce-107">Tomēr klienti šim nolūkam var arī izveidot pielāgotu Excel darbgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="151ce-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="151ce-108">Excel darbgrāmatas izveide un konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="151ce-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="151ce-109">Lai izveidotu un konfigurētu Excel darbgrāmatu un varētu rediģēt mazumtirdzniecības darījumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="151ce-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="151ce-110">Atveriet programmu Excel un izveidojiet tukšu darbgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="151ce-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="151ce-111">Cilnē **Ievietot** atlasiet **Manas pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="151ce-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="151ce-112">Labajā rūtī atlasiet saiti **Pievienot servera informāciju**.</span><span class="sxs-lookup"><span data-stu-id="151ce-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="151ce-113">Ievadiet servera vietrādi URL un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="151ce-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="151ce-114">Ja saņemat kļūdas ziņojumu “Nav atrasta neviena sīkprogrammas reģistrācija”, veiciet tālāk norādītās darbības, lai atrisinātu problēmu.</span><span class="sxs-lookup"><span data-stu-id="151ce-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="151ce-115">Programmā Commerce dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Office programmu parametri**.</span><span class="sxs-lookup"><span data-stu-id="151ce-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="151ce-116">Kopsavilkuma cilnē **Programmas parametri** atlasiet **Inicializēt programmas parametrus**.</span><span class="sxs-lookup"><span data-stu-id="151ce-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="151ce-117">Apstiprinājuma ziņojuma lodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="151ce-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="151ce-118">Kopsavilkuma cilnē **Reģistrētās sīkprogrammas** atlasiet **Inicializēt sīkprogrammu reģistrāciju**.</span><span class="sxs-lookup"><span data-stu-id="151ce-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="151ce-119">Atkārtojiet trīs iepriekšējās darbības pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="151ce-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="151ce-120">Atlasiet **Noformējums** un pēc tam atlasiet **Pievienot tabulu**.</span><span class="sxs-lookup"><span data-stu-id="151ce-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="151ce-121">Pamatojoties uz modificējamajiem datiem, atlasiet elementus, kas jāpievieno Excel darbgrāmatai rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="151ce-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="151ce-122">Izmantojiet tālāk esošo tabulu kā atsauci.</span><span class="sxs-lookup"><span data-stu-id="151ce-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="151ce-123">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="151ce-123">Transaction type</span></span> | <span data-ttu-id="151ce-124">Izmantojamie datu elementi</span><span class="sxs-lookup"><span data-stu-id="151ce-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="151ce-125">Darījumi, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, tiešsaistes pasūtījumi, asinhroni debitoru pasūtījumi, asinhroni debitoru piedāvājumi</span><span class="sxs-lookup"><span data-stu-id="151ce-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="151ce-126">Darījums (auditējams), pārdošanas darījums (auditējams), maksājumu darījumi (auditējami), nodokļu darījumi (auditējami), atlaižu darījumi (auditējami), maksas darījumi (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="151ce-127">Noguldījums bankā</span><span class="sxs-lookup"><span data-stu-id="151ce-127">Bank drop</span></span> | <span data-ttu-id="151ce-128">Darījums (auditējams), norēķinu darījumi noguldījumiem bankā (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="151ce-129">Noguldījums seifā</span><span class="sxs-lookup"><span data-stu-id="151ce-129">Safe drop</span></span> | <span data-ttu-id="151ce-130">Darījums (auditējams), norēķinu darījumi noguldījumiem seifā (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="151ce-131">Norēķinu uzskaite</span><span class="sxs-lookup"><span data-stu-id="151ce-131">Tender declaration</span></span> | <span data-ttu-id="151ce-132">Darījums (auditējams), norēķinu uzskaites darījumi (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="151ce-133">Ienākumi, izdevumi</span><span class="sxs-lookup"><span data-stu-id="151ce-133">Income, Expense</span></span> | <span data-ttu-id="151ce-134">Darījums (auditējams), ienākumu/izdevumu darījumi (auditējami), maksājumu darījumi (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="151ce-135">Sākuma summas norādīšana, norēķinu noņemšana, mainīgā ievade, izdodamā atlikuma norēķini, rēķinu apmaksa, debitora depozīts</span><span class="sxs-lookup"><span data-stu-id="151ce-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="151ce-136">Darījums (auditējams), maksājumu darījumi (auditējami)</span><span class="sxs-lookup"><span data-stu-id="151ce-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="151ce-137">Ir svarīgi katrai Excel darbgrāmatai pievienot tikai vienu datu elementu.</span><span class="sxs-lookup"><span data-stu-id="151ce-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="151ce-138">Turklāt visi lauki, kas atzīmēti ar atslēgas simbolu, ir jāpievieno atbilstošajai darbgrāmatai.</span><span class="sxs-lookup"><span data-stu-id="151ce-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="151ce-139">Pēc darbgrāmatas konfigurēšanas lietojiet pieprasītos filtrus.</span><span class="sxs-lookup"><span data-stu-id="151ce-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="151ce-140">Noteikti izmantojiet tos pašus filtrus visām faila darblapām.</span><span class="sxs-lookup"><span data-stu-id="151ce-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="151ce-141">Izvairieties no ļoti lielu datu apjomu ielādēšanas Excel failā.</span><span class="sxs-lookup"><span data-stu-id="151ce-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="151ce-142">Pretējā gadījumā var tikt ietekmēta veiktspēja, un programmas Excel un jūsu sistēmas darbība var palēnināties.</span><span class="sxs-lookup"><span data-stu-id="151ce-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="151ce-143">Kā faila filtrus iesakām vienmēr izmantot elementus “Uzņēmums” un “Pārskata numurs” vai “Darījuma numurs”.</span><span class="sxs-lookup"><span data-stu-id="151ce-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="151ce-144">Pēc filtru konfigurēšanas atlasiet **Atsvaidzināt**, lai ielādētu datus.</span><span class="sxs-lookup"><span data-stu-id="151ce-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="151ce-145">Rediģējiet vajadzīgos datus un pēc tam publicējiet tos.</span><span class="sxs-lookup"><span data-stu-id="151ce-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="151ce-146">Ja poga **Publicēt** nav pieejama, iespējams, daži galvenie lauki netika pievienoti Excel darbgrāmatai.</span><span class="sxs-lookup"><span data-stu-id="151ce-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="151ce-147">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="151ce-147">Additional resources</span></span>

[<span data-ttu-id="151ce-148">Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="151ce-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="151ce-149">Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="151ce-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="151ce-150">Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="151ce-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="151ce-151">Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="151ce-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
