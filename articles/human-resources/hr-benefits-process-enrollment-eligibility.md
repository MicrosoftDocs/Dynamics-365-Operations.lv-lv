---
title: Reģistrācijas piemērotības apstrāde
description: Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009753"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="76620-103">Reģistrācijas piemērotības apstrāde</span><span class="sxs-lookup"><span data-stu-id="76620-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="76620-104">Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.</span><span class="sxs-lookup"><span data-stu-id="76620-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="76620-105">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Reģistrācijas piemērotības apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="76620-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="76620-106">Dialoglodziņā **Izpildīt atvieglojumu reģistrācijas piemērotības apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="76620-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="76620-107">Lauks</span><span class="sxs-lookup"><span data-stu-id="76620-107">Field</span></span> | <span data-ttu-id="76620-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="76620-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="76620-109">Reģistrācijas periods</span><span class="sxs-lookup"><span data-stu-id="76620-109">Enrollment period</span></span> | <span data-ttu-id="76620-110">Reģistrācijas periods, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="76620-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="76620-111">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="76620-111">Legal entity</span></span> | <span data-ttu-id="76620-112">Juridiskā persona, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="76620-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="76620-113">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="76620-113">Worker</span></span> | <span data-ttu-id="76620-114">Nodarbinātais, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="76620-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="76620-115">Ja šo lauku atstāsiet tukšu, reģistrācijas piemērotība tiks apstrādāta visiem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="76620-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="76620-116">Atvieglojumu plāns</span><span class="sxs-lookup"><span data-stu-id="76620-116">Benefit plan</span></span> | <span data-ttu-id="76620-117">Atvieglojumu plāns, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="76620-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="76620-118">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="76620-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="76620-119">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="76620-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="76620-120">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="76620-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="76620-121">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="76620-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="76620-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="76620-122">Select **OK**.</span></span> <span data-ttu-id="76620-123">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="76620-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="76620-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="76620-124">Select **OK**.</span></span>
