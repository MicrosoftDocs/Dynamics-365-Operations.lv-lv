---
title: TDS iestāžu maksājumu iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt maksājumu nodevas, kas tiek iekasētas par No kopējo ienākumu summas atskaitītā nodokļa (TDS) iestādes maksājumiem.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023433"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="11f8d-103">TDS iestāžu maksājumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="11f8d-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11f8d-104">Šajā tēmā ir paskaidrots, kā iestatīt maksājumu nodevas, kas tiek iekasētas par No kopējo ienākumu summas atskaitītā nodokļa (TDS) iestādes maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="11f8d-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="11f8d-105">Pārejiet uz sadaļu **Kreditori \> Maksājuma iestatījumi \> Komisijas maksa**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="11f8d-106">[![Maksājumu apmaksas lapa](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="11f8d-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="11f8d-107">Atlasiet **Jauns**, lai izveidotu maksājumu apmaksu, un pēc tam ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="11f8d-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="11f8d-108">Laukā **Maksājuma tips** atlasiet maksājuma apmaksas tipu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="11f8d-109">**Neviens**</span><span class="sxs-lookup"><span data-stu-id="11f8d-109">**None**</span></span>
    - <span data-ttu-id="11f8d-110">**Procenti** – procenti tiek aprēķināti par nokavētiem maksājumiem, kas tiek veikti TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="11f8d-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="11f8d-111">**Citi** – Citi maksājumi tiek aprēķināti par kavējumiem, kas tiek veikti TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="11f8d-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="11f8d-112">Atlasot **Procenti** vai **Citi**, lauks **Maksa** automātiski tiek iestatīts **Virsgrāmatā**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="11f8d-113">Ja atlasījāt **Procenti** vai **Citi** laukā **Lauka tips**, laukā **Galvenais konts**, atlasiet Virsgrāmatas kontu, kurā grāmatot procentus vai citas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="11f8d-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="11f8d-114">Ievadiet pārējo nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="11f8d-114">Enter the other required details.</span></span>
6. <span data-ttu-id="11f8d-115">Darbību rūtī atlasiet **Komisijas maksu iestatījumi**, lai atvērtu lapu **Komisijas maksu iestatījumi**, kur var iestatīt maksājumu komisijas dažādām banku kombinācijām, maksāšanas metodēm, maksājumu specifikācijām, valūtām un datumu intervāliem.</span><span class="sxs-lookup"><span data-stu-id="11f8d-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="11f8d-116">[![Maksājumu apmaksu iestatīšanas lapa](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="11f8d-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="11f8d-117">Cilnē **Pārskats** laukā **Grupēšana** norādiet, kurām bankām jūs iestatāt maksājuma komisiju:</span><span class="sxs-lookup"><span data-stu-id="11f8d-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="11f8d-118">**Tabula** – komisijas maksa ir derīga noteiktam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="11f8d-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="11f8d-119">**Grupa** – komisijas maksa ir derīga noteiktai bankas grupai.</span><span class="sxs-lookup"><span data-stu-id="11f8d-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="11f8d-120">**Visi** - komisijas maksājums ir derīgs visiem bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="11f8d-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="11f8d-121">Ja atlasāt **Tabula** vai **Grupa** laukā **Grupēšana**, laukā **Bankas saistība**, atlasiet noteiktu bankas kontu vai bankas grupu, kam iestatāt komisijas maksu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="11f8d-122">Laukā **Maksājuma metode** atlasiet metodi, kas tiks izmantota maksājumu komisijas apmaksai.</span><span class="sxs-lookup"><span data-stu-id="11f8d-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="11f8d-123">Laukā **Maksājuma specifikācija** atlasiet vai ievadiet maksājuma specifikācijas kodu, kas tika izveidots **Maksājumu specifikācijas** lapā.</span><span class="sxs-lookup"><span data-stu-id="11f8d-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="11f8d-124">Maksājuma specifikācija tiek izmantota maksāšanas metodēm, kas attiecināmas uz elektronisko līdzekļu pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="11f8d-125">Laukā **Maksājuma valūta** atlasiet valūtu, kas aktivizē maksu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="11f8d-126">Tikai darījumi, kas izmanto atlasīto valūtu, var aktivizēt papildu maksu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="11f8d-127">Ja šo lauku atstājat tukšu, visas valūtas aktivizē papildu maksu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="11f8d-128">Laukā **Procenti/summa** atlasiet aprēķina metodi.</span><span class="sxs-lookup"><span data-stu-id="11f8d-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="11f8d-129">Opcijas ir **Summa**, **Procenti** un **Intervāls**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="11f8d-130">Laukā **Papildmaksu summa** norādiet maksājuma summu kā maksājuma procentus vai kā summu vienam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="11f8d-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="11f8d-131">Laukā **Maksas valūta** norādiet maksas valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="11f8d-132">Atlasiet cilni **Vispārīgi**, lai skatītu vai modificētu atlasītā bankas konta detalizēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="11f8d-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="11f8d-133">[![Cilne Vispārīgi](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="11f8d-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="11f8d-134">Laukā **Minimālais** ievadiet minimālo darījumu summu, kas aktivizē komisiju.</span><span class="sxs-lookup"><span data-stu-id="11f8d-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="11f8d-135">Laukā **Maksimālais** ievadiet maksimālo darījuma summu, kas aktivizē komisiju.</span><span class="sxs-lookup"><span data-stu-id="11f8d-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="11f8d-136">Laukos **sākuma datums** un **Beigu datums** definējiet datumu diapazonu maksu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="11f8d-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="11f8d-137">Laukā **Minimāla papildmaksa** norādiet papildmaksu summu kā maksājuma procentus vai kā summu vienam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="11f8d-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="11f8d-138">Laukā **PVN grupa** atlasiet PVN grupu, ko izmantot, lai aprēķinātu PVN maksājuma summai.</span><span class="sxs-lookup"><span data-stu-id="11f8d-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="11f8d-139">Laukā **Krājuma PVN grupa** atlasiet krājuma PVN grupu, ko izmantot, lai aprēķinātu krājuma PVN maksājuma summai.</span><span class="sxs-lookup"><span data-stu-id="11f8d-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="11f8d-140">Atlasiet cilni **Intervāls**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="11f8d-141">[![Cilne Intervāls](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="11f8d-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="11f8d-142">Laukā **Dienas** ievadiet dienu skaitu starp maksājuma grāmatošanas datumu (atlaides datumu) un parādzīmes izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="11f8d-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="11f8d-143">Laukā **Procenti/summa** atlasiet, vai specifikācija ir procenti vai iestatītā summa.</span><span class="sxs-lookup"><span data-stu-id="11f8d-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="11f8d-144">Laukā **Papildmaksas summa** ievadiet papildmaksu summu kā maksājuma procentus vai kā summu vienam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="11f8d-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="11f8d-145">Aizveriet lapu **Papildmaksu iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="11f8d-146">Aizveriet lapu **Papildmaksas**.</span><span class="sxs-lookup"><span data-stu-id="11f8d-146">Close the **Payment fee** page.</span></span>
