---
title: Nevar izveidot vidi PowerApps administrēšanas centrā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft PowerApps administrēšanas centrā.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305371"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="0a277-103">Nevar izveidot vidi PowerApps administrēšanas centrā</span><span class="sxs-lookup"><span data-stu-id="0a277-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a277-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="0a277-104">**Issue**</span></span>

- <span data-ttu-id="0a277-105">Nomnieka/vides administrators nevar izveidot vidi Microsoft PowerApps administrēšanas centrā.</span><span class="sxs-lookup"><span data-stu-id="0a277-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="0a277-106">Licence, kas dod lietotājiem tiesības veikt vides izveides darbību, nav piešķirts tieši lietotājam, kurš veic attiecīgo darbību.</span><span class="sxs-lookup"><span data-stu-id="0a277-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="0a277-107">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="0a277-107">**Solution**</span></span>

<span data-ttu-id="0a277-108">Pārliecinieties, ka nomnieka administrators ir piešķīris derīgu PowerApps P2 licenci tieši lietotājam, kurš veiks vides izveides soli.</span><span class="sxs-lookup"><span data-stu-id="0a277-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="0a277-109">Tālāk ir norādīti Microsoft Dynamics pakalpojumu plāni, kas nodrošina šīs tiesības.</span><span class="sxs-lookup"><span data-stu-id="0a277-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="0a277-110">Vispārēja preču noliktavas vienība (SKU)</span><span class="sxs-lookup"><span data-stu-id="0a277-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="0a277-111">PowerApps P2 pak. plāns</span><span class="sxs-lookup"><span data-stu-id="0a277-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="0a277-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="0a277-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="0a277-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0a277-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="0a277-114">Microsoft Dynamics 365 plāns Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="0a277-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="0a277-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0a277-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="0a277-116">Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas PowerApps 2. plāna SKU.</span><span class="sxs-lookup"><span data-stu-id="0a277-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="0a277-117">Ir svarīgi, lai būtu viena šīm SKU.</span><span class="sxs-lookup"><span data-stu-id="0a277-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="0a277-118">Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="0a277-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="0a277-119">Izveidojiet vides, izpildot instrukcijas sadaļā [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="0a277-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
