---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "361962"
---
# <a name="create-new-users"></a><span data-ttu-id="ec8f3-103">Jaunu lietotāju izveide</span><span class="sxs-lookup"><span data-stu-id="ec8f3-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec8f3-104">Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="ec8f3-105">Sistēmas administratori var veikt šo procedūru, lai pievienotu lietotājus sistēmai.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="ec8f3-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="ec8f3-107">Pievienot jaunu lietotāju</span><span class="sxs-lookup"><span data-stu-id="ec8f3-107">Add a new user</span></span>
1. <span data-ttu-id="ec8f3-108">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="ec8f3-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-109">Click New.</span></span>
3. <span data-ttu-id="ec8f3-110">Laukā Lietotāja ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="ec8f3-111">Ievadiet unikālu lietotāja identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="ec8f3-112">Jānorāda lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-112">A user ID is required.</span></span>  
4. <span data-ttu-id="ec8f3-113">Laukā Lietotāja nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="ec8f3-114">Ievadiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="ec8f3-115">Laukā Domēns ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="ec8f3-116">Ievadiet lietotāja domēnu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="ec8f3-117">Laukā Aizstājvārds ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="ec8f3-118">Ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="ec8f3-119">Laukā Uzņēmums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ec8f3-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ec8f3-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ec8f3-122">Lietotāja uzņēmuma atlase</span><span class="sxs-lookup"><span data-stu-id="ec8f3-122">Select the user's company</span></span>  
10. <span data-ttu-id="ec8f3-123">Noklikšķiniet uz Piešķirt lomas.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-123">Click Assign roles.</span></span>
11. <span data-ttu-id="ec8f3-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ec8f3-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-125">Click OK.</span></span>
13. <span data-ttu-id="ec8f3-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="ec8f3-127">Importēt lietotājus</span><span class="sxs-lookup"><span data-stu-id="ec8f3-127">Import users</span></span>
1. <span data-ttu-id="ec8f3-128">Noklikšķiniet uz Importēt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-128">Click Import users.</span></span>
2. <span data-ttu-id="ec8f3-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ec8f3-130">Noklikšķiniet uz Importēt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-130">Click Import users.</span></span>
4. <span data-ttu-id="ec8f3-131">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="ec8f3-131">Click Close.</span></span>

