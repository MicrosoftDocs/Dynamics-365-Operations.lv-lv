---
title: Grāmatu skaits katrā žurnālā
description: Šī tēma apraksta attiecības starp žurnāliem un līdzekļu grāmatām, kad, izmantojot pakešuzdevumu, izveidojat pamatlīdzekļa iegādes vai nolietojuma priekšlikumu. Varat definēt maksimālo grāmatu skaitu, kas ir iekļautas katrai iegādei un nolietojumam.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650672"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="91e44-104">Grāmatu skaits katrā žurnālā</span><span class="sxs-lookup"><span data-stu-id="91e44-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91e44-105">Šī tēma apraksta attiecības starp žurnāliem un līdzekļu grāmatām, kad, izmantojot pakešuzdevumu, izveidojat pamatlīdzekļa iegādes vai nolietojuma priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="91e44-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="91e44-106">Varat definēt maksimālo grāmatu skaitu, kas ir iekļautas katrai iegādei un nolietojumam, izmantojot laukus sadaļā **Grāmatu skaits žurnālā**, cilnē **Vispārīgi**, kas atrodama lapā **Parametri** ( **Pamatlīdzekļi \> Iestatījumi \> Pamatlīdzekļu iestatījumi**).</span><span class="sxs-lookup"><span data-stu-id="91e44-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="91e44-107">Šie lauki ļauj jums sadalīt pamatlīdzekļu grāmatu skaitu uz iegādes žurnālu un nolietojuma žurnālu.</span><span class="sxs-lookup"><span data-stu-id="91e44-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="91e44-108">Iegādes priekšlikumam noklusētā vērtība ir vismaz 10 000 grāmatas.</span><span class="sxs-lookup"><span data-stu-id="91e44-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="91e44-109">Nolietojuma priekšlikumam noklusētā vērtība ir vismaz 2000 grāmatas.</span><span class="sxs-lookup"><span data-stu-id="91e44-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="91e44-110">Piemēram, ja ir 4000 pamatlīdzekļi un ar katru pamatlīdzekli ir saistītas divas grāmatas, viena grāmata tiks grāmatota pašreizējā slānī, un cita grāmata tiks grāmatota nodokļa slānī.</span><span class="sxs-lookup"><span data-stu-id="91e44-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="91e44-111">Ja iegūstat 4000 pamatlīdzekļus, izmantojot pakešapstrādi, pakešuzdevums, kas izveido vienu pamatlīdzekļu iegādes žurnālu, ietver 4000 līdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="91e44-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="91e44-112">Izveidotais žurnāls tiks izmantots, līdz pakešuzdevums būs pabeigts.</span><span class="sxs-lookup"><span data-stu-id="91e44-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="91e44-113">Atvasinātās grāmatas nav iekļautas maksimālajā grāmatu skaitā žurnālam.</span><span class="sxs-lookup"><span data-stu-id="91e44-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="91e44-114">Varat izmantot pakešapstrādi, lai izpildītu nolietojumu tai pašai iegūto līdzekļu kopai.</span><span class="sxs-lookup"><span data-stu-id="91e44-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="91e44-115">Piemēram, pakešuzdevums izveido divus nolietojuma žurnālus, katrs no tiem ietver 2000 līdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="91e44-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="91e44-116">Pirmajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 1 līdz 2000.</span><span class="sxs-lookup"><span data-stu-id="91e44-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="91e44-117">Otrajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 2001 līdz 4000.</span><span class="sxs-lookup"><span data-stu-id="91e44-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="91e44-118">Pakešapstrādes darbs izslēdz slēgtās grāmatas.</span><span class="sxs-lookup"><span data-stu-id="91e44-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="91e44-119">Piemēram, nolietojuma pakešuzdevumā ir slēgtas 10 no pirmajām 2000 grāmatām ir slēgtas.</span><span class="sxs-lookup"><span data-stu-id="91e44-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="91e44-120">Pirmajā gadījumā pirmajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 1 līdz 2011.</span><span class="sxs-lookup"><span data-stu-id="91e44-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="91e44-121">Otrajā žurnālā būs ietvertas grāmatas, kas ir saistītas ar pamatlīdzekļiem, kuri numurēti no 2012 līdz 4000.</span><span class="sxs-lookup"><span data-stu-id="91e44-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="91e44-122">Grāmatu skaita ierobežojums tiek pielietots, ja tajā pašā žurnālā neeksistē pamatlīdzekļu ID dublikāti.</span><span class="sxs-lookup"><span data-stu-id="91e44-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="91e44-123">Tomēr, ja pamatlīdzekļa ID ir tas pats, kas grāmatas ID, žurnāla grāmatu skaits var tikt pārsniegts, lai saglabātu pamatlīdzekļa ID tajā pašā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="91e44-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="91e44-124">Piemēram, ir 5001 pamatlīdzekļu ID, trīs grāmatas ir saistītas ar katru pamatlīdzekļa ID, un katra pamatlīdzekļu grāmata tiek grāmatota vienā grāmatošanas līmenī.</span><span class="sxs-lookup"><span data-stu-id="91e44-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="91e44-125">Nolietojums tiek palaists trīs mēnešus pēc kārtas bez summēšanas.</span><span class="sxs-lookup"><span data-stu-id="91e44-125">You run depreciation for three consecutive months, without summarization.</span></span> <span data-ttu-id="91e44-126">Nolietojuma žurnāls tiks izveidots, izmantojot pakešuzdevumu, un sistēma izveidos septiņus žurnālus, kuriem ir 667 pamatlīdzekļu ID un trīs grāmatas katram pamatlīdzekļa ID.</span><span class="sxs-lookup"><span data-stu-id="91e44-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="91e44-127">Rezultāts būs 2001 grāmata.</span><span class="sxs-lookup"><span data-stu-id="91e44-127">The result will be 2,001 books.</span></span> <span data-ttu-id="91e44-128">Tāpēc trijos mēnešos būs 6003 žurnāla rindas, lai tajā pašā žurnālā uzturētu tos pašus pamatlīdzekļu ID.</span><span class="sxs-lookup"><span data-stu-id="91e44-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="91e44-129">Sistēmā tiks izveidots arī viens žurnāls, kurā ir 332 pamatlīdzekļu ID un trīs grāmatas katram pamatlīdzekļa ID.</span><span class="sxs-lookup"><span data-stu-id="91e44-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="91e44-130">Trijos mēnešos būs 2988 rindas.</span><span class="sxs-lookup"><span data-stu-id="91e44-130">In three months, there will be 2,988 lines.</span></span>
