--- 
title: "Sagādes kataloga izveide"
description: "Šajā ceļvedī ir parādīts, kā izveidot sagādes katalogu."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="af438-103">Sagādes kataloga izveide</span><span class="sxs-lookup"><span data-stu-id="af438-103">Create a procurement catalog</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af438-104">Šajā ceļvedī ir parādīts, kā izveidot sagādes katalogu.</span><span class="sxs-lookup"><span data-stu-id="af438-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="af438-105">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="af438-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="af438-106">Jūs arī uzzināsiet, kā darbinieki var izmantot katalogu, kad viņi veido pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="af438-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="af438-107">Lai varētu izveidot katalogu, jūsu sistēma ir jābūt sagādes kategoriju hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="af438-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="af438-108">Jaunais katalogs pārmanto šo hierarhiju, kā arī visas preces, kas atrodas šajā hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="af438-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="af438-109">Šo ceļvedi varat izmantot demonstrācijas datu uzņēmumā USMF, kur sagādes kategoriju hierarhija ir pieejama, kā arī procedūras darbībās izmantotajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="af438-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="af438-110">Pārliecinieties, ka pastāv sagādes kategoriju hierarhija</span><span class="sxs-lookup"><span data-stu-id="af438-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="af438-111">Pārejiet uz Sagāde un avoti > Sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="af438-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="af438-112">Sagādes kategoriju hierarhija ir pieejama USMF demonstrācijas datu uzņēmumā, un preces ir pievienotas kategorijai Biroja aparatūra/datori.</span><span class="sxs-lookup"><span data-stu-id="af438-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="af438-113">Ja šo procedūru izpildāt kā uzdevuma ceļvedi, ir nepieciešams atbloķēt šo ceļvedi, ja vēlaties pārlūkot kategoriju.</span><span class="sxs-lookup"><span data-stu-id="af438-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="af438-114">Ja hierarhija nebija pieejama, jums tā būtu jāizveido, noklikšķinot uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="af438-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="af438-115">To var izdarīt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="af438-115">This can only be done once.</span></span>  
2. <span data-ttu-id="af438-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="af438-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="af438-117">Kataloga izveidošana</span><span class="sxs-lookup"><span data-stu-id="af438-117">Create a catalog</span></span>
1. <span data-ttu-id="af438-118">Pārejiet uz sadaļu Sagāde un avoti > Katalogi > Sagādes katalogi.</span><span class="sxs-lookup"><span data-stu-id="af438-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="af438-119">Noklikšķiniet uz Jauns sagādes katalogs, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="af438-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="af438-120">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="af438-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="af438-121">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="af438-121">Click OK.</span></span>
5. <span data-ttu-id="af438-122">Koka struktūrā izvērsiet vienumu “KORP. SAGĀDES KATEGORIJAS”.</span><span class="sxs-lookup"><span data-stu-id="af438-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="af438-123">Koka struktūrā izvērsiet vienumu “BIROJA APARATŪRA”.</span><span class="sxs-lookup"><span data-stu-id="af438-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="af438-124">Koka struktūrā atlasiet vienumu “Datori”.</span><span class="sxs-lookup"><span data-stu-id="af438-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="af438-125">Preces no sagādes kategorijas tiek parādītas sarakstā.</span><span class="sxs-lookup"><span data-stu-id="af438-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="af438-126">Ja vēlaties kategorijai pievienot kādu preci, tas ir jādara lapā Sagādes kategoriju hierarhija vai lapā Detalizēta informācija par krājumu.</span><span class="sxs-lookup"><span data-stu-id="af438-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="af438-127">Noklusējuma atjaunināšanas tips nosaka, vai sagādes kategoriju hierarhijai pievienotās jaunās preces katalogā kļūst redzamas uzreiz.</span><span class="sxs-lookup"><span data-stu-id="af438-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="af438-128">Ja atjaunināšanas tips ir iestatīts uz Dinamisks, izmaiņas ir redzamas nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="af438-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="af438-129">Ja atjaunināšanas tips ir Statisks, jaunās preces kļūst redzamas tikai personām, kas katalogu lieto pēc tam, kad katalogs ir pārpublicēts.</span><span class="sxs-lookup"><span data-stu-id="af438-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="af438-130">Darbība Publicēt ir pieejama darbību rūtī lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="af438-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="af438-131">Ja preces tiek noņemtas no sagādes kategoriju hierarhijas, šīs izmaiņas kļūst redzamas nekavējoties, neatkarīgi no vērtības laukā Noklusējuma atjaunināšanas tips.</span><span class="sxs-lookup"><span data-stu-id="af438-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="af438-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af438-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="af438-133">Noklikšķiniet uz Slēpt.</span><span class="sxs-lookup"><span data-stu-id="af438-133">Click Hide.</span></span>
10. <span data-ttu-id="af438-134">Darbību rūtī noklikšķiniet uz Kategoriju navigācija.</span><span class="sxs-lookup"><span data-stu-id="af438-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="af438-135">Noklikšķiniet uz Atspējot.</span><span class="sxs-lookup"><span data-stu-id="af438-135">Click Disable.</span></span>
12. <span data-ttu-id="af438-136">Darbību rūtī noklikšķiniet uz Kategoriju navigācija.</span><span class="sxs-lookup"><span data-stu-id="af438-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="af438-137">Noklikšķiniet uz Iespējot.</span><span class="sxs-lookup"><span data-stu-id="af438-137">Click Enable.</span></span>
14. <span data-ttu-id="af438-138">Noklikšķiniet uz Aktivizēt katalogu.</span><span class="sxs-lookup"><span data-stu-id="af438-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="af438-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="af438-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="af438-140">Padarīt katalogu redzamu</span><span class="sxs-lookup"><span data-stu-id="af438-140">Make the catalog visible</span></span>
1. <span data-ttu-id="af438-141">Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas.</span><span class="sxs-lookup"><span data-stu-id="af438-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="af438-142">Atlasiet vienumu Sagādes politika USMF.</span><span class="sxs-lookup"><span data-stu-id="af438-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="af438-143">Ir jāatlasa pirkšanas politika tai juridiskajai personai, kurā ar jūsu lietotāja profilu saistītajam nodarbinātajam ir atļauts pasūtīt preces.</span><span class="sxs-lookup"><span data-stu-id="af438-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="af438-144">USMF demonstrācijas datos lietotājs ar lomu Administrators ir savienots ar nodarbināto, kuru sauc Jūlija Funderburka, un viņa pēc noklusējuma pasūta preces uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="af438-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="af438-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="af438-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="af438-146">Atlasiet katalogu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="af438-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="af438-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="af438-147">Click OK.</span></span>
6. <span data-ttu-id="af438-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="af438-148">Close the page.</span></span>
7. <span data-ttu-id="af438-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="af438-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="af438-150">Lietot katalogu</span><span class="sxs-lookup"><span data-stu-id="af438-150">Use the catalog</span></span>
1. <span data-ttu-id="af438-151">Dodieties uz sadaļu Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="af438-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="af438-152">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="af438-152">Click New.</span></span>
3. <span data-ttu-id="af438-153">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="af438-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="af438-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="af438-154">Click OK.</span></span>
5. <span data-ttu-id="af438-155">Noklikšķiniet uz Pievienot preces.</span><span class="sxs-lookup"><span data-stu-id="af438-155">Click Add products.</span></span>
6. <span data-ttu-id="af438-156">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af438-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af438-157">Lai filtrētu šīs preces, varat lietot kreisajā pusē esošo kategoriju hierarhiju vai filtru saraksta augšpusē.</span><span class="sxs-lookup"><span data-stu-id="af438-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="af438-158">Noklikšķiniet uz Pievienot rindām.</span><span class="sxs-lookup"><span data-stu-id="af438-158">Click Add to lines.</span></span>
8. <span data-ttu-id="af438-159">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af438-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="af438-160">Noklikšķiniet uz Pievienot rindām.</span><span class="sxs-lookup"><span data-stu-id="af438-160">Click Add to lines.</span></span>
10. <span data-ttu-id="af438-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="af438-161">Click OK.</span></span>


