---
title: Darba pasūtījumu izveidošana
description: Šajā tēmā ir paskaidrots, kā izveidot darba pasūtījumus programmā Asset Management.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131797"
---
# <a name="creating-work-orders"></a><span data-ttu-id="efc45-103">Darba pasūtījumu izveidošana</span><span class="sxs-lookup"><span data-stu-id="efc45-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efc45-104">Kad ir izveidots profilaktisks uzturēšanas darbs, nākamais solis ir darba pasūtījumu izveide darbiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="efc45-105">Šo soli var izpildīt, izmantojot vienu no uzturēšanas grafikiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="efc45-106">Uzturēšanas grafikā ieplānotajiem darbiem var būt dažādi atsauces veidi, kā norādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="efc45-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="efc45-107">Atsauces tips</span><span class="sxs-lookup"><span data-stu-id="efc45-107">Reference type</span></span> | <span data-ttu-id="efc45-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="efc45-108">Description</span></span> |
|---|---|
| <span data-ttu-id="efc45-109">Uzturēšanas plāni</span><span class="sxs-lookup"><span data-stu-id="efc45-109">Maintenance plans</span></span> | <span data-ttu-id="efc45-110">Profilaktiskie uzturēšanas darbi, balstoties uz apkopes plāna veidiem *Laiks* vai *Skaitītājs*.</span><span class="sxs-lookup"><span data-stu-id="efc45-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="efc45-111">Uzturēšanas cikls</span><span class="sxs-lookup"><span data-stu-id="efc45-111">Maintenance rounds</span></span> | <span data-ttu-id="efc45-112">Profilaktiskie uzturēšanas darbi, kas satur vairākus līdzekļus, kam vajadzīga viena veida uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="efc45-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="efc45-113">Uzturēšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="efc45-113">Maintenance request</span></span> | <span data-ttu-id="efc45-114">Manuāli izveidots pieprasījums par pamatlīdzekļa uzturēšanu vai remontu.</span><span class="sxs-lookup"><span data-stu-id="efc45-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="efc45-115">Šo pieprasījumu var konvertēt uz darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="efc45-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="efc45-116">Darba pasūtījumu izveide, pamatojoties uz uzturēšanas grafiku</span><span class="sxs-lookup"><span data-stu-id="efc45-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="efc45-117">Lai izveidotu darba pasūtījumus, kas ir balstīti uz uzturēšanas grafiku, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="efc45-118">Atveriet vienu no šīm lapām atkarībā no tā, kā vēlaties atlasīt grafika krājumus darba pasūtījumiem:</span><span class="sxs-lookup"><span data-stu-id="efc45-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="efc45-119">Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)</span><span class="sxs-lookup"><span data-stu-id="efc45-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="efc45-120">Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)</span><span class="sxs-lookup"><span data-stu-id="efc45-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="efc45-121">Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)</span><span class="sxs-lookup"><span data-stu-id="efc45-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="efc45-122">Režģī atzīmējiet izvēles rūtiņu katram plānotajam uzturēšanas darbam, kuram vēlaties izveidot darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="efc45-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="efc45-123">Darbību rūtī atlasiet **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="efc45-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="efc45-124">Tiek parādīts dialoglodziņš **Izveidot darba pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="efc45-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="efc45-125">Kopīgais paredzamais stundu skaits atlasītajām rindām tiek parādīts laukā **Uzturēšanas prognozes stundas**.</span><span class="sxs-lookup"><span data-stu-id="efc45-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Darba pasūtījumu dialoglodziņa izveide](media/18-preventive-maintenance.png)

