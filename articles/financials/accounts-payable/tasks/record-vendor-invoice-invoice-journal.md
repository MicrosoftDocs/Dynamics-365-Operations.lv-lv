--- 
title: "Kreditora rēķina reģistrēšana rēķinu žurnālā"
description: "Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 26515140b020d824f99441b9f1ee560a44e28f8f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="73961-103">Kreditora rēķina reģistrēšana rēķinu žurnālā</span><span class="sxs-lookup"><span data-stu-id="73961-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73961-104">Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="73961-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="73961-105">Šī rēķina tipa piemēri ietver izdevumus par piegādēm vai pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="73961-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="73961-106">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="73961-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="73961-107">Pārejiet uz sadaļu Kreditori > Darbvietas > Kreditora rēķina ieraksts.</span><span class="sxs-lookup"><span data-stu-id="73961-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="73961-108">Noklikšķiniet uz Jauns rēķinu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="73961-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="73961-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="73961-109">Click New.</span></span>
4. <span data-ttu-id="73961-110">Laukā Nosaukums ievadiet žurnāla nosaukumu vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="73961-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="73961-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="73961-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="73961-112">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="73961-112">Click Lines.</span></span>
    * <span data-ttu-id="73961-113">Laukā Datums ievadiet grāmatošanas datumu, kas atjauninās vienumu Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="73961-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="73961-114">Laukā Konts norādiet Kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="73961-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="73961-115">Laukā Rēķins ievadiet rēķina numuru.</span><span class="sxs-lookup"><span data-stu-id="73961-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="73961-116">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="73961-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="73961-117">Laukā Kredīts ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="73961-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="73961-118">Laukā Korespondējošais konts ievadiet konta numuru vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="73961-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="73961-119">PVN grupa pēc noklusējuma tiek ņemta no kreditora konta datiem.</span><span class="sxs-lookup"><span data-stu-id="73961-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="73961-120">Krājumu PVN grupa pēc noklusējuma tiek ņemta no galvenā konta, kurš norādīts laukā Korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="73961-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="73961-121">Izpildes datums tiek aprēķināts, ņemot vērā vienumu Apmaksas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="73961-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="73961-122">Vērtība Termiņatlaide pēc noklusējuma tiek ņemta no datiem Kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="73961-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="73961-123">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="73961-123">Click Post.</span></span>
13. <span data-ttu-id="73961-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="73961-124">Close the page.</span></span>


