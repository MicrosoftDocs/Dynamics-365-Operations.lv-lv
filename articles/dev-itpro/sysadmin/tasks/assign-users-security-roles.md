--- 
title: "Piešķirt lietotājus drošības lomām"
description: "Lai piekļūtu programmai Microsoft Dynamics 365 for Finance and Operations, lietotājiem jābūt piešķirtai drošības lomai."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0ab51a56c33a84dea9cf945e808fa7bc42d3727c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="546ff-103">Drošības lomu piešķiršana lietotājiem</span><span class="sxs-lookup"><span data-stu-id="546ff-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="546ff-104">Lai piekļūtu programmai Microsoft Dynamics 365 for Finance and Operations, lietotājiem jābūt piešķirtai drošības lomai.</span><span class="sxs-lookup"><span data-stu-id="546ff-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="546ff-105">Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem.</span><span class="sxs-lookup"><span data-stu-id="546ff-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="546ff-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="546ff-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="546ff-107">Automātiski piešķirt lietotājus lomām</span><span class="sxs-lookup"><span data-stu-id="546ff-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="546ff-108">Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="546ff-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="546ff-109">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="546ff-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="546ff-110">Atlasiet lomu, kurai vēlaties konfigurēt kārtulu.</span><span class="sxs-lookup"><span data-stu-id="546ff-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="546ff-111">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="546ff-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="546ff-112">Noklikšķiniet uz Pievienot kārtulu, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="546ff-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="546ff-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="546ff-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="546ff-114">Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.</span><span class="sxs-lookup"><span data-stu-id="546ff-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="546ff-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="546ff-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="546ff-116">Noklikšķiniet uz Rediģēt vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="546ff-116">Click Edit query.</span></span>
    * <span data-ttu-id="546ff-117">Rediģējiet vaicājumu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="546ff-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="546ff-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="546ff-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="546ff-119">Izslēgt lietotājus no automātiskas lomu piešķiršanas</span><span class="sxs-lookup"><span data-stu-id="546ff-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="546ff-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="546ff-120">Close the page.</span></span>
2. <span data-ttu-id="546ff-121">Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="546ff-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="546ff-122">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="546ff-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="546ff-123">Atlasīt lomu.</span><span class="sxs-lookup"><span data-stu-id="546ff-123">Select a role.</span></span> <span data-ttu-id="546ff-124">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="546ff-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="546ff-125">Noklikšķiniet Manuāli piešķirt/izslēgt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="546ff-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="546ff-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="546ff-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="546ff-127">Atlasiet lietotāju.</span><span class="sxs-lookup"><span data-stu-id="546ff-127">Select a user.</span></span>  
6. <span data-ttu-id="546ff-128">Noklikšķiniet Izslēgt no lomas.</span><span class="sxs-lookup"><span data-stu-id="546ff-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="546ff-129">Noklikšķiniet uz Izslēgt no lomas, lai izslēgtu atlasītos lietotājus no lomas.</span><span class="sxs-lookup"><span data-stu-id="546ff-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="546ff-130">Lai noņemtu izslēgšanu, atlasiet lietotājus, kuriem vēlaties noņemt izslēgšanu, un pēc tam noklikšķiniet uz Atiestatīt statusu.</span><span class="sxs-lookup"><span data-stu-id="546ff-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="546ff-131">Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski.</span><span class="sxs-lookup"><span data-stu-id="546ff-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="546ff-132">Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma.</span><span class="sxs-lookup"><span data-stu-id="546ff-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="546ff-133">Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.</span><span class="sxs-lookup"><span data-stu-id="546ff-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


