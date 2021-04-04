---
title: Ražošanas pasūtījumu nodošana izpildei
description: Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem.
author: johanhoffmann
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ee20983209b9900037a46d56b6213d47bf852e4
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487703"
---
# <a name="release-production-orders"></a><span data-ttu-id="5e53a-104">Ražošanas pasūtījumu nodošana izpildei</span><span class="sxs-lookup"><span data-stu-id="5e53a-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e53a-105">Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="5e53a-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="5e53a-106">Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="5e53a-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="5e53a-107">Stāvokļa Izlaists raksturojums</span><span class="sxs-lookup"><span data-stu-id="5e53a-107">Characteristics of the Released state</span></span>

<span data-ttu-id="5e53a-108">Stāvoklis **Izlaists** ir viens no ražošanas pasūtījuma dzīves cikla stāvokļiem.</span><span class="sxs-lookup"><span data-stu-id="5e53a-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="5e53a-109">Ražošanas pasūtījumi, kuru stāvoklis ir **Izlaists**, ir pieejami izpildei ražotnē un noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="5e53a-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="5e53a-110">Tālāk ir norādītas stāvokļa **Izlaists** raksturīpašības.</span><span class="sxs-lookup"><span data-stu-id="5e53a-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="5e53a-111">Ražošanas pasūtījuma stāvokli var mainīt uz **Izlaists**, izmantojot ražošanas pasūtījumu vai pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="5e53a-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="5e53a-112">Ražošanas pasūtījumu var arī automātiski atjaunināt, izmantojot plānotos ražošanas pasūtījumus, kas ir apstiprināti, izmantojot lauku **Apstiprināšanas periods** lapā **Vispārējais plāns**.</span><span class="sxs-lookup"><span data-stu-id="5e53a-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="5e53a-113">Stāvoklis **Izlaists** norāda ražotnes operatoriem (operatoriem), ka viņi var sākt ražošanas darbu izpildi ražotnē.</span><span class="sxs-lookup"><span data-stu-id="5e53a-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="5e53a-114">Ražošanas dokumenti, piemēram, maršrutu kartes, maršrutu darbi, un darbu kartes, sniedz informāciju par ražošanas darbiem, un tos var izsniegt.</span><span class="sxs-lookup"><span data-stu-id="5e53a-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="5e53a-115">Materiāliem, kas ir fiziski rezervēti, tiek ģenerēts noliktavas darbs, lai izdotu materiālus ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="5e53a-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="5e53a-116">Darbu izlaišana izpildei ražotnē</span><span class="sxs-lookup"><span data-stu-id="5e53a-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="5e53a-117">Kad ražošanas pasūtījums ir izlaists, ar to saistītie ražošanas darbi ir redzami un pieejami reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="5e53a-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="5e53a-118">Operatori var reģistrēt darbus, piemēram, Sākt, Apturēt, Pabeigšana, lapā **Darbu karšu terminālis** vai **Darbu kartes ierīce**.</span><span class="sxs-lookup"><span data-stu-id="5e53a-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="5e53a-119">Reģistrētie laika un daudzuma dati tiek automātiski pārsūtīti no reģistrācijas lapas uz ražošanas žurnāliem, lai sekotu līdzi laika un resursu patēriņam.</span><span class="sxs-lookup"><span data-stu-id="5e53a-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="5e53a-120">Maršruta kartes</span><span class="sxs-lookup"><span data-stu-id="5e53a-120">Route cards</span></span>

<span data-ttu-id="5e53a-121">Maršruta karte nodrošina pārskatu par informāciju no maršruta, operācijas iestatījumiem un operāciju un darbu plānošanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="5e53a-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="5e53a-122">Maršruta darbi</span><span class="sxs-lookup"><span data-stu-id="5e53a-122">Route jobs</span></span>

<span data-ttu-id="5e53a-123">Maršruta darbs sniedz detalizētu informāciju par katru operācijas darbu, un tajā ir ietverti iestatīšanas, procesa, gaidīšanas un transportēšanas laiki.</span><span class="sxs-lookup"><span data-stu-id="5e53a-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="5e53a-124">Piemēram, tādai operācijai kā krāsošana var būt nepieciešami atsevišķi darbi, piemēram iestatīšanas laiks, izpildes laiks krāsošanas procesam un gaidīšanas laiks žāvēšanai.</span><span class="sxs-lookup"><span data-stu-id="5e53a-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="5e53a-125">Darba kartes</span><span class="sxs-lookup"><span data-stu-id="5e53a-125">Job cards</span></span>

