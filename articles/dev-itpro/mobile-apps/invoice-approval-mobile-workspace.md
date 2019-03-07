---
title: Mobilā darbvieta Rēķinu apstiprinājumi
description: Šajā tēmā ir sniegta informācija par mobilo darbvietu Rēķinu apstiprinājumi. Šajā darbvietā tiek sniegts saraksts ar rēķiniem, kas jums ir piešķirti, izmantojot kreditora rēķina virsraksta darbplūsmas procesu.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff726670e0fd7566a74e6def73555a7c53b86f97
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "327002"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="e66ed-104">Mobilā darbvieta Rēķinu apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="e66ed-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e66ed-105">Šajā tēmā ir sniegta informācija par mobilo darbvietu **Rēķinu apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="e66ed-106">Šajā darbvietā tiek sniegts saraksts ar rēķiniem, kas jums ir piešķirti, izmantojot kreditora rēķina virsraksta darbplūsmas procesu.</span><span class="sxs-lookup"><span data-stu-id="e66ed-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="e66ed-107">Šī mobilā darbvieta ir paredzēta lietošanai kopā ar programmu Microsoft Dynamics 365 for Unified Operations Mobile</span><span class="sxs-lookup"><span data-stu-id="e66ed-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="e66ed-108">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e66ed-108">Overview</span></span>

<span data-ttu-id="e66ed-109">Mobilā darbvieta **Rēķinu apstiprinājumi** darbiniekiem un vadītājiem no moduļa Kreditori ļauj apskatītu rēķinus, kas viņiem ir piešķirti kā daļa no kreditora rēķina virsraksta darbplūsmas procesa.</span><span class="sxs-lookup"><span data-stu-id="e66ed-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="e66ed-110">Varat skatīt rēķina informāciju un pat detalizētu informāciju par rindām un sadali, lai varētu labāk pieņemtu informētus apstiprinājuma lēmumus.</span><span class="sxs-lookup"><span data-stu-id="e66ed-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="e66ed-111">No šīs darbvietas varat veikt pasākumus, lai rēķinu pārvietotu darbplūsmas procesā.</span><span class="sxs-lookup"><span data-stu-id="e66ed-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e66ed-112">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="e66ed-112">Prerequisites</span></span>

<span data-ttu-id="e66ed-113">Lai varētu izmantot šo mobilo darbvietu, vispirms ir jāizpilda tālāk norādītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="e66ed-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e66ed-114">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="e66ed-114">Prerequisite</span></span></th>
<th><span data-ttu-id="e66ed-115">Loma</span><span class="sxs-lookup"><span data-stu-id="e66ed-115">Role</span></span></th>
<th><span data-ttu-id="e66ed-116">apraksts</span><span class="sxs-lookup"><span data-stu-id="e66ed-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e66ed-117">Jūsu organizācijā ir jābūt izvietotai programmai Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e66ed-117">Microsoft Dynamics 365 for Finance and Operations must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="e66ed-118">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="e66ed-118">System administrator</span></span></td>
<td><span data-ttu-id="e66ed-119">Skatiet rakstu <a href="../deployment/deploy-demo-environment.md">Izvietot demonstrācijas vidi</a>.</span><span class="sxs-lookup"><span data-stu-id="e66ed-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e66ed-120">Mobilajai darbvietai <strong>Rēķinu apstiprinājumi</strong> ir jābūt publicētai.</span><span class="sxs-lookup"><span data-stu-id="e66ed-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="e66ed-121">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="e66ed-121">System administrator</span></span></td>
<td><span data-ttu-id="e66ed-122">Skatiet tēmu <a href="publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>.</span><span class="sxs-lookup"><span data-stu-id="e66ed-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="e66ed-123">Mobilās programmas lejupielāde un instalēšana</span><span class="sxs-lookup"><span data-stu-id="e66ed-123">Download and install the mobile app</span></span>

<span data-ttu-id="e66ed-124">Lejupielādējiet un instalējiet mobilo programmu Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="e66ed-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="e66ed-125">Android tālruņiem</span><span class="sxs-lookup"><span data-stu-id="e66ed-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="e66ed-126">Tālruņiem iPhone</span><span class="sxs-lookup"><span data-stu-id="e66ed-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="e66ed-127">Pierakstīšanās mobilajā programmā</span><span class="sxs-lookup"><span data-stu-id="e66ed-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="e66ed-128">Palaidiet programmu savā mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="e66ed-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="e66ed-129">Ievadiet savu Microsoft Dynamics 365 vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="e66ed-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="e66ed-130">Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="e66ed-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="e66ed-131">Ievadiet savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="e66ed-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="e66ed-132">Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="e66ed-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="e66ed-133">Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.</span><span class="sxs-lookup"><span data-stu-id="e66ed-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="e66ed-134">[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="e66ed-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="e66ed-135">Apstiprināt rēķinus, izmantojot mobilo darbvietu Rēķinu apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="e66ed-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="e66ed-136">Mobilajā ierīcē atlasiet darbvietu **Rēķinu apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="e66ed-137">Atlasiet rēķinu, kas jums ir piešķirts ar kreditora rēķina virsraksta darbplūsmas procesu.</span><span class="sxs-lookup"><span data-stu-id="e66ed-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="e66ed-138">Lapā **Rēķina informācija** pārskatiet rēķina galvenes informāciju, piemēram, informāciju par kreditoru un datumu.</span><span class="sxs-lookup"><span data-stu-id="e66ed-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="e66ed-139">Rēķinā atlasiet rindu, lai par to skatītu detalizētu informāciju skatā **Rēķina rindas informācija**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="e66ed-140">Skatā **Rēķina rindas informācija** atlasiet vienumu **Sadales**, lai rādītu rindas sadales.</span><span class="sxs-lookup"><span data-stu-id="e66ed-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="e66ed-141">Šeit varat skatīt rēķina rindas uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="e66ed-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="e66ed-142">Rādītā informācija ietver finanšu dimensijas un galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="e66ed-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="e66ed-143">Lapā **Rēķina informācija** atlasiet vienumu **Sadales**, lai rādītu visas sadales.</span><span class="sxs-lookup"><span data-stu-id="e66ed-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="e66ed-144">Šeit varat skatīt visa rēķina uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="e66ed-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="e66ed-145">Rādītā informācija ietver finanšu dimensijas un galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="e66ed-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="e66ed-146">Atlasiet vienumu **Pielikumi**, lai skatītu visas šim rēķinam pievienotās piezīmes vai failus.</span><span class="sxs-lookup"><span data-stu-id="e66ed-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="e66ed-147">Lapā **Rēķina informācija** atlasiet atbilstošo darbplūsmas darbību, lai pabeigtu savu pārskatīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="e66ed-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="e66ed-148">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-148">Select **Done**.</span></span>
