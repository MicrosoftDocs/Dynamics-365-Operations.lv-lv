---
title: Patēriņa atskaišu veidošana
description: Šajā tēmā ir paskaidrots, kā izveidot patēriņa atskaites programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
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
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216440"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="f476c-103">Patēriņa atskaišu veidošana</span><span class="sxs-lookup"><span data-stu-id="f476c-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f476c-104">Kad ir izveidota un publicēta patēriņa reģistrācija darba pasūtījumiem programmā Asset Management, ir pieejamas divas atskaites, kas parāda patēriņa informāciju.</span><span class="sxs-lookup"><span data-stu-id="f476c-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="f476c-105">Līdzekļu patēriņa atskaite</span><span class="sxs-lookup"><span data-stu-id="f476c-105">Asset consumption report</span></span>

<span data-ttu-id="f476c-106">Kad ir publicēts darba pasūtījumu patēriņš, varat izdrukāt līdzekļa patēriņa atskaiti.</span><span class="sxs-lookup"><span data-stu-id="f476c-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="f476c-107">Atskaitē parādītas stundas, stundas izmaksas, vienuma izmaksas, līdzekļiem publicētie izdevumi.</span><span class="sxs-lookup"><span data-stu-id="f476c-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="f476c-108">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Atskaites** > **Līdzekļi** > **Līdzekļu patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="f476c-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="f476c-109">Dialogā **Līdzekļu patēriņš** atlasiet parametrus un detaļu līmeni, ko gribat redzēt, atlasot **Jā** attiecīgajās pārslēgšanas pogās un ievietojot funkcionālo novietojumu sadaļā **Rādīt**.</span><span class="sxs-lookup"><span data-stu-id="f476c-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="f476c-110">Jūs varat izmantot lauku **Līmeņi**, lai noteiktu, cik detalizētas vēlaties līdzekļa rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="f476c-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="f476c-111">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visi līdzekļi funkcionālajam novietojumam tiks uzrādīti augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienots no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="f476c-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="f476c-112">Ja laukā **Līmeņi** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs līdzekļus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="f476c-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="f476c-113">Lai redzētu summas katram apakšlīdzeklim atskaitē, atlasiet **Jā** pārslēgšanas pogā **Visu apakšlīdzekļu summa**.</span><span class="sxs-lookup"><span data-stu-id="f476c-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="f476c-114">Atlasiet datuma intervālu sadaļā **Datumi**.</span><span class="sxs-lookup"><span data-stu-id="f476c-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="f476c-115">Kopsavilkuma cilnē **Galamērķis** atlasiet, vai vēlaties skatīt atskaiti ekrānā, izdrukāt vai saglabāt kā failu vai e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f476c-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="f476c-116">Ja vajadzīgs, varat atlasīt konkrētus līdzekļus, ko parādīt atskaitē.</span><span class="sxs-lookup"><span data-stu-id="f476c-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="f476c-117">Kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un pievienojiet līdzekļus, ko vēlaties iekļaut sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f476c-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="f476c-118">Klikšķiniet **Labi**, lai izveidotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="f476c-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="f476c-119">Darba pasūtījuma patēriņa atskaite</span><span class="sxs-lookup"><span data-stu-id="f476c-119">Work order consumption report</span></span>

<span data-ttu-id="f476c-120">Kad ir publicēts darba pasūtījumu patēriņš, varat izdrukāt darba pasūtījumu patēriņa atskaiti.</span><span class="sxs-lookup"><span data-stu-id="f476c-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="f476c-121">Atskaitē parādītas darba pasūtījumiem publicētās stundas, stundas izmaksas, vienuma izmaksas, izdevumi.</span><span class="sxs-lookup"><span data-stu-id="f476c-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="f476c-122">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Atskaites** > **Darba pasūtījumi** > **Darba pasūtījumu patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="f476c-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="f476c-123">Dialogā **Darba pasūtījuma patēriņš** atlasiet parametrus, ko vēlaties iekļaut atskaitē, atlasot **Jā** attiecīgajās pārslēgšanas pogās un ievietojot funkcionālo novietojumu sadaļā **Rādīt**.</span><span class="sxs-lookup"><span data-stu-id="f476c-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="f476c-124">Atlasiet datuma intervālu sadaļā **Datumi**.</span><span class="sxs-lookup"><span data-stu-id="f476c-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="f476c-125">Kopsavilkuma cilnē **Galamērķis** atlasiet, vai vēlaties skatīt atskaiti ekrānā, izdrukāt vai saglabāt kā failu vai e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f476c-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="f476c-126">Ja vajadzīgs, varat atlasīt konkrētus darba pasūtījumus, ko parādīt atskaitē.</span><span class="sxs-lookup"><span data-stu-id="f476c-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="f476c-127">Kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un pievienojiet darba pasūtījumus, ko vēlaties iekļaut sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f476c-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="f476c-128">Klikšķiniet **Labi**, lai izveidotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="f476c-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="f476c-129">Varat arī izveidot [darba pasūtījuma atskaiti](../work-orders/work-order-report.md), kas satur vel vairāk darba pasūtījuma detaļu.</span><span class="sxs-lookup"><span data-stu-id="f476c-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

