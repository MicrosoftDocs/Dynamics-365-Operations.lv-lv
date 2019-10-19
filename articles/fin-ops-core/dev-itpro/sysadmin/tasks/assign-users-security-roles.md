---
title: Drošības lomu piešķiršana lietotājiem
description: Lai piekļūtu Finance and Operations programmām, lietotājiem jābūt piešķirtai drošības lomai.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180971"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="1602e-103">Drošības lomu piešķiršana lietotājiem</span><span class="sxs-lookup"><span data-stu-id="1602e-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1602e-104">Lai izmantotu citas iespējas, kas nav kopīgas iespējas, lietotājiem jābūt piešķirtiem drošības lomām.</span><span class="sxs-lookup"><span data-stu-id="1602e-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="1602e-105">Šī procedūra skaidro kā sistēmas administratori var automātiski piešķirt lietotājiem lomas, pamatojoties uz biznesa datiem.</span><span class="sxs-lookup"><span data-stu-id="1602e-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="1602e-106">Automātiski piešķirt lietotājus lomām</span><span class="sxs-lookup"><span data-stu-id="1602e-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="1602e-107">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="1602e-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="1602e-108">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="1602e-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1602e-109">Atlasiet lomu, kurai vēlaties konfigurēt kārtulu.</span><span class="sxs-lookup"><span data-stu-id="1602e-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="1602e-110">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="1602e-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="1602e-111">Noklikšķiniet uz **Pievienot kārtulu**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="1602e-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="1602e-112">Sarakstā **Vaicājuma atlase** atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1602e-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="1602e-113">Atlasiet vaicājumu, lai varētu izmantot šo kārtulu.</span><span class="sxs-lookup"><span data-stu-id="1602e-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="1602e-114">Sarakstā **Dalības kārtulas nosaukums** noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1602e-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1602e-115">Noklikšķiniet uz **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="1602e-115">Click **Edit query**.</span></span> <span data-ttu-id="1602e-116">Rediģējiet vaicājumu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="1602e-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="1602e-117">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1602e-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="1602e-118">Izslēgt lietotājus no automātiskas lomu piešķiršanas</span><span class="sxs-lookup"><span data-stu-id="1602e-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="1602e-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1602e-119">Close the page.</span></span>
2. <span data-ttu-id="1602e-120">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Drošība > Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="1602e-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="1602e-121">Kokā atlasiet 'Uzskaites supervizors'.</span><span class="sxs-lookup"><span data-stu-id="1602e-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1602e-122">Atlasīt lomu.</span><span class="sxs-lookup"><span data-stu-id="1602e-122">Select a role.</span></span> <span data-ttu-id="1602e-123">Šajā piemērā atlasiet Uzskaites supervizoru.</span><span class="sxs-lookup"><span data-stu-id="1602e-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="1602e-124">Izvēlnē **Lomai piešķirtie lietotāji** atlasiet **Manuāli piešķirt/izslēgt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="1602e-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="1602e-125">Sarakstā **Piešķirt lomai vai izslēgt no lomas lietotājus** atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1602e-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="1602e-126">Atlasiet lietotāju.</span><span class="sxs-lookup"><span data-stu-id="1602e-126">Select a user.</span></span>  
6. <span data-ttu-id="1602e-127">Sadaļā **Darbību rūts** atlasiet **Izslēgt no lomas**.</span><span class="sxs-lookup"><span data-stu-id="1602e-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="1602e-128">Noklikšķiniet uz **Izslēgt no lomas**, lai izslēgtu atlasītos lietotājus no lomas.</span><span class="sxs-lookup"><span data-stu-id="1602e-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="1602e-129">Lai atceltu izslēgšanu, atlasiet lietotājus, kuriem vēlaties atcelt izslēgšanu, un pēc tam noklikšķiniet uz **Atiestatīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="1602e-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="1602e-130">Noņemot izslēgšanu, atiestatot lietotāja statusu, lietotāja loma atkal tiek piešķirta automātiski.</span><span class="sxs-lookup"><span data-stu-id="1602e-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="1602e-131">Tomēr, atiestatot statusu, lietotājam netiek uzreiz piešķirta vai izslēgta loma.</span><span class="sxs-lookup"><span data-stu-id="1602e-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="1602e-132">Tā vietā, lietotājam tiek piešķirta vai noņemta loma, nākamreiz, kad tiek palaistas automātiskās lomas norīkojuma kārtulas.</span><span class="sxs-lookup"><span data-stu-id="1602e-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
