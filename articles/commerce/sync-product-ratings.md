---
title: Preču vērtējumu sinhronizācija pakalpojumā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīts, kā sinhronizēt preču vērtējumus risinājumā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ab6de4bfa619df74bafc5511affddd516bdb34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260313"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="8a83b-103">Preču vērtējumu sinhronizācija pakalpojumā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8a83b-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a83b-104">Šajā tēmā ir aprakstīts, kā sinhronizēt preču vērtējumus risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a83b-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8a83b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8a83b-105">Overview</span></span>

<span data-ttu-id="8a83b-106">Lai izmantotu preču vērtējumus vairākos kanālos, piemēram, pārdošanas punktā (POS) un zvanu centros, preču novērtējumi no vērtējumu un pārskatu pakalpojuma ir jāimportē Commerce kanāla datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="8a83b-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="8a83b-107">Kad preču vērtējumi ir pieejami vairākos kanālos, tie var netieši palīdzēt klientiem to mijiedarbības laikā ar pārdošanas partneriem.</span><span class="sxs-lookup"><span data-stu-id="8a83b-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="8a83b-108">Šajā tēmā ir aprakstīti tālāk norādītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="8a83b-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="8a83b-109">Konfigurējiet **Preču vērtēšanas sinhronizācijas darbu** kā pakešuzdevumu, lai sinhronizētu preču novērtējumus no **Vērtējumu un apskatu pakalpojuma**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="8a83b-110">Pārbaudīt, vai pakešuzdevumu preču vērtējuma sinhronizēšana bija veiksmīga.</span><span class="sxs-lookup"><span data-stu-id="8a83b-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="8a83b-111">Padarīt preces vērtējumus pieejamus POS.</span><span class="sxs-lookup"><span data-stu-id="8a83b-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="8a83b-112">Konfigurēt mazumtirdzniecības pakešuzdevumu, lai sinhronizētu preču vērtējumus.</span><span class="sxs-lookup"><span data-stu-id="8a83b-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a83b-113">Pirms sākat, pārliecinieties, ka ir instalēta Dynamics 365 Commerce versija 10.0.6 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="8a83b-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="8a83b-114">Komercijas plānotāja inicializēšana</span><span class="sxs-lookup"><span data-stu-id="8a83b-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="8a83b-115">Lai inicializētu komercijas plānotāju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="8a83b-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="8a83b-116">Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Inicializēt komercijas plānotāju**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="8a83b-117">Varat arī meklēt “inicializēt komercijas plānotāju”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="8a83b-118">Dialoglodziņā **Inicializēt komercijas plānotāju** pārliecinieties, vai opcija **Dzēst esošo konfigurāciju** ir iestatīta uz **Nē** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="8a83b-119">Pārbaudīt RetailProductRating apakšdarbu</span><span class="sxs-lookup"><span data-stu-id="8a83b-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="8a83b-120">Lai pārbaudītu, vai **RetailProductRating** apakšdarbs pastāv, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="8a83b-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="8a83b-121">Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Plānotāja apakšdarbi**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="8a83b-122">Vai arī meklējiet “plānotāja apakšdarbi”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="8a83b-123">Apakšdarbu sarakstā atrodiet vai meklējiet **RetailProductRating** apakšdarbu.</span><span class="sxs-lookup"><span data-stu-id="8a83b-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="8a83b-124">Tālāk redzamajā attēlā ir parādīts Commerce apakšdarba detalizētas informācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="8a83b-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Detalizēta informācija par RetailProductRating apakšdarbu](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="8a83b-126">Ja neatrodat **RetailProductRating** apakšdarbu, iespējams, jau esat palaidis darbu **Sinhronizēt preču vērtējumus** darbu un darbu **1040 CDX** pirms Commerce plānotāja inicializēšanas.</span><span class="sxs-lookup"><span data-stu-id="8a83b-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="8a83b-127">Šādā gadījumā veiciet šīs darbības, lai palaistu darbu **Pilnīga datu sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="8a83b-128">Dodieties uz **Retail un Commerce \> Headquarters uzstādīšanas programmas \> Commerce plānotājs \> Kanāla datubāze**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="8a83b-129">Vai arī meklējiet “kanāla datubāze”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="8a83b-130">Atlasiet sinhronizējamo kanāla datubāzi.</span><span class="sxs-lookup"><span data-stu-id="8a83b-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="8a83b-131">Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="8a83b-132">Dialoglodziņa nolaižamajā sarakstā **Atlasīt sadales grafiki** atlasiet **1040 — preces** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="8a83b-133">Atkārtojiet iepriekšējās procedūras darbības, lai pārbaudītu, vai **RetailProductRating** apakšdarbs ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="8a83b-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="8a83b-134">Preču vērtējumu importēšana</span><span class="sxs-lookup"><span data-stu-id="8a83b-134">Import product ratings</span></span>

<span data-ttu-id="8a83b-135">Lai importētu preču vērtējumus Commerce no vērtējumu un pārskatu pakalpojuma, rīkojieties, kā aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="8a83b-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="8a83b-136">Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Commerce plānotājs \> Sinhronizēt preces vērtējuma darbu**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="8a83b-137">Varat arī meklēt “Sinhronizēt preces vērtējuma darbu”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="8a83b-138">Dialoglodziņā **Izvilkt preces vērtējumus**, kas atrodas kopsavilkuma cilnē **Palaist fonā**, atlasiet **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="8a83b-139">Dialoglodziņā **Definēt periodiskumu** iestatiet periodiskuma modeli.</span><span class="sxs-lookup"><span data-stu-id="8a83b-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="8a83b-140">(Ieteicamā vērtība ir divas stundas.) Neplānojiet periodiskumu, kas ir mazāks par vienu stundu.</span><span class="sxs-lookup"><span data-stu-id="8a83b-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="8a83b-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-141">Select **OK**.</span></span>
1. <span data-ttu-id="8a83b-142">Iestatiet opciju **Pakešveida apstrāde** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="8a83b-143">Šis iestatījums palīdz garantēt, ka jūs varēsiet pārbaudīt žurnālus un pārbaudīt pakešuzdevuma statusu.</span><span class="sxs-lookup"><span data-stu-id="8a83b-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="8a83b-144">Atlasiet **Labi**, lai ieplānotu pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="8a83b-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="8a83b-145">Tālāk redzamajā attēlā ir parādīta pakešuzdevuma konfigurācija programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a83b-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Pakešuzdevumu preču vērtējuma sinhronizēšanas konfigurācija](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="8a83b-147">Pārbaudīt, vai pakešuzdevumu preču vērtējuma sinhronizēšana bija veiksmīga</span><span class="sxs-lookup"><span data-stu-id="8a83b-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="8a83b-148">Lai pārbaudītu, vai pakešuzdevums **Sinhronizēt preces vērtējumu** bija veiksmīgs, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8a83b-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="8a83b-149">Dodieties uz **Retail un commerce \> Sistēmas administrators \> Uzziņas \> Pakešuzdevumi** vai, ja izmantojat tikai Commerce noliktavas vienību (SKU), **Retail un Commerce \> Uzziņas un pārskati \> Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="8a83b-150">Vai arī meklējiet “Pakešuzdevumi”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="8a83b-151">Lai skatītu detalizētu informāciju par pakešuzdevumu, pakešuzdevumu sarakstā, kolonnā **Darba apraksts** meklējiet aprakstu, kas satur “Izvilkt preces vērtējumus”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="8a83b-152">Atlasiet darba ID, lai skatītu detalizētu informāciju par pakešuzdevumu, piemēram, plānoto sākuma datumu/laiku un periodiskuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="8a83b-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="8a83b-153">Tālāk esošajā attēlā parādīts piemērs ar pakešuzdevuma detalizētu informāciju programmā Commerce, kad pakešuzdevums tiek plānots izpildei divu stundu intervālos.</span><span class="sxs-lookup"><span data-stu-id="8a83b-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Pakešuzdevumu preču vērtējuma sinhronizēšanas detalizēta informācija](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="8a83b-155">Padarīt preces vērtējumus pieejamus POS</span><span class="sxs-lookup"><span data-stu-id="8a83b-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="8a83b-156">Vērtējumu un pārskatu risinājums Dynamics 365 Commerce ir vairāku kanālu risinājums.</span><span class="sxs-lookup"><span data-stu-id="8a83b-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="8a83b-157">Tomēr preču vērtējumi pēc noklusējuma netiek parādīti POS.</span><span class="sxs-lookup"><span data-stu-id="8a83b-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="8a83b-158">Lai palīdzētu klientiem veikalos skatīt vērtējumus un pārskatus, kad viņiem palīdz pārdošanas partneri, jums ir jāieslēdz preču vērtējumi POS.</span><span class="sxs-lookup"><span data-stu-id="8a83b-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="8a83b-159">Lai ieslēgtu preču vērtējumus POS, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="8a83b-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="8a83b-160">Pārejiet uz sadaļu **Retail un Commerce \> Commerce iestatīšana \> Parametri \> Komercijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="8a83b-161">Varat arī meklēt “Commerce parametri”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="8a83b-162">Cilnē **Konfigurācijas parametri** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="8a83b-163">Ievadiet nosaukumu, piemēram, **RatingsAndReviews.EnableProductRatingsForRetailStores**, un iestatiet vērtību uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="8a83b-164">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-164">Select **Save**.</span></span>
1. <span data-ttu-id="8a83b-165">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="8a83b-166">Vai arī meklējiet “Sadales grafiks”.</span><span class="sxs-lookup"><span data-stu-id="8a83b-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="8a83b-167">Darbu sarakstā atlasiet **1110** (**Globālā konfigurācija**) un pēc tam atlasiet **Palaist tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="8a83b-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="8a83b-168">Pēc tam, kad darbs ir veiksmīgi palaists, pārbaudiet, vai preču vērtējumi tagad ir redzami POS.</span><span class="sxs-lookup"><span data-stu-id="8a83b-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="8a83b-169">Tālāk esošajā attēlā parādīts piemērs par Commerce parametru konfigurāciju, lai POS sistēmā ieslēgtu preces vērtējumus.</span><span class="sxs-lookup"><span data-stu-id="8a83b-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Commerce parametru konfigurācija preču vērtējumiem POS sistēmā](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="8a83b-171">Nākamajā attēlā ir parādīts piemērs ar preces vērtējumiem POS sistēmā.</span><span class="sxs-lookup"><span data-stu-id="8a83b-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Preču vērtējumi POS sistēmā](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="8a83b-173">Nākamajā attēlā ir parādīts piemērs ar preces vērtējumiem zvanu centra kanālos.</span><span class="sxs-lookup"><span data-stu-id="8a83b-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Preču vērtējumi zvanu centra kanālā](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="8a83b-175">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8a83b-175">Additional resources</span></span>

[<span data-ttu-id="8a83b-176">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="8a83b-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="8a83b-177">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="8a83b-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="8a83b-178">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="8a83b-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="8a83b-179">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8a83b-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]