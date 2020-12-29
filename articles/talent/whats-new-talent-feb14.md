---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 14. februāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461886"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a><span data-ttu-id="6e7fb-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 14. februāris)</span><span class="sxs-lookup"><span data-stu-id="6e7fb-103">What's new or changed in Dynamics 365 Talent (February 14, 2019)</span></span>

<span data-ttu-id="6e7fb-104">Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="6e7fb-105">Izmaiņas programmā Attract</span><span class="sxs-lookup"><span data-stu-id="6e7fb-105">Changes in Attract</span></span>
<span data-ttu-id="6e7fb-106">Šajā laidienā ir ietverti nelieli kļūdu labojumi.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="6e7fb-107">Izmaiņas pievienošanas procesā</span><span class="sxs-lookup"><span data-stu-id="6e7fb-107">Changes in Onboarding</span></span>
<span data-ttu-id="6e7fb-108">Šajā laidienā ir ietverti nelieli kļūdu labojumi.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="6e7fb-109">Izmaiņas programmā Core HR</span><span class="sxs-lookup"><span data-stu-id="6e7fb-109">Changes in Core HR</span></span> 
<span data-ttu-id="6e7fb-110">**8.1.2146 būvējums**</span><span class="sxs-lookup"><span data-stu-id="6e7fb-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="6e7fb-111">Elements Darbinieka fiksētā atlīdzība nenodrošina visu ierakstu eksportēšanu</span><span class="sxs-lookup"><span data-stu-id="6e7fb-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="6e7fb-112">Šīs izmaiņas nodrošina, ka tagad elements **Darbinieka fiksētā atlīdzība** nodrošina visu ierakstu eksportēšanu.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="6e7fb-113">Šo elementu var izmantot, lai izveidotu jaunus un atjauninātu esošos darbinieku fiksētās atlīdzības ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="6e7fb-114">Darbinieka vēlamās laika zonas iestatījuma neņemšana vērā, nosakot nodarbinātības beigu datumu</span><span class="sxs-lookup"><span data-stu-id="6e7fb-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="6e7fb-115">Tagad, brīdī, kad darbinieks sāk vai beidz strādāt uzņēmumā, nosakot nodarbinātības beigu datumu, tiek ņemts vērā lietotāja vēlamās laika joslas iestatījums.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="6e7fb-116">Lielbritānijā esošu adrešu rādīšana kā Austrumšveicē esošu programmā Analytics</span><span class="sxs-lookup"><span data-stu-id="6e7fb-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="6e7fb-117">Šajā laidienā ir veiktas izmaiņas, lai novērstu adrešu neatbilstību darbvietas **Personāla vadība** pārskatā Darbinieku skaits pēc atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="6e7fb-118">Darba attiecību pārtraukšanas koda nenorādīšana nodarbinātā amata piešķires ierakstā, kad tiek beigta amata piešķire</span><span class="sxs-lookup"><span data-stu-id="6e7fb-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="6e7fb-119">Ir veiktas izmaiņas, lai brīdī, kad tiek beigta amata piešķire darbiniekam, tiktu norādīta koda Darba attiecību pārtraukšanas pamatojums noklusējuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="6e7fb-120">Jauna darba atlīdzības līmeņu elementa izveide</span><span class="sxs-lookup"><span data-stu-id="6e7fb-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="6e7fb-121">Ir izveidots jauns datu pārvaldības struktūras (data management framework — DMF) elements.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="6e7fb-122">Šis elements sniedz iespēju izveidot un atjaunināt katra sistēmā definētā darba atlīdzības līmeņus, tirgus vērtības un aptauju informāciju.</span><span class="sxs-lookup"><span data-stu-id="6e7fb-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
