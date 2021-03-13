---
title: Izveidot patapinājuma priekšmetus
description: Patapinājuma priekšmeti ir ieraksti, kas palīdz izsekot fiziskus vienumus, piemēram, tālruņus vai datorus, kurus jūsu uzņēmums patapina darbiniekiem.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7da578c57be57b55e9175600461549416faa1298
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130353"
---
# <a name="create-loan-items"></a><span data-ttu-id="89256-103">Izveidot patapinājuma priekšmetus</span><span class="sxs-lookup"><span data-stu-id="89256-103">Create loan items</span></span>



<span data-ttu-id="89256-104">Patapinājuma priekšmeti ir ieraksti, kas palīdz izsekot fiziskus vienumus, piemēram, tālruņus vai datorus, kurus jūsu uzņēmums patapina darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="89256-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="89256-105">Katram fiziskam priekšmetam jābūt atbilstošam patapinājuma priekšmetam.</span><span class="sxs-lookup"><span data-stu-id="89256-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="89256-106">Katram patapinājuma priekšmeta ierakstam ir jāapraksta, kas tiek patapināts, kurš ir atbildīgs par patapinājumu un cik dienas priekšmets var būt patapināts.</span><span class="sxs-lookup"><span data-stu-id="89256-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="89256-107">Vienlaikus varat izveidot vairākus patapinājuma priekšmetus, piemēram, atslēgas, piekļuves kartes vai formastērpus.</span><span class="sxs-lookup"><span data-stu-id="89256-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="89256-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="89256-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="89256-109">Patapinājumu tipu izveide</span><span class="sxs-lookup"><span data-stu-id="89256-109">Create Loan types</span></span>
1. <span data-ttu-id="89256-110">Dodieties uz Personāla vadība > Darbinieki > Patapinājuma priekšmeti > Patapinājumu tipi.</span><span class="sxs-lookup"><span data-stu-id="89256-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="89256-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="89256-111">Click New.</span></span>
3. <span data-ttu-id="89256-112">Ierakstiet vērtību laukā Patapinājuma tips.</span><span class="sxs-lookup"><span data-stu-id="89256-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="89256-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="89256-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="89256-114">Ievadiet dienu skaitu, par kādu šī tipa patapinājumiem atļauts kavēt priekšmetu atpakaļatgriešanu.</span><span class="sxs-lookup"><span data-stu-id="89256-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="89256-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="89256-115">Click Save.</span></span>
7. <span data-ttu-id="89256-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="89256-116">Close the page.</span></span>
8. <span data-ttu-id="89256-117">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="89256-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="89256-118">Izveidot patapinājuma priekšmetus</span><span class="sxs-lookup"><span data-stu-id="89256-118">Create Loan items</span></span>
1. <span data-ttu-id="89256-119">Dodieties uz Personāla vadība > Darbinieki > Patapinājuma priekšmeti > Patapinājuma priekšmeti.</span><span class="sxs-lookup"><span data-stu-id="89256-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="89256-120">Noklikšķiniet uz Izveidot patapinājuma priekšmetus.</span><span class="sxs-lookup"><span data-stu-id="89256-120">Click Create loan items.</span></span>
3. <span data-ttu-id="89256-121">Laukā Daudz. ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="89256-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="89256-122">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="89256-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="89256-123">Laukā Patapinājuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89256-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="89256-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="89256-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="89256-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89256-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="89256-126">Ievadiet priekšmeta patapinājuma iespējamo dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="89256-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="89256-127">Noklusēto vērtību lapas Patapinātais aprīkojums laukā Plānotā atgriešana aprēķina kā pašreizējo datumu, kuram tiek pieskaitīts šis skaitlis.</span><span class="sxs-lookup"><span data-stu-id="89256-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="89256-128">Laukā Atbildīgais darbinieks noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89256-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="89256-129">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="89256-129">Click Select.</span></span>
11. <span data-ttu-id="89256-130">Ievadiet skaitli laukā Sākuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="89256-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="89256-131">Ievadiet skaitli laukā Intervāls.</span><span class="sxs-lookup"><span data-stu-id="89256-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="89256-132">Ierakstiet vērtību laukā Formāts.</span><span class="sxs-lookup"><span data-stu-id="89256-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="89256-133">Piemēram, ja patapinājuma priekšmeta sākuma numurs ir 10, laukā Formāts ievadiet divus skaitļa simbolus.</span><span class="sxs-lookup"><span data-stu-id="89256-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="89256-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="89256-134">Click OK.</span></span>
15. <span data-ttu-id="89256-135">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="89256-135">Refresh the page.</span></span>

