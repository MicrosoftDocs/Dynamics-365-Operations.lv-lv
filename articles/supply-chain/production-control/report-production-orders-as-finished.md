---
title: Ziņošana par ražošanas pasūtījumu pabeigšanu
description: “Ziņot kā pabeigtu” ir ražošanas posms. Šī posma ietvaros tiek ziņots par preces pabeigšanu un tā tiek pārvietota no ražošanas pasūtījuma uz krājumiem.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61c12ee3a831abcb46af18645eba55fe100c99c9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "315824"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="0e93c-104">Ziņošana par ražošanas pasūtījumu pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="0e93c-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e93c-105">“Ziņot kā pabeigtu” ir ražošanas posms.</span><span class="sxs-lookup"><span data-stu-id="0e93c-105">Report as finished is a production stage.</span></span> <span data-ttu-id="0e93c-106">Šī posma ietvaros tiek ziņots par preces pabeigšanu un tā tiek pārvietota no ražošanas pasūtījuma uz krājumiem.</span><span class="sxs-lookup"><span data-stu-id="0e93c-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="0e93c-107">Kad pabeigto preču daudzumu ražošanas pasūtījumā reģistrē kā pabeigtu, tiek atjaunināts rīcībā esošo krājumu daudzums.</span><span class="sxs-lookup"><span data-stu-id="0e93c-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="0e93c-108">Daļējos daudzumus sākotnēji plānotajā pasūtījuma daudzumā var reģistrēt kā pabeigtus.</span><span class="sxs-lookup"><span data-stu-id="0e93c-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="0e93c-109">Reģistrējot daudzumus kā pabeigtus, ir iespējams arī ziņot par kļūdainiem daudzumiem, norādot saistīto kļūdu pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="0e93c-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="0e93c-110">Kad ražošanas pasūtījums sasniedz stadiju Fiziski pabeigts, tas nozīmē, ka par pārējiem daudzumiem ražošanas pasūtījumā netiks ziņots.</span><span class="sxs-lookup"><span data-stu-id="0e93c-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="0e93c-111">Šīs īpašības arī saistītas ar procesu **Reģistrēt pabeigšanu**:</span><span class="sxs-lookup"><span data-stu-id="0e93c-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="0e93c-112">Ir iespējams iestatīt izejmateriālu patēriņu un laiku, kas ir proporcionāls paziņotajam daudzumam (reversā norakstīšana)</span><span class="sxs-lookup"><span data-stu-id="0e93c-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="0e93c-113">Izvietošanas darbu var izveidot krājumiem, kas ir iespējoti noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="0e93c-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="0e93c-114">Pabeigto preču plānoto vai standarta izmaksu vērtību var iestatīt tā, lai tā tiktu ziņota Virsgrāmatas kontiem.</span><span class="sxs-lookup"><span data-stu-id="0e93c-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="0e93c-115">Kvalitātes pārbaudes pasūtījumu var izveidot paziņotajam daudzumam, pamatojoties uz kvalitātes piesaistes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="0e93c-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="0e93c-116">Daudzums tiek ziņots ražojuma novietojumam.</span><span class="sxs-lookup"><span data-stu-id="0e93c-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="0e93c-117">Pēc tam tiek ģenerēts noliktavas darbs, lai pārvietotu daudzumu no ražojuma novietojuma uz galamērķi, ko nosaka izvietošanas darba novietojuma direktīva.</span><span class="sxs-lookup"><span data-stu-id="0e93c-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="0e93c-118">Kvalitātes pārbaudes pasūtījumu var izveidot, kad ražošanas pasūtījums ir reģistrēts kā pabeigts, ja ir iestatīta kvalitātes piesaiste.</span><span class="sxs-lookup"><span data-stu-id="0e93c-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="0e93c-119">Ražošanas pasūtījuma iestatīšana uz Fiziski pabeigts</span><span class="sxs-lookup"><span data-stu-id="0e93c-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="0e93c-120">Ražošanas pasūtījumu var iestatīt uz statusu **Fiziski pabeigts**, izmantojot standarta ražošanas pasūtījuma atjaunināšanas funkciju, vai maršrutu un darba karšu žurnālus, vai žurnālu **Fiziski pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e93c-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="0e93c-121">Jūs varat arī atjaunināt stadiju uz **Fiziski pabeigts**, izmantojot darbu karšu terminālu un darbu karšu ierīces lapas, sniedzot pārskatu par pēdējo ražošanas pasūtījuma darbu.</span><span class="sxs-lookup"><span data-stu-id="0e93c-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="0e93c-122">Visbeidzot, jūs varat iespējot opciju **Fiziski pabeigts** kā rokas noliktavas ierīces risinājuma procesu.</span><span class="sxs-lookup"><span data-stu-id="0e93c-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  



