---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556713"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="d6e63-103">Drošības lomu piešķiršana lietotājiem</span><span class="sxs-lookup"><span data-stu-id="d6e63-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6e63-104">Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām.</span><span class="sxs-lookup"><span data-stu-id="d6e63-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="d6e63-105">Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem.</span><span class="sxs-lookup"><span data-stu-id="d6e63-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="d6e63-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="d6e63-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="d6e63-107">Automātiski piešķirt lietotājus lomām</span><span class="sxs-lookup"><span data-stu-id="d6e63-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="d6e63-108">Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="d6e63-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="d6e63-109">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="d6e63-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="d6e63-110">Atlasiet lomu, kurai vēlaties konfigurēt kārtulu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="d6e63-111">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="d6e63-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="d6e63-112">Noklikšķiniet uz Pievienot kārtulu, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="d6e63-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6e63-114">Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="d6e63-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d6e63-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d6e63-116">Noklikšķiniet uz Rediģēt vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-116">Click Edit query.</span></span>
    * <span data-ttu-id="d6e63-117">Rediģējiet vaicājumu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="d6e63-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="d6e63-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d6e63-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="d6e63-119">Izslēgt lietotājus no automātiskas lomu piešķiršanas</span><span class="sxs-lookup"><span data-stu-id="d6e63-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="d6e63-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-120">Close the page.</span></span>
2. <span data-ttu-id="d6e63-121">Dodieties uz Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="d6e63-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="d6e63-122">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="d6e63-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="d6e63-123">Atlasīt lomu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-123">Select a role.</span></span> <span data-ttu-id="d6e63-124">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="d6e63-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="d6e63-125">Noklikšķiniet Manuāli piešķirt/izslēgt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="d6e63-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="d6e63-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d6e63-127">Atlasiet lietotāju.</span><span class="sxs-lookup"><span data-stu-id="d6e63-127">Select a user.</span></span>  
6. <span data-ttu-id="d6e63-128">Noklikšķiniet Izslēgt no lomas.</span><span class="sxs-lookup"><span data-stu-id="d6e63-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="d6e63-129">Noklikšķiniet uz Izslēgt no lomas, lai izslēgtu atlasītos lietotājus no lomas.</span><span class="sxs-lookup"><span data-stu-id="d6e63-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="d6e63-130">Lai noņemtu izslēgšanu, atlasiet lietotājus, kuriem vēlaties noņemt izslēgšanu, un pēc tam noklikšķiniet uz Atiestatīt statusu.</span><span class="sxs-lookup"><span data-stu-id="d6e63-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="d6e63-131">Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski.</span><span class="sxs-lookup"><span data-stu-id="d6e63-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="d6e63-132">Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma.</span><span class="sxs-lookup"><span data-stu-id="d6e63-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="d6e63-133">Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d6e63-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

