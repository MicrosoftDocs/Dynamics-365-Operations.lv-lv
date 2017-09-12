---
title: "Ražošanas pasūtījumu nodošana izpildei"
description: "Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa38c50a58bed5702332182b9e0827b863f536f7
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="release-production-orders"></a><span data-ttu-id="9e382-104">Ražošanas pasūtījumu nodošana izpildei</span><span class="sxs-lookup"><span data-stu-id="9e382-104">Release production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e382-105">Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9e382-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="9e382-106">Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="9e382-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="9e382-107">Stāvokļa Izlaists raksturojums</span><span class="sxs-lookup"><span data-stu-id="9e382-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="9e382-108">Stāvoklis **Izlaists** ir viens no ražošanas pasūtījuma dzīves cikla stāvokļiem.</span><span class="sxs-lookup"><span data-stu-id="9e382-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="9e382-109">Ražošanas pasūtījumi, kuru stāvoklis ir **Izlaists**, ir pieejami izpildei ražotnē un noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="9e382-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="9e382-110">Tālāk ir norādītas stāvokļa **Izlaists** raksturīpašības.</span><span class="sxs-lookup"><span data-stu-id="9e382-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="9e382-111">Ražošanas pasūtījuma stāvokli var mainīt uz **Izlaists**, izmantojot ražošanas pasūtījumu vai pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="9e382-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="9e382-112">Ražošanas pasūtījumu var arī automātiski atjaunināt, izmantojot plānotos ražošanas pasūtījumus, kas ir apstiprināti, izmantojot lauku **Apstiprināšanas periods** lapā **Vispārējais plāns**.</span><span class="sxs-lookup"><span data-stu-id="9e382-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="9e382-113">Stāvoklis **Izlaists** norāda ražotnes operatoriem (operatoriem), ka viņi var sākt ražošanas darbu izpildi ražotnē.</span><span class="sxs-lookup"><span data-stu-id="9e382-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="9e382-114">Ražošanas dokumenti, piemēram, maršrutu kartes, maršrutu darbi, un darbu kartes, sniedz informāciju par ražošanas darbiem, un tos var izsniegt.</span><span class="sxs-lookup"><span data-stu-id="9e382-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="9e382-115">Materiāliem, kas ir fiziski rezervēti, tiek ģenerēts noliktavas darbs, lai izdotu materiālus ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="9e382-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="9e382-116">Darbu izlaišana izpildei ražotnē</span><span class="sxs-lookup"><span data-stu-id="9e382-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="9e382-117">Kad ražošanas pasūtījums ir izlaists, ar to saistītie ražošanas darbi ir redzami un pieejami reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="9e382-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="9e382-118">Operatori var reģistrēt darbus, piemēram, Sākt, Apturēt, Pabeigšana, lapā **Darbu karšu terminālis** vai **Darbu kartes ierīce**.</span><span class="sxs-lookup"><span data-stu-id="9e382-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="9e382-119">Reģistrētie laika un daudzuma dati tiek automātiski pārsūtīti no reģistrācijas lapas uz ražošanas žurnāliem, lai sekotu līdzi laika un resursu patēriņam.</span><span class="sxs-lookup"><span data-stu-id="9e382-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="9e382-120">Maršruta kartes</span><span class="sxs-lookup"><span data-stu-id="9e382-120">Route cards</span></span>
<span data-ttu-id="9e382-121">Maršruta karte nodrošina pārskatu par informāciju no maršruta, operācijas iestatījumiem un operāciju un darbu plānošanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="9e382-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="9e382-122">Maršruta darbi</span><span class="sxs-lookup"><span data-stu-id="9e382-122">Route jobs</span></span>
<span data-ttu-id="9e382-123">Maršruta darbs sniedz detalizētu informāciju par katru operācijas darbu, un tajā ir ietverti iestatīšanas, procesa, gaidīšanas un transportēšanas laiki.</span><span class="sxs-lookup"><span data-stu-id="9e382-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="9e382-124">Piemēram, tādai operācijai kā krāsošana var būt nepieciešami atsevišķi darbi, piemēram iestatīšanas laiks, izpildes laiks krāsošanas procesam un gaidīšanas laiks žāvēšanai.</span><span class="sxs-lookup"><span data-stu-id="9e382-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="9e382-125">Darba kartes</span><span class="sxs-lookup"><span data-stu-id="9e382-125">Job cards</span></span>
<span data-ttu-id="9e382-126">Darbu kartē ir norādīti noteiktas operācijas atsevišķo darbu numuri.</span><span class="sxs-lookup"><span data-stu-id="9e382-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="9e382-127">Katrā lapā ir redzams viens darbs.</span><span class="sxs-lookup"><span data-stu-id="9e382-127">One job appears on each page.</span></span> <span data-ttu-id="9e382-128">Darba kartē iekļautie darbi un to paredzami laiki tiek ņemti no maršruta un operācijas iestatīšanas informācijas.</span><span class="sxs-lookup"><span data-stu-id="9e382-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="9e382-129">Darbu kartē varat atvērt lapu **Ražošanas žurnāla rindas**, **darbu karte**.</span><span class="sxs-lookup"><span data-stu-id="9e382-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="9e382-130">Darbinieki, kas strādā ar operācijas resursiem, var sniegt atsauksmes par ražošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="9e382-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="9e382-131">Šeit ir lauki, kur varat ievadīt patēriņa statistiku un tādu informāciju kā kļūdu daudzums.</span><span class="sxs-lookup"><span data-stu-id="9e382-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="9e382-132">Izejmateriālu izdošanas noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="9e382-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="9e382-133">Izlaišanas laikā tiek ģenerēts izejmateriālu izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="9e382-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="9e382-134">Darbs tiek ģenerēts tikai tam materiālu daudzumam, kas tika fiziski rezervēts ražošanas pasūtījumam pirms pasūtījuma nodošanas izpildei.</span><span class="sxs-lookup"><span data-stu-id="9e382-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="9e382-135">Lai varētu ģenerēt noliktavas darbu izejmateriālu izdošanai, ir jāveic tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="9e382-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="9e382-136">Izejmateriālu izdošanas novietojuma direktīva, kas nosaka, kurā noliktavas novietojumā ir jāizdod materiāli</span><span class="sxs-lookup"><span data-stu-id="9e382-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="9e382-137">Izejmateriālu laidiena veidne, kur ir konfigurēti noliktavas darba izpildes ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="9e382-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="9e382-138">Ražošanas ievades novietojums, kas nosaka, kur materiāli tiek novietoti</span><span class="sxs-lookup"><span data-stu-id="9e382-138">A production input location that determines where materials are put</span></span>





