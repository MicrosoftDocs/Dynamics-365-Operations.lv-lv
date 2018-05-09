--- 
title: "Tā pārskata darbināšana, kurā finanšu dimensijas ir izmantotas kā datu avots"
description: "Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fefac4db9d6fec926068483bbe8ae91a6d5d6028
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source"></a><span data-ttu-id="99269-103">Tā pārskata darbināšana, kurā finanšu dimensijas ir izmantotas kā datu avots</span><span class="sxs-lookup"><span data-stu-id="99269-103">Run a report that uses financial dimensions as a data source</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99269-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="99269-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="99269-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="99269-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="99269-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (3. daļa: Pārskata izkārtošana).</span><span class="sxs-lookup"><span data-stu-id="99269-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="99269-107">Jums nepieciešams konfigurēt arī noklusējuma dokumentu veidus Elektronisko pārskatu veidošanas parametru lapā.</span><span class="sxs-lookup"><span data-stu-id="99269-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="99269-108">Noklusējuma dokumentu veidi tiek iestatīti arī lejupielādējot un importējot jebkādu ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="99269-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="99269-109">Palaist pārskatu</span><span class="sxs-lookup"><span data-stu-id="99269-109">Run report</span></span>
1. <span data-ttu-id="99269-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="99269-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="99269-111">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="99269-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="99269-112">Kokā atlasiet 'Finanšu dimensiju parauga modelis\Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="99269-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="99269-113">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="99269-113">Click Run.</span></span>
5. <span data-ttu-id="99269-114">Laukā Dimensijas nosaukums ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="99269-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="99269-115">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="99269-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="99269-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="99269-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="99269-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="99269-117">Click Filter.</span></span>
8. <span data-ttu-id="99269-118">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="99269-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="99269-119">Laukā Kritēriji ierakstiet '00057'.</span><span class="sxs-lookup"><span data-stu-id="99269-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="99269-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="99269-120">Click OK.</span></span>
11. <span data-ttu-id="99269-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="99269-121">Click OK.</span></span>
    * <span data-ttu-id="99269-122">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="99269-122">Review the generated output.</span></span> <span data-ttu-id="99269-123">Ņemiet vērā, ka katrai darbībai no izvēlētās partijas, tiek piedāvātas finanšu dimensijas no atbilstošajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="99269-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="99269-124">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai no šai Dynamics 365 for Finance and Operations instancei konfigurēto dimensiju skaita.</span><span class="sxs-lookup"><span data-stu-id="99269-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


