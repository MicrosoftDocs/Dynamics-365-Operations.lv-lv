---
title: Plānoto pasūtījumu uzturēšana
description: Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus. Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecda1c113a0663ff430aa15a0023668097078ad1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213818"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="c3bd4-104">Plānoto pasūtījumu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="c3bd4-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3bd4-105">Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="c3bd4-106">Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="c3bd4-107">Plānotos pasūtījumus var pārvaldīt no darbvietas **Vispārējā plānošana**, saraksta **Plānotais pasūtījums** vai saraksta **Plānotie ražošanas pasūtījumi**, **Plānotie pirkšanas pasūtījumi** un **Plānotā pārsūtīšana**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="c3bd4-108">Plānotā pasūtījuma statuss</span><span class="sxs-lookup"><span data-stu-id="c3bd4-108">Planned order status</span></span>
<span data-ttu-id="c3bd4-109">Lai sekotu norisei, varat izmantot lauku **Statuss**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="c3bd4-110">Tiek izmantotas šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-110">The following values are used:</span></span>

-   <span data-ttu-id="c3bd4-111">Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss **Neapstrādāts**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="c3bd4-112">Ja izvēlaties neapstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="c3bd4-113">Ja vēlaties apstiprināt plānoto pasūtījumu, varat mainīt statusu uz **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="c3bd4-114">Plānotos pasūtījumus ar statusu **Apstiprināts** ievēro vispārējā plānošana, tāpēc tie vēlākās galvenās plānošanas laikā netiek modificēti vai dzēsti.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="c3bd4-115">Lai to sasniegtu, plānošanas loģika kopē **Apstiprinātos** plānotos pasūtījumus no vecās plāna versijas uz jauno plāna versiju vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="c3bd4-116">Apstiprinot plānotos pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="c3bd4-116">Firming planned orders</span></span> 
<span data-ttu-id="c3bd4-117">Apstiprinot plānotos pasūtījumus, tiek izveidoti faktiskie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="c3bd4-118">Tie ir zināmi arī kā *Izlaistie* vai *Atvērtie pasūtījumi*.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="c3bd4-119">Kad plānotais pasūtījums apstiprināts, tas tiek pārvietots attiecīgā moduļa pasūtījumu sadaļai.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="c3bd4-120">No **Plānotie pasūtījumi** lapas varat atlasīt divas apstiprināšanas opcijas:</span><span class="sxs-lookup"><span data-stu-id="c3bd4-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="c3bd4-121">**Atstiprināt**— tas apstiprinās vienu vai vairākus atlasītos plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="c3bd4-122">**Apstiprināt visu**— tas apstiprinās visus plānotos pasūtījumus filtrā.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="c3bd4-123">Izmantojot **Apstiprināt visu** , nav jāatlasa plānotais pasūtījums, visi plānotie pasūtījumi filtrā tiks apstiprināti.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="c3bd4-124">Šī opcija var būt noderīga, ja jūs apstiprinājiet lielu skaitu plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="c3bd4-125">Jūs varat izsekot plānoto pasūtījumu, kas tika apstiprināts no **Apstiprināšanas vēsture** zem **Plānoto pasūtījumu forma > Skatīt > Apstiprināšanas vēsture.**</span><span class="sxs-lookup"><span data-stu-id="c3bd4-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="c3bd4-126">Veikt paralēlu apstiprināšanu</span><span class="sxs-lookup"><span data-stu-id="c3bd4-126">Parallelize firming</span></span>
<span data-ttu-id="c3bd4-127">Ja jūs plānojat apstiprināt daudzus pasūtījumus vienlaicīgi, paralēlā izpilde var uzlabot izpildes laiku vai veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="c3bd4-128">Šī opcija ir pieejama, apstiprinot vairākus plānotos pasūtījumus ar **Atstiprināt** vai **Apstiprināt visu**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="c3bd4-129">Ir pieejami šādi parametri:</span><span class="sxs-lookup"><span data-stu-id="c3bd4-129">The following parameters are available:</span></span>

-   <span data-ttu-id="c3bd4-130">**Paralēlā apstiprināšana** – ja **Jā**, apstiprināšanas process būs paralēls ar pavedienu skaitu, kas definēts **Pavedienu skaits** sadaļā.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="c3bd4-131">**Pavedienu skaits**— kontrolē pavedienu skaitu izmantoto, lai apstiprināšanas process būtu paralēls.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="c3bd4-132">Parametrs parādās tikai tad, ja **Paralēlā apstiprināšana** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="c3bd4-133">**Paralēla apstiprināšana** opcija tiek rādīta tikai tad, ja ir atlasīts vairāk nekā viens plānotais pasūtījums apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="c3bd4-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c3bd4-134">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c3bd4-134">Additional resources</span></span>
--------

[<span data-ttu-id="c3bd4-135">Vispārējo plānu pārskats</span><span class="sxs-lookup"><span data-stu-id="c3bd4-135">Master plans overview</span></span>](master-plans.md)



