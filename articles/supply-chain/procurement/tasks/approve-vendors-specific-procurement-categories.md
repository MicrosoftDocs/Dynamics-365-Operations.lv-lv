---
title: Kreditoru apstiprināšana noteiktām sagādes kategorijām
description: Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 Supply Chain Management.
author: RichardLuan
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c337fd6c2c7cea088b2151bebb54cec326c5240d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237329"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="ba98d-103">Kreditoru apstiprināšana noteiktām sagādes kategorijām</span><span class="sxs-lookup"><span data-stu-id="ba98d-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba98d-104">Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ba98d-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ba98d-105">Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas.</span><span class="sxs-lookup"><span data-stu-id="ba98d-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="ba98d-106">Šajā procedūrā ir parādīts, kā norādīt, ka kreditors ir apstiprināts vai vēlams noteiktai sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="ba98d-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="ba98d-107">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="ba98d-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="ba98d-108">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="ba98d-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="ba98d-109">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="ba98d-110">Atlasiet kreditoru, kuru vēlaties iestatīt kā apstiprināto vai vēlamo kreditoru kādai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="ba98d-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="ba98d-111">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="ba98d-112">Atlasiet **Kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-112">Select **Categories**.</span></span>
5. <span data-ttu-id="ba98d-113">Atlasiet **Pievienot kategoriju**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-113">Select **Add category**.</span></span>
6. <span data-ttu-id="ba98d-114">Laukā **Kategorija** atlasiet **BIROJA UN GALDA PIEDERUMI (BIROJA UN GALDA PIEDERUMI)**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="ba98d-115">Laukā **Piegādātāja kategorijas statuss** atlasiet **Vēlamais**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="ba98d-116">Vienai kategorijai ir iespējams norādīt vairākus vēlamos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="ba98d-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="ba98d-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-117">Select **Save**.</span></span>
9. <span data-ttu-id="ba98d-118">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Iepirkumu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="ba98d-119">Kokā atlasiet **UZŅĒMUMA IEPIRKUMU KATEGORIJAS\BIROJA UN GALDA PIEDERUMI**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="ba98d-120">Izvērsiet sadaļu **Piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="ba98d-121">Pārbaudiet, vai jūsu atlasītais kreditors ir redzams kā vēlamais kreditors kategorijai Biroja un kancelejas piederumi.</span><span class="sxs-lookup"><span data-stu-id="ba98d-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="ba98d-122">Ja veicat šo procedūru kā uzdevuma vadītājs, jums var būt jāatlasa poga **Atbloķēt**, lai varētu ritināt uz leju uz piegādātāju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ba98d-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="ba98d-123">Šajā lapā ir iespējams pievienot vēlamos un apstiprinātos kreditorus.</span><span class="sxs-lookup"><span data-stu-id="ba98d-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="ba98d-124">Kokā atlasiet **BIROJA UN GALDA PIEDERUMI** un atlasiet **Šķēres**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="ba98d-125">Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Nē**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="ba98d-126">Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ba98d-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]