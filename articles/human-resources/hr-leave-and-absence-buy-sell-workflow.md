---
title: Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide
description: Izveidojiet atvaļinājumu pirkšanas un pārdošanas pieprasījumu darbplūsmu, lai konsekventi pārvaldītu pirkšanas un pārdošanas atvaļinājumu pieprasījumus sistēmā Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc31740218e3f171d89debace339dee0177d826
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053975"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="17ba1-103">Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="17ba1-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="17ba1-104">Varat sistēmā Dynamics 365 Human Resources izveidot darbplūsmu, lai konsekventi pārvaldītu atvaļinājuma pirkšanas un pārdošanas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="17ba1-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="17ba1-105">**Atvaļinājuma pirkšanas un pārdošanas** darbplūsma ļauj:</span><span class="sxs-lookup"><span data-stu-id="17ba1-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="17ba1-106">Definēt uzdevumus</span><span class="sxs-lookup"><span data-stu-id="17ba1-106">Define tasks</span></span>
- <span data-ttu-id="17ba1-107">Noteikt, kam ir jāpabeidz uzdevumi</span><span class="sxs-lookup"><span data-stu-id="17ba1-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="17ba1-108">Norādīt, kurš var apstiprināt vai noraidīt pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="17ba1-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="17ba1-109">Atvaļinājuma pirkšanas un pārdošanas pieprasījuma darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="17ba1-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="17ba1-110">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="17ba1-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="17ba1-111">Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="17ba1-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="17ba1-112">Atlasiet **Jauns** un pēc tam atlasiet **Atvaļinājuma pirkšanas un pārdošanas pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="17ba1-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="17ba1-113">Kad parādās ziņojuma lodziņš **Vai atvērt šo failu?**, atlasiet **Atvērt** un piesakieties ar sava uzņēmuma akreditācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="17ba1-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="17ba1-114">Izmantojiet darbplūsmas redaktoru, lai izveidotu jūsu atvaļinājuma pieprasījumu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="17ba1-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="17ba1-115">Lai iegūtu vairāk informācijas par darbu ar darbplūsmām, skatiet [Darbplūsmas apskatu izveide](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="17ba1-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="17ba1-116">Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas datu elementi</span><span class="sxs-lookup"><span data-stu-id="17ba1-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="17ba1-117">Jūs varat izmantot tālāk norādītos datu elementus, lai izveidotu nosacījuma vai automātiskus apstiprinājumus darbplūsmās atvaļinājumu pirkšanas un pārdošanas pieprasījumiem:</span><span class="sxs-lookup"><span data-stu-id="17ba1-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="17ba1-118">**Daudzums**</span><span class="sxs-lookup"><span data-stu-id="17ba1-118">**Amount**</span></span>
- <span data-ttu-id="17ba1-119">**Atvaļinājuma iegādes un pārdošanas politika**</span><span class="sxs-lookup"><span data-stu-id="17ba1-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="17ba1-120">**Uzņēmums**</span><span class="sxs-lookup"><span data-stu-id="17ba1-120">**Company**</span></span>
- <span data-ttu-id="17ba1-121">**Izveidots**</span><span class="sxs-lookup"><span data-stu-id="17ba1-121">**Created by**</span></span>
- <span data-ttu-id="17ba1-122">**Izveidošanas datums un laiks**</span><span class="sxs-lookup"><span data-stu-id="17ba1-122">**Created date and time**</span></span>
- <span data-ttu-id="17ba1-123">**Beigu datums**</span><span class="sxs-lookup"><span data-stu-id="17ba1-123">**End date**</span></span>
- <span data-ttu-id="17ba1-124">**Atvaļinājuma veids**</span><span class="sxs-lookup"><span data-stu-id="17ba1-124">**Leave type**</span></span>
- <span data-ttu-id="17ba1-125">**Modificēja:**</span><span class="sxs-lookup"><span data-stu-id="17ba1-125">**Modified by**</span></span>
- <span data-ttu-id="17ba1-126">**Modificēšanas datums un laiks**</span><span class="sxs-lookup"><span data-stu-id="17ba1-126">**Modified date and time**</span></span>
- <span data-ttu-id="17ba1-127">**Pieprasījuma ID**</span><span class="sxs-lookup"><span data-stu-id="17ba1-127">**Request ID**</span></span>
- <span data-ttu-id="17ba1-128">**Sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="17ba1-128">**Start date**</span></span>
- <span data-ttu-id="17ba1-129">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="17ba1-129">**Status**</span></span> 
- <span data-ttu-id="17ba1-130">**Iesniegšanas datums**</span><span class="sxs-lookup"><span data-stu-id="17ba1-130">**Submission date**</span></span>
- <span data-ttu-id="17ba1-131">**Iesniedza**</span><span class="sxs-lookup"><span data-stu-id="17ba1-131">**Submitted by**</span></span>
- <span data-ttu-id="17ba1-132">**Iesniedza personāla vadības nodaļa**</span><span class="sxs-lookup"><span data-stu-id="17ba1-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="17ba1-133">**Iesniedza vadītājs**</span><span class="sxs-lookup"><span data-stu-id="17ba1-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="17ba1-134">**Iesniegts vārdā**</span><span class="sxs-lookup"><span data-stu-id="17ba1-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="17ba1-135">**Darbinieks**</span><span class="sxs-lookup"><span data-stu-id="17ba1-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="17ba1-136">Darbplūsmas piemēri</span><span class="sxs-lookup"><span data-stu-id="17ba1-136">Workflow examples</span></span>

<span data-ttu-id="17ba1-137">Šie piemēri parāda, kā var izveidot dažādus darbplūsmas nosacījumu veidus, izmantojot šos datu elementus:</span><span class="sxs-lookup"><span data-stu-id="17ba1-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="17ba1-138">Izmantojiet **Iesniedza personāla vadības nodaļa** un **Iesniedza vadītājs**, lai automātiski apstiprinātu atvaļinājumu pirkšanas un pārdošanas pieprasījumus, ko šīs lomas iesniedz darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="17ba1-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="17ba1-139">Plašāku informāciju par šīm automātiskajām darbībām skatiet [Konfigurēt apstiprināšanas procesus darbplūsmā](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="17ba1-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="17ba1-140">Izmantojiet **Atvaļinājuma veidu** nosacījuma pārskatā vai automātiskajās darbībās, lai kontrolētu, kā darbplūsma maršrutē pieprasījumus ar noteiktiem atvaļinājumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="17ba1-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="17ba1-141">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="17ba1-141">See also</span></span>

[<span data-ttu-id="17ba1-142">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="17ba1-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="17ba1-143">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="17ba1-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]