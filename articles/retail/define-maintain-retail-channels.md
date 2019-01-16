---
title: "Mazumtirdzniecības kanālu definēšana un uzturēšana"
description: "Šajā tēmā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="909c7-104">Mazumtirdzniecības kanālu definēšana un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="909c7-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="909c7-105">Šajā tēmā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem.</span><span class="sxs-lookup"><span data-stu-id="909c7-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="909c7-106">Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="909c7-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="909c7-107">Dynamics 365 for Retail atbalsta vairākus mazumtirdzniecības kanālus, piemēram, tiešsaistes veikalus, zvanu centrus un fiziskus veikalus.</span><span class="sxs-lookup"><span data-stu-id="909c7-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="909c7-108">Fizisks veikals tiek saukts par mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="909c7-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="909c7-109">Katram mazumtirdzniecības veikalam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="909c7-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="909c7-110">Pirms izveidojat mazumtirdzniecības veikalu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="909c7-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="909c7-111">Pēc mazumtirdzniecības veikala izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā izmantot.</span><span class="sxs-lookup"><span data-stu-id="909c7-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="909c7-112">Veikalam var arī piešķirt darbiniekus, kases sistēmas un debitorus.</span><span class="sxs-lookup"><span data-stu-id="909c7-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="909c7-113">Visbeidzot, pievienojiet jaunu veikalu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="909c7-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="909c7-114">Mazumtirdzniecības veikalu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="909c7-114">Setting up retail stores</span></span>

<span data-ttu-id="909c7-115">Pirms mazumtirdzniecības veikala iestatīšanas programmatūrā Dynamics 365 for Retail, ir jāizpilda daži priekšnosacījumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="909c7-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="909c7-116">Pēc tam varat izveidot mazumtirdzniecības veikalu un pievienot detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="909c7-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="909c7-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="909c7-117">Prerequisites</span></span>

<span data-ttu-id="909c7-118">Lai varētu iestatīt mazumtirdzniecības veikalu, jums ir jāizpilda tālāk uzskaitītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="909c7-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="909c7-119">Konfigurējiet savas organizācijas struktūru un iestatiet organizācijas hierarhijas mazumtirdzniecības preču klāstiem, papildināšanai un atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="909c7-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="909c7-120">Iestatiet noliktavu, kas pārstāv mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="909c7-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="909c7-121">Iestatiet numuru sērijas mazumtirdzniecības veikaliem, veikala pārskatiem un deklarācijas dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="909c7-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="909c7-122">Konfigurējiet mazumtirdzniecības parametrus.</span><span class="sxs-lookup"><span data-stu-id="909c7-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="909c7-123">Iestatiet veikalam pieņemamas maksājumu metodes.</span><span class="sxs-lookup"><span data-stu-id="909c7-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="909c7-124">Lai apstrādātu kredītkaršu transakcijas mazumtirdzniecības pārdošanas punkta (POS) kases sistēmās, varat iestatīt arī maksāšanas pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="909c7-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="909c7-125">Iestatiet PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="909c7-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="909c7-126">Iestatiet mazumtirdzniecības preces.</span><span class="sxs-lookup"><span data-stu-id="909c7-126">Set up retail products.</span></span> <span data-ttu-id="909c7-127">Kā daļu no šī uzdevuma varat arī iestatīt mazumtirdzniecības preču hierarhijas, preču variantus un preču klāstus.</span><span class="sxs-lookup"><span data-stu-id="909c7-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="909c7-128">Iestatiet preču cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="909c7-128">Set up product price groups.</span></span>
10. <span data-ttu-id="909c7-129">Iestatiet mazumtirdzniecības preču cenu noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="909c7-129">Set up retail product pricing.</span></span> <span data-ttu-id="909c7-130">Kā daļu no šo uzdevuma varat iestatīt arī cenu korekcijas, atlaides un atlaižu periodus.</span><span class="sxs-lookup"><span data-stu-id="909c7-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="909c7-131">Iestatiet darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="909c7-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="909c7-132">Ir jāpiešķir arī atbilstošas atļaujas darbiniekiem, lai viņi varētu pierakstīties un izpildīt uzdevumus, izmantojot sistēmu Dynamics 365 for Retail for Retail POS.</span><span class="sxs-lookup"><span data-stu-id="909c7-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="909c7-133">Konfigurējiet Retail POS profilus, ko piešķirt veikalam.</span><span class="sxs-lookup"><span data-stu-id="909c7-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="909c7-134">Šis uzdevums iekļauj daudzus citus uzdevumus, piemēram, kases sistēmu iestatīšanu, bezsaistes profilu iestatīšanu un kvīšu formātu un profilu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="909c7-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="909c7-135">Pārskatiet visus priekšnosacījumā ietvertos uzdevumus un izpildiet tikai tos uzdevumus, kuri attiecas uz jums.</span><span class="sxs-lookup"><span data-stu-id="909c7-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="909c7-136">Iestatīt mazumtirdzniecības veikalu</span><span class="sxs-lookup"><span data-stu-id="909c7-136">Set up a retail store</span></span>

