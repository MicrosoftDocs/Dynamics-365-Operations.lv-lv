---
title: Konfigurēt ieturējumus
description: Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.
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
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092733"
---
# <a name="configure-deductions"></a><span data-ttu-id="f0895-103">Konfigurēt ieturējumus</span><span class="sxs-lookup"><span data-stu-id="f0895-103">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f0895-104">Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.</span><span class="sxs-lookup"><span data-stu-id="f0895-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="f0895-105">Ieturējumi stājas spēkā noteiktā datumā, tāpēc varat uzturēt vēsturisku ieturējumu informācijas reģistru.</span><span class="sxs-lookup"><span data-stu-id="f0895-105">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="f0895-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Ieturējumi**.</span><span class="sxs-lookup"><span data-stu-id="f0895-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="f0895-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f0895-107">Select **New**.</span></span>

3. <span data-ttu-id="f0895-108">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="f0895-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f0895-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="f0895-109">Field</span></span> | <span data-ttu-id="f0895-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f0895-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f0895-111">Ieturējumi</span><span class="sxs-lookup"><span data-stu-id="f0895-111">Deduction</span></span> | <span data-ttu-id="f0895-112">Unikālais ID, kas tiek izmantots atvieglojumu ieturējumu identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="f0895-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="f0895-113">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f0895-113">Description</span></span> | <span data-ttu-id="f0895-114">Ieturējuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="f0895-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="f0895-115">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="f0895-115">Effective</span></span> | <span data-ttu-id="f0895-116">Sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="f0895-116">The start date.</span></span> <span data-ttu-id="f0895-117">Noklusējuma vērtība ir pašreizējais sistēmas datums.</span><span class="sxs-lookup"><span data-stu-id="f0895-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="f0895-118">Termiņa beigas</span><span class="sxs-lookup"><span data-stu-id="f0895-118">Expiration</span></span> | <span data-ttu-id="f0895-119">Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="f0895-119">The end date.</span></span> <span data-ttu-id="f0895-120">Noklusējuma vērtība ir 12/31/2154, kas nozīmē nekad.</span><span class="sxs-lookup"><span data-stu-id="f0895-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="f0895-121">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="f0895-121">Heading</span></span> | <span data-ttu-id="f0895-122">Virsraksta kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="f0895-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="f0895-123">To izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="f0895-123">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="f0895-124">Darbinieka algas ieturējumu atsauce</span><span class="sxs-lookup"><span data-stu-id="f0895-124">Employee payroll deduction reference</span></span> | <span data-ttu-id="f0895-125">Ieturējumu kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="f0895-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="f0895-126">Summas virsraksts</span><span class="sxs-lookup"><span data-stu-id="f0895-126">Amount heading</span></span> | <span data-ttu-id="f0895-127">Virsraksta kods no algu sistēmas, ko šī ieturējumu summa izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="f0895-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="f0895-128">To parasti izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="f0895-128">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="f0895-129">Var izdzēst</span><span class="sxs-lookup"><span data-stu-id="f0895-129">Can delete</span></span> | <span data-ttu-id="f0895-130">Norāda, vai eksportētā vērtība no Dynamics 365 for Finance and Operations var izraisīt vērtības dzēšanu algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="f0895-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="f0895-131">Pārī savienotās kolonnas</span><span class="sxs-lookup"><span data-stu-id="f0895-131">Paired columns</span></span> | <span data-ttu-id="f0895-132">Norāda, vai uz algu sistēmu eksportēt virsrakstu un ieturējumu summu pāra blakus esošās kolonnās.</span><span class="sxs-lookup"><span data-stu-id="f0895-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="f0895-133">Izmaiņu spēkā stāšanās datums</span><span class="sxs-lookup"><span data-stu-id="f0895-133">Change effective date</span></span> | <span data-ttu-id="f0895-134">Datums, kad atvieglojumu ieturējumu izmaiņas stāsies spēkā.</span><span class="sxs-lookup"><span data-stu-id="f0895-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="f0895-135">Šajā datumā sistēma automātiski mainīs atvieglojumu ieturējumu un atjauninās visus atvieglojumu plānus, kas saistīti ar šo ieturējumu, kamēr vien izpildāt ieturējumu izmaiņu atjaunināšanas apstrādi.</span><span class="sxs-lookup"><span data-stu-id="f0895-135">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="f0895-136">Ieturējumu maiņa ir pabeigta</span><span class="sxs-lookup"><span data-stu-id="f0895-136">Deduction change completed</span></span> | <span data-ttu-id="f0895-137">Tiklīdz ieturējumu atjaunināšanas apstrāde mainīs atvieglojumu ieturējumu likmi, izvēles rūtiņa Ieturējumu izmaiņas pabeigtas tiks atlasīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="f0895-137">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="f0895-138">Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.</span><span class="sxs-lookup"><span data-stu-id="f0895-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="f0895-139">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f0895-139">Select **Save**.</span></span> 
