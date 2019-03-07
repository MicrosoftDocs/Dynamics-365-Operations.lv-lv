---
title: Sagādes kategoriju hierarhijas iestatīšana
description: Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "334523"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="066a8-103">Sagādes kategoriju hierarhijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="066a8-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="066a8-104">Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā.</span><span class="sxs-lookup"><span data-stu-id="066a8-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="066a8-105">Šos uzdevumus parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="066a8-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="066a8-106">Pirms var sākt šo procedūru, ir jābūt Sagādes tipa kategoriju hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="066a8-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="066a8-107">Ja izmantojat demonstrācijas datu uzņēmumu, šo procedūru varat veikt USMF uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="066a8-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="066a8-108">Jaunas sagādes kategorijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="066a8-108">Add a new procurement category</span></span>
1. <span data-ttu-id="066a8-109">Pārejiet uz Sagāde un avoti > Sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="066a8-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="066a8-110">Noklikšķiniet uz Rediģēt kategoriju hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="066a8-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="066a8-111">Pašreizējā sagādes kategoriju hierarhija tiek parādīta lapas kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="066a8-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="066a8-112">Jūs gatavojaties modificēt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="066a8-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="066a8-113">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="066a8-113">Click New category node.</span></span>
    * <span data-ttu-id="066a8-114">Sistēma atlasa augšējo zaru pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="066a8-114">The system selects the top node by default.</span></span> <span data-ttu-id="066a8-115">Ja veicāt šo procedūru kā uzdevumu ceļvedi, varat noklikšķināt uz pogas Atbloķēt un atlasīt citu pamatzaru, kura jāievieto jūsu jaunais zars.</span><span class="sxs-lookup"><span data-stu-id="066a8-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="066a8-116">Kad tas tiks izdarīts, atkal bloķējiet uzdevumu ceļvedi un pēc tam noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="066a8-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="066a8-117">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="066a8-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="066a8-118">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="066a8-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="066a8-119">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="066a8-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="066a8-120">Draudzīgais nosaukums nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="066a8-120">The friendly name is optional.</span></span> <span data-ttu-id="066a8-121">Tas tiks parādīts kategorijas uzmeklēšanās kopā ar kategorijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="066a8-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="066a8-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="066a8-123">Preču pievienošana jaunajai sagādes kategorijai</span><span class="sxs-lookup"><span data-stu-id="066a8-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="066a8-124">Pārejiet uz Sagāde un avoti > Sagādes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="066a8-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="066a8-125">Atlasiet zaru, ko tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="066a8-125">Select the node you just added.</span></span> <span data-ttu-id="066a8-126">Ja veicāt šo procedūru kā uzdevuma ceļvedi, lai atlasītu zaru, iespējams, būs jāatbloķē šis uzdevuma ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="066a8-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="066a8-127">Pārslēdziet sadaļas Preces paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="066a8-128">Noklikšķiniet uz Pievienot, lai saistītu preces ar sagādes kategoriju.</span><span class="sxs-lookup"><span data-stu-id="066a8-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="066a8-129">Atlasiet preci, ko vēlaties pievienot sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="066a8-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="066a8-130">Noklikšķiniet uz bultiņas, lai atlasītu preci.</span><span class="sxs-lookup"><span data-stu-id="066a8-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="066a8-131">Atlasiet citu preci, ko vēlaties pievienot sagādes kategorijai.</span><span class="sxs-lookup"><span data-stu-id="066a8-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="066a8-132">Noklikšķiniet uz bultiņas, lai atlasītu preci.</span><span class="sxs-lookup"><span data-stu-id="066a8-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="066a8-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="066a8-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="066a8-134">Apstiprināto vai vēlamo kreditoru pievienošana</span><span class="sxs-lookup"><span data-stu-id="066a8-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="066a8-135">Pārslēdziet sadaļas Kreditori paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="066a8-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="066a8-136">Click Add.</span></span>
    * <span data-ttu-id="066a8-137">Var pievienot kreditoru sagādes kategorijai un norādīt, vai kreditors ir vēlams vai apstiprināts šai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="066a8-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="066a8-138">Dzēšot kreditoru no kategorijas, vēsturiskās transakcijas ar kreditoru kategorijā netiek dzēstas.</span><span class="sxs-lookup"><span data-stu-id="066a8-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="066a8-139">Atrodiet kreditoru, ko vēlaties pievienot kategorijai.</span><span class="sxs-lookup"><span data-stu-id="066a8-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="066a8-140">Noklikšķiniet uz bultiņas, lai atlasītu kreditoru.</span><span class="sxs-lookup"><span data-stu-id="066a8-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="066a8-141">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="066a8-141">Click OK.</span></span>
6. <span data-ttu-id="066a8-142">Izvēlieties kreditora rindu, ko vēlaties modificēt.</span><span class="sxs-lookup"><span data-stu-id="066a8-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="066a8-143">Laukā Kreditora statuss atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="066a8-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="066a8-144">Kreditora izvēles iestatījums Kategorijas ierobežojuma nosacījumos reglamentē, vai pirkšanas pieprasījumos pieejami vēlamie, apstiprinātie vai visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="066a8-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="066a8-145">Papildinformācijas pievienošana kategorijai</span><span class="sxs-lookup"><span data-stu-id="066a8-145">Add additional information to the category</span></span>
1. <span data-ttu-id="066a8-146">Pārslēdziet sadaļas Kreditoru vērtēšanas kritēriju grupas sadaļas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="066a8-147">Šī cilne ļauj definēt, pēc kuriem kritērijiem jāvērtē kreditori sagādes kategorijā.</span><span class="sxs-lookup"><span data-stu-id="066a8-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="066a8-148">Lai to izdarītu, jānoklikšķina uz Pievienot un pēc tam jāatlasa kreditoru novērtēšanas grupa, kas satur vēlamos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="066a8-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="066a8-149">Pārslēdziet sadaļas Anketas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="066a8-150">Šī cilne ļauj jums pievienot anketas, kas parādīsies uz pieprasījumā, ja Aktivitātes tips ir iestatīts uz "Pieprasījums".</span><span class="sxs-lookup"><span data-stu-id="066a8-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="066a8-151">Pēc tam pieprasītājam jāaizpilda anketa pirms pieprasījuma iesniegšanas par noteiktu preci vai precēm sagādes kategorijā.</span><span class="sxs-lookup"><span data-stu-id="066a8-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="066a8-152">Pārslēdziet sadaļas Krājumu PVN grupas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="066a8-153">Laukā Krājumu PVN grupa: noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="066a8-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="066a8-154">Atlasiet PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="066a8-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="066a8-155">Pārslēdziet sadaļas Kategorijas lapa paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="066a8-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="066a8-156">Kategorijas lapas tiek izveidotas lapā Kategoriju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="066a8-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="066a8-157">Tās satur informāciju par sagādes kategoriju, piemēram, informāciju par preču tipu kategorijā, preču attēliem kategorijā un paziņojumiem, piemēram, atlaidēm, kas ir pieejamas kategorijā.</span><span class="sxs-lookup"><span data-stu-id="066a8-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="066a8-158">Kategorijas lapas informācija tiek parādīta pirkšanas pieprasījumos.</span><span class="sxs-lookup"><span data-stu-id="066a8-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="066a8-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="066a8-159">Close the page.</span></span>

