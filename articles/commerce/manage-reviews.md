---
title: Vērtējumu un atsauksmju pārvaldība
description: Šajā tēmā izskaidrots, kā pārvaldīt vērtējumus un apskatus, izmantojot Microsoft Dynamics 365 Commerce vērtējumu un apskatu regulēšanas rīku.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698030"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="76e83-103">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="76e83-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="76e83-104">Šajā tēmā izskaidrots, kā pārvaldīt vērtējumus un apskatus, izmantojot Microsoft Dynamics 365 Commerce vērtējumu un apskatu regulēšanas rīku.</span><span class="sxs-lookup"><span data-stu-id="76e83-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="76e83-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="76e83-105">Overview</span></span>

<span data-ttu-id="76e83-106">Dynamics 365 Commerce izmanto Microsoft Azure Cognitive Service, lai automātiski moderētu apskata tekstu, rediģējot nepiedienīgos vārdus.</span><span class="sxs-lookup"><span data-stu-id="76e83-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="76e83-107">Turklāt moderatori var izmantot vērtējumu un apskatu moderēšanas rīku tālāk minētajiem manuālajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="76e83-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="76e83-108">Moderēt apskatus, atbildot uz tiem vai noņemot tos.</span><span class="sxs-lookup"><span data-stu-id="76e83-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="76e83-109">Dzēst klienta apskatu pēc klienta pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="76e83-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="76e83-110">Importēt visu preču vērtējumu un apskatu datus lielā apjomā Microsoft Power BI veidnē, lai varētu analizēt vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="76e83-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="76e83-111">Apskata lasīšana</span><span class="sxs-lookup"><span data-stu-id="76e83-111">Read a review</span></span> 

1. <span data-ttu-id="76e83-112">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="76e83-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="76e83-113">Lai filtrētu apskatus, kas tiek parādīti pēc preces ID, preces nosaukuma vai apskata teksta, izmantojiet meklēšanas lauku lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="76e83-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="76e83-114">Papildu filtri ļauj ierobežot apskatus pēc perioda, vērtējuma, kanāla vai svarīguma statusa (noņemts, atbildēts vai ziņots).</span><span class="sxs-lookup"><span data-stu-id="76e83-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderēšanas sākumlapa](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="76e83-116">Atbildēšana uz apskatu</span><span class="sxs-lookup"><span data-stu-id="76e83-116">Respond to a review</span></span> 

<span data-ttu-id="76e83-117">Dažkārt klienti, kuri iegādājušies preci, izsaka savu apmierinātību vai neapmierinātību vai nesaprot, kā izmantot preci.</span><span class="sxs-lookup"><span data-stu-id="76e83-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="76e83-118">Kā moderators varat ievietot atbildi uz apskatu.</span><span class="sxs-lookup"><span data-stu-id="76e83-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="76e83-119">Šī atbilde parādīsies vietnē kopā ar apskatu.</span><span class="sxs-lookup"><span data-stu-id="76e83-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="76e83-120">Lai atbildētu uz apskatu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="76e83-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="76e83-121">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="76e83-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="76e83-122">Atrodiet un atlasiet apskatu, kam nepieciešama atbilde.</span><span class="sxs-lookup"><span data-stu-id="76e83-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="76e83-123">Rekvizītu rūts labajā pusē atlasiet **Pievienot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="76e83-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="76e83-124">Ievadiet atbildes tekstu un parādāmo atbildētāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="76e83-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="76e83-125">Noklusējuma atbildētāja vārds ir **Moderators**.</span><span class="sxs-lookup"><span data-stu-id="76e83-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="76e83-126">Pēc pabeigšanas atlasiet **Ievietot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="76e83-126">When you've finished, select **Post response**.</span></span>

