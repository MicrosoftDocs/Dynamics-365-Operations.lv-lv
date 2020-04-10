---
title: Sagādes kataloga izveide
description: Šajā tēmā ir paskaidrots, kā izveidot sagādes katalogu.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94d5c3f6677ec10ea1b9ac3c488c3b8d7dc6856f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147484"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="b2208-103">Sagādes kataloga izveide</span><span class="sxs-lookup"><span data-stu-id="b2208-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2208-104">Šajā tēmā ir paskaidrots, kā izveidot sagādes katalogu.</span><span class="sxs-lookup"><span data-stu-id="b2208-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="b2208-105">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="b2208-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="b2208-106">Jūs arī uzzināsiet, kā darbinieki var izmantot katalogu, kad viņi veido pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="b2208-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="b2208-107">Lai varētu izveidot katalogu, jūsu sistēma ir jābūt sagādes kategoriju hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="b2208-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="b2208-108">Jaunais katalogs pārmanto šo hierarhiju, kā arī visas preces, kas atrodas šajā hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="b2208-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="b2208-109">Šo ceļvedi varat izmantot demonstrācijas datu uzņēmumā USMF, kur sagādes kategoriju hierarhija ir pieejama, kā arī procedūras darbībās izmantotajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="b2208-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="b2208-110">Pārliecinieties, ka pastāv sagādes kategoriju hierarhija</span><span class="sxs-lookup"><span data-stu-id="b2208-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="b2208-111">Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Sagādes kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="b2208-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="b2208-112">Sagādes kategoriju hierarhija ir pieejama USMF demonstrācijas datu uzņēmumā, un preces ir pievienotas kategorijai **Biroja aparatūra/datori**.</span><span class="sxs-lookup"><span data-stu-id="b2208-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="b2208-113">Ja šo procedūru izpildāt kā uzdevuma ceļvedi, ir nepieciešams atbloķēt šo ceļvedi, ja vēlaties pārlūkot kategoriju.</span><span class="sxs-lookup"><span data-stu-id="b2208-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="b2208-114">Ja hierarhija nebija pieejama, jums tā būtu jāizveido, noklikšķinot uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b2208-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="b2208-115">To var izdarīt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="b2208-115">This can only be done once.</span></span>  
2. <span data-ttu-id="b2208-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2208-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="b2208-117">Kataloga izveidošana</span><span class="sxs-lookup"><span data-stu-id="b2208-117">Create a catalog</span></span>
1. <span data-ttu-id="b2208-118">Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Katalogi > Sagādes katalogi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="b2208-119">Atlasiet **Jauns sagādes katalogs**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b2208-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="b2208-120">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2208-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b2208-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-121">Select **OK**.</span></span>
5. <span data-ttu-id="b2208-122">Koka struktūrā izvērsiet vienumu **KORP. SAGĀDES KATEGORIJAS**.</span><span class="sxs-lookup"><span data-stu-id="b2208-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="b2208-123">Koka struktūrā izvērsiet vienumu **BIROJA APARATŪRA**.</span><span class="sxs-lookup"><span data-stu-id="b2208-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="b2208-124">Koka struktūrā atlasiet vienumu **Datori**.</span><span class="sxs-lookup"><span data-stu-id="b2208-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="b2208-125">Preces no sagādes kategorijas tiek parādītas sarakstā.</span><span class="sxs-lookup"><span data-stu-id="b2208-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="b2208-126">Ja vēlaties kategorijai pievienot kādu preci, tas ir jādara lapā **Sagādes kategoriju hierarhija** vai lapā **Detalizēta informācija par krājumu**.</span><span class="sxs-lookup"><span data-stu-id="b2208-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="b2208-127">**Noklusējuma** atjaunināšanas tips nosaka, vai sagādes kategoriju hierarhijai pievienotās jaunās preces katalogā kļūst redzamas uzreiz.</span><span class="sxs-lookup"><span data-stu-id="b2208-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="b2208-128">Ja atjaunināšanas tips ir iestatīts uz **Dinamisks**, izmaiņas ir redzamas nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="b2208-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="b2208-129">Ja atjaunināšanas tips ir **Statisks**, jaunās preces kļūst redzamas tikai personām, kas katalogu lieto pēc tam, kad katalogs ir pārpublicēts.</span><span class="sxs-lookup"><span data-stu-id="b2208-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="b2208-130">Darbība **Publicēt** ir pieejama darbību rūtī lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="b2208-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="b2208-131">Ja preces tiek noņemtas no sagādes kategoriju hierarhijas, šīs izmaiņas kļūst redzamas nekavējoties, neatkarīgi no vērtības laukā **Noklusējuma** atjaunināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="b2208-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="b2208-132">Darbību rūtī atlasiet **Kategoriju navigācija** un pārliecinieties, vai ir atlasīta opcija **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="b2208-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="b2208-133">Atlasiet **Aktivizēt katalogu**.</span><span class="sxs-lookup"><span data-stu-id="b2208-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="b2208-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2208-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="b2208-135">Padarīt katalogu redzamu</span><span class="sxs-lookup"><span data-stu-id="b2208-135">Make the catalog visible</span></span>
1. <span data-ttu-id="b2208-136">Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="b2208-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="b2208-137">Atlasiet **Sagādes politika USMF**.</span><span class="sxs-lookup"><span data-stu-id="b2208-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="b2208-138">Ir jāatlasa pirkšanas politika tai juridiskajai personai, kurā ar jūsu lietotāja profilu saistītajam nodarbinātajam ir atļauts pasūtīt preces.</span><span class="sxs-lookup"><span data-stu-id="b2208-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="b2208-139">In the USMF demo data, the Admin user is connected to the worker called **Jūlija Funderburka**, un viņa pēc noklusējuma pasūta preces uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="b2208-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="b2208-140">Atlasiet katalogu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="b2208-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="b2208-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="b2208-142">Lietot katalogu</span><span class="sxs-lookup"><span data-stu-id="b2208-142">Use the catalog</span></span>
1. <span data-ttu-id="b2208-143">Dodieties uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="b2208-144">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b2208-144">Select **New**.</span></span>
3. <span data-ttu-id="b2208-145">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2208-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b2208-146">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-146">Select **OK**.</span></span>
5. <span data-ttu-id="b2208-147">Atlasiet **Pievienot preces**.</span><span class="sxs-lookup"><span data-stu-id="b2208-147">Select **Add products**.</span></span>
6. <span data-ttu-id="b2208-148">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2208-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="b2208-149">Lai filtrētu šīs preces, varat lietot kreisajā pusē esošo kategoriju hierarhiju vai filtru saraksta augšpusē.</span><span class="sxs-lookup"><span data-stu-id="b2208-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="b2208-150">Atlasiet **Pievienot rindām**.</span><span class="sxs-lookup"><span data-stu-id="b2208-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="b2208-151">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b2208-151">Select **OK**.</span></span>

