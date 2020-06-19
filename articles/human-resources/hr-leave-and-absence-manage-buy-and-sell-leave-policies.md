---
title: Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas
description: Varat ļaut darbiniekiem pirkt un pārdot atvaļinājumu Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429017"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="1d78a-103">Pārvaldīt atvaļinājuma pirkšanas un pārdošanas politikas</span><span class="sxs-lookup"><span data-stu-id="1d78a-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1d78a-104">Varat nodrošināt, ka darbinieki var nopirkt atvaļinājumu, izveidojot atvaļinājuma pirkšanas politiku.</span><span class="sxs-lookup"><span data-stu-id="1d78a-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="1d78a-105">Ļaujiet darbiniekiem pirkt un pārdot atvaļinājumu</span><span class="sxs-lookup"><span data-stu-id="1d78a-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="1d78a-106">Lapā **Atvaļinājumu un prombūtnes parametri** atlasiet **Jā** opcijai **Ļaut darbiniekiem pirkt atvaļinājumu**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="1d78a-107">Atvaļinājuma pirkšanas izveide</span><span class="sxs-lookup"><span data-stu-id="1d78a-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="1d78a-108">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="1d78a-109">Atlasiet **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="1d78a-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-110">Select **New**.</span></span>

4. <span data-ttu-id="1d78a-111">Ievadiet politikai **Nosaukums** un **Apraksts** sadaļā **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="1d78a-112">Atlasiet **Politikas veids**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="1d78a-113">Pieejamie politikas veidi ir **Summa** un **Stundas nedēļā**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="1d78a-114">Atlasiet **Summa**, lai ievadītu **Fiksētā summa** maksimālajai summai, par kuru darbinieki var pirkt un pārdot.</span><span class="sxs-lookup"><span data-stu-id="1d78a-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="1d78a-115">Atlasot **Stundas nedēļā**, darba laiks, kas noteikts darbiniekam piešķirtajā darba laika kalendārā, tiek izmantots, lai noteiktu maksimālo politikas summu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="1d78a-116">Atlasiet politikai **Sākuma datums** and **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="1d78a-117">Pieprasījumi pirkt vai pārdot atvaļinājumu būs pieejami iesniegšanai tikai šajā laika posmā.</span><span class="sxs-lookup"><span data-stu-id="1d78a-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="1d78a-118">Sadaļā **Pirkšanas politika** atlasiet **Pilna laika ekvivalents** (FTE), lai proporcionāli pārvērtētu maksimālo summu, pamatojoties uz darbinieka amatā noteikto FTE.</span><span class="sxs-lookup"><span data-stu-id="1d78a-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="1d78a-119">Ja politikas veids ir **Summa**, ievadiet **Maksimālā fiksētā summa**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="1d78a-120">Atlasiet **Pievienot**, lai pievienotu atvaļinājuma veidus darbiniekiem, kuri iegādājas atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="1d78a-121">Politikai var pievienot vairākus atvaļinājuma veidus.</span><span class="sxs-lookup"><span data-stu-id="1d78a-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="1d78a-122">Lai noteiktu maksimālo summu, ko darbinieks var nopirkt, ievadiet **Nodarbinātības mēnešu skaits** atvaļinājuma veidu, kas ļauj definēt dažādu nodarbinātības mēnešu skaitu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="1d78a-123">Ievadiet **Maksimālā summa** atvaļinājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="1d78a-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="1d78a-124">Ievadiet **Kurss**, pie kāda darbinieks nopirks atvaļinājumu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="1d78a-125">Pēc izvēles ievadiet **Pelnīšanas kods**, kas jāizmanto atvaļinājuma pirkšanai.</span><span class="sxs-lookup"><span data-stu-id="1d78a-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="1d78a-126">Pēc izvēles iestatiet, vai lietot FTE, lai noteiktu atvaļinājuma veida maksimālo summu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="1d78a-127">Atvaļinājuma pirkšanas un pārdošanas politikas pievienošana atvaļinājuma un prombūtnes plānam</span><span class="sxs-lookup"><span data-stu-id="1d78a-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="1d78a-128">Lapā **Atvaļinājums un prombūtne** atlasiet atvaļinājumu un prombūtnes plānu.</span><span class="sxs-lookup"><span data-stu-id="1d78a-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="1d78a-129">Sadaļā **Noteikumi** select **Atvaļinājuma pirkšanas un pārdošanas politika**.</span><span class="sxs-lookup"><span data-stu-id="1d78a-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d78a-130">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="1d78a-130">See also</span></span>

[<span data-ttu-id="1d78a-131">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="1d78a-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="1d78a-132">Konfigurēt atvaļinājumu un kavējumu veidus</span><span class="sxs-lookup"><span data-stu-id="1d78a-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="1d78a-133">Uzkrāt atvaļinājumu un kavējumu plānus</span><span class="sxs-lookup"><span data-stu-id="1d78a-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="1d78a-134">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d78a-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