<span data-ttu-id="909c7-137">Pēc priekšnosacījumu uzdevumu izpildīšanas izpildiet tālāk uzskaitītos uzdevumus, lai iestatītu detalizētu informāciju par mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="909c7-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="909c7-138">Izveidojiet mazumtirdzniecības veikalu.</span><span class="sxs-lookup"><span data-stu-id="909c7-138">Create a retail store.</span></span>
2. <span data-ttu-id="909c7-139">Piešķiriet veikalam PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="909c7-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="909c7-140">Piešķiriet veikalam akceptētās maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="909c7-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="909c7-141">Pievienojiet detalizētu informāciju preču aprakstiem attiecībā uz precēm, kuras tiek piedāvātas jūsu mazumtirdzniecības veikalos.</span><span class="sxs-lookup"><span data-stu-id="909c7-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="909c7-142">Piemēram, var pievienot bagātināto tekstu un attēlus.</span><span class="sxs-lookup"><span data-stu-id="909c7-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="909c7-143">Šī detalizēta informācija par preci ir redzama dažādos kontekstos, piemēram, POS reģistrā vai drukātajās etiķetēs.</span><span class="sxs-lookup"><span data-stu-id="909c7-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="909c7-144">Pievienojiet veikalu noklusējuma organizācijas hierarhijai, kura ir piešķirta nolūkiem **Mazumtirdzniecības preču klāsts**, **Mazumtirdzniecības papildināšana** vai **Mazumtirdzniecības atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="909c7-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="909c7-145">Pēc mazumtirdzniecības veikala iestatīšanas</span><span class="sxs-lookup"><span data-stu-id="909c7-145">After you set up a retail store</span></span>

<span data-ttu-id="909c7-146">Kad ir ievadīta detalizēta informācija par mazumtirdzniecības veikalu, izpildiet tālāk uzskaitītos uzdevumus, lai mazumtirdzniecības veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="909c7-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="909c7-147">Konfigurējiet veikala POS kases sistēmas.</span><span class="sxs-lookup"><span data-stu-id="909c7-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="909c7-148">Pievienojiet veikalam preču klāstu.</span><span class="sxs-lookup"><span data-stu-id="909c7-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="909c7-149">Apstrādājiet preču klāstu, lai ģenerētu to preču sarakstu, kuras tiek iekļautas klāstā, un padarītu preces pieejamas mazumtirdzniecības veikalā.</span><span class="sxs-lookup"><span data-stu-id="909c7-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="909c7-150">Nosūtiet datus, piemēram, numuru sērijas, aparatūras profilus un POS ekrāna izkārtojumus, uz Retail POS reģistriem.</span><span class="sxs-lookup"><span data-stu-id="909c7-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="909c7-151">Publicējiet mazumtirdzniecības veikalu, lai veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="909c7-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="909c7-152">Izpildiet darbus, lai veikala datus nosūtītu uz Retail POS.</span><span class="sxs-lookup"><span data-stu-id="909c7-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="909c7-153">Organizācijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="909c7-153">Organization hierarchies</span></span>

<span data-ttu-id="909c7-154">Programmatūrā Dynamics 365 for Retail tiek izmantotas organizācijas hierarhijas, lai strukturētu mazumtirdzniecība kanālus.</span><span class="sxs-lookup"><span data-stu-id="909c7-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="909c7-155">Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="909c7-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="909c7-156">Iestatot veikalus, varat tos pievienot organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="909c7-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="909c7-157">Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="909c7-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

