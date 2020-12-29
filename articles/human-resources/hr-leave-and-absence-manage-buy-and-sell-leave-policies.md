---
title: Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas
description: Varat ļaut darbiniekiem pirkt un pārdot atvaļinājumu Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419599"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="8e679-103">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="8e679-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="8e679-104">Varat nodrošināt, ka darbinieki var nopirkt un pārdot atvaļinājumu, izveidojot atvaļinājuma pirkšanas un pārdošanas politiku.</span><span class="sxs-lookup"><span data-stu-id="8e679-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="8e679-105">Šīs politikas var konfigurēt, lai izmantotu darbplūsmu apstiprinājumiem, iestatīt maksimālās summas un likmes un iestatīt likmes pirkšanai un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="8e679-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="8e679-106">Ļaujiet darbiniekiem pirkt un pārdot atvaļinājumu</span><span class="sxs-lookup"><span data-stu-id="8e679-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="8e679-107">Lapā **Atvaļinājumu un prombūtnes parametri** atlasiet **Jā** opcijai **Ļaut darbiniekiem pirkt atvaļinājumu** un **Ļaut darbiniekiem pārdot atvaļinājumu**.</span><span class="sxs-lookup"><span data-stu-id="8e679-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="8e679-108">Atvaļinājuma iegādes un pārdošanas politikas izveide</span><span class="sxs-lookup"><span data-stu-id="8e679-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="8e679-109">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="8e679-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="8e679-110">Atlasiet **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="8e679-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="8e679-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8e679-111">Select **New**.</span></span>

4. <span data-ttu-id="8e679-112">Ievadiet politikai **Nosaukums** un **Apraksts** sadaļā **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="8e679-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="8e679-113">Atlasiet **Politikas veids**.</span><span class="sxs-lookup"><span data-stu-id="8e679-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="8e679-114">Pieejamie politikas veidi ir **Summa** un **Stundas nedēļā**.</span><span class="sxs-lookup"><span data-stu-id="8e679-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="8e679-115">Atlasiet **Summa**, lai ievadītu **Fiksētā summa** maksimālajai summai, par kuru darbinieki var pirkt un pārdot.</span><span class="sxs-lookup"><span data-stu-id="8e679-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="8e679-116">Atlasot **Stundas nedēļā**, darba laiks, kas noteikts darbiniekam piešķirtajā darba laika kalendārā, tiek izmantots, lai noteiktu maksimālo politikas summu.</span><span class="sxs-lookup"><span data-stu-id="8e679-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="8e679-117">Atlasiet politikai **Sākuma datums** and **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="8e679-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="8e679-118">Pieprasījumi pirkt vai pārdot atvaļinājumu būs pieejami iesniegšanai tikai šajā laika posmā.</span><span class="sxs-lookup"><span data-stu-id="8e679-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="8e679-119">Atlasiet **Darbplūsmas ID** politikai.</span><span class="sxs-lookup"><span data-stu-id="8e679-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="8e679-120">Visi pirkšanas un pārdošanas pieprasījumi izmantos šo darbplūsmu pārskatīšanai un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="8e679-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="8e679-121">Sadaļā **Pirkšanas politika** atlasiet **Pilna laika ekvivalents** (FTE), lai proporcionāli pārvērtētu maksimālo summu, pamatojoties uz darbinieka amatā noteikto FTE.</span><span class="sxs-lookup"><span data-stu-id="8e679-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="8e679-122">Ja politikas veids ir **Summa**, ievadiet **Maksimālā fiksētā summa**.</span><span class="sxs-lookup"><span data-stu-id="8e679-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="8e679-123">Atlasiet **Pievienot**, lai pievienotu atvaļinājuma veidus darbiniekiem, kuri iegādājas atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="8e679-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="8e679-124">Politikai var pievienot vairākus atvaļinājuma veidus.</span><span class="sxs-lookup"><span data-stu-id="8e679-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="8e679-125">Lai noteiktu maksimālo summu, ko darbinieks var nopirkt, ievadiet **Nodarbinātības mēnešu skaits** atvaļinājuma veidu, kas ļauj definēt dažādu nodarbinātības mēnešu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8e679-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="8e679-126">Ievadiet **Maksimālā summa** atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="8e679-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="8e679-127">Ievadiet **Kurss**, pie kāda darbinieks nopirks atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="8e679-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="8e679-128">Pēc izvēles ievadiet **Pelnīšanas kods**, kas jāizmanto atvaļinājuma pirkšanai.</span><span class="sxs-lookup"><span data-stu-id="8e679-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="8e679-129">Pēc izvēles iestatiet, vai lietot FTE, lai noteiktu atvaļinājuma veida maksimālo summu.</span><span class="sxs-lookup"><span data-stu-id="8e679-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="8e679-130">Lai izveidotu pārdošanas politiku, izpildiet no 8. līdz 14. solim sadaļā **Pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="8e679-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="8e679-131">Atvaļinājuma pirkšanas un pārdošanas politikas pievienošana atvaļinājuma un prombūtnes plānam</span><span class="sxs-lookup"><span data-stu-id="8e679-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="8e679-132">Lapā **Atvaļinājums un prombūtne** atlasiet atvaļinājumu un prombūtnes plānu.</span><span class="sxs-lookup"><span data-stu-id="8e679-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="8e679-133">Sadaļā **Noteikumi** select **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="8e679-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e679-134">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="8e679-134">See also</span></span>

[<span data-ttu-id="8e679-135">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="8e679-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="8e679-136">Konfigurēt atvaļinājumu un kavējumu veidus</span><span class="sxs-lookup"><span data-stu-id="8e679-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="8e679-137">Uzkrāt atvaļinājumu un kavējumu plānus</span><span class="sxs-lookup"><span data-stu-id="8e679-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="8e679-138">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="8e679-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

