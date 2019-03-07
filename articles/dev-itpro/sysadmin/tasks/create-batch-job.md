---
title: Pakešuzdevuma izveide
description: Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "313363"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="dca29-103">Pakešuzdevuma izveide</span><span class="sxs-lookup"><span data-stu-id="dca29-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dca29-104">Pakešuzdevums ir uzdevumu grupa, kas tiek iesniegta Programmas objektu servera (AOS) instancē automātiskai apstrādei.</span><span class="sxs-lookup"><span data-stu-id="dca29-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="dca29-105">Pakešuzdevumi tiek izpildīti, izmantojot darbu izveidojušā lietotāja drošības akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="dca29-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="dca29-106">Lai izveidotu pakešuzdevumu, izpildiet tālāk aprakstīto procedūru.</span><span class="sxs-lookup"><span data-stu-id="dca29-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="dca29-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="dca29-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="dca29-108">Izveidot pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="dca29-108">Create the batch job</span></span>
1. <span data-ttu-id="dca29-109">Doties uz Sistēmas administrēšana > Vaicājumi > Pakešuzdevumi.</span><span class="sxs-lookup"><span data-stu-id="dca29-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="dca29-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="dca29-110">Click New.</span></span>
3. <span data-ttu-id="dca29-111">Laukā Darba apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dca29-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="dca29-112">Laukā Plānotais sākuma datums/laiks ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="dca29-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="dca29-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dca29-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="dca29-114">Izveidot atkārtošanos</span><span class="sxs-lookup"><span data-stu-id="dca29-114">Create a recurrence</span></span>
1. <span data-ttu-id="dca29-115">Darbību rūtī noklikšķiniet uz Pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="dca29-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="dca29-116">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="dca29-116">Click Recurrence.</span></span>
    * <span data-ttu-id="dca29-117">Izmantojiet šīs opcijas, lai ievadītu periodiskuma diapazonu un modeli.</span><span class="sxs-lookup"><span data-stu-id="dca29-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="dca29-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dca29-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="dca29-119">Pievienot brīdinājumus</span><span class="sxs-lookup"><span data-stu-id="dca29-119">Add alerts</span></span>
1. <span data-ttu-id="dca29-120">Darbību rūtī noklikšķiniet uz Pakešuzdevums.</span><span class="sxs-lookup"><span data-stu-id="dca29-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="dca29-121">Noklikšķiniet uz Brīdinājumi.</span><span class="sxs-lookup"><span data-stu-id="dca29-121">Click Alerts.</span></span>
    * <span data-ttu-id="dca29-122">Norādiet, vai vēlaties sūtīt brīdinājuma ziņojumus, kad pakešuzdevums beidzas, kad tam ir kļūda vai kad tas tiek atcelts.</span><span class="sxs-lookup"><span data-stu-id="dca29-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="dca29-123">Pēc tam norādiet, vai vēlaties brīdinājumus rādīt kā uznirstošos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="dca29-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="dca29-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dca29-124">Click OK.</span></span>

