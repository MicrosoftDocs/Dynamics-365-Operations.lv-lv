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
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918307"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="4d4bf-103">Līdzekļu kļūmju izmaksu kontrole</span><span class="sxs-lookup"><span data-stu-id="4d4bf-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4d4bf-104">Programmā Asset Management, varat aprēķināt reģistrēto līdzekļu kļūmju izmaksas, lai iegūtu pārskatu salīdzinājumā ar kļūmju budžetētajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="4d4bf-105">Faktiskās izmaksas ir balstītas uz publicētajiem darījumiem.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="4d4bf-106">Datums ir kļūmes datums, kurā tika reģistrēts simptoms.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="4d4bf-107">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļa kļūme** > **Līdzekļa kļūmes izmaksu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="4d4bf-108">Dialogā **Līdzekļu kļūmju izmaksu kontrole** izvēlieties finansiālo rādītāju kopu, ko iekļaut aprēķinā, ja vajadzīgs.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="4d4bf-109">Pārslēgšanas pogā **Izlaist nulli** atlasiet „Jā”, ja nevēlaties, lai rāda rezultātus, kas satur nulles izmaksas.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="4d4bf-110">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties izmaksu kontroles rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="4d4bf-111">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas līdzekļu kļūmju izmaksu kontroles rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="4d4bf-112">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas grafika rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="4d4bf-113">Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus kopsavilkuma cilnē **Iekļaujamie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="4d4bf-114">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="4d4bf-115">Darbības rūšu grupās **Grupēt pēc...** klikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4d4bf-116">Atlasītās darbības rūts pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="4d4bf-117">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="4d4bf-118">Tālāk esošajā attēlā ir parādīts līdzekļu kļūmes izmaksu kontroles aprēķina piemērs.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![1. attēls](media/05-controlling-and-reporting.png)

<span data-ttu-id="4d4bf-120">Skatiet sadaļu [Kļūmju pārvaldība](../setup-for-work-orders/fault-management.md), lai uzzinātu, kā iestatīt kļūmes.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="4d4bf-121">Laukā **Sākotnējais budžets** rāda budžetētās izmaksas no darba pasūtījuma prognozes.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="4d4bf-122">Laukā **Faktiskās izmaksas** rāda publicētās izmaksas darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="4d4bf-123">**Saistību izmaksu** lauks rāda kopīgās izmaksas, par kurām jūsu uzņēmumam ir saistības attiecībā uz darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="4d4bf-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

