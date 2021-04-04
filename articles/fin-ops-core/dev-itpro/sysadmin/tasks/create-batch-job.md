---
title: Pakešuzdevuma izveide
description: Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 753a78dd140ca82c8c42ff8fdd3772e66b5a1cb0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571081"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="965f8-103">Pakešuzdevuma izveide</span><span class="sxs-lookup"><span data-stu-id="965f8-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="965f8-104">Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.</span><span class="sxs-lookup"><span data-stu-id="965f8-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="965f8-105">Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="965f8-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="965f8-106">Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru.</span><span class="sxs-lookup"><span data-stu-id="965f8-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="965f8-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="965f8-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="965f8-108">Izveidot pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="965f8-108">Create the batch job</span></span>
1. <span data-ttu-id="965f8-109">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="965f8-110">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="965f8-110">Click **New**.</span></span>
3. <span data-ttu-id="965f8-111">Laukā **Pienākumu apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="965f8-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="965f8-112">Laukā **Plānotais sākuma datums/laiks** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="965f8-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="965f8-113">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="965f8-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="965f8-114">Izveidot atkārtošanos</span><span class="sxs-lookup"><span data-stu-id="965f8-114">Create a recurrence</span></span>
1. <span data-ttu-id="965f8-115">Darbību rūtī noklikšķiniet uz **Pakešuzdevums**.</span><span class="sxs-lookup"><span data-stu-id="965f8-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="965f8-116">Noklikšķiniet uz **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="965f8-116">Click **Recurrence**.</span></span> <span data-ttu-id="965f8-117">Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.</span><span class="sxs-lookup"><span data-stu-id="965f8-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="965f8-118">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="965f8-119">Pievienot brīdinājumus</span><span class="sxs-lookup"><span data-stu-id="965f8-119">Add alerts</span></span>
1. <span data-ttu-id="965f8-120">Darbību rūtī noklikšķiniet uz **Pakešuzdevums**.</span><span class="sxs-lookup"><span data-stu-id="965f8-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="965f8-121">Noklikšķiniet uz **Brīdinājumi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-121">Click **Alerts**.</span></span> <span data-ttu-id="965f8-122">Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts.</span><span class="sxs-lookup"><span data-stu-id="965f8-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="965f8-123">Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="965f8-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="965f8-124">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="965f8-125">Pakešuzdevuma statusa pielāgošana</span><span class="sxs-lookup"><span data-stu-id="965f8-125">Adjust batch job status</span></span>
1. <span data-ttu-id="965f8-126">Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="965f8-127">Atlasiet atbilstošo pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="965f8-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="965f8-128">Darbību rūtī noklikšķiniet uz **Pakešuzdevums > Funkcijas > Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="965f8-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="965f8-129">Atlasiet atbilstošo statusu.</span><span class="sxs-lookup"><span data-stu-id="965f8-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="965f8-130">**Aizturēt**: atlasiet pakešuzdevuma statusu **aizturēt**, lai tas tiktu aizturēts no pakešuzdevumu plānotāja.</span><span class="sxs-lookup"><span data-stu-id="965f8-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="965f8-131">Līdzvērtīgs funkcijai *apturēt*.</span><span class="sxs-lookup"><span data-stu-id="965f8-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="965f8-132">**Gaida**: atlasiet pakešuzdevuma statusu **gaida**, lai tas gaidītu rindā, līdz to izvēlēsies pakešuzdevumu plānotājs.</span><span class="sxs-lookup"><span data-stu-id="965f8-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="965f8-133">Līdzvērtīgs funkcijai *sākt*.</span><span class="sxs-lookup"><span data-stu-id="965f8-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="965f8-134">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="965f8-134">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]