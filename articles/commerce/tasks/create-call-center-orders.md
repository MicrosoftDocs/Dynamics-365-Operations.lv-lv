---
title: " Zvanu centra pasūtījumu izveide"
description: Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141434"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="dc30e-103"> Zvanu centra pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="dc30e-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc30e-104">Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora.</span><span class="sxs-lookup"><span data-stu-id="dc30e-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="dc30e-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, un to paredzēts izmantot darbiniekam, kurš izstrādā pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="dc30e-106">Priekšnosacījumi: lietotājs, kas izpilda procedūru, ir iestatīts kā zvanu centra lietotājs, un Fabrikam pusgada katalogs ir publicēts ar vismaz vienu avota kodu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="dc30e-107">Dodieties uz Retail un Commerce > Debitori > Debitoru apkalpošana.</span><span class="sxs-lookup"><span data-stu-id="dc30e-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="dc30e-108">Laukā SearchText ievadiet meklēšanas kritērijus, lai atrastu debitoru.</span><span class="sxs-lookup"><span data-stu-id="dc30e-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="dc30e-109">Lai veiktu šo procedūru, ierakstiet “karen” un nospiediet tabulēšanas taustiņu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="dc30e-110">Noklikšķiniet uz Meklēt.</span><span class="sxs-lookup"><span data-stu-id="dc30e-110">Click Search.</span></span>
    * <span data-ttu-id="dc30e-111">Demonstrācijas datos ir tikai viens debitors ar nosaukumu Karen, tādēļ tas tiks automātiski atlasīts.</span><span class="sxs-lookup"><span data-stu-id="dc30e-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="dc30e-112">Noklikšķiniet uz Jauns pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="dc30e-112">Click New sales order.</span></span>
5. <span data-ttu-id="dc30e-113">Izvērsiet vai sakļaujiet sadaļas Pārdošanas pasūtījums galveni.</span><span class="sxs-lookup"><span data-stu-id="dc30e-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="dc30e-114">Atlasiet kataloga avota kodu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="dc30e-115">Ja nav aktīvu avota kodu, varat aizvērt lauku Avots un izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="dc30e-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="dc30e-116">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-116">Click Add line.</span></span>
8. <span data-ttu-id="dc30e-117">Laukā Krājuma numurs ievadiet ar krājumu saistīto meklējamo terminu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="dc30e-118">Lai veiktu šo procedūru, ievadiet daļēju krājuma numuru “8111” un nospiediet tabulēšanas taustiņu. Tas tiks parādīts krājuma meklēšanas logā.</span><span class="sxs-lookup"><span data-stu-id="dc30e-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="dc30e-119">Atlasiet preci, ko pievienot pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="dc30e-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="dc30e-120">Ievadiet pārdodamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="dc30e-121">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="dc30e-121">Click Create.</span></span>
12. <span data-ttu-id="dc30e-122">Noklikšķiniet uz Pabeigt, lai iekasētu no debitora maksājumu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="dc30e-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="dc30e-123">Click Add.</span></span>
    * <span data-ttu-id="dc30e-124">Sadaļa Pievienot saiti ir pieejama cilnē Maksājumi. Izvērsiet cilni Maksājumi, ja tā ir sakļauta.</span><span class="sxs-lookup"><span data-stu-id="dc30e-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="dc30e-125">Atlasiet maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="dc30e-125">Select the payment method.</span></span>
    * <span data-ttu-id="dc30e-126">Lai veiktu šo procedūru, atlasiet skaidras naudas maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="dc30e-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="dc30e-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-127">Close the page.</span></span>
16. <span data-ttu-id="dc30e-128">Ievadiet summu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-128">Enter the amount.</span></span>
    * <span data-ttu-id="dc30e-129">Lai veiktu šo procedūru, ievadiet summu, kas ir vienāda ar pasūtījuma bilanci, ko var redzēt lapā Pārdošanas pasūtījumu kopsavilkums pa kreisi no summas lauka.</span><span class="sxs-lookup"><span data-stu-id="dc30e-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="dc30e-130">Tādējādi varēsit izpildīt pasūtījumu kā pilnībā apmaksātu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="dc30e-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc30e-131">Click OK.</span></span>
18. <span data-ttu-id="dc30e-132">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="dc30e-132">Click Submit.</span></span>

