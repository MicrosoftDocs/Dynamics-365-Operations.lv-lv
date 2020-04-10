---
title: Mazumtirdzniecības kanālu finanšu dimensiju izveide un dimensiju vērtību konfigurēšana veikalos
description: Šajā procedūrā ir aprakstīts tirdzniecības kanāla dimensijas izveides process, izmantojot dimensijas vērtības, kā arī finanšu dimensijas vērtību konfigurēšanas process veikalos.
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
ms.openlocfilehash: ea36732023092f714b3a783d98b512c0fea7dade
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141411"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="b0688-103">Mazumtirdzniecības kanālu finanšu dimensiju izveide un dimensiju vērtību konfigurēšana veikalos</span><span class="sxs-lookup"><span data-stu-id="b0688-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0688-104">Šajā procedūrā ir aprakstīts tirdzniecības kanāla dimensijas izveides process, izmantojot dimensijas vērtības, kā arī finanšu dimensijas vērtību konfigurēšanas process veikalos.</span><span class="sxs-lookup"><span data-stu-id="b0688-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="b0688-105">Šajā tēmā nav aprakstītas citas saistītās darbības, piemēram, dimensiju kopu un kontu struktūru izveide.</span><span class="sxs-lookup"><span data-stu-id="b0688-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="b0688-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="b0688-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b0688-107">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b0688-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b0688-108">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="b0688-108">Click New.</span></span>
3. <span data-ttu-id="b0688-109">Laukā ¨Izmantot vērtības no¨ atlasiet ¨Tirdzniecības kanāli¨.</span><span class="sxs-lookup"><span data-stu-id="b0688-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="b0688-110">Laukā Dimensijas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b0688-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="b0688-111">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="b0688-111">Click Activate.</span></span>
6. <span data-ttu-id="b0688-112">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="b0688-112">Click Close.</span></span>
7. <span data-ttu-id="b0688-113">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="b0688-113">Click Activate.</span></span>
8. <span data-ttu-id="b0688-114">Noklikšķiniet uz Dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="b0688-114">Click Dimension values.</span></span>
9. <span data-ttu-id="b0688-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b0688-115">Close the page.</span></span>
10. <span data-ttu-id="b0688-116">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b0688-116">Click Save.</span></span>
11. <span data-ttu-id="b0688-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b0688-117">Close the page.</span></span>
12. <span data-ttu-id="b0688-118">Parejiet uz Retail un Commerce > Kanāli > Veikali > Visi veikali.</span><span class="sxs-lookup"><span data-stu-id="b0688-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="b0688-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0688-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b0688-120">Pārslēdziet sadaļas Finanšu dimensijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="b0688-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="b0688-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b0688-121">Click Edit.</span></span>
16. <span data-ttu-id="b0688-122">Laukā ¨Tirdzniecības kanāls¨ noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0688-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b0688-123">Sarakstā atrodiet un atlasiet dimensijas vērtību veikalam, kas tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="b0688-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="b0688-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0688-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="b0688-125">Laukā CostCenter noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0688-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="b0688-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b0688-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="b0688-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0688-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="b0688-128">Laukā Nodaļa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b0688-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="b0688-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b0688-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="b0688-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0688-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="b0688-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b0688-131">Click Save.</span></span>

