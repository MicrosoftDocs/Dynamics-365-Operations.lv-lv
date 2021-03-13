---
title: Darba stundu kontrole
description: Šajā tēmā ir aprakstīta darba stundu kontrole līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc4382d72e032fdfad05f2077ffe8e41e64c6a55
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018475"
---
# <a name="work-hour-control"></a><span data-ttu-id="1e100-103">Darba stundu kontrole</span><span class="sxs-lookup"><span data-stu-id="1e100-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1e100-104">Līdzekļu pārvaldībā varat aprēķināt stundas, lai iegūtu pārskatu par faktiskajām stundām, salīdzinot ar budžeta stundām uz līdzekļiem, funkcionālajiem novietojumiem vai darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="1e100-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="1e100-105">Faktiskās stundas ir balstītas uz grāmatotajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1e100-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="1e100-106">Darba stundu kontrole līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="1e100-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="1e100-107">Aprēķini, kas veikti līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem, ir gandrīz identiski.</span><span class="sxs-lookup"><span data-stu-id="1e100-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="1e100-108">Tikai atšķirība ir tā, ka līdzekļiem un funkcionālajam novietojumam aprēķinā var iekļaut arī pakārtotus līdzekļus un pakārtotas atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="1e100-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="1e100-109">Datums ir transakcijas datums, kad reģistrācija tika ierakstīta.</span><span class="sxs-lookup"><span data-stu-id="1e100-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="1e100-110">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu stundu kontrole** vai **Funkcionālā novietojuma stundu kontrole**, vai **Līdzekļu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu stundu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="1e100-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="1e100-111">Dialoglodziņā **Līdzekļu stundu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="1e100-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="1e100-112">Dialoglodziņā **Līdzekļa stundu kontrole** / **Funkcionālā novietojuma stundu kontrole** / **Darba pasūtījumu stundu kontrole** atlasiet periodu, kas jāaprēķina laukos **No datuma** un **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="1e100-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="1e100-113">Ja nepieciešams, atlasiet **Finanšu dimensiju kopu**, kas jāiekļauj aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="1e100-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="1e100-114">Ja nevēlaties rādīt rezultātus, kas satur nulles, atlasiet “Jā” pārslēgšanas pogā **Izlaist nulles**.</span><span class="sxs-lookup"><span data-stu-id="1e100-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="1e100-115">Varat izmantot lauku **Līmenis**, lai norādītu, cik detalizētas jūs vēlaties stundu kontroles rindas attiecībā uz funkcionālajiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="1e100-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="1e100-116">Piemēram, ja laukā tiek ievietots skaitlis “1” un jums ir vairāku līmeņu funkcionālo novietojumu hierarhija, visaugstākajā līmenī tiks rādītas visas stundu kontroles rindas funkcionālā novietojumā, tāpēc stundas rindā var tikt pievienotas no funkcionālajiem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="1e100-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="1e100-117">Ja laukā **Līmenis** tiek ievadīts skaitlis “0”, tiek parādīts detalizēts rezultāts, kas parāda visas stundu kontroles rindas visiem funkcionālā novietojuma vietas līmeņiem, ar kuriem tās ir saistītas.</span><span class="sxs-lookup"><span data-stu-id="1e100-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="1e100-118">Atlasiet “Jā” pārslēgšanas pogā **Ietvert pakārtotos līdzekļus**, lai parādītu izmaksas, kas saistītas ar pakārtotajiem līdzekļiem kā atsevišķas rindas.</span><span class="sxs-lookup"><span data-stu-id="1e100-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="1e100-119">Ja vēlaties ierobežot meklēšanu, varat atlasīt konkrētus līdzekļus/funkcionālos novietojumus/darba pasūtījumus, lai iekļautu kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**.</span><span class="sxs-lookup"><span data-stu-id="1e100-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="1e100-120">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="1e100-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="1e100-121">Lapā **Stundu izmaksu kontrole** noklikšķiniet uz attiecīgās pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="1e100-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="1e100-122">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="1e100-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="1e100-123">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="1e100-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="1e100-124">Paraugs</span><span class="sxs-lookup"><span data-stu-id="1e100-124">Example</span></span>

<span data-ttu-id="1e100-125">Ekrānšāviņā redzams aprēķina **Līdzekļu stundu kontrole** piemērs.</span><span class="sxs-lookup"><span data-stu-id="1e100-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="1e100-126">Lauks **Sākotnējais budžets** rāda budžeta stundas no darba pasūtījuma prognozes.</span><span class="sxs-lookup"><span data-stu-id="1e100-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="1e100-127">Lauks **Faktiskās stundas** rāda darba pasūtījumu grāmatotās stundas.</span><span class="sxs-lookup"><span data-stu-id="1e100-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="1e100-128">Lauks **Fiksētās stundas** parāda kopējo stundu summu, ko jūsu uzņēmums ir izmantojis saistībā ar darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="1e100-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Pamatlīdzekļu stundu kontroles aprēķina piemērs](media/04-controlling-and-reporting.png)

<span data-ttu-id="1e100-130">Cits stundu aprēķina veids ir vairāku atlasīto līdzekļu atlasīšana sadaļās **Visi līdzekļi** vai **Aktīvie līdzekļi**</span><span class="sxs-lookup"><span data-stu-id="1e100-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="1e100-131">Pēc tam noklikšķiniet uz pogas **Stundu kontrole**, kas atrodas kopsavilkuma cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="1e100-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="1e100-132">Atlasītie līdzekļi automātiski tiek ievietoti laukā **Līdzekļi** kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**.</span><span class="sxs-lookup"><span data-stu-id="1e100-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="1e100-133">Noklikšķiniet uz **Labi** dialoglodziņā **Līdzekļu stundu kontrole**, un tiks parādīts atlasīto līdzekļu aprēķins.</span><span class="sxs-lookup"><span data-stu-id="1e100-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="1e100-134">To pašu procedūru var veikt funkcionālajiem novietojumiem sadaļās **Visi funkcionālie novietojumi** vai **Aktīvie funkcionālie novietojumi** un darba pasūtījumiem sadaļās **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="1e100-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


