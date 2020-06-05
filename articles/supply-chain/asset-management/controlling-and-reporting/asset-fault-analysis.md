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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32cd8fb55cd9245a9a7c426a7c956bb40c3fdb0e
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383554"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="8c326-103">Līdzekļu defektu analīze</span><span class="sxs-lookup"><span data-stu-id="8c326-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8c326-104">Programmā Asset Management varat analizēt reģistrētās kļūdas, lai iegūtu pārskatu par kopējo kļūmju skaitu, kas reģistrēts noteiktā laika posmā.</span><span class="sxs-lookup"><span data-stu-id="8c326-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="8c326-105">Kļūdu reģistrācijas var analizēt no dažādiem aspektiem, piemēram, koncentrējoties uz līdzekļiem, līdzekļu veidiem, funkcionālajiem novietojumiem, kļūmju simptomiem vai kļūmju veidiem.</span><span class="sxs-lookup"><span data-stu-id="8c326-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="8c326-106">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes analīze**.</span><span class="sxs-lookup"><span data-stu-id="8c326-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="8c326-107">Dialogā **Līdzekļu kļūmes analīzes aprēķins** varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties līdzekļu kļūmes rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="8c326-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="8c326-108">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas aktīvu kļūmju rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="8c326-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="8c326-109">Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas līdzekļu kļūmju rindas visos funkcionālā novietojuma līmeņos, ar kuriem tās ir saistītas.</span><span class="sxs-lookup"><span data-stu-id="8c326-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="8c326-110">Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus, un kļūmju labojumus kopsavilkuma cilnē **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="8c326-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="8c326-111">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="8c326-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="8c326-112">Cilnē **Līdzekļu kļūmju analīze** noklikšķiniet uz vienas vai vairākām pogām **Grupēt pēc**, lai parādītu detalizētas informācijas līmeni, kādu vēlaties redzēt.</span><span class="sxs-lookup"><span data-stu-id="8c326-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="8c326-113">Aktivizētās pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="8c326-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="8c326-114">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="8c326-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="8c326-115">Noklikšķiniet uz **Atjaunināt aprēķinus**, lai parādītu savas atlases ekrānā.</span><span class="sxs-lookup"><span data-stu-id="8c326-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="8c326-116">Katru reizi, kad aktivizējat vai deaktivizējat pogu **Grupēc pēc**, neaizmirstiet noklikšķināt uz pogas **Atjaunināt aprēķinus**.</span><span class="sxs-lookup"><span data-stu-id="8c326-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="8c326-117">Tas tādēļ, ka tiek apstrādāts liels datu daudzums, atkārtoti pārrēķinot kļūmes iespēju.</span><span class="sxs-lookup"><span data-stu-id="8c326-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="8c326-118">Piemēri</span><span class="sxs-lookup"><span data-stu-id="8c326-118">Examples</span></span>

<span data-ttu-id="8c326-119">Ir daudzi veidi, kā analizēt kļūmju reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="8c326-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="8c326-120">Šajā sadaļā ir sniegti pieci piemēri tam, kā dažādas datu atlases var sniegt dziļāku ieskatu un detalizētāku informāciju, analizējot kļūmju reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="8c326-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="8c326-121">Grupēt pēc simptomiem</span><span class="sxs-lookup"><span data-stu-id="8c326-121">Group by symptoms</span></span>

