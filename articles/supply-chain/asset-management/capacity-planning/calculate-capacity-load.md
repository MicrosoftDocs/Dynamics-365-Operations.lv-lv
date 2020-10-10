---
title: Aprēķināt noslodzes grafiku
description: Šajā tēmā paskaidrots, kā aprēķināt noslodzi programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888742"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="aae88-103">Aprēķināt noslodzes grafiku</span><span class="sxs-lookup"><span data-stu-id="aae88-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="aae88-104">Līdzekļu pārvaldībā varat aprēķināt noslodzi</span><span class="sxs-lookup"><span data-stu-id="aae88-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="aae88-105">uzturēšanas grafika rindām,</span><span class="sxs-lookup"><span data-stu-id="aae88-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="aae88-106">darba pasūtījumiem, kas vēl nav ieplānoti,</span><span class="sxs-lookup"><span data-stu-id="aae88-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="aae88-107">ieplānotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="aae88-107">scheduled work orders</span></span>

<span data-ttu-id="aae88-108">Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamo noslodzi konkrētam periodam.</span><span class="sxs-lookup"><span data-stu-id="aae88-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="aae88-109">Noslodzes aprēķinu var veikt visiem līdzekļiem vai atlasītiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="aae88-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="aae88-110">Jūs varat izveidot aprēķinu arī dīkstāves uzturēšanas dēļ darbībām vai darba pasūtījumu apkopojumiem.</span><span class="sxs-lookup"><span data-stu-id="aae88-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="aae88-111">Klikšķiniet uz pogas **Līdzekļu pārvaldība** > **Pieprasījumi** > **Noslodze** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Darbu pasūtījuma kopas** > **Visas darbu pasūtījumu kopas** / **Aktīvās darba pasūtījumu kopas** >, atlasiet darba pasūtījumu kopu sarakstā > **Noslodze** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Dīkstāve uzturēšanas dēļ** > **Visas dīkstāves uzturēšanas dēļ darbības** / **Aktīvās dīkstāves uzturēšanas dēļ darbības** >, atlasīt uzturēšanas darbību sarakstā > **Noslodze**.</span><span class="sxs-lookup"><span data-stu-id="aae88-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="aae88-112">Dialogā **Aprēķināt noslodzi** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Sākuma datums/laiks** un **Beigu datums/laiks**.</span><span class="sxs-lookup"><span data-stu-id="aae88-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="aae88-113">Pārslēgšanas pogā **Iekļaut uzturēšanas grafiku** atlasiet "Jā", ja vēlaties iekļaut aprēķinā uzturēšanas grafika rindas.</span><span class="sxs-lookup"><span data-stu-id="aae88-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="aae88-114">Pārslēgšanas pogā **Iekļaut darba pasūtījumu**. atlasiet "Jā", ja vēlaties iekļaut aprēķinā darba pasūtījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="aae88-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="aae88-115">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētu vēlaties noslodzes rindu aprēķinu attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="aae88-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="aae88-116">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas un darba pasūtījumus funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="aae88-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="aae88-117">Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas un darba pasūtījumus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="aae88-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="aae88-118">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="aae88-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="aae88-119">Grupās **Grupēt pēc...** noklikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="aae88-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="aae88-120">Attēlā tālāk atlasītās pogas **Grupēt pēc** ir izceltas zilā krāsā.</span><span class="sxs-lookup"><span data-stu-id="aae88-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="aae88-121">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="aae88-121">Click on a button to activate or deactivate it.</span></span>

    ![1. attēls](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="aae88-123">Ja vēlaties koncentrēties tikai uz noslodzes plānošanu attiecībā uz ieplānotiem darba pasūtījumiem, skatiet [Aprēķināt noslodzi ieplānotiem darba pasūtījumiem](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="aae88-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

