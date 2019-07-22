---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
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
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711135"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="d7fe9-103">Drošības lomu piešķiršana lietotājiem</span><span class="sxs-lookup"><span data-stu-id="d7fe9-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7fe9-104">Lai piekļūtu Microsoft Dynamics 365 for Finance and Operations Enterprise edition, lietotājiem jābūt piešķirtām drošības lomām.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="d7fe9-105">Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="d7fe9-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="d7fe9-107">Automātiski piešķirt lietotājus lomām</span><span class="sxs-lookup"><span data-stu-id="d7fe9-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="d7fe9-108">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="d7fe9-109">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d7fe9-110">Atlasiet lomu, kurai vēlaties konfigurēt kārtulu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="d7fe9-111">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="d7fe9-112">Noklikšķiniet uz **Pievienot kārtulu**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="d7fe9-113">Sarakstā **Vaicājuma atlase** atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="d7fe9-114">Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="d7fe9-115">Sarakstā **Dalības kārtulas nosaukums** noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d7fe9-116">Noklikšķiniet uz **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-116">Click **Edit query**.</span></span> <span data-ttu-id="d7fe9-117">Rediģējiet vaicājumu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="d7fe9-118">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="d7fe9-119">Izslēgt lietotājus no automātiskas lomu piešķiršanas</span><span class="sxs-lookup"><span data-stu-id="d7fe9-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="d7fe9-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-120">Close the page.</span></span>
2. <span data-ttu-id="d7fe9-121">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="d7fe9-122">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d7fe9-123">Atlasīt lomu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-123">Select a role.</span></span> <span data-ttu-id="d7fe9-124">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="d7fe9-125">Izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="d7fe9-126">Sarakstā **Piešķirt lomai vai izslēgt no lomas lietotājus** atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="d7fe9-127">Atlasiet lietotāju.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-127">Select a user.</span></span>  
6. <span data-ttu-id="d7fe9-128">Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="d7fe9-129">Noklikšķiniet uz **Izslēgt no lomas**, lai izslēgtu atlasītos lietotājus no lomas.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="d7fe9-130">Lai atceltu izslēgšanu, atlasiet lietotājus, kuriem vēlaties atcelt izslēgšanu, un pēc tam noklikšķiniet uz **Atiestatīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="d7fe9-131">Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="d7fe9-132">Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="d7fe9-133">Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
