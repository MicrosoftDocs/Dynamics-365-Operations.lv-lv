---
title: Brīva teksta rēķina veidnes piešķiršana debitoram
description: Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19742c53406cd1c616e8be1172b93157437132e8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445485"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="a7da2-103">Brīva teksta rēķina veidnes piešķiršana debitoram</span><span class="sxs-lookup"><span data-stu-id="a7da2-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7da2-104">Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni.</span><span class="sxs-lookup"><span data-stu-id="a7da2-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="a7da2-105">Šajā uzdevumā izmantots demonstrācijas uzņēmums USMF, un šis uzdevums ir paredzēts lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.</span><span class="sxs-lookup"><span data-stu-id="a7da2-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="a7da2-106">**Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="a7da2-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a7da2-107">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a7da2-108">**Darbību rūtī** noklikšķiniet uz **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a7da2-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="a7da2-109">Klikšķiniet uz **Periodiskie rēķini**.</span><span class="sxs-lookup"><span data-stu-id="a7da2-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="a7da2-110">Izmantojiet šo lapu, lai piešķirtu brīva teksta rēķinu veidnes debitoriem un norādītu, cik bieži rēķini tiks nosūtīti debitoram.</span><span class="sxs-lookup"><span data-stu-id="a7da2-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="a7da2-111">Lai klientam piešķirtu jaunu veidni, noklikšķiniet uz **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="a7da2-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="a7da2-112">Laukā **Veidne** atlasiet brīva teksta rēķina veidni, ko vēlaties piešķirt klientam.</span><span class="sxs-lookup"><span data-stu-id="a7da2-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="a7da2-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a7da2-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="a7da2-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a7da2-115">Laukā **Rēķinu izrakstīšanas sākuma datums** ievadiet datumu, kad tiks izveidots pirmais rēķins.</span><span class="sxs-lookup"><span data-stu-id="a7da2-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="a7da2-116">Sadaļā **Periodiskuma beigas** ievadiet perioda beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="a7da2-117">Atlasiet kādu no šīm vērtībām: Bez beigu datuma — rēķini tiek ģenerēts uz nenoteiktu laiku, līdz veidne tiek noņemta no debitora konta.</span><span class="sxs-lookup"><span data-stu-id="a7da2-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="a7da2-118">Norēķinu beigu datums — atlasiet šo opciju un ievadiet pēdējo datumu, kad var ģenerēt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="a7da2-119">Laukā **Maksimālā uzkrātā summa** ievadiet maksimālo uzkrāto summu, pēc kuras beigsies rēķinu veidošana.</span><span class="sxs-lookup"><span data-stu-id="a7da2-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="a7da2-120">Ievadiet maksimālo kopējo summu, kuru atļauts sasniegt, izmantojot atlasīto veidni.</span><span class="sxs-lookup"><span data-stu-id="a7da2-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="a7da2-121">Piemēram, ja ievadāt 1000,00 un ģenerējat ikmēneša rēķinus, katru 100,00 vērtībā, rēķinu ģenerēšana tiks pārtraukta pēc desmitā rēķina izveides.</span><span class="sxs-lookup"><span data-stu-id="a7da2-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="a7da2-122">Sadaļā **Veidot periodiskus rēķinus, izmantojot noklusējuma vērtības no** izvēlieties brīva teksta ievades veidni vai klienta kontu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="a7da2-123">Atlasiet, vai izmantot brīvā teksta rēķina veidni vai debitora kontu, lai noteiktu noklusējuma vērtības valodai, grāmatošanas profilam, PVN grupai, krājumu PVN grupai, saraksta kodam, piegādes valstij/reģionam, valūtai, maksāšanas termiņiem, maksāšanas metodei, maksājuma specifikācijai, maksājumu grafikam, termiņatlaidei, finanšu dimensijām un žiro naudas pārskaitīšanas sarakstam, kad tiek izveidoti rēķini.</span><span class="sxs-lookup"><span data-stu-id="a7da2-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="a7da2-124">Laukā **Atkārtošanās shēma** atlasiet atkārtošanās shēmu.</span><span class="sxs-lookup"><span data-stu-id="a7da2-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="a7da2-125">Dienas — atlasiet šo opciju un ievadiet dienu skaitu laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="a7da2-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="a7da2-126">Piemēram, ja ievadāt 15, tad rēķins šim debitoram tiks ģenerēts ik pēc 15 dienām.</span><span class="sxs-lookup"><span data-stu-id="a7da2-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="a7da2-127">Nedēļas — atlasiet šo opciju un ievadiet nedēļu skaitu laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="a7da2-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="a7da2-128">Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc divām nedēļām.</span><span class="sxs-lookup"><span data-stu-id="a7da2-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="a7da2-129">Mēneša — atlasiet šo opciju un ievadiet mēnešu skaitu laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="a7da2-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="a7da2-130">Piemēram, ja ievadāt 6, tad rēķins šim debitoram tiks ģenerēts ik pēc sešiem mēnešiem.</span><span class="sxs-lookup"><span data-stu-id="a7da2-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="a7da2-131">Gada — atlasiet šo opciju un ievadiet gadu skaitu laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="a7da2-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="a7da2-132">Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc diviem gadiem.</span><span class="sxs-lookup"><span data-stu-id="a7da2-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="a7da2-133">Laukā **Par** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="a7da2-133">In the **Per** field, enter a number.</span></span>

