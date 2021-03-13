---
title: Darba pasūtījumu veidi
description: Šajā tēmā ir paskaidroti darba pasūtījuma veidi līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9111ffa552059883696cf8248a02dfe70bc12ee7
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021533"
---
# <a name="work-order-types"></a><span data-ttu-id="168cd-103">Darba pasūtījumu veidi</span><span class="sxs-lookup"><span data-stu-id="168cd-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="168cd-104">Darba pasūtījumu veidi tiek izmantoti, lai kategorizētu darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="168cd-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="168cd-105">Piemēram, jums var būt darba pasūtījumi, kas saistīti ar profilaktisko uzturēšanu vai koriģējošo uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="168cd-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="168cd-106">Darba pasūtījuma veids definē piederību darba pasūtījuma dzīves cikla modelim.</span><span class="sxs-lookup"><span data-stu-id="168cd-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="168cd-107">Darba pasūtījuma dzīves cikla modelis definē darba pasūtījuma dzīves cikla stāvokļus, kurus var iestatīt darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="168cd-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="168cd-108">(Darba pasūtījumu dzīves cikla stāvokļu piemēri ir **Izveidots**, **Apstrādē** un **Pabeigts**.)</span><span class="sxs-lookup"><span data-stu-id="168cd-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="168cd-109">Lai iegūtu vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un projekta posmiem, skatiet sadaļu [Darba pasūtījuma dzīves cikla stāvokļi](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="168cd-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="168cd-110">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Darba pasūtījumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="168cd-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="168cd-111">Atlasiet **Jauns**, lai izveidotu jaunu darba pasūtījuma veidu.</span><span class="sxs-lookup"><span data-stu-id="168cd-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="168cd-112">Laukā **Darba pasūtījuma veids** ievadiet darba pasūtījuma veida ID.</span><span class="sxs-lookup"><span data-stu-id="168cd-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="168cd-113">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="168cd-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="168cd-114">Atlasiet dzīves cikla modeli laukā **Darba pasūtījuma dzīves cikla modelis**.</span><span class="sxs-lookup"><span data-stu-id="168cd-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="168cd-115">Iestatiet opciju **Viens uzturēšanas speciālists** uz **Jā**, ja visiem darba pasūtījumu uzdevumiem, kas saistīti ar šī veida darba pasūtījumu, ir jābūt plānotiem vienam uzturēšanas speciālistam.</span><span class="sxs-lookup"><span data-stu-id="168cd-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="168cd-116">Laukā **Izmaksu veids** atlasiet **Labojošs**, **Profilaktisks** vai **Investīciju** pēc atbilstības.</span><span class="sxs-lookup"><span data-stu-id="168cd-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="168cd-117">Visiem darba pasūtījuma uzdevumiem darba pasūtījumā jābūt ar vienādu izmaksu veidu.</span><span class="sxs-lookup"><span data-stu-id="168cd-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="168cd-118">Sadaļā **Obligāts** iestatiet atbilstošās opcijas uz **Jā**, lai norādītu, kura ar defektu vai uzturēšanas dīkstāvi saistītā informācija tiek pievienota šī veida darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="168cd-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="168cd-119">Opcijas sadaļā **Obligāts** ir saistītas ar opcijām kopsavilkuma cilnē **Validēt** lapā **Darba pasūtījuma dzīves cikla stāvokļi** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Dzīves cikla stāvokļi**).</span><span class="sxs-lookup"><span data-stu-id="168cd-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="168cd-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="168cd-120">Select **Save**.</span></span>

![Darba pasūtījumu veidi](media/16-setup-for-work-orders.png)
