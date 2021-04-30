---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892231"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="b3da7-103">Nevar izveidot vidi Power Apps administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="b3da7-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b3da7-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="b3da7-104">**Issue**</span></span>

- <span data-ttu-id="b3da7-105">Nomnieka/vides administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="b3da7-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="b3da7-106">Lietotājam nav licences, kas dod tiesības izveidot vides.</span><span class="sxs-lookup"><span data-stu-id="b3da7-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="b3da7-107">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="b3da7-107">**Solution**</span></span>

<span data-ttu-id="b3da7-108">Pārliecinieties, vai nomnieka administrators ir piešķīris derīgu Power Apps P2 licenci lietotājam, kas veido vidi.</span><span class="sxs-lookup"><span data-stu-id="b3da7-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="b3da7-109">Šādi Microsoft Dynamics pakalpojumu plāni sniedz atļaujas vides izveidošanai:</span><span class="sxs-lookup"><span data-stu-id="b3da7-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="b3da7-110">Vispārēja preču noliktavas vienība (SKU)</span><span class="sxs-lookup"><span data-stu-id="b3da7-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="b3da7-111">Power Apps P2 pakalpojumu plāns</span><span class="sxs-lookup"><span data-stu-id="b3da7-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="b3da7-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="b3da7-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="b3da7-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b3da7-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="b3da7-114">Microsoft Dynamics 365 plāns Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="b3da7-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="b3da7-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b3da7-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="b3da7-116">Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas Power Apps 2. plāna SKU.</span><span class="sxs-lookup"><span data-stu-id="b3da7-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="b3da7-117">Ir svarīgi, lai būtu viena šīm SKU.</span><span class="sxs-lookup"><span data-stu-id="b3da7-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="b3da7-118">Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="b3da7-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="b3da7-119">Izveidojiet vides, izpildot instrukcijas [Human Resources nodrošināšana](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="b3da7-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]