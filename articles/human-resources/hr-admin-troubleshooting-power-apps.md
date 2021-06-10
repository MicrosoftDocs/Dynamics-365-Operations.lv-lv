---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053351"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="aba6c-103">Nevar izveidot vidi Power Apps administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="aba6c-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aba6c-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="aba6c-104">**Issue**</span></span>

- <span data-ttu-id="aba6c-105">Nomnieka/vides administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="aba6c-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="aba6c-106">Lietotājam nav licences, kas dod tiesības izveidot vides.</span><span class="sxs-lookup"><span data-stu-id="aba6c-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="aba6c-107">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="aba6c-107">**Solution**</span></span>

<span data-ttu-id="aba6c-108">Pārliecinieties, vai nomnieka administrators ir piešķīris derīgu Power Apps P2 licenci lietotājam, kas veido vidi.</span><span class="sxs-lookup"><span data-stu-id="aba6c-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="aba6c-109">Šādi Microsoft Dynamics pakalpojumu plāni sniedz atļaujas vides izveidošanai:</span><span class="sxs-lookup"><span data-stu-id="aba6c-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="aba6c-110">Vispārēja preču noliktavas vienība (SKU)</span><span class="sxs-lookup"><span data-stu-id="aba6c-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="aba6c-111">Power Apps P2 pakalpojumu plāns</span><span class="sxs-lookup"><span data-stu-id="aba6c-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="aba6c-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="aba6c-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="aba6c-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="aba6c-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="aba6c-114">Microsoft Dynamics 365 plāns Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="aba6c-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="aba6c-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="aba6c-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="aba6c-116">Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas Power Apps 2. plāna SKU.</span><span class="sxs-lookup"><span data-stu-id="aba6c-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="aba6c-117">Ir svarīgi, lai būtu viena šīm SKU.</span><span class="sxs-lookup"><span data-stu-id="aba6c-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="aba6c-118">Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="aba6c-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="aba6c-119">Izveidojiet vides, izpildot instrukcijas [Human Resources nodrošināšana](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="aba6c-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]