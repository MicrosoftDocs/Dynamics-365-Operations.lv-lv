---
title: Atlīdzības organizācijas izstrāde
description: Šajā rakstā aprakstīts, kā izveidot fiksētas atlīdzības plānu un pieteikt nodarbinātos plānā, izmantojot piemērotības kārtulas.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115900"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="fd09c-103">Atlīdzības organizācijas izstrāde</span><span class="sxs-lookup"><span data-stu-id="fd09c-103">Develop a compensation structure</span></span>

<span data-ttu-id="fd09c-104">Šajā rakstā aprakstīts, kā izveidot fiksētas atlīdzības plānu un pieteikt nodarbinātos plānā, izmantojot piemērotības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="fd09c-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="fd09c-105">Šajā rakstā tiek izmantoti USMF demonstrācijas dati, un tie attiecas uz kompensāciju un atvieglojumu pārvaldniekiem.</span><span class="sxs-lookup"><span data-stu-id="fd09c-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="fd09c-106">Fiksētās atlīdzības plāna izveide</span><span class="sxs-lookup"><span data-stu-id="fd09c-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="fd09c-107">Atlasiet **Kompensāciju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="fd09c-108">Atlasiet **Fiksētu atlīdzību plāni**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="fd09c-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-109">Select **New**.</span></span>

4. <span data-ttu-id="fd09c-110">Laukā **Plāns** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="fd09c-111">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="fd09c-112">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="fd09c-113">Laukā **Tips** atlasiet, vai šis fiksētas atlīdzības plāns ir **Joslas**, **Līmeņa** vai **Pakāpes** plāns.</span><span class="sxs-lookup"><span data-stu-id="fd09c-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="fd09c-114">Izvēles rūtiņa **Ieteikšana atļauta** darbojas kā noklusējuma vērtība visām darbībām, kas šim plānam tiek pievienotas apstrādes notikumā.</span><span class="sxs-lookup"><span data-stu-id="fd09c-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="fd09c-115">Ja ieteikšana ir atļauta, atlīdzības apstrādāšanas laikā varat ignorēt aprēķināto vadlīniju summu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="fd09c-116">Lauks **Tolerance ārpus diapazona** jums ļauj norādīt, kā vēlaties apstrādāt atlīdzības summas, kuras attiecīgajam līmenim neietilpst norādītajā atlīdzību struktūras diapazonā.</span><span class="sxs-lookup"><span data-stu-id="fd09c-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="fd09c-117">Iestatot lauku **Tolerance ārpus diapazona** uz **Nav**, varat izmantot jebkuru atlīdzības summu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="fd09c-118">**Nestingrā tolerance** brīdina lietotājus, ja atlīdzības summa ir mazāka par minimālo atsauces punkta summu attiecīgajam līmenim vai lielāka par maksimālo atsauces punktu summu šim līmenim.</span><span class="sxs-lookup"><span data-stu-id="fd09c-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="fd09c-119">Lietotāji var ignorēt šo brīdinājumu un turpināt.</span><span class="sxs-lookup"><span data-stu-id="fd09c-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="fd09c-120">**Stingrā tolerance** ģenerē kļūdu, kad darbinieka atlīdzība tiek iestatīta ārpus minimālā un maksimālā atsauces punkta diapazona attiecīgajam līmenim, un darbinieka atlīdzība tiek automātiski pielāgota, lai ietilptu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="fd09c-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="fd09c-121">Lauks **Nolīgšanas kārtula** aprēķina darbinieka atlīdzību procesa notikuma laikā.</span><span class="sxs-lookup"><span data-stu-id="fd09c-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="fd09c-122">**Nolīgšanas kārtula** **Procenti** aprēķina palielinājumu, kas ir proporcionāli sadalīts laika ilgumam, kādu darbinieks ir bijis nodarbināts attiecīgajā ciklā.</span><span class="sxs-lookup"><span data-stu-id="fd09c-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="fd09c-123">Laukā **Valūta** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="fd09c-124">Laukā **Apmaksas likmes konvertēšana** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="fd09c-125">Izvērsiet sadaļu **Diapazona lietojuma matrica**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="fd09c-126">Pēc izvēles pievienojiet diapazona izmantošanas ierakstus, lai darbinieki līdz savam viduspunktam nokļūtu ātrāk un tiktu kavēta darbinieku diapazona maksimuma sasniegšana.</span><span class="sxs-lookup"><span data-stu-id="fd09c-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="fd09c-127">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-127">Select **Save**.</span></span> <span data-ttu-id="fd09c-128">Tas aktivizē pogu **Atlīdzības iestatīšana** un turpina definēt jūsu atlīdzības organizāciju plānam.</span><span class="sxs-lookup"><span data-stu-id="fd09c-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="fd09c-129">Atlasiet **Atlīdzības iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-129">Select **Set up compensation**.</span></span> <span data-ttu-id="fd09c-130">Varat izveidot atlīdzības organizāciju, izmantojot vienu no šīm trim metodēm:</span><span class="sxs-lookup"><span data-stu-id="fd09c-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="fd09c-131">Izveidojiet pilnīgi jaunu struktūru, atlasot atsauces punktu kopu un pievienojot līmeņus, lai izveidotu pats savu struktūru.</span><span class="sxs-lookup"><span data-stu-id="fd09c-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="fd09c-132">Kādu atlīdzību struktūru no jau esoša plāna kopējiet kā sākuma punktu un to pārveidot jaunajam plānam.</span><span class="sxs-lookup"><span data-stu-id="fd09c-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="fd09c-133">Atlasiet jau esošu atlīdzību režģi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-133">Select an existing compensation grid.</span></span> <span data-ttu-id="fd09c-134">Ja atlīdzību režģi jau izmanto cits plāns, šis plāns arī atspoguļo jebkādas izmaiņas, kas izdarītas režģim.</span><span class="sxs-lookup"><span data-stu-id="fd09c-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="fd09c-135">Atlasiet **Izveidot jaunu no jau esošas atlīdzības matricas**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="fd09c-136">Laukā **Kopēt no režģa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="fd09c-137">Ja vēlaties, varat mainīt nosaukumu jaunajam atlīdzību režģim, ko izveidojat, kopējot atlasīto režģi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="fd09c-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-138">Select **OK**.</span></span>

