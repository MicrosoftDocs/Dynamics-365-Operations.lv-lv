---
title: Atvaļinājumu un prombūtnes veidu konfigurēšana
description: Iestatiet atvaļinājumu tipus, ko darbinieki var izņemt pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198054"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="a06a5-103">Atvaļinājumu un prombūtnes veidu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a06a5-103">Configure leave and absence types</span></span>

<span data-ttu-id="a06a5-104">Atvaļinājumu veidi pakalpojumā Dynamics 365 Human Resources definē, kādu veidu prombūtnes laiku darbinieki var pieprasīt.</span><span class="sxs-lookup"><span data-stu-id="a06a5-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="a06a5-105">Varat pielāgot atvaļinājumu veidus atbilstoši organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="a06a5-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="a06a5-106">Atvaļinājumu veidu piemēri ietver:</span><span class="sxs-lookup"><span data-stu-id="a06a5-106">Examples of leave types include:</span></span>

- <span data-ttu-id="a06a5-107">Apmaksāts brīvais laiks (PTO)</span><span class="sxs-lookup"><span data-stu-id="a06a5-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="a06a5-108">Neapmaksāts atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-108">Unpaid leave</span></span>
- <span data-ttu-id="a06a5-109">Apmaksāts atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-109">Paid vacation</span></span>
- <span data-ttu-id="a06a5-110">Slimības atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-110">Sick leave</span></span>
- <span data-ttu-id="a06a5-111">Medicīnisks atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-111">Medical leave</span></span>
- <span data-ttu-id="a06a5-112">Ģimenes atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-112">Family leave</span></span>
- <span data-ttu-id="a06a5-113">Īslaicīga invaliditāte</span><span class="sxs-lookup"><span data-stu-id="a06a5-113">Short-term disability</span></span>
- <span data-ttu-id="a06a5-114">Apbedīšanas atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="a06a5-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="a06a5-115">Pievienot atvaļinājuma tipu</span><span class="sxs-lookup"><span data-stu-id="a06a5-115">Add a leave type</span></span>

1. <span data-ttu-id="a06a5-116">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="a06a5-117">Sadaļā **Iestatīšana**atlasiet **Atvaļinājumu un kavējumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="a06a5-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-118">Select **New**.</span></span>

4. <span data-ttu-id="a06a5-119">Ievadiet atvaļinājuma veida nosaukumu laukā **Veids**, atlasiet darbplūsmu no **Darbplūsmas ID** un ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="a06a5-120">Laukā **Vispārīgi** atlasiet **Neviens**, **Plānots** vai **Neplānots** nolaižamajā sarakstā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="a06a5-121">Atlasiet pelnīšanas kodu no nolaižamā saraksta **Ienākumu veida kods**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="a06a5-122">Laukā **Nepieciešams pamatojuma kods**izvēlieties, vai vēlaties pieprasīt pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="a06a5-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="a06a5-123">Ja vēlaties pieprasīt pamatojuma kodus, iespējams, tie ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="a06a5-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="a06a5-124">Sadaļā **Pamatojumu kodi** atlasiet **Pievienot**, atlasiet pamatojuma kodu un pēc tam blakus atzīmējiet izvēles rūtiņu**Iespējoti**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="a06a5-125">Sadaļā **Ierobežot piekļuvi atlasītajām lomām**izvēlieties, vai vēlaties ierobežot piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="a06a5-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="a06a5-126">Pēc tam atlasiet drošības lomas sadaļā **Drošības lomas šim atvaļinājuma veidam**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="a06a5-127">Drošības lomas ir definētas darbplūsmā, ko atlasījāt laukā **Darbplūsmas ID** iepriekš šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="a06a5-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="a06a5-128">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="a06a5-129">Konfigurēt atvaļinājumu veidu kārtulas</span><span class="sxs-lookup"><span data-stu-id="a06a5-129">Configure leave type rules</span></span>

1. <span data-ttu-id="a06a5-130">Iestatiet noapaļošanas opcijas atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="a06a5-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="a06a5-131">Opcijas ietver **Neviens**, **Uz augšu**, **Uz leju** un **Tuvākais**.</span><span class="sxs-lookup"><span data-stu-id="a06a5-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="a06a5-132">Atvaļinājuma veidam var arī iestatīt noapaļošanas precizitāti.</span><span class="sxs-lookup"><span data-stu-id="a06a5-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="a06a5-133">Iestatiet atvaļinājuma veida **Brīvdienu labojumu**</span><span class="sxs-lookup"><span data-stu-id="a06a5-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="a06a5-134">Atlasot šo opciju, Human Resources izmanto to brīvdienu skaitu, kuras iekrīt darba dienā, lai noteiktu, kā uzkrāt brīvo laiku atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="a06a5-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="a06a5-135">Piemēram, ja Ziemassvētki ir pirmdienā, Human Resources, apstrādājot uzkrājumus, atņem vienu dienu no atvaļinājuma veida.</span><span class="sxs-lookup"><span data-stu-id="a06a5-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="a06a5-136">Brīvdienas varat iestatīt darba laika kalendārā.</span><span class="sxs-lookup"><span data-stu-id="a06a5-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="a06a5-137">Papildinformāciju skatiet šeit šeit: [Darba laika kalendāra izveide](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="a06a5-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="a06a5-138">Priekšskatījuma līdzekļu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a06a5-138">Configure preview features</span></span>

<span data-ttu-id="a06a5-139">Ja esat iespējojis priekšskatījuma līdzekļus atvaļinājumiem un prombūtnei, arī tiem ir jākonfigurē iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a06a5-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="a06a5-140">Izvēlieties atvaļinājuma veidu pārnešanas bilancēm, uz kurām jāpārsūta.</span><span class="sxs-lookup"><span data-stu-id="a06a5-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="a06a5-141">Varat arī izveidot jaunu atvaļinājuma veidu pārnešanai.</span><span class="sxs-lookup"><span data-stu-id="a06a5-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="a06a5-142">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a06a5-142">See also</span></span>

- [<span data-ttu-id="a06a5-143">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="a06a5-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="a06a5-144">Izveidot atvaļinājumu un kavējuma plānu</span><span class="sxs-lookup"><span data-stu-id="a06a5-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="a06a5-145">Darba laika kalendāra izveide</span><span class="sxs-lookup"><span data-stu-id="a06a5-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
