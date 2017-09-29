--- 
title: "Izvietojuma kodu iestatīšana"
description: "Šī procedūra fokusējas uz atgriešanas metodes koda iestatīšanu, ko var izmantot mobilā ierīcē atgriezto pasūtījumu saņemšanas procesam."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c004543188656dfd53d7539717cd6e93d0b9f47a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="c47f2-103">Izvietojuma kodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c47f2-103">Set up dispositions codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c47f2-104">Šī procedūra fokusējas uz atgriešanas metodes koda iestatīšanu, ko var izmantot mobilā ierīcē atgriezto pasūtījumu saņemšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="c47f2-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="c47f2-105">Atgriešanas metodes kodi ir noteikumu kopums, kas tiek izmantots, kad tiek saņemti krājumi.</span><span class="sxs-lookup"><span data-stu-id="c47f2-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="c47f2-106">Piemēram, kad darba lietotājs izmanto mobilo ierīci, lai saņemtu krājumus, kas tika bojāti, lietotājam jānoskenē bojāto krājumu atgriešanas metodes kods.</span><span class="sxs-lookup"><span data-stu-id="c47f2-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="c47f2-107">Saņemto preču krājumu statusu, darba veidni un novietojuma direktīvu var noteikt pēc skenēta atgriešanas metodes koda.</span><span class="sxs-lookup"><span data-stu-id="c47f2-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="c47f2-108">Pirkšanas pasūtījuma saņemšanas procesam un ražošanas pasūtījuma pārskatam kā pabeigtam procesam atgriešanas metodes koda izmantošana nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="c47f2-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="c47f2-109">Pārdošanas pasūtījuma atgriešanas saņemšanas procesam, ja krājumi ir reģistrēti, izmantojot mobilo ierīci, atgriešanas metodes koda izmantošana ir obligāta.</span><span class="sxs-lookup"><span data-stu-id="c47f2-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="c47f2-110">Šajā ceļvedī tiek izmantoti demonstrācijas uzņēmuma USMF dati.</span><span class="sxs-lookup"><span data-stu-id="c47f2-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="c47f2-111">Šī procedūra ir paredzēta noliktavas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="c47f2-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="c47f2-112">Pārejiet uz sadaļu Noliktavas pārvaldība > Iestatījumi > Mobilā ierīce > Izvietojuma kodi.</span><span class="sxs-lookup"><span data-stu-id="c47f2-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="c47f2-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c47f2-113">Click New.</span></span>
    * <span data-ttu-id="c47f2-114">Izveidojiet jaunu atgriešanas metodes kodu, lai izmantotu debitora atgrieztajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="c47f2-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="c47f2-115">Laukā Atgriešanas metodes kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c47f2-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="c47f2-116">Laukā Krājumu statuss atlasiet krājumu statusu, kur pastāv krājuma bloķēšana.</span><span class="sxs-lookup"><span data-stu-id="c47f2-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="c47f2-117">Ja jūs izmantojat USMF, atlasiet "Bloķēšana".</span><span class="sxs-lookup"><span data-stu-id="c47f2-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="c47f2-118">Jūs varat pievienot krājumu statusu atgriešanas metodes kodam, lai ignorētu noklusējuma statusu, kas ir pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="c47f2-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="c47f2-119">Laukā Darba veidne ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c47f2-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="c47f2-120">Nav obligāti: atlasiet darba veidnes kodu, kas ir saistīts ar atgriešanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c47f2-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="c47f2-121">Ja vērtības nav, darba veidne tiks atrisināta, izmantojot standarta noteikumus, kas konfigurēti jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c47f2-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="c47f2-122">Darba veidnes izvēle ierobežos procesus, ar kuriem var izmantot šo atgriešanas metodes kodu.</span><span class="sxs-lookup"><span data-stu-id="c47f2-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="c47f2-123">Piemēram, ja atgriešanas metodes kodam ir darba veidne ar darba pasūtījumu ar tipu pirkšanas pasūtījums, to nevar izmantot, lai reģistrētu krājumus, ko atgriež debitori.</span><span class="sxs-lookup"><span data-stu-id="c47f2-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="c47f2-124">Laukā Atgriešanas metodes kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c47f2-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="c47f2-125">Atgriešanas metodes kods nosaka atlikušo atgriešanas pasūtījuma procesu reģistrētiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="c47f2-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="c47f2-126">Šajā piemērā klientam jāsaņem kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="c47f2-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="c47f2-127">Pievienojiet atgriešanas metodes kodu, kuras satur darbību Kredīts.</span><span class="sxs-lookup"><span data-stu-id="c47f2-127">Add a returns disposition code that contains an action Credit.</span></span>  


