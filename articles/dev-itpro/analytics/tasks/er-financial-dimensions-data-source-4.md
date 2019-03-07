---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (4. daļa. Pārskata palaišana)
description: Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "345287"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="532ae-103">ER Finanšu dimensijas, ko izmanto kā datu avotu (4. daļa: Palaist pārskatu)</span><span class="sxs-lookup"><span data-stu-id="532ae-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="532ae-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="532ae-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="532ae-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="532ae-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="532ae-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (3. daļa: Pārskata izkārtošana).</span><span class="sxs-lookup"><span data-stu-id="532ae-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="532ae-107">Jums nepieciešams konfigurēt arī noklusējuma dokumentu veidus Elektronisko pārskatu veidošanas parametru lapā.</span><span class="sxs-lookup"><span data-stu-id="532ae-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="532ae-108">Noklusējuma dokumentu veidi tiek iestatīti arī lejupielādējot un importējot jebkādu ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="532ae-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="532ae-109">Palaist pārskatu</span><span class="sxs-lookup"><span data-stu-id="532ae-109">Run report</span></span>
1. <span data-ttu-id="532ae-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="532ae-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="532ae-111">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="532ae-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="532ae-112">Kokā atlasiet 'Finanšu dimensiju parauga modelis\Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="532ae-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="532ae-113">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="532ae-113">Click Run.</span></span>
5. <span data-ttu-id="532ae-114">Laukā Dimensijas nosaukums, Laukā Dimensijas nosaukums ievadiet vai atlasiet kādu vērtību..</span><span class="sxs-lookup"><span data-stu-id="532ae-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="532ae-115">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="532ae-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="532ae-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="532ae-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="532ae-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="532ae-117">Click Filter.</span></span>
8. <span data-ttu-id="532ae-118">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="532ae-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="532ae-119">Laukā Kritēriji ierakstiet '00057'.</span><span class="sxs-lookup"><span data-stu-id="532ae-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="532ae-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="532ae-120">Click OK.</span></span>
11. <span data-ttu-id="532ae-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="532ae-121">Click OK.</span></span>
    * <span data-ttu-id="532ae-122">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="532ae-122">Review the generated output.</span></span> <span data-ttu-id="532ae-123">Ņemiet vērā, ka katrai darbībai no izvēlētās partijas, tiek piedāvātas finanšu dimensijas no atbilstošajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="532ae-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="532ae-124">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai dimensiju skaita, kas ir konfigurētas šai Dynamics 365 for Finance and Operations Enterprise edition instancei.</span><span class="sxs-lookup"><span data-stu-id="532ae-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

