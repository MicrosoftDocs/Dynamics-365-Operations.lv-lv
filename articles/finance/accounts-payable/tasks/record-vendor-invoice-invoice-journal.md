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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178905"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="31821-103">Kreditora rēķina reģistrēšana rēķinu žurnālā</span><span class="sxs-lookup"><span data-stu-id="31821-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31821-104">Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="31821-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="31821-105">Šī rēķina tipa piemēri ietver izdevumus par piegādēm vai pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="31821-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="31821-106">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="31821-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="31821-107">Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Darbvietas > Kreditora rēķina ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="31821-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="31821-108">Sadaļā **Darbību rūts** noklikšķiniet uz **Jauns rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="31821-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="31821-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="31821-109">Click **New**.</span></span>
4. <span data-ttu-id="31821-110">Laukā **Nosaukums** ievadiet žurnāla nosaukumu vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31821-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="31821-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="31821-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="31821-112">**Darbību rūtī** noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="31821-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="31821-113">Laukā **Datums** ievadiet grāmatošanas datumu, kas atjauninās vienumu Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="31821-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="31821-114">Laukā **Konts** norādiet **Kreditora konts**.</span><span class="sxs-lookup"><span data-stu-id="31821-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="31821-115">Laukā **Rēķins** ievadiet rēķina numuru</span><span class="sxs-lookup"><span data-stu-id="31821-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="31821-116">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="31821-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="31821-117">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="31821-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="31821-118">Laukā **Korespondējošais konts** ievadiet konta numuru vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="31821-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="31821-119">**PVN grupa** pēc noklusējuma tiek ņemta no kreditora konta datiem.</span><span class="sxs-lookup"><span data-stu-id="31821-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="31821-120">**Krājumu PVN grupa** pēc noklusējuma tiek ņemta no galvenā konta, kurš norādīts laukā **Korespondējošais konts**.</span><span class="sxs-lookup"><span data-stu-id="31821-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="31821-121">**Izpildes datums** tiek aprēķināts, ņemot vērā vienumu Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="31821-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="31821-122">Vērtība **Termiņatlaide** pēc noklusējuma tiek ņemta no datiem Kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="31821-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="31821-123">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="31821-123">Click **Post**.</span></span>
13. <span data-ttu-id="31821-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="31821-124">Close the page.</span></span>