![Atbildēšana uz apskatu](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="76e83-128">Apskata noņemšana</span><span class="sxs-lookup"><span data-stu-id="76e83-128">Take down a review</span></span> 

<span data-ttu-id="76e83-129">Dažreiz moderatoriem ir biznesa pamatojums, lai noņemtu klienta apskatus.</span><span class="sxs-lookup"><span data-stu-id="76e83-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="76e83-130">Lai noņemtu apskatu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="76e83-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="76e83-131">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="76e83-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="76e83-132">Atrodiet un atlasiet apskatu, kas jānoņem.</span><span class="sxs-lookup"><span data-stu-id="76e83-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="76e83-133">Labajā pusē rekvizītu rūtī atlasiet noņemšanas iemeslu un pēc tam atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="76e83-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="76e83-134">Klienta apskata dzēšana pēc klienta pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="76e83-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="76e83-135">Dažkārt klienti vēlas, lai viņu vērtējumu un apskatu dati tiktu neatgriezeniski dzēsti no e-tirdzniecības vietnes.</span><span class="sxs-lookup"><span data-stu-id="76e83-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="76e83-136">Moderators, kas saņem noņemšanas pieprasījumu no klienta, var noņemt klienta datus, izmantojot apstatu dzēšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="76e83-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="76e83-137">Lai atrastu un dzēstu klienta datus, moderatoram ir nepieciešama e-pasta adrese, ko klients izmantojis, lai pierakstītos un sniegtu apskatus.</span><span class="sxs-lookup"><span data-stu-id="76e83-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="76e83-138">Lai atrastu un dzēstu klienta datus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="76e83-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="76e83-139">Dodieties uz **Sākums \> Apskati \> Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="76e83-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="76e83-140">Laukā **Meklēt lietotājus pēc e-pasta adreses** ievadiet klienta e-pasta adresi un pēc tam atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="76e83-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="76e83-141">Ja klients veicis kādas apskatīšanas aktivitātes (piemēram, iesniedzis apskatus, balsojis par cita klienta apskatu noderīgumu vai komentējis cita klienta apskatu), tiek parādīti rezultāti.</span><span class="sxs-lookup"><span data-stu-id="76e83-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="76e83-142">Katram elementam ir poga **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="76e83-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="76e83-143">Katram elementam, kas jāizdzēš, atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="76e83-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="76e83-144">Kad tiek pieprasīts apstiprinājums, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="76e83-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klienta datu dzēšana](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="76e83-146">Var paiet līdz septiņām dienām, lai dati tiktu pilnībā noņemti no sistēmas.</span><span class="sxs-lookup"><span data-stu-id="76e83-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="76e83-147">Moderatoriem jāpaziņo klientiem par šo kavēšanos.</span><span class="sxs-lookup"><span data-stu-id="76e83-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="76e83-148">Ja klienti ir mainījuši savu vārdu konta iestatījumos, meklēšanas rezultātos var parādīties vairāki elementi.</span><span class="sxs-lookup"><span data-stu-id="76e83-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="76e83-149">Šādā gadījumā, lai pilnībā dzēstu klienta datus, moderatoram katram elementam jāatlasa **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="76e83-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="76e83-150">Vērtējumu un apskatu datu lejupielāde</span><span class="sxs-lookup"><span data-stu-id="76e83-150">Download ratings and reviews data</span></span>

<span data-ttu-id="76e83-151">Vērtējumu un apskatu moderēšanas rīks ļauj moderatoriem importēt vērtējumu un apskatu datus lielā apjomā, lai varētu analizēt tendences.</span><span class="sxs-lookup"><span data-stu-id="76e83-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="76e83-152">Ir pieejama Power BI veidne, kas ietver pamata rādītājus.</span><span class="sxs-lookup"><span data-stu-id="76e83-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="76e83-153">Moderatori var izmantot šo veidni, lai savienotu lielā apjomā importētos datus un skatītu informācijas paneli.</span><span class="sxs-lookup"><span data-stu-id="76e83-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="76e83-154">Viņiem nav jāizveido pielāgots informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="76e83-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="76e83-155">Moderatori var arī pielāgot Power BI veidni, lai tā atbilstu viņu īpašajām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="76e83-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="76e83-156">Lai lejupielādētu vērtējumu un apskatu datus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="76e83-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="76e83-157">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="76e83-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="76e83-158">Atlasiet **Lejupielādēt apskatu datus**, lai lejupielādētu vērtējumu un apskatu datus lielā apjomā ar komatu atdalītu vērtību (CSV) formātā.</span><span class="sxs-lookup"><span data-stu-id="76e83-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="76e83-159">Vērtējumu un apskatu tendenču skatīšana</span><span class="sxs-lookup"><span data-stu-id="76e83-159">View ratings and reviews trends</span></span>

<span data-ttu-id="76e83-160">Moderatori var lejupielādēt Power BI veidni, lai varētu skatīt tendences informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="76e83-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="76e83-161">Lai skatītu vērtējumu un apskatu tendences, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="76e83-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="76e83-162">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="76e83-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="76e83-163">Atlasiet **PowerBI veidne**, lai lejupielādētu veidni.</span><span class="sxs-lookup"><span data-stu-id="76e83-163">Select **PowerBI template** to download the template.</span></span>

    ![Power BI veidnes lejupielāde](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="76e83-165">Atveriet lejupielādēto veidni, izmantojot Power BI programmu.</span><span class="sxs-lookup"><span data-stu-id="76e83-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="76e83-166">Aizveriet parādījušos dialoglodziņu **Piekļuve tīmekļa saturam** un pēc tam aizveriet parādījušos "Atsvaidzināt" kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="76e83-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="76e83-167">Dodieties uz **Sākums**, atlasiet **Rediģēt vaicājumus** un pēc tam atlasiet **Datu avota iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="76e83-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="76e83-168">Dialoglodziņā **Datu avota iestatījumi** atlasiet **Mainīt avotu**.</span><span class="sxs-lookup"><span data-stu-id="76e83-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="76e83-169">Laukā **URL** ievadiet ceļu uz apskatu datiem, ko lejupielādējāt iepriekšējā procedūrā (piemēram, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="76e83-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL lauks ar komatu atdalīto vērtību dialoglodziņā](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="76e83-171">Atlasiet **Labi** un pēc tam atlasiet **Piemērot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="76e83-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="76e83-172">Lai datu avotam tiktu piemērotas izmaiņas, būs nepieciešamas vienas līdz divas minūtes.</span><span class="sxs-lookup"><span data-stu-id="76e83-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="76e83-173">Atlasiet **Tendenču loksne**, lai skatītu vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="76e83-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Vērtējumu un apskatu tendences](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="76e83-175">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="76e83-175">Additional resources</span></span>

[<span data-ttu-id="76e83-176">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="76e83-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="76e83-177">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="76e83-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="76e83-178">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="76e83-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="76e83-179">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="76e83-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
