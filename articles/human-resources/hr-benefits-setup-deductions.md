---
title: Konfigurēt ieturējumus
description: Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.
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
ms.openlocfilehash: 5e645c3f098163626cb686aba347897781d7ebc0
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230066"
---
# <a name="configure-deductions"></a><span data-ttu-id="c7910-103">Konfigurēt ieturējumus</span><span class="sxs-lookup"><span data-stu-id="c7910-103">Configure deductions</span></span>

<span data-ttu-id="c7910-104">Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.</span><span class="sxs-lookup"><span data-stu-id="c7910-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="c7910-105">Ieturējumi stājas spēkā noteiktā datumā, tāpēc varat uzturēt vēsturisku ieturējumu informācijas reģistru.</span><span class="sxs-lookup"><span data-stu-id="c7910-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="c7910-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Ieturējumi**.</span><span class="sxs-lookup"><span data-stu-id="c7910-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="c7910-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c7910-107">Select **New**.</span></span>

3. <span data-ttu-id="c7910-108">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="c7910-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c7910-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="c7910-109">Field</span></span> | <span data-ttu-id="c7910-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c7910-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c7910-111">**Ieturējumi**</span><span class="sxs-lookup"><span data-stu-id="c7910-111">**Deduction**</span></span> | <span data-ttu-id="c7910-112">Unikālais ID, kas tiek izmantots atvieglojumu ieturējumu identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7910-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="c7910-113">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="c7910-113">**Description**</span></span> | <span data-ttu-id="c7910-114">Ieturējuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="c7910-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="c7910-115">**Ir spēkā**</span><span class="sxs-lookup"><span data-stu-id="c7910-115">**Effective**</span></span> | <span data-ttu-id="c7910-116">Sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="c7910-116">The start date.</span></span> <span data-ttu-id="c7910-117">Noklusējuma vērtība ir pašreizējais sistēmas datums.</span><span class="sxs-lookup"><span data-stu-id="c7910-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="c7910-118">**Termiņa beigas**</span><span class="sxs-lookup"><span data-stu-id="c7910-118">**Expiration**</span></span> | <span data-ttu-id="c7910-119">Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="c7910-119">The end date.</span></span> <span data-ttu-id="c7910-120">Noklusējuma vērtība ir 12/31/2154, kas nozīmē nekad.</span><span class="sxs-lookup"><span data-stu-id="c7910-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="c7910-121">**Virsraksts**</span><span class="sxs-lookup"><span data-stu-id="c7910-121">**Heading**</span></span> | <span data-ttu-id="c7910-122">Virsraksta kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="c7910-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c7910-123">To izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="c7910-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="c7910-124">**Darbinieka algas ieturējumu atsauce**</span><span class="sxs-lookup"><span data-stu-id="c7910-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="c7910-125">Ieturējumu kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="c7910-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="c7910-126">**Summas virsraksts**</span><span class="sxs-lookup"><span data-stu-id="c7910-126">**Amount heading**</span></span> | <span data-ttu-id="c7910-127">Virsraksta kods no algu sistēmas, ko šī ieturējumu summa izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="c7910-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c7910-128">To parasti izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="c7910-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="c7910-129">**Var izdzēst**</span><span class="sxs-lookup"><span data-stu-id="c7910-129">**Can delete**</span></span> | <span data-ttu-id="c7910-130">Norāda, vai eksportētā vērtība no Dynamics 365 for Finance and Operations var izraisīt vērtības dzēšanu algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c7910-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="c7910-131">**Pārī savienotās kolonnas**</span><span class="sxs-lookup"><span data-stu-id="c7910-131">**Paired columns**</span></span> | <span data-ttu-id="c7910-132">Norāda, vai uz algu sistēmu eksportēt virsrakstu un ieturējumu summu pāra blakus esošās kolonnās.</span><span class="sxs-lookup"><span data-stu-id="c7910-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="c7910-133">**Izmaiņu spēkā stāšanās datums**</span><span class="sxs-lookup"><span data-stu-id="c7910-133">**Change effective date**</span></span> | <span data-ttu-id="c7910-134">Datums, kad atvieglojumu ieturējumu izmaiņas stāsies spēkā.</span><span class="sxs-lookup"><span data-stu-id="c7910-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="c7910-135">Šajā datumā sistēma automātiski maina atvieglojumu ieturējumu un atjaunina visus atvieglojumu plānus, kas saistīti ar šo ieturējumu, kamēr vien izpildāt **Ieturējumu izmaiņu atjaunināšanas** apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c7910-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="c7910-136">**Ieturējumu maiņa ir pabeigta**</span><span class="sxs-lookup"><span data-stu-id="c7910-136">**Deduction change completed**</span></span> | <span data-ttu-id="c7910-137">Tiklīdz ieturējumu atjaunināšanas apstrāde mainīs atvieglojumu ieturējumu likmi, izvēles rūtiņa **Ieturējumu izmaiņas pabeigtas** tiks atlasīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="c7910-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="c7910-138">Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.</span><span class="sxs-lookup"><span data-stu-id="c7910-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="c7910-139">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c7910-139">Select **Save**.</span></span> 
