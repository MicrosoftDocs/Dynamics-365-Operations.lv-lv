---
title: Mazumtirdzniecības kanālu definēšana un uzturēšana
description: Šajā tēmā ir sniegts apskats par to, kā iestatīt fiziskos veikalus, kas programmā Dynamics 365 Commerce tiek saukti par veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc veikala iestatīšanas.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 63639d69af90c6aa37bbf7af7868bca71942063f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023243"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="a67ad-104">Mazumtirdzniecības kanālu definēšana un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="a67ad-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a67ad-105">Šajā tēmā ir sniegts apskats par to, kā iestatīt fiziskos veikalus, kas programmā Dynamics 365 Commerce tiek saukti par veikaliem.</span><span class="sxs-lookup"><span data-stu-id="a67ad-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a67ad-106">Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc veikala iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="a67ad-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="a67ad-107">Commerce atbalsta vairākus kanālus, piemēram, tiešsaistes veikalus, zvanu centrus un fiziskos veikalus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="a67ad-108">Fizisks veikals tiek saukts par veikalu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="a67ad-109">Katram veikalam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="a67ad-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="a67ad-110">Pirms izveidojat veikalu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="a67ad-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="a67ad-111">Pēc veikala izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā izmantot.</span><span class="sxs-lookup"><span data-stu-id="a67ad-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="a67ad-112">Veikalam var arī piešķirt darbiniekus, kases sistēmas un debitorus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="a67ad-113">Visbeidzot, pievienojiet jaunu veikalu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="a67ad-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="a67ad-114">Veikalu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a67ad-114">Setting up stores</span></span>

<span data-ttu-id="a67ad-115">Pirms veikala iestatīšanas programmā Commerce, ir jāveic daži priekšnosacījumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="a67ad-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="a67ad-116">Pēc tam varat izveidot veikalu un pievienot detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="a67ad-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a67ad-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a67ad-117">Prerequisites</span></span>

<span data-ttu-id="a67ad-118">Lai varētu iestatīt veikalu, jums ir jāizpilda tālāk uzskaitītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="a67ad-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="a67ad-119">Konfigurējiet savas organizācijas struktūru un iestatiet organizācijas hierarhijas mazumtirdzniecības preču klāstiem, papildināšanai un atskaišu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="a67ad-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="a67ad-120">Iestatiet noliktavu, kas pārstāv veikalu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="a67ad-121">Iestatiet numuru sērijas veikaliem, veikala pārskatiem un deklarācijas dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="a67ad-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="a67ad-122">Konfigurējiet programmas Commerce parametrus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="a67ad-123">Iestatiet veikalam pieņemamas maksājumu metodes.</span><span class="sxs-lookup"><span data-stu-id="a67ad-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="a67ad-124">Lai apstrādātu kredītkaršu transakcijas mazumtirdzniecības pārdošanas punkta (POS) kases sistēmās, varat iestatīt arī maksāšanas pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="a67ad-125">Iestatiet PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="a67ad-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="a67ad-126">Iestatiet mazumtirdzniecības preces.</span><span class="sxs-lookup"><span data-stu-id="a67ad-126">Set up retail products.</span></span> <span data-ttu-id="a67ad-127">Kā daļu no šī uzdevuma varat arī iestatīt preču hierarhijas, preču variantus un preču klāstus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="a67ad-128">Iestatiet preču cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="a67ad-128">Set up product price groups.</span></span>
10. <span data-ttu-id="a67ad-129">Iestatiet preču cenu noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-129">Set up product pricing.</span></span> <span data-ttu-id="a67ad-130">Kā daļu no šo uzdevuma varat iestatīt arī cenu korekcijas, atlaides un atlaižu periodus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="a67ad-131">Iestatiet darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a67ad-132">Turklāt ir jāpiešķir darbiniekiem atbilstošās atļaujas, lai viņi varētu pierakstīties un izpildīt uzdevumus, izmantojot sistēmu POS.</span><span class="sxs-lookup"><span data-stu-id="a67ad-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="a67ad-133">Konfigurējiet POS profilus, kuri tiks piešķirti veikalam.</span><span class="sxs-lookup"><span data-stu-id="a67ad-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="a67ad-134">Šis uzdevums iekļauj daudzus citus uzdevumus, piemēram, kases sistēmu iestatīšanu, bezsaistes profilu iestatīšanu un kvīšu formātu un profilu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="a67ad-135">Pārskatiet visus priekšnosacījumos ietvertos uzdevumus un izpildiet tikai tos uzdevumus, kuri attiecas uz jums.</span><span class="sxs-lookup"><span data-stu-id="a67ad-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="a67ad-136">Veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a67ad-136">Set up a store</span></span>

