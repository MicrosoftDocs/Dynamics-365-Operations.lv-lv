---
title: Ieturējumu konfigurēšana
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009828"
---
# <a name="configure-deductions"></a><span data-ttu-id="d65b3-102">Ieturējumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d65b3-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d65b3-103">Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.</span><span class="sxs-lookup"><span data-stu-id="d65b3-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="d65b3-104">Ieturējumi stājas spēkā noteiktā datumā, tāpēc varat uzturēt vēsturisku ieturējumu informācijas reģistru.</span><span class="sxs-lookup"><span data-stu-id="d65b3-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="d65b3-105">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Ieturējumi**.</span><span class="sxs-lookup"><span data-stu-id="d65b3-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="d65b3-106">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d65b3-106">Select **New**.</span></span>

3. <span data-ttu-id="d65b3-107">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="d65b3-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d65b3-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="d65b3-108">Field</span></span> | <span data-ttu-id="d65b3-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d65b3-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d65b3-110">Ieturējumi</span><span class="sxs-lookup"><span data-stu-id="d65b3-110">Deduction</span></span> | <span data-ttu-id="d65b3-111">Unikālais ID, kas tiek izmantots atvieglojumu ieturējumu identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="d65b3-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="d65b3-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d65b3-112">Description</span></span> | <span data-ttu-id="d65b3-113">Ieturējuma apraksts.</span><span class="sxs-lookup"><span data-stu-id="d65b3-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="d65b3-114">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="d65b3-114">Effective</span></span> | <span data-ttu-id="d65b3-115">Sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="d65b3-115">The start date.</span></span> <span data-ttu-id="d65b3-116">Noklusējuma vērtība ir pašreizējais sistēmas datums.</span><span class="sxs-lookup"><span data-stu-id="d65b3-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="d65b3-117">Termiņa beigas</span><span class="sxs-lookup"><span data-stu-id="d65b3-117">Expiration</span></span> | <span data-ttu-id="d65b3-118">Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="d65b3-118">The end date.</span></span> <span data-ttu-id="d65b3-119">Noklusējuma vērtība ir 12/31/2154, kas nozīmē nekad.</span><span class="sxs-lookup"><span data-stu-id="d65b3-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="d65b3-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="d65b3-120">Heading</span></span> | <span data-ttu-id="d65b3-121">Virsraksta kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="d65b3-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d65b3-122">To izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="d65b3-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d65b3-123">Darbinieka algas ieturējumu atsauce</span><span class="sxs-lookup"><span data-stu-id="d65b3-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="d65b3-124">Ieturējumu kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="d65b3-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="d65b3-125">Summas virsraksts</span><span class="sxs-lookup"><span data-stu-id="d65b3-125">Amount heading</span></span> | <span data-ttu-id="d65b3-126">Virsraksta kods no algu sistēmas, ko šī ieturējumu summa izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas.</span><span class="sxs-lookup"><span data-stu-id="d65b3-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d65b3-127">To parasti izmanto, kad izmantojat trešās puses algu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="d65b3-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d65b3-128">Var izdzēst</span><span class="sxs-lookup"><span data-stu-id="d65b3-128">Can delete</span></span> | <span data-ttu-id="d65b3-129">Norāda, vai eksportētā vērtība no Dynamics 365 for Finance and Operations var izraisīt vērtības dzēšanu algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d65b3-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="d65b3-130">Pārī savienotās kolonnas</span><span class="sxs-lookup"><span data-stu-id="d65b3-130">Paired columns</span></span> | <span data-ttu-id="d65b3-131">Norāda, vai uz algu sistēmu eksportēt virsrakstu un ieturējumu summu pāra blakus esošās kolonnās.</span><span class="sxs-lookup"><span data-stu-id="d65b3-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="d65b3-132">Izmaiņu spēkā stāšanās datums</span><span class="sxs-lookup"><span data-stu-id="d65b3-132">Change effective date</span></span> | <span data-ttu-id="d65b3-133">Datums, kad atvieglojumu ieturējumu izmaiņas stāsies spēkā.</span><span class="sxs-lookup"><span data-stu-id="d65b3-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="d65b3-134">Šajā datumā sistēma automātiski mainīs atvieglojumu ieturējumu un atjauninās visus atvieglojumu plānus, kas saistīti ar šo ieturējumu, kamēr vien izpildāt ieturējumu izmaiņu atjaunināšanas apstrādi.</span><span class="sxs-lookup"><span data-stu-id="d65b3-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="d65b3-135">Ieturējumu maiņa ir pabeigta</span><span class="sxs-lookup"><span data-stu-id="d65b3-135">Deduction change completed</span></span> | <span data-ttu-id="d65b3-136">Tiklīdz ieturējumu atjaunināšanas apstrāde mainīs atvieglojumu ieturējumu likmi, izvēles rūtiņa Ieturējumu izmaiņas pabeigtas tiks atlasīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="d65b3-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="d65b3-137">Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.</span><span class="sxs-lookup"><span data-stu-id="d65b3-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="d65b3-138">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d65b3-138">Select **Save**.</span></span> 
