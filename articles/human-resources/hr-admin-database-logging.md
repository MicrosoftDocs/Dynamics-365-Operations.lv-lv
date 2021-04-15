---
title: Datu bāzu reģistrācijas konfigurēšana un pārvaldība
description: Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801339"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="e749f-103">Datu bāzu reģistrācijas konfigurēšana un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e749f-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e749f-104">Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="e749f-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="e749f-105">Šajā tēmā ir aprakstīts, kā:</span><span class="sxs-lookup"><span data-stu-id="e749f-105">This topic describes how to:</span></span>

- <span data-ttu-id="e749f-106">Pārvaldīt drošības un veiktspējas datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="e749f-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="e749f-107">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="e749f-107">Set up database logging</span></span>
- <span data-ttu-id="e749f-108">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="e749f-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="e749f-109">Datu bāzes reģistrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="e749f-109">Overview of database logging</span></span>

<span data-ttu-id="e749f-110">Datubāzes reģistrēšana izseko specifiskas izmaiņas Microsoft Dynamics 365 Human Resources tabulās un laukos.</span><span class="sxs-lookup"><span data-stu-id="e749f-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="e749f-111">Šīs izmaiņas ietver ievietošanu, atjaunināšanu vai dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="e749f-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="e749f-112">Datu bāzes reģistrācija saglabā ierakstu par izmaiņām tabulās vai laukos datu bāzes žurnāla tabulā.</span><span class="sxs-lookup"><span data-stu-id="e749f-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="e749f-113">Biznesa datu bāzes reģistrācijas izmantošana ietver:</span><span class="sxs-lookup"><span data-stu-id="e749f-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="e749f-114">Tiek izveidots audita ieraksts par izmaiņām noteiktās tabulās, kurās ir sensitīva informācija.</span><span class="sxs-lookup"><span data-stu-id="e749f-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="e749f-115">Atsevišķu darbību izsekošana.</span><span class="sxs-lookup"><span data-stu-id="e749f-115">Tracking single transactions.</span></span> <span data-ttu-id="e749f-116">Datu bāzes reģistrēšana nav paredzēta automatizēto darbību izsekošanai, kas darbojas pakešuzdevumos.</span><span class="sxs-lookup"><span data-stu-id="e749f-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="e749f-117">Drošība datu bāzes reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="e749f-117">Security for database logging</span></span>

<span data-ttu-id="e749f-118">Datubāzes žurnālos var būt sensitīvi dati.</span><span class="sxs-lookup"><span data-stu-id="e749f-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="e749f-119">Ierobežojiet piekļuvi, lai iekļautu tikai tās drošības lomas, kurām nepieciešama piekļuve žurnāla datiem.</span><span class="sxs-lookup"><span data-stu-id="e749f-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="e749f-120">Datu bāzes reģistrēšana un veiktspēja</span><span class="sxs-lookup"><span data-stu-id="e749f-120">Database logging and performance</span></span>

<span data-ttu-id="e749f-121">Lai gan no biznesa perspektīvas tā ir vērtīga, datu bāzes reģistrēšana resursu izmantošanā un vadībā var būt dārga.</span><span class="sxs-lookup"><span data-stu-id="e749f-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="e749f-122">Datu bāzes reģistrēšanas veiktspējas ietekme ietver:</span><span class="sxs-lookup"><span data-stu-id="e749f-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="e749f-123">Datu bāzes žurnāla tabula var ātri augt un radīt datu bāzes apjoma palielinājumu.</span><span class="sxs-lookup"><span data-stu-id="e749f-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="e749f-124">Pieaugums ir atkarīgs no reģistrēto datu apjoma, ko izlemjat paturēt.</span><span class="sxs-lookup"><span data-stu-id="e749f-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="e749f-125">Pēc noklusējuma datu bāzes žurnāla tabula uztur tikai 30 dienu žurnāla datus.</span><span class="sxs-lookup"><span data-stu-id="e749f-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="e749f-126">Datu bāzes reģistrācija var negatīvi ietekmēt ilgstošos automatizētos procesus, piemēram, ilgstošo datu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="e749f-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="e749f-127">Noteikumi</span><span class="sxs-lookup"><span data-stu-id="e749f-127">Best practices</span></span>

<span data-ttu-id="e749f-128">Lai uzlabotu veiktspēju, ierobežojiet reģistrēšanas ierakstus, atlasot reģistrēšanai īpašus laukus, bet nereģistrējiet visas tabulas.</span><span class="sxs-lookup"><span data-stu-id="e749f-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="e749f-129">Lai palīdzētu uzturēt vispārējo veiktspēju, datu bāzes reģistrēšana ir ierobežota līdz 20 tabulām.</span><span class="sxs-lookup"><span data-stu-id="e749f-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="e749f-130">Dažreiz laukiem var reģistrēt tikai atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="e749f-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="e749f-131">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="e749f-131">Set up database logging</span></span>

