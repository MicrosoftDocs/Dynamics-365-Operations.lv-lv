---
title: Automātiskā apstiprināšana, izmantojot plānošanas optimizāciju
description: Šajā tēmā skaidrots, kā izmantot automātiskās apstiprināšanas ar Plānošanas optimizācijas rīku.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227799"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="e8ae1-103">Automātiskā apstiprināšana, izmantojot plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="e8ae1-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8ae1-104">Automātiskā apstiprināšana ļauj apstiprināt (t.i., izlaist) plānotos pasūtījumus kā daļu no vispārējās plānošanas procesa.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="e8ae1-105">Kad plānotie pasūtījumi ir apstiprināti, tie tiek pārveidoti par faktiskajiem pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem vai ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="e8ae1-106">Kad tiek izmantots Plānošanas optimizācijas rīks, plānotie pasūtījumi tiek apstiprināti vispārējās plānošanas izpildes laikā, kad pasūtījuma datums (tas ir, sākuma datums) ir laika periods apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="e8ae1-107">Plānotā pirkšanas pasūtījuma automātisko apstiprināšanu var veikt tikai tad, ja krājums ir saistīts ar kreditoru.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="e8ae1-108">Automātiskās apstiprināšanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="e8ae1-108">Turn on autofirming</span></span>

<span data-ttu-id="e8ae1-109">Lai ieslēgtu automātisko apstiprināšanu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="e8ae1-110">Darbvietā **Līdzekļu pārvaldība** cilnē **Jauns** sarakstā atlasiet **Automātiskā apstiprināšana Plānošanas optimizācijai**.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="e8ae1-111">Ja šī funkcija netiek parādīta cilnē **Jauns**, skatiet cilnēs **Neiespējotās** un **Visas**.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e8ae1-112">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-112">Select **Enable now**.</span></span> <span data-ttu-id="e8ae1-113">Pēc izvēles atlasiet **Grafiks** un pēc tam atlasiet laiku, kad vēlaties ieslēgt līdzekli.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="e8ae1-114">Iestatiet apstiprināšanas noteikšanas periodu</span><span class="sxs-lookup"><span data-stu-id="e8ae1-114">Set up the firming time fence</span></span>

<span data-ttu-id="e8ae1-115">Apstiprināšanas periods tiek aprēķināts uz priekšu, sākot no vispārējās plānošanas datuma.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="e8ae1-116">To nosaka ievadīto dienu skaits.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="e8ae1-117">Apstiprināšanas laika ierobežojumu var kontrolēt šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="e8ae1-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="e8ae1-118">Lai definētu noklusējuma apstiprināšanas laika ierobežojumu nodrošinājuma grupai, dodieties uz **Vispārējā plānošana**\>**Iestatījumi**\>**Nodrošinājums**\>**Nodrošinājuma grupas** un atlasiet nodrošinājuma grupu.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="e8ae1-119">Pēc tam no kopsavilkuma cilnes **Citi** laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="e8ae1-120">Lai pārrakstītu apstiprināšanas laika periodu, kas noteikts nodrošinājuma grupai noteiktam krājumam, dodieties uz **Produkta informācijas pārvaldība** \> **Izlaistās preces**, pēc tam no darbības rūts atlasiet **Plāns** un pēc tam atlasiet **Krājumu nodrošinājums**.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="e8ae1-121">Pēc tam cilnē **Vispārīgi** atlasiet **Ignorēt laika periodu** un laukā **Automātisks apstiprināšanas periods (dienas)** ievadiet dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="e8ae1-122">Lai pārrakstītu apstiprināšanas laika periodu, kas ir definēts nodrošinājuma grupai un krājumu nodrošinājumam noteiktam vispārējam plānam, dodieties uz **Vispārējā plānošana**\>**Iestatījumi**\>**Vispārējie plāni** un atlasiet vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="e8ae1-123">Pēc tam kopsavilkuma cilnē  **Periods dienās** lauciņu **Apstiprināt** uzstādiet uz **Jā** un ievadiet dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="e8ae1-124">Ja ir ieslēgta automātiskā apstiprināšana vispārējai plānošanai, kas izmanto Plānošanas optimizāciju, automātiskās apstiprināšanas process tiek veikts saskaņā ar automātiskās apstiprināšanas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="e8ae1-125">Ja automātiskā apstiprināšana nav ieslēgta vai ja plānošana tiek sākta no lapas **Tīkla prasības**, automātiskās apstiprināšanas process tiek izlaists.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="e8ae1-126">Plānošanas optimizācija pret iebūvēto Supply Chain Management plānošanas programmu</span><span class="sxs-lookup"><span data-stu-id="e8ae1-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="e8ae1-127">Plānošanas optimizāciju un plānošanas programmu, kas ir iebūvēta Microsoft Dynamics 365 Supply Chain Management, var izmantot, lai automātiski apstiprinātu plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="e8ae1-128">Taču pastāv dažas svarīgas atšķirības.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-128">However, there are some important differences.</span></span> <span data-ttu-id="e8ae1-129">Piemēram, tā kā Plānošanas optimizācija izmanto pasūtījuma datumu (t.i., sākuma datumu), lai noteiktu, kurus plānotos pasūtījumus apstiprināt, iebūvētā Supply Chain Management plānošanas programma izmanto prasības datumu (t.i., beigu datumu).</span><span class="sxs-lookup"><span data-stu-id="e8ae1-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="e8ae1-130">Lūk, kopsavilkums par atšķirībām.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="e8ae1-131">**Plānošanas optimizācija**</span><span class="sxs-lookup"><span data-stu-id="e8ae1-131">**Planning Optimization**</span></span>

- <span data-ttu-id="e8ae1-132">Automātiskā apstiprināšana ir balstīta uz pasūtījuma datumu (sākuma datumu).</span><span class="sxs-lookup"><span data-stu-id="e8ae1-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="e8ae1-133">Tā kā pasūtījuma datums (sākuma datums) aktivizē apstiprināšanu, jums nav jāapsver izpildes laiks kā daļa no apstiprināšanas laika ierobežojuma.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="e8ae1-134">Ja vēlaties apstiprināt visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt vienai nedēļai.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="e8ae1-135">**Iebūvēta Supply Chain Management plānošanas programma**</span><span class="sxs-lookup"><span data-stu-id="e8ae1-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="e8ae1-136">Automātiskā apstiprināšana ir balstīta uz prasības datumu (beigu datuma).</span><span class="sxs-lookup"><span data-stu-id="e8ae1-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="e8ae1-137">Lai palīdzētu nodrošināt, ka pasūtījumi ir apstiprināti noteiktā laikā, apstiprināšanas laika periodam jābūt ilgākam par izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="e8ae1-138">Ja vēlaties apstiprināt visus pasūtījumus, kam jāsākas pašreizējās nedēļas laikā, apstiprināšanas laika periodam jābūt izpildes laikam plus viena nedēļa.</span><span class="sxs-lookup"><span data-stu-id="e8ae1-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]