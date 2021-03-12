---
title: Kreditora rēķina reģistrēšana rēķinu žurnālā
description: Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18d8b74bd8783c23e548a3185414d1461bc1d869
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971832"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="3e6fc-103">Kreditora rēķina reģistrēšana rēķinu žurnālā</span><span class="sxs-lookup"><span data-stu-id="3e6fc-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e6fc-104">Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="3e6fc-105">Šī rēķina tipa piemēri ietver izdevumus par piegādēm vai pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="3e6fc-106">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="3e6fc-107">Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Darbvietas > Kreditora rēķina ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="3e6fc-108">Sadaļā **Darbību rūts** noklikšķiniet uz **Jauns rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="3e6fc-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-109">Click **New**.</span></span>
4. <span data-ttu-id="3e6fc-110">Laukā **Nosaukums** ievadiet žurnāla nosaukumu vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="3e6fc-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="3e6fc-112">**Darbību rūtī** noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="3e6fc-113">Laukā **Datums** ievadiet grāmatošanas datumu, kas atjauninās vienumu Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="3e6fc-114">Laukā **Konts** norādiet **Kreditora konts**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="3e6fc-115">Laukā **Rēķins** ievadiet rēķina numuru</span><span class="sxs-lookup"><span data-stu-id="3e6fc-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="3e6fc-116">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="3e6fc-117">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="3e6fc-118">Laukā **Korespondējošais konts** ievadiet konta numuru vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="3e6fc-119">**PVN grupa** pēc noklusējuma tiek ņemta no kreditora konta datiem.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="3e6fc-120">**Krājumu PVN grupa** pēc noklusējuma tiek ņemta no galvenā konta, kurš norādīts laukā **Korespondējošais konts**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="3e6fc-121">**Izpildes datums** tiek aprēķināts, ņemot vērā vienumu Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="3e6fc-122">Vērtība **Termiņatlaide** pēc noklusējuma tiek ņemta no datiem Kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="3e6fc-123">Ja esat iespējojis kreditoru rēķinu žurnāla darbplūsmu, noklikšķiniet uz **Darbplūsma > Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="3e6fc-124">Kad iesniegšana ir apstiprināta, datums tiks pārlikts uz nākamā brīvā perioda pirmo dienu, ja darījuma grāmatošanas datums iekrīt periodā, kas ir aizturēts vai slēgts grāmatošanai Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="3e6fc-125">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-125">Click **Post**.</span></span>
13. <span data-ttu-id="3e6fc-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-126">Close the page.</span></span>

