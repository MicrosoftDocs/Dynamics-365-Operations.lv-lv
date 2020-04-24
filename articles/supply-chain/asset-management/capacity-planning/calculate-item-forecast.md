---
title: Aprēķināt krājumu prognozi
description: Šajā tēmā paskaidrots, kā aprēķināt vienuma prognozi programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
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
ms.openlocfilehash: 20f969b68e4e9a9936f377000191ba9db202447f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216463"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="68ffb-103">Aprēķināt krājumu prognozi</span><span class="sxs-lookup"><span data-stu-id="68ffb-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="68ffb-104">Tāpat kā veikt noslodzes aprēķinus, kas aprakstīti iepriekšējā sadaļā, varat veikt arī vienuma prognozes aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="68ffb-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="68ffb-105">uzturēšanas grafika rindām,</span><span class="sxs-lookup"><span data-stu-id="68ffb-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="68ffb-106">darba pasūtījumiem, kas vēl nav ieplānoti,</span><span class="sxs-lookup"><span data-stu-id="68ffb-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="68ffb-107">ieplānotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="68ffb-107">scheduled work orders</span></span>

<span data-ttu-id="68ffb-108">Tas ir noderīgi, ja vēlaties iegūt pārskatu par paredzamo vienuma patēriņu (rezerves daļas un citi vienumi, kas vajadzīgi darba pasūtījuma pabeigšanai) noteiktam periodam.</span><span class="sxs-lookup"><span data-stu-id="68ffb-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="68ffb-109">Vienuma prognozes aprēķinu var veikt visiem līdzekļiem vai atlasītiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="68ffb-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="68ffb-110">Varat veikt arī dīkstāves uzturēšanas dēļ aprēķinu (**Visas dīkstāves uzturēšanas dēļ darbības** vai **Aktīvās dīkstāves uzturēšanas dēļ darbības**) vai darba pasūtījumu kopai (**Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas**).</span><span class="sxs-lookup"><span data-stu-id="68ffb-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="68ffb-111">Klikšķiniet uz pogas **Aktīvu pārvaldība** > **Pieprasījumi** > **Vienuma prognoze** vai **Līdzekļu pārvaldība** > **Kopīgi** > **Darbu pasūtījuma kopas** > **Visas darbu pasūtījumu kopas** / **Aktīvās darba pasūtījumu kopas** > atlasiet darba pasūtījumu kopu sarakstā > **Vienuma prognoze** vai **Aktīvu pārvaldība** > **Vispārīgi** > **Dīkstāve uzturēšanas dēļ** > **Visas dīkstāves uzturēšanas dēļ darbības** / **Aktīvās dīkstāves uzturēšanas dēļ darbības** > atlasiet uzturēšanas darbību sarakstā > **Vienuma prognoze**.</span><span class="sxs-lookup"><span data-stu-id="68ffb-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="68ffb-112">Dialogā **Aprēķināt vienuma prognozi** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Sākuma datums/laiks** un **Beigu datums/laiks**.</span><span class="sxs-lookup"><span data-stu-id="68ffb-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="68ffb-113">Pārslēgšanas pogā **Iekļaut uzturēšanas grafiku**. atlasiet "Jā", ja vēlaties iekļaut prognozes aprēķinā uzturēšanas grafika rindas.</span><span class="sxs-lookup"><span data-stu-id="68ffb-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="68ffb-114">Pārslēgšanas pogā **Iekļaut darba pasūtījumu**. atlasiet "Jā", ja vēlaties iekļaut prognozes aprēķinā darba pasūtījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="68ffb-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="68ffb-115">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties vienuma prognozes rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="68ffb-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="68ffb-116">Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas un darba pasūtījumus funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="68ffb-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="68ffb-117">Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas un darba pasūtījumus visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="68ffb-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="68ffb-118">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="68ffb-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="68ffb-119">Grupās **Grupēt pēc...** noklikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="68ffb-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="68ffb-120">Attēlā tālāk atlasītās pogas **Grupēt pēc** ir izceltas zilā krāsā.</span><span class="sxs-lookup"><span data-stu-id="68ffb-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="68ffb-121">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="68ffb-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="68ffb-122">Ja vēlaties rādīt produkta, glabāšanas vai izsekošanas īpašības, kas saistītas ar vienumu, noklikšķiniet uz **Rādīt izmērus**.</span><span class="sxs-lookup"><span data-stu-id="68ffb-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="68ffb-123">Atzīmējiet attiecīgās izvēles rūtiņas un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="68ffb-123">Select the relevant check boxes, and click **OK**.</span></span>

![1. attēls](media/02-capacity-planning.png)
