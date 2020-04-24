---
title: Izveidot seguma opcijas
description: Vajadzību opcijas programmā Microsoft Dynamics 365 Human Resources ir nodrošinājuma līmeņi dalībnieka vēlēšanām atvieglojumu plānā vai programmā.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 021fea7604af2fff833ddc6868d55a316ef70aae
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230181"
---
# <a name="create-coverage-options"></a><span data-ttu-id="25d09-103">Izveidot seguma opcijas</span><span class="sxs-lookup"><span data-stu-id="25d09-103">Create coverage options</span></span>

<span data-ttu-id="25d09-104">Vajadzību opcijas programmā Microsoft Dynamics 365 Human Resources ir nodrošinājuma līmeņi dalībnieka vēlēšanām atvieglojumu plānā vai programmā.</span><span class="sxs-lookup"><span data-stu-id="25d09-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="25d09-105">Piemēram, vajadzības opcijas var iekļaut **Tikai darbinieks** medicīniskajam plānam vai **Atalgojums x2** dzīvības apdrošināšanas plānam.</span><span class="sxs-lookup"><span data-stu-id="25d09-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="25d09-106">Pēc definēšanas varat atkārtoti izmantot atvieglojumu vajadzību opcijas.</span><span class="sxs-lookup"><span data-stu-id="25d09-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="25d09-107">Varat saistīt opciju ar vienu vai vairākiem plāniem.</span><span class="sxs-lookup"><span data-stu-id="25d09-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="25d09-108">Kad seguma opcijas ir definētas, pievienojiet seguma opcijas atvieglojumu plāna veidam.</span><span class="sxs-lookup"><span data-stu-id="25d09-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="25d09-109">Pēc tam plāna veids tiek saistīts ar atvieglojumu plānu vai programmu.</span><span class="sxs-lookup"><span data-stu-id="25d09-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="25d09-110">Seguma opcijas, kas saistītas ar plāna veidu, ir pieejamas visiem plāniem, kas izveidoti ar šo plāna veidu.</span><span class="sxs-lookup"><span data-stu-id="25d09-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="25d09-111">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Seguma opcijas**.</span><span class="sxs-lookup"><span data-stu-id="25d09-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="25d09-112">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="25d09-112">Select **New**.</span></span>

