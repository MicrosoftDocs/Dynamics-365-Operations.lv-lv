---
title: Atvaļinājumu un prombūtnes parametru konfigurēšana
description: Definējiet cilvēkresursu parametrus atvaļinājumam un prombūtnei pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056856"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="ba6a2-103">Atvaļinājumu un prombūtnes parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="ba6a2-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ba6a2-104">Pirms atvaļinājumu un prombūtnes plānu iestatīšanas pakalpojumā Dynamics 365 Human Resources, ir ieteicams pārbaudīt visu saistīto personāla vadības parametru iestatījumus, tostarp:</span><span class="sxs-lookup"><span data-stu-id="ba6a2-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="ba6a2-105">Atvaļinājumu pieprasījumu numuru sēriju</span><span class="sxs-lookup"><span data-stu-id="ba6a2-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="ba6a2-106">Likuma par ģimenes un medicīniskajiem atvaļinājumiem (FMLA) iestatījumus</span><span class="sxs-lookup"><span data-stu-id="ba6a2-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="ba6a2-107">Darbinieku patstāvīgi izmantojamo pakalpojumu iestatījumus atvaļinājumu un prombūtnes pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="ba6a2-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="ba6a2-108">Atvaļinājumu un prombūtnes parametri</span><span class="sxs-lookup"><span data-stu-id="ba6a2-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="ba6a2-109">Skatīt un mainīt personāla vadības parametrus</span><span class="sxs-lookup"><span data-stu-id="ba6a2-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="ba6a2-110">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ba6a2-111">Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="ba6a2-112">Cilnē **Numuru sērijas** pārbaudiet **Numuru secības kodu** **Atvaļinājuma pieprasījuma ID** un pēc nepieciešamības veiciet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="ba6a2-113">Šis iestatījums nosaka secību, kas tiek izmantota, lai automātiski piešķirtu ID atvaļinājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="ba6a2-114">Cilnē **FMLA** pārbaudiet FMLA iestatījumus un pēc nepieciešamības mainiet.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="ba6a2-115">Cilnē **Darbinieku patstāvīgi izmantojamie pakalpojumi** norādiet, vai vadītāji var ievadīt atvaļinājumu un kavējumu pieprasījumus savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="ba6a2-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ba6a2-117">Pašlaik priekšskatījumā tiek apskatīts atvaļinājums un prombūtne uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="ba6a2-118">Jums vajadzēs iespējot to savā **Smilškastes** vidē, lai parādītu atvaļinājumu un prombūtnes opciju.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="ba6a2-119">Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="ba6a2-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="ba6a2-120">Skatīt un mainīt Personāla vadības kopīgotos parametrus</span><span class="sxs-lookup"><span data-stu-id="ba6a2-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="ba6a2-121">Lapā **Personāla vadība** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ba6a2-122">Sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgotie parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="ba6a2-123">Cilnē **Iepriekšēja piekļuve** atlasiet **Jā** opcijai **Iespējot starpuzņēmuma atvaļinājumu skatu**, lai ļautu atvaļinājumu apskatīt visā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="ba6a2-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="ba6a2-125">Skatīt un mainīt atvaļinājumu un prombūtnes parametrus</span><span class="sxs-lookup"><span data-stu-id="ba6a2-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="ba6a2-126">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ba6a2-127">Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un prombūtnes parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="ba6a2-128">Cilnē **Vispārīgi** iestatiet šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="ba6a2-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="ba6a2-129">Iestatiet **Vienību atvaļinājumam un prombūtni** vai nu stundām, vai dienām.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="ba6a2-130">Ja dienas, jūs varat atlasīt **Iespējot pusi dienas definīciju**, lai ļautu darbiniekiem izvēlēties vai nu pirmo, vai otro pusi no dienas , kad tiek veikti prombūtnes pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="ba6a2-131">Atlasiet **Darba mēnešu spēkā stāšanās datums**, lai iestatītu, kad uzkrāšanas likmes stājas spēkā atvaļinājumu plāniem, izmantojot darba mēnešus.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="ba6a2-132">Atlasiet **Bilances aprēķinu**, lai parādītu bilances, kas tiek rādītas no šodienas vai no uzkrāšanas perioda.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="ba6a2-133">Ja atlasāt **Bilanci no šodienas**, bilance parāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no šodienas.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="ba6a2-134">Ja atlasāt **Bilance no uzkrāšanas perioda**, bilance rāda visu uzkrājumu, korekciju un pieprasījumu kopsummu no uzkrājumu perioda, kas definēts, izmantojot atvaļinājumu plāna biežumu.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="ba6a2-135">Iestatiet sākuma laiku pārnestā termiņa beigu pakešuzdevumam.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="ba6a2-136">Atlasiet **Jā** opcijām **Atļaut darbiniekiem pirkt atvaļinājumu** un **Atļaut darbiniekiem pārdot atvaļinājumu**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="ba6a2-137">Ja šīm opcijām atlasāt **Jā**, varat izveidot pirkšanas un pārdošanas atvaļinājuma politikas un dot iespēju darbiniekiem iesniegt pirkšanas un pārdošanas atvaļinājumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="ba6a2-138">Konfigurējiet kalendāra parametrus</span><span class="sxs-lookup"><span data-stu-id="ba6a2-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="ba6a2-139">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ba6a2-140">Sadaļā **Iestatīšana** atlasiet **Atvaļinājumu un prombūtnes parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="ba6a2-141">Cilnē **Kalendārs** pēc nepieciešamības mainiet kalendāra iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="ba6a2-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ba6a2-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba6a2-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="ba6a2-143">See also</span></span>

- [<span data-ttu-id="ba6a2-144">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="ba6a2-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]