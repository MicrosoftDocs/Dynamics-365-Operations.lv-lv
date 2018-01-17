---
title: "Finanšu pārskatu datuves atiestatīšana"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu datuvi."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: lv-lv
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="a883d-103">Finanšu pārskatu datuves atiestatīšana</span><span class="sxs-lookup"><span data-stu-id="a883d-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a883d-104">Šajā tēmā ir izskaidrots, kā atiestatīt finanšu pārskatu datuvi tālāk norādītajās versijās.</span><span class="sxs-lookup"><span data-stu-id="a883d-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="a883d-105">Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati, laidiens 7.2.6.0 un jaunāks</span><span class="sxs-lookup"><span data-stu-id="a883d-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="a883d-106">Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati, laidiens 7.0.10000.4 un jaunāks</span><span class="sxs-lookup"><span data-stu-id="a883d-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="a883d-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (lokālā)</span><span class="sxs-lookup"><span data-stu-id="a883d-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="a883d-108">Lai saņemtu Finance and Operations Finanšu pārskati laidienu 7.2.6.0, varat lejupielādēt KB 4052514 no <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="a883d-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="a883d-109">Finanšu pārskatu datuves atiestatīšana Finance and Operations Finanšu pārskati laidienam 7.2.6.0 un jaunākam</span><span class="sxs-lookup"><span data-stu-id="a883d-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="a883d-110">Finanšu pārskatu datuves atiestatīšana no pārskatu veidotāja</span><span class="sxs-lookup"><span data-stu-id="a883d-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-111">Šajā procedūrā ietvertās darbības tiek atbalstītas Finance and Operations Finanšu pārskati laidienā 7.2.6.0 un jaunākos.</span><span class="sxs-lookup"><span data-stu-id="a883d-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="a883d-112">Ja jums ir agrāks laidiens, sazinieties ar atbalsta darba grupu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="a883d-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="a883d-113">Noteiktos scenārijos jums var būt nepieciešams atiestatīt finanšu pārskatu datuvi.</span><span class="sxs-lookup"><span data-stu-id="a883d-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="a883d-114">Šo uzdevumu varat veikt pārskatu veidotāja klientā.</span><span class="sxs-lookup"><span data-stu-id="a883d-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="a883d-115">Tālāk ir aprakstīti daži scenāriji, kuros varētu rasties nepieciešamība atiestatīt datuvi.</span><span class="sxs-lookup"><span data-stu-id="a883d-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="a883d-116">Finance and Operations datu bāze tika atjaunota, bet datuve netika atjaunota.</span><span class="sxs-lookup"><span data-stu-id="a883d-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="a883d-117">Kādam periodam tiek rādīti nepareizi dati.</span><span class="sxs-lookup"><span data-stu-id="a883d-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="a883d-118">Atbalsta dienests jūs instruē, ka traucējummeklēšanas procedūras ietvaros ir nepieciešams atiestatīt datuvi.</span><span class="sxs-lookup"><span data-stu-id="a883d-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="a883d-119">Datuves atiestatīšanu vajadzētu veikt tikai laikā, kad datu bāzes apstrādes apjoms ir mazs.</span><span class="sxs-lookup"><span data-stu-id="a883d-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="a883d-120">Atiestatīšanas procesa laika finanšu pārskati nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="a883d-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="a883d-121">Datuves atiestatīšana</span><span class="sxs-lookup"><span data-stu-id="a883d-121">Reset the data mart</span></span>

<span data-ttu-id="a883d-122">Lai atiestatītu datuvi, pārskatu veidotāja izvēlnē **Rīki** atlasiet **Atiestatīt datuvi**.</span><span class="sxs-lookup"><span data-stu-id="a883d-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="a883d-123">Tiek parādīts dialoglodziņš ar divām sadaļām: **Statistika** un **Atiestatīt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="a883d-124">[![Datuves atiestatīšanas dialoglodziņš](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="a883d-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="a883d-125">Integrācijas mēģinājumi</span><span class="sxs-lookup"><span data-stu-id="a883d-125">Integration attempts</span></span>

