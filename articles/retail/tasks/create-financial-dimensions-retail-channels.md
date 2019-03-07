---
title: Mazumtirdzniecības kanālu finanšu dimensiju izveide un dimensiju vērtību konfigurēšana veikalos
description: Šajā procedūrā ir aprakstīts mazumtirdzniecības kanāla dimensijas izveides process, izmantojot dimensijas vērtības, kā arī finanšu dimensijas vērtību konfigurēšanas process mazumtirdzniecības veikalos.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "354533"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="6ea91-103">Mazumtirdzniecības kanālu finanšu dimensiju izveide un dimensiju vērtību konfigurēšana veikalos</span><span class="sxs-lookup"><span data-stu-id="6ea91-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6ea91-104">Šajā procedūrā ir aprakstīts mazumtirdzniecības kanāla dimensijas izveides process, izmantojot dimensijas vērtības, kā arī finanšu dimensijas vērtību konfigurēšanas process mazumtirdzniecības veikalos.</span><span class="sxs-lookup"><span data-stu-id="6ea91-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="6ea91-105">Šajā tēmā nav aprakstītas citas saistītās darbības, piemēram, dimensiju kopu un kontu struktūru izveide.</span><span class="sxs-lookup"><span data-stu-id="6ea91-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="6ea91-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="6ea91-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6ea91-107">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6ea91-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="6ea91-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6ea91-108">Click New.</span></span>
3. <span data-ttu-id="6ea91-109">Laukā Izmantot vērtības no atlasiet Mazumtirdzniecības kanāli.</span><span class="sxs-lookup"><span data-stu-id="6ea91-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="6ea91-110">Laukā Dimensijas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6ea91-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="6ea91-111">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-111">Click Activate.</span></span>
6. <span data-ttu-id="6ea91-112">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-112">Click Close.</span></span>
7. <span data-ttu-id="6ea91-113">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-113">Click Activate.</span></span>
8. <span data-ttu-id="6ea91-114">Noklikšķiniet uz Dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="6ea91-114">Click Dimension values.</span></span>
9. <span data-ttu-id="6ea91-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-115">Close the page.</span></span>
10. <span data-ttu-id="6ea91-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-116">Click Save.</span></span>
11. <span data-ttu-id="6ea91-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-117">Close the page.</span></span>
12. <span data-ttu-id="6ea91-118">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="6ea91-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="6ea91-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6ea91-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6ea91-120">Pārslēdziet sadaļas Finanšu dimensijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="6ea91-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-121">Click Edit.</span></span>
16. <span data-ttu-id="6ea91-122">Laukā Mazumtirdzniecības kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="6ea91-123">Sarakstā atrodiet un atlasiet dimensijas vērtību veikalam, kas tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="6ea91-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="6ea91-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6ea91-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="6ea91-125">Laukā CostCenter noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6ea91-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6ea91-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6ea91-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6ea91-128">Laukā Nodaļa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="6ea91-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6ea91-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="6ea91-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6ea91-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6ea91-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6ea91-131">Click Save.</span></span>

