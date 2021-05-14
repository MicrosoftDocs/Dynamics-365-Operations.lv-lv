---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923029"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="5ff1d-103">Bieži uzdotie jautājumi par finanšu pārskatu veidošanu</span><span class="sxs-lookup"><span data-stu-id="5ff1d-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="5ff1d-104">Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="5ff1d-105">Kā var ierobežot piekļuvi pārskatam, izmantojot koka drošību?</span><span class="sxs-lookup"><span data-stu-id="5ff1d-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="5ff1d-106">Šajā piemērā parādīts, kā ierobežot piekļuvi pārskatam, izmantojot koka drošību.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="5ff1d-107">USMF demonstrācijas uzņēmumam ir bilances pārskats, kuram nedrīkstētu piekļūt visi finanšu pārskatu lietotāji.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="5ff1d-108">Lai ierobežotu piekļuvi, varat izmantot koka drošību, lai ierobežotu piekļuvi atsevišķam pārskatam, lai tikai noteikti lietotāji varētu piekļūt pārskatam.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="5ff1d-109">Lai ierobežotu piekļuvi, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="5ff1d-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="5ff1d-110">Pierakstieties rīkā Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="5ff1d-111">Izveidojiet jaunu koka definīciju.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-111">Create a new tree definition.</span></span> <span data-ttu-id="5ff1d-112">Go to **Fails > Jauns > Koka definīcija**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="5ff1d-113">Veiciet dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="5ff1d-114">Atlasiet **Lietotāji un grupas**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="5ff1d-115">Atlasiet lietotājus vai grupu, kam vajadzīga piekļuve šim pārskatam.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="5ff1d-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-116">Select **Save**.</span></span>
7. <span data-ttu-id="5ff1d-117">Pārskata definīcijā pievienojiet jaunu koka definīciju.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="5ff1d-118">Koka definīcijā atlasiet **Iestatījums**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="5ff1d-119">Sadaļā **Pārskata vienību atlase** atlasiet **Iekļaut visas vienības**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="5ff1d-120">Kā var noteikt, kuri konti neatbilst manām bilancēm?</span><span class="sxs-lookup"><span data-stu-id="5ff1d-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="5ff1d-121">Ja jums ir pārskats, kurā nav saskaņotu bilanču, tālāk norādītas dažas darbības, ko varat veikt, lai identificētu šos kontus un novirzes.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="5ff1d-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="5ff1d-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="5ff1d-123">Rīkā Financial Reporter Report Designer izveidojiet jaunu rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="5ff1d-124">Atlasiet **Rediģēt > Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="5ff1d-125">Atlasiet **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="5ff1d-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-126">Select **OK**.</span></span>
5. <span data-ttu-id="5ff1d-127">Saglabājiet rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-127">Save the row definition.</span></span>
6. <span data-ttu-id="5ff1d-128">Jaunas kolonnas definīcijas izveide</span><span class="sxs-lookup"><span data-stu-id="5ff1d-128">Create a new column definition</span></span>
7. <span data-ttu-id="5ff1d-129">Izveidojiet jaunu pārskata definīciju.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-129">Create a new report definition.</span></span>
8. <span data-ttu-id="5ff1d-130">Atlasiet **Iestatījumi** un noņemiet atzīmi šai opcijai.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="5ff1d-131">Ģenerējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-131">Generate the report.</span></span> 
10. <span data-ttu-id="5ff1d-132">Eksportējiet pārskatu uz Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="5ff1d-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="5ff1d-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="5ff1d-134">Programmā Dynamics 365 Finance dodieties uz **Virsgrāmata > Pieprasījumi un pārskati > Apgrozījuma bilance**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="5ff1d-135">Iestatiet šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="5ff1d-135">Set the following parameters:</span></span>
   - <span data-ttu-id="5ff1d-136">**Sākuma datums** — ievadiet finanšu gada sākumu.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="5ff1d-137">**Beigu datums** — ievadiet datumu, kuram ģenerējat pārskatu.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="5ff1d-138">**Finanšu dimensija** — iestatiet šo lauku kā **Galvenā konta kopa**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="5ff1d-139">Atlasiet **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="5ff1d-140">Eksportējiet pārskatu uz Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="5ff1d-141">Tagad vajadzētu būt iespējai no Finanšu pārskatu Excel pārskata kopēt datus uz apgrozījuma bilances pārskatu, lai varat salīdzināt kolonnas **Beigu bilance**.</span><span class="sxs-lookup"><span data-stu-id="5ff1d-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]