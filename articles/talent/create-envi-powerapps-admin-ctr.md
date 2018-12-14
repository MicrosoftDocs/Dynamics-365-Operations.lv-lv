---
title: "Nevar izveidot vidi PowerApps administrēšanas centrā"
description: "Šajā tēmā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft PowerApps administr. centrā."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="9e02d-103">Nevar izveidot vidi PowerApps administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="9e02d-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e02d-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="9e02d-104">**Issue**</span></span>

- <span data-ttu-id="9e02d-105">Nomnieka/vides administrators nevar izveidot vidi Microsoft PowerApps administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="9e02d-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="9e02d-106">Licence, kas dod lietotājiem tiesības veikt vides izveides darbību, nav piešķirts tieši lietotājam, kurš veic attiecīgo darbību.</span><span class="sxs-lookup"><span data-stu-id="9e02d-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="9e02d-107">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="9e02d-107">**Solution**</span></span>

<span data-ttu-id="9e02d-108">Pārliecinieties, ka nomnieka administrators ir piešķīris derīgu PowerApps P2 licenci tieši lietotājam, kurš veiks vides izveides soli.</span><span class="sxs-lookup"><span data-stu-id="9e02d-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="9e02d-109">Minētās tiesības nodrošina šādi Microsoft Dynamics pakalpojumu plāni.</span><span class="sxs-lookup"><span data-stu-id="9e02d-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="9e02d-110">Vispārēja preču noliktavas vienība (SKU)</span><span class="sxs-lookup"><span data-stu-id="9e02d-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="9e02d-111">PowerApps P2 pak. plāns</span><span class="sxs-lookup"><span data-stu-id="9e02d-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="9e02d-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="9e02d-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="9e02d-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9e02d-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="9e02d-114">Microsoft Dynamics 365 pl. Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="9e02d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="9e02d-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9e02d-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="9e02d-116">Ņemiet vērā, ka dažādas Microsoft Office SKU arī nodrošina tiesības kopā ar savrupā PowerApps 2. plānu SKU.</span><span class="sxs-lookup"><span data-stu-id="9e02d-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="9e02d-117">Ir svarīgi, lai būtu viena šīm SKU.</span><span class="sxs-lookup"><span data-stu-id="9e02d-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="9e02d-118">Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="9e02d-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="9e02d-119">Izveidojiet vides, izpildot instrukcijas sadaļā [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="9e02d-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

