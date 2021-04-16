---
title: Atvaļinājumu un prombūtnes veidu konfigurēšana
description: Iestatiet atvaļinājumu tipus, ko darbinieki var izņemt pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf868ad44e52b0ed7d0ca6e1f133efa030f3c4a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794569"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="1b29d-103">Atvaļinājumu un prombūtnes veidu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="1b29d-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1b29d-104">Atvaļinājumu veidi pakalpojumā Dynamics 365 Human Resources definē, kādu veidu prombūtnes laiku darbinieki var pieprasīt.</span><span class="sxs-lookup"><span data-stu-id="1b29d-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="1b29d-105">Varat pielāgot atvaļinājumu veidus atbilstoši organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="1b29d-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="1b29d-106">Atvaļinājumu veidu piemēri ietver:</span><span class="sxs-lookup"><span data-stu-id="1b29d-106">Examples of leave types include:</span></span>

- <span data-ttu-id="1b29d-107">Apmaksāts brīvais laiks (PTO)</span><span class="sxs-lookup"><span data-stu-id="1b29d-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="1b29d-108">Neapmaksāts atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-108">Unpaid leave</span></span>
- <span data-ttu-id="1b29d-109">Apmaksāts atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-109">Paid vacation</span></span>
- <span data-ttu-id="1b29d-110">Slimības atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-110">Sick leave</span></span>
- <span data-ttu-id="1b29d-111">Medicīnisks atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-111">Medical leave</span></span>
- <span data-ttu-id="1b29d-112">Ģimenes atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-112">Family leave</span></span>
- <span data-ttu-id="1b29d-113">Īslaicīga invaliditāte</span><span class="sxs-lookup"><span data-stu-id="1b29d-113">Short-term disability</span></span>
- <span data-ttu-id="1b29d-114">Apbedīšanas atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="1b29d-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="1b29d-115">Pievienot atvaļinājuma tipu</span><span class="sxs-lookup"><span data-stu-id="1b29d-115">Add a leave type</span></span>

1. <span data-ttu-id="1b29d-116">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="1b29d-117">Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un kavējumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="1b29d-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-118">Select **New**.</span></span>

4. <span data-ttu-id="1b29d-119">Ievadiet atvaļinājuma veida nosaukumu laukā **Veids**, atlasiet darbplūsmu no **Darbplūsmas ID** un ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="1b29d-120">Laukā **Vispārīgi** atlasiet **Neviens**, **Plānots** vai **Neplānots** nolaižamajā sarakstā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="1b29d-121">Atlasiet pelnīšanas kodu no nolaižamā saraksta **Ienākumu veida kods**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="1b29d-122">Laukā **Nepieciešams pamatojuma kods** izvēlieties, vai vēlaties pieprasīt pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="1b29d-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="1b29d-123">Ja vēlaties pieprasīt pamatojuma kodus, iespējams, tie ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="1b29d-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="1b29d-124">Sadaļā **Pamatojumu kodi** atlasiet **Pievienot**, atlasiet pamatojuma kodu un pēc tam blakus atzīmējiet izvēles rūtiņu **Iespējoti**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="1b29d-125">Sadaļā **Ierobežot piekļuvi atlasītajām lomām** izvēlieties, vai vēlaties ierobežot piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="1b29d-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="1b29d-126">Pēc tam atlasiet drošības lomas sadaļā **Drošības lomas šim atvaļinājuma veidam**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="1b29d-127">Drošības lomas ir definētas darbplūsmā, ko atlasījāt laukā **Darbplūsmas ID** iepriekš šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="1b29d-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="1b29d-128">Sadaļā **Kalendāra krāsa** izvēlieties krāsu, ko parādīt atvaļinājuma un kavējumu kalendāros šim atvaļinājuma tipam.</span><span class="sxs-lookup"><span data-stu-id="1b29d-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="1b29d-129">Sadaļā **Atlikšanas attiecības** izvēlieties, vai vēlaties, lai šo atvaļinājuma veidu aiztur cits cits atvaļinājuma veids vai arī to aptur cits atvaļinājuma veids.</span><span class="sxs-lookup"><span data-stu-id="1b29d-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="1b29d-130">Ja prombūtnes atvaļinājuma pieprasījums ir iesniegts atliktam atvaļinājuma veidam, tad aizturētā atvaļinājuma veidam automātiski tiks izveidota atvaļinājuma atlikšana.</span><span class="sxs-lookup"><span data-stu-id="1b29d-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="1b29d-131">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="1b29d-132">Konfigurēt atvaļinājumu veidu kārtulas</span><span class="sxs-lookup"><span data-stu-id="1b29d-132">Configure leave type rules</span></span>