<span data-ttu-id="5e53a-126">Darbu kartē ir norādīti noteiktas operācijas atsevišķo darbu numuri.</span><span class="sxs-lookup"><span data-stu-id="5e53a-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="5e53a-127">Katrā lapā ir redzams viens darbs.</span><span class="sxs-lookup"><span data-stu-id="5e53a-127">One job appears on each page.</span></span> <span data-ttu-id="5e53a-128">Darba kartē iekļautie darbi un to paredzami laiki tiek ņemti no maršruta un operācijas iestatīšanas informācijas.</span><span class="sxs-lookup"><span data-stu-id="5e53a-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="5e53a-129">Darbu kartē varat atvērt lapu **Ražošanas žurnāla rindas**, **darbu karte**.</span><span class="sxs-lookup"><span data-stu-id="5e53a-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="5e53a-130">Darbinieki, kas strādā ar operācijas resursiem, var sniegt atsauksmes par ražošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5e53a-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="5e53a-131">Šeit ir lauki, kur varat ievadīt patēriņa statistiku un tādu informāciju kā kļūdu daudzums.</span><span class="sxs-lookup"><span data-stu-id="5e53a-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="5e53a-132">Noliktavas darba izejmateriālu izdošanai</span><span class="sxs-lookup"><span data-stu-id="5e53a-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="5e53a-133">Izlaišanas laikā tiek ģenerēts izejmateriālu izdošanas darbs.</span><span class="sxs-lookup"><span data-stu-id="5e53a-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="5e53a-134">Darbs tiek ģenerēts tikai tam materiālu daudzumam, kas tika fiziski rezervēts ražošanas pasūtījumam pirms pasūtījuma nodošanas izpildei.</span><span class="sxs-lookup"><span data-stu-id="5e53a-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="5e53a-135">Lai varētu ģenerēt noliktavas darbu izejmateriālu izdošanai, ir jāveic tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="5e53a-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="5e53a-136">Izejmateriālu izdošanas novietojuma direktīva, kas nosaka, kurā noliktavas novietojumā ir jāizdod materiāli</span><span class="sxs-lookup"><span data-stu-id="5e53a-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="5e53a-137">Izejmateriālu laidiena veidne, kur ir konfigurēti noliktavas darba izpildes ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="5e53a-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="5e53a-138">Ražošanas ievades novietojums, kas nosaka, kur materiāli tiek novietoti</span><span class="sxs-lookup"><span data-stu-id="5e53a-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="5e53a-139">Izmantojot noliktavas vienību, kas ir kontrolēti ar numura zīmi, var izvēlēties, vai pasūtītais daudzums vai viss krājumam pieejamais daudzums ir jāizņem, apstrādājot izejmateriālu izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="5e53a-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="5e53a-140">Lai to iestatītu:</span><span class="sxs-lookup"><span data-stu-id="5e53a-140">To set this option:</span></span>

1. <span data-ttu-id="5e53a-141">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Tirdzniecībā izlaistās preces** un atveriet attiecīgo krājumu.</span><span class="sxs-lookup"><span data-stu-id="5e53a-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="5e53a-142">Izvērsiet **Noliktava** kopsavilkuma cilni.</span><span class="sxs-lookup"><span data-stu-id="5e53a-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="5e53a-143">Atlasiet vienu no šīm opcijām **Materiālu izdošanas noliktavas vienību novietojumu** laukā:</span><span class="sxs-lookup"><span data-stu-id="5e53a-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="5e53a-144">*Pasūtījuma izdošana*: Jāpaņem tikai pasūtītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="5e53a-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="5e53a-145">*Sagatavošana*: Ja iespējams, ir jāpaņem viss noliktavas vienībā pieejamais daudzums.</span><span class="sxs-lookup"><span data-stu-id="5e53a-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="5e53a-146">Lai darbinieks varētu saņemt visu noliktavas vienības daudzumu, noliktavai nav jāietver jaukti krājumi, un tai nedrīkst būt jauktas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5e53a-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="5e53a-147">Ja numura zīmi ietver jauktas dimensijas vai krājumus, izdošana tiks turpināta, it kā tā būtu iestatīta uz *Pasūtījuma izdošana*.</span><span class="sxs-lookup"><span data-stu-id="5e53a-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]