---
title: Sagādes un avotu darbplūsmu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar sagādes un avotu darbplūsmām.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018541"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="87d53-103">Sagādes un avotu darbplūsmu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="87d53-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="87d53-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar sagādes un avotu darbplūsmām.</span><span class="sxs-lookup"><span data-stu-id="87d53-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="87d53-105">Kļūda, atkārtoti iesniedzot pirkšanas pasūtījumu darbplūsmai pēc izmaiņu veikšanas: “Izmaiņas pirkšanas pasūtījumā X ir atļautas tikai Melnraksta stāvoklī, kad ir aktivizēta izmaiņu pārvaldība”</span><span class="sxs-lookup"><span data-stu-id="87d53-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="87d53-106">Šī problēma rodas tikai tad, ja pirkšanas pasūtījums bija stāvoklī *Apstiprināts* , pirms jūs pieprasījāt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="87d53-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="87d53-107">Ja tiek pieprasītas izmaiņas, kamēr pirkšanas pasūtījums ir stāvoklī *Apstiprināts* , darbplūsma var tikt veiksmīgi apstrādāta.</span><span class="sxs-lookup"><span data-stu-id="87d53-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="87d53-108">Kļūdas apraksts</span><span class="sxs-lookup"><span data-stu-id="87d53-108">Error description</span></span>

<span data-ttu-id="87d53-109">Kad pirkšanas pasūtījums tiek atkārtoti iesniegts pēc izmaiņu veikšanas, darbplūsmā rodas šāda kļūda:</span><span class="sxs-lookup"><span data-stu-id="87d53-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="87d53-110">Apturēts (kļūda): X++ izņēmums: izmaiņas pirkšanas pasūtījumā PO0000569 ir atļautas tikai Melnraksta stāvoklī, ja tiek aktivizēta izmaiņu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="87d53-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="87d53-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="87d53-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="87d53-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="87d53-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="87d53-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="87d53-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="87d53-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="87d53-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="87d53-115">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="87d53-115">Issue resolution</span></span>

<span data-ttu-id="87d53-116">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="87d53-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="87d53-117">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts* , dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="87d53-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="87d53-118">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="87d53-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="87d53-119">Problēma tiks novērsta, izmantojot [šo Microsoft zināšanu bāzes (KB) rakstu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="87d53-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="87d53-120">Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.</span><span class="sxs-lookup"><span data-stu-id="87d53-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="87d53-121">Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.</span><span class="sxs-lookup"><span data-stu-id="87d53-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="87d53-122">Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts* , dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="87d53-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="87d53-123">Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="87d53-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="87d53-124">Ja pirkšanas pasūtījumā, kurā ir ieslēgta izmaiņu pārvaldība, tiek atcelts nosūtīšanas atlikums, tad pirkšanas pasūtījums tiek nosūtīts uz statusu Apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="87d53-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="87d53-125">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="87d53-125">Issue description</span></span>

<span data-ttu-id="87d53-126">Pirkšanas pasūtījums, kas pakļauts izmaiņu pārvaldībai, ja vienīgā pieprasītā izmaiņa ir nosūtīšanas atlikuma atcelšana vienai vai vairākām rindām, tiks tieši pārsūtīts uz statusu *Apstiprināts* , kad tas tiks apstiprināts un žurnāls netiks izveidots.</span><span class="sxs-lookup"><span data-stu-id="87d53-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="87d53-127">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="87d53-127">Issue resolution</span></span>

<span data-ttu-id="87d53-128">Nosūtīšanas atlikuma atcelšana neietekmē apstiprinājumu žurnāla saturu.</span><span class="sxs-lookup"><span data-stu-id="87d53-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="87d53-129">Šī funkcionalitāte jāizmanto, kad rinda ir daļēji saņemta un atlikusī kvalitāte ir jāatceļ procesa posmā pēc tam, kad ar kreditoru ir apstiprināts pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="87d53-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="87d53-130">Ja tas jāatspoguļo pirkšanas pasūtījuma apstiprinājumā, daudzums ir jākoriģē pirkšanas pasūtījuma rindā, lai apstiprinājums tiktu pieprasīts.</span><span class="sxs-lookup"><span data-stu-id="87d53-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="87d53-131">Pretējā gadījumā, ja rindā nekas nav saņemts, daudzumu var noņemt.</span><span class="sxs-lookup"><span data-stu-id="87d53-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="87d53-132">Šādā gadījumā būs nepieciešams atkārtots apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="87d53-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="87d53-133">Atceltie pirkšanas pasūtījumi tiek parādīti Pirkšanas pasūtījumu sagatavošanas darbvietas melnrakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="87d53-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="87d53-134">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="87d53-134">Issue description</span></span>

<span data-ttu-id="87d53-135">Atceļot pirkšanas pasūtījumus, ar statusu *Apstiprināts* , atceltie pirkšanas pasūtījumi joprojām parādās **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="87d53-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="87d53-136">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="87d53-136">Issue resolution</span></span>

<span data-ttu-id="87d53-137">Šī problēma rodas tikai tiem pirkšanas pasūtījumiem, kas ir pakļauti izmaiņu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="87d53-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="87d53-138">Tas notiek tāpēc, ka atcelšana tiek uzskatīta par izmaiņu, kas ir jāapstiprina.</span><span class="sxs-lookup"><span data-stu-id="87d53-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="87d53-139">Apstiprinājumu sistēma var veikt automātiski.</span><span class="sxs-lookup"><span data-stu-id="87d53-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="87d53-140">Atceltais pirkšanas pasūtījums ir jāiesniedz apstiprināšanas darbplūsmai, lai to varētu nosūtīt uz statusu *Apstiprināts*.</span><span class="sxs-lookup"><span data-stu-id="87d53-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="87d53-141">Pēc tam pirkšanas pasūtījums vairs netiks rādīts **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="87d53-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

