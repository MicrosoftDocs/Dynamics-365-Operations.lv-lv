---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (4. daļa. Pārskata palaišana)
description: Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406478"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="81798-103">ER finanšu dimensijas, ko izmanto kā datu avotu (4. daļa. Pārskata palaišana)</span><span class="sxs-lookup"><span data-stu-id="81798-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81798-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="81798-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="81798-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="81798-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="81798-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (3. daļa: Pārskata izkārtošana).</span><span class="sxs-lookup"><span data-stu-id="81798-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="81798-107">Jums nepieciešams konfigurēt arī noklusējuma dokumentu veidus Elektronisko pārskatu veidošanas parametru lapā.</span><span class="sxs-lookup"><span data-stu-id="81798-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="81798-108">Noklusējuma dokumentu veidi tiek iestatīti arī lejupielādējot un importējot jebkādu ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="81798-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="81798-109">Palaist pārskatu</span><span class="sxs-lookup"><span data-stu-id="81798-109">Run report</span></span>
1. <span data-ttu-id="81798-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="81798-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="81798-111">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="81798-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="81798-112">Kokā atlasiet 'Finanšu dimensiju parauga modelis\Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="81798-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="81798-113">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="81798-113">Click Run.</span></span>
<span data-ttu-id="81798-114">![ER konfigurāciju lapa](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="81798-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="81798-115">Ievadiet vai atlasiet vērtību laukā Dimensijas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="81798-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="81798-116">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="81798-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER konfigurāciju lapa](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="81798-118">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="81798-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="81798-119">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="81798-119">Click Filter.</span></span>
8. <span data-ttu-id="81798-120">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="81798-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="81798-121">Laukā Kritēriji ierakstiet '00057'.</span><span class="sxs-lookup"><span data-stu-id="81798-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="81798-122">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="81798-122">Click OK.</span></span>
11. <span data-ttu-id="81798-123">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="81798-123">Click OK.</span></span>
<span data-ttu-id="81798-124">![ER konfigurāciju lapa](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="81798-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="81798-125">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="81798-125">Review the generated output.</span></span> <span data-ttu-id="81798-126">Katrai darbībai no izvēlētās partija, tiek piedāvātas finanšu dimensijas no atbilstošajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="81798-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="81798-127">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskatu nav atkarīgs no atlasīto dimensiju skaita, vai dimensiju skaita, kas ir konfigurētas šai instancei.</span><span class="sxs-lookup"><span data-stu-id="81798-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER konfigurāciju lapa](../media/er-financial-dimensions-guides-run4.png)
