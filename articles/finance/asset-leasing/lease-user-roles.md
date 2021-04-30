---
title: Nomas lietotāju lomu piešķiršana
description: Šajā tēmā aprakstītas drošības lomas, kas tiek izmantotas līdzekļu nomā. Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 05728f5027dc079dd413dde1c3aa78cddcea136b
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881064"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="e8b67-104">Nomas lietotāju lomu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="e8b67-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8b67-105">Šajā tēmā aprakstītas drošības lomas, kas tiek izmantotas līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="e8b67-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="e8b67-106">Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.</span><span class="sxs-lookup"><span data-stu-id="e8b67-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="e8b67-107">Trīs lietotāju lomas nodrošina atšķirīgu piekļuvi līdzekļu nomai.</span><span class="sxs-lookup"><span data-stu-id="e8b67-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="e8b67-108">Viena loma ir piemērota nomu uzturēšanai, otra ir piemērota nomu skatīšanai, bet trešā ir piemērota nomas sekretāra pienākumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="e8b67-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="e8b67-109">Katrai lomai ir noteiktas atļaujas visām nomas lapām, un katra no tām ļauj lietotājiem skatīt, izveidot, rediģēt vai dzēst nomu saskaņā ar darba pienākumiem.</span><span class="sxs-lookup"><span data-stu-id="e8b67-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="e8b67-110">Loma</span><span class="sxs-lookup"><span data-stu-id="e8b67-110">Role</span></span>           | <span data-ttu-id="e8b67-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e8b67-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="e8b67-112">Nomas uzturēšana</span><span class="sxs-lookup"><span data-stu-id="e8b67-112">Maintain Lease</span></span> | <span data-ttu-id="e8b67-113">Lietotāji ar šo lomu var pievienot, rediģēt, dzēst un apskatīt nomu.</span><span class="sxs-lookup"><span data-stu-id="e8b67-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="e8b67-114">Šī loma ir paredzēta ikdienas lietotājiem, kuru uzdevumi ir ikmēneša žurnāla ierakstu izveide un grāmatošana, kā arī jaunu nomu pievienošana.</span><span class="sxs-lookup"><span data-stu-id="e8b67-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="e8b67-115">Šī loma sniedz piekļuvi visām līdzekļu nomas funkcionalitātēm.</span><span class="sxs-lookup"><span data-stu-id="e8b67-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="e8b67-116">Nomas skatīšana</span><span class="sxs-lookup"><span data-stu-id="e8b67-116">View Lease</span></span>     | <span data-ttu-id="e8b67-117">Lietotāji ar šo nomu var tikai skatīt nomas ierakstus, grafikus un palaist pārskatus.</span><span class="sxs-lookup"><span data-stu-id="e8b67-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="e8b67-118">Viņi nevar izveidot jaunas nomas, rediģēt esošās nomas vai izveidot žurnāla ierakstus nomām.</span><span class="sxs-lookup"><span data-stu-id="e8b67-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="e8b67-119">Loma ir paredzēta lietotājiem, kuriem ir tikai jāskata nomas, nomu grafiki un darījumi, kas notiek attiecībā saistība ar šīm nomām.</span><span class="sxs-lookup"><span data-stu-id="e8b67-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="e8b67-120">Nomas darbinieks</span><span class="sxs-lookup"><span data-stu-id="e8b67-120">Lease Clerk</span></span>    | <span data-ttu-id="e8b67-121">Lietotāji ar šo lomu var tikai izveidot tikai jaunas nomas.</span><span class="sxs-lookup"><span data-stu-id="e8b67-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="e8b67-122">Viņi nevar labot vai dzēst esošās nomas, skatīt nomu grafikus vai grāmatot nomu žurnālu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e8b67-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="e8b67-123">Šī loma ir paredzēta lietotājiem, kuri strādā datu ievadē.</span><span class="sxs-lookup"><span data-stu-id="e8b67-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="e8b67-124">Veiciet šīs darbības, lai piešķirtu lietotājus lomām, kas tiek izmantotas līdzekļu nomā.</span><span class="sxs-lookup"><span data-stu-id="e8b67-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="e8b67-125">Dodieties uz **Sistēmas administrēšana \> Drošība \> Piešķirt lomas lietotājiem**.</span><span class="sxs-lookup"><span data-stu-id="e8b67-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="e8b67-126">Atlasiet lomu **Nomas uzturēšana**, **Nomas darbinieks** vai **Nomas skatīšana** un pēc tam atlasiet **Manuāli piešķirt/izslēgt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="e8b67-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="e8b67-127">Atlasiet lietotāju, kuram piešķirt lomu, un pēc tam atlasiet **Piešķirt lomai**.</span><span class="sxs-lookup"><span data-stu-id="e8b67-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
