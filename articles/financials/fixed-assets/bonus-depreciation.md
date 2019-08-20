---
title: Papildnolietojums
description: Šajā rakstā ir sniegts pārskats par papildnolietojuma funkcionalitāti.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840677"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="1af3f-103">Papildnolietojums</span><span class="sxs-lookup"><span data-stu-id="1af3f-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1af3f-104">Šajā rakstā ir sniegts pārskats par papildnolietojuma funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="1af3f-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="1af3f-105">Papildnolietojumam varat izmantot papildnolietojuma summas pirmā gada laikā, kad līdzeklis tiek ievadīts ekspluatācijā un nolietots.</span><span class="sxs-lookup"><span data-stu-id="1af3f-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="1af3f-106">Papildnolietojums ir jāizmanto pirms pārējiem nolietojuma aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="1af3f-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="1af3f-107">Tādēļ papildnolietojumu ieteicams izmantot ar grāmatām, kur ir atspējota funkcionalitāte Grāmatot virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="1af3f-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="1af3f-108">Varat izmantot opciju **Dzēst virsgrāmatā negrāmatotās transakcijas**, lai dzēstu vēsturiskās transakcijas grāmatām, kuras neveic grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="1af3f-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="1af3f-109">Pēc tam papildnolietojumu varat vēlāk uzkrāt attiecīgā līdzekļa kalpošanas cikla gaitā, dzēšot iepriekš grāmatotās nolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="1af3f-110">Papildnolietojumu var aprēķināt, izmantojot priekšlikuma procesu, vai varat izveidot manuālas papildnolietojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="1af3f-111">Papildnolietojuma transakcijas nevar izveidot, ja šī līdzekļa grāmatai pastāv nolietojuma transakcijas vai nolietojuma pielāgojuma transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="1af3f-112">Kad izmantojot priekšlikuma procesu, lai aprēķinātu papildnolietojumu, bāzes aprēķinā tiek iekļautas visas esošās papildtransakcijas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="1af3f-113">Aprēķinā tiek iekļauti visi iepriekšējie papildnolietojumi, ko šim līdzeklim ievadījāt manuāli.</span><span class="sxs-lookup"><span data-stu-id="1af3f-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="1af3f-114">Ja līdzeklim tiks ņemti vairāki papildnolietojumi, tiek ņemta vērā prioritāte.</span><span class="sxs-lookup"><span data-stu-id="1af3f-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="1af3f-115">Katrs papildinājums samazina pamatlīdzekļa bāzi nākamajam papildinājumam.</span><span class="sxs-lookup"><span data-stu-id="1af3f-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="1af3f-116">Lūžņu vērtība netiek ņemta vērā kā līdzekļu pamats papildnolietojuma aprēķiniem, un nolietojuma aprēķināšanas metode neattiecas uz papildnolietojumu.</span><span class="sxs-lookup"><span data-stu-id="1af3f-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="1af3f-117">Pašlaik Amerikas Savienotajās Valstīs noteikts īpašums atbilst 179. sadaļas īpašumam.</span><span class="sxs-lookup"><span data-stu-id="1af3f-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="1af3f-118">Izmantojot 179. sadaļas ieturējumu, varat atgūt visu maksu vai daļu no maksas par noteiktu īpašumu, līdz zināmam ierobežojumam.</span><span class="sxs-lookup"><span data-stu-id="1af3f-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="1af3f-119">Varat atgūt šo maksu, atskaitot to tajā gadā, kad šo īpašumu ievadījāt ekspluatācijā.</span><span class="sxs-lookup"><span data-stu-id="1af3f-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="1af3f-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="1af3f-120">Example</span></span>
<span data-ttu-id="1af3f-121">Ar līdzekļa nolietojuma grāmatu ir saistīti tālāk uzskaitītie papildnolietojumi.</span><span class="sxs-lookup"><span data-stu-id="1af3f-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="1af3f-122">**179. sadaļa:** 1000,00, prioritāte 1</span><span class="sxs-lookup"><span data-stu-id="1af3f-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="1af3f-123">**Brīvā zona:** 30 procenti, prioritāte 2</span><span class="sxs-lookup"><span data-stu-id="1af3f-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="1af3f-124">Līdzekļa iegādes izmaksas ir 5000,00.</span><span class="sxs-lookup"><span data-stu-id="1af3f-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="1af3f-125">Kad tiek aprēķināts papildnolietojums, 179. sadaļas nolietojumam pirmā papildnolietojuma summa ir 1000,00.</span><span class="sxs-lookup"><span data-stu-id="1af3f-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="1af3f-126">Nākamā papildnolietojuma summa — brīvās zonas nolietojumam — tiek aprēķināta tālāk parādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="1af3f-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="1af3f-127">Iegādes izmaksas — 1000 (179. sadaļas nolietojums) x 30 procenti = 1200</span><span class="sxs-lookup"><span data-stu-id="1af3f-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="1af3f-128">Ja papildnolietojuma summa ir lielāka par atlikušajām iegādes izmaksām, tad papildnolietojuma summa ir vai nu papildnolietojuma aprēķina rezultāts, vai atlikušās iegādes izmaksas atkarībā no tā, kura summa ir mazāka.</span><span class="sxs-lookup"><span data-stu-id="1af3f-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="1af3f-129">Ja atlikušās iegādes izmaksas ir 0 (nulle) vai mazāk, tad papildnolietojuma transakcijas netiek ģenerētas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="1af3f-130">Ja papildnolietojums tiek aprēķināts, izmantojot priekšlikuma procesu, tiek izveidota papildnolietojuma transakcija visiem piemērojamajiem papildnolietojuma ierakstiem, kas ir saistīti ar līdzekļa grāmatu.</span><span class="sxs-lookup"><span data-stu-id="1af3f-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="1af3f-131">Var izveidot neierobežotu papildnolietojuma ierakstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="1af3f-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="1af3f-132">Pēc šo ierakstu piešķiršanas līdzekļu grupas grāmatai tie tiek lietoti attiecīgajai līdzekļu grāmatai.</span><span class="sxs-lookup"><span data-stu-id="1af3f-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="1af3f-133">Papildnolietojums tiek ievadīts kā procenti vai kā fiksēta summa.</span><span class="sxs-lookup"><span data-stu-id="1af3f-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="1af3f-134">Kad grāmatojot nolietojuma priekšlikumus, papildnolietojuma transakcijas šajā grāmatā tiek grāmatotas kā no nolietojuma transakcijām atsevišķas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1af3f-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