<span data-ttu-id="a883d-126">Režģī **Integrācijas mēģinājumi** tiek rādīts, cik reižu sistēma ir mēģinājusi integrēt transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a883d-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="a883d-127">Ja pirmie daži mēģinājumi ir nesekmīgi, sistēma datu integrēšanu turpina mēģināt vairākas dienas.</span><span class="sxs-lookup"><span data-stu-id="a883d-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="a883d-128">Varat zināt, ka datuvi ir nepieciešams atiestatīt, ja šo mēģinājumu skaits ir 8 vai vairāk, kā arī, ja ir daudz dimensiju kombināciju vai transakciju ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a883d-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="a883d-129">Šādā gadījumā par datiem netiek ziņots.</span><span class="sxs-lookup"><span data-stu-id="a883d-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="a883d-130">Datu statuss</span><span class="sxs-lookup"><span data-stu-id="a883d-130">Data status</span></span>

<span data-ttu-id="a883d-131">Režģī **Datu statuss** ir sniegts momentuzņēmums par transakcijām, valūtas maiņas kursiem un dimensiju vērtībām datuvē.</span><span class="sxs-lookup"><span data-stu-id="a883d-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="a883d-132">Liels daudzums novecojušu ierakstu norāda, ka ierakstiem ir notikuši daudzi atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="a883d-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="a883d-133">Šāda situācija var palēnināt pārskatu ģenerēšanas laikus.</span><span class="sxs-lookup"><span data-stu-id="a883d-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="a883d-134">Nesalāgotas galvenā konta kategorijas</span><span class="sxs-lookup"><span data-stu-id="a883d-134">Misaligned main account categories</span></span>

<span data-ttu-id="a883d-135">Ja izmantojat laidienu, kas ir agrāks par Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati laidienu 7.2.1, datuvi var būt nepieciešams atiestatīt, ja pārdēvējat kontus vai pārvietojat kontus starp dažādām kategorijām.</span><span class="sxs-lookup"><span data-stu-id="a883d-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="a883d-136">Šīs darbības var izraisīt nepareizu galvenā konta kategoriju salāgošanu.</span><span class="sxs-lookup"><span data-stu-id="a883d-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="a883d-137">Laukā **Nesalāgotas galvenā konta kategorijas** tiek rādīts, vai ir radusies šī problēma.</span><span class="sxs-lookup"><span data-stu-id="a883d-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="a883d-138">Datuves atiestatīšana Finance and Operations Finanšu pārskati laidienā 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="a883d-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="a883d-139">Lai datuvi atiestatītu Finance and Operations Finanšu pārskati laidienā 7.2.6.0 un agrākos laidienos, dialoglodziņā **Atiestatīt datuvi** atzīmējiet izvēles rūtiņu **Atiestatīt datuvi** un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a883d-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="a883d-140">Datuves atiestatīšanu vajadzētu veikt tikai laikā, kad nav ieplānots darbs.</span><span class="sxs-lookup"><span data-stu-id="a883d-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="a883d-141">[![Datuves atiestatīšanas izvēles rūtiņa](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="a883d-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="a883d-142">Datuves atiestatīšana un iemesla atlasīšana Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati laidienā 7.3.0</span><span class="sxs-lookup"><span data-stu-id="a883d-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="a883d-143">Ja konstatējat, ka ir nepieciešams atiestatīt datuvi, atzīmējiet izvēles rūtiņu **Atiestatīt datuvi** un pēc tam laukā **Iemesls** atlasiet iemeslu.</span><span class="sxs-lookup"><span data-stu-id="a883d-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="a883d-144">Ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="a883d-144">The following options are available:</span></span>