<span data-ttu-id="e749f-132">Varat izmantot **Reģistrēšanas datu bāzes izmaiņu** ceļvedi, lai iestatītu datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="e749f-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="e749f-133">Ceļvedis sniedz elastīgu veidu, kā iestatīt reģistrāciju tabulām vai laukiem.</span><span class="sxs-lookup"><span data-stu-id="e749f-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="e749f-134">Dodieties uz **Sistēmas administrēšanu > Saites > Datu bāzes > Datu bāzes žurnāla iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e749f-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="e749f-135">Atlasiet **Jauns**, lai sāktu **Datu bāzes izmaiņu reģistrēšanas** ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="e749f-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="e749f-136">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="e749f-136">Select **Next**.</span></span> 
3. <span data-ttu-id="e749f-137">Vedņa lapā **Tabulas un lauki** atlasiet tabulas un laukus, kuros vēlaties iespējot datu bāzes reģistrēšanu, un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="e749f-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="e749f-138">Datu bāzes reģistrēšana nav pieejama visās personāla vadības datu bāzes tabulās.</span><span class="sxs-lookup"><span data-stu-id="e749f-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="e749f-139">Atlasot **Rādīt visas tabulas** zem saraksta, tiek izvērsts tabulu un lauku saraksts, lai parādītu visas datu bāzes tabulas, kurām ir pieejama datu bāzes reģistrēšana, bet tā būs pilna datu bāzu tabulu saraksta apakškopa.</span><span class="sxs-lookup"><span data-stu-id="e749f-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="e749f-140">Vedņa lapā **Izmaiņu tipi** atlasiet datu operācijas, kurām vēlaties reģistrēt katras tabulas un lauka izmaiņas, un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="e749f-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="e749f-141">Tālāk esošajā tabulā ir sniegts reģistrēšanai pieejamo datu operāciju apraksts.</span><span class="sxs-lookup"><span data-stu-id="e749f-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="e749f-142">Lapā **Pabeigt** pārskatiet veiktās izmaiņas un atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="e749f-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="e749f-143">Operācija</span><span class="sxs-lookup"><span data-stu-id="e749f-143">Operation</span></span> | <span data-ttu-id="e749f-144">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e749f-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="e749f-145">Izsekot jaunās darbības</span><span class="sxs-lookup"><span data-stu-id="e749f-145">Track new transactions</span></span> | <span data-ttu-id="e749f-146">Izveidojiet žurnālu jauniem ierakstiem, kas izveidoti tabulā.</span><span class="sxs-lookup"><span data-stu-id="e749f-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="e749f-147">Grāmatot</span><span class="sxs-lookup"><span data-stu-id="e749f-147">Update</span></span> | <span data-ttu-id="e749f-148">Izveidojiet žurnālu tabulu ierakstu atjauninājumiem vai atsevišķi atlasītu tabulas lauku atjauninājumiem.</span><span class="sxs-lookup"><span data-stu-id="e749f-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="e749f-149">Ja izvēlaties reģistrēt tabulas atjauninājumus, žurnāla ieraksts tiek izveidots ikreiz, kad tiek atjaunināts jebkurš tabulas ieraksta lauks.</span><span class="sxs-lookup"><span data-stu-id="e749f-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="e749f-150">Ja izvēlaties reģistrēt atjauninājumus noteiktiem laukiem, žurnāla ieraksts tiek izveidots tikai tad, kad šiem tabulas ierakstu laukiem tiek veikti atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="e749f-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="e749f-151">Delete</span><span class="sxs-lookup"><span data-stu-id="e749f-151">Delete</span></span> | <span data-ttu-id="e749f-152">Izveidojiet žurnālu ierakstiem, kas izdzēsti no tabulas.</span><span class="sxs-lookup"><span data-stu-id="e749f-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="e749f-153">Pārdēvēt atslēgu</span><span class="sxs-lookup"><span data-stu-id="e749f-153">Rename key</span></span> | <span data-ttu-id="e749f-154">Kad tabulas atslēga ir pārdēvēta, izveidojiet žurnāla ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e749f-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="e749f-155">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="e749f-155">Clean up database logs</span></span>

<span data-ttu-id="e749f-156">Varat izdzēst visu vai daļu no datu bāzes žurnāliem, izmantojot šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="e749f-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="e749f-157">Atlasiet visus žurnālus noteiktai tabulai.</span><span class="sxs-lookup"><span data-stu-id="e749f-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="e749f-158">Atlasiet specifiskus datu bāzes žurnāla tipus.</span><span class="sxs-lookup"><span data-stu-id="e749f-158">Select specific types of database log.</span></span>
- <span data-ttu-id="e749f-159">Atlasiet datumu un laiku, kad tika izveidots žurnāls.</span><span class="sxs-lookup"><span data-stu-id="e749f-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="e749f-160">Lai iestatītu datu bāzes žurnāla tīrīšanu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="e749f-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="e749f-161">Dodieties uz **Sistēmas administrēšana > Saites > Datu bāzes > Datu bāzes žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="e749f-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="e749f-162">Atlasiet **Tīrīt žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="e749f-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="e749f-163">Izvēlieties metodi, kā atlasīt žurnālus dzēšanai, ievadot vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="e749f-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="e749f-164">Tabulas ID</span><span class="sxs-lookup"><span data-stu-id="e749f-164">Table ID</span></span>
   - <span data-ttu-id="e749f-165">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="e749f-165">Type of log</span></span>
   - <span data-ttu-id="e749f-166">Izveidotais datums un laiks</span><span class="sxs-lookup"><span data-stu-id="e749f-166">Created date and time</span></span>

3. <span data-ttu-id="e749f-167">Izmantojiet cilni **Datu bāzes žurnāla tīrīšana**, lai noteiktu, kad palaist žurnāla tīrīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="e749f-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="e749f-168">Pēc noklusējuma datu bāzes žurnāli ir pieejami 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="e749f-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
