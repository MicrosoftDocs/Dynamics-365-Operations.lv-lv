---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180948"
---
# <a name="create-new-users"></a><span data-ttu-id="f322e-103">Jaunu lietotāju izveide</span><span class="sxs-lookup"><span data-stu-id="f322e-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f322e-104">Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.</span><span class="sxs-lookup"><span data-stu-id="f322e-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f322e-105">Saistīt lietotāju ar licenci (tikai jauni licences veidi)</span><span class="sxs-lookup"><span data-stu-id="f322e-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="f322e-106">Attiecībā uz debitoriem, kuriem ir viens no jaunajiem licences tipiem, kas tika pievienoti 2019. oktobrī, lietotājiem jābūt saistītiem ar licenci.</span><span class="sxs-lookup"><span data-stu-id="f322e-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="f322e-107">Lietotāji, kas ir saistīti ar licenci, tiek automātiski pievienoti kā sistēmas lietotāji, kuriem nav lomas, pirmo reizi pierakstoties sistēmā.</span><span class="sxs-lookup"><span data-stu-id="f322e-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="f322e-108">Lietotāji, kuri nav saistīti ar licenci, saņem brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f322e-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="f322e-109">Sistēmas administratori var [piešķirt licences lietotājiem](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="f322e-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="f322e-110">Pievienot jaunu lietotāju</span><span class="sxs-lookup"><span data-stu-id="f322e-110">Add a new user</span></span>
1. <span data-ttu-id="f322e-111">Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="f322e-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f322e-112">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f322e-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f322e-113">Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="f322e-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="f322e-114">Jānorāda lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="f322e-114">A user ID is required.</span></span>  
4. <span data-ttu-id="f322e-115">Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="f322e-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="f322e-116">Laukā **Domēns** ievadiet lietotāja domēnu.</span><span class="sxs-lookup"><span data-stu-id="f322e-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="f322e-117">Laukā **Aizstājvārds** ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="f322e-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="f322e-118">Laukā **Uzņēmums** atlasiet vēlamo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="f322e-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="f322e-119">Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas** [piešķirtu lietotājus drošības lomām](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="f322e-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="f322e-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f322e-120">Select **OK**.</span></span>
10. <span data-ttu-id="f322e-121">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f322e-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="f322e-122">Importēt lietotājus</span><span class="sxs-lookup"><span data-stu-id="f322e-122">Import users</span></span>
1. <span data-ttu-id="f322e-123">Darbību rūtī atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="f322e-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="f322e-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f322e-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f322e-125">Atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="f322e-125">Select **Import users**.</span></span>
4. <span data-ttu-id="f322e-126">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f322e-126">Select **Close**.</span></span>

