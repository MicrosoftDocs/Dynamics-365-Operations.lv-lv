---
title: Vienības izdošanas apstiprinājums
description: Šajā tēmā ir aprakstīts, kā jūs varat iestatīt un lietot vienību izdošanas apstiprināšanas funkciju mobilajā ierīcē.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed63245066799d7d8f14362ab6c9193c0cda7c4a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432657"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="6b212-103">Vienības izdošanas apstiprinājums</span><span class="sxs-lookup"><span data-stu-id="6b212-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b212-104">Vienības izdošana ļauj apstiprināt katru krājuma vienību, izmantojot izdošanas vai inventarizācijas darbu mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="6b212-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="6b212-105">Attiecībā uz izdodamo vienību varat pārbaudīt apstrādājamo darba daudzumu vai izdodamo daudzumu, kas norādīts darbā.</span><span class="sxs-lookup"><span data-stu-id="6b212-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="6b212-106">Attiecībā uz inventarizācijas darbu varat skenēt krājumu, kas tiek uzskaitīts, un izsekot kopsummu.</span><span class="sxs-lookup"><span data-stu-id="6b212-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="6b212-107">Iespējojot vienības izdošanu, preču apstiprinājums tiek automātiski atlasīts.</span><span class="sxs-lookup"><span data-stu-id="6b212-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="6b212-108">Attiecībā uz darba veida izdošanu ir iespējots maksimālais vienību skaits.</span><span class="sxs-lookup"><span data-stu-id="6b212-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="6b212-109">Tādējādi var iestatīt maksimālo vienību skaitu, kas ir jāapstiprina darba procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="6b212-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="6b212-110">Maksimālais daudzums ir atkarīgs no pašreizējās darba vienības, kas tiek apstrādāta.</span><span class="sxs-lookup"><span data-stu-id="6b212-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="6b212-111">Inventarizācijas darba veidā nav atļauts maksimālais daudzums.</span><span class="sxs-lookup"><span data-stu-id="6b212-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="6b212-112">Var izmantot arī daudzumu un mērvienību (UOM), kas saistīta ar skenēto svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="6b212-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="6b212-113">Tas darbosies ienākošo plūsmu saņemšanā, tostarp saņemot jauktas noliktavas vienības, pirkšanas pasūtījuma krājumiem, pārsūtīšanas pasūtījuma krājumiem un noslodzes krājumiem.</span><span class="sxs-lookup"><span data-stu-id="6b212-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="6b212-114">To var izmantot arī vienības izdošanai, ja skenējot svītrkodu, apstiprināto vienību kopskaitam tiks pievienos daudzums, kas tiks pārveidots starp svītrkoda UOM un darba vienību.</span><span class="sxs-lookup"><span data-stu-id="6b212-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="6b212-115">Ja uzskaitot svītrkoda UOM, tiek apstiprināts, ka daudzums ir atļauts inventarizācijai secību grupā, daudzums tiks pievienots kopējam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="6b212-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6b212-116">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="6b212-116">Where it applies</span></span>

<span data-ttu-id="6b212-117">Vienības izdošana darbojas visos inventarizācijas darbos un jebkura veida darba sākotnējā izdošanā.</span><span class="sxs-lookup"><span data-stu-id="6b212-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="6b212-118">Vienības izdošana nedarbojas, ja krājums tiek kontrolēts, izmantojot sērijas numurus, vai, ja tas ir ražošanas vai Kanban izdošana no noliktavas vienības (LP) atrašanās vietas, un krājumam ir iestatīti sagatavošanas posmi.</span><span class="sxs-lookup"><span data-stu-id="6b212-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="6b212-119">Vienības izdošanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6b212-119">Set up piece picking</span></span>

1.  <span data-ttu-id="6b212-120">Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai: Noliktavas pārvaldība > **Noliktavas pārvaldība** > **Iestatījumi** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="6b212-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="6b212-121">No mobilās ierīces izvēlnes vienuma atveriet sadaļu Darba apstiprinājuma iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="6b212-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="6b212-122">Tālāk minētās opcijas ir pieejamas atlasei, ja darbs ir izdošanas vai inventarizācijas darbs.</span><span class="sxs-lookup"><span data-stu-id="6b212-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="6b212-123">Opcija</span><span class="sxs-lookup"><span data-stu-id="6b212-123">Option</span></span>           |                                                                            <span data-ttu-id="6b212-124">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6b212-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b212-125">Vienības izdošanas apstiprinājums</span><span class="sxs-lookup"><span data-stu-id="6b212-125">Piece picking confirmation</span></span> | <span data-ttu-id="6b212-126">Izdošanai un inventarizācijai pieejamie darba veidi.</span><span class="sxs-lookup"><span data-stu-id="6b212-126">Available for pick and counting work types.</span></span> <span data-ttu-id="6b212-127">Preču apstiprināšana tiek automātiski atlasīta.</span><span class="sxs-lookup"><span data-stu-id="6b212-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="6b212-128">Ļauj apstiprināt katru krājuma vienību no mobilās ierīces.</span><span class="sxs-lookup"><span data-stu-id="6b212-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="6b212-129">Maksimālais vienību skaits</span><span class="sxs-lookup"><span data-stu-id="6b212-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="6b212-130">Darbs, kas pieejams izdošanai, ja vienības izdošanas apstiprināšana ir iespējota.</span><span class="sxs-lookup"><span data-stu-id="6b212-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="6b212-131">Iestata vienību skaita ierobežojumu, kas ir jāapstiprina.</span><span class="sxs-lookup"><span data-stu-id="6b212-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

