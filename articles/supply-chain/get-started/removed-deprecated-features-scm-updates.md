---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt sistēmā Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597120"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="41604-103">Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="41604-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41604-104">Šī tēma tiks atjaunināta, kolīdz būs dokumentēti jauni noņemti vai novecojuši līdzekļi Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="41604-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="41604-105">*Noņemts* līdzeklis produktā vairs nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="41604-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="41604-106">*Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="41604-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="41604-107">Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.</span><span class="sxs-lookup"><span data-stu-id="41604-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="41604-108">Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="41604-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="41604-109">Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.</span><span class="sxs-lookup"><span data-stu-id="41604-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="41604-110">Noņemtie vai novecojuši līdzekļi programmas Supply Chain Management 10.0.11 laidienā</span><span class="sxs-lookup"><span data-stu-id="41604-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="41604-111">Iebūvētā Supply Chain Management vispārējās plānošanas programmas izmantošana izplatīšanas scenārijiem</span><span class="sxs-lookup"><span data-stu-id="41604-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="41604-112">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="41604-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="41604-113">Lai uzlabotu veiktspēju un minimizētu SQL datu bāzes noslodzi vispārējās plānošanas izpildes laikā, iebūvētā Supply Chain Management vispārējā plānošanas programma tiek aizstāta ar Plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="41604-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="41604-114">Plānošanas optimizācija atļauj ātro plānošanu, ko var veikt pat darba stundu laikā.</span><span class="sxs-lookup"><span data-stu-id="41604-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="41604-115">Tas ļauj plānotājiem nekavējoties reaģēt uz pieprasījuma vai plānošanas parametru izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="41604-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="41604-116">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="41604-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="41604-117">Jā, Plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management vispārējo plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="41604-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="41604-118">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="41604-118">**Product areas affected**</span></span>         | <span data-ttu-id="41604-119">Supply Chain Management - vispārējā plānošana</span><span class="sxs-lookup"><span data-stu-id="41604-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="41604-120">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="41604-120">**Deployment option**</span></span>              | <span data-ttu-id="41604-121">Tikai mākonis.</span><span class="sxs-lookup"><span data-stu-id="41604-121">Cloud only.</span></span> <span data-ttu-id="41604-122">Plānošanas optimizācija netiek atbalstīta ar lokālajām izvietošanām.</span><span class="sxs-lookup"><span data-stu-id="41604-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="41604-123">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="41604-123">**Status**</span></span>                         | <span data-ttu-id="41604-124">Novecojis.</span><span class="sxs-lookup"><span data-stu-id="41604-124">Deprecated.</span></span> <span data-ttu-id="41604-125">2021. gada aprīlī izplatīšanas scenāriji vairs netiks atbalstīti ar iebūvēto Dynamics 365 Supply Chain Management vispārējās plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="41604-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="41604-126">Izplatīšanas scenārijiem klientiem jāizmanto Plānošanas optimizācija vispārējās plānošanas aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="41604-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="41604-127">Papildinformāciju skatiet [Plānošanas optimizācijas dokumentācija](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="41604-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="41604-128">Klienti, kuriem ir Dynamics 365 Supply Chain Management lokālās izvietošanas, var turpināt izmantot Supply Chain Management vispārējās plānošanas programmu izplatīšanas scenārijiem pēc 2021. gada aprīļa.</span><span class="sxs-lookup"><span data-stu-id="41604-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="41604-129">Tomēr papildu līdzekļu uzlabojumi netiks nodrošināti.</span><span class="sxs-lookup"><span data-stu-id="41604-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="41604-130">Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="41604-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="41604-131">Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="41604-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
