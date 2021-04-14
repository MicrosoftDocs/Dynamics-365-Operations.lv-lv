---
title: Pienākumu sadales konfliktu identificēšana un atrisināšana
description: Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745817"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="507df-103">Pienākumu sadales konfliktu identificēšana un atrisināšana</span><span class="sxs-lookup"><span data-stu-id="507df-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="507df-104">Šajā tēmā ir paskaidrots, kā identificēt un atrisināt pienākumu sadales konfliktus.</span><span class="sxs-lookup"><span data-stu-id="507df-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="507df-105">Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="507df-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="507df-106">Šī koncepcija ir nosaukta par pienākumu sadali.</span><span class="sxs-lookup"><span data-stu-id="507df-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="507df-107">Ja drošības lomas definīcija vai lietotāju lomu piešķires pārkāpj noteikumus, tiek reģistrēts konflikts.</span><span class="sxs-lookup"><span data-stu-id="507df-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="507df-108">Visi konflikti ir jāatrisina administratoram.</span><span class="sxs-lookup"><span data-stu-id="507df-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="507df-109">Lai identificētu un atrisinātu konfliktus, veiciet sekojošo procedūru.</span><span class="sxs-lookup"><span data-stu-id="507df-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="507df-110">Pēc kārtulas pievienošanas pārbaudiet, vai visas esošās lomas ir saderīgas.</span><span class="sxs-lookup"><span data-stu-id="507df-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="507df-111">Pārbaudiet, vai esošās lomas atbilst jaunajiem nosacījumiem par pienākumu sadali</span><span class="sxs-lookup"><span data-stu-id="507df-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="507df-112">Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="507df-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="507df-113">Atlasiet **Apstiprināt pienākumus un lomas**.</span><span class="sxs-lookup"><span data-stu-id="507df-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="507df-114">Ja jebkuras esošās lomas pārkāpj kārtulas, tiek parādīts ziņojums, kas ietver kārtulas nosaukumu, lomu un konfliktējošo pienākumu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="507df-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="507df-115">Konfliktējošās lomas ir jāpārkonfigurē, izmantojot **Drošības konfigurāciju**, un tās nevar ietvert konfliktējošos pienākumus.</span><span class="sxs-lookup"><span data-stu-id="507df-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="507df-116">Ja neviena loma nepārkāpj atlasīto kārtulu, ziņojumā norādīts, ka visas lomas ir atbilstošas.</span><span class="sxs-lookup"><span data-stu-id="507df-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="507df-117">Apstiprināšana tiek veikta tikai atlasītajai kārtulai.</span><span class="sxs-lookup"><span data-stu-id="507df-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="507df-118">Ir svarīgi pārbaudīt katras kārtulas atbilstību.</span><span class="sxs-lookup"><span data-stu-id="507df-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="507df-119">Kad tiek izveidota vai modificēta loma, automātiski tiek ieviestas pienākumu sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="507df-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="507df-120">Lomai nevar piešķirt konfliktējošos pienākumus.</span><span class="sxs-lookup"><span data-stu-id="507df-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="507df-121">Pēc tam pārbaudiet, vai visas esošās lomu piešķires ir saderīgas.</span><span class="sxs-lookup"><span data-stu-id="507df-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="507df-122">Pārbaude, vai lietotāju lomu piešķires atbilst jaunajām kārtulām par pienākumu sadali</span><span class="sxs-lookup"><span data-stu-id="507df-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="507df-123">Dodieties uz **Sistēmas administrēšana > Drošība > Pienākumu sadale > Pārbaudīt lietotāja lomu norīkojumu atbilstību**.</span><span class="sxs-lookup"><span data-stu-id="507df-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="507df-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="507df-124">Select **OK**.</span></span> <span data-ttu-id="507df-125">Paziņojumā tiek parādīti pārbaudes rezultāti.</span><span class="sxs-lookup"><span data-stu-id="507df-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="507df-126">Konflikti tiek arī reģistrēti lapā **Pienākumu sadales konflikti**.</span><span class="sxs-lookup"><span data-stu-id="507df-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="507df-127">Kad lietotājiem tiek piešķirtas lomas, automātiski tiek ieviestas pienākumu sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="507df-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="507df-128">Mēģinot piešķirt lietotāju lomām, kas ietver konfliktējošus pienākumus, saņemat kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="507df-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="507df-129">Pēc tam jums ir jāatrisina konflikts, liedzot vai atļaujot papildu lomas piešķiri.</span><span class="sxs-lookup"><span data-stu-id="507df-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="507df-130">Pēc piešķires piešķiršanas tiks piešķirta papildu loma.</span><span class="sxs-lookup"><span data-stu-id="507df-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="507df-131">Konflikti pašlaik nav pārbaudīti lietotājiem, kuriem ir piešķirtas lomas, pamatojoties uz Active Directory Domain grupām.</span><span class="sxs-lookup"><span data-stu-id="507df-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="507df-132">Konfliktējošo lietotāju lomu piešķiru skatīšana un atrisināšana</span><span class="sxs-lookup"><span data-stu-id="507df-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="507df-133">Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales neatrisinātie konflikti**.</span><span class="sxs-lookup"><span data-stu-id="507df-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="507df-134">Atlasiet konfliktu un pēc tam atlasiet vienu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="507df-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="507df-135">**Noraidīt piešķiri**: noraidīt papildu drošības lomas piešķiri lietotājam.</span><span class="sxs-lookup"><span data-stu-id="507df-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="507df-136">Liedzot automātisko lomu piešķiri, lietotājs tiek atzīmēts kā izslēgts no lomas.</span><span class="sxs-lookup"><span data-stu-id="507df-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="507df-137">Izslēgtam lietotājam nav piešķirta piekļuve, kas ir saistīta ar lomu, un lietotāju nevar piešķirt lomai, kamēr administrators nenoņems izslēgšanu.</span><span class="sxs-lookup"><span data-stu-id="507df-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="507df-138">**Atļaut piešķiri**: ignorēt konfliktu un atļaut piešķirt lietotāju abām drošības lomām.</span><span class="sxs-lookup"><span data-stu-id="507df-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="507df-139">Ja ignorējat konfliktu, laukā **Ignorēšanas pamatojums** jāievada pamatojums.</span><span class="sxs-lookup"><span data-stu-id="507df-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="507df-140">Visas ignorētās lomu piešķires var skatīt **Pienākumu sadales konfliktu** lapā.</span><span class="sxs-lookup"><span data-stu-id="507df-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="507df-141">Ja vienam un tam pašam lietotājam ir norādīti vairāki konflikti, atlasiet lietotāja ierakstu un novērtējiet **Lietotāju** lapā piešķirtās lomas.</span><span class="sxs-lookup"><span data-stu-id="507df-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="507df-142">Lai izvairītos no šī konflikta, apstipriniet katru kārtulu pēc tās pievienošanas vai modificēšanas.</span><span class="sxs-lookup"><span data-stu-id="507df-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]