1. <span data-ttu-id="efc45-127">Sadaļā **Parametri** norādiet izveidojamo darba pasūtījumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="efc45-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="efc45-128">Izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="efc45-128">Select one of the following options:</span></span>

    - <span data-ttu-id="efc45-129">**Viens darba pasūtījums katrā rindā** – izveidot vienu darba pasūtījumu katrai uzturēšanas grafika rindai.</span><span class="sxs-lookup"><span data-stu-id="efc45-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="efc45-130">**Viens darba pasūtījums katram** – izveidojiet darba pasūtījumus, kas ir grupēti atbilstoši citu opciju iestatījumiem, kaskļūst pieejami, izvēloties šo opciju.</span><span class="sxs-lookup"><span data-stu-id="efc45-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="efc45-131">Laukā **Darba pasūtījuma veids** atlasiet darba pasūtījuma veidu, ko izmantot visiem izveidotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="efc45-132">Atlasiet **Labi**, lai izveidotu darba pasūtījumus atbilstoši iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="efc45-133">Grupēt darba pasūtījuma rindas, kas tiek automātiski izveidotas uzturēšanas plāna izpildes laikā</span><span class="sxs-lookup"><span data-stu-id="efc45-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efc45-134">Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no privātā priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="efc45-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="efc45-135">Saturs un funkcionalitāte var tikt mainīti.</span><span class="sxs-lookup"><span data-stu-id="efc45-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="efc45-136">Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="efc45-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="efc45-137">Šī funkcija ļauj definēt noteikumus darba pasūtījumu rindu grupēšanai saskaņā ar vienu darba pasūtījumu, ja sistēma ir iestatīta darba pasūtījumu automātiskai ģenerēšanai, pamatojoties uz uzturēšanas plānu.</span><span class="sxs-lookup"><span data-stu-id="efc45-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="efc45-138">Iepriekš automātiski izveidotie darba pasūtījumi var ietvert tikai vienu rindu.</span><span class="sxs-lookup"><span data-stu-id="efc45-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="efc45-139">Tomēr tagad var grupēt darba pasūtījumus pēc, piemēram, pamatlīdzekļa, pamatlīdzekļa tipa vai funkcionālās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="efc45-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="efc45-140">(Manuāli izveidotos darba pasūtījumus jau var grupēt šādā veidā, kā aprakstīts šīs tēmas iepriekšējā sadaļā.)</span><span class="sxs-lookup"><span data-stu-id="efc45-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="efc45-141">Iespējot grupēšanu automātiski ģenerētiem darba pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="efc45-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="efc45-142">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="efc45-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="efc45-143">Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="efc45-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="efc45-144">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="efc45-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="efc45-145">**Modulise:** *Līdzekļu pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="efc45-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="efc45-146">**Līdzekļa nosaukums:** *(Priekšskatījums) Piemērot noteikumus darba pasūtījumu grupēšanai uzturēšanas plāna izpildes laikā*</span><span class="sxs-lookup"><span data-stu-id="efc45-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="efc45-147">Iestatīt grupēšanu automātiski ģenerētiem darba pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="efc45-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="efc45-148">Lai iestatītu grupēšanu automātiski ģenerētiem darba pasūtījumiem, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="efc45-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="efc45-149">Dodieties uz **Līdzekļu pārvaldība \> Uzstādīšana \> Preventīvā uzturēšana \> Uzturēšanas plāni**.</span><span class="sxs-lookup"><span data-stu-id="efc45-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="efc45-150">Katram plānam, kur vēlaties izveidot grupētus darba pasūtījumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="efc45-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="efc45-151">Sarakstu rūtī atlasiet plānu.</span><span class="sxs-lookup"><span data-stu-id="efc45-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="efc45-152">Kopsavilkuma cilnē **Rindas** pārliecinieties, vai katrā rindā ir atzīmēta izvēles rūtiņa **Automātiski izveidot**.</span><span class="sxs-lookup"><span data-stu-id="efc45-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="efc45-153">Dodieties uz **Līdzekļu pārvaldība \> Periodiskās darbības \> Profilaktiskā uzturēšana \> Ieplānot uzturēšanas plānus**.</span><span class="sxs-lookup"><span data-stu-id="efc45-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="efc45-154">Dialoglodziņa **Plānot uzturēšanas plānus** sadaļā **Periods** norādiet plāna laika diapazonu (cik tālu uz priekšu meklējiet plānotos uzturēšanas darbus, lai ģenerētu darbu).</span><span class="sxs-lookup"><span data-stu-id="efc45-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="efc45-155">Iestatiet opciju **Automātiski izveidot darba pasūtījumu no grafika** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="efc45-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="efc45-156">Sadaļā **Apliecinājums** izvēlieties vienu no šīm opcijām:</span><span class="sxs-lookup"><span data-stu-id="efc45-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="efc45-157">**Viens darba pasūtījums katrā rindā** – izveidot vienu darba pasūtījumu katrai uzturēšanas grafika rindai.</span><span class="sxs-lookup"><span data-stu-id="efc45-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="efc45-158">(Šī opcija nodrošina to pašu funkcionalitāti, kas ir pieejama, ja ir atspējota funkcija *Piemērot darba pasūtījumu grupēšanas kārtulas, kamēr uzturēšanas plāna līdzeklis*.)</span><span class="sxs-lookup"><span data-stu-id="efc45-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="efc45-159">**Viens darba pasūtījums katram** – izveidojiet darba pasūtījumus, kas ir grupēti atbilstoši citu opciju iestatījumiem, kaskļūst pieejami, izvēloties šo opciju.</span><span class="sxs-lookup"><span data-stu-id="efc45-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="efc45-160">Ja vēlaties, lai opcijas tiek lietotas, kad palaižat tikai dažus no jūsu uzturēšanas plāniem, kopsavilkuma cilnē **Iekļaujamie ieraksti** pievienojiet filtrus pēc vajadzības, tāpat kā citiem Microsoft Dynamics 365 Supply Chain Management  pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="efc45-161">Kopsavilkuma cilnē **Palaist fonā** iestatiet pakešuzdevumu un plānošanas opcijas pēc vajadzības, tāpat kā citiem Supply Chain Management pakešuzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="efc45-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="efc45-162">Atlasiet **Labi**, lai palaistu un/vai plānotu atlasītos uzturēšanas plānus.</span><span class="sxs-lookup"><span data-stu-id="efc45-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
