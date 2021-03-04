---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070221"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="30c10-103">Bieži uzdotie jautājumi par finanšu pārskatu veidošanu</span><span class="sxs-lookup"><span data-stu-id="30c10-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="30c10-104">Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji.</span><span class="sxs-lookup"><span data-stu-id="30c10-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="30c10-105">Kā var ierobežot piekļuvi pārskatam, izmantojot drošības koku?</span><span class="sxs-lookup"><span data-stu-id="30c10-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="30c10-106">Scenārijs: USMF demonstrācijas uzņēmumam ir bilances pārskats, un uzņēmums nevēlas, lai visi finanšu pārskatu lietotāji to varētu skatīt pakalpojumā D365.</span><span class="sxs-lookup"><span data-stu-id="30c10-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="30c10-107">Risinājums: jūs varat izmantot drošības koku, lai ierobežotu piekļuvi atsevišķam pārskatam, lai tikai noteikti lietotāji varētu piekļūt pārskatam.</span><span class="sxs-lookup"><span data-stu-id="30c10-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="30c10-108">Piesakieties finanšu pārskatu veidotājā</span><span class="sxs-lookup"><span data-stu-id="30c10-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="30c10-109">Izveidojiet jaunu koka definīciju (Fails | Jauns | Koka definīcija) a.</span><span class="sxs-lookup"><span data-stu-id="30c10-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="30c10-110">Veiciet dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="30c10-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="30c10-111">i.</span><span class="sxs-lookup"><span data-stu-id="30c10-111">i.</span></span>    <span data-ttu-id="30c10-112">Noklikšķiniet uz Lietotāji un grupas.</span><span class="sxs-lookup"><span data-stu-id="30c10-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="30c10-113">1. Atlasiet lietotājus vai grupu, kas vēlas piekļūt šim pārskatam.</span><span class="sxs-lookup"><span data-stu-id="30c10-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="30c10-114">[![lietotāja ekrāns](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="30c10-115">[![drošības ekrāns](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="30c10-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="30c10-116">b.</span><span class="sxs-lookup"><span data-stu-id="30c10-116">b.</span></span>    <span data-ttu-id="30c10-117">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="30c10-117">Click **Save**.</span></span>
  
<span data-ttu-id="30c10-118">[![poga Saglabāt](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="30c10-119">Pārskata definīcijā pievienojiet jaunu koka definīciju</span><span class="sxs-lookup"><span data-stu-id="30c10-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="30c10-120">[![koka definīcijas forma](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="30c10-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="30c10-121">A.</span><span class="sxs-lookup"><span data-stu-id="30c10-121">A.</span></span>  <span data-ttu-id="30c10-122">Koka definīcijas sadaļā noklikšķiniet uz Iestatījums un sadaļā “Pārskata vienību atlase” atzīmējiet “Iekļaut visas vienības”</span><span class="sxs-lookup"><span data-stu-id="30c10-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="30c10-123">[![pārskata vienības atlases forma](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="30c10-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="30c10-124">**Pirms:** [![pirms ekrānuzņēmuma](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="30c10-125">**Pēc:** [![pēc ekrānuzņēmuma](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="30c10-126">Piezīme. Iepriekš minētā ziņojuma iemesls ir: lietotājam nav piekļuves šim pārskatam pēc vienības drošības lietošanas</span><span class="sxs-lookup"><span data-stu-id="30c10-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="30c10-127">Kā var noteikt, kuri konti neatbilst manām bilancēm pakalpojumā D365?</span><span class="sxs-lookup"><span data-stu-id="30c10-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="30c10-128">Ja jums ir pārskats, kas neatbilst tam, ko varētu sagaidīt pakalpojumā D365, tālāk norādītas dažas darbības, ko varat veikt, lai identificētu šos kontus un novirzes.</span><span class="sxs-lookup"><span data-stu-id="30c10-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="30c10-129">Finanšu pārskatu veidotājā</span><span class="sxs-lookup"><span data-stu-id="30c10-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="30c10-130">Izveidojiet jaunu rindas definīciju a.</span><span class="sxs-lookup"><span data-stu-id="30c10-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="30c10-131">Noklikšķiniet uz Rediģēt | Ievietot rindas no dimensijām i.</span><span class="sxs-lookup"><span data-stu-id="30c10-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="30c10-132">Atlasiet MainAccount [![Atlasiet galveno ekrānu](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="30c10-133">ii.</span><span class="sxs-lookup"><span data-stu-id="30c10-133">ii.</span></span> <span data-ttu-id="30c10-134">Noklikšķiniet uz Labi b.</span><span class="sxs-lookup"><span data-stu-id="30c10-134">Click Ok b.</span></span>    <span data-ttu-id="30c10-135">Saglabājiet rindas definīciju</span><span class="sxs-lookup"><span data-stu-id="30c10-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="30c10-136">Izveidojiet jaunu kolonnas definīciju     [![Izveidojiet jaunu kolonnas definīciju](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="30c10-137">Izveidojiet jaunu pārskata definīciju a.</span><span class="sxs-lookup"><span data-stu-id="30c10-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="30c10-138">Noklikšķiniet uz iestatījumiem un noņemiet atzīmi no [![Iestatījumu formas](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="30c10-139">Ģenerējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="30c10-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="30c10-140">Eksportējiet pārskatu uz programmu Excel.</span><span class="sxs-lookup"><span data-stu-id="30c10-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="30c10-141">Pakalpojumā D365:</span><span class="sxs-lookup"><span data-stu-id="30c10-141">In D365:</span></span> 
1.  <span data-ttu-id="30c10-142">Noklikšķiniet uz Virsgrāmata | Pieprasījumi un pārskati | Apgrozījuma bilance a.</span><span class="sxs-lookup"><span data-stu-id="30c10-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="30c10-143">Parametri i.</span><span class="sxs-lookup"><span data-stu-id="30c10-143">Parameters i.</span></span>  <span data-ttu-id="30c10-144">Sākuma datums: finanšu gada sākums ii.</span><span class="sxs-lookup"><span data-stu-id="30c10-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="30c10-145">Beigu datums: datums, kam ģenerēts pārskats iii.</span><span class="sxs-lookup"><span data-stu-id="30c10-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="30c10-146">Finanšu dimensijas kopa “Galvenā konta kopa” [![Galvenā konta forma](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="30c10-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="30c10-147">b.</span><span class="sxs-lookup"><span data-stu-id="30c10-147">b.</span></span>    <span data-ttu-id="30c10-148">Noklikšķiniet uz Aprēķināt</span><span class="sxs-lookup"><span data-stu-id="30c10-148">Click Calculate</span></span>

2.  <span data-ttu-id="30c10-149">Eksportējiet pārskatu uz programmu Excel</span><span class="sxs-lookup"><span data-stu-id="30c10-149">Export the report to Excel</span></span>

<span data-ttu-id="30c10-150">Tagad vajadzētu būt iespējai no FR Excel pārskata kopēt datus uz D365 apgrozījuma bilances pārskatu un salīdzināt kolonnas “Beigu bilance”.</span><span class="sxs-lookup"><span data-stu-id="30c10-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>