- <span data-ttu-id="a883d-145">**Trūkstoši vai nepareizi dati** — pamatojoties uz statistisko informāciju, esat konstatējis, ka trūkst datu.</span><span class="sxs-lookup"><span data-stu-id="a883d-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="a883d-146">Pirms turpināšanas ieteicams sadarboties ar atbalsta dienestu, lai noteiktu cēloni.</span><span class="sxs-lookup"><span data-stu-id="a883d-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="a883d-147">**Atjaunot datu bāzi** — Finance and Operations datu bāze tika atjaunota, bet datuve netika atjaunota.</span><span class="sxs-lookup"><span data-stu-id="a883d-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="a883d-148">**Cits** — datuvi atiestatāt cita iemesla dēļ.</span><span class="sxs-lookup"><span data-stu-id="a883d-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="a883d-149">Ja raizējaties, ka varētu pastāvēt kāda problēma, sazinieties ar atbalsta dienestu, lai to noskaidrotu.</span><span class="sxs-lookup"><span data-stu-id="a883d-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="a883d-150">[![Atiestatīt data mart](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="a883d-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-151">Pirms sākat atiestatīšanu, ir jāpārbauda, vai visiem datuves atiestatīšanas uzdevumiem ir pabeigta sākotnējā ielāde.</span><span class="sxs-lookup"><span data-stu-id="a883d-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="a883d-152">To varat pārbaudīt, meklējot vērtību kolonnā “Pēdējais izpildlaiks”, atlasot **Rīki** &gt; **Integrācijas statuss**.</span><span class="sxs-lookup"><span data-stu-id="a883d-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="a883d-153">Notīrīt lietotājus un uzņēmumus</span><span class="sxs-lookup"><span data-stu-id="a883d-153">Clear users and companies</span></span>

<span data-ttu-id="a883d-154">Atzīmējiet izvēles rūtiņu **Notīrīt lietotājus un uzņēmumus**, ja atjaunojāt savu datu bāzi, bet pēc tam veicāt kādas izmaiņas lietotājiem vai uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="a883d-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="a883d-155">Vajadzībai atzīmēt šo izvēles rūtiņu vajadzētu rasties reti.</span><span class="sxs-lookup"><span data-stu-id="a883d-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="a883d-156">Kad esat gatavs sākt atiestatīšanas procesu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a883d-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="a883d-157">Tiek parādīta uzvedne ar lūgumu apstiprināt, ka esat gatavs procesa sākšanai.</span><span class="sxs-lookup"><span data-stu-id="a883d-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="a883d-158">Ņemiet vērā, ka atiestatīšanas laikā finanšu pārskati nav pieejami un pēc tam notiek sākotnējo datu integrēšana.</span><span class="sxs-lookup"><span data-stu-id="a883d-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="a883d-159">Ja vēlaties pārskatīt integrācijas statusu, atlasiet **Rīki** &gt; **Integrācijas statuss**, lai apskatītu pēdējo reizi, kad tika veikta integrēšana, un tās statusu.</span><span class="sxs-lookup"><span data-stu-id="a883d-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="a883d-160">[![Integrācijas statusa skatīšana](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="a883d-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-161">Atiestatīšana ir pabeigta, kad visos kartējumos tiek rādīts statuss RanToCompletion un logā “Integrācijas statuss“” kreisajā apakšējā stūrī ir rakstīts “Integrēšana pabeigta”.</span><span class="sxs-lookup"><span data-stu-id="a883d-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="a883d-162">Finanšu pārskatu datuves atiestatīšana Finance and Operations Finanšu pārskati laidienam 7.0.10000.4 un jaunākam</span><span class="sxs-lookup"><span data-stu-id="a883d-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="a883d-163">Ja savu Finance and Operations datu bāzi kaut kad atjaunojat no dublējuma vai kopējat datu bāzi no citas vides, ir jāizpilda šajā sadaļā norādītās darbības, lai palīdzētu nodrošināt, ka finanšu pārskatu datuve pareizi izmanto atjaunoto Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="a883d-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-164">Šajā procedūrā ietvertās darbības tiek atbalstītas Microsoft Dynamics AX programmas versijai 7.0.1 (2016. gada maijs) (programmas būvējums 7.0.1265.23014 un finanšu pārskatu būvējums 7.0.10000.4) un vēlākai.</span><span class="sxs-lookup"><span data-stu-id="a883d-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="a883d-165">Ja lietojat vecāku Finance and Operations versiju, sazinieties ar atbalsta dienestu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="a883d-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="a883d-166">Pārskatu definīciju eksportēšana</span><span class="sxs-lookup"><span data-stu-id="a883d-166">Export report definitions</span></span>

