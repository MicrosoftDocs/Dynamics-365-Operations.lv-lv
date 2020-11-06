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
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107356"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="1d1a6-103"> Zvanu centra pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="1d1a6-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d1a6-104">Šajā procedūrā parādīts, kā meklēt debitoru, izveidot jaunu pasūtījumu, meklēt preci un iekasēt maksājumu no debitora.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="1d1a6-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, un to paredzēts izmantot darbiniekam, kurš izstrādā pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="1d1a6-106">Priekšnosacījumi: lietotājs, kas izpilda procedūru, ir iestatīts kā zvanu centra lietotājs, un Fabrikam pusgada katalogs ir publicēts ar vismaz vienu avota kodu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="1d1a6-107">Dodieties uz **Mazumtirdzniecība un komercija \> Debitori \> Debitoru apkalpošana**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="1d1a6-108">Laukā **SearchText** ievadiet meklēšanas kritērijus, lai atrastu debitoru.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="1d1a6-109">Lai veiktu šo procedūru, ierakstiet “Karen” un atlasiet **Cilne**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="1d1a6-110">Atlasiet Meklēt.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-110">Select Search.</span></span>
    * <span data-ttu-id="1d1a6-111">Demonstrācijas datos ir tikai viens debitors ar nosaukumu "Karen", tādēļ rezultāts tiks automātiski atlasīts.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="1d1a6-112">Atlasiet vienumu **Jauns pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="1d1a6-113">Izvērsiet vai sakļaujiet sadaļas **Pārdošanas pasūtījums** galveni.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="1d1a6-114">Atlasiet kataloga avota kodu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="1d1a6-115">Ja nav aktīvu avota kodu, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="1d1a6-116">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-116">Select **Add line**.</span></span>
8. <span data-ttu-id="1d1a6-117">Laukā **Krājuma numurs**  ievadiet ar krājumu saistīto meklējamo terminu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="1d1a6-118">Lai veiktu šo procedūru, ievadiet daļēju krājuma numuru “8111” un nospiediet tabulēšanas taustiņu. Šī darbība parādīs krājuma meklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="1d1a6-119">Atlasiet preci, ko pievienot pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="1d1a6-120">Ievadiet pārdodamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="1d1a6-121">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-121">Select **Create**.</span></span>
12. <span data-ttu-id="1d1a6-122">Atlasiet **Pabeigt** , lai iekasētu no debitora maksājumu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="1d1a6-123">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-123">Select **Add**.</span></span>
    * <span data-ttu-id="1d1a6-124">Sadaļa Pievienot saiti ir pieejama cilnē Maksājumi. Izvērsiet cilni Maksājumi, ja tā ir sakļauta.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="1d1a6-125">Atlasiet maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-125">Select the payment method.</span></span>
    * <span data-ttu-id="1d1a6-126">Lai veiktu šo procedūru, atlasiet skaidras naudas maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="1d1a6-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-127">Close the page.</span></span>
16. <span data-ttu-id="1d1a6-128">Ievadiet summu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-128">Enter the amount.</span></span>
    * <span data-ttu-id="1d1a6-129">Lai veiktu šo procedūru, ievadiet summu, kas ir vienāda ar pasūtījuma bilanci, kuru var redzēt lapā Pārdošanas pasūtījumu kopsavilkums pa kreisi no summas lauka.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="1d1a6-130">Šī darbība ļaus izpildīt pasūtījumu kā pilnībā apmaksātu.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="1d1a6-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-131">Select **OK**.</span></span>
18. <span data-ttu-id="1d1a6-132">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-132">Select **Submit**.</span></span>

