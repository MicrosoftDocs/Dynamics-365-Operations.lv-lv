---
title: Neatbilstību diagnostikas tipi
description: Šajā tēmā ir aprakstīts, kā izmantot un izveidot diagnostikas tipus, kas var tikt izmantoti ar neatbilstībām.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022280"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="65b02-103">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="65b02-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65b02-104">Šajā tēmā ir aprakstīts, kā izmantot un izveidot diagnostikas tipus, kas var tikt izmantoti ar neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="65b02-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="65b02-105">Izmantojiet lapu **Diagnostikas tipi**, lai definētu diagnostikas darbību klasifikāciju.</span><span class="sxs-lookup"><span data-stu-id="65b02-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="65b02-106">Pēc tam, veidojot neatbilstības labojumu, atlasiet diagnostiku.</span><span class="sxs-lookup"><span data-stu-id="65b02-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="65b02-107">Labojumā norāda, kāda veida diagnostikas darbība jāveic attiecībā uz apstiprināto neatbilstību un kam tā ir jāveic.</span><span class="sxs-lookup"><span data-stu-id="65b02-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="65b02-108">Tajā norāda arī pieprasīto un plānotais pabeigšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="65b02-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="65b02-109">Diagnostikas tipu paraugi</span><span class="sxs-lookup"><span data-stu-id="65b02-109">Examples of diagnostic types</span></span>

<span data-ttu-id="65b02-110">Jūs strādājat ražošanas uzņēmumā, un vairākiem krājumiem ir nesekmīgi kvalitātes testi.</span><span class="sxs-lookup"><span data-stu-id="65b02-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="65b02-111">Šie krājumi tiek pārvietoti karantīnas zonā un iezīmēti kā neatbilstoši produkti.</span><span class="sxs-lookup"><span data-stu-id="65b02-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="65b02-112">Neatbilstības ieraksts tiek izveidots programmā Microsoft Dynamics 365 Supply Chain Management, lai varētu izsekot detalizētu informāciju, izmantojot problēmas atrisināšanu.</span><span class="sxs-lookup"><span data-stu-id="65b02-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="65b02-113">Šajā gadījumā kvalitātes problēmas rodas tāpēc, ka iekārtas gultņi, kas sapako preces, ir bijuši slikti un pārkarsuši.</span><span class="sxs-lookup"><span data-stu-id="65b02-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="65b02-114">Šīs problēmas labojums ir aizvietot iekārtas daļas.</span><span class="sxs-lookup"><span data-stu-id="65b02-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="65b02-115">Konfigurējot diagnostikas tipus, var izveidot daudzus ierakstus, no kuriem katrs parāda atšķirīgu problēmas tipu, kāds var būt iekārtai.</span><span class="sxs-lookup"><span data-stu-id="65b02-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="65b02-116">Alternatīvi jūs varat izveidot vienu vispārēju diagnostikas tipu, kas pārstāv iekārtu remontu.</span><span class="sxs-lookup"><span data-stu-id="65b02-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="65b02-117">Izveidot diagnostikas tipu</span><span class="sxs-lookup"><span data-stu-id="65b02-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="65b02-118">Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Diagnostikas tipi**.</span><span class="sxs-lookup"><span data-stu-id="65b02-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="65b02-119">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="65b02-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="65b02-120">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="65b02-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="65b02-121">**Diagnostika** - Ievadiet unikālu diagnostikas tipa ID vai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="65b02-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="65b02-122">**Apraksts** — ievadiet diagnostikas tipa detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="65b02-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="65b02-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="65b02-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65b02-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="65b02-124">Additional resources</span></span>

- [<span data-ttu-id="65b02-125">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="65b02-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="65b02-126">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="65b02-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="65b02-127">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="65b02-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="65b02-128">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="65b02-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="65b02-129">Neatbilstību problēmu tipi</span><span class="sxs-lookup"><span data-stu-id="65b02-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="65b02-130">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="65b02-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="65b02-131">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="65b02-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="65b02-132">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="65b02-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
