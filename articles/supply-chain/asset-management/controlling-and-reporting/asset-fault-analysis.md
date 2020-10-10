---
title: Līdzekļu defektu analīze
description: Šajā tēmā ir paskaidrota līdzekļu kļūmju analīze programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e911f7ca3b67acd9d5a1b170d8c99135da730847
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889150"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="832d4-103">Līdzekļu defektu analīze</span><span class="sxs-lookup"><span data-stu-id="832d4-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="832d4-104">Programmā Asset Management varat analizēt reģistrētās kļūdas, lai iegūtu pārskatu par kopējo kļūmju skaitu, kas reģistrēts noteiktā laika posmā.</span><span class="sxs-lookup"><span data-stu-id="832d4-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="832d4-105">Kļūdu reģistrācijas var analizēt no dažādiem aspektiem, piemēram, koncentrējoties uz līdzekļiem, līdzekļu veidiem, funkcionālajiem novietojumiem, kļūmju simptomiem vai kļūmju veidiem.</span><span class="sxs-lookup"><span data-stu-id="832d4-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="832d4-106">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes analīze**.</span><span class="sxs-lookup"><span data-stu-id="832d4-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="832d4-107">Dialogā **Līdzekļu kļūmes analīzes aprēķins** varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties līdzekļu kļūmes rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="832d4-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="832d4-108">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas aktīvu kļūmju rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="832d4-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="832d4-109">Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas līdzekļu kļūmju rindas visos funkcionālā novietojuma līmeņos, ar kuriem tās ir saistītas.</span><span class="sxs-lookup"><span data-stu-id="832d4-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="832d4-110">Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus, un kļūmju labojumus kopsavilkuma cilnē **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="832d4-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="832d4-111">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="832d4-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="832d4-112">Cilnē **Līdzekļu kļūmju analīze** noklikšķiniet uz vienas vai vairākām pogām **Grupēt pēc**, lai parādītu detalizētas informācijas līmeni, kādu vēlaties redzēt.</span><span class="sxs-lookup"><span data-stu-id="832d4-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="832d4-113">Aktivizētās pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="832d4-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="832d4-114">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="832d4-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="832d4-115">Noklikšķiniet uz **Atjaunināt aprēķinus**, lai parādītu savas atlases ekrānā.</span><span class="sxs-lookup"><span data-stu-id="832d4-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="832d4-116">Katru reizi, kad aktivizējat vai deaktivizējat pogu **Grupēc pēc**, neaizmirstiet noklikšķināt uz pogas **Atjaunināt aprēķinus**.</span><span class="sxs-lookup"><span data-stu-id="832d4-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="832d4-117">Tas tādēļ, ka tiek apstrādāts liels datu daudzums, atkārtoti pārrēķinot kļūmes iespēju.</span><span class="sxs-lookup"><span data-stu-id="832d4-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="832d4-118">Piemēri</span><span class="sxs-lookup"><span data-stu-id="832d4-118">Examples</span></span>

<span data-ttu-id="832d4-119">Ir daudzi veidi, kā analizēt kļūmju reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="832d4-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="832d4-120">Šajā sadaļā ir sniegti pieci piemēri tam, kā dažādas datu atlases var sniegt dziļāku ieskatu un detalizētāku informāciju, analizējot kļūmju reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="832d4-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="832d4-121">Grupēt pēc simptomiem</span><span class="sxs-lookup"><span data-stu-id="832d4-121">Group by symptoms</span></span>

