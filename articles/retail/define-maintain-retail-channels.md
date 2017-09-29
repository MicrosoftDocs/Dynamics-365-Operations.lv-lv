---
title: "Mazumtirdzniecības kanālu definēšana un uzturēšana"
description: "Šajā rakstā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmatūrā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 700b8868a68be7f0172202d737b4f1ae9813ecf3
ms.contentlocale: lv-lv
ms.lasthandoff: 08/30/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="53867-104">Mazumtirdzniecības kanālu definēšana un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="53867-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="53867-105">Šajā rakstā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmatūrā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem.</span><span class="sxs-lookup"><span data-stu-id="53867-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="53867-106">Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="53867-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="53867-107">Dynamics 365 for Retail atbalsta vairākus mazumtirdzniecības kanālus, piemēram, tiešsaistes veikalus, zvanu centrus un fiziskus veikalus.</span><span class="sxs-lookup"><span data-stu-id="53867-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="53867-108">Fizisks veikals tiek saukts par mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="53867-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="53867-109">Katram mazumtirdzniecības veikalam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="53867-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="53867-110">Pirms izveidojat mazumtirdzniecības veikalu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="53867-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="53867-111">Pēc mazumtirdzniecības veikala izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā izmantot.</span><span class="sxs-lookup"><span data-stu-id="53867-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="53867-112">Veikalam var arī piešķirt darbiniekus, kases sistēmas un debitorus.</span><span class="sxs-lookup"><span data-stu-id="53867-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="53867-113">Visbeidzot, pievienojiet jaunu veikalu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="53867-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="53867-114">Mazumtirdzniecības veikalu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="53867-114">Setting up retail stores</span></span>
<span data-ttu-id="53867-115">Pirms mazumtirdzniecības veikala iestatīšanas programmatūrā Dynamics 365 for Retail, ir jāizpilda daži priekšnosacījumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="53867-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="53867-116">Pēc tam varat izveidot mazumtirdzniecības veikalu un pievienot detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="53867-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="53867-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="53867-117">Prerequisites</span></span>

<span data-ttu-id="53867-118">Lai varētu iestatīt mazumtirdzniecības veikalu, jums ir jāizpilda tālāk uzskaitītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="53867-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="53867-119">Konfigurējiet savas organizācijas struktūru un iestatiet organizācijas hierarhijas mazumtirdzniecības preču klāstiem, papildināšanai un atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="53867-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="53867-120">Iestatiet noliktavu, kas pārstāv mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="53867-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="53867-121">Iestatiet numuru sērijas mazumtirdzniecības veikaliem, veikala pārskatiem un deklarācijas dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="53867-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="53867-122">Konfigurējiet mazumtirdzniecības parametrus.</span><span class="sxs-lookup"><span data-stu-id="53867-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="53867-123">Iestatiet veikalam pieņemamas maksājumu metodes.</span><span class="sxs-lookup"><span data-stu-id="53867-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="53867-124">Lai apstrādātu kredītkaršu transakcijas mazumtirdzniecības pārdošanas punkta (POS) kases sistēmās, varat iestatīt arī maksāšanas pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="53867-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="53867-125">Iestatiet PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="53867-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="53867-126">Iestatiet mazumtirdzniecības preces.</span><span class="sxs-lookup"><span data-stu-id="53867-126">Set up retail products.</span></span> <span data-ttu-id="53867-127">Kā daļu no šī uzdevuma varat arī iestatīt mazumtirdzniecības preču hierarhijas, preču variantus un preču klāstus.</span><span class="sxs-lookup"><span data-stu-id="53867-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="53867-128">Iestatiet preču cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="53867-128">Set up product price groups.</span></span>
10. <span data-ttu-id="53867-129">Iestatiet mazumtirdzniecības preču cenu noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="53867-129">Set up retail product pricing.</span></span> <span data-ttu-id="53867-130">Kā daļu no šo uzdevuma varat iestatīt arī cenu korekcijas, atlaides un atlaižu periodus.</span><span class="sxs-lookup"><span data-stu-id="53867-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="53867-131">Iestatiet darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="53867-131">Set up staff members.</span></span> <span data-ttu-id="53867-132">**Piezīme.** Ir arī jāpiešķir darbiniekiem atbilstošas atļaujas, lai viņi varētu pierakstīties un izpildīt uzdevumus, izmantojot sistēmu Dynamics 365 for Retail for Retail POS.</span><span class="sxs-lookup"><span data-stu-id="53867-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="53867-133">Konfigurējiet Retail POS profilus, ko piešķirt veikalam.</span><span class="sxs-lookup"><span data-stu-id="53867-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="53867-134">Šis uzdevums iekļauj daudzus citus uzdevumus, piemēram, kases sistēmu iestatīšanu, bezsaistes profilu iestatīšanu un kvīšu formātu un profilu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="53867-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="53867-135">Pārskatiet visus priekšnosacījumā ietvertos uzdevumus un izpildiet tikai tos uzdevumus, kuri attiecas uz jums.</span><span class="sxs-lookup"><span data-stu-id="53867-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="53867-136">Iestatīt mazumtirdzniecības veikalu</span><span class="sxs-lookup"><span data-stu-id="53867-136">Set up a retail store</span></span>