19. <span data-ttu-id="fd09c-139">Atlasiet **Masveida izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-139">Select **Mass change**.</span></span> <span data-ttu-id="fd09c-140">**Masveida izmaiņas** jums ļauj uzturēt atlīdzību matricas summas, lietojot procentuālus vai fiksētus summas pieaugumus vienam vai vairākiem līmeņiem vai atsauces punktiem.</span><span class="sxs-lookup"><span data-stu-id="fd09c-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="fd09c-141">Laukā **Korekcijas summa** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="fd09c-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="fd09c-142">Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.</span><span class="sxs-lookup"><span data-stu-id="fd09c-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="fd09c-143">Noklikšķiniet uz **Piemērot režģim**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="fd09c-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-144">Close the page.</span></span> <span data-ttu-id="fd09c-145">Kad izveidojat atlīdzību organizāciju, varat atlasīt, kuru no atsauces punktiem izmantot kā fiksētās atlīdzības plāna atskaites punktu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="fd09c-146">Atskaites punkts tiek izmantots, lai aprēķinātu darbinieka algas koeficientu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="fd09c-147">Laukā **Atskaites punkts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="fd09c-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="fd09c-149">Izveidot piemērotības kārtulu jaunajam fiksētas atlīdzības plānam</span><span class="sxs-lookup"><span data-stu-id="fd09c-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="fd09c-150">Varat piešķirt fiksētas atlīdzības plānu nodarbinātajam, līdz plānam ir definētas piemērotības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="fd09c-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="fd09c-151">Atlasiet **Piemērotības kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="fd09c-152">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="fd09c-152">Select **New**.</span></span>

3. <span data-ttu-id="fd09c-153">Laukā **Piemērotība** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="fd09c-154">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="fd09c-155">Laukā **Spēkā stāšanās datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="fd09c-156">Gan fiksēto, gan mainīgo atlīdzību plāni izmanto piemērotības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="fd09c-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="fd09c-157">Laukā **Veids** atlasiet plāna veidu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="fd09c-158">Laukā **Plāns** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd09c-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="fd09c-159">Atlasiet kritērijus, kādiem darbiniekam ir jāatbilst, lai darbinieks būtu piemērots šim atlīdzību plānam.</span><span class="sxs-lookup"><span data-stu-id="fd09c-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="fd09c-160">Kritēriji var ietvert:</span><span class="sxs-lookup"><span data-stu-id="fd09c-160">Criteria can include:</span></span>

    - <span data-ttu-id="fd09c-161">**Nodaļa**</span><span class="sxs-lookup"><span data-stu-id="fd09c-161">**Department**</span></span>
    - <span data-ttu-id="fd09c-162">**Arodbiedrība**</span><span class="sxs-lookup"><span data-stu-id="fd09c-162">**Labor union**</span></span>
    - <span data-ttu-id="fd09c-163">**Atrašanās vieta** (**Atlīdzības reģions**)</span><span class="sxs-lookup"><span data-stu-id="fd09c-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="fd09c-164">**Darbs**</span><span class="sxs-lookup"><span data-stu-id="fd09c-164">**Job**</span></span>
    - <span data-ttu-id="fd09c-165">**Funkcija**</span><span class="sxs-lookup"><span data-stu-id="fd09c-165">**Function**</span></span>
    - <span data-ttu-id="fd09c-166">**Darba tips**</span><span class="sxs-lookup"><span data-stu-id="fd09c-166">**Job type**</span></span>
    - <span data-ttu-id="fd09c-167">**Atlīdzības līmenis**</span><span class="sxs-lookup"><span data-stu-id="fd09c-167">**Compensation level**</span></span>
    
    <span data-ttu-id="fd09c-168">Lai darbinieks būtu piemērots atlīdzību plānam, šim darbiniekam ir jāatbilst visiem norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="fd09c-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="fd09c-169">Ja nenorādāt kritērijus, visi nodarbinātie ir piemēroti atlīdzību plānam.</span><span class="sxs-lookup"><span data-stu-id="fd09c-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="fd09c-170">Ja darbinieks neatbilst piemērotības kārtulās norādītajiem kritērijiem vai kādam atlīdzību plānam nav norādīta piemērotības kārtula, tad šis atlīdzību plāns netiks parādīts uzmeklēšanā, kad darbiniekam tiek veidots fiksētas atlīdzības ieraksts.</span><span class="sxs-lookup"><span data-stu-id="fd09c-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="fd09c-171">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-171">Close the page.</span></span>

8. <span data-ttu-id="fd09c-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fd09c-172">Close the page.</span></span>