<span data-ttu-id="832d4-122">Attēluzņēmumā šeit tālāk ir atlasīta tikai poga **Simptoms**.</span><span class="sxs-lookup"><span data-stu-id="832d4-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="832d4-123">Kļūmes var reģistrēt trim kļūmju simptomiem: „Gaisa sūce”, „Izsists drošinātājs”, „Iekārta aizsprostojusies”.</span><span class="sxs-lookup"><span data-stu-id="832d4-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="832d4-124">Slejā **Iespējamība %** visas procentu vērtības kopā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="832d4-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="832d4-125">Iespējamība balstīta uz visu **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="832d4-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![1. attēls](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="832d4-127">Grupēt pēc simptomiem un laika perioda</span><span class="sxs-lookup"><span data-stu-id="832d4-127">Group by symptoms and time period</span></span>

<span data-ttu-id="832d4-128">Šajā ekrānuzņēmumā pievienots **Gads** un **Mēnesis**, lai parādītu, kā var skatīt kļūmju reģistrācijas noteikta laika posmā.</span><span class="sxs-lookup"><span data-stu-id="832d4-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="832d4-129">Kļūmju simptomus tagad rāda kā reģistrācijas gadā/mēnesī.</span><span class="sxs-lookup"><span data-stu-id="832d4-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="832d4-130">Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības katram mēnesim, kopā tās sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="832d4-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="832d4-131">Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="832d4-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="832d4-132">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.</span><span class="sxs-lookup"><span data-stu-id="832d4-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![2. attēls](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="832d4-134">Grupēt pēc vairākiem simptomiem un līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="832d4-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="832d4-135">Līdzekļu un līdzekļu veida kombinācija tiek izmantota, kā pamats šajos trijos ekrānuzņēmumos parādītajiem aprēķiniem, un tiem samazinās detalizācijas līmenis.</span><span class="sxs-lookup"><span data-stu-id="832d4-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="832d4-136">Vispārīgi pogas Darbību rūts grupās **Grupēt pēc datuma**, **Grupēt pēc līdzekļa**, **Grupēt pēc funkcionālā novietojums**, kā arī poga **Kļūme** (Kļūmes ID) satur periodus vai līdzekļu saistības.</span><span class="sxs-lookup"><span data-stu-id="832d4-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="832d4-137">Pogas **Simptoms**, **Joma**, **Veids**, **Iemesls** un **Labojums** ir kategorizācijas, ko izmanto kļūmju pārvaldībā, lai analizētu līdzekļu kļūmes un noteiktu problēmu jomas.</span><span class="sxs-lookup"><span data-stu-id="832d4-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="832d4-138">**Grupēt pēc simptoma, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="832d4-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="832d4-139">Šajā ekrānuzņēmumā pievienots **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.</span><span class="sxs-lookup"><span data-stu-id="832d4-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="832d4-140">Kļūmju simptomi tagad ir sadalīti kombinācijās **Līdzekļi** / **Līdzekļu veids** / **Simptoms**.</span><span class="sxs-lookup"><span data-stu-id="832d4-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="832d4-141">Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="832d4-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="832d4-142">Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="832d4-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="832d4-143">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.</span><span class="sxs-lookup"><span data-stu-id="832d4-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![3. attēls](media/08-controlling-and-reporting.png)

<span data-ttu-id="832d4-145">**Grupēt pēc diviem simptomiem, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="832d4-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="832d4-146">Šajā ekrānuzņēmumā **Simptomam** pievienota **Joma**, **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.</span><span class="sxs-lookup"><span data-stu-id="832d4-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="832d4-147">Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="832d4-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="832d4-148">Iespējamība balstīta uz kombināciju **Simptoms** un **Joma** šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="832d4-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="832d4-149">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes joma, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šai kļūmes jomai.</span><span class="sxs-lookup"><span data-stu-id="832d4-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![4. attēls](media/09-controlling-and-reporting.png)

<span data-ttu-id="832d4-151">**Grupēt pēc trim simptomiem, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="832d4-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="832d4-152">Šajā ekrāuzņēmumā pievienots **Veids**, un šajā piemērā parādīts visdetalizētākais aprēķins,</span><span class="sxs-lookup"><span data-stu-id="832d4-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="832d4-153">Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="832d4-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="832d4-154">Iespējamība balstīta uz kombināciju **Simptoms** un **Joma**, un **Veids** šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="832d4-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="832d4-155">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes veids, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes veidam.</span><span class="sxs-lookup"><span data-stu-id="832d4-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![5. attēls](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="832d4-157">Lai pārskatītu visas kļūmju reģistrācijas, kas izveidotas darbu pasūtījumiem un uzturēšanas pieprasījumiem, klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="832d4-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="832d4-158">Lapā **Līdzekļu kļūmes** atlasiet līdzekļu kļūmes reģistrāciju un izvērsiet rūti **Saistītā informācija**, lai redzētu informāciju par saistīto darba pasūtījumu vai uzturēšanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="832d4-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