<span data-ttu-id="a883d-167">Vispirms izpildiet darbības pārskatu dizainu eksportēšanai no pārskatu veidotāja.</span><span class="sxs-lookup"><span data-stu-id="a883d-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="a883d-168">Pārskatu veidotājā atlasiet **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="a883d-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="a883d-169">Atlasiet eksportējamo veidošanas bloku grupu un pēc tam atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a883d-170">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="a883d-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="a883d-171">Atlasiet eksportējamās pārskatu definīcijas, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a883d-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="a883d-172">Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, atlasiet **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="a883d-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="a883d-173">Lai eksportētu noteiktus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet atbilstošo cilni un pēc tam atlasiet eksportējamos vienumus.</span><span class="sxs-lookup"><span data-stu-id="a883d-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="a883d-174">Lai cilnē atlasītu vairākus vienumus, nospiediet un turiet taustiņu Ctrl. Kad eksportēšanai atlasāt pārskatus, tiek atlasītas arī saistītās rindas, kolonnas, koki un dimensiju kopas.</span><span class="sxs-lookup"><span data-stu-id="a883d-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="a883d-175">Atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-175">Select **Export**.</span></span>
5. <span data-ttu-id="a883d-176">Ievadiet faila nosaukumu un atlasiet drošu atrašanās vietu, kur vēlaties saglabāt eksportētās pārskatu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="a883d-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="a883d-177">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-177">Select **Save**.</span></span>

