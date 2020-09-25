---
title: Projekta resursu plānošanas veiktspēja
description: Šī tēma sniedz informāciju par to, kā uzlabot resursu plānošanas veiktspēju lielam projektu skaitam.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760609"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="0978a-103">Projekta resursu plānošanas veiktspēja</span><span class="sxs-lookup"><span data-stu-id="0978a-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="0978a-104">Veiktspējas problēmas, kas saistītas ar resursu plānošanu, var notikt, kad projektu skaits sasniedz tūkstošus.</span><span class="sxs-lookup"><span data-stu-id="0978a-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="0978a-105">Lai uzlabotu resursu plānošanas veiktspēju, ir pieejams līdzeklis, kas ļauj lietotājiem samazināt laiku, kas nepieciešams, lai palaistu resursu pieejamības veidlapu.</span><span class="sxs-lookup"><span data-stu-id="0978a-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="0978a-106">Konkrēti tas noņem resursu noslodzes apkopošanas sinhronizācijas procesu un izmanto tabulu **ResProjectResource**, lai paātrinātu resursu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0978a-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="0978a-107">Ievērojiet, ka tabula **ResRollup** vairs netiks izmantota.</span><span class="sxs-lookup"><span data-stu-id="0978a-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0978a-108">Ja ir atkarība vai nu no resursu noslodzes apkopošanas sinhronizācijas procesa, vai no tabulas **ResProjectResource**, neizmantojiet šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="0978a-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0978a-109">Iespējot resursu plānošanas veiktspējas uzlabojumu</span><span class="sxs-lookup"><span data-stu-id="0978a-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="0978a-110">Lai iespējotu resursu plānošanas veiktspējas uzlabojumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="0978a-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="0978a-111">Dodieties uz **Līdzekļu pārvaldība** > **Visas**, un līdzekļu sarakstā atrodiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="0978a-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0978a-112">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="0978a-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="0978a-113">Ja sarakstā nevarat atrast līdzekli, atlasiet **Pārbaudīt, vai nav atjauninājumu** lai atsvaidzinātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0978a-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="0978a-114">Atsvaidziniet pārlūkprogrammu un pēc tam dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Projektu resursi** > **Sinhronizēt resursu kalendāru noslodzi visiem uzņēmumiem**.</span><span class="sxs-lookup"><span data-stu-id="0978a-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="0978a-115">Iestatiet **Noņemt esošos noslodzes ierakstus** uz **Jā**, lai noņemtu iepriekšējos datus.</span><span class="sxs-lookup"><span data-stu-id="0978a-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0978a-116">Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0978a-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="0978a-117">Laukā **Perioda kods** atlasiet periodu, kurā jāģenerē dati.</span><span class="sxs-lookup"><span data-stu-id="0978a-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0978a-118">Ja atlasāt perioda kodu, sākuma un beigu datums nav jādefinē.</span><span class="sxs-lookup"><span data-stu-id="0978a-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="0978a-119">Ja atstājat tukšu lauku **Perioda kods**, atlasiet konkrētus sākuma un beigu datumus, lai ģenerētu datus.</span><span class="sxs-lookup"><span data-stu-id="0978a-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="0978a-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0978a-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="0978a-121">Tādējādi tabulā **ResCalendarCapacity** visos uzņēmumos jūsu vidē tiks izplatīti vispārīgi dati, tāpēc pakešuzdevums ir jāizpilda tikai vienā juridiskā personā.</span><span class="sxs-lookup"><span data-stu-id="0978a-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0978a-122">Šie pakešuzdevuma dati ir vajadzīgi, lai aprēķinātu resursu noslodz, izmantojot saistīto kalendāru.</span><span class="sxs-lookup"><span data-stu-id="0978a-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="0978a-123">Dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Projektu resursi** > **Projekta resursu aizpildīšana visos uzņēmumos** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0978a-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="0978a-124">Šis ir datu jaunināšanas skripts vispārējiem datiem tabulās **ResProjectResource** , **ResCalendarDateTimeRange** un **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="0978a-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="0978a-125">Tiek atjauninātas arī lauka **PSAPRojSchedRole.RootActivity** vērtības.</span><span class="sxs-lookup"><span data-stu-id="0978a-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="0978a-126">Ja tas netiek izpildīts, jūs saņemsiet brīdinājumu, kad mēģināsit izpildīt resursu plānošanas operācijas.</span><span class="sxs-lookup"><span data-stu-id="0978a-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="0978a-127">Izslēgt resursu plānošanas veiktspējas uzlabojumu</span><span class="sxs-lookup"><span data-stu-id="0978a-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="0978a-128">Dodieties uz **Līdzekļu pārvaldība** > **Visas**  un meklējiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="0978a-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="0978a-129">Atlasiet līdzekli un pēc tam atlasiet pogu **Atspējot**.</span><span class="sxs-lookup"><span data-stu-id="0978a-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="0978a-130">Atsvaidziniet pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0978a-130">Refresh your browser.</span></span>
4. <span data-ttu-id="0978a-131">Dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Noslodzes sinhronizācija** > **Sinhronizēt resursa noslodzes apkopojumus**.</span><span class="sxs-lookup"><span data-stu-id="0978a-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="0978a-132">Lapā **Noslodzes apkopošanas sinhronizācija** iestatiet **Esošo noslodzes ierakstu noņemšana** uz **Jā**, lai noņemtu iepriekšējos datus.</span><span class="sxs-lookup"><span data-stu-id="0978a-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="0978a-133">Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0978a-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="0978a-134">Laukā **Perioda kods** atlasiet periodu, kurā jāģenerē dati.</span><span class="sxs-lookup"><span data-stu-id="0978a-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="0978a-135">Ja atlasāt perioda kodu, sākuma un beigu datums nav jādefinē.</span><span class="sxs-lookup"><span data-stu-id="0978a-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="0978a-136">Ja atstājat tukšu lauku **Perioda kods**, atlasiet konkrētus sākuma un beigu datumus, lai ģenerētu datus.</span><span class="sxs-lookup"><span data-stu-id="0978a-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="0978a-137">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0978a-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="0978a-138">Tādējādi tabulā **ResRollup** visos uzņēmumos jūsu vidē tiks izplatīti vispārīgi dati, tāpēc pakešuzdevums ir jāizpilda tikai vienā juridiskā personā.</span><span class="sxs-lookup"><span data-stu-id="0978a-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="0978a-139">Šis pakešuzdevums ir nepieciešams visiem **Resursu pieejamības** skatiem.</span><span class="sxs-lookup"><span data-stu-id="0978a-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="0978a-140">Ja šis pakešuzdevums netiek izpildīts, **ResRollup** dati tiks ģenerēti ātri, kas var aizņemt laiku.</span><span class="sxs-lookup"><span data-stu-id="0978a-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
