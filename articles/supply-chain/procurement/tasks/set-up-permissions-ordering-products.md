--- 
title: "Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā"
description: "Šajā procedūrā ir parādīts, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 30d91d2ffab74250b3a8a46d7b7c5441a94d8dfd
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="c780e-103">Atļauju iestatīšana preču pasūtīšanai kāda cita vārdā</span><span class="sxs-lookup"><span data-stu-id="c780e-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c780e-104">Šajā procedūrā ir parādīts, kā nodarbinātajiem piešķirt atļauju sagatavot pirkšanas pieprasījumus citu nodarbināto vārdā.</span><span class="sxs-lookup"><span data-stu-id="c780e-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="c780e-105">Citiem vārdiem sakot, pirkšanas pieprasījuma "sagatavotājs" var izveidot pieprasījuma cita "pieprasītāja" vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="c780e-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="c780e-106">Šajā procedūrā skaidrots arī, kā piešķirt darbinieku atļaujas pasūtīt krājumus un pakalpojumus dažādās juridiskajās personās vai pārvaldības struktūrvienībās.</span><span class="sxs-lookup"><span data-stu-id="c780e-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="c780e-107">Parasti šos uzdevumus veic pirkšanas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="c780e-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="c780e-108">Šo procedūru varat lietot ar datiem demonstrācijas datu uzņēmumam USMF vai ar paši saviem datiem.</span><span class="sxs-lookup"><span data-stu-id="c780e-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="c780e-109">Piešķirt atļauju ievadīt pirkšanas pieprasījumus cita nodarbinātā vārdā</span><span class="sxs-lookup"><span data-stu-id="c780e-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="c780e-110">Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas pieprasījumu atļaujas.</span><span class="sxs-lookup"><span data-stu-id="c780e-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="c780e-111">Pārliecinieties, ka laukam Pašreizējais skats ir iestatīta vērtība Pēc sagatavotāja.</span><span class="sxs-lookup"><span data-stu-id="c780e-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="c780e-112">Kreisajā rūtī esošajā sarakstā tiek rādītas personas, kurām var piešķirt atļauju sagatavot pieprasījumus citu personu vārdā.</span><span class="sxs-lookup"><span data-stu-id="c780e-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="c780e-113">Atlasiet personu, kurai piešķirt atļauju (sagatavotāju).</span><span class="sxs-lookup"><span data-stu-id="c780e-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="c780e-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c780e-114">Click Add.</span></span>
4. <span data-ttu-id="c780e-115">Atrodiet un atlasiet personu, ko pievienot kā pieprasītāju.</span><span class="sxs-lookup"><span data-stu-id="c780e-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="c780e-116">Pieprasītājs ir persona, kuras vārdā sagatavotājs varat izveidot pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="c780e-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="c780e-117">Laukā Autorizācija atlasiet vērtību Specifisks, ja sagatavotājam ir jāspēj izveidot pirkšanas pieprasījumus atlasītā nodarbinātā vārdā.</span><span class="sxs-lookup"><span data-stu-id="c780e-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="c780e-118">Atlasiet vērtību Pārskati, ja sagatavotājam ir arī jāspēj izveidot pirkšanas pieprasījumus visus to nodarbināto vārdā, kuri atskaitās šim nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="c780e-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="c780e-119">Laukā Ir spēkā ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="c780e-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="c780e-120">Laukā Termiņa beigas ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="c780e-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="c780e-121">Skatīt sagatavotājus, kuriem ir atļauja izveidot pirkšanas pieprasījumus atlasītajam nodarbinātajam</span><span class="sxs-lookup"><span data-stu-id="c780e-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="c780e-122">Laukā Pašreizējais skats atlasiet vienumu “Pēc pieprasītāja”.</span><span class="sxs-lookup"><span data-stu-id="c780e-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="c780e-123">Šajā skatā tiek rādīts saraksts ar sagatavotājiem, kuriem ir piešķirta atļauja izveidot pirkšanas pieprasījumus atlasīta nodarbinātā vārdā.</span><span class="sxs-lookup"><span data-stu-id="c780e-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="c780e-124">Izmantojiet ātro filtru, lai atrastu darbinieku, kuru tikko pievienojāt kā prasītāju.</span><span class="sxs-lookup"><span data-stu-id="c780e-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="c780e-125">Atlasiet šo pieprasītāju.</span><span class="sxs-lookup"><span data-stu-id="c780e-125">Select the requester.</span></span>
    * <span data-ttu-id="c780e-126">Sarakstā Sagatavotājs tiek rādītas personas, kam ir atļauja pasūtīt krājumus kreisajā rūtī atlasītā pieprasītāja vārdā.</span><span class="sxs-lookup"><span data-stu-id="c780e-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="c780e-127">Šeit varat pievienot papildu sagatavotājus.</span><span class="sxs-lookup"><span data-stu-id="c780e-127">You can add additional preparers here.</span></span>   <span data-ttu-id="c780e-128">Šis skats jums ļauj arī piešķirt pieprasītājam atļauju izveidot pieprasījumus juridiskajās personās un pārvaldības struktūrvienībās, kas nav šīs personas primārā juridiskā persona vai pārvaldības struktūrvienība.</span><span class="sxs-lookup"><span data-stu-id="c780e-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


