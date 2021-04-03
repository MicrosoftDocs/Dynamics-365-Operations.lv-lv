---
title: Mobilā darbvieta Rēķinu apstiprinājumi
description: Šajā tēmā ir sniegta informācija par mobilo darbvietu Rēķinu apstiprinājumi.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570079"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="9d19e-103">Mobilā darbvieta Rēķinu apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="9d19e-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d19e-104">Šajā tēmā ir sniegta informācija par mobilo darbvietu **Rēķinu apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="9d19e-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="9d19e-105">Šajā darbvietā tiek sniegts saraksts ar rēķiniem, kas jums ir piešķirti, izmantojot kreditora rēķina virsraksta darbplūsmas procesu.</span><span class="sxs-lookup"><span data-stu-id="9d19e-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="9d19e-106">Šī mobilā darbvieta ir paredzēta lietošanai kopā ar mobilo programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9d19e-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="9d19e-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9d19e-107">Overview</span></span>

<span data-ttu-id="9d19e-108">Mobilā darbvieta **Rēķinu apstiprinājumi** darbiniekiem un vadītājiem no moduļa Kreditori ļauj apskatītu rēķinus, kas viņiem ir piešķirti kā daļa no kreditora rēķina virsraksta darbplūsmas procesa.</span><span class="sxs-lookup"><span data-stu-id="9d19e-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="9d19e-109">Varat skatīt rēķina informāciju un pat detalizētu informāciju par rindām un sadali, lai varētu labāk pieņemtu informētus apstiprinājuma lēmumus.</span><span class="sxs-lookup"><span data-stu-id="9d19e-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="9d19e-110">No šīs darbvietas varat veikt pasākumus, lai rēķinu pārvietotu darbplūsmas procesā.</span><span class="sxs-lookup"><span data-stu-id="9d19e-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9d19e-111">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="9d19e-111">Prerequisites</span></span>

<span data-ttu-id="9d19e-112">Lai varētu izmantot šo mobilo darbvietu, vispirms ir jāizpilda tālāk norādītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="9d19e-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9d19e-113">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="9d19e-113">Prerequisite</span></span></th>
<th><span data-ttu-id="9d19e-114">Loma</span><span class="sxs-lookup"><span data-stu-id="9d19e-114">Role</span></span></th>
<th><span data-ttu-id="9d19e-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9d19e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d19e-116">Jūsu organizācijā ir jābūt izvietotai programmai Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9d19e-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="9d19e-117">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="9d19e-117">System administrator</span></span></td>
<td><span data-ttu-id="9d19e-118">Skatiet rakstu <a href="../deployment/deploy-demo-environment.md">Izvietot demonstrācijas vidi</a>.</span><span class="sxs-lookup"><span data-stu-id="9d19e-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d19e-119">Mobilajai darbvietai <strong>Rēķinu apstiprinājumi</strong> ir jābūt publicētai.</span><span class="sxs-lookup"><span data-stu-id="9d19e-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="9d19e-120">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="9d19e-120">System administrator</span></span></td>
<td><span data-ttu-id="9d19e-121">Skatiet tēmu <a href="publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>.</span><span class="sxs-lookup"><span data-stu-id="9d19e-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="9d19e-122">Mobilās programmas lejupielāde un instalēšana</span><span class="sxs-lookup"><span data-stu-id="9d19e-122">Download and install the mobile app</span></span>

<span data-ttu-id="9d19e-123">Mobilās programmas Finance and Operations lejupielāde un instalēšana.</span><span class="sxs-lookup"><span data-stu-id="9d19e-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="9d19e-124">. Android tālruņiem</span><span class="sxs-lookup"><span data-stu-id="9d19e-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="9d19e-125">Tālruņiem iPhone</span><span class="sxs-lookup"><span data-stu-id="9d19e-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="9d19e-126">Pierakstīšanās mobilajā programmā</span><span class="sxs-lookup"><span data-stu-id="9d19e-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="9d19e-127">Palaidiet programmu savā mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="9d19e-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="9d19e-128">Ievadiet savu Microsoft Dynamics 365 vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="9d19e-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="9d19e-129">Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="9d19e-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="9d19e-130">Ievadiet savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="9d19e-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="9d19e-131">Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="9d19e-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="9d19e-132">Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.</span><span class="sxs-lookup"><span data-stu-id="9d19e-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="9d19e-133">[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="9d19e-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="9d19e-134">Apstiprināt rēķinus, izmantojot mobilo darbvietu Rēķinu apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="9d19e-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="9d19e-135">Mobilajā ierīcē atlasiet darbvietu **Rēķinu apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="9d19e-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="9d19e-136">Atlasiet rēķinu, kas jums ir piešķirts ar kreditora rēķina virsraksta darbplūsmas procesu.</span><span class="sxs-lookup"><span data-stu-id="9d19e-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="9d19e-137">Lapā **Rēķina informācija** pārskatiet rēķina galvenes informāciju, piemēram, informāciju par kreditoru un datumu.</span><span class="sxs-lookup"><span data-stu-id="9d19e-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="9d19e-138">Rēķinā atlasiet rindu, lai par to skatītu detalizētu informāciju skatā **Rēķina rindas informācija**.</span><span class="sxs-lookup"><span data-stu-id="9d19e-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="9d19e-139">Skatā **Rēķina rindas informācija** atlasiet vienumu **Sadales**, lai rādītu rindas sadales.</span><span class="sxs-lookup"><span data-stu-id="9d19e-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="9d19e-140">Šeit varat skatīt rēķina rindas uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="9d19e-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="9d19e-141">Rādītā informācija ietver finanšu dimensijas un galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="9d19e-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="9d19e-142">Lapā **Rēķina informācija** atlasiet vienumu **Sadales**, lai rādītu visas sadales.</span><span class="sxs-lookup"><span data-stu-id="9d19e-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="9d19e-143">Šeit varat skatīt visa rēķina uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="9d19e-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="9d19e-144">Rādītā informācija ietver finanšu dimensijas un galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="9d19e-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="9d19e-145">Atlasiet vienumu **Pielikumi**, lai skatītu visas šim rēķinam pievienotās piezīmes vai failus.</span><span class="sxs-lookup"><span data-stu-id="9d19e-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="9d19e-146">Lapā **Rēķina informācija** atlasiet atbilstošo darbplūsmas darbību, lai pabeigtu savu pārskatīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="9d19e-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="9d19e-147">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="9d19e-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]