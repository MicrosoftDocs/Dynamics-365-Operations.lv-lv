---
title: PP punktu skaitīšanas metodes izveide
description: Šajā procedūrā ir parādīts, kā izveidot punktu skaitīšanas metodi.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbbc941b810cd8e5db5ba15a23dc6bd72a29506
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838074"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="677e3-103">PP punktu skaitīšanas metodes izveide</span><span class="sxs-lookup"><span data-stu-id="677e3-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="677e3-104">Šajā procedūrā ir parādīts, kā izveidot punktu skaitīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="677e3-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="677e3-105">Punktu skaitīšanas metode ir kritēriju kopa, ko var izmantot, lai salīdzinātu piedāvājumus, kuri ir iesūtīti kā atbilde uz piedāvājuma pieprasījumu (IP).</span><span class="sxs-lookup"><span data-stu-id="677e3-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="677e3-106">Piemēram, jūs, iespējams, vēlaties novērt kādu kreditoru pēc tā iepriekšējām darbībām, vai vēlaties novērtēt, vai uzņēmums ir videi draudzīgs, vai ar to ir izdevīgi sadarboties, vai arī piedāvājumus vēlaties salīdzināt, pamatojoties uz cenu.</span><span class="sxs-lookup"><span data-stu-id="677e3-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="677e3-107">Punktu skaitīšanas metodi var saistīt ar lūguma tipu kā noklusējuma punktu skaitīšanas metodi attiecīgā tipa IP.</span><span class="sxs-lookup"><span data-stu-id="677e3-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="677e3-108">Šos uzdevumus parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="677e3-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="677e3-109">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="677e3-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="677e3-110">Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Piedāvājuma pieprasījums > Punktu skaitīšanas metode.</span><span class="sxs-lookup"><span data-stu-id="677e3-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="677e3-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="677e3-111">Click New.</span></span>
3. <span data-ttu-id="677e3-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="677e3-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="677e3-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="677e3-114">Click Save.</span></span>
6. <span data-ttu-id="677e3-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="677e3-115">Click New.</span></span>
7. <span data-ttu-id="677e3-116">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="677e3-117">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="677e3-118">Šis apraksts tiek rādīts kopā ar punktu skaitīšanas metodes nosaukumu, kad IP tiek atlasīta punktu skaitīšanas metode.</span><span class="sxs-lookup"><span data-stu-id="677e3-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="677e3-119">Ievadiet kādu skaitli laukā Diapazons no.</span><span class="sxs-lookup"><span data-stu-id="677e3-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="677e3-120">Diapazons ierobežo datus, ko sagādes speciālists var ievadīt kā punktu skaitu.</span><span class="sxs-lookup"><span data-stu-id="677e3-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="677e3-121">Ja kādam IP ir vairāki punktu skaitīšanas kritēriji, tad ievadītie punkti tiek savstarpēji saskaitīti un šī summa kļūst pieejama piedāvājumu salīdzināšanai.</span><span class="sxs-lookup"><span data-stu-id="677e3-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="677e3-122">Ievadiet kādu skaitli laukā Diapazons līdz.</span><span class="sxs-lookup"><span data-stu-id="677e3-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="677e3-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="677e3-123">Click New.</span></span>
12. <span data-ttu-id="677e3-124">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="677e3-125">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="677e3-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="677e3-126">Ievadiet kādu skaitli laukā Diapazons no.</span><span class="sxs-lookup"><span data-stu-id="677e3-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="677e3-127">Ievadiet kādu skaitli laukā Diapazons līdz.</span><span class="sxs-lookup"><span data-stu-id="677e3-127">In the Range to field, enter a number.</span></span>

