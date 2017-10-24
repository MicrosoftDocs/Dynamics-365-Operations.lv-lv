--- 
title: "Pakešuzdevuma izveide"
description: "Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="33322-103">Pakešuzdevuma izveide</span><span class="sxs-lookup"><span data-stu-id="33322-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33322-104">Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.</span><span class="sxs-lookup"><span data-stu-id="33322-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="33322-105">Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="33322-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="33322-106">Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru.</span><span class="sxs-lookup"><span data-stu-id="33322-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="33322-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="33322-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="33322-108">Izveidot pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="33322-108">Create the batch job</span></span>
1. <span data-ttu-id="33322-109">Doties uz Sistēmas administrēšana > Vaicājumi > Pakešuzdevumi.</span><span class="sxs-lookup"><span data-stu-id="33322-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="33322-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="33322-110">Click New.</span></span>
3. <span data-ttu-id="33322-111">Laukā Darba apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33322-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="33322-112">Laukā Plānotais sākuma datums/laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="33322-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="33322-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33322-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="33322-114">Izveidot atkārtošanos</span><span class="sxs-lookup"><span data-stu-id="33322-114">Create a recurrence</span></span>
1. <span data-ttu-id="33322-115">Darbību rūtī noklikšķiniet uz Pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="33322-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="33322-116">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="33322-116">Click Recurrence.</span></span>
    * <span data-ttu-id="33322-117">Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.</span><span class="sxs-lookup"><span data-stu-id="33322-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="33322-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33322-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="33322-119">Pievienot brīdinājumus</span><span class="sxs-lookup"><span data-stu-id="33322-119">Add alerts</span></span>
1. <span data-ttu-id="33322-120">Darbību rūtī noklikšķiniet uz Pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="33322-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="33322-121">Noklikšķiniet uz Brīdinājumi.</span><span class="sxs-lookup"><span data-stu-id="33322-121">Click Alerts.</span></span>
    * <span data-ttu-id="33322-122">Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts.</span><span class="sxs-lookup"><span data-stu-id="33322-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="33322-123">Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="33322-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="33322-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33322-124">Click OK.</span></span>


