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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054816"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="86f4e-103">Datu bāzu reģistrācijas konfigurēšana un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="86f4e-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="86f4e-104">Jūs variet reģistrēt izmaiņas tabulās un laukos Dynamics 365 Human Resources ar datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="86f4e-105">Šajā tēmā ir aprakstīts, kā:</span><span class="sxs-lookup"><span data-stu-id="86f4e-105">This topic describes how to:</span></span>

- <span data-ttu-id="86f4e-106">Pārvaldīt drošības un veiktspējas datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="86f4e-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="86f4e-107">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="86f4e-107">Set up database logging</span></span>
- <span data-ttu-id="86f4e-108">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="86f4e-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="86f4e-109">Datu bāzes reģistrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="86f4e-109">Overview of database logging</span></span>

<span data-ttu-id="86f4e-110">Datubāzes reģistrēšana izseko specifiskas izmaiņas Microsoft Dynamics 365 Human Resources tabulās un laukos.</span><span class="sxs-lookup"><span data-stu-id="86f4e-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="86f4e-111">Šīs izmaiņas ietver ievietošanu, atjaunināšanu vai dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="86f4e-112">Datu bāzes reģistrācija saglabā ierakstu par izmaiņām tabulās vai laukos datu bāzes žurnāla tabulā.</span><span class="sxs-lookup"><span data-stu-id="86f4e-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="86f4e-113">Biznesa datu bāzes reģistrācijas izmantošana ietver:</span><span class="sxs-lookup"><span data-stu-id="86f4e-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="86f4e-114">Tiek izveidots audita ieraksts par izmaiņām noteiktās tabulās, kurās ir sensitīva informācija.</span><span class="sxs-lookup"><span data-stu-id="86f4e-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="86f4e-115">Atsevišķu darbību izsekošana.</span><span class="sxs-lookup"><span data-stu-id="86f4e-115">Tracking single transactions.</span></span> <span data-ttu-id="86f4e-116">Datu bāzes reģistrēšana nav paredzēta automatizēto darbību izsekošanai, kas darbojas pakešuzdevumos.</span><span class="sxs-lookup"><span data-stu-id="86f4e-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="86f4e-117">Drošība datu bāzes reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="86f4e-117">Security for database logging</span></span>

<span data-ttu-id="86f4e-118">Datubāzes žurnālos var būt sensitīvi dati.</span><span class="sxs-lookup"><span data-stu-id="86f4e-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="86f4e-119">Ierobežojiet piekļuvi, lai iekļautu tikai tās drošības lomas, kurām nepieciešama piekļuve žurnāla datiem.</span><span class="sxs-lookup"><span data-stu-id="86f4e-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="86f4e-120">Datu bāzes reģistrēšana un veiktspēja</span><span class="sxs-lookup"><span data-stu-id="86f4e-120">Database logging and performance</span></span>

<span data-ttu-id="86f4e-121">Lai gan no biznesa perspektīvas tā ir vērtīga, datu bāzes reģistrēšana resursu izmantošanā un vadībā var būt dārga.</span><span class="sxs-lookup"><span data-stu-id="86f4e-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="86f4e-122">Datu bāzes reģistrēšanas veiktspējas ietekme ietver:</span><span class="sxs-lookup"><span data-stu-id="86f4e-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="86f4e-123">Datu bāzes žurnāla tabula var ātri augt un radīt datu bāzes apjoma palielinājumu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="86f4e-124">Pieaugums ir atkarīgs no reģistrēto datu apjoma, ko izlemjat paturēt.</span><span class="sxs-lookup"><span data-stu-id="86f4e-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="86f4e-125">Pēc noklusējuma datu bāzes žurnāla tabula uztur tikai 30 dienu žurnāla datus.</span><span class="sxs-lookup"><span data-stu-id="86f4e-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="86f4e-126">Datu bāzes reģistrācija var negatīvi ietekmēt ilgstošos automatizētos procesus, piemēram, ilgstošo datu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="86f4e-127">Noteikumi</span><span class="sxs-lookup"><span data-stu-id="86f4e-127">Best practices</span></span>

<span data-ttu-id="86f4e-128">Lai uzlabotu veiktspēju, ierobežojiet reģistrēšanas ierakstus, atlasot reģistrēšanai īpašus laukus, bet nereģistrējiet visas tabulas.</span><span class="sxs-lookup"><span data-stu-id="86f4e-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="86f4e-129">Lai palīdzētu uzturēt vispārējo veiktspēju, datu bāzes reģistrēšana ir ierobežota līdz 20 tabulām.</span><span class="sxs-lookup"><span data-stu-id="86f4e-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="86f4e-130">Dažreiz laukiem var reģistrēt tikai atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="86f4e-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="86f4e-131">Iestatīt datu bāzes reģistrēšanu</span><span class="sxs-lookup"><span data-stu-id="86f4e-131">Set up database logging</span></span>

