---
title: Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai
description: Šajā procedūrā ir parādīts, kā iestatīt vienumu izvēlnē Mobilā ierīce.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "337559"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="9f73e-103">Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai</span><span class="sxs-lookup"><span data-stu-id="9f73e-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f73e-104">Šajā procedūrā ir parādīts, kā iestatīt vienumu izvēlnē Mobilā ierīce.</span><span class="sxs-lookup"><span data-stu-id="9f73e-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="9f73e-105">Šajā piemērā izvēlnes vienums tiek lietots, lai veiktu darbu ar tipu Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9f73e-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="9f73e-106">Ar izvēlnes vienumu saistītā darba klase nosaka, kurš darbs ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="9f73e-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="9f73e-107">Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="9f73e-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="9f73e-108">Parasti šo procedūru izpilda noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="9f73e-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="9f73e-109">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="9f73e-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="9f73e-110">Dodieties uz sadaļu Mobilās ierīces izvēlnes vienumi.</span><span class="sxs-lookup"><span data-stu-id="9f73e-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="9f73e-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f73e-111">Click New.</span></span>
3. <span data-ttu-id="9f73e-112">Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f73e-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="9f73e-113">Ievadiet unikālu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f73e-113">Enter a unique value.</span></span> <span data-ttu-id="9f73e-114">Varat ierakstīt, piemēram, POMove.</span><span class="sxs-lookup"><span data-stu-id="9f73e-114">For example, you could type POMove.</span></span> <span data-ttu-id="9f73e-115">Atcerieties šo vērtību, jums tā vēlāk būs nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="9f73e-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="9f73e-116">Laukā Virsraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f73e-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="9f73e-117">Tas ir nosaukums, kas tiks rādīts mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="9f73e-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="9f73e-118">Varat ierakstīt, piemēram, PO pārvietošana.</span><span class="sxs-lookup"><span data-stu-id="9f73e-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="9f73e-119">Laukā Režīms atlasiet "Darbs".</span><span class="sxs-lookup"><span data-stu-id="9f73e-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="9f73e-120">Laukā Izmantot esošo darbu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9f73e-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="9f73e-121">Šis mobilās ierīces izvēlnes elements tiek izmantots, lai veiktu esošu darbu.</span><span class="sxs-lookup"><span data-stu-id="9f73e-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="9f73e-122">Tādēļ šī vērtība jums ir jāiestata uz Jā.</span><span class="sxs-lookup"><span data-stu-id="9f73e-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="9f73e-123">Lauks Rādīt krājumu statusu nosaka, vai noliktavas darbiniekam mobilajā ierīcē tiks parādīts rīcībā esošo krājumu statuss.</span><span class="sxs-lookup"><span data-stu-id="9f73e-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="9f73e-124">Laukā Novirzītājs atlasiet vienumu Sistēmas grupēšana.</span><span class="sxs-lookup"><span data-stu-id="9f73e-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="9f73e-125">Kad kaut ko atlasāt laukā Novirzītājs, šīs lapas sadaļā Vispārīgi kļūst redzami papildu lauki.</span><span class="sxs-lookup"><span data-stu-id="9f73e-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="9f73e-126">Rādītie lauki ir atkarīgi no jūsu veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="9f73e-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="9f73e-127">Kad atlasāt Sistēmas grupēšana, tiek pievienoti divi jauni lauki.</span><span class="sxs-lookup"><span data-stu-id="9f73e-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="9f73e-128">Tie ir paskaidroti tālāk.</span><span class="sxs-lookup"><span data-stu-id="9f73e-128">These are explained below.</span></span>  
8. <span data-ttu-id="9f73e-129">Laukā Sistēmas grupēšana atlasiet “WorkPoolId”.</span><span class="sxs-lookup"><span data-stu-id="9f73e-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="9f73e-130">Kad noliktavas darbinieki atver šo izvēlnes elementu, viņiem tiek lūgts skenēt darbu kopas ID.</span><span class="sxs-lookup"><span data-stu-id="9f73e-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="9f73e-131">Visi darbu pasūtījumi ar šo darbu kopas ID un atvērtām darbu pasūtījuma rindām, kurās šim izvēlnes elementam ir pievienota viena no darbu klasēm, tiks padoti lietotājam.</span><span class="sxs-lookup"><span data-stu-id="9f73e-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="9f73e-132">Laukā Sistēmas grupēšanas etiķete ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f73e-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="9f73e-133">Šis ir teksts, kas tiek rādīts lietotājam mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="9f73e-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="9f73e-134">Varat ierakstīt, piemēram, Darbu kopa.</span><span class="sxs-lookup"><span data-stu-id="9f73e-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="9f73e-135">Laukā Ignorēt noliktavas vienību izvietojot atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9f73e-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="9f73e-136">Šī opcija noliktavas darbiniekiem ļauj ignorēt mērķa noliktavas vienības numura zīmi, kad krājumi tiek izvietoti no numura zīmes atkarīgā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="9f73e-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="9f73e-137">Laukā Grupēt izvietošanu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9f73e-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="9f73e-138">Ja visiem darbu pasūtījumiem izvietošanas rindās ir tas pats novietojums, tad lietotājs saņems vienu kombinētu izvietošanas instrukciju visām rindām.</span><span class="sxs-lookup"><span data-stu-id="9f73e-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="9f73e-139">Audita veidnes ID: darba audita veidne jums ļauj norādīt, ka darba process kādam izvēlnes elementam ir jāpārtrauc, lai varētu izpildīt citu operāciju.</span><span class="sxs-lookup"><span data-stu-id="9f73e-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="9f73e-140">Piemēram, ja šis izvēlnes elements ir paredzēts ienākošam darbam, tad audita veidnē var tikt pieprasīts, lai darbinieks pārbaudītu temperatūru.</span><span class="sxs-lookup"><span data-stu-id="9f73e-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="9f73e-141">Procesa pārtraukšanas brīdis ir norādīts audita veidnē un tas var būt, piemēram, brīdis, kad darbs tiek sākts vai pabeigts, vai brīdis, kad tiek mainīts darba statuss.</span><span class="sxs-lookup"><span data-stu-id="9f73e-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="9f73e-142">Izvērsiet sadaļu Darba klases.</span><span class="sxs-lookup"><span data-stu-id="9f73e-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="9f73e-143">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f73e-143">Click New.</span></span>
14. <span data-ttu-id="9f73e-144">Laukā Darba klases ID ierakstiet “Pirkšana”.</span><span class="sxs-lookup"><span data-stu-id="9f73e-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="9f73e-145">Darbu veidne ierobežo darbu, kam šo izvēlnes elementu var izmantot.</span><span class="sxs-lookup"><span data-stu-id="9f73e-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="9f73e-146">Šajā gadījumā tā tiks izmantota atvērtajām darbu pasūtījuma rindām, kam ir pirkšanas darba klases ID.</span><span class="sxs-lookup"><span data-stu-id="9f73e-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="9f73e-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f73e-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="9f73e-148">Darba apstiprinājuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9f73e-148">Set up work confirmation</span></span>
1. <span data-ttu-id="9f73e-149">Noklikšķiniet uz vienuma Darba apstiprinājuma iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="9f73e-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="9f73e-150">Laukā Darba tips atlasiet vienumu “Izdošana”.</span><span class="sxs-lookup"><span data-stu-id="9f73e-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="9f73e-151">Atzīmējiet izvēles rūtiņu Automātiskā apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="9f73e-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="9f73e-152">Darba instrukcija ar darba tipu Izdošana tiks apstiprināta automātiski.</span><span class="sxs-lookup"><span data-stu-id="9f73e-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="9f73e-153">Šī instrukcija netiks parādīta lietotājam.</span><span class="sxs-lookup"><span data-stu-id="9f73e-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="9f73e-154">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f73e-154">Click New.</span></span>
5. <span data-ttu-id="9f73e-155">Laukā Darba tips atlasiet vienumu “Izvietošana”.</span><span class="sxs-lookup"><span data-stu-id="9f73e-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="9f73e-156">Atzīmējiet izvēles rūtiņu Novietojuma apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="9f73e-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="9f73e-157">Kad krājums tiek nolikts, noliktavas darbiniekam tiek lūgts izpildīt novietojuma apstiprinājuma skenēšanu.</span><span class="sxs-lookup"><span data-stu-id="9f73e-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="9f73e-158">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f73e-158">Click Save.</span></span>
8. <span data-ttu-id="9f73e-159">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f73e-159">Close the page.</span></span>
9. <span data-ttu-id="9f73e-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f73e-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="9f73e-161">Izvēlnes elementa pievienošana mobilās ierīces izvēlnei</span><span class="sxs-lookup"><span data-stu-id="9f73e-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="9f73e-162">Dodieties uz sadaļu Mobilās ierīces izvēlne.</span><span class="sxs-lookup"><span data-stu-id="9f73e-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="9f73e-163">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9f73e-163">Click Edit.</span></span>
3. <span data-ttu-id="9f73e-164">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="9f73e-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9f73e-165">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "ienākošs".</span><span class="sxs-lookup"><span data-stu-id="9f73e-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="9f73e-166">Jūs vēlaties atrast izvēlni, kuru izmantojat ienākošajiem izvēlnes elementiem.</span><span class="sxs-lookup"><span data-stu-id="9f73e-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="9f73e-167">Uzņēmumā USMF tā tiek saukta par Ienākošais.</span><span class="sxs-lookup"><span data-stu-id="9f73e-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="9f73e-168">Kokā atlasiet "vērtība".</span><span class="sxs-lookup"><span data-stu-id="9f73e-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="9f73e-169">Noklikšķiniet uz bultiņas, kas rāda pa labi.</span><span class="sxs-lookup"><span data-stu-id="9f73e-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="9f73e-170">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f73e-170">Click Save.</span></span>
7. <span data-ttu-id="9f73e-171">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9f73e-171">Close the page.</span></span>