1. <span data-ttu-id="1b29d-133">Iestatiet noapaļošanas opcijas atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="1b29d-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="1b29d-134">Opcijas ietver **Neviens**, **Uz augšu**, **Uz leju** un **Tuvākais**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="1b29d-135">Atvaļinājuma veidam var arī iestatīt noapaļošanas precizitāti.</span><span class="sxs-lookup"><span data-stu-id="1b29d-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="1b29d-136">Iestatiet atvaļinājuma veida **Brīvdienu labojumu**</span><span class="sxs-lookup"><span data-stu-id="1b29d-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="1b29d-137">Atlasot šo opciju, Human Resources izmanto to brīvdienu skaitu, kuras iekrīt darba dienā, lai noteiktu, kā uzkrāt brīvo laiku atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="1b29d-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="1b29d-138">Piemēram, ja Ziemassvētki ir pirmdienā, Human Resources, apstrādājot uzkrājumus, atņem vienu dienu no atvaļinājuma veida.</span><span class="sxs-lookup"><span data-stu-id="1b29d-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="1b29d-139">Brīvdienas varat iestatīt darba laika kalendārā.</span><span class="sxs-lookup"><span data-stu-id="1b29d-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="1b29d-140">Papildinformāciju skatiet šeit šeit: [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="1b29d-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="1b29d-141">Iestatiet atvaļinājuma veidam **Pārnesta atvaļinājuma veids**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="1b29d-142">Atlasot šo opciju, visas pārnešanas bilances tiks pārsūtītas uz norādīto atvaļinājumu veidu.</span><span class="sxs-lookup"><span data-stu-id="1b29d-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="1b29d-143">Pārnestā atvaļinājuma veids ir jāiekļauj arī atvaļinājumu un prombūtnes plānā.</span><span class="sxs-lookup"><span data-stu-id="1b29d-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="1b29d-144">Definējiet atvaļinājuma veidam **Beigu nosacījumu noteikumus**.</span><span class="sxs-lookup"><span data-stu-id="1b29d-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="1b29d-145">Konfigurējot šo opciju, varat izvēlēties dienu vai mēnešu vienību un iestatīt beigu termiņu.</span><span class="sxs-lookup"><span data-stu-id="1b29d-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="1b29d-146">Varat arī iestatīt termiņa beigu nosacījuma spēkā stāšanās datumu.</span><span class="sxs-lookup"><span data-stu-id="1b29d-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="1b29d-147">Spēkā stāšanās datumu izmanto, lai noteiktu, kad sākt palaist pakešuzdevumu, kas apstrādā atvaļinājuma beigu datumu, vai datumu, kad noteikums stājas spēkā.</span><span class="sxs-lookup"><span data-stu-id="1b29d-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="1b29d-148">Termiņa beigas vienmēr notiks atvaļinājuma plāna sākuma datumā pēc tam, kad pakešuzdevums būs iestatīts apstrādājams.</span><span class="sxs-lookup"><span data-stu-id="1b29d-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="1b29d-149">Piemēram, plāna sākuma datums var būt 2020. gada 1. janvāris, bet noteikums netika izveidots līdz 2020. gada 1. jūnijam.</span><span class="sxs-lookup"><span data-stu-id="1b29d-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="1b29d-150">Iestatot spēkā stāšanās datumu 2020. gada 1. jūnijā, noteikums tiks apstrādāts ar nākamā gada robežu, tādējādi 2021. gada 1. janvārī.</span><span class="sxs-lookup"><span data-stu-id="1b29d-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="1b29d-151">Visas atvaļinājuma bilances, kas pastāv beigu laikā, tiks atskaitītas no atvaļinājuma veida, un tās tiks atspoguļotas atvaļinājumu bilancē.</span><span class="sxs-lookup"><span data-stu-id="1b29d-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="1b29d-152">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="1b29d-152">See also</span></span>

- [<span data-ttu-id="1b29d-153">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="1b29d-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="1b29d-154">Izveidot atvaļinājumu un kavējuma plānu</span><span class="sxs-lookup"><span data-stu-id="1b29d-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="1b29d-155">Darba laika kalendāra izveide</span><span class="sxs-lookup"><span data-stu-id="1b29d-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="1b29d-156">Pārtraukt atvaļinājumu</span><span class="sxs-lookup"><span data-stu-id="1b29d-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
