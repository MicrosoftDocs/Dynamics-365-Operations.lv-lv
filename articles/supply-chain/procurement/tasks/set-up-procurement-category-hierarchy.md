---
title: Sagādes kategoriju hierarhijas iestatīšana
description: Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7010fb702d16dc276bfee397066ccf95bf5d25a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147277"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="be572-103">Sagādes kategoriju hierarhijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="be572-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be572-104">Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā.</span><span class="sxs-lookup"><span data-stu-id="be572-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="be572-105">Šos uzdevumus parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="be572-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="be572-106">Pirms var sākt šo procedūru, ir jābūt Sagādes tipa kategoriju hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="be572-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="be572-107">Ja izmantojat demonstrācijas datu uzņēmumu, šo procedūru varat veikt USMF uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="be572-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="be572-108">Jaunas sagādes kategorijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="be572-108">Add a new procurement category</span></span>
1. <span data-ttu-id="be572-109">Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Sūtījums > Sagādes kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="be572-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="be572-110">Darbību rūtī atlasiet **Rediģēt kategoriju hierarhiju**.</span><span class="sxs-lookup"><span data-stu-id="be572-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="be572-111">Pašreizējā sagādes kategoriju hierarhija tiek parādīta lapas kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="be572-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="be572-112">Jūs gatavojaties modificēt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="be572-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="be572-113">Darbību rūtī atlasiet **Jauns kategorijas zars**.</span><span class="sxs-lookup"><span data-stu-id="be572-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="be572-114">Sistēma atlasa augšējo zaru pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="be572-114">The system selects the top node by default.</span></span> <span data-ttu-id="be572-115">Ja veicāt šo procedūru kā uzdevumu ceļvedi, varat noklikšķināt uz pogas Atbloķēt un atlasīt citu pamatzaru, kura jāievieto jūsu jaunais zars.</span><span class="sxs-lookup"><span data-stu-id="be572-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="be572-116">Kad tas tiks izdarīts, atkal bloķējiet uzdevumu ceļvedi un pēc tam noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="be572-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="be572-117">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="be572-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="be572-118">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="be572-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="be572-119">Laukā **Draudzīgais nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="be572-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="be572-120">Draudzīgais nosaukums nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="be572-120">The friendly name is optional.</span></span> <span data-ttu-id="be572-121">Tas tiks parādīts kategorijas uzmeklēšanās kopā ar kategorijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="be572-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="be572-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="be572-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="be572-123">Preču pievienošana jaunajai sagādes kategorijai</span><span class="sxs-lookup"><span data-stu-id="be572-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="be572-124">Pārejiet uz **Sagāde un avoti > Sūtījums > Sagādes kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="be572-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="be572-125">Atlasiet zaru, ko tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="be572-125">Select the node you just added.</span></span> <span data-ttu-id="be572-126">Ja veicāt šo procedūru kā uzdevuma ceļvedi, lai atlasītu zaru, iespējams, būs jāatbloķē šis uzdevuma ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="be572-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="be572-127">Pārslēdziet sadaļas **Preces** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="be572-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="be572-128">Atlasiet **Pievienot**, lai saistītu preces ar sagādes kategoriju.</span><span class="sxs-lookup"><span data-stu-id="be572-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="be572-129">Atlasiet preces, ko vēlaties pievienot sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="be572-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="be572-130">Atlasiet bultu, lai pievienotu preces tabulai **Atlasīts**.</span><span class="sxs-lookup"><span data-stu-id="be572-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="be572-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="be572-131">Select **OK**.</span></span>
