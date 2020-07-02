---
title: Datu bāzu reģistrācijas konfigurēšana un pārvaldība
description: Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443587"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="6f983-103">Datu bāzu reģistrācijas konfigurēšana un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6f983-103">Configure and manage database logging</span></span>

<span data-ttu-id="6f983-104">Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f983-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="6f983-105">Šajā tēmā ir aprakstīts, kā:</span><span class="sxs-lookup"><span data-stu-id="6f983-105">This topic describes how to:</span></span>

- <span data-ttu-id="6f983-106">Pārvaldīt drošības un veiktspējas datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="6f983-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="6f983-107">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="6f983-107">Set up database logging</span></span>
- <span data-ttu-id="6f983-108">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="6f983-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="6f983-109">Datu bāzes reģistrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="6f983-109">Overview of database logging</span></span>

<span data-ttu-id="6f983-110">Datubāzes reģistrēšana izseko specifiskas izmaiņas Microsoft Dynamics 365 Human Resources tabulās un laukos.</span><span class="sxs-lookup"><span data-stu-id="6f983-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="6f983-111">Šīs izmaiņas ietver ievietošanu, atjaunināšanu vai dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f983-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="6f983-112">Datu bāzes reģistrācija saglabā ierakstu par izmaiņām tabulās vai laukos datu bāzes žurnāla tabulā.</span><span class="sxs-lookup"><span data-stu-id="6f983-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="6f983-113">Biznesa datu bāzes reģistrācijas izmantošana ietver:</span><span class="sxs-lookup"><span data-stu-id="6f983-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="6f983-114">Tiek izveidots audita ieraksts par izmaiņām noteiktās tabulās, kurās ir sensitīva informācija.</span><span class="sxs-lookup"><span data-stu-id="6f983-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="6f983-115">Atsevišķu darbību izsekošana.</span><span class="sxs-lookup"><span data-stu-id="6f983-115">Tracking single transactions.</span></span> <span data-ttu-id="6f983-116">Datu bāzes reģistrēšana nav paredzēta automatizēto darbību izsekošanai, kas darbojas pakešuzdevumos.</span><span class="sxs-lookup"><span data-stu-id="6f983-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="6f983-117">Drošība datu bāzes reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="6f983-117">Security for database logging</span></span>

<span data-ttu-id="6f983-118">Datubāzes žurnālos var būt sensitīvi dati.</span><span class="sxs-lookup"><span data-stu-id="6f983-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="6f983-119">Ierobežojiet piekļuvi, lai iekļautu tikai tās drošības lomas, kurām nepieciešama piekļuve žurnāla datiem.</span><span class="sxs-lookup"><span data-stu-id="6f983-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="6f983-120">Datu bāzes reģistrēšana un veiktspēja</span><span class="sxs-lookup"><span data-stu-id="6f983-120">Database logging and performance</span></span>

<span data-ttu-id="6f983-121">Lai gan no biznesa perspektīvas tā ir vērtīga, datu bāzes reģistrēšana resursu izmantošanā un vadībā var būt dārga.</span><span class="sxs-lookup"><span data-stu-id="6f983-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="6f983-122">Datu bāzes reģistrēšanas veiktspējas ietekme ietver:</span><span class="sxs-lookup"><span data-stu-id="6f983-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="6f983-123">Datu bāzes žurnāla tabula var ātri augt un radīt datu bāzes apjoma palielinājumu.</span><span class="sxs-lookup"><span data-stu-id="6f983-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="6f983-124">Pieaugums ir atkarīgs no reģistrēto datu apjoma, ko izlemjat paturēt.</span><span class="sxs-lookup"><span data-stu-id="6f983-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="6f983-125">Pēc noklusējuma datu bāzes žurnāla tabula uztur tikai 30 dienu žurnāla datus.</span><span class="sxs-lookup"><span data-stu-id="6f983-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="6f983-126">Datu bāzes reģistrācija var negatīvi ietekmēt ilgstošos automatizētos procesus, piemēram, ilgstošo datu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f983-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="6f983-127">Noteikumi</span><span class="sxs-lookup"><span data-stu-id="6f983-127">Best practices</span></span>

<span data-ttu-id="6f983-128">Lai uzlabotu veiktspēju, ierobežojiet reģistrēšanas ierakstus, atlasot reģistrēšanai īpašus laukus, bet nereģistrējiet visas tabulas.</span><span class="sxs-lookup"><span data-stu-id="6f983-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="6f983-129">Lai palīdzētu uzturēt vispārējo veiktspēju, datu bāzes reģistrēšana ir ierobežota līdz 20 tabulām.</span><span class="sxs-lookup"><span data-stu-id="6f983-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="6f983-130">Dažreiz laukiem var reģistrēt tikai atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="6f983-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="6f983-131">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="6f983-131">Set up database logging</span></span>

<span data-ttu-id="6f983-132">Varat izmantot **Reģistrēšanas datu bāzes izmaiņu** ceļvedi, lai iestatītu datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="6f983-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="6f983-133">Ceļvedis sniedz elastīgu veidu, kā iestatīt reģistrāciju tabulām vai laukiem.</span><span class="sxs-lookup"><span data-stu-id="6f983-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="6f983-134">Dodieties uz **Sistēmas administrēšanu > Saites > Datu bāzes > Datu bāzes žurnāla iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="6f983-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="6f983-135">Atlasiet **Jauns**, lai sāktu **Datu bāzes izmaiņu reģistrēšanas** ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="6f983-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="6f983-136">Pabeidziet ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="6f983-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="6f983-137">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="6f983-137">Clean up database logs</span></span>

<span data-ttu-id="6f983-138">Varat izdzēst visu vai daļu no datu bāzes žurnāliem, izmantojot šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="6f983-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="6f983-139">Atlasiet visus žurnālus noteiktai tabulai.</span><span class="sxs-lookup"><span data-stu-id="6f983-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="6f983-140">Atlasiet specifiskus datu bāzes žurnāla tipus.</span><span class="sxs-lookup"><span data-stu-id="6f983-140">Select specific types of database log.</span></span>
- <span data-ttu-id="6f983-141">Atlasiet datumu un laiku, kad tika izveidots žurnāls.</span><span class="sxs-lookup"><span data-stu-id="6f983-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="6f983-142">Lai iestatītu datu bāzes žurnāla tīrīšanu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="6f983-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="6f983-143">Dodieties uz **Sistēmas administrēšana > Saites > Datu bāzes > Datu bāzes žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="6f983-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="6f983-144">Atlasiet **Tīrīt žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="6f983-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="6f983-145">Izvēlieties metodi, kā atlasīt žurnālus dzēšanai, ievadot vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="6f983-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="6f983-146">Tabulas ID</span><span class="sxs-lookup"><span data-stu-id="6f983-146">Table ID</span></span>
   - <span data-ttu-id="6f983-147">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="6f983-147">Type of log</span></span>
   - <span data-ttu-id="6f983-148">Izveidotais datums un laiks</span><span class="sxs-lookup"><span data-stu-id="6f983-148">Created date and time</span></span>

3. <span data-ttu-id="6f983-149">Izmantojiet cilni **Datu bāzes žurnāla tīrīšana**, lai noteiktu, kad palaist žurnāla tīrīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="6f983-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="6f983-150">Pēc noklusējuma datu bāzes žurnāli ir pieejami 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="6f983-150">By default, database logs are available for 30 days.</span></span>