<span data-ttu-id="8c326-122">Attēluzņēmumā šeit tālāk ir atlasīta tikai poga **Simptoms**.</span><span class="sxs-lookup"><span data-stu-id="8c326-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="8c326-123">Kļūmes var reģistrēt trim kļūmju simptomiem: „Gaisa sūce”, „Izsists drošinātājs”, „Iekārta aizsprostojusies”.</span><span class="sxs-lookup"><span data-stu-id="8c326-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="8c326-124">Slejā **Iespējamība %** visas procentu vērtības kopā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="8c326-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="8c326-125">Iespējamība balstīta uz visu **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="8c326-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![1. attēls](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="8c326-127">Grupēt pēc simptomiem un laika perioda</span><span class="sxs-lookup"><span data-stu-id="8c326-127">Group by symptoms and time period</span></span>

<span data-ttu-id="8c326-128">Šajā ekrānuzņēmumā pievienots **Gads** un **Mēnesis**, lai parādītu, kā var skatīt kļūmju reģistrācijas noteikta laika posmā.</span><span class="sxs-lookup"><span data-stu-id="8c326-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="8c326-129">Kļūmju simptomus tagad rāda kā reģistrācijas gadā/mēnesī.</span><span class="sxs-lookup"><span data-stu-id="8c326-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="8c326-130">Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības katram mēnesim, kopā tās sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="8c326-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="8c326-131">Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="8c326-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="8c326-132">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.</span><span class="sxs-lookup"><span data-stu-id="8c326-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![2. attēls](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="8c326-134">Grupēt pēc vairākiem simptomiem un līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="8c326-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="8c326-135">Līdzekļu un līdzekļu veida kombinācija tiek izmantota, kā pamats šajos trijos ekrānuzņēmumos parādītajiem aprēķiniem, un tiem samazinās detalizācijas līmenis.</span><span class="sxs-lookup"><span data-stu-id="8c326-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="8c326-136">Vispārīgi pogas Darbību rūts grupās **Grupēt pēc datuma**, **Grupēt pēc līdzekļa**, **Grupēt pēc funkcionālā novietojums**, kā arī poga **Kļūme** (Kļūmes ID) satur periodus vai līdzekļu saistības.</span><span class="sxs-lookup"><span data-stu-id="8c326-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="8c326-137">Pogas **Simptoms**, **Joma**, **Veids**, **Iemesls** un **Labojums** ir kategorizācijas, ko izmanto kļūmju pārvaldībā, lai analizētu līdzekļu kļūmes un noteiktu problēmu jomas.</span><span class="sxs-lookup"><span data-stu-id="8c326-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="8c326-138">**Grupēt pēc simptoma, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="8c326-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="8c326-139">Šajā ekrānuzņēmumā pievienots **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.</span><span class="sxs-lookup"><span data-stu-id="8c326-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="8c326-140">Kļūmju simptomi tagad ir sadalīti kombinācijās **Līdzekļi** / **Līdzekļu veids** / **Simptoms**.</span><span class="sxs-lookup"><span data-stu-id="8c326-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="8c326-141">Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="8c326-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="8c326-142">Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="8c326-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="8c326-143">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.</span><span class="sxs-lookup"><span data-stu-id="8c326-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![3. attēls](media/08-controlling-and-reporting.png)

<span data-ttu-id="8c326-145">**Grupēt pēc diviem simptomiem, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="8c326-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="8c326-146">Šajā ekrānuzņēmumā **Simptomam**pievienota **Joma**, **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.</span><span class="sxs-lookup"><span data-stu-id="8c326-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="8c326-147">Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="8c326-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="8c326-148">Iespējamība balstīta uz kombināciju **Simptoms** un **Joma** šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="8c326-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="8c326-149">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes joma, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šai kļūmes jomai.</span><span class="sxs-lookup"><span data-stu-id="8c326-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![4. attēls](media/09-controlling-and-reporting.png)

<span data-ttu-id="8c326-151">**Grupēt pēc trim simptomiem, līdzekļa un līdzekļa veida**</span><span class="sxs-lookup"><span data-stu-id="8c326-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="8c326-152">Šajā ekrāuzņēmumā pievienots **Veids**, un šajā piemērā parādīts visdetalizētākais aprēķins,</span><span class="sxs-lookup"><span data-stu-id="8c326-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="8c326-153">Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %.</span><span class="sxs-lookup"><span data-stu-id="8c326-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="8c326-154">Iespējamība balstīta uz kombināciju **Simptoms** un **Joma**, un **Veids** šai kļūmju analīzei.</span><span class="sxs-lookup"><span data-stu-id="8c326-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="8c326-155">Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes veids, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes veidam.</span><span class="sxs-lookup"><span data-stu-id="8c326-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![5. attēls](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="8c326-157">Lai pārskatītu visas kļūmju reģistrācijas, kas izveidotas darbu pasūtījumiem un uzturēšanas pieprasījumiem, klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="8c326-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="8c326-158">Lapā **Līdzekļu kļūmes** atlasiet līdzekļu kļūmes reģistrāciju un izvērsiet rūti **Saistītā informācija**, lai redzētu informāciju par saistīto darba pasūtījumu vai uzturēšanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="8c326-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

