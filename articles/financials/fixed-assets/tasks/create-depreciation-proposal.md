---
title: Izveidot nolietojuma priekšlikumu
description: Šajā procedūrā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549539"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="4625c-103">Izveidot nolietojuma priekšlikumu</span><span class="sxs-lookup"><span data-stu-id="4625c-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4625c-104">Šajā procedūrā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="4625c-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="4625c-105">Šajā uzdevumā izmantots USMF demonstrācijas uzņēmums un grāmatveža loma.</span><span class="sxs-lookup"><span data-stu-id="4625c-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="4625c-106">Izveidot nolietojuma priekšlikumu</span><span class="sxs-lookup"><span data-stu-id="4625c-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="4625c-107">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="4625c-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="4625c-108">Laukā Žurnāla nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4625c-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4625c-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4625c-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4625c-110">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="4625c-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4625c-111">Atlasiet opciju Izveidot nolietojuma kopsavilkumu, lai ikmēneša nolietojumiem izveidotu kopsavilkumu vienā žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="4625c-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="4625c-112">Piemēram, ja beigu datuma vērtība ir 2015. gada 31. marts, tiek ģenerēts šādam apraksts: "Nolietojums kopš 2015. gada 31. janvāra".</span><span class="sxs-lookup"><span data-stu-id="4625c-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="4625c-113">Pēc tam piedāvātajās žurnāla rindās, laukā Datums tiek iestatīta vērtība 2015. gada 31. marts.</span><span class="sxs-lookup"><span data-stu-id="4625c-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="4625c-114">Nolietojuma priekšlikumu var filtrēt pēc pamatlīdzekļa, pamatlīdzekļu grupas vai citiem kritērijiem, izmantojot filtra opciju.</span><span class="sxs-lookup"><span data-stu-id="4625c-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="4625c-115">Pamatlīdzekļu veidnē lietojot Izveidot iegādes vai nolietojuma priekšlikumus, varat ierosināt nolietojumu paketēs.</span><span class="sxs-lookup"><span data-stu-id="4625c-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="4625c-116">Šo iespēju ieteicams izmantot lielākiem priekšlikumiem, kas aizņem vairāk sistēmas resursu.</span><span class="sxs-lookup"><span data-stu-id="4625c-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="4625c-117">Ja atlasāt pakešu opciju, šajā laikā varat pabeigt citus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="4625c-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="4625c-118">Kad piedāvājat nolietojumu veikt šādi, nolietojums tiek aprēķināts pamatlīdzekļu vērtības modeļiem.</span><span class="sxs-lookup"><span data-stu-id="4625c-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="4625c-119">Noklikšķiniet uz Izveidot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="4625c-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="4625c-120">Nolietojuma ierakstu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="4625c-120">Review depreciation entries</span></span>
1. <span data-ttu-id="4625c-121">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="4625c-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="4625c-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4625c-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4625c-123">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="4625c-123">Click Lines.</span></span>
4. <span data-ttu-id="4625c-124">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="4625c-124">Click Post.</span></span>

