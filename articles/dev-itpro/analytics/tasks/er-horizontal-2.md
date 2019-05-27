---
title: ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)
description: Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes.
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
ms.openlocfilehash: 33c1a3134659bb66a67166fec3d7f53af0aa4c6c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544430"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2-run-format"></a><span data-ttu-id="bb803-103">ER izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas programmas Excel pārskatos (2. daļa: Palaist formātu)</span><span class="sxs-lookup"><span data-stu-id="bb803-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb803-104">Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes.</span><span class="sxs-lookup"><span data-stu-id="bb803-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="bb803-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="bb803-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="bb803-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz procedūras “ER Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos (1. daļa: Izstrādāt formātu)“ darbības.</span><span class="sxs-lookup"><span data-stu-id="bb803-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="bb803-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="bb803-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="bb803-108">Atrast izveidoto formātu</span><span class="sxs-lookup"><span data-stu-id="bb803-108">Find created format</span></span>
1. <span data-ttu-id="bb803-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bb803-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bb803-110">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="bb803-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bb803-111">Koka struktūrā atlasiet 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span><span class="sxs-lookup"><span data-stu-id="bb803-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="bb803-112">Izpildīt formātu, lai izveidotu Excel izvadi</span><span class="sxs-lookup"><span data-stu-id="bb803-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="bb803-113">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="bb803-113">Click Run.</span></span>
2. <span data-ttu-id="bb803-114">Laukā Dimensijas ierakstiet 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="bb803-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="bb803-115">Ievadiet vai atlasiet vērtību laukā Dimensijas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="bb803-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="bb803-116">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="bb803-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="bb803-117">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="bb803-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="bb803-118">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="bb803-118">Click Filter.</span></span>
5. <span data-ttu-id="bb803-119">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="bb803-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="bb803-120">Laukā Kritēriji ierakstiet '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="bb803-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="bb803-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="bb803-121">00057..00058</span></span>  
7. <span data-ttu-id="bb803-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bb803-122">Click OK.</span></span>
8. <span data-ttu-id="bb803-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bb803-123">Click OK.</span></span>
    * <span data-ttu-id="bb803-124">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bb803-124">Review the generated output.</span></span> <span data-ttu-id="bb803-125">Ņemiet vērā, ka tikko izveidotais Excel fails ietver finanšu dimensijām atlasīto kolonnu skaitu.</span><span class="sxs-lookup"><span data-stu-id="bb803-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="bb803-126">Pārskata galvenē šajās kolonnās ir norādīti finanšu dimensiju nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="bb803-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="bb803-127">Transakcijas rindās šajās kolonnās ir norādītas finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bb803-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="bb803-128">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskats nav atkarīgs no atlasīto dimensiju skaita vai dimensiju skaita, kas ir konfigurētas šai Dynamics 365 for Finance and Operations Enterprise edition instancei.</span><span class="sxs-lookup"><span data-stu-id="bb803-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

