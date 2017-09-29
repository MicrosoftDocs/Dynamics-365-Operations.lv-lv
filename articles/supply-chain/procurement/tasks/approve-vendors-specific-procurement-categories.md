--- 
title: "Kreditoru apstiprināšana noteiktām sagādes kategorijām"
description: "Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 83945932d56abf6bf44476e5647f8ae7abdc3602
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="4d371-103">Kreditoru apstiprināšana noteiktām sagādes kategorijām</span><span class="sxs-lookup"><span data-stu-id="4d371-103">Approve vendors for specific procurement categories</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d371-104">Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas.</span><span class="sxs-lookup"><span data-stu-id="4d371-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="4d371-105">Šajā procedūrā ir parādīts, kā norādīt, ka kreditors ir apstiprināts vai vēlams noteiktai sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="4d371-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="4d371-106">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="4d371-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="4d371-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="4d371-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="4d371-108">Pārejiet uz sadaļu Sagāde un avoti > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="4d371-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="4d371-109">Atlasiet kreditoru, kuru vēlaties iestatīt kā apstiprināto vai vēlamo kreditoru kādai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="4d371-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="4d371-110">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="4d371-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="4d371-111">Noklikšķiniet uz Kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4d371-111">Click Categories.</span></span>
5. <span data-ttu-id="4d371-112">Noklikšķiniet uz Pievienot kategoriju.</span><span class="sxs-lookup"><span data-stu-id="4d371-112">Click Add category.</span></span>
6. <span data-ttu-id="4d371-113">Laukā Kategorija atlasiet vienumu BIROJA UN KANCELEJAS PIEDERUMI (BIROJA UN KANCELEJAS PIEDERUMI).</span><span class="sxs-lookup"><span data-stu-id="4d371-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="4d371-114">Laukā Kreditora kategorijas statuss atlasiet vienumu “Vēlams”.</span><span class="sxs-lookup"><span data-stu-id="4d371-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="4d371-115">Vienai kategorijai ir iespējams norādīt vairākus vēlamos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="4d371-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="4d371-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4d371-116">Click Save.</span></span>
9. <span data-ttu-id="4d371-117">Pārejiet uz Sagāde un avoti > Sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4d371-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="4d371-118">Koka struktūrā atlasiet “KORP. SAGĀDES KATEGORIJAS\BIROJA UN KANCELEJAS PIEDERUMI”.</span><span class="sxs-lookup"><span data-stu-id="4d371-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="4d371-119">Izvērsiet sadaļu Kreditori.</span><span class="sxs-lookup"><span data-stu-id="4d371-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="4d371-120">Pārbaudiet, vai jūsu atlasītais kreditors ir redzams kā vēlamais kreditors kategorijai Biroja un kancelejas piederumi.</span><span class="sxs-lookup"><span data-stu-id="4d371-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="4d371-121">Ja šo procedūru izpildāt kā uzdevuma ceļvedi, iespējams, jums ir jānoklikšķina uz pogas Atbloķēt, lai varētu ritināt uz leju līdz kreditoru sarakstam.</span><span class="sxs-lookup"><span data-stu-id="4d371-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="4d371-122">Šajā lapā ir iespējams pievienot vēlamos un apstiprinātos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="4d371-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="4d371-123">Koka struktūrā izvērsiet vienumu “BIROJA UN KANCELEJAS PIEDERUMI”.</span><span class="sxs-lookup"><span data-stu-id="4d371-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="4d371-124">Kokā struktūrā atlasiet vienumu “Šķēres”.</span><span class="sxs-lookup"><span data-stu-id="4d371-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="4d371-125">Laukā Pārmantot kreditorus no pamatkategorijas: atlasiet vērtību Nē.</span><span class="sxs-lookup"><span data-stu-id="4d371-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="4d371-126">Laukā Pārmantot kreditorus no pamatkategorijas: atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="4d371-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


