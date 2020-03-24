---
title: Izveidot seguma opcijas
description: Seguma opcijas Microsoft Dynamics 365 Human Resources ir seguma līmeņi dalībnieka izvēlei atvieglojumu plānā vai programmā, piemēram, tikai darbinieki ārstniecības plānam vai 2x alga dzīvības apdrošināšanas plānam.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092710"
---
# <a name="create-coverage-options"></a><span data-ttu-id="1982d-103">Izveidot seguma opcijas</span><span class="sxs-lookup"><span data-stu-id="1982d-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1982d-104">Seguma opcijas Microsoft Dynamics 365 Human Resources ir seguma līmeņi dalībnieka izvēlei atvieglojumu plānā vai programmā, piemēram, tikai darbinieki ārstniecības plānam vai 2x alga dzīvības apdrošināšanas plānam.</span><span class="sxs-lookup"><span data-stu-id="1982d-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="1982d-105">Kad tās definētas, atvieglojumu seguma opcijas ir izmantojamas atkārtoti, un varat saistīt opciju ar vienu vai vairākiem plāniem.</span><span class="sxs-lookup"><span data-stu-id="1982d-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="1982d-106">Kad seguma opcijas ir definētas, pievienojiet seguma opcijas atvieglojumu plāna veidam.</span><span class="sxs-lookup"><span data-stu-id="1982d-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="1982d-107">Pēc tam plāna veids tiek saistīts ar atvieglojumu plānu vai programmu.</span><span class="sxs-lookup"><span data-stu-id="1982d-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="1982d-108">Seguma opcijas, kas saistītas ar plāna veidu, būs pieejamas visiem plāniem, kas izveidoti ar šo plāna veidu.</span><span class="sxs-lookup"><span data-stu-id="1982d-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="1982d-109">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Seguma opcijas**.</span><span class="sxs-lookup"><span data-stu-id="1982d-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="1982d-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1982d-110">Select **New**.</span></span>

3. <span data-ttu-id="1982d-111">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="1982d-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1982d-112">Lauks</span><span class="sxs-lookup"><span data-stu-id="1982d-112">Field</span></span> | <span data-ttu-id="1982d-113">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1982d-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1982d-114">**Seguma opcija**</span><span class="sxs-lookup"><span data-stu-id="1982d-114">**Coverage option**</span></span> | <span data-ttu-id="1982d-115">Unikāls seguma opcijas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="1982d-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="1982d-116">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="1982d-116">**Description**</span></span> | <span data-ttu-id="1982d-117">Seguma opcijas apraksts.</span><span class="sxs-lookup"><span data-stu-id="1982d-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="1982d-118">**Vajadz. aprēķ. metode**</span><span class="sxs-lookup"><span data-stu-id="1982d-118">**Coverage code**</span></span> | <span data-ttu-id="1982d-119">Seguma kodi piešķir minimālo un maksimālo summu katram segumam piemērotās personas veidam.</span><span class="sxs-lookup"><span data-stu-id="1982d-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="1982d-120">Seguma kods norāda, kuram ir segums, vai plāna veidam atļautā seguma summu.</span><span class="sxs-lookup"><span data-stu-id="1982d-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="1982d-121">Seguma summu varat izteikt kā summu dolāros vai procentuālu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1982d-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="1982d-122">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="1982d-122">For example:</span></span></br></br><span data-ttu-id="1982d-123">- **Darbinieks+1** — lai kvalificētos, darbiniekam ir jābūt atlasītam vienam apgādājamam (ja atlasīts vairāk nekā viens, tie vairs nekvalificējas).</span><span class="sxs-lookup"><span data-stu-id="1982d-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="1982d-124">- **Darbinieks+ģimene** — lai kvalificētos, darbiniekam jāatlasa vismaz divi apgādājamie.</span><span class="sxs-lookup"><span data-stu-id="1982d-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="1982d-125">**Maksimālais skaits**</span><span class="sxs-lookup"><span data-stu-id="1982d-125">**Maximum number**</span></span> | <span data-ttu-id="1982d-126">Maksimālais apgādājamo skaits.</span><span class="sxs-lookup"><span data-stu-id="1982d-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="1982d-127">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="1982d-127">**Status**</span></span> | <span data-ttu-id="1982d-128">Seguma opcijas statuss.</span><span class="sxs-lookup"><span data-stu-id="1982d-128">The status of the coverage option.</span></span> <span data-ttu-id="1982d-129">Ja seguma opcijas statuss ir iestatīts uz Neaktīvs, plānu veidos nevar atlasīt seguma opciju.</span><span class="sxs-lookup"><span data-stu-id="1982d-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="1982d-130">**Procenti**</span><span class="sxs-lookup"><span data-stu-id="1982d-130">**Percent**</span></span> | <span data-ttu-id="1982d-131">Procentuālā summa.</span><span class="sxs-lookup"><span data-stu-id="1982d-131">The percent amount.</span></span> <span data-ttu-id="1982d-132">Šis lauks ir aktīvs tikai tad, ja laukā Seguma kods ir atlasīts % x alga.</span><span class="sxs-lookup"><span data-stu-id="1982d-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="1982d-133">**Dalītājs**</span><span class="sxs-lookup"><span data-stu-id="1982d-133">**Divisor**</span></span> | <span data-ttu-id="1982d-134">Dalītājs, ko izmanto aprēķinā, kad atlasīts seguma kods % x alga.</span><span class="sxs-lookup"><span data-stu-id="1982d-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="1982d-135">**Minimālā procentuālā vērtība**</span><span class="sxs-lookup"><span data-stu-id="1982d-135">**Percent minimum**</span></span> | <span data-ttu-id="1982d-136">Minimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu.</span><span class="sxs-lookup"><span data-stu-id="1982d-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="1982d-137">**Maksimālā procentuālā vērtība**</span><span class="sxs-lookup"><span data-stu-id="1982d-137">**Percent maximum**</span></span> | <span data-ttu-id="1982d-138">Maksimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu.</span><span class="sxs-lookup"><span data-stu-id="1982d-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="1982d-139">Sadaļā **Personisko kontaktpersonu piemērotības opcijas** katrai seguma opcijai pievienojiet atbilstošās personiskās kontaktpersonas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="1982d-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="1982d-140">Sadaļā **Patstāvīgi izmantojamais pakalpojums** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="1982d-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="1982d-141">Lauks</span><span class="sxs-lookup"><span data-stu-id="1982d-141">Field</span></span> | <span data-ttu-id="1982d-142">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1982d-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1982d-143">**Atļaut darbinieku ieguldījumu summu**</span><span class="sxs-lookup"><span data-stu-id="1982d-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="1982d-144">Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt iemaksu summu par atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="1982d-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1982d-145">Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz iemaksu summu, ko darbinieks ievada atvieglojumu patstāvīgi izmantojamajā pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1982d-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="1982d-146">**Atļaut darbinieku vajadzību summu**</span><span class="sxs-lookup"><span data-stu-id="1982d-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="1982d-147">Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt seguma summu par atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="1982d-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="1982d-148">Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz seguma summu, ko darbinieks ievada darbinieku patstāvīgi izmantojamajā pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1982d-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="1982d-149">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1982d-149">Select **Save**.</span></span> 
