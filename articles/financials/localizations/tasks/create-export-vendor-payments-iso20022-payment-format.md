--- 
title: "Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022"
description: "Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="f3de0-103">Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022</span><span class="sxs-lookup"><span data-stu-id="f3de0-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3de0-104">Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru.</span><span class="sxs-lookup"><span data-stu-id="f3de0-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="f3de0-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="f3de0-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="f3de0-106">Šī ir piektā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="f3de0-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f3de0-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="f3de0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="f3de0-108">Maksājuma rindu izveide</span><span class="sxs-lookup"><span data-stu-id="f3de0-108">Create payment lines</span></span>
1. <span data-ttu-id="f3de0-109">Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="f3de0-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f3de0-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f3de0-110">Click New.</span></span>
3. <span data-ttu-id="f3de0-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f3de0-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f3de0-112">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f3de0-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="f3de0-113">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="f3de0-113">Click Lines.</span></span>
6. <span data-ttu-id="f3de0-114">Noklikšķiniet uz Maksājuma priekšlikums.</span><span class="sxs-lookup"><span data-stu-id="f3de0-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="f3de0-115">Noklikšķiniet uz Izveidot maksājuma priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="f3de0-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="f3de0-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="f3de0-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="f3de0-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="f3de0-117">Click Filter.</span></span>
10. <span data-ttu-id="f3de0-118">Sarakstā atlasiet rindu Kreditoru tabulai un Kreditora konta laukam.</span><span class="sxs-lookup"><span data-stu-id="f3de0-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="f3de0-119">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f3de0-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="f3de0-120">Varat lietot visus kritērijus, atlasot kreditoru darījumus, kas jāapmaksā, šim piemēram izmantojiet DE-001 kā kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="f3de0-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="f3de0-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3de0-121">Click OK.</span></span>
13. <span data-ttu-id="f3de0-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3de0-122">Click OK.</span></span>
14. <span data-ttu-id="f3de0-123">Noklikšķiniet uz Izveidot maksājumus.</span><span class="sxs-lookup"><span data-stu-id="f3de0-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="f3de0-124">ISO20022 maksājuma faila ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="f3de0-124">Generate an ISO20022 payment file</span></span>


