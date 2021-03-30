---
title: Vērtējumu un atsauksmju pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārvaldīt vērtējumus un atsauksmes Microsoft Dynamics 365 Commerce vietņu veidotājā.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8ab85605bce11934f71237ad1ef7cd24804319b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250808"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="f189b-103">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="f189b-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f189b-104">Šajā tēmā ir paskaidrots, kā pārvaldīt vērtējumus un atsauksmes Microsoft Dynamics 365 Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="f189b-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="f189b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f189b-105">Overview</span></span>

<span data-ttu-id="f189b-106">Dynamics 365 Commerce izmanto Microsoft Azure Cognitive Service, lai automātiski moderētu apskata tekstu, rediģējot nepiedienīgos vārdus.</span><span class="sxs-lookup"><span data-stu-id="f189b-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="f189b-107">Turklāt moderatori var izmantot Dynamics 365 Commerce vietņu veidotāju, lai ieviestu šādus manuālus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="f189b-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="f189b-108">Moderēt apskatus, atbildot uz tiem vai noņemot tos.</span><span class="sxs-lookup"><span data-stu-id="f189b-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="f189b-109">Dzēst klienta apskatu pēc klienta pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="f189b-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="f189b-110">Importēt visu preču vērtējumu un apskatu datus lielā apjomā Microsoft Power BI veidnē, lai varētu analizēt vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="f189b-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="f189b-111">Apskata lasīšana</span><span class="sxs-lookup"><span data-stu-id="f189b-111">Read a review</span></span> 

<span data-ttu-id="f189b-112">Lai lasītu atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f189b-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-113">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="f189b-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f189b-114">Lai filtrētu apskatus, kas tiek parādīti pēc preces ID, preces nosaukuma vai apskata teksta, izmantojiet meklēšanas lauku lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="f189b-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="f189b-115">Papildu filtri ļauj ierobežot apskatus pēc perioda, vērtējuma, kanāla vai svarīguma statusa (noņemts, atbildēts vai ziņots).</span><span class="sxs-lookup"><span data-stu-id="f189b-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderēšanas sākumlapa](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="f189b-117">Atbildēšana uz apskatu</span><span class="sxs-lookup"><span data-stu-id="f189b-117">Respond to a review</span></span> 

<span data-ttu-id="f189b-118">Dažkārt klienti, kuri iegādājušies preci, izsaka savu apmierinātību vai neapmierinātību vai nesaprot, kā izmantot preci.</span><span class="sxs-lookup"><span data-stu-id="f189b-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="f189b-119">Kā moderators varat ievietot atbildi uz apskatu.</span><span class="sxs-lookup"><span data-stu-id="f189b-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="f189b-120">Šī atbilde parādīsies vietnē kopā ar apskatu.</span><span class="sxs-lookup"><span data-stu-id="f189b-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="f189b-121">Lai atbildētu uz atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f189b-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-122">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="f189b-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f189b-123">Atrodiet un atlasiet apskatu, kam nepieciešama atbilde.</span><span class="sxs-lookup"><span data-stu-id="f189b-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="f189b-124">Rekvizītu rūts labajā pusē atlasiet **Pievienot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="f189b-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="f189b-125">Ievadiet atbildes tekstu un parādāmo atbildētāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="f189b-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="f189b-126">Noklusējuma atbildētāja vārds ir **Moderators**.</span><span class="sxs-lookup"><span data-stu-id="f189b-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="f189b-127">Pēc pabeigšanas atlasiet **Ievietot atbildi**.</span><span class="sxs-lookup"><span data-stu-id="f189b-127">When you've finished, select **Post response**.</span></span>

