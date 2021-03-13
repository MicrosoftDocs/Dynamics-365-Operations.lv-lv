---
title: Līdzekļu skaitītāju manuāla atjaunināšana
description: Šajā tēmā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5318bac961682f88e192ac70c4993c62b69b399c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020889"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="47787-103">Pamatlīdzekļu skaitītāju manuāla atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="47787-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="47787-104">Skaitītāji tiek izmantoti, lai veidotu reģistrācijas uz līdzekļa, piemēram, reģistrācijas par līdzekļa darbības stundu skaitu, vai par saražoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="47787-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="47787-105">Atlasītais skaitītāja veids var būt iestatīts tā, lai tas pārmantotu skaitītāja vērtības.</span><span class="sxs-lookup"><span data-stu-id="47787-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="47787-106">Citiem vārdiem, opcija **Pārmantot līdzekļa skaitītāja vērtības** ir iestatīta uz **Jā**, kas atrodas kopsavilkuma cilnē **Vispārīgi** lapā **Skaitītāji** (**Līdzekļa pārvaldība** > **Iestatīšana** > **Līdzekļu veidi** > **Skaitītāji**).</span><span class="sxs-lookup"><span data-stu-id="47787-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="47787-107">Šādā gadījumā, veidojot jaunu šī vaida skaitītāja rindu, katrs pakārtotais līdzeklis, kas izmanto tādu pašu skaitītāja veidu, tiek automātiski atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="47787-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="47787-108">Lapā **Visi līdzekļi** jūs izveidojat stundu vai daudzuma skaitītāja reģistrācijas līdzeklim, pamatojoties uz jūsu līdzekļa lasījumiem.</span><span class="sxs-lookup"><span data-stu-id="47787-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="47787-109">Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**</span><span class="sxs-lookup"><span data-stu-id="47787-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="47787-110">Atlasiet līdzekli un pēc tam darbības rūtī, cilnē **Līdzeklis** grupā **Profilaktiska** atlasiet **Skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="47787-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="47787-111">Lapā **Līdzekļu skaitītāji** ir redzams saraksts ar visām iepriekšējām skaitītāju reģistrācijām, kas tika veiktas atlasītajā līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="47787-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="47787-112">Atlasiet **Jauns**, lai izveidotu reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="47787-112">Select **New** to create a registration.</span></span> <span data-ttu-id="47787-113">Līdzekļa ID tiek automātiski ievadīts laukā **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="47787-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="47787-114">Laukā **Skaitītājs** atlasiet atbilstošo skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="47787-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="47787-115">Atlasei ir pieejami vienīgi tie skaitītāji, kas ir saistīti ar līdzekļa tipu, kas atlasīts līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="47787-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="47787-116">Saistītais vienums tiek automātiski ievadīts laukā **Vienums**.</span><span class="sxs-lookup"><span data-stu-id="47787-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="47787-117">Laukā **Reģistrētajā** atlasiet skaitītāja reģistrācijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="47787-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="47787-118">Laukā **Vērtība** ievadiet numuru kopš pēdējās skaitītāja reģistrācijas.</span><span class="sxs-lookup"><span data-stu-id="47787-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="47787-119">Vai arī laukā **Uzkrātā vērtība** ievadiet kopējo skaitu.</span><span class="sxs-lookup"><span data-stu-id="47787-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="47787-120">Ņemiet vērā šādus punktus:</span><span class="sxs-lookup"><span data-stu-id="47787-120">Note the following points:</span></span>

- <span data-ttu-id="47787-121">Ja jūs līdzeklim fiziski instalējat jaunu skaitītāju, jums ir jāreģistrē līdzekļa izmaiņas lapā **Līdzekļa skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="47787-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="47787-122">Pēc tam jāizveido divas reģistrācijas rindas ar identiskiem laikspiedoliem.</span><span class="sxs-lookup"><span data-stu-id="47787-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="47787-123">Pirmajai rindai jābūt aizvietotajam skaitītājam.</span><span class="sxs-lookup"><span data-stu-id="47787-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="47787-124">Rindā, kas saistīta ar jauno skaitītāju, atzīmējiet izvēles rūtiņu **Skaitītāja atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="47787-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="47787-125">Laukā **Kopsumma** kopējais skaits ir skaitītāja kopsummas no visām šajā skaitītāja tipā reģistrētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="47787-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="47787-126">Ja līdzeklī tiek atlasīta izvēles rūtiņa **Skaitītāja atiestatīšana**, izmantojot uzturēšanas plānu ar intervāla veidu "Vienreiz no..." vai "Kad sasniegts...", skaitītājs joprojām ir aktīvs jaunajai skaitītāja rindai, jo jūs izveidojat atsevišķu skaitītāja rindu un sākat no jauna ar jaunu skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="47787-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="47787-127">Attēlā zemāk ir parādīta lapa **Līdzekļu skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="47787-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![1. attēls](media/11-work-orders.png)

<span data-ttu-id="47787-129">Lapā **Līdzekļu skaitītāji** (**Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu skaitītāji**) var veikt skaitītāja reģistrācijas vairākiem līdzekļiem vienlaicīgi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="47787-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="47787-130">Varat iestatīt diapazonu, lai definētu novirzes manuālā skaitītāja reģistrācijās.</span><span class="sxs-lookup"><span data-stu-id="47787-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="47787-131">Varat arī norādīt ziņojuma veidu, kas tiek parādīts, ja reģistrācijas ir ārpus definētā diapazona.</span><span class="sxs-lookup"><span data-stu-id="47787-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="47787-132">Papildinformāciju par to, kā iestatīt saistītos skaitītājus, skatiet [Skaitītāji](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="47787-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

