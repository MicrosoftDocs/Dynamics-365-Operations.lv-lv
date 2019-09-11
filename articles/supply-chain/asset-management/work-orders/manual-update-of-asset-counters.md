---
title: Līdzekļu skaitītāju manuāla atjaunināšana
description: Šajā tēmā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875779"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="1fc7d-103">Līdzekļu skaitītāju manuāla atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1fc7d-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="1fc7d-104">Skaitītāji tiek izmantoti, lai izveidotu līdzekļa reģistrācijas, piemēram, attiecībā uz darbības stundām vai saražoto vienību daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="1fc7d-105">Ja skaitītāja tips, kas atlasīts skaitītājam, ir iestatīts uz mantotām skaitītāja vērtībām (**Līdzekļu pārvaldība** > **Uzstādīšana** > **Līdzekļu tipi** > **Skaitītāji** > **Vispārīgi** kopsavilkuma cilne > pārslēgšanas poga **Mantot līdzekļa skaitītāja vērtības** iestatīta uz "Jā"), tad, izveidojot jaunu skaitītāja rindu šim tipam, jebkurš apakšlīdzeklis, kurš izmanto to pašu skaitītāja tipu, tiek automātiski atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="1fc7d-106">Laukā **Visi līdzekļi** jūs izveidojat stundu vai daudzuma skaitītāja reģistrācijas līdzeklim, pamatojoties uz jūsu līdzekļa lasījumiem.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="1fc7d-107">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="1fc7d-108">Sarakstā atlasiet līdzekli un noklikšķiniet uz **Skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="1fc7d-109">Veidlapā **Līdzekļu skaitītāji** ir redzams saraksts ar visām iepriekšējām skaitītāju reģistrācijām atlasītajā līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="1fc7d-110">Lai izveidotu jaunu reģistrāciju, noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="1fc7d-111">Līdzekļa ID tiek ievietots automātiski.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="1fc7d-112">Laukā **Skaitītājs** atlasiet atbilstošo skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="1fc7d-113">Ir pieejami vienīgi tie skaitītāji, kas ir saistīti ar līdzekļa tipu, kas atlasīts līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="1fc7d-114">Saistītai vienums tiek automātiski ievadīts laukā **Vienums**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="1fc7d-115">Atlasiet skaitītāja reģistrācijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="1fc7d-116">Laukā **Vērtība** ievadiet skaitu kopš pēdējās skaitītāja reģistrācijas vai laukā **Apkopotā vērtība** ievadiet kopējo skaitu.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="1fc7d-117">Ja jūs līdzeklim fiziski instalējat jaunu skaitītāju, jums ir jāreģistrē līdzekļa izmaiņas laukā **Līdzekļa skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="1fc7d-118">Pēc tam jums ir jāizveido divas reģistrācijas rindas ar identiskiem laikspiedoliem un rindā, kas attiecas uz jauno skaitītāju, jūs atlasāt izvēles rūtiņu **Skaitītāja atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="1fc7d-119">Izveidojot divas reģistrācijas rindas, pirmajai rindai ir jāattiecas uz skaitītāju, kuru aizvietojat.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="1fc7d-120">Laukā **Kopsumma** kopējais skaits ir skaitītāja kopsumma no visām šajā skaitītāja tipā reģistrētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="1fc7d-121">Ja līdzeklī tiek atlasīta izvēles rūtiņa **Skaitītāja atiestatīšana**, izmantojot uzturēšanas plānu ar intervāla tipu "Vienreiz no..." vai "Kad sasniegts...", skaitītājs joprojām ir aktīvs jaunajai skaitītāja rindai, jo jūs izveidojat atsevišķu skaitītāja rindu un sākat no jauna ar jaunu skaitītāju.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![1. attēls](media/11-work-orders.png)


<span data-ttu-id="1fc7d-123">Ja jums ir jāveic skaitītāja reģistrācijas vairākiem līdzekļiem, to var izdarīt **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu skaitītāji**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="1fc7d-124">Jūs varat uzstādīt diapazonu, lai definētu nobīdes manuālajās skaitītāja reģistrācijās un ziņojuma veidu, kurš būtu jāuzrāda, ja reģistrācijas ir ārpus definētā diapazona.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="1fc7d-125">Skatiet tēmu [Skaitītāji](../setup-for-objects/counters.md) attiecībā uz skaitītāju uzstādīšanu.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
