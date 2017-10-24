--- 
title: "Palaist pārskatu, kas izmanto finanšu dimensijas kā datu avotu elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="39038-103">Palaist pārskatu, kas izmanto finanšu dimensijas kā datu avotu elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="39038-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39038-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="39038-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="39038-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="39038-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="39038-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (3. daļa: Pārskata izkārtošana).</span><span class="sxs-lookup"><span data-stu-id="39038-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="39038-107">Jums nepieciešams konfigurēt arī noklusējuma dokumentu veidus Elektronisko pārskatu veidošanas parametru lapā.</span><span class="sxs-lookup"><span data-stu-id="39038-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="39038-108">Noklusējuma dokumentu veidi tiek iestatīti arī lejupielādējot un importējot jebkādu ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="39038-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="39038-109">Palaist pārskatu</span><span class="sxs-lookup"><span data-stu-id="39038-109">Run report</span></span>
1. <span data-ttu-id="39038-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="39038-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="39038-111">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="39038-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="39038-112">Kokā atlasiet 'Finanšu dimensiju parauga modelis\Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="39038-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="39038-113">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="39038-113">Click Run.</span></span>
5. <span data-ttu-id="39038-114">Laukā Dimensijas nosaukums, Laukā Dimensijas nosaukums ievadiet vai atlasiet kādu vērtību..</span><span class="sxs-lookup"><span data-stu-id="39038-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="39038-115">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="39038-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="39038-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="39038-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="39038-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="39038-117">Click Filter.</span></span>
8. <span data-ttu-id="39038-118">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="39038-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="39038-119">Laukā Kritēriji ierakstiet '00057'.</span><span class="sxs-lookup"><span data-stu-id="39038-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="39038-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="39038-120">Click OK.</span></span>
11. <span data-ttu-id="39038-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="39038-121">Click OK.</span></span>
    * <span data-ttu-id="39038-122">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="39038-122">Review the generated output.</span></span> <span data-ttu-id="39038-123">Ņemiet vērā, ka katrai darbībai no izvēlētās partijas, tiek piedāvātas finanšu dimensijas no atbilstošajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="39038-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="39038-124">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai dimensiju skaita, kas ir konfigurētas šai Dynamics 365 for Finance and Operations Enterprise edition instancei.</span><span class="sxs-lookup"><span data-stu-id="39038-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


