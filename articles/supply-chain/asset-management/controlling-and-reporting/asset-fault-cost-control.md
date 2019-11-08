---
title: Līdzekļu kļūmju izmaksu kontrole
description: Šajā tēmā ir paskaidrota līdzekļu kļūmju izmaksu kontrole programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c34180ad99db29147587bb002aaa6badc918717
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652245"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="ed93f-103">Līdzekļu kļūmju izmaksu kontrole</span><span class="sxs-lookup"><span data-stu-id="ed93f-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ed93f-104">Programmā Līdzekļu pārvaldība, varat aprēķināt reģistrēto līdzekļu kļūmju izmaksas, lai iegūtu pārskatu salīdzinājumā ar budžetētajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="ed93f-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="ed93f-105">Faktiskās izmaksas ir balstītas uz publicētajiem darījumiem.</span><span class="sxs-lookup"><span data-stu-id="ed93f-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="ed93f-106">Datums ir kļūmes datums, kurā tika reģistrēts simptoms.</span><span class="sxs-lookup"><span data-stu-id="ed93f-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="ed93f-107">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļa kļūme** > **Līdzekļa kļūmes izmaksu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="ed93f-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="ed93f-108">Dialogā **Līdzekļu kļūmju izmaksu kontrole** izvēlieties finansiālo rādītāju kopu, ko iekļaut aprēķinā, ja vajadzīgs.</span><span class="sxs-lookup"><span data-stu-id="ed93f-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="ed93f-109">Pārslēgšanas pogā **Izlaist nulli** atlasiet „Jā”, ja nevēlaties, lai rāda rezultātus, kas satur nulles izmaksas.</span><span class="sxs-lookup"><span data-stu-id="ed93f-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="ed93f-110">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties izmaksu kontroles rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="ed93f-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="ed93f-111">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas līdzekļu kļūmju izmaksu kontroles rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="ed93f-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="ed93f-112">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="ed93f-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="ed93f-113">Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus kopsavilkuma cilnē **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="ed93f-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="ed93f-114">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="ed93f-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="ed93f-115">Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="ed93f-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="ed93f-116">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="ed93f-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="ed93f-117">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="ed93f-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="ed93f-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ed93f-118">Example</span></span>

<span data-ttu-id="ed93f-119">Šajā piemērā ir parādīts līdzekļu kļūmes izmaksu kontroles aprēķins.</span><span class="sxs-lookup"><span data-stu-id="ed93f-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="ed93f-120">Laukā **Sākotnējais budžets** rāda budžetētās izmaksas no darba pasūtījuma prognozes.</span><span class="sxs-lookup"><span data-stu-id="ed93f-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="ed93f-121">Laukā **Faktiskās izmaksas** rāda publicētās izmaksas darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ed93f-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="ed93f-122">**Saistību izmaksu** lauks rāda kopīgās izmaksas, par kurām jūsu uzņēmumam ir saistības attiecībā uz darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ed93f-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![1. attēls](media/05-controlling-and-reporting.png)

<span data-ttu-id="ed93f-124">Papildinformāciju par kļūmju iestatīšanu skatiet tēmā [Kļūmju pārvaldība](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="ed93f-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
