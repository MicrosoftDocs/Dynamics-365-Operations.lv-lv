---
title: Ārvalstu valūtas pārvērtēšana bankas kontiem
description: Šajā tēmā ir sniegta informācija par ārvalstu valūtas pārvērtēšanu bankas kontiem.
author: panolte
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86d62d5d281eaf243b61d2d86591257f758d5d3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264981"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a><span data-ttu-id="502ca-103">Ārvalstu valūtas pārvērtēšana bankas kontiem</span><span class="sxs-lookup"><span data-stu-id="502ca-103">Foreign currency revaluation for bank accounts</span></span>

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a><span data-ttu-id="502ca-104">Ārvalstu valūtas summu pārvērtēšana bankas kontu transakcijām</span><span class="sxs-lookup"><span data-stu-id="502ca-104">Revalue foreign currency amounts for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="502ca-105">Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Polijā.</span><span class="sxs-lookup"><span data-stu-id="502ca-105">This section applies only to legal entities that have a primary address in Poland.</span></span>

<span data-ttu-id="502ca-106">Varat pārvērtēt ārvalstu valūtas summas bankas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="502ca-106">You can revalue foreign currency amounts for bank transactions.</span></span> <span data-ttu-id="502ca-107">Pēc tam varat izveidot pārskatu, lai skatītu bankas transakcijas, kurām ir ārvalstu valūtas pārvērtēšanas korekcijas.</span><span class="sxs-lookup"><span data-stu-id="502ca-107">You can then create a report to view the bank transactions that have adjustments for foreign currency revaluations.</span></span>

1. <span data-ttu-id="502ca-108">Atlasiet vienumu **Skaidras naudas un bankas pārvaldība** &gt; **Periodiskie uzdevumi** &gt; **Banka — Valūtas maiņas korekcija (FIFO un LIFO)**.</span><span class="sxs-lookup"><span data-stu-id="502ca-108">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Bank - Exchange adjustment (FIFO/LIFO)**.</span></span>
2. <span data-ttu-id="502ca-109">Laukā **Datumā** ievadiet pārvērtēšanas beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="502ca-109">In the **On date** field, enter an end date for the revaluation.</span></span> <span data-ttu-id="502ca-110">Aprēķinos tiek iekļautas tikai transakcijas, kuru datums ir pirms norādītā datuma.</span><span class="sxs-lookup"><span data-stu-id="502ca-110">The calculation includes only transactions that have a date that is before the specified date.</span></span>
3. <span data-ttu-id="502ca-111">Atlasiet **Iekļaujamie ieraksti** &gt; **Filtrēt** &gt; **Pievienot**, lai pievienotu bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="502ca-111">Select **Records to include** &gt; **Filter** &gt; **Add** to add a bank account.</span></span> <span data-ttu-id="502ca-112">Ja nenorādīsit bankas kontu, tiek pārvērtētas visas bankas kontu summas.</span><span class="sxs-lookup"><span data-stu-id="502ca-112">If you don't specify a bank account, amounts are revalued for all bank accounts.</span></span>
4. <span data-ttu-id="502ca-113">Atlasiet **Labi**, lai aizvērtu vaicājuma lapu.</span><span class="sxs-lookup"><span data-stu-id="502ca-113">Select **OK** to close the query page.</span></span>
5. <span data-ttu-id="502ca-114">Lapā **Ārvalstu valūtas pārvērtēšana** atzīmējiet izvēles rūtiņu **Pārrēķins**, lai pārvērtētu ārvalstu valūtas summas par visiem atvērtajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="502ca-114">On the **Foreign currency revaluation** page, select the **Recalculation** check box to revalue foreign currency amounts for all open periods.</span></span>

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a><span data-ttu-id="502ca-115">Pārskata izveide, lai skatītu bankas transakcijas, kurām ir ārvalstu valūtas pārvērtēšanas korekcijas</span><span class="sxs-lookup"><span data-stu-id="502ca-115">Create a report to view bank transactions that have adjustments for foreign currency revaluations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="502ca-116">Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Polijā.</span><span class="sxs-lookup"><span data-stu-id="502ca-116">This section applies only to legal entities that have a primary address in Poland.</span></span>

1. <span data-ttu-id="502ca-117">Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Pieprasījumi un pārskati** &gt; **Pārskats “Banka — Valūtas maiņas korekcija”**.</span><span class="sxs-lookup"><span data-stu-id="502ca-117">Select **Cash and bank management** &gt; **Inquiries and reports** &gt; **Bank - Exchange adjustment report**.</span></span>
2. <span data-ttu-id="502ca-118">Atlasiet vienumu **Iekļaujamie ieraksti** &gt; **Filtrēt**, lai atrastu vienu vai vairākus bankas kontus, par kuriem skatīt informāciju.</span><span class="sxs-lookup"><span data-stu-id="502ca-118">Select **Records to include** &gt; **Filter** to find one or more bank accounts to view information for.</span></span>
3. <span data-ttu-id="502ca-119">Neobligāti: laukā **Bankas konts** atlasiet bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="502ca-119">Optional: In the **Bank account** field, select a bank account.</span></span> <span data-ttu-id="502ca-120">Atstājot šo lauku tukšu, pārskatā tiek iekļauta bankas transakciju informācija par visiem bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="502ca-120">If you leave this field blank, the report includes bank transaction details for all bank accounts.</span></span>
4. <span data-ttu-id="502ca-121">Atlasiet **Labi**, lai izveidotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="502ca-121">Select **OK** to generate the report.</span></span> 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a><span data-ttu-id="502ca-122">Valūtas maiņas kursa korekciju aprēķins bankas konta transakcijām</span><span class="sxs-lookup"><span data-stu-id="502ca-122">Calculate exchange rate adjustments for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="502ca-123">Šī sadaļa attiecas tikai uz juridiskajām personām, kuru primārā adrese ir Čehijas Republikā, Igaunijā, Lietuvā vai Latvijā.</span><span class="sxs-lookup"><span data-stu-id="502ca-123">This section applies only to legal entities that have a primary address in the Czech Republic, Estonia, Lithuania, or Latvia.</span></span>

