--- 
title: "Izveidot patapinājuma priekšmetus"
description: "Patapinājuma priekšmeti ir ieraksti, kas palīdz izsekot fiziskus vienumus, piemēram, tālruņus vai datorus, kurus jūsu uzņēmums patapina darbiniekiem."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="f3364-103">Izveidot patapinājuma priekšmetus</span><span class="sxs-lookup"><span data-stu-id="f3364-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3364-104">Patapinājuma priekšmeti ir ieraksti, kas palīdz izsekot fiziskus vienumus, piemēram, tālruņus vai datorus, kurus jūsu uzņēmums patapina darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="f3364-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="f3364-105">Katram fiziskam priekšmetam jābūt atbilstošam patapinājuma priekšmetam.</span><span class="sxs-lookup"><span data-stu-id="f3364-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="f3364-106">Katram patapinājuma priekšmeta ierakstam ir jāapraksta, kas tiek patapināts, kurš ir atbildīgs par patapinājumu un cik dienas priekšmets var būt patapināts.</span><span class="sxs-lookup"><span data-stu-id="f3364-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="f3364-107">Vienlaikus varat izveidot vairākus patapinājuma priekšmetus, piemēram, atslēgas, piekļuves kartes vai formastērpus.</span><span class="sxs-lookup"><span data-stu-id="f3364-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="f3364-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="f3364-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="f3364-109">Patapinājumu tipu izveide</span><span class="sxs-lookup"><span data-stu-id="f3364-109">Create Loan types</span></span>
1. <span data-ttu-id="f3364-110">Dodieties uz Personāla vadība > Darbinieki > Patapinājuma priekšmeti > Patapinājumu tipi.</span><span class="sxs-lookup"><span data-stu-id="f3364-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="f3364-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f3364-111">Click New.</span></span>
3. <span data-ttu-id="f3364-112">Ierakstiet vērtību laukā Patapinājuma tips.</span><span class="sxs-lookup"><span data-stu-id="f3364-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="f3364-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f3364-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3364-114">Ievadiet dienu skaitu, par kādu šī tipa patapinājumiem atļauts kavēt priekšmetu atpakaļatgriešanu.</span><span class="sxs-lookup"><span data-stu-id="f3364-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="f3364-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f3364-115">Click Save.</span></span>
7. <span data-ttu-id="f3364-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3364-116">Close the page.</span></span>
8. <span data-ttu-id="f3364-117">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="f3364-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="f3364-118">Izveidot patapinājuma priekšmetus</span><span class="sxs-lookup"><span data-stu-id="f3364-118">Create Loan items</span></span>
1. <span data-ttu-id="f3364-119">Dodieties uz Personāla vadība > Darbinieki > Patapinājuma priekšmeti > Patapinājuma priekšmeti.</span><span class="sxs-lookup"><span data-stu-id="f3364-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="f3364-120">Noklikšķiniet uz Izveidot patapinājuma priekšmetus.</span><span class="sxs-lookup"><span data-stu-id="f3364-120">Click Create loan items.</span></span>
3. <span data-ttu-id="f3364-121">Laukā Daudz.</span><span class="sxs-lookup"><span data-stu-id="f3364-121">In the Qty.</span></span> <span data-ttu-id="f3364-122">ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f3364-122">field, enter a number.</span></span>
4. <span data-ttu-id="f3364-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f3364-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3364-124">Laukā Patapinājuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f3364-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f3364-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f3364-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f3364-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f3364-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f3364-127">Ievadiet priekšmeta patapinājuma iespējamo dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="f3364-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="f3364-128">Noklusēto vērtību lapas Patapinātais aprīkojums laukā Plānotā atgriešana aprēķina kā pašreizējo datumu, kuram tiek pieskaitīts šis skaitlis.</span><span class="sxs-lookup"><span data-stu-id="f3364-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="f3364-129">Laukā Atbildīgais darbinieks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f3364-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f3364-130">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="f3364-130">Click Select.</span></span>
11. <span data-ttu-id="f3364-131">Ievadiet skaitli laukā Sākuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="f3364-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="f3364-132">Ievadiet skaitli laukā Intervāls.</span><span class="sxs-lookup"><span data-stu-id="f3364-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="f3364-133">Ierakstiet vērtību laukā Formāts.</span><span class="sxs-lookup"><span data-stu-id="f3364-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="f3364-134">Piemēram, ja patapinājuma priekšmeta sākuma numurs ir 10, laukā Formāts ievadiet divus skaitļa simbolus.</span><span class="sxs-lookup"><span data-stu-id="f3364-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="f3364-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3364-135">Click OK.</span></span>
15. <span data-ttu-id="f3364-136">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="f3364-136">Refresh the page.</span></span>


