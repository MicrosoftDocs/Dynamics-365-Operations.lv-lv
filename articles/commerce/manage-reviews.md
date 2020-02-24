---
title: Vērtējumu un atsauksmju pārvaldība
description: Šajā tēmā izskaidrots, kā pārvaldīt vērtējumus un apskatus, izmantojot Microsoft Dynamics 365 Commerce vērtējumu un apskatu regulēšanas rīku.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027246"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="31ba2-103">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="31ba2-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31ba2-104">Šajā tēmā izskaidrots, kā pārvaldīt vērtējumus un apskatus, izmantojot Microsoft Dynamics 365 Commerce vērtējumu un apskatu regulēšanas rīku.</span><span class="sxs-lookup"><span data-stu-id="31ba2-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="31ba2-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="31ba2-105">Overview</span></span>

<span data-ttu-id="31ba2-106">Dynamics 365 Commerce izmanto Microsoft Azure Cognitive Service, lai automātiski moderētu apskata tekstu, rediģējot nepiedienīgos vārdus.</span><span class="sxs-lookup"><span data-stu-id="31ba2-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="31ba2-107">Turklāt moderatori var izmantot vērtējumu un apskatu moderēšanas rīku tālāk minētajiem manuālajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="31ba2-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="31ba2-108">Moderēt apskatus, atbildot uz tiem vai noņemot tos.</span><span class="sxs-lookup"><span data-stu-id="31ba2-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="31ba2-109">Dzēst klienta apskatu pēc klienta pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="31ba2-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="31ba2-110">Importēt visu preču vērtējumu un apskatu datus lielā apjomā Microsoft Power BI veidnē, lai varētu analizēt vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="31ba2-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="31ba2-111">Piekļuve vērtējumu un pārskatu regulēšanas līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="31ba2-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="31ba2-112">Lai piekļūtu vērtējumu un pārskatu regulēšanas līdzekļiem e-komercijas vietnes pārvaldības rīkā, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="31ba2-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-113">Pierakstieties portālā [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="31ba2-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="31ba2-114">Atveriet projektu, kas satur vidi, kurā vēlaties inicializēt e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="31ba2-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="31ba2-115">Sadaļā **Vides** atlasiet vidi.</span><span class="sxs-lookup"><span data-stu-id="31ba2-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="31ba2-116">Sadaļā **Vides līdzekļi** atlasiet **Mazumtirdzniecības pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="31ba2-117">Cilnē **e-komercija** sadaļā **Saites**atlasiet **e-commerce vietnes pārvaldības rīks**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="31ba2-118">Apskata lasīšana</span><span class="sxs-lookup"><span data-stu-id="31ba2-118">Read a review</span></span> 

1. <span data-ttu-id="31ba2-119">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="31ba2-120">Lai filtrētu apskatus, kas tiek parādīti pēc preces ID, preces nosaukuma vai apskata teksta, izmantojiet meklēšanas lauku lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="31ba2-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="31ba2-121">Papildu filtri ļauj ierobežot apskatus pēc perioda, vērtējuma, kanāla vai svarīguma statusa (noņemts, atbildēts vai ziņots).</span><span class="sxs-lookup"><span data-stu-id="31ba2-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderēšanas sākumlapa](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="31ba2-123">Atbildēšana uz apskatu</span><span class="sxs-lookup"><span data-stu-id="31ba2-123">Respond to a review</span></span> 

<span data-ttu-id="31ba2-124">Dažkārt klienti, kuri iegādājušies preci, izsaka savu apmierinātību vai neapmierinātību vai nesaprot, kā izmantot preci.</span><span class="sxs-lookup"><span data-stu-id="31ba2-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="31ba2-125">Kā moderators varat ievietot atbildi uz apskatu.</span><span class="sxs-lookup"><span data-stu-id="31ba2-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="31ba2-126">Šī atbilde parādīsies vietnē kopā ar apskatu.</span><span class="sxs-lookup"><span data-stu-id="31ba2-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="31ba2-127">Lai atbildētu uz apskatu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="31ba2-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-128">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="31ba2-129">Atrodiet un atlasiet apskatu, kam nepieciešama atbilde.</span><span class="sxs-lookup"><span data-stu-id="31ba2-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="31ba2-130">Rekvizītu rūts labajā pusē atlasiet **Pievienot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="31ba2-131">Ievadiet atbildes tekstu un parādāmo atbildētāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="31ba2-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="31ba2-132">Noklusējuma atbildētāja vārds ir **Moderators**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="31ba2-133">Pēc pabeigšanas atlasiet **Ievietot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-133">When you've finished, select **Post response**.</span></span>

![Atbildēšana uz apskatu](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="31ba2-135">Apskata noņemšana</span><span class="sxs-lookup"><span data-stu-id="31ba2-135">Take down a review</span></span> 

<span data-ttu-id="31ba2-136">Dažreiz moderatoriem ir biznesa pamatojums, lai noņemtu klienta apskatus.</span><span class="sxs-lookup"><span data-stu-id="31ba2-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="31ba2-137">Lai noņemtu apskatu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="31ba2-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-138">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="31ba2-139">Atrodiet un atlasiet apskatu, kas jānoņem.</span><span class="sxs-lookup"><span data-stu-id="31ba2-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="31ba2-140">Labajā pusē rekvizītu rūtī atlasiet noņemšanas iemeslu un pēc tam atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="31ba2-141">Klienta apskata dzēšana pēc klienta pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="31ba2-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="31ba2-142">Dažkārt klienti vēlas, lai viņu vērtējumu un apskatu dati tiktu neatgriezeniski dzēsti no e-tirdzniecības vietnes.</span><span class="sxs-lookup"><span data-stu-id="31ba2-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="31ba2-143">Moderators, kas saņem noņemšanas pieprasījumu no klienta, var noņemt klienta datus, izmantojot apstatu dzēšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="31ba2-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="31ba2-144">Lai atrastu un dzēstu klienta datus, moderatoram ir nepieciešama e-pasta adrese, ko klients izmantojis, lai pierakstītos un sniegtu apskatus.</span><span class="sxs-lookup"><span data-stu-id="31ba2-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="31ba2-145">Lai atrastu un dzēstu klienta datus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="31ba2-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-146">Dodieties uz **Sākums \> Apskati \> Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="31ba2-147">Laukā **Meklēt lietotājus pēc e-pasta adreses** ievadiet klienta e-pasta adresi un pēc tam atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="31ba2-148">Ja klients veicis kādas apskatīšanas aktivitātes (piemēram, iesniedzis apskatus, balsojis par cita klienta apskatu noderīgumu vai komentējis cita klienta apskatu), tiek parādīti rezultāti.</span><span class="sxs-lookup"><span data-stu-id="31ba2-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="31ba2-149">Katram elementam ir poga **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="31ba2-150">Katram elementam, kas jāizdzēš, atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="31ba2-151">Kad tiek pieprasīts apstiprinājums, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klienta datu dzēšana](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="31ba2-153">Var paiet līdz septiņām dienām, lai dati tiktu pilnībā noņemti no sistēmas.</span><span class="sxs-lookup"><span data-stu-id="31ba2-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="31ba2-154">Moderatoriem jāpaziņo klientiem par šo kavēšanos.</span><span class="sxs-lookup"><span data-stu-id="31ba2-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="31ba2-155">Ja klienti ir mainījuši savu vārdu konta iestatījumos, meklēšanas rezultātos var parādīties vairāki elementi.</span><span class="sxs-lookup"><span data-stu-id="31ba2-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="31ba2-156">Šādā gadījumā, lai pilnībā dzēstu klienta datus, moderatoram katram elementam jāatlasa **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="31ba2-157">Vērtējumu un apskatu datu lejupielāde</span><span class="sxs-lookup"><span data-stu-id="31ba2-157">Download ratings and reviews data</span></span>

<span data-ttu-id="31ba2-158">Vērtējumu un apskatu moderēšanas rīks ļauj moderatoriem importēt vērtējumu un apskatu datus lielā apjomā, lai varētu analizēt tendences.</span><span class="sxs-lookup"><span data-stu-id="31ba2-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="31ba2-159">Ir pieejama Power BI veidne, kas ietver pamata rādītājus.</span><span class="sxs-lookup"><span data-stu-id="31ba2-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="31ba2-160">Moderatori var izmantot šo veidni, lai savienotu lielā apjomā importētos datus un skatītu informācijas paneli.</span><span class="sxs-lookup"><span data-stu-id="31ba2-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="31ba2-161">Viņiem nav jāizveido pielāgots informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="31ba2-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="31ba2-162">Moderatori var arī pielāgot Power BI veidni, lai tā atbilstu viņu īpašajām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="31ba2-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="31ba2-163">Lai lejupielādētu vērtējumu un apskatu datus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="31ba2-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-164">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="31ba2-165">Atlasiet **Lejupielādēt apskatu datus**, lai lejupielādētu vērtējumu un apskatu datus lielā apjomā ar komatu atdalītu vērtību (CSV) formātā.</span><span class="sxs-lookup"><span data-stu-id="31ba2-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="31ba2-166">Vērtējumu un apskatu tendenču skatīšana</span><span class="sxs-lookup"><span data-stu-id="31ba2-166">View ratings and reviews trends</span></span>

<span data-ttu-id="31ba2-167">Moderatori var lejupielādēt Power BI veidni, lai varētu skatīt tendences informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="31ba2-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="31ba2-168">Lai skatītu vērtējumu un apskatu tendences, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="31ba2-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="31ba2-169">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="31ba2-170">Atlasiet **PowerBI veidne**, lai lejupielādētu veidni.</span><span class="sxs-lookup"><span data-stu-id="31ba2-170">Select **PowerBI template** to download the template.</span></span>

    ![Power BI veidnes lejupielāde](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="31ba2-172">Atveriet lejupielādēto veidni, izmantojot Power BI programmu.</span><span class="sxs-lookup"><span data-stu-id="31ba2-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="31ba2-173">Aizveriet parādījušos dialoglodziņu **Piekļuve tīmekļa saturam** un pēc tam aizveriet parādījušos "Atsvaidzināt" kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="31ba2-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="31ba2-174">Dodieties uz **Sākums**, atlasiet **Rediģēt vaicājumus** un pēc tam atlasiet **Datu avota iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="31ba2-175">Dialoglodziņā **Datu avota iestatījumi** atlasiet **Mainīt avotu**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="31ba2-176">Laukā **URL** ievadiet ceļu uz apskatu datiem, ko lejupielādējāt iepriekšējā procedūrā (piemēram, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="31ba2-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL lauks ar komatu atdalīto vērtību dialoglodziņā](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="31ba2-178">Atlasiet **Labi** un pēc tam atlasiet **Piemērot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="31ba2-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="31ba2-179">Lai datu avotam tiktu piemērotas izmaiņas, būs nepieciešamas vienas līdz divas minūtes.</span><span class="sxs-lookup"><span data-stu-id="31ba2-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="31ba2-180">Atlasiet **Tendenču loksne**, lai skatītu vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="31ba2-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Vērtējumu un apskatu tendences](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="31ba2-182">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="31ba2-182">Additional resources</span></span>

[<span data-ttu-id="31ba2-183">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="31ba2-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="31ba2-184">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="31ba2-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="31ba2-185">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="31ba2-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="31ba2-186">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="31ba2-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
