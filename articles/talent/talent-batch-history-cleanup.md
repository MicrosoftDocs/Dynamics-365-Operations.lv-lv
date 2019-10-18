---
title: Optimizēt veiktspēju ar automātiskās tīrīšanas uzdevumiem
description: Šajā tēmā tiek skaidrots, kā atrisināt dažas veiktspējas problēmas ar Microsoft Dynamics 365 Talent , iztīrot pakešuzdevuma vēsturi.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 1e9d237817024800ad9880ec58db3505ac1c493f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027088"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="052d8-103">Optimizēt veiktspēju ar automātiskās tīrīšanas uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="052d8-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="052d8-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="052d8-104">**Issue**</span></span>

<span data-ttu-id="052d8-105">Microsoft Dynamics 365 Talent var rasties veiktspējas problēmas, ja pakešuzdevumu vēsture kļūst pārāk liela.</span><span class="sxs-lookup"><span data-stu-id="052d8-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="052d8-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="052d8-106">**Cause**</span></span>

<span data-ttu-id="052d8-107">Bieži izpildīti pakešuzdevumi, var izraisīt nestabilu pakešuzdevuma vēstures izaugsmi.</span><span class="sxs-lookup"><span data-stu-id="052d8-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="052d8-108">Tas var izraisīt veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="052d8-108">This can cause performance issues.</span></span> 

<span data-ttu-id="052d8-109">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="052d8-109">**Resolution**</span></span>

<span data-ttu-id="052d8-110">Ieplānojiet automātisku jūsu pakešuzdevuma vēstures tīrīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="052d8-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="052d8-111">Mēs rekomendējam iestatīt uzdevumu tā, lai tas palaistos reizi nedēļā, taču, atkarībā no jūsu vides, var būt nepieciešams veikt tīrīšanu biežāk vai retāk.</span><span class="sxs-lookup"><span data-stu-id="052d8-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="052d8-112">Sekojošajā procedūrā ir ietverti mūsu ieteicamie iestatījumi, bet tos var mainīt atbilstoši jūsu vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="052d8-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="052d8-113">Pakalpojumā Talant atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="052d8-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="052d8-114">Joslā **Meklēšana** ievadiet **Pakešuzdevuma darba vēstures tīrīšana.**</span><span class="sxs-lookup"><span data-stu-id="052d8-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Meklējiet pakešuzdevumu vēstures tīrīšanu](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="052d8-116">**Vēstures ierobežojums (dienas)** joslā ievadiet **30**.</span><span class="sxs-lookup"><span data-stu-id="052d8-116">In **History limit (days)**, enter **30**.</span></span>

   ![Iestatiet vēstures glabāšanu uz 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="052d8-118">Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums.**</span><span class="sxs-lookup"><span data-stu-id="052d8-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Iestatiet periodiskumu](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="052d8-120">Sadaļā **Definēt periodiskumu**iestatiet **Sākuma datums** un **Sākuma laiks**, kas jāveic ārpus darba laika vai nedēļas nogalē, un pēc tam atlasiet **BEZ BEIGU DATUMA.**</span><span class="sxs-lookup"><span data-stu-id="052d8-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definējiet periodiskuma sākuma datumu un laiku](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="052d8-122">Sadaļā **PERIODISKUMA MODELIS** atlasiet **Dienas** un iestatiet **ATKĀRTOT PĒC NORĀDĪTĀ INTERVĀLA** uz **7**.</span><span class="sxs-lookup"><span data-stu-id="052d8-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Iestatiet tīrīšanu tā, lai tā atkārtotos katru nedēļu](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="052d8-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="052d8-124">Select **OK**.</span></span>

8. <span data-ttu-id="052d8-125">Mainiet jebkurus citus parametrus zem **Izpildīt fonā**, pēc nepieciešamības, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="052d8-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