<span data-ttu-id="502ca-124">Ir jāpārvērtē un jākoriģē banku konti, ja pastāv maiņas kursu atšķirība starp uzskaites valūtu un pārskata valūtu.</span><span class="sxs-lookup"><span data-stu-id="502ca-124">You must revalue and adjust bank accounts if there is a difference in the exchange rate between the accounting currency and the reporting currency.</span></span> <span data-ttu-id="502ca-125">Šis uzdevums palīdz jums aprēķināt pareizo bilanci gan uzskaites valūtā, gan pārskata valūtā bankas kontos.</span><span class="sxs-lookup"><span data-stu-id="502ca-125">This task helps you calculate the correct balance in both the accounting currency and the reporting currency for the bank accounts.</span></span>

1. <span data-ttu-id="502ca-126">Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Iestatīšana** &gt; **Skaidras naudas un bankas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="502ca-126">Select **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="502ca-127">Cilnes **Numuru sērijas** laukā **Atsauce** atlasiet numuru sēriju atsaucei **Banka — Valūtas maiņas korekcija**.</span><span class="sxs-lookup"><span data-stu-id="502ca-127">On the **Number sequences** tab, in the **Reference** field, select a number sequence for the **Bank - Exchange adjustment** reference.</span></span>
3. <span data-ttu-id="502ca-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="502ca-128">Close the page.</span></span>
4. <span data-ttu-id="502ca-129">Atlasiet **Virsgrāmata** &gt; **Iestatīšana** &gt; **Valūta** &gt; **Valūtas maiņas kursi**.</span><span class="sxs-lookup"><span data-stu-id="502ca-129">Select **General ledger** &gt; **Setup** &gt; **Currency** &gt; **Currency exchange rates**.</span></span> <span data-ttu-id="502ca-130">Lapā **Valūtas maiņas kursi** var definēt maiņas kursu starp divām valūtām vai valūtu pāri.</span><span class="sxs-lookup"><span data-stu-id="502ca-130">On the **Currency exchange rates** page, you can define the exchange rate between two currencies or a currency pair.</span></span>
5. <span data-ttu-id="502ca-131">Kad esat beidzis, aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="502ca-131">When you've finished, close the page.</span></span>
6. <span data-ttu-id="502ca-132">Atlasiet **Virsgrāmata** &gt; **Iestatīšana** &gt; **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="502ca-132">Select **General ledger** &gt; **Setup** &gt; **Ledger**.</span></span> <span data-ttu-id="502ca-133">Laukos **Nerealizētā peļņa** un **Nerealizētie zaudējumi** atlasiet galveno kontu, kurā tiek grāmatoti maiņas kursi.</span><span class="sxs-lookup"><span data-stu-id="502ca-133">In the **Unrealized gain** and **Unrealized loss** fields, select the main account that the exchange rates are posted for.</span></span>
7. <span data-ttu-id="502ca-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="502ca-134">Close the page.</span></span>
8. <span data-ttu-id="502ca-135">Atlasiet **Skaidras naudas un bankas pārvaldība** &gt; **Periodiskie uzdevumi** &gt; **Ārvalstu valūtas pārvērtēšana**.</span><span class="sxs-lookup"><span data-stu-id="502ca-135">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Foreign currency revaluation**.</span></span>
9. <span data-ttu-id="502ca-136">Laukā **Datumā** atlasiet pārvērtēšanas datumu vai korekcijas datumu.</span><span class="sxs-lookup"><span data-stu-id="502ca-136">In the **On date** field, select the revaluation date or adjustment date.</span></span>
10. <span data-ttu-id="502ca-137">Laukā **No valūtas** atlasiet pašreizējās valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="502ca-137">In the **From currency** field, select the current currency code.</span></span> <span data-ttu-id="502ca-138">Laukā **Uz valūtu** atlasiet valūtu, kura jākoriģē.</span><span class="sxs-lookup"><span data-stu-id="502ca-138">In the **To currency** field, select the currency that the adjustment should be made to.</span></span>
11. <span data-ttu-id="502ca-139">Atlasiet **Iekļaujamie ieraksti** &gt; **Filtrēt**, lai atrastu bankas kontu, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="502ca-139">Select **Records to include** &gt; **Filter** to find the bank account, and then select **OK**.</span></span>
12. <span data-ttu-id="502ca-140">Lapā **Ārvalstu valūtas pārvērtēšana** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="502ca-140">On the **Foreign currency revaluation** page, select **OK**.</span></span> <span data-ttu-id="502ca-141">Bankas kontu darījumu korekcija atlasītajā datumā tiek aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="502ca-141">The adjustment for the bank account transactions on the selected date is calculated.</span></span>

> [!NOTE]
> <span data-ttu-id="502ca-142">Virsgrāmatā var skatīt divas atsevišķas transakcijas: uzskaites valūtai un pārskata valūtai.</span><span class="sxs-lookup"><span data-stu-id="502ca-142">In the general ledger, you can view two separate transactions: one for the accounting currency and one for the reporting currency.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]