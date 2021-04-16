---
title: PP lūgumu tipus un punktu skaitīšanas kritēriju izveide
description: Šajā ceļvedī ir parādīts, kā izveidot lūguma tipu un saistīt to ar punktu skaitīšanas metodi.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812066"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="1df90-103">PP lūgumu tipus un punktu skaitīšanas kritēriju izveide</span><span class="sxs-lookup"><span data-stu-id="1df90-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1df90-104">Šajā ceļvedī ir parādīts, kā izveidot lūguma tipu un saistīt to ar punktu skaitīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1df90-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="1df90-105">Tajā ir arī parādīts, kā lūguma tipu lietot piedāvājuma pieprasījumā (IP), kurš pēc tam iestata noklusējuma punktu skaitīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1df90-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="1df90-106">Šos uzdevumus parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="1df90-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="1df90-107">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="1df90-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="1df90-108">Pirms sākšanas jums ir jābūt pieejamai punktu skaitīšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="1df90-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="1df90-109">Lūguma veida izveide</span><span class="sxs-lookup"><span data-stu-id="1df90-109">Create a solicitation type</span></span>
1. <span data-ttu-id="1df90-110">Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Piedāvājuma pieprasījums > Lūguma tips.</span><span class="sxs-lookup"><span data-stu-id="1df90-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="1df90-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1df90-111">Click New.</span></span>
3. <span data-ttu-id="1df90-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1df90-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1df90-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1df90-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1df90-114">Laukā Punktu skaitīšanas metode atlasiet punktu skaitīšanas metodi, kuru vēlaties izmantot šim lūguma tipam.</span><span class="sxs-lookup"><span data-stu-id="1df90-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="1df90-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1df90-115">Click Save.</span></span>
7. <span data-ttu-id="1df90-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1df90-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="1df90-117">Lietot lūguma tipu</span><span class="sxs-lookup"><span data-stu-id="1df90-117">Use the solicitation type</span></span>
1. <span data-ttu-id="1df90-118">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="1df90-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="1df90-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1df90-119">Click New.</span></span>
3. <span data-ttu-id="1df90-120">Laukā Lūguma tips atlasiet lūguma tipu, kuru tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="1df90-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="1df90-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1df90-121">Click OK.</span></span>
5. <span data-ttu-id="1df90-122">Noklikšķiniet uz Punktu skaitīšanas kritēriji.</span><span class="sxs-lookup"><span data-stu-id="1df90-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="1df90-123">Rādītie punktu skaitīšanas kritēriji ir kritēriji no punktu skaitīšanas metodes, kuru esat saistījis ar šo lūguma tipu.</span><span class="sxs-lookup"><span data-stu-id="1df90-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="1df90-124">Kritērijus šajā lapā varat pievienot vai dzēst.</span><span class="sxs-lookup"><span data-stu-id="1df90-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="1df90-125">Varat arī pievienot jaunus kritērijus, kopējot tās no citām punktu skaitīšanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="1df90-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="1df90-126">Noklikšķiniet uz Kopēt kritērijus.</span><span class="sxs-lookup"><span data-stu-id="1df90-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="1df90-127">Laukā Punktu skaitīšanas metode ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1df90-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="1df90-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1df90-128">Click OK.</span></span>
9. <span data-ttu-id="1df90-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1df90-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]