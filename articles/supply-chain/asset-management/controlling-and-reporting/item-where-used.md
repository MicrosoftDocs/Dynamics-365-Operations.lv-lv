---
title: Krājuma izmantošanas vietas
description: Šajā tēmā ir paskaidrots, kā iegūt pārskatu par to, kur vienums tiek izmantots Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc78568e314c7cf83848ed2c39f9613d6ed638ba
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889629"
---
# <a name="item-where-used"></a><span data-ttu-id="d1fc4-103">Krājuma izmantošanas vietas</span><span class="sxs-lookup"><span data-stu-id="d1fc4-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d1fc4-104">Jūs varat veikt aprēķinu konkrētam vienumam, lai iegūtu pārskatu par to, kur vienums tiek izmantots Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="d1fc4-105">Rezultātos tiek parādīts konteksts, kurā vienums ir izmantots tā dzīves laikā.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="d1fc4-106">Līdzekļu pārvaldības galvenajā izvēlē var atvērt lapu **Vienums, kurā izmantots** un tai var arī piekļūt no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="d1fc4-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="d1fc4-107">Līdzekļa MK</span><span class="sxs-lookup"><span data-stu-id="d1fc4-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="d1fc4-108">Rezerves daļas līdzekļa tipa noklusējumos</span><span class="sxs-lookup"><span data-stu-id="d1fc4-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="d1fc4-109">Uzturēšanas darbu tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu tirdzniecība un uzturēšanas kontrolsaraksti</span><span class="sxs-lookup"><span data-stu-id="d1fc4-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="d1fc4-110">Uzturēšanas prognoze</span><span class="sxs-lookup"><span data-stu-id="d1fc4-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="d1fc4-111">Sagāde</span><span class="sxs-lookup"><span data-stu-id="d1fc4-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="d1fc4-112">Darba pasūtījuma iegāde</span><span class="sxs-lookup"><span data-stu-id="d1fc4-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="d1fc4-113">Veiciet aprēķinu par elementu, kurā izmantots</span><span class="sxs-lookup"><span data-stu-id="d1fc4-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="d1fc4-114">Noklikšķiniet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Elements, kurā izveidots** vai atlasiet pogu **Elements, kurā izmantots** vienā no augstāk minētajām lapām.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="d1fc4-115">Dialoglodziņā **Elements, kurā izmantots** laukā **Vienuma numurs** atlasiet vienumu, kuram vēlaties veikt aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="d1fc4-116">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties elementa rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="d1fc4-117">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas vienuma rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="d1fc4-118">Tādējādi relāciju/daudzumu rindā var pievienot no funkcionālā novietojuma, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="d1fc4-119">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas vienuma rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="d1fc4-120">Sadaļā **Iekļaut**. atlasiet "Jā" pārslēgšanas pogās, kuras vēlaties iekļaut aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="d1fc4-121">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="d1fc4-122">Cilnē **Vienums, kurā izmantots** atlasiet **Grupēt pēc** pogas, lai uzrādītu nepieciešamo aprēķina informācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d1fc4-123">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="d1fc4-124">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="d1fc4-125">Ja vēlaties rādīt izmērus, kas saistīti ar vienumu, noklikšķiniet **Rādīt izmērus** un atlasiet uzrādāmos izmērus.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="d1fc4-126">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d1fc4-126">Example</span></span>

<span data-ttu-id="d1fc4-127">Zemāk redzamajā ekrānuzņēmumā ir redzams "vienuma, kurā izmantots" aprēķina piemērs vienuma numuram "1000".</span><span class="sxs-lookup"><span data-stu-id="d1fc4-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

!["Vienuma, kurā izmantots" aprēķina piemērs](media/12-controlling-and-reporting.png)

