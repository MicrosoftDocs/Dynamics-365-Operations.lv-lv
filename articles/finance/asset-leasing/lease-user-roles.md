---
title: Nomas lietotāju lomu piešķiršana
description: Šajā tēmā aprakstītas drošības lomas, kas tiek izmantotas līdzekļu nomā. Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445798"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="7fd80-104">Nomas lietotāju lomu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="7fd80-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fd80-105">Šajā tēmā aprakstītas drošības lomas, kas tiek izmantotas līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="7fd80-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="7fd80-106">Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.</span><span class="sxs-lookup"><span data-stu-id="7fd80-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="7fd80-107">Trīs lietotāju lomas nodrošina atšķirīgu piekļuvi līdzekļu nomai.</span><span class="sxs-lookup"><span data-stu-id="7fd80-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="7fd80-108">Viena loma ir piemērota nomu uzturēšanai, otra ir piemērota nomu skatīšanai, bet trešā ir piemērota nomas sekretāra pienākumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="7fd80-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="7fd80-109">Katrai lomai ir noteiktas atļaujas visām nomas lapām, un katra no tām ļauj lietotājiem skatīt, izveidot, rediģēt vai dzēst nomu saskaņā ar darba pienākumiem.</span><span class="sxs-lookup"><span data-stu-id="7fd80-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="7fd80-110">Loma</span><span class="sxs-lookup"><span data-stu-id="7fd80-110">Role</span></span>           | <span data-ttu-id="7fd80-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7fd80-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="7fd80-112">Nomas uzturēšana</span><span class="sxs-lookup"><span data-stu-id="7fd80-112">Maintain Lease</span></span> | <span data-ttu-id="7fd80-113">Lietotāji ar šo lomu var pievienot, rediģēt, dzēst un apskatīt nomu.</span><span class="sxs-lookup"><span data-stu-id="7fd80-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="7fd80-114">Šī loma ir paredzēta ikdienas lietotājiem, kuru uzdevumi ir ikmēneša žurnāla ierakstu izveide un grāmatošana, kā arī jaunu nomu pievienošana.</span><span class="sxs-lookup"><span data-stu-id="7fd80-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="7fd80-115">Šī loma sniedz piekļuvi visām līdzekļu nomas funkcionalitātēm.</span><span class="sxs-lookup"><span data-stu-id="7fd80-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="7fd80-116">Nomas skatīšana</span><span class="sxs-lookup"><span data-stu-id="7fd80-116">View Lease</span></span>     | <span data-ttu-id="7fd80-117">Lietotāji ar šo nomu var tikai skatīt nomas ierakstus, grafikus un palaist pārskatus.</span><span class="sxs-lookup"><span data-stu-id="7fd80-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="7fd80-118">Viņi nevar izveidot jaunas nomas, rediģēt esošās nomas vai izveidot žurnāla ierakstus nomām.</span><span class="sxs-lookup"><span data-stu-id="7fd80-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="7fd80-119">Loma ir paredzēta lietotājiem, kuriem ir tikai jāskata nomas, nomu grafiki un darījumi, kas notiek attiecībā saistība ar šīm nomām.</span><span class="sxs-lookup"><span data-stu-id="7fd80-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="7fd80-120">Nomas darbinieks</span><span class="sxs-lookup"><span data-stu-id="7fd80-120">Lease Clerk</span></span>    | <span data-ttu-id="7fd80-121">Lietotāji ar šo lomu var tikai izveidot tikai jaunas nomas.</span><span class="sxs-lookup"><span data-stu-id="7fd80-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="7fd80-122">Viņi nevar labot vai dzēst esošās nomas, skatīt nomu grafikus vai grāmatot nomu žurnālu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="7fd80-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="7fd80-123">Šī loma ir paredzēta lietotājiem, kuri strādā datu ievadē.</span><span class="sxs-lookup"><span data-stu-id="7fd80-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="7fd80-124">Veiciet šīs darbības, lai piešķirtu lietotājus lomām, kas tiek izmantotas līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="7fd80-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="7fd80-125">Dodieties uz **Sistēmas administrēšana \> Drošība \> Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="7fd80-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="7fd80-126">Atlasiet lomu **Nomas uzturēšana**, **Nomas darbinieks** vai **Nomas skatīšana** un pēc tam atlasiet **Manuāli piešķirt/izslēgt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="7fd80-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="7fd80-127">Atlasiet lietotāju, kuram piešķirt lomu, un pēc tam atlasiet **Piešķirt lomai**.</span><span class="sxs-lookup"><span data-stu-id="7fd80-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