![Atbildēšana uz apskatu](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="f189b-129">Apskata noņemšana</span><span class="sxs-lookup"><span data-stu-id="f189b-129">Take down a review</span></span> 

<span data-ttu-id="f189b-130">Dažreiz moderatoriem ir biznesa pamatojums, lai noņemtu klienta apskatus.</span><span class="sxs-lookup"><span data-stu-id="f189b-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="f189b-131">Lai noņemtu atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f189b-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-132">Dodieties uz **Sākums \> Apskati \> Moderēšana**.</span><span class="sxs-lookup"><span data-stu-id="f189b-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="f189b-133">Atrodiet un atlasiet apskatu, kas jānoņem.</span><span class="sxs-lookup"><span data-stu-id="f189b-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="f189b-134">Labajā pusē rekvizītu rūtī atlasiet noņemšanas iemeslu sadaļā **Noņemt atsauksmi** un tad atlasiet **Noņemt**.</span><span class="sxs-lookup"><span data-stu-id="f189b-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="f189b-135">Klienta apskata dzēšana pēc klienta pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="f189b-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="f189b-136">Dažkārt klienti vēlas, lai viņu vērtējumu un apskatu dati tiktu neatgriezeniski dzēsti no e-tirdzniecības vietnes.</span><span class="sxs-lookup"><span data-stu-id="f189b-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="f189b-137">Moderators, kas saņem noņemšanas pieprasījumu no klienta, var noņemt klienta datus, izmantojot apstatu dzēšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="f189b-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="f189b-138">Lai atrastu un dzēstu klienta datus, moderatoram ir nepieciešama e-pasta adrese, ko klients izmantojis, lai pierakstītos un sniegtu apskatus.</span><span class="sxs-lookup"><span data-stu-id="f189b-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="f189b-139">Lai atrastu un dzēstu klienta datus Commerce vietņu veidotājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="f189b-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-140">Dodieties uz **Sākums \> Apskati \> Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="f189b-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="f189b-141">Lodziņā **Meklēt lietotājus pēc e-pasta adreses** ievadiet klienta e-pasta adresi un pēc tam atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="f189b-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="f189b-142">Ja klients veicis kādas apskatīšanas aktivitātes (piemēram, iesniedzis apskatus, balsojis par cita klienta apskatu noderīgumu vai komentējis cita klienta apskatu), tiek parādīti rezultāti.</span><span class="sxs-lookup"><span data-stu-id="f189b-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="f189b-143">Katram elementam ir poga **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="f189b-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="f189b-144">Katram elementam, kas jāizdzēš, atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="f189b-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="f189b-145">Kad tiek pieprasīts apstiprinājums, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f189b-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Klienta datu dzēšana](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="f189b-147">Var paiet līdz septiņām dienām, lai dati tiktu pilnībā noņemti no sistēmas.</span><span class="sxs-lookup"><span data-stu-id="f189b-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="f189b-148">Moderatoriem jāpaziņo klientiem par šo kavēšanos.</span><span class="sxs-lookup"><span data-stu-id="f189b-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="f189b-149">Ja klienti ir mainījuši savu vārdu konta iestatījumos, meklēšanas rezultātos var parādīties vairāki elementi.</span><span class="sxs-lookup"><span data-stu-id="f189b-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="f189b-150">Šādā gadījumā, lai pilnībā dzēstu klienta datus, moderatoram katram elementam jāatlasa **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="f189b-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="f189b-151">Vērtējumu un apskatu datu lejupielāde</span><span class="sxs-lookup"><span data-stu-id="f189b-151">Download ratings and reviews data</span></span>

<span data-ttu-id="f189b-152">Commerce vietņu veidotājs ļauj moderatoriem importēt vērtējumu un atsauksmju datus lielapjomā, lai varētu analizēt tendences.</span><span class="sxs-lookup"><span data-stu-id="f189b-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="f189b-153">Ir pieejama Power BI veidne, kas ietver pamata rādītājus.</span><span class="sxs-lookup"><span data-stu-id="f189b-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="f189b-154">Moderatori var izmantot šo veidni, lai savienotu lielā apjomā importētos datus un skatītu informācijas paneli.</span><span class="sxs-lookup"><span data-stu-id="f189b-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="f189b-155">Viņiem nav jāizveido pielāgots informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="f189b-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="f189b-156">Moderatori var arī pielāgot Power BI veidni, lai tā atbilstu viņu īpašajām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="f189b-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="f189b-157">Lai lejupielādētu vērtējumu un atsauksmju datus Commerce vietņu veidotājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="f189b-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-158">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="f189b-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="f189b-159">Atlasiet **Lejupielādēt atsauksmju datus**, lai lejupielādētu vērtējumu un atsauksmju datus lielapjomā ar komatiem atdalītu vērtību (CSV) formātā.</span><span class="sxs-lookup"><span data-stu-id="f189b-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="f189b-160">Vērtējumu un apskatu tendenču skatīšana</span><span class="sxs-lookup"><span data-stu-id="f189b-160">View ratings and reviews trends</span></span>

<span data-ttu-id="f189b-161">Moderatori var lejupielādēt Power BI veidni, lai varētu skatīt tendences informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="f189b-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="f189b-162">Lai skatītu vērtējumu un atsauksmju tendences Commerce vietņu veidotājā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="f189b-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f189b-163">Dodieties uz **Sākums \> Apskati \> Ziņošana**.</span><span class="sxs-lookup"><span data-stu-id="f189b-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="f189b-164">Atlasiet **PowerBI veidne**, lai lejupielādētu veidni.</span><span class="sxs-lookup"><span data-stu-id="f189b-164">Select **PowerBI template** to download the template.</span></span>

    ![Lejupielādējiet Power BI veidni](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="f189b-166">Atveriet lejupielādēto veidni, izmantojot Power BI programmu.</span><span class="sxs-lookup"><span data-stu-id="f189b-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="f189b-167">Aizveriet parādījušos dialoglodziņu **Piekļuve tīmekļa saturam** un pēc tam aizveriet parādījušos "Atsvaidzināt" kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f189b-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="f189b-168">Dodieties uz **Sākums**, atlasiet **Rediģēt vaicājumus** un pēc tam atlasiet **Datu avota iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="f189b-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="f189b-169">Dialoglodziņā **Datu avota iestatījumi** atlasiet **Mainīt avotu**.</span><span class="sxs-lookup"><span data-stu-id="f189b-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="f189b-170">Laukā **URL** ievadiet ceļu uz apskatu datiem, ko lejupielādējāt iepriekšējā procedūrā (piemēram, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="f189b-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL lauks ar komatu atdalīto vērtību dialoglodziņā](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="f189b-172">Atlasiet **Labi** un pēc tam atlasiet **Piemērot izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="f189b-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="f189b-173">Lai datu avotam tiktu piemērotas izmaiņas, būs nepieciešamas vienas līdz divas minūtes.</span><span class="sxs-lookup"><span data-stu-id="f189b-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="f189b-174">Atlasiet **Tendenču loksne**, lai skatītu vērtējumu un apskatu tendences.</span><span class="sxs-lookup"><span data-stu-id="f189b-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Vērtējumu un apskatu tendences](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="f189b-176">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f189b-176">Additional resources</span></span>

[<span data-ttu-id="f189b-177">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="f189b-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f189b-178">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="f189b-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f189b-179">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f189b-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="f189b-180">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f189b-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]