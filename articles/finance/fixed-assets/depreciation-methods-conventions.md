---
title: Nolietojuma metodes un konvencijas
description: Šajā rakstā ir sniegts apskats par nolietojuma aprēķināšanas metodēm un nolietojuma metodēm, kas tiek atbalstītas programmā Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af1c1a222981a0bcf9d7341cde5b83dd720da802
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994969"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="ae316-103">Nolietojuma metodes un konvencijas</span><span class="sxs-lookup"><span data-stu-id="ae316-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae316-104">Šajā rakstā ir sniegts apskats par atbalstītajām nolietojuma aprēķināšanas metodēm un nolietojuma metodēm.</span><span class="sxs-lookup"><span data-stu-id="ae316-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="ae316-105">Var atlasīt dažādas nolietojuma metodes un konvencijas.</span><span class="sxs-lookup"><span data-stu-id="ae316-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="ae316-106">Šo metožu nolūks ir sadalīt pamatlīdzekļa nolietojuma vērtību pa finanšu periodiem.</span><span class="sxs-lookup"><span data-stu-id="ae316-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="ae316-107">Pamatlīdzekļa nolietojuma vērtība ir iegādes cenas un lūžņu vērtības (ja tāda ir) starpība.</span><span class="sxs-lookup"><span data-stu-id="ae316-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="ae316-108">Ja izmantojat nolietojuma konvencijas un modificējat pamatlīdzekļa pēdējo nolietojuma aprēķināšanas datumu, tādējādi izraisot dažu nolietojuma aprēķinu izlaišanu, nolietojums pēdējā gadā var būt lielāks vai mazāks par paredzēto.</span><span class="sxs-lookup"><span data-stu-id="ae316-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="ae316-109">Nolietojums tiek koriģēts ar nolietojuma periodu skaitu, ko ietekmē pēdējā nolietojuma aprēķināšanas datuma modifikācija.</span><span class="sxs-lookup"><span data-stu-id="ae316-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="ae316-110">Piemēram, ja trīs gadus lietojat pusgada nolietojuma konvenciju, nolietošanās parasti notiek 3 1/2 gados.</span><span class="sxs-lookup"><span data-stu-id="ae316-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="ae316-111">Ja trīsarpus gadu laikā maināt pēdējo nolietojuma aprēķināšanas datumu, pēdējais nolietojums iziet ārpus ietekmēto periodu skaita.</span><span class="sxs-lookup"><span data-stu-id="ae316-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="ae316-112">Ja maināt datumu par trīs mēnešiem, pēdējam gadam tiek aprēķināts deviņu mēnešu nolietojums, lai gan parasti tam vajadzētu būt sešu mēnešu nolietojumam.</span><span class="sxs-lookup"><span data-stu-id="ae316-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="ae316-113">Varat atlasīt kādu no tālāk norādītajām nolietojuma konvencijām.</span><span class="sxs-lookup"><span data-stu-id="ae316-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="ae316-114">Pusgads</span><span class="sxs-lookup"><span data-stu-id="ae316-114">Half year</span></span>
-   <span data-ttu-id="ae316-115">Pilns mēnesis</span><span class="sxs-lookup"><span data-stu-id="ae316-115">Full month</span></span>
-   <span data-ttu-id="ae316-116">Puse ceturkšņa</span><span class="sxs-lookup"><span data-stu-id="ae316-116">Mid quarter</span></span>
-   <span data-ttu-id="ae316-117">Puse mēneša (mēneša 1. datums)</span><span class="sxs-lookup"><span data-stu-id="ae316-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="ae316-118">Puse mēneša (mēneša 15. datums)</span><span class="sxs-lookup"><span data-stu-id="ae316-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="ae316-119">Pusgads (gada sākums)</span><span class="sxs-lookup"><span data-stu-id="ae316-119">Half year (start of year)</span></span>
-   <span data-ttu-id="ae316-120">Puse gada (nākamais gads)</span><span class="sxs-lookup"><span data-stu-id="ae316-120">Half year (next year)</span></span>

<span data-ttu-id="ae316-121">Varat atlasīt kādu no tālāk norādītajām nolietojuma metodēm.</span><span class="sxs-lookup"><span data-stu-id="ae316-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="ae316-122">Lineārais lietošanas ilgums</span><span class="sxs-lookup"><span data-stu-id="ae316-122">Straight line service life</span></span>
-   <span data-ttu-id="ae316-123">Atlik. samazinošā</span><span class="sxs-lookup"><span data-stu-id="ae316-123">Reducing balance</span></span>
-   <span data-ttu-id="ae316-124">Manuālā</span><span class="sxs-lookup"><span data-stu-id="ae316-124">Manual</span></span>
-   <span data-ttu-id="ae316-125">Koeficients</span><span class="sxs-lookup"><span data-stu-id="ae316-125">Factor</span></span>
-   <span data-ttu-id="ae316-126">Patēriņš</span><span class="sxs-lookup"><span data-stu-id="ae316-126">Consumption</span></span>
-   <span data-ttu-id="ae316-127">Lineārais atlikušais mūžs</span><span class="sxs-lookup"><span data-stu-id="ae316-127">Straight line life remaining</span></span>
-   <span data-ttu-id="ae316-128">200% atlikumu bilance</span><span class="sxs-lookup"><span data-stu-id="ae316-128">200% reducing balance</span></span>
-   <span data-ttu-id="ae316-129">175% atlikumu bilance</span><span class="sxs-lookup"><span data-stu-id="ae316-129">175% reducing balance</span></span>
-   <span data-ttu-id="ae316-130">150% atlikumu bilance</span><span class="sxs-lookup"><span data-stu-id="ae316-130">150% reducing balance</span></span>
-   <span data-ttu-id="ae316-131">125% atlikumu bilance</span><span class="sxs-lookup"><span data-stu-id="ae316-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="ae316-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ae316-132">Additional resources</span></span>
--------

[<span data-ttu-id="ae316-133">Pamatlīdzekļu nolietojums</span><span class="sxs-lookup"><span data-stu-id="ae316-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="ae316-134">Lietošanas ilguma lineārā aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="ae316-135">Degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="ae316-136">Pamatlīdzekļu manuālais nolietojums</span><span class="sxs-lookup"><span data-stu-id="ae316-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="ae316-137">Koeficienta nolietojums</span><span class="sxs-lookup"><span data-stu-id="ae316-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="ae316-138">Patēriņa nolietojuma aprēķins</span><span class="sxs-lookup"><span data-stu-id="ae316-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="ae316-139">Atlikušā lietošanas ilguma lineārā aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="ae316-140">125 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="ae316-141">150 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="ae316-142">175 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="ae316-143">200 procentu degresīvā nolietojuma aprēķināšanas metode</span><span class="sxs-lookup"><span data-stu-id="ae316-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



