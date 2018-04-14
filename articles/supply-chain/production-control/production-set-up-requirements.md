---
title: "Ražošanas iestatījumu prasības"
description: "Šajā rakstā ir sniegta informācija par iestatīšanas prasībām, kas jāievēro, lai varētu strādāt ar ražošanas kontroli."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bcca20889fa0b79a289175ab901167509a908f3f
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="production-setup-requirements"></a><span data-ttu-id="95945-103">Ražošanas iestatījumu prasības</span><span class="sxs-lookup"><span data-stu-id="95945-103">Production setup requirements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="95945-104">Šajā rakstā ir sniegta informācija par iestatīšanas prasībām, kas jāievēro, lai varētu strādāt ar ražošanas kontroli.</span><span class="sxs-lookup"><span data-stu-id="95945-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="95945-105">Modulis Ražošanas kontrole ir integrēts citu moduļu līdzekļos.</span><span class="sxs-lookup"><span data-stu-id="95945-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="95945-106">Šīs savstarpējās saistīšanas iespējas jums ļauj mainīt ražošanas pasūtījumus un nodrošināt, ka tie automātiski tiek atjaunināti visos pārējos sistēmas saistītajos procesos un aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="95945-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="95945-107">Nākamās iestatīšanas procedūras ir uzskaitītas tādā secībā, kādā jums tās ir jāizpilda.</span><span class="sxs-lookup"><span data-stu-id="95945-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="95945-108">Nepieciešamais bāzlīnijas iestatījums citos moduļos</span><span class="sxs-lookup"><span data-stu-id="95945-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="95945-109">Lai varētu strādāt ar ražošanas kontroli, ir jāiestata informācija pārējos moduļos.</span><span class="sxs-lookup"><span data-stu-id="95945-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="95945-110">Šajā iestatīšanā ir iekļauti tālāk minētie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="95945-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="95945-111">Iestatiet vispārējo uzņēmuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="95945-111">Set up general company information.</span></span>
-   <span data-ttu-id="95945-112">Iestatiet Virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="95945-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="95945-113">Definējiet krājumu grupas.</span><span class="sxs-lookup"><span data-stu-id="95945-113">Define item groups.</span></span>
-   <span data-ttu-id="95945-114">Iestatiet krājumu grupām Virsgrāmatas kontus.</span><span class="sxs-lookup"><span data-stu-id="95945-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="95945-115">Iestatiet krājuma vienību tabulu sadaļā Krājumu vadība.</span><span class="sxs-lookup"><span data-stu-id="95945-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="95945-116">Izveidojiet materiālu komplektus (MK) un MK versijas sadaļa Krājumu vadība.</span><span class="sxs-lookup"><span data-stu-id="95945-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="95945-117">Nepieciešamais kalendāra un resursu iestatījums</span><span class="sxs-lookup"><span data-stu-id="95945-117">Required calendar and resource setup</span></span>
<span data-ttu-id="95945-118">Pirms lietojat ražošanas kontroli, atveriet sadaļu Organizācijas administrēšana, un izveidojiet un definējiet kalendāru un operācijas resursus tālāk norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="95945-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="95945-119">**Darba laika veidnes** — iestatiet darba laiku veidnes, lai definētu ražošanas plānošanai pieejamos laikus.</span><span class="sxs-lookup"><span data-stu-id="95945-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="95945-120">**Kalendāri** — iestatiet darba laika kalendārus, lai definētu tās gada dienas, kas ir pieejamas ražošanas plānošanai.</span><span class="sxs-lookup"><span data-stu-id="95945-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="95945-121">**Resursu grupas** — iestatiet resursu grupas, lai grupētu operāciju resursus — šādi varat gūt pārskatu par visu brīvo noslodzi, kad izpildāt plānošanu.</span><span class="sxs-lookup"><span data-stu-id="95945-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="95945-122">Nav nepieciešams iestatīt resursu grupas, pirms esat iestatījis operācijas resursus.</span><span class="sxs-lookup"><span data-stu-id="95945-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="95945-123">Taču iesakām izprast veidu, ka grupēt resursus, kad iestatāt ražošanas kontroli.</span><span class="sxs-lookup"><span data-stu-id="95945-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="95945-124">**Resursi** — iestatiet operācijas resursus, lai definētu resursus, ko izmantot ražošanas procesu veikšanai un noslodzes plānošanai.</span><span class="sxs-lookup"><span data-stu-id="95945-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="95945-125">Nepieciešamais ražošanas parametru iestatījums</span><span class="sxs-lookup"><span data-stu-id="95945-125">Required production parameters setup</span></span>
<span data-ttu-id="95945-126">**Ražošanas kontroles parametri** — iestatiet ražošanas pamata parametrus, lai definētu, kā sistēmā tiek izmantoti un apstrādāti ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="95945-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="95945-127">Definējiet veidu, kā ražošanas pasūtījumi tiek izveidoti, novērtēti, plānoti un patērēti.</span><span class="sxs-lookup"><span data-stu-id="95945-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="95945-128">Varat arī atlasīt, kāda veida atsauksmes vēlaties un kā veikt izmaksu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="95945-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="95945-129">Nepieciešamā žurnāla nosaukuma identifikācija</span><span class="sxs-lookup"><span data-stu-id="95945-129">Required journal name identification</span></span>
<span data-ttu-id="95945-130">**Ražošanas žurnāla nosaukumi** — norādiet ražošanas žurnālu nosaukumus, kas tiek izmantoti, lai ierakstītu un grāmatotu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="95945-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="95945-131">Iestatījums, ja izmantojat operācijas</span><span class="sxs-lookup"><span data-stu-id="95945-131">Setup if you use operations</span></span>
<span data-ttu-id="95945-132">Operācijas pārstāv specifiskās aktivitātes, kas tiek izpildītas, lai ražotu pabeigtās preces.</span><span class="sxs-lookup"><span data-stu-id="95945-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="95945-133">**Piezīme.** Jums ir jāzina, kāda tipa aktivitātes ir nepieciešamas, lai saražotu jūsu krājumu, kā arī jāzina šo aktivitāšu secība un prioritātes.</span><span class="sxs-lookup"><span data-stu-id="95945-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="95945-134">Jums ir arī jāzina, kuri resursi ir iesaistīti un to daudzums.</span><span class="sxs-lookup"><span data-stu-id="95945-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="95945-135">**Operācijas** — iestatiet operācijas, lai parādītu uzdevumus, kas ir jāizpilda, lai saražotu pabeigto krājumu.</span><span class="sxs-lookup"><span data-stu-id="95945-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="95945-136">**Relācijas** — iestatiet operāciju relācijas, lai izveidotu detalizētus rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="95945-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="95945-137">Lai definētu operāciju relācijas, noklikšķiniet uz**Relācijas** lapā **Operācijas**.</span><span class="sxs-lookup"><span data-stu-id="95945-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="95945-138">Iestatījums, ja izmantojat maršrutus</span><span class="sxs-lookup"><span data-stu-id="95945-138">Setup if you use routes</span></span>
<span data-ttu-id="95945-139">Ja strādājat ar maršrutiem, tad operācijas ir nepieciešams definēt katram ražošanas maršrutam, ko iestatāt.</span><span class="sxs-lookup"><span data-stu-id="95945-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="95945-140">Maršruts parāda ceļu, ko krājums veic no vienas operācijas uz citu, no ražošanas procesa sākuma līdz pat beigām.</span><span class="sxs-lookup"><span data-stu-id="95945-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="95945-141">**Izmaksu kategorijas** — iestatiet izmaksu kategorijas, lai definētu stundas izmaksas noteiktiem procesiem un sagatavošanas laikiem.</span><span class="sxs-lookup"><span data-stu-id="95945-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="95945-142">**Izmaksu grupas** — iestatiet izmaksu grupas, lai izveidotu un uzturētu dažādus izmaksu aprēķināšanas tipus.</span><span class="sxs-lookup"><span data-stu-id="95945-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="95945-143">**Maršrutu grupas** — iestatiet maršrutu grupas, lai definētu parametrus, kas ir saistīti ar maršrutu grupām.</span><span class="sxs-lookup"><span data-stu-id="95945-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="95945-144">Maršrutu grupas ir jāiestata pirms ražošanas maršrutu izveidošanas.</span><span class="sxs-lookup"><span data-stu-id="95945-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="95945-145">**Maršruti** — iestatiet ražošanas maršrutus un definējiet noklusējuma iestatījumus, lai kontrolētu plānošanu, izmaksu aprēķināšanu, un maršruta operāciju cenu noteikšanu, kā arī lai kontrolētu progresa atskaišu izveidi.</span><span class="sxs-lookup"><span data-stu-id="95945-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="95945-146">**Maršruti** — iestatiet maršruta versijas, lai ražošanā iespējotu krājumu variācijas.</span><span class="sxs-lookup"><span data-stu-id="95945-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="95945-147">Neobligātie papildu iestatījumi</span><span class="sxs-lookup"><span data-stu-id="95945-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="95945-148">**Ražošanas grupas** — iestatiet ražošanas grupas, lai izveidotu relācijas starp ražošanas pasūtījumu un virsgrāmatas kontiem.</span><span class="sxs-lookup"><span data-stu-id="95945-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="95945-149">Virsgrāmatas konti tiek izmantoti, lai pasūtījumus grāmatotu vai tos grupētu atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="95945-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="95945-150">**Ražošanas kopas** — izveidojiet ražošanas pūlus, lai grupētu ražošanas pasūtījumus; šādi varat apstrādāt steidzamus ražošanas pasūtījumus vai dzēst un grāmatot pasūtījumu grupas.</span><span class="sxs-lookup"><span data-stu-id="95945-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="95945-151">**Rekvizīti** — definējiet rekvizītus, lai izveidotu īpašus atribūtus, kurus varat piešķirt saviem resursiem, lai kontrolētu ražošanas secību.</span><span class="sxs-lookup"><span data-stu-id="95945-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="95945-152">Šie atribūti ir savienoti ar darba laiku veidni.</span><span class="sxs-lookup"><span data-stu-id="95945-152">These attributes are connected to the working time template.</span></span>