<span data-ttu-id="53867-137">Pēc priekšnosacījumu uzdevumu izpildīšanas izpildiet tālāk uzskaitītos uzdevumus, lai iestatītu detalizētu informāciju par mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="53867-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="53867-138">Izveidojiet mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="53867-138">Create a retail store.</span></span>
2.  <span data-ttu-id="53867-139">Piešķiriet veikalam PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="53867-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="53867-140">Piešķiriet veikalam akceptētās maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="53867-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="53867-141">Pievienojiet detalizētu informāciju preču aprakstiem attiecībā uz precēm, kuras tiek piedāvātas jūsu mazumtirdzniecības veikalos.</span><span class="sxs-lookup"><span data-stu-id="53867-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="53867-142">Piemēram, var pievienot bagātināto tekstu un attēlus.</span><span class="sxs-lookup"><span data-stu-id="53867-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="53867-143">Šī detalizēta informācija par preci ir redzama dažādos kontekstos, piemēram, POS reģistrā vai drukātajās etiķetēs.</span><span class="sxs-lookup"><span data-stu-id="53867-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="53867-144">Pievienojiet veikalu noklusējuma organizācijas hierarhijai, kura ir piešķirta nolūkiem **Mazumtirdzniecības preču klāsts**, **Mazumtirdzniecības papildināšana** vai **Mazumtirdzniecības atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="53867-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="53867-145">Pēc mazumtirdzniecības veikala iestatīšanas</span><span class="sxs-lookup"><span data-stu-id="53867-145">After you set up a retail store</span></span>

<span data-ttu-id="53867-146">Kad ir ievadīta detalizēta informācija par mazumtirdzniecības veikalu, izpildiet tālāk uzskaitītos uzdevumus, lai mazumtirdzniecības veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="53867-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="53867-147">Konfigurējiet veikala POS kases sistēmas.</span><span class="sxs-lookup"><span data-stu-id="53867-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="53867-148">Pievienojiet veikalam preču klāstu.</span><span class="sxs-lookup"><span data-stu-id="53867-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="53867-149">Apstrādājiet preču klāstu, lai ģenerētu to preču sarakstu, kuras tiek iekļautas klāstā, un padarītu preces pieejamas mazumtirdzniecības veikalā.</span><span class="sxs-lookup"><span data-stu-id="53867-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="53867-150">Nosūtiet datus, piemēram, numuru sērijas, aparatūras profilus un POS ekrāna izkārtojumus, uz Retail POS reģistriem.</span><span class="sxs-lookup"><span data-stu-id="53867-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="53867-151">Publicējiet mazumtirdzniecības veikalu, lai veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="53867-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="53867-152">Izpildiet darbus, lai veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="53867-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="53867-153">Organizācijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="53867-153">Organization hierarchies</span></span>
<span data-ttu-id="53867-154">Programmatūrā Dynamics 365 for Retail tiek izmantotas organizācijas hierarhijas, lai strukturētu mazumtirdzniecība kanālus.</span><span class="sxs-lookup"><span data-stu-id="53867-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="53867-155">Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="53867-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="53867-156">Iestatot veikalus, varat tos pievienot organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="53867-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="53867-157">Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="53867-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