<span data-ttu-id="86f4e-132">Varat izmantot **Reģistrēšanas datu bāzes izmaiņu** ceļvedi, lai iestatītu datu bāzes reģistrēšanu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="86f4e-133">Ceļvedis sniedz elastīgu veidu, kā iestatīt reģistrāciju tabulām vai laukiem.</span><span class="sxs-lookup"><span data-stu-id="86f4e-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="86f4e-134">Dodieties uz **Sistēmas administrēšanu > Saites > Datu bāzes > Datu bāzes žurnāla iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="86f4e-135">Atlasiet **Jauns**, lai sāktu **Datu bāzes izmaiņu reģistrēšanas** ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="86f4e-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="86f4e-136">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-136">Select **Next**.</span></span> 
3. <span data-ttu-id="86f4e-137">Vedņa lapā **Tabulas un lauki** atlasiet tabulas un laukus, kuros vēlaties iespējot datu bāzes reģistrēšanu, un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="86f4e-138">Datu bāzes reģistrēšana nav pieejama visās personāla vadības datu bāzes tabulās.</span><span class="sxs-lookup"><span data-stu-id="86f4e-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="86f4e-139">Atlasot **Rādīt visas tabulas** zem saraksta, tiek izvērsts tabulu un lauku saraksts, lai parādītu visas datu bāzes tabulas, kurām ir pieejama datu bāzes reģistrēšana, bet tā būs pilna datu bāzu tabulu saraksta apakškopa.</span><span class="sxs-lookup"><span data-stu-id="86f4e-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="86f4e-140">Vedņa lapā **Izmaiņu tipi** atlasiet datu operācijas, kurām vēlaties reģistrēt katras tabulas un lauka izmaiņas, un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="86f4e-141">Tālāk esošajā tabulā ir sniegts reģistrēšanai pieejamo datu operāciju apraksts.</span><span class="sxs-lookup"><span data-stu-id="86f4e-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="86f4e-142">Lapā **Pabeigt** pārskatiet veiktās izmaiņas un atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="86f4e-143">Operācija</span><span class="sxs-lookup"><span data-stu-id="86f4e-143">Operation</span></span> | <span data-ttu-id="86f4e-144">Apraksts</span><span class="sxs-lookup"><span data-stu-id="86f4e-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="86f4e-145">Izsekot jaunās darbības</span><span class="sxs-lookup"><span data-stu-id="86f4e-145">Track new transactions</span></span> | <span data-ttu-id="86f4e-146">Izveidojiet žurnālu jauniem ierakstiem, kas izveidoti tabulā.</span><span class="sxs-lookup"><span data-stu-id="86f4e-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="86f4e-147">Grāmatot</span><span class="sxs-lookup"><span data-stu-id="86f4e-147">Update</span></span> | <span data-ttu-id="86f4e-148">Izveidojiet žurnālu tabulu ierakstu atjauninājumiem vai atsevišķi atlasītu tabulas lauku atjauninājumiem.</span><span class="sxs-lookup"><span data-stu-id="86f4e-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="86f4e-149">Ja izvēlaties reģistrēt tabulas atjauninājumus, žurnāla ieraksts tiek izveidots ikreiz, kad tiek atjaunināts jebkurš tabulas ieraksta lauks.</span><span class="sxs-lookup"><span data-stu-id="86f4e-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="86f4e-150">Ja izvēlaties reģistrēt atjauninājumus noteiktiem laukiem, žurnāla ieraksts tiek izveidots tikai tad, kad šiem tabulas ierakstu laukiem tiek veikti atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="86f4e-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="86f4e-151">Delete</span><span class="sxs-lookup"><span data-stu-id="86f4e-151">Delete</span></span> | <span data-ttu-id="86f4e-152">Izveidojiet žurnālu ierakstiem, kas izdzēsti no tabulas.</span><span class="sxs-lookup"><span data-stu-id="86f4e-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="86f4e-153">Pārdēvēt atslēgu</span><span class="sxs-lookup"><span data-stu-id="86f4e-153">Rename key</span></span> | <span data-ttu-id="86f4e-154">Kad tabulas atslēga ir pārdēvēta, izveidojiet žurnāla ierakstu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="86f4e-155">Iztīrīt datu bāzes žurnālus</span><span class="sxs-lookup"><span data-stu-id="86f4e-155">Clean up database logs</span></span>

<span data-ttu-id="86f4e-156">Varat izdzēst visu vai daļu no datu bāzes žurnāliem, izmantojot šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="86f4e-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="86f4e-157">Atlasiet visus žurnālus noteiktai tabulai.</span><span class="sxs-lookup"><span data-stu-id="86f4e-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="86f4e-158">Atlasiet specifiskus datu bāzes žurnāla tipus.</span><span class="sxs-lookup"><span data-stu-id="86f4e-158">Select specific types of database log.</span></span>
- <span data-ttu-id="86f4e-159">Atlasiet datumu un laiku, kad tika izveidots žurnāls.</span><span class="sxs-lookup"><span data-stu-id="86f4e-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="86f4e-160">Lai iestatītu datu bāzes žurnāla tīrīšanu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="86f4e-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="86f4e-161">Dodieties uz **Sistēmas administrēšana > Saites > Datu bāzes > Datu bāzes žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="86f4e-162">Atlasiet **Tīrīt žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="86f4e-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="86f4e-163">Izvēlieties metodi, kā atlasīt žurnālus dzēšanai, ievadot vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="86f4e-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="86f4e-164">Tabulas ID</span><span class="sxs-lookup"><span data-stu-id="86f4e-164">Table ID</span></span>
   - <span data-ttu-id="86f4e-165">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="86f4e-165">Type of log</span></span>
   - <span data-ttu-id="86f4e-166">Izveidotais datums un laiks</span><span class="sxs-lookup"><span data-stu-id="86f4e-166">Created date and time</span></span>

3. <span data-ttu-id="86f4e-167">Izmantojiet cilni **Datu bāzes žurnāla tīrīšana**, lai noteiktu, kad palaist žurnāla tīrīšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="86f4e-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="86f4e-168">Pēc noklusējuma datu bāzes žurnāli ir pieejami 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="86f4e-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