3. <span data-ttu-id="25d09-113">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="25d09-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="25d09-114">Lauks</span><span class="sxs-lookup"><span data-stu-id="25d09-114">Field</span></span> | <span data-ttu-id="25d09-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="25d09-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="25d09-116">**Seguma opcija**</span><span class="sxs-lookup"><span data-stu-id="25d09-116">**Coverage option**</span></span> | <span data-ttu-id="25d09-117">Unikāls seguma opcijas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="25d09-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="25d09-118">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="25d09-118">**Description**</span></span> | <span data-ttu-id="25d09-119">Seguma opcijas apraksts.</span><span class="sxs-lookup"><span data-stu-id="25d09-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="25d09-120">**Vajadz. aprēķ. metode**</span><span class="sxs-lookup"><span data-stu-id="25d09-120">**Coverage code**</span></span> | <span data-ttu-id="25d09-121">Seguma kodi piešķir minimālo un maksimālo summu katram segumam piemērotās personas veidam.</span><span class="sxs-lookup"><span data-stu-id="25d09-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="25d09-122">Seguma kods norāda, kuram ir segums, vai plāna veidam atļautā seguma summu.</span><span class="sxs-lookup"><span data-stu-id="25d09-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="25d09-123">Seguma summu varat izteikt kā summu dolāros vai procentuālu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25d09-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="25d09-124">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="25d09-124">For example:</span></span></br></br><span data-ttu-id="25d09-125">- **Darbinieks+1** — lai kvalificētos, darbiniekam ir jābūt atlasītam vienam apgādājamam (ja atlasīts vairāk nekā viens, tie vairs nekvalificējas).</span><span class="sxs-lookup"><span data-stu-id="25d09-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="25d09-126">- **Darbinieks+ģimene** — lai kvalificētos, darbiniekam jāatlasa vismaz divi apgādājamie.</span><span class="sxs-lookup"><span data-stu-id="25d09-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="25d09-127">**Maksimālais skaits**</span><span class="sxs-lookup"><span data-stu-id="25d09-127">**Maximum number**</span></span> | <span data-ttu-id="25d09-128">Maksimālais apgādājamo skaits.</span><span class="sxs-lookup"><span data-stu-id="25d09-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="25d09-129">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="25d09-129">**Status**</span></span> | <span data-ttu-id="25d09-130">Seguma opcijas statuss.</span><span class="sxs-lookup"><span data-stu-id="25d09-130">The status of the coverage option.</span></span> <span data-ttu-id="25d09-131">Ja seguma opcijas statuss ir iestatīts uz Neaktīvs, plānu veidos nevar atlasīt seguma opciju.</span><span class="sxs-lookup"><span data-stu-id="25d09-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="25d09-132">**Procenti**</span><span class="sxs-lookup"><span data-stu-id="25d09-132">**Percent**</span></span> | <span data-ttu-id="25d09-133">Procentuālā summa.</span><span class="sxs-lookup"><span data-stu-id="25d09-133">The percent amount.</span></span> <span data-ttu-id="25d09-134">Šis lauks ir aktīvs tikai tad, ja laukā Seguma kods ir atlasīts % x alga.</span><span class="sxs-lookup"><span data-stu-id="25d09-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="25d09-135">**Dalītājs**</span><span class="sxs-lookup"><span data-stu-id="25d09-135">**Divisor**</span></span> | <span data-ttu-id="25d09-136">Dalītājs, ko izmanto aprēķinā, kad atlasīts seguma kods % x alga.</span><span class="sxs-lookup"><span data-stu-id="25d09-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="25d09-137">**Minimālā procentuālā vērtība**</span><span class="sxs-lookup"><span data-stu-id="25d09-137">**Percent minimum**</span></span> | <span data-ttu-id="25d09-138">Minimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu.</span><span class="sxs-lookup"><span data-stu-id="25d09-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="25d09-139">**Maksimālā procentuālā vērtība**</span><span class="sxs-lookup"><span data-stu-id="25d09-139">**Percent maximum**</span></span> | <span data-ttu-id="25d09-140">Maksimālā procentuālā vērtība, atlasot procentuālās vērtības seguma kodu.</span><span class="sxs-lookup"><span data-stu-id="25d09-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="25d09-141">Sadaļā **Personisko kontaktpersonu piemērotības opcijas** katrai seguma opcijai pievienojiet atbilstošās personiskās kontaktpersonas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="25d09-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="25d09-142">Sadaļā **Patstāvīgi izmantojamais pakalpojums** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="25d09-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="25d09-143">Lauks</span><span class="sxs-lookup"><span data-stu-id="25d09-143">Field</span></span> | <span data-ttu-id="25d09-144">Apraksts</span><span class="sxs-lookup"><span data-stu-id="25d09-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="25d09-145">**Atļaut darbinieku ieguldījumu summu**</span><span class="sxs-lookup"><span data-stu-id="25d09-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="25d09-146">Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt iemaksu summu par atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="25d09-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="25d09-147">Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz iemaksu summu, ko darbinieks ievada atvieglojumu patstāvīgi izmantojamajā pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="25d09-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="25d09-148">**Atļaut darbinieku vajadzību summu**</span><span class="sxs-lookup"><span data-stu-id="25d09-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="25d09-149">Norāda, vai, atlasot atvieglojumus patstāvīgi izmantojamā pakalpojumā, atļaut darbiniekiem mainīt seguma summu par atvieglojumiem.</span><span class="sxs-lookup"><span data-stu-id="25d09-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="25d09-150">Ja atzīmējat šo izvēles rūtiņu, sistēma aprēķinās atvieglojumu plāna parametrus, pamatojoties uz seguma summu, ko darbinieks ievada darbinieku patstāvīgi izmantojamajā pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="25d09-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="25d09-151">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="25d09-151">Select **Save**.</span></span> 
