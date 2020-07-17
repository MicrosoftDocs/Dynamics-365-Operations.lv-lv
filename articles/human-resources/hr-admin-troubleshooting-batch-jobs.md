---
title: Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba
description: Šajā tēmā ir paskaidrots, kā atrisināt veiktspējas problēmas ar Microsoft Dynamics 365 Human Resources , plānojot ilglaicīgus pakešuzdevumus pēc darba.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500509"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="2b78e-103">Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba</span><span class="sxs-lookup"><span data-stu-id="2b78e-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="2b78e-104">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="2b78e-104">Issue</span></span>

<span data-ttu-id="2b78e-105">Microsoft Dynamics 365 Human Resources var rasties veiktspējas problēmas, ja ilglaicīgi pakešuzdevumi darbojas ierastajā darba laikā.</span><span class="sxs-lookup"><span data-stu-id="2b78e-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="2b78e-106">Novēršana</span><span class="sxs-lookup"><span data-stu-id="2b78e-106">Resolution</span></span>

<span data-ttu-id="2b78e-107">Šādus pakešuzdevumus ieplānojiet ārpus darba laika.</span><span class="sxs-lookup"><span data-stu-id="2b78e-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="2b78e-108">Ieteicams pārskatīt arī bieži izpildāmo pakešuzdevumu biežumu.</span><span class="sxs-lookup"><span data-stu-id="2b78e-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="2b78e-109">Ja iespējams, samaziniet pakešuzdevuma atkārtošanos.</span><span class="sxs-lookup"><span data-stu-id="2b78e-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="2b78e-110">Daudzos gadījumos noklusējuma frekvence ir pietiekama.</span><span class="sxs-lookup"><span data-stu-id="2b78e-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="2b78e-111">Šādus pakešuzdevumus ieteicams izpildīt naktī vai pēc darba.</span><span class="sxs-lookup"><span data-stu-id="2b78e-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="2b78e-112">Noteikti pārbaudiet periodisko pakešuzdevumu laika joslu.</span><span class="sxs-lookup"><span data-stu-id="2b78e-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="2b78e-113">Daži pakešuzdevumi izmanto Klusā okeāna standarta laiku (PST).</span><span class="sxs-lookup"><span data-stu-id="2b78e-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="2b78e-114">Pakešuzdevums</span><span class="sxs-lookup"><span data-stu-id="2b78e-114">Batch job</span></span> | <span data-ttu-id="2b78e-115">Noklusējuma atkārtojums</span><span class="sxs-lookup"><span data-stu-id="2b78e-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="2b78e-116">Pakešuzdevuma vēstures tīrīšana</span><span class="sxs-lookup"><span data-stu-id="2b78e-116">Batch job history cleanup</span></span> | <span data-ttu-id="2b78e-117">1 reizi mēnesī</span><span class="sxs-lookup"><span data-stu-id="2b78e-117">1 time per month</span></span> |
| <span data-ttu-id="2b78e-118">Eksporta sagatavošanas posmu tīrīšana</span><span class="sxs-lookup"><span data-stu-id="2b78e-118">Export staging cleanup</span></span> | <span data-ttu-id="2b78e-119">1 reizi dienā</span><span class="sxs-lookup"><span data-stu-id="2b78e-119">1 time per day</span></span> |
| <span data-ttu-id="2b78e-120">Common Data Service integrācijas neizpildīto pieprasījumu sinhronizēšana</span><span class="sxs-lookup"><span data-stu-id="2b78e-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="2b78e-121">1 reizi dienā</span><span class="sxs-lookup"><span data-stu-id="2b78e-121">1 time per day</span></span> |
| <span data-ttu-id="2b78e-122">Datu bāzes saspiešanas sistēmas darbs, kas jāveic regulāri, ārpus darba laikā</span><span class="sxs-lookup"><span data-stu-id="2b78e-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="2b78e-123">1 reizi dienā</span><span class="sxs-lookup"><span data-stu-id="2b78e-123">1 time per day</span></span> |
| <span data-ttu-id="2b78e-124">Datu bāzes indeksa pārbūves sistēmas darbs, kas jāveic regulāri, ārpus darba laikā</span><span class="sxs-lookup"><span data-stu-id="2b78e-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="2b78e-125">1 reizi dienā</span><span class="sxs-lookup"><span data-stu-id="2b78e-125">1 time per day</span></span> |

1. <span data-ttu-id="2b78e-126">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="2b78e-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="2b78e-127">Joslā **Meklēšana** meklējiet vienu no iepriekš minētajiem pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="2b78e-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="2b78e-128">Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="2b78e-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Iestatiet periodiskumu](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="2b78e-130">Zem **Definēt periodiskumu** iestatiet **Sākuma datums** un **Sākuma laiks**, kas ir ārpus darba laika, vai nedēļas nogalē.</span><span class="sxs-lookup"><span data-stu-id="2b78e-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="2b78e-131">Atlasiet **Bez beigu datuma**.</span><span class="sxs-lookup"><span data-stu-id="2b78e-131">Select **No end date**.</span></span> 

   ![Definējiet periodiskuma sākuma datumu un laiku](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="2b78e-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2b78e-133">Select **OK**.</span></span>

6. <span data-ttu-id="2b78e-134">Ja nepieciešams, mainiet jebkurus citus parametrus zem **Izpildīt fonā** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2b78e-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b78e-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2b78e-135">Additional resources</span></span>

[<span data-ttu-id="2b78e-136">Veiktspējas optimizēšana ar automātiskās tīrīšanas uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="2b78e-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