<span data-ttu-id="a67ad-137">Pēc priekšnosacījumu uzdevumu izpildes izpildiet tālāk uzskaitītos uzdevumus, lai iestatītu detalizētu informāciju par veikalu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="a67ad-138">Izveidojiet veikalu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-138">Create a store.</span></span>
2. <span data-ttu-id="a67ad-139">Piešķiriet veikalam PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="a67ad-140">Piešķiriet veikalam akceptētās maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="a67ad-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="a67ad-141">Pievienojiet detalizētu informāciju preču aprakstiem attiecībā uz precēm, kuras tiek piedāvātas jūsu veikalos.</span><span class="sxs-lookup"><span data-stu-id="a67ad-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="a67ad-142">Piemēram, var pievienot bagātināto tekstu un attēlus.</span><span class="sxs-lookup"><span data-stu-id="a67ad-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="a67ad-143">Šī detalizēta informācija par preci ir redzama dažādos kontekstos, piemēram, POS reģistrā vai drukātajās etiķetēs.</span><span class="sxs-lookup"><span data-stu-id="a67ad-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="a67ad-144">Pievienojiet veikalu noklusējuma organizācijas hierarhijai, kura ir piešķirta nolūkiem **Mazumtirdzniecības preču klāsts**, **Mazumtirdzniecības papildināšana** vai **Mazumtirdzniecības atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="a67ad-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="a67ad-145">Pēc veikala iestatīšanas</span><span class="sxs-lookup"><span data-stu-id="a67ad-145">After you set up a store</span></span>

<span data-ttu-id="a67ad-146">Pēc detalizētas informācijas par mazumtirdzniecības veikalu ievades, veiciet šos uzdevumus, lai nosūtītu datus par jaunu mazumtirdzniecības veikalu uz POS:</span><span class="sxs-lookup"><span data-stu-id="a67ad-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="a67ad-147">Konfigurējiet veikala POS kases sistēmas.</span><span class="sxs-lookup"><span data-stu-id="a67ad-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="a67ad-148">Pievienojiet veikalam preču klāstu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="a67ad-149">Apstrādājiet preču klāstu, lai ģenerētu to preču sarakstu, kuras tiek iekļautas klāstā, un padarītu preces pieejamas veikalā.</span><span class="sxs-lookup"><span data-stu-id="a67ad-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="a67ad-150">Nosūtiet datus, piemēram, numuru sērijas, aparatūras profilus un POS ekrāna izkārtojumus, uz POS reģistriem.</span><span class="sxs-lookup"><span data-stu-id="a67ad-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="a67ad-151">Publicējiet veikalu, lai nosūtītu veikala datus uz POS.</span><span class="sxs-lookup"><span data-stu-id="a67ad-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="a67ad-152">Izpildiet darbus, lai nosūtītu veikala datus uz POS.</span><span class="sxs-lookup"><span data-stu-id="a67ad-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="a67ad-153">Organizācijas hierarhijas</span><span class="sxs-lookup"><span data-stu-id="a67ad-153">Organization hierarchies</span></span>

<span data-ttu-id="a67ad-154">Programma Commerce izmanto organizāciju hierarhijas, lai mazumtirdzniecības kanāliem piešķirtu struktūru.</span><span class="sxs-lookup"><span data-stu-id="a67ad-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="a67ad-155">Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="a67ad-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="a67ad-156">Iestatot veikalus, varat tos pievienot organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="a67ad-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="a67ad-157">Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="a67ad-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="a67ad-158">Lai izmantotu mazumtirdzniecības pārdošanas funkcionalitāti, jāaktivizē **Vairākas izsūtīšanas** konfigurācijas atslēga.</span><span class="sxs-lookup"><span data-stu-id="a67ad-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="a67ad-159">Šo konfigurācijas atslēgu var atrast atslēgās **Tirdzniecības konfigurācija** sadaļā **Sistēmas administrēšana**\>**Iestatījumi**\>**Licences konfigurācija.**</span><span class="sxs-lookup"><span data-stu-id="a67ad-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="a67ad-160">Tas ir nepieciešams, mazumtirdzniecības funkcionalitātes dēļ, kas veic dažādas validācijas, pamatojoties uz piegādes adresi, kas konfigurēta pārdošanas pasūtījuma rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="a67ad-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>

