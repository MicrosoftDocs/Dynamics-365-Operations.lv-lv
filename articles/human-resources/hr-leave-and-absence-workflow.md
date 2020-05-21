---
title: Atvaļinājuma pieprasījuma darbplūsmas izveide
description: Izveidojiet atvaļinājumu un prombūtnes pieprasījumu darbplūsmu, lai konsekventi pārvaldītu atvaļinājumu pieprasījumus sistēmā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
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
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353692"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="22798-103">Atvaļinājuma pieprasījuma darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="22798-103">Create a leave request workflow</span></span>

<span data-ttu-id="22798-104">Varat sistēmā Dynamics 365 Human Resources izveidot darbplūsmu, lai konsekventi pārvaldītu savus atvaļinājuma un prombūtnes pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="22798-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="22798-105">**Atvaļinājumu un prombūtnes** darbplūsma ļauj:</span><span class="sxs-lookup"><span data-stu-id="22798-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="22798-106">Definēt uzdevumus</span><span class="sxs-lookup"><span data-stu-id="22798-106">Define tasks</span></span>
- <span data-ttu-id="22798-107">Noteikt, kam ir jāpabeidz uzdevumi</span><span class="sxs-lookup"><span data-stu-id="22798-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="22798-108">Norādīt, kurš var apstiprināt vai noraidīt pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="22798-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="22798-109">Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="22798-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="22798-110">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="22798-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="22798-111">Sadaļā **Iestatījumi** atlasiet **Personāla vadības darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="22798-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="22798-112">Atlasiet **Jauna**un pēc tam atlasiet **Atvaļinājuma un prombūtnes pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="22798-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="22798-113">Kad parādās ziņojuma lodziņš **Vai atvērt šo failu?**, atlasiet **Atvērt** un piesakieties ar sava uzņēmuma akreditācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="22798-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="22798-114">Izmantojiet darbplūsmas redaktoru, lai izveidotu jūsu atvaļinājuma pieprasījumu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="22798-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="22798-115">Lai iegūtu vairāk informācijas par darbu ar darbplūsmām, skatiet [Darbplūsmas apskatu izveide](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="22798-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="22798-116">Atvaļinājuma un prombūtnes pieprasījuma darbplūsmas datu elementi</span><span class="sxs-lookup"><span data-stu-id="22798-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="22798-117">Jūs varat izmantot tālāk norādītos datu elementus, lai izveidotu nosacījuma vai automātiskus apstiprinājumus darbplūsmās atvaļinājumu un kavējumu pieprasījumiem:</span><span class="sxs-lookup"><span data-stu-id="22798-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="22798-118">**Komentārs**</span><span class="sxs-lookup"><span data-stu-id="22798-118">**Comment**</span></span>
- <span data-ttu-id="22798-119">**Uzņēmums**</span><span class="sxs-lookup"><span data-stu-id="22798-119">**Company**</span></span>
- <span data-ttu-id="22798-120">**Izveidots**</span><span class="sxs-lookup"><span data-stu-id="22798-120">**Created by**</span></span>
- <span data-ttu-id="22798-121">**Izveidotais datums un laiks**</span><span class="sxs-lookup"><span data-stu-id="22798-121">**Created date and time**</span></span>
- <span data-ttu-id="22798-122">**Beigu datums**</span><span class="sxs-lookup"><span data-stu-id="22798-122">**End date**</span></span>
- <span data-ttu-id="22798-123">**Atvaļinājuma tips**</span><span class="sxs-lookup"><span data-stu-id="22798-123">**Leave type**</span></span>
- <span data-ttu-id="22798-124">**Labojis**</span><span class="sxs-lookup"><span data-stu-id="22798-124">**Modified by**</span></span>
- <span data-ttu-id="22798-125">**Modificēšanas datums un laiks**</span><span class="sxs-lookup"><span data-stu-id="22798-125">**Modified date and time**</span></span>
- <span data-ttu-id="22798-126">**Iemeslu kodi**</span><span class="sxs-lookup"><span data-stu-id="22798-126">**Reason code**</span></span>
- <span data-ttu-id="22798-127">**Pieprasījuma ID**</span><span class="sxs-lookup"><span data-stu-id="22798-127">**Request ID**</span></span>
- <span data-ttu-id="22798-128">**Sākuma datums**</span><span class="sxs-lookup"><span data-stu-id="22798-128">**Start date**</span></span>
- <span data-ttu-id="22798-129">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="22798-129">**Status**</span></span> 
- <span data-ttu-id="22798-130">**Iesniegšanas datums**</span><span class="sxs-lookup"><span data-stu-id="22798-130">**Submission date**</span></span>
- <span data-ttu-id="22798-131">**Iesniedza**</span><span class="sxs-lookup"><span data-stu-id="22798-131">**Submitted by**</span></span>
- <span data-ttu-id="22798-132">**Iesniedza personāla vadības nodaļa**</span><span class="sxs-lookup"><span data-stu-id="22798-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="22798-133">**Iesniedza vadītājs**</span><span class="sxs-lookup"><span data-stu-id="22798-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="22798-134">**Iesniegts vārdā**</span><span class="sxs-lookup"><span data-stu-id="22798-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="22798-135">**Darbinieks**</span><span class="sxs-lookup"><span data-stu-id="22798-135">**Worker**</span></span>
- <span data-ttu-id="22798-136">**Nodarbinātā veids**</span><span class="sxs-lookup"><span data-stu-id="22798-136">**Worker type**</span></span>

<span data-ttu-id="22798-137">Šie piemēri parāda, kā var izveidot dažādus darbplūsmas nosacījumu veidus, izmantojot šos datu elementus:</span><span class="sxs-lookup"><span data-stu-id="22798-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="22798-138">Izmantojiet **Pamatojuma kodu** nosacījuma pārskatā, lai maršrutētu slimības atvaļinājuma pieprasījumus ar iemesla kodu **Ķirurģija** uz PV apstiprināšanai, bet visus pārējos pamatojuma kodus pāradresētu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="22798-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="22798-139">Papildinformāciju par nosacījuma priekšrakstiem skatiet [Konfigurēt nosacījuma lēmumus darbplūsmā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="22798-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="22798-140">Izmantojiet **Iesniedza personāla vadības nodaļa** un **Iesniedza vadītājs**, lai automātiski apstiprinātu atvaļinājumu pieprasījumus, ko šīs lomas iesniedz darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="22798-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="22798-141">Plašāku informāciju par šīm automātiskajām darbībām skatiet [Konfigurēt apstiprināšanas procesus darbplūsmā](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="22798-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="22798-142">Izmantojiet **Atvaļinājuma veidu** nosacījuma pārskatā vai automātiskajās darbībās, lai kontrolētu, kā darbplūsma maršrutē pieprasījumus ar noteiktiem atvaļinājumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="22798-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="22798-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="22798-143">See also</span></span>

- [<span data-ttu-id="22798-144">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="22798-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
