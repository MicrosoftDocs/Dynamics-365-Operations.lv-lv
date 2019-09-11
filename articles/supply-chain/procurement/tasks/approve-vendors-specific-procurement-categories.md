---
title: Kreditoru apstiprināšana noteiktām sagādes kategorijām
description: Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 for Finance and Operations.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867153"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="fa302-103">Kreditoru apstiprināšana noteiktām sagādes kategorijām</span><span class="sxs-lookup"><span data-stu-id="fa302-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa302-104">Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa302-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fa302-105">Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas.</span><span class="sxs-lookup"><span data-stu-id="fa302-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="fa302-106">Šajā procedūrā ir parādīts, kā norādīt, ka kreditors ir apstiprināts vai vēlams noteiktai sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="fa302-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="fa302-107">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="fa302-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="fa302-108">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="fa302-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="fa302-109">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="fa302-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="fa302-110">Atlasiet kreditoru, kuru vēlaties iestatīt kā apstiprināto vai vēlamo kreditoru kādai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="fa302-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="fa302-111">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="fa302-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="fa302-112">Atlasiet **Kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="fa302-112">Select **Categories**.</span></span>
5. <span data-ttu-id="fa302-113">Atlasiet **Pievienot kategoriju**.</span><span class="sxs-lookup"><span data-stu-id="fa302-113">Select **Add category**.</span></span>
6. <span data-ttu-id="fa302-114">Laukā **Kategorija** atlasiet **BIROJA UN GALDA PIEDERUMI (BIROJA UN GALDA PIEDERUMI)**.</span><span class="sxs-lookup"><span data-stu-id="fa302-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="fa302-115">Laukā **Piegādātāja kategorijas statuss** atlasiet **Vēlamais**.</span><span class="sxs-lookup"><span data-stu-id="fa302-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="fa302-116">Vienai kategorijai ir iespējams norādīt vairākus vēlamos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="fa302-116">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="fa302-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fa302-117">Select **Save**.</span></span>
9. <span data-ttu-id="fa302-118">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Iepirkumu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="fa302-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="fa302-119">Kokā atlasiet **UZŅĒMUMA IEPIRKUMU KATEGORIJAS\BIROJA UN GALDA PIEDERUMI**.</span><span class="sxs-lookup"><span data-stu-id="fa302-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="fa302-120">Izvērsiet sadaļu **Piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="fa302-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="fa302-121">Pārbaudiet, vai jūsu atlasītais kreditors ir redzams kā vēlamais kreditors kategorijai Biroja un kancelejas piederumi.</span><span class="sxs-lookup"><span data-stu-id="fa302-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="fa302-122">Ja veicat šo procedūru kā uzdevuma vadītājs, jums var būt jāatlasa poga **Atbloķēt**, lai varētu ritināt uz leju uz piegādātāju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="fa302-122">If you’re running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="fa302-123">Šajā lapā ir iespējams pievienot vēlamos un apstiprinātos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="fa302-123">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="fa302-124">Kokā atlasiet **BIROJA UN GALDA PIEDERUMI** un atlasiet **Šķēres**.</span><span class="sxs-lookup"><span data-stu-id="fa302-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="fa302-125">Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Nē**.</span><span class="sxs-lookup"><span data-stu-id="fa302-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="fa302-126">Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="fa302-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

