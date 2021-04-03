---
title: ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā OPENXML darblapu (Excel) failus. (2. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0b8c997549bca2cae5500c926ccba916a473b5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569537"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="bd409-104">ER horizontāli paplašināmi diapazoni, ko izmanto dinamiskai kolonnu pievienošanai programmas Excel pārskatos (2. daļa. Formāta palaišana)</span><span class="sxs-lookup"><span data-stu-id="bd409-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd409-105">Tālāk norādītās darbības izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izveidotu pārskatus kā OPENXML darblapas (Excel) failus, kuros var dinamiski izveidot nepieciešamās kolonnas kā horizontāli izvēršamas virknes.</span><span class="sxs-lookup"><span data-stu-id="bd409-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="bd409-106">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="bd409-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="bd409-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz procedūras "ER Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos (1. daļa: Izstrādāt formātu)" darbības.</span><span class="sxs-lookup"><span data-stu-id="bd409-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="bd409-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="bd409-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="bd409-109">Atrast izveidoto formātu</span><span class="sxs-lookup"><span data-stu-id="bd409-109">Find created format</span></span>
1. <span data-ttu-id="bd409-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bd409-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bd409-111">Kokā izvērsiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="bd409-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bd409-112">Koka struktūrā atlasiet 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span><span class="sxs-lookup"><span data-stu-id="bd409-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="bd409-113">Izpildīt formātu, lai izveidotu Excel izvadi</span><span class="sxs-lookup"><span data-stu-id="bd409-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="bd409-114">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="bd409-114">Click Run.</span></span>
2. <span data-ttu-id="bd409-115">Laukā Dimensijas ierakstiet 'BusinessUnit;CostCenter;Department'.</span><span class="sxs-lookup"><span data-stu-id="bd409-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="bd409-116">Ievadiet vai atlasiet vērtību laukā Dimensijas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="bd409-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="bd409-117">Lai atlasītu visas pašreizējā uzņēmuma dimensijas, ievadiet tālāk norādīto informāciju: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="bd409-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="bd409-118">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="bd409-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="bd409-119">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="bd409-119">Click Filter.</span></span>
5. <span data-ttu-id="bd409-120">Atlasiet rindu tabulai Virsgrāmatas žurnāls un laukam Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="bd409-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="bd409-121">Laukā Kritēriji ierakstiet '00057..00058'.</span><span class="sxs-lookup"><span data-stu-id="bd409-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="bd409-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="bd409-122">00057..00058</span></span>  
7. <span data-ttu-id="bd409-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bd409-123">Click OK.</span></span>
8. <span data-ttu-id="bd409-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bd409-124">Click OK.</span></span>
    * <span data-ttu-id="bd409-125">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bd409-125">Review the generated output.</span></span> <span data-ttu-id="bd409-126">Ņemiet vērā, ka tikko izveidotais Excel fails ietver finanšu dimensijām atlasīto kolonnu skaitu.</span><span class="sxs-lookup"><span data-stu-id="bd409-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="bd409-127">Pārskata galvenē šajās kolonnās ir norādīti finanšu dimensiju nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="bd409-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="bd409-128">Transakcijas rindās šajās kolonnās ir norādītas finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bd409-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="bd409-129">Palaidiet šo pārskatu un atlasiet dažādas dimensijas, lai pārliecinātos, ka pārskatu nav atkarīgs no atlasīto dimensiju skaita, vai dimensiju skaita, kas ir konfigurētas šai instancei.</span><span class="sxs-lookup"><span data-stu-id="bd409-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]