---
title: Pienākumu sadales iestatīšana
description: Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcbd32131f9980a4f55e91b9d7ad48171069f72e
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826398"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="99af9-103">Pienākumu sadales iestatīšana</span><span class="sxs-lookup"><span data-stu-id="99af9-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99af9-104">Var iestatīt nosacījumus, lai atdalītu uzdevumus, kas ir jāveic dažādiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="99af9-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="99af9-105">Šī koncepcija ir nosaukta par pienākumu sadali.</span><span class="sxs-lookup"><span data-stu-id="99af9-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="99af9-106">Piemēram, iespējams, nevēlēsieties, lai viena un tā pati persona apstiprina preču saņemšanu un apstrādātu maksājumus kreditoram.</span><span class="sxs-lookup"><span data-stu-id="99af9-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="99af9-107">Pienākumu sadale palīdz samazināt pārkāpumu risku un palīdz arī noteikt kļūdas vai neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="99af9-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="99af9-108">Pienākumu sadali var izmantot arī, lai lietotu iekšējās kontroles politikas.</span><span class="sxs-lookup"><span data-stu-id="99af9-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="99af9-109">Lai izveidotu nosacījumus, veiciet tālākminēto procedūru.</span><span class="sxs-lookup"><span data-stu-id="99af9-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="99af9-110">Lai izpildītu šo procedūru, jums ir jābūt sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="99af9-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="99af9-111">Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Pienākumu sadale** > **Pienākumu sadales nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="99af9-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="99af9-112">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="99af9-112">Click **New**.</span></span>
3. <span data-ttu-id="99af9-113">Laukā **Nosaukums** ierakstiet kārtulas vērtību.</span><span class="sxs-lookup"><span data-stu-id="99af9-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="99af9-114">Laukā **Pirmais pienākums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="99af9-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="99af9-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="99af9-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="99af9-116">Atlasiet pirmo pienākumu, ko kontrolē nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="99af9-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="99af9-117">Laukā **Otrais pienākums** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="99af9-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="99af9-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="99af9-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="99af9-119">Atlasiet otro pienākumu, ko kontrolē nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="99af9-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="99af9-120">Laukā **Stingrība** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="99af9-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="99af9-121">Atlasiet riska smagumu, kas rodas, ja viens un tas pats lietotājs vai loma pilda abus pienākumus.</span><span class="sxs-lookup"><span data-stu-id="99af9-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="99af9-122">Laukā **Drošības risks** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="99af9-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="99af9-123">Ievadiet drošības riska aprakstu.</span><span class="sxs-lookup"><span data-stu-id="99af9-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="99af9-124">Laukā **Drošības mazinājums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="99af9-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="99af9-125">Ievadiet darbību parakstu, kas jāveic, lai mazinātu drošības risku.</span><span class="sxs-lookup"><span data-stu-id="99af9-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="99af9-126">Piemēram, var mazināt risku, veicot detalizētāku procesa pārskatīšanu, veicot ikmēneša vadības pārskatīšanu vai koplietojot resursus ar citām nodaļām.</span><span class="sxs-lookup"><span data-stu-id="99af9-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="99af9-127">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="99af9-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="99af9-128">Veidojot kārtulu, pienākumu sadales kārtulas netiek pārbaudītas.</span><span class="sxs-lookup"><span data-stu-id="99af9-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="99af9-129">Varat izveidot kārtulu, kas izveido konfliktu esošajām lomām.</span><span class="sxs-lookup"><span data-stu-id="99af9-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="99af9-130">Esošās lietotāja lomu piešķires var arī būt pretrunā ar jauno kārtulu.</span><span class="sxs-lookup"><span data-stu-id="99af9-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="99af9-131">Pēc kārtulas izveidošanas vai modificēšanas ir jāpārbauda atbilstība.</span><span class="sxs-lookup"><span data-stu-id="99af9-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="99af9-132">Papildinformāciju skatiet sadaļā [Pienākumu sadales konfliktu identificēšana un atrisināšana](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="99af9-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>
