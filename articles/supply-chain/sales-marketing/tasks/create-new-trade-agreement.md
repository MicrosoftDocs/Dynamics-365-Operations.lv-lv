---
title: Jauna pakalpojumu līguma izveide
description: Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 592b3d0265a3be92a5a823c6aabdd40b4e3f0a27
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919945"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="9a5e8-103">Jauna pakalpojumu līguma izveide</span><span class="sxs-lookup"><span data-stu-id="9a5e8-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a5e8-104">Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="9a5e8-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9a5e8-106">Ja jūs izmantojat savus datus pirms sākat veikt šajā ceļvedī aprakstītās darbības, jums ir jāpārliecinās, ka nosaukums Tirdzniecības līgumu žurnāls eksistē un Noklusējuma relācija ir iestatīta uz "Cena (pārdošana)".</span><span class="sxs-lookup"><span data-stu-id="9a5e8-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>

## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="9a5e8-107">Jauna tirdzniecības līgumu žurnāla izveide un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="9a5e8-107">Create and post a new trade agreement journal</span></span>

1. <span data-ttu-id="9a5e8-108">Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Cenas un atlaides > Tirdzniecības līgumu žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="9a5e8-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-109">Click **New**.</span></span>
3. <span data-ttu-id="9a5e8-110">Laukā **Nosaukums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9a5e8-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9a5e8-112">**Darbību rūtī** noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="9a5e8-113">Laukā **Konta kods** atlasiet “Tabula”.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="9a5e8-114">Šajā piemērā tiek atjaunināta cena noteiktam debitoram, kas nozīmē, ka jums ir jāizvēlas Tabula.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="9a5e8-115">Ja veicat preču saraksta cenas atjaunināšanu, jāatlasa “Visi”, lai jaunā cena būtu derīga visiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="9a5e8-116">Ja cenas dažādos debitoru segmentos atšķiras, jāatlasa Grupa.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="9a5e8-117">Lai atlasītu Grupa, ir jāiestata Debitoru cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="9a5e8-118">Laukā **Konta atlase** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9a5e8-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9a5e8-120">Laukā **Krājuma kods** atlasiet “Tabula”.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="9a5e8-121">Ja ievadāt tirdzniecības līgumu, kura tips ir “Cena (pārdošana)”, laukā **Krājuma kods** ir jāatlasa tikai “Tabula”.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="9a5e8-122">Tas ir tāpēc, ka cena ir absolūtā vērtība un nevar būt vienāda visiem produktiem vai produktu grupai.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="9a5e8-123">Laukā **Krājumu saistība** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu pārlūku.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9a5e8-124">Sarakstā atlasiet preci, ko vēlaties ietvert līgumā.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="9a5e8-125">Atzīmējiet, kuru preci atlasījāt.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="9a5e8-126">Laukā **No** ievadiet minimālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="9a5e8-127">Ja debitoram ir jāpasūta minimālais daudzums pirms tas var pretendēt uz jaunu cenu, tad ir jānorāda daudzums šeit.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="9a5e8-128">Ievadiet vērtību laukā **Līdz**, lai norādītu maksimālo daudzumu, kuru pārsniedzot līguma cena vairs nebūs spēkā.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="9a5e8-129">Ja piedāvājat cenas un atlaides, pamatojoties uz vairākiem daudzuma sadalījuma variantiem, norādiet katru daudzuma grupu kā minimālā un maksimālā daudzuma pāri attiecīgi laukos **No** un **Līdz**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="9a5e8-130">Laukā **Summa valūtā** ievadiet cenu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="9a5e8-131">Sadaļā **Detalizēta informācija** laukā **Sākuma datums** ievadiet datumu, no kura šis līgums ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="9a5e8-132">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-132">Click **Save**.</span></span>
16. <span data-ttu-id="9a5e8-133">Noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-133">Click **Validate**.</span></span>
17. <span data-ttu-id="9a5e8-134">Noklikšķiniet uz **Validēt atlasītās rindas.**</span><span class="sxs-lookup"><span data-stu-id="9a5e8-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="9a5e8-135">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-135">Click **OK**.</span></span>
19. <span data-ttu-id="9a5e8-136">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-136">Click **Post**.</span></span>
20. <span data-ttu-id="9a5e8-137">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="9a5e8-138">Ar preci saistīto tirdzniecības līgumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="9a5e8-138">View trade agreements for a product</span></span>

1. <span data-ttu-id="9a5e8-139">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="9a5e8-140">Sarakstā atrodiet un atlasiet preci, kuras cenu tikko atjaunojāt.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="9a5e8-141">**Darbību rūtī** noklikšķiniet uz **Pārdošana**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="9a5e8-142">Noklikšķiniet uz **Skatīt tirdzniecības līgumus**.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="9a5e8-143">Pārskatiet detalizētu informāciju par tikko izveidoto cenu tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-143">Review the details of the price trade agreement you have just created.</span></span>

5. <span data-ttu-id="9a5e8-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a5e8-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9a5e8-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="9a5e8-146">Tehniskais dokuments</span><span class="sxs-lookup"><span data-stu-id="9a5e8-146">Whitepaper</span></span>

<span data-ttu-id="9a5e8-147">Lai iegūtu plašāku informāciju, lejupielādējiet tālāk norādīto papīru (rakstīts AX 2012 atbalstam, bet joprojām tiek piemērots Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="9a5e8-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>

- [<span data-ttu-id="9a5e8-148">Tirdzniecības līgumi</span><span class="sxs-lookup"><span data-stu-id="9a5e8-148">Trade agreements</span></span>](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="9a5e8-149">Kopienas emuāri</span><span class="sxs-lookup"><span data-stu-id="9a5e8-149">Community blogs</span></span>

- [<span data-ttu-id="9a5e8-150">Pārdošanas cenas programmā Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a5e8-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]