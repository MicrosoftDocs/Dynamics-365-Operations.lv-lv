--- 
title: " POS reģistru finanšu dimensiju izveide un dimensiju vērtību konfigurēšana reģistros"
description: "Šajā procedūrā ir aprakstīts, kā izveidot finanšu dimensijas pārdošanas punkta (POS) reģistriem un kā reģistros konfigurēt finanšu dimensijas vērtības."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8a3a6abc19bae20b7899628d0463cf458955671a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="9daf8-103"> POS reģistru finanšu dimensiju izveide un dimensiju vērtību konfigurēšana reģistros</span><span class="sxs-lookup"><span data-stu-id="9daf8-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9daf8-104">Šajā procedūrā ir aprakstīts, kā izveidot finanšu dimensijas pārdošanas punkta (POS) reģistriem un kā reģistros konfigurēt finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="9daf8-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="9daf8-105">Šajā procedūrā nav aprakstītas citas saistītās darbības, piemēram, dimensiju kopu un kontu struktūru izveide.</span><span class="sxs-lookup"><span data-stu-id="9daf8-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="9daf8-106">Informāciju par šiem uzdevumiem var skatīt citās tēmās.</span><span class="sxs-lookup"><span data-stu-id="9daf8-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="9daf8-107">Šajā piemērā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="9daf8-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="9daf8-108">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9daf8-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="9daf8-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9daf8-109">Click New.</span></span>
3. <span data-ttu-id="9daf8-110">Laukā Izmantot vērtības no atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9daf8-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="9daf8-111">Laukā Dimensijas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9daf8-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="9daf8-112">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-112">Click Activate.</span></span>
6. <span data-ttu-id="9daf8-113">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-113">Click Close.</span></span>
7. <span data-ttu-id="9daf8-114">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-114">Click Activate.</span></span>
8. <span data-ttu-id="9daf8-115">Noklikšķiniet uz Dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="9daf8-115">Click Dimension values.</span></span>
9. <span data-ttu-id="9daf8-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9daf8-116">Close the page.</span></span>
10. <span data-ttu-id="9daf8-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-117">Click Save.</span></span>
11. <span data-ttu-id="9daf8-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9daf8-118">Close the page.</span></span>
12. <span data-ttu-id="9daf8-119">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāla iestatīšana > POS iestatīšana > Reģistri.</span><span class="sxs-lookup"><span data-stu-id="9daf8-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="9daf8-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9daf8-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9daf8-121">Pārslēdziet sadaļas Finanšu dimensijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="9daf8-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="9daf8-122">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-122">Click Edit.</span></span>
16. <span data-ttu-id="9daf8-123">Laukā Terminālis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="9daf8-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9daf8-124">Sarakstā atrodiet un atlasiet dimensijas vērtību reģistram, kas tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="9daf8-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="9daf8-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9daf8-125">Click Save.</span></span>