<span data-ttu-id="a883d-178">Failu varat kopēt vai augšupielādēt drošā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="a883d-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="a883d-179">Šādi failu vēlāk var importēt citā vidē.</span><span class="sxs-lookup"><span data-stu-id="a883d-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="a883d-180">Informācija par Microsoft Azure krātuves konta lietošanu skatiet šeit [Datu pārsūtīšana, izmantojot komandrindas utilītu AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="a883d-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-181">Krātuves kontu Microsoft nenodrošina Dynamics 365 for Finance and Operations līguma ietvaros.</span><span class="sxs-lookup"><span data-stu-id="a883d-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="a883d-182">Jums ir jāiegādājas krātuves konts vai jāizmanto atsevišķa Azure abonementa krātuves konts.</span><span class="sxs-lookup"><span data-stu-id="a883d-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="a883d-183">Ņemiet vērā D diska uzvedību Azure virtuālajās mašīnās (VM).</span><span class="sxs-lookup"><span data-stu-id="a883d-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="a883d-184">Eksportētās veidošanas bloku grupas nedrīkst ilgstoši glabāt D diskā. Papildinformāciju par pagaidu diskiem skatiet šeit: [Izpratne par pagaidu disku Windows Azure virtuālajās mašīnās](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="a883d-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="a883d-185">Pakalpojumu apturēšana</span><span class="sxs-lookup"><span data-stu-id="a883d-185">Stop services</span></span>

<span data-ttu-id="a883d-186">Tālāk norādītajos Microsoft Windows pakalpojumus būs atvērti savienojumi ar Finance and Operations datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="a883d-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="a883d-187">Tādēļ ir jālieto Microsoft attālā darbvirsma, lai izveidotu savienojumu ar visiem datoriem šajā vidē, un pēc tam ir jāizmanto fails services.msc, lai apturētu šos pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="a883d-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="a883d-188">Globālā tīmekļa publicēšanas pakalpojums (visos Application Object Servers [AOS] datoros)</span><span class="sxs-lookup"><span data-stu-id="a883d-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="a883d-189">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="a883d-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="a883d-190">Management Reporter 2012 Process Service (tikai biznesa informācijas [BI] datoros)</span><span class="sxs-lookup"><span data-stu-id="a883d-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="a883d-191">Atiestatīt</span><span class="sxs-lookup"><span data-stu-id="a883d-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="a883d-192">Visjaunākās MinorVersionDataUpgrade.zip pakotnes lejupielādēšana</span><span class="sxs-lookup"><span data-stu-id="a883d-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="a883d-193">Lejupielādējiet visjaunāko MinorVersionDataUpgrade.zip pakotni.</span><span class="sxs-lookup"><span data-stu-id="a883d-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="a883d-194">Norādījumus par to, kā atrast un lejupielādēt pareizo datu jaunināšanas pakotnes versiju, skatiet šeit: [Visjaunākās izvietojamās datu jaunināšanas pakotnes lejupielādēšana](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="a883d-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="a883d-195">Lai lejupielādētu MinorVersionDataUpgrade.zip pakotni, nav nepieciešams jauninājums.</span><span class="sxs-lookup"><span data-stu-id="a883d-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="a883d-196">Tādēļ jums ir tikai jāizpilda darbības attiecīgās tēmas sadaļā “Visjaunākās izvietojamās datu jaunināšanas pakotnes lejupielādēšana”.</span><span class="sxs-lookup"><span data-stu-id="a883d-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="a883d-197">Visas pārējās tēmā aprakstītās darbības varat izlaist.</span><span class="sxs-lookup"><span data-stu-id="a883d-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="a883d-198">Skriptu palaišana ar Finance and Operations datu bāzi</span><span class="sxs-lookup"><span data-stu-id="a883d-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="a883d-199">Palaidiet tālāk norādītos skriptus ar Finance and Operations datu bāzi (nevis ar finanšu pārskatu datu bāzi).</span><span class="sxs-lookup"><span data-stu-id="a883d-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="a883d-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="a883d-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="a883d-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="a883d-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="a883d-202">Šie skripti palīdz nodrošināt, ka lietotāju, lomu un izmaiņu izsekošanas iestatījumi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="a883d-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="a883d-203">Windows PowerShell komandas palaišana datu bāzes atiestatīšanai</span><span class="sxs-lookup"><span data-stu-id="a883d-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="a883d-204">AOS datorā palaidiet Microsoft Windows PowerShell kā lietotājs ar administratora tiesībām un palaidiet tālāk norādītās komandas, lai atiestatītu integrāciju starp Finance and Operations un finanšu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="a883d-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="a883d-205">Tālāk ir sniegts paskaidrojums par komandā **Reset-DatamartIntegration** ietvertajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="a883d-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="a883d-206">Parametra **-Reason** derīgās vērtības ir **SERVICING**, **BADDATA** un **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="a883d-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="a883d-207">Parametra **-ReasonDetail** vērtība ir brīvs teksts.</span><span class="sxs-lookup"><span data-stu-id="a883d-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="a883d-208">Iemesla un iemesla informācijas vērtības tiek reģistrētas telemetrijas/vides pārraudzībā.</span><span class="sxs-lookup"><span data-stu-id="a883d-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="a883d-209">Pēc šo komandu palaišanas jums tiks lūgts ievadīt **Y**, lai apstiprinātu, ka vēlaties atiestatīt datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="a883d-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="a883d-210">Pakalpojumu restartēšana</span><span class="sxs-lookup"><span data-stu-id="a883d-210">Restart services</span></span>

<span data-ttu-id="a883d-211">Izmantojiet failu services.msc, lai atkal startētu pakalpojumus, ko iepriekš apturējāt.</span><span class="sxs-lookup"><span data-stu-id="a883d-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="a883d-212">Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)</span><span class="sxs-lookup"><span data-stu-id="a883d-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="a883d-213">Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)</span><span class="sxs-lookup"><span data-stu-id="a883d-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="a883d-214">Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)</span><span class="sxs-lookup"><span data-stu-id="a883d-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="a883d-215">Pārskatu definīciju importēšana</span><span class="sxs-lookup"><span data-stu-id="a883d-215">Import report definitions</span></span>

<span data-ttu-id="a883d-216">Importējiet savus pārskatu dizainus no pārskatu veidotāja, izmantojot eksportēšanas laikā izveidoto failu.</span><span class="sxs-lookup"><span data-stu-id="a883d-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="a883d-217">Pārskatu veidotājā atlasiet **Uzņēmums** &gt; **Veidošanas bloku grupas**.</span><span class="sxs-lookup"><span data-stu-id="a883d-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="a883d-218">Atlasiet eksportējamo veidošanas bloku grupu un pēc tam atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a883d-219">Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="a883d-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="a883d-220">Atlasiet veidošanas bloku **Noklusējums** un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="a883d-221">Atlasiet failu, kurā ir eksportētās pārskatu definīcijas, un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="a883d-222">Dialoglodziņā **Importēšana** atlasiet importējamās pārskata definīcijas.</span><span class="sxs-lookup"><span data-stu-id="a883d-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="a883d-223">Lai importētu visas pārskatu definīcijas un saistītos veidošanas blokus, atlasiet **Atlasīt visu**.</span><span class="sxs-lookup"><span data-stu-id="a883d-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="a883d-224">Lai importētu noteiktus pārskatus, rindas, kolonnas, kokus vai dimensiju kopas, atlasiet importējamos vienumus.</span><span class="sxs-lookup"><span data-stu-id="a883d-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="a883d-225">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a883d-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="a883d-226">Finanšu pārskatu datuves atiestatīšana programmai Finance and Operations (lokālā)</span><span class="sxs-lookup"><span data-stu-id="a883d-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="a883d-227">Līdziet visiem lietotājiem iziet no Finance and Operations pārskatu veidotāja un finanšu pārskatu apgabala.</span><span class="sxs-lookup"><span data-stu-id="a883d-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="a883d-228">Palaidiet tālāk norādīto skriptu ar finanšu pārskatu datu bāzi (MRDB).</span><span class="sxs-lookup"><span data-stu-id="a883d-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="a883d-229">Apcērtiet vai izdzēsiet visus ierakstus no tabulas FINANCIALREPORTS programmas Finance and Operations datu bāzē (AXDB).</span><span class="sxs-lookup"><span data-stu-id="a883d-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="a883d-230">Apcērtiet vai izdzēsiet visus ierakstus no tabulas FINANCIALREPORTVERSION, ja šāda tabula pastāv programmas Finance and Operations datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="a883d-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="a883d-231">Ja šī tabula nepastāv programmas Finance and Operations datu bāzē, izlaidiet šo soli.</span><span class="sxs-lookup"><span data-stu-id="a883d-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="a883d-232">Palaidiet skriptu **ResetDatamart.sql** ar finanšu pārskatu datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="a883d-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="a883d-233">Šis skripts atspējo datuves integrēšanu, izdzēš visus datuves datus un pēc tam no jauna iespējo datuves integrēšanu.</span><span class="sxs-lookup"><span data-stu-id="a883d-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="a883d-234">Pēc atiestatīšanas varat manuāli pārbaudīt datu pārlādēšanu, finanšu pārskatu datu bāzei izpildot tālāk norādīto vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="a883d-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="a883d-235">Pārliecinieties, vai visām rindām ir vērtība **LastRunTime** un vai vienums **StateType** ir iestatīts uz **5**.</span><span class="sxs-lookup"><span data-stu-id="a883d-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="a883d-236">Vienuma **StateType** vērtība **5** norāda, ka dati tika sekmīgi pārlādēti.</span><span class="sxs-lookup"><span data-stu-id="a883d-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="a883d-237">Vērtība **7** norāda uz kļūmes stāvokli.</span><span class="sxs-lookup"><span data-stu-id="a883d-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="a883d-238">Reizēm organizācijas hierarhijas kartei šāds stāvoklis ir pēc pirmās izpildīšanas reizes.</span><span class="sxs-lookup"><span data-stu-id="a883d-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="a883d-239">Taču kļūmes stāvoklim vajadzētu atrisināties automātiski.</span><span class="sxs-lookup"><span data-stu-id="a883d-239">However, the faulted state but should be automatically resolved.</span></span>

