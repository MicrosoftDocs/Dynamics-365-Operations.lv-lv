---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā sniegtas atbildes uz dažiem bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266637"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="27d09-103">Bieži uzdotie jautājumi par finanšu pārskatu veidošanu</span><span class="sxs-lookup"><span data-stu-id="27d09-103">Financial reporting FAQ</span></span>

<span data-ttu-id="27d09-104">Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu.</span><span class="sxs-lookup"><span data-stu-id="27d09-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="27d09-105">Kā var ierobežot piekļuvi pārskatam, izmantojot koka drošību?</span><span class="sxs-lookup"><span data-stu-id="27d09-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="27d09-106">Šajā piemērā parādīts, kā ierobežot piekļuvi pārskatam, izmantojot koka drošību.</span><span class="sxs-lookup"><span data-stu-id="27d09-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="27d09-107">USMF demonstrācijas uzņēmumam ir **bilances pārskats**, kuram nedrīkstētu piekļūt visi finanšu pārskatu lietotāji.</span><span class="sxs-lookup"><span data-stu-id="27d09-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="27d09-108">Varat izmantot koka drošību, lai ierobežotu piekļuvi atsevišķam pārskatam, ļaujot piekļūt tikai konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="27d09-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="27d09-109">Pierakstieties programmā Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="27d09-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="27d09-110">Lai izveidotu jaunu koka definīciju, atlasiet **Fails \> Jauns \> Koka definīcija**.</span><span class="sxs-lookup"><span data-stu-id="27d09-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="27d09-111">Veiciet dubultskārienu vai dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="27d09-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="27d09-112">Atlasiet **Lietotāji un grupas**.</span><span class="sxs-lookup"><span data-stu-id="27d09-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="27d09-113">Atlasiet lietotājus vai grupas, kam vajadzīga piekļuve šim pārskatam.</span><span class="sxs-lookup"><span data-stu-id="27d09-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="27d09-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="27d09-114">Select **Save**.</span></span>
7. <span data-ttu-id="27d09-115">Pārskata definīcijā pievienojiet jaunu koka definīciju.</span><span class="sxs-lookup"><span data-stu-id="27d09-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="27d09-116">Koka definīcijā atlasiet **Iestatījums**.</span><span class="sxs-lookup"><span data-stu-id="27d09-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="27d09-117">Pēc tam sadaļā **Pārskata vienību atlase** atlasiet **Iekļaut visas vienības**.</span><span class="sxs-lookup"><span data-stu-id="27d09-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="27d09-118">Kā noteikt, kuri konti neatbilst manām bilancēm?</span><span class="sxs-lookup"><span data-stu-id="27d09-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="27d09-119">Ja jums ir pārskats, kurā nav atbilstošu bilanču, veiciet tālāk norādītās darbības, lai identificētu visus kontus un novirzes.</span><span class="sxs-lookup"><span data-stu-id="27d09-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="27d09-120">Programmā Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="27d09-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="27d09-121">Izveidojiet jaunu rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="27d09-121">Create a new row definition.</span></span>
2. <span data-ttu-id="27d09-122">Atlasiet **Rediģēt \> Ievietot rindas no dimensijām**.</span><span class="sxs-lookup"><span data-stu-id="27d09-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="27d09-123">Atlasiet **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="27d09-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="27d09-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="27d09-124">Select **OK**.</span></span>
5. <span data-ttu-id="27d09-125">Saglabājiet rindas definīciju.</span><span class="sxs-lookup"><span data-stu-id="27d09-125">Save the row definition.</span></span>
6. <span data-ttu-id="27d09-126">Izveidojiet jaunu kolonnas definīciju.</span><span class="sxs-lookup"><span data-stu-id="27d09-126">Create a new column definition.</span></span>
7. <span data-ttu-id="27d09-127">Izveidojiet jaunu pārskata definīciju.</span><span class="sxs-lookup"><span data-stu-id="27d09-127">Create a new report definition.</span></span>
8. <span data-ttu-id="27d09-128">Atlasiet **Iestatījumi** un noņemiet atzīmi šai opcijai.</span><span class="sxs-lookup"><span data-stu-id="27d09-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="27d09-129">Ģenerējiet pārskatu.</span><span class="sxs-lookup"><span data-stu-id="27d09-129">Generate the report.</span></span> 
10. <span data-ttu-id="27d09-130">Eksportējiet pārskatu uz Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27d09-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="27d09-131">Programmā Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="27d09-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="27d09-132">Dodieties uz **Virsgrāmata \> Pieprasījumi un pārskati \> Apgrozījuma bilance**.</span><span class="sxs-lookup"><span data-stu-id="27d09-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="27d09-133">Iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="27d09-133">Set the following fields:</span></span>

    - <span data-ttu-id="27d09-134">**Sākuma datums** — ievadiet finanšu gada sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="27d09-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="27d09-135">**Beigu datums** — ievadiet datumu, kuram ģenerējat pārskatu.</span><span class="sxs-lookup"><span data-stu-id="27d09-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="27d09-136">**Finanšu dimensija** — iestatiet šo lauku kā **Galvenā konta kopa**.</span><span class="sxs-lookup"><span data-stu-id="27d09-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="27d09-137">Atlasiet **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="27d09-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="27d09-138">Eksportējiet pārskatu uz programmu Excel.</span><span class="sxs-lookup"><span data-stu-id="27d09-138">Export the report to Excel.</span></span>

<span data-ttu-id="27d09-139">Tagad jābūt iespējai no Financial Reporter Excel pārskata kopēt datus uz pārskatu **Apgrozījuma bilance**, lai varētu salīdzināt kolonnas **Beigu bilance**.</span><span class="sxs-lookup"><span data-stu-id="27d09-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="27d09-140">Kad rīkā Report Designer izveidoju pārskatu vai ģenerēju finanšu pārskatu, saņemu šādu ziņojumu: “Operāciju neizdevās pabeigt datu nodrošinātāja struktūras problēmas dēļ.”</span><span class="sxs-lookup"><span data-stu-id="27d09-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="27d09-141">Kā reaģēt?</span><span class="sxs-lookup"><span data-stu-id="27d09-141">How should I respond?</span></span>

<span data-ttu-id="27d09-142">Ziņojums norāda, ka radās problēma, sistēmai mēģinot izgūt finanšu metadatus no data mart laikā, kad izmantojāt rīku Financial Reporting.</span><span class="sxs-lookup"><span data-stu-id="27d09-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="27d09-143">Uz šo problēmu var reaģēt divos tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="27d09-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="27d09-144">Pārskatiet datu integrācijas statusu, rīkā Report Designer dodoties uz **Rīki \> Integrācijas statuss**.</span><span class="sxs-lookup"><span data-stu-id="27d09-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="27d09-145">Ja integrācija ir nepilnīga, uzgaidiet, līdz tā tiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="27d09-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="27d09-146">Pēc tam vēlreiz mēģiniet veikt darbību, ko veicāt, kad saņēmāt ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="27d09-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="27d09-147">Sazinieties ar atbalsta dienestu, lai identificētu un novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="27d09-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="27d09-148">Iespējams, sistēmā ir nekonsekventi dati.</span><span class="sxs-lookup"><span data-stu-id="27d09-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="27d09-149">Atbalsta tehniskie darbinieki var palīdzēt identificēt šo problēmu serverī un atrast konkrētos datus, kurus var būt nepieciešams atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="27d09-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
