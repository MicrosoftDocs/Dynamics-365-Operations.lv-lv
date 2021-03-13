---
title: Pasūtījuma operāciju atsaukšana punktā POS
description: Šajā tēmā ir paskaidrotas līdzekļa iespējas, kas pieejamas uzlabotajām pasūtījuma atsaukuma lapām punktā POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010078"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="627a7-103">Pasūtījuma operāciju atsaukšana punktā POS</span><span class="sxs-lookup"><span data-stu-id="627a7-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="627a7-104">Darbība **Pasūtījuma atsaukšana** Commerce pārdošanas punktā (POS) nodrošina atjauninātus pasūtījuma meklēšanas un filtrēšanas līdzekļus un ar pasūtījumu saistītu informāciju.</span><span class="sxs-lookup"><span data-stu-id="627a7-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="627a7-105">Šis līdzeklis ir pieejams Commerce versijās 10.0.15 un jaunākās.</span><span class="sxs-lookup"><span data-stu-id="627a7-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="627a7-106">Lai iespējotu šo funkcionalitāti ieslēdziet līdzekli **Uzlabota pasūtījuma operāciju atsaukšana punktā POS**, kas atrodas **Līdzekļu pārvaldība** darbvietā, programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="627a7-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="627a7-107">Pēc līdzekļa iespējošanas, apsveriet iespēju atjaunināt [ekrāna izkārtojumus](pos-screen-layouts.md) punktā POS, lai izmantotu dažas no mainītajām iespējām.</span><span class="sxs-lookup"><span data-stu-id="627a7-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="627a7-108">Operāciju pogas **Atsaukt pasūtījumu** konfigurēšana ļauj organizācijām izvietot operāciju ar iepriekš definētu displeju.</span><span class="sxs-lookup"><span data-stu-id="627a7-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Pogu rindas konfigurēšana](media/recallorderbuttongrid.png)

<span data-ttu-id="627a7-110">Displeja opcijas ir aprakstītas šeit.</span><span class="sxs-lookup"><span data-stu-id="627a7-110">The display options are as follows.</span></span>
- <span data-ttu-id="627a7-111">**Nav** – šī opcija izvieto operāciju bez noteikta displeja.</span><span class="sxs-lookup"><span data-stu-id="627a7-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="627a7-112">Kad lietotājs atver operāciju ar šo konfigurāciju, viņam tiks piedāvāts meklēt un atrast pasūtījumus vai izvēlēties no iepriekš definēta pasūtījumu filtra.</span><span class="sxs-lookup"><span data-stu-id="627a7-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="627a7-113">**Izpildāmie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu veikalā izpildāmo pasūtījumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="627a7-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="627a7-114">Šie pasūtījumi ir konfigurēti saņemšanai veikalā vai veikala sūtījumiem, un šo pasūtījumu rindas vēl nav izdotas vai iepakotas.</span><span class="sxs-lookup"><span data-stu-id="627a7-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="627a7-115">**Izdodamie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu sarakstu ar pasūtījumiem, kuri ir konfigurēti saņemšanai lietotāja pašreizējā veikalā.</span><span class="sxs-lookup"><span data-stu-id="627a7-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="627a7-116">**Nosūtāmie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu sarakstu ar pasūtījumiem, kuri ir konfigurēti nosūtīšanai no lietotāja pašreizējā veikala.</span><span class="sxs-lookup"><span data-stu-id="627a7-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="627a7-117">Uzsākot **Atsaukt pasūtījumu** operāciju no punkta POS, ja displejs ir konfigurēts uz **Nav**, lietotājs varēs meklēt un izgūt pasūtījumus vienā no tālāk norādītajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="627a7-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="627a7-118">Skenēt pasūtījumu svītrkodus.</span><span class="sxs-lookup"><span data-stu-id="627a7-118">Scan order barcodes.</span></span> <span data-ttu-id="627a7-119">Šādā veidā tiks meklētas atbilstības pasūtījuma numura, kanāla atsauces un saņemšanas ID laukos.</span><span class="sxs-lookup"><span data-stu-id="627a7-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="627a7-120">Lai izmantotu filtrēšanas mehānismu un atrastu pasūtījumus, kas atbilst filtrēšanas kritērijiem, atlasiet **Meklēt pasūtījumus** vai **Meklēt un filtrēt** ikonu, kas atrodas AppBar.</span><span class="sxs-lookup"><span data-stu-id="627a7-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="627a7-121">Nolaižamajā izvēlnē **Rādīt pasūtījumus** izvēlieties kādu no iepriekš definētajiem filtriem (izpildāmie pasūtījumi, izdodamie pasūtījumi vai nosūtāmie pasūtījumi).</span><span class="sxs-lookup"><span data-stu-id="627a7-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="627a7-123">Pēc meklēšanas kritēriju piemērošanas programmā tiks parādīts atbilstošo pārdošanas pasūtījumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="627a7-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="627a7-125">Lietotājs sarakstā var atlasīt pasūtījumu, lai skatītu papildu informāciju.</span><span class="sxs-lookup"><span data-stu-id="627a7-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="627a7-126">Informācijas panelī ekrāna labajā pusē tiek parādīta atlasītā pasūtījuma specifika, ieskaitot pasūtījuma rindas informāciju, piegādes informāciju un izpildes informāciju.</span><span class="sxs-lookup"><span data-stu-id="627a7-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="627a7-127">Lietotājs var atlasīt operāciju no AppBar.</span><span class="sxs-lookup"><span data-stu-id="627a7-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="627a7-128">Atkarībā no pasūtījuma statusa, atsevišķas operācijas var nebūt iespējotas.</span><span class="sxs-lookup"><span data-stu-id="627a7-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="627a7-129">**Atgriezt** – izpilda atgriešanu vienam vai vairākiem rēķiniem, kas saistīti ar atlasīto debitora pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="627a7-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="627a7-130">**Atcelt** – izpilda atlasītā pārdošanas pasūtījuma pilnīgu atcelšanu.</span><span class="sxs-lookup"><span data-stu-id="627a7-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="627a7-131">**Izpildīt** – pārsūta lietotāju uz pasūtījuma izpildes lapu, kas tiks iepriekš filtrēta atlasītajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="627a7-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="627a7-132">Tiks parādītas tikai tās pasūtījuma rindas, kas ir atvērtas, lai lietotāja veikals varētu izpildīt atlasīto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="627a7-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="627a7-133">**Rediģēt** – ļauj lietotājiem veikt izmaiņas atlasītajā debitora pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="627a7-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="627a7-134">**Izdot** – uzsāk izdošanas plūsmu, kas ļauj lietotājam izvēlēties saņemamās preces un izveido izdošanas pārdošanas transakciju.</span><span class="sxs-lookup"><span data-stu-id="627a7-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
