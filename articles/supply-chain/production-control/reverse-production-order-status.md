---
title: "Ražošanas pasūtījuma statusa atsaukšana"
description: "Šajā tēmā ir aprakstīts, kā atsaukt ražošanas pasūtījuma statusu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="b3bb1-103">Ražošanas pasūtījuma statusa atsaukšana</span><span class="sxs-lookup"><span data-stu-id="b3bb1-103">Reverse the production order status</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b3bb1-104">Šajā tēmā ir aprakstīts, kā atsaukt ražošanas pasūtījuma statusu.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="b3bb1-105">Ja atsaucat ražošanas pasūtījuma statusu, pasūtījums un visas ar maršrutiem saistītās operācijas tiek pārnesti atpakaļ uz iepriekšējo ražošanas dzīves cikla posmu.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="b3bb1-106">Pieņemsim, ka ražošanas pasūtījuma statuss ir **Ieplānots** un jūs maināt statusu atpakaļ uz **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="b3bb1-107">Šādā gadījumā sistēmā statuss vispirms ir jāmaina uz **Novērtēts**, kas ir iepriekšējais statuss pirms statusa **Ieplānots**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="b3bb1-108">Pēc tam sistēmā statuss var tikt mainīts uz vajadzīgo statusu **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="b3bb1-109">**Piezīme.** Ja pasūtījuma statuss jau ir **Reģistrēt pabeigšanu**, joprojām varat to atsaukt un atjaunot kādu no iepriekšējiem statusiem.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="b3bb1-110">Taču ir vēlreiz jāveic novērtēšana un operāciju plānošana vai darbu plānošana, vai abu veidu plānošana, lai atjauninātu pasūtījumā ietverto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="b3bb1-111">Šī darbība ir obligāti jāveic, jo ir jāatiestata arī visas atlikušā krājumu patēriņa un operācijas resursu patēriņa rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="b3bb1-112">Šī raksta turpinājumā ir paskaidrots, kas notiek, kad atsaucat ražošanas pasūtījuma statusu tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="b3bb1-113">No **Novērtēts** uz **Izveidots**</span><span class="sxs-lookup"><span data-stu-id="b3bb1-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="b3bb1-114">No **Ieplānots** uz **Novērtēts**</span><span class="sxs-lookup"><span data-stu-id="b3bb1-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="b3bb1-115">No **Izlaists** uz **Ieplānots**</span><span class="sxs-lookup"><span data-stu-id="b3bb1-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="b3bb1-116">No **Sākts** uz **Izlaists**</span><span class="sxs-lookup"><span data-stu-id="b3bb1-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="b3bb1-117">No Novērtēts uz Izveidots</span><span class="sxs-lookup"><span data-stu-id="b3bb1-117">From Estimated to Created</span></span>
<span data-ttu-id="b3bb1-118">Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Ieplānots** uz **Izveidots**, tiek noņemts krājumu patēriņš, kas krājumiem tika aprēķināts materiālu komplektā (MK).</span><span class="sxs-lookup"><span data-stu-id="b3bb1-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="b3bb1-119">Tiek dzēstas krājumu transakcijas ražošanas rindā, un ražošanas pasūtījuma MK rindās lauka **Nepabeigtā pasūtījuma statuss** vērtība tiek atiestatīta uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="b3bb1-120">Ja ir atlasītas opcijas **Atvasinātie pirkšanas pasūtījumi** un **Atvasinātā ražošana**, tiek dzēsti visi pamata pirkšanas pasūtījumi vai ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="b3bb1-121">Ja novērtējāt ražošanas pasūtījuma izmaksas vai manuāli rezervējāt krājumus, lai tos varētu izmantot ražošanā, šīs transakcijas tiek noņemtas.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="b3bb1-122">No Ieplānots uz Novērtēts</span><span class="sxs-lookup"><span data-stu-id="b3bb1-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="b3bb1-123">Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Ieplānots** uz **Novērtēts**, tiek noņemti ieplānotie sākuma un beigu datumi un laiks.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="b3bb1-124">Tiek noņemtas plānošanas laikā veiktās noslodzes rezervācijas, un tiek dzēsti darbu plānošanas laikā izveidotie darbi.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="b3bb1-125">Tiek atiestatīta visa lapā **Ražošanas pasūtījumu informācija** reģistrētā informācija par operāciju plānošanu un darbu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="b3bb1-126">No Izlaists uz Ieplānots</span><span class="sxs-lookup"><span data-stu-id="b3bb1-126">From Released to Scheduled</span></span>
<span data-ttu-id="b3bb1-127">Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Izlaists** uz **ieplānots**, tiek mainīta vienīgi statusa lauka vērtība.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="b3bb1-128">No Sākts uz Izlaists</span><span class="sxs-lookup"><span data-stu-id="b3bb1-128">From Started to Released</span></span>
<span data-ttu-id="b3bb1-129">Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Sākts** uz **Izlaists**, tiek atsaukts visu to krājumu statuss, kas ir reģistrēti kā pabeigti.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="b3bb1-130">Ja materiāls ir izdots vai ir veikta ieejošā vai izejošā piegāde ražošanai, šie iestatījumi tiek atsaukti.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="b3bb1-131">Ražošanas pasūtījuma MK rindu lauka**Nepabeigtā pasūtījuma statuss** tiek mainīts no **Pabeigts** uz **Materiālu patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="b3bb1-132">Ja operācijām ražošanas maršrutā ir reģistrēts laiks vai daudzumi ir reģistrēti kā pabeigti, šie iestatījumi tiek atsaukti.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="b3bb1-133">Ražošanas maršruta lauka**Nepabeigtā pasūtījuma statuss** tiek mainīts no **Pabeigts** uz **Maršruta patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="b3bb1-134">Tiek atsaukti visu to krājumu iestatījumi, kas ir grāmatoti kā notiekošs process vai nepabeigtā ražošana.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="b3bb1-135">Lapā **Ražošanas pasūtījumu informācija** tiek atiestatīti lauki, kuros ir redzams daudzums, kas ir sākts vai reģistrēts kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="b3bb1-136">Tiek atiestatīti arī šo transakciju datumi.</span><span class="sxs-lookup"><span data-stu-id="b3bb1-136">The dates for those transactions are also reset.</span></span>




