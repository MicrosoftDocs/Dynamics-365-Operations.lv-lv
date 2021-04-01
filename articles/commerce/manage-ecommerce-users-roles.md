---
title: Lietotāju un lomu pārvaldība e-tirdzniecībā
description: Šajā tēmā izskaidrots, kā piešķirt lietotājiem piekļuvi Microsoft Dynamics 365 Commerce vietnes autorēšanas videi.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255923"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="bda0f-103">Lietotāju un lomu pārvaldība e-tirdzniecībā</span><span class="sxs-lookup"><span data-stu-id="bda0f-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bda0f-104">Šajā tēmā izskaidrots, kā piešķirt lietotājiem piekļuvi Microsoft Dynamics 365 Commerce vietnes autorēšanas videi.</span><span class="sxs-lookup"><span data-stu-id="bda0f-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="bda0f-105">Lai palīdzētu kontrolēt lietotāju piekļuvi un piešķirtu lietotājiem atļaujas veikt noteiktus uzdevumus, vietnes autorēšanas vide izmanto drošības grupas, ko izveidojat Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="bda0f-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="bda0f-106">Vispirms no Azure AD piešķiriet jaunu vai esošu drošības grupu katrai lomai autorēšanas vidē.</span><span class="sxs-lookup"><span data-stu-id="bda0f-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="bda0f-107">Pēc tam piešķiriet vai atsauciet atļaujas atsevišķiem lietotājiem, vai nu pievienojot šos lietotājus atbilstošai drošības grupai, vai noņemot tos no drošības grupas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="bda0f-108">Lomu pārskats autorēšanas vidē</span><span class="sxs-lookup"><span data-stu-id="bda0f-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="bda0f-109">Dynamics 365 for Commerce autorēšanas vide atbalsta tālāk minētās lomas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="bda0f-110">Loma</span><span class="sxs-lookup"><span data-stu-id="bda0f-110">Role</span></span>                 | <span data-ttu-id="bda0f-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="bda0f-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="bda0f-112">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="bda0f-112">System Administrator</span></span> | <span data-ttu-id="bda0f-113">Lietotājiem, kuriem ir šī loma, ir visas privilēģijas visiem rīkiem, vērtējumiem un apskatiem.</span><span class="sxs-lookup"><span data-stu-id="bda0f-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="bda0f-114">Viņi var arī izveidot vietnes.</span><span class="sxs-lookup"><span data-stu-id="bda0f-114">They can also create sites.</span></span> |
| <span data-ttu-id="bda0f-115">Administrators</span><span class="sxs-lookup"><span data-stu-id="bda0f-115">Administrator</span></span>   | <span data-ttu-id="bda0f-116">Lietotājiem, kuriem ir šī loma, ir visas privilēģijas visiem rīkiem un RnR noteiktā vietnes struktūrā.</span><span class="sxs-lookup"><span data-stu-id="bda0f-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="bda0f-117">Tīmekļa producents</span><span class="sxs-lookup"><span data-stu-id="bda0f-117">Web Producer</span></span>         | <span data-ttu-id="bda0f-118">Lietotāji, kuriem ir šī loma, var izveidot lapas, fragmentus un veidnes, augšupielādēt un pārvaldīt līdzekļus un papildināt preces un kategorijas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="bda0f-119">Lasītājs</span><span class="sxs-lookup"><span data-stu-id="bda0f-119">Reader</span></span>               | <span data-ttu-id="bda0f-120">Lietotāji, kuriem ir šī loma, var skatīt lapas, veidnes, līdzekļus, fragmentus, izkārtojumus un iestatījumus, bet nevar veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="bda0f-121">RnR moderators</span><span class="sxs-lookup"><span data-stu-id="bda0f-121">RnR Moderator</span></span>        | <span data-ttu-id="bda0f-122">Lietotāji, kuriem ir šī loma, var moderēt preču apskatus.</span><span class="sxs-lookup"><span data-stu-id="bda0f-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="bda0f-123">Sistēmas administratora loma</span><span class="sxs-lookup"><span data-stu-id="bda0f-123">System Administrator role</span></span>

<span data-ttu-id="bda0f-124">Kad jūs nodrošināt Dynamics 365 Commerce Microsoft Dynamics Lifecycle Services (LCS) vidē, jums tiek lūgts norādīt drošības grupu lomai **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="bda0f-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="bda0f-125">Šī loma tiek automātiski piemērota visām vietnēm, ko izveidojat jūsu konfigurētajā vidē.</span><span class="sxs-lookup"><span data-stu-id="bda0f-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="bda0f-126">Šīs lomas drošības grupu var atjaunināt tikai LCS.</span><span class="sxs-lookup"><span data-stu-id="bda0f-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="bda0f-127">Visu vietņu lapā **Vietnes administrēšana** tas parādās kā tikai lasāms un paredzēts tikai informatīviem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="bda0f-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="bda0f-128">Administratora loma</span><span class="sxs-lookup"><span data-stu-id="bda0f-128">Administrator role</span></span>

<span data-ttu-id="bda0f-129">Kad jūs Commerce izveidojat jaunu vietni, jums tiek lūgts nodrošināt drošības grupu lomai **Administrators**.</span><span class="sxs-lookup"><span data-stu-id="bda0f-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="bda0f-130">Skatīt šajā tēmā iepriekš minēto tabulu, lai apskatītu šai lomai piešķirtās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="bda0f-131">Drošības grupu pievienošana vai atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="bda0f-131">Add or update security groups</span></span>

<span data-ttu-id="bda0f-132">Pēc vietnes izveides tikai tie lietotāji, kuri ir drošības grupās, kas saistītas ar lomām **Sistēmas administrators** un **Administrators**, var piekļūt šīs vietnes autorēšanas videi.</span><span class="sxs-lookup"><span data-stu-id="bda0f-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="bda0f-133">Lai piešķirtu lietotājiem lomas **Tīmekļa producents**, **RnR moderators** un **Lasītājs**, šīm lomām ir jāpiešķir drošības grupas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="bda0f-134">Lai lomai pievienotu drošības grupu vai atjauninātu drošības grupu, kas pašlaik ir piešķirta lomai, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="bda0f-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="bda0f-135">Dodieties uz vietni, ko vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="bda0f-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="bda0f-136">**Vietnes vadība** atveriet lapu **Drošība**.</span><span class="sxs-lookup"><span data-stu-id="bda0f-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="bda0f-137">Atlasiet lomu, ko paredzēts modificēt.</span><span class="sxs-lookup"><span data-stu-id="bda0f-137">Select the role to modify.</span></span>
1. <span data-ttu-id="bda0f-138">Pievienojiet vai noņemiet lomām drošības grupas.</span><span class="sxs-lookup"><span data-stu-id="bda0f-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bda0f-139">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bda0f-139">Additional resources</span></span>

[<span data-ttu-id="bda0f-140">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="bda0f-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="bda0f-141">Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei</span><span class="sxs-lookup"><span data-stu-id="bda0f-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="bda0f-142">Satura drošības politikas (CSP) pārvaldība</span><span class="sxs-lookup"><span data-stu-id="bda0f-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]