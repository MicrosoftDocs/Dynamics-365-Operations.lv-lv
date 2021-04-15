---
title: Nolietojuma priekšlikuma izveide
description: Šajā tēmā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013c768c8a016f399a27b1488ad0d5b339fdf7cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813583"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="2662b-103">Nolietojuma priekšlikuma izveide</span><span class="sxs-lookup"><span data-stu-id="2662b-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2662b-104">Šajā tēmā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="2662b-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="2662b-105">Šajā uzdevumā izmantots USMF demonstrācijas uzņēmums un grāmatveža loma.</span><span class="sxs-lookup"><span data-stu-id="2662b-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="2662b-106">Nolietojuma priekšlikuma izveide</span><span class="sxs-lookup"><span data-stu-id="2662b-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="2662b-107">Navigācijas rūtī ejiet uz **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma priekšlikumu**.</span><span class="sxs-lookup"><span data-stu-id="2662b-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="2662b-108">Laukā **Žurnāla nosaukums** nolaižamajā izvēlnē atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2662b-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="2662b-109">Ievadiet datumu laukā **Līdz datumam**.</span><span class="sxs-lookup"><span data-stu-id="2662b-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="2662b-110">Atlasiet opciju **Nolietojuma kopsavilkums**, lai apkopotu ikmēneša nolietojumus vienā žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="2662b-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="2662b-111">Piemēram, ja beigu datuma vērtība ir 2015. gada 31. marts, tiek ģenerēts šādam apraksts: "Nolietojums kopš 2015. gada 31. janvāra".</span><span class="sxs-lookup"><span data-stu-id="2662b-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="2662b-112">Tad lauks **Datums** piedāvātajās žurnāla līnijās tiek iestatīts kā 2015. gada 31. marts.</span><span class="sxs-lookup"><span data-stu-id="2662b-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="2662b-113">Nolietojuma priekšlikumu var filtrēt pēc līdzekļa, līdzekļa grupas vai cita kritērija, izmantojot opciju **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="2662b-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="2662b-114">Izmantojot veidlapu **Izveidot pamatlīdzekļu iegādes vai nolietojuma priekšlikumu**, varat izteikt priekšlikumu par nolietojumu partijām.</span><span class="sxs-lookup"><span data-stu-id="2662b-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="2662b-115">Šo iespēju ieteicams izmantot lielākiem priekšlikumiem, kas aizņem vairāk sistēmas resursu.</span><span class="sxs-lookup"><span data-stu-id="2662b-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="2662b-116">Ja atlasāt pakešu opciju, šajā laikā varat pabeigt citus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="2662b-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="2662b-117">Kad piedāvājat nolietojumu veikt šādi, nolietojums tiek aprēķināts pamatlīdzekļu vērtības modeļiem.</span><span class="sxs-lookup"><span data-stu-id="2662b-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="2662b-118">Atlasiet **Izveidot žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="2662b-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="2662b-119">Nolietojuma ierakstu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="2662b-119">Review depreciation entries</span></span>
1. <span data-ttu-id="2662b-120">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="2662b-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="2662b-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2662b-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2662b-122">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="2662b-122">Select **Lines**.</span></span>
4. <span data-ttu-id="2662b-123">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="2662b-123">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]