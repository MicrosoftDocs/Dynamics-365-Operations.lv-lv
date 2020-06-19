---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431065"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="c5164-103">Nevar izveidot vidi Power Apps administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="c5164-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="c5164-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="c5164-104">**Issue**</span></span>

- <span data-ttu-id="c5164-105">Nomnieka/vides administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="c5164-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="c5164-106">Licence, kas dod lietotājiem tiesības veikt vides izveides darbību, nav piešķirts tieši lietotājam, kurš veic attiecīgo darbību.</span><span class="sxs-lookup"><span data-stu-id="c5164-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="c5164-107">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="c5164-107">**Solution**</span></span>

<span data-ttu-id="c5164-108">Pārliecinieties, ka nomnieka administrators ir piešķīris derīgu Power Apps P2 licenci tieši lietotājam, kurš veiks vides izveides soli.</span><span class="sxs-lookup"><span data-stu-id="c5164-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="c5164-109">Tālāk ir norādīti Microsoft Dynamics pakalpojumu plāni, kas nodrošina šīs tiesības.</span><span class="sxs-lookup"><span data-stu-id="c5164-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="c5164-110">Vispārēja preču noliktavas vienība (SKU)</span><span class="sxs-lookup"><span data-stu-id="c5164-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="c5164-111">Power Apps P2 pakalpojumu plāns</span><span class="sxs-lookup"><span data-stu-id="c5164-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="c5164-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="c5164-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="c5164-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c5164-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="c5164-114">Microsoft Dynamics 365 plāns Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c5164-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="c5164-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c5164-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="c5164-116">Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas Power Apps 2. plāna SKU.</span><span class="sxs-lookup"><span data-stu-id="c5164-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="c5164-117">Ir svarīgi, lai būtu viena šīm SKU.</span><span class="sxs-lookup"><span data-stu-id="c5164-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="c5164-118">Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="c5164-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c5164-119">Izveidojiet vides, izpildot instrukcijas [Human Resources nodrošināšana](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="c5164-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
