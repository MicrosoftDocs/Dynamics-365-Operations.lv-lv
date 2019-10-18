---
title: Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram
description: Var reģistrēt detalizētu informāciju par iegrāmatoto no klienta saņemto čeku.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f27675a2aa2160619bf78eea33bba2ce0b7bd81
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188100"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="680c7-103">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</span><span class="sxs-lookup"><span data-stu-id="680c7-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="680c7-104">Var reģistrēt detalizētu informāciju par iegrāmatoto no klienta saņemto čeku.</span><span class="sxs-lookup"><span data-stu-id="680c7-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="680c7-105">Var arī grāmatot ar iepriekšēju datumu datēto čeku un ģenerētu finanšu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="680c7-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="680c7-106">Pirms no debitora saņemt ar iepriekšēju datumu datēta čeka reģistrēšanas un grāmatošanas veiciet tālāk norādītos uzdevumus. • Iestatiet ar iepriekšējo datumu datētos čekus lapā Kases un bankas pārvaldība. • Iestatīt ar iepriekšējo datumu datēto čeku maksāšanas metodi. Šīs procedūras izpildei ir nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="680c7-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="680c7-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="680c7-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="680c7-108">Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="680c7-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="680c7-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="680c7-109">Click New.</span></span>
3. <span data-ttu-id="680c7-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="680c7-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="680c7-111">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="680c7-111">Click Lines.</span></span>
5. <span data-ttu-id="680c7-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="680c7-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="680c7-113">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="680c7-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="680c7-114">Laukā Kredīts ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="680c7-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="680c7-115">Ievadiet summu, kas norādīta ar iepriekšēju datumu datētajā čekā.</span><span class="sxs-lookup"><span data-stu-id="680c7-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="680c7-116">Noklikšķiniet uz cilnes Maksājums.</span><span class="sxs-lookup"><span data-stu-id="680c7-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="680c7-117">Ierakstiet vērtību laukā Maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="680c7-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="680c7-118">Maksāšanas tipa atlasīšana ar iepriekšēju datumu datētajam čekam</span><span class="sxs-lookup"><span data-stu-id="680c7-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="680c7-119">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="680c7-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="680c7-120">Laukā Samaksas galējais datums ierakstiet datumu.</span><span class="sxs-lookup"><span data-stu-id="680c7-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="680c7-121">Ievadiet datumu, kad jāveic ar iepriekšēju datumu datēta čeka maksājums.</span><span class="sxs-lookup"><span data-stu-id="680c7-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="680c7-122">Laukā Izdevēja bankas filiāle ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="680c7-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="680c7-123">Ievadiet bankas informāciju ar iepriekšēju datumu datētajam čekam.</span><span class="sxs-lookup"><span data-stu-id="680c7-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="680c7-124">Laukā Čeka numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="680c7-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="680c7-125">Laukā Izdevēja bankas nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="680c7-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="680c7-126">Ievadiet bankas informāciju ar iepriekšēju datumu datētajam čekam.</span><span class="sxs-lookup"><span data-stu-id="680c7-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="680c7-127">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="680c7-127">Click Post.</span></span>
16. <span data-ttu-id="680c7-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="680c7-128">Close the page.</span></span>

