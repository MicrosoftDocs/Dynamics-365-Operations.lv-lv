---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435588"
---
# <a name="create-new-users"></a><span data-ttu-id="d4c56-103">Jaunu lietotāju izveide</span><span class="sxs-lookup"><span data-stu-id="d4c56-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4c56-104">Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.</span><span class="sxs-lookup"><span data-stu-id="d4c56-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="d4c56-105">Saistīt lietotāju ar licenci (tikai jauni licences veidi)</span><span class="sxs-lookup"><span data-stu-id="d4c56-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="d4c56-106">Attiecībā uz debitoriem, kuriem ir viens no jaunajiem licences tipiem, kas tika pievienoti 2019. oktobrī, lietotājiem jābūt saistītiem ar licenci.</span><span class="sxs-lookup"><span data-stu-id="d4c56-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="d4c56-107">Lietotāji, kas ir saistīti ar licenci, tiek automātiski pievienoti kā sistēmas lietotāji, kuriem nav lomas, pirmo reizi pierakstoties sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d4c56-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="d4c56-108">Sistēmas administratori var [piešķirt licences lietotājiem](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="d4c56-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="d4c56-109">Saistīt ārējo lietotāju ar licenci (tikai jauni licences veidi)</span><span class="sxs-lookup"><span data-stu-id="d4c56-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="d4c56-110">Lietotāji, kas ir ārēji nomniekam, kurā tika izvietota vide, jānorāda resursdatora nomnieka direktorijā (Azure Active Directory (Azure AD)), lai tiem varētu piešķirt licences.</span><span class="sxs-lookup"><span data-stu-id="d4c56-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="d4c56-111">Šie ārējie lietotāji jāpievieno nomniekam Azure AD kā vieslietotāji un pēc tam jāpiešķir atbilstošās licences.</span><span class="sxs-lookup"><span data-stu-id="d4c56-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="d4c56-112">Papildinformāciju skatiet [Azure Active Directory B2B sadarbības lietotāju pievienošana Azure portālā](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="d4c56-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="d4c56-113">Pievienot jaunu lietotāju</span><span class="sxs-lookup"><span data-stu-id="d4c56-113">Add a new user</span></span>
1. <span data-ttu-id="d4c56-114">Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="d4c56-115">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d4c56-116">Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="d4c56-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="d4c56-117">Jānorāda lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="d4c56-117">A user ID is required.</span></span>  
4. <span data-ttu-id="d4c56-118">Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="d4c56-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="d4c56-119">Laukā **Domēns** ievadiet lietotāja domēnu.</span><span class="sxs-lookup"><span data-stu-id="d4c56-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="d4c56-120">Laukā **Aizstājvārds** ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="d4c56-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="d4c56-121">Laukā **Uzņēmums** atlasiet vēlamo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="d4c56-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="d4c56-122">Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**, lai pieškirtu lietotājus drošības lomām.</span><span class="sxs-lookup"><span data-stu-id="d4c56-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="d4c56-123">Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d4c56-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="d4c56-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-124">Select **OK**.</span></span>
10. <span data-ttu-id="d4c56-125">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="d4c56-126">Importēt lietotājus</span><span class="sxs-lookup"><span data-stu-id="d4c56-126">Import users</span></span>
1. <span data-ttu-id="d4c56-127">Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="d4c56-128">Darbību rūtī atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="d4c56-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4c56-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d4c56-130">Atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-130">Select **Import users**.</span></span>
5. <span data-ttu-id="d4c56-131">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="d4c56-131">Select **Close**.</span></span>

