---
title: "Sūtījuma krājumu pārraudzība, izmantojot kreditoru sadarbību"
description: "Šajā procedūrā ir parādīts kā izmantot kreditoru sadarbību, lai skatītu informāciju par preces rezerves līmeni, kas tika novietots sūtījumā ar debitoru."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="54e88-103">Sūtījuma krājumu pārraudzība, izmantojot kreditoru sadarbību</span><span class="sxs-lookup"><span data-stu-id="54e88-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54e88-104">Šajā procedūrā ir parādīts kā izmantot kreditoru sadarbību, lai skatītu informāciju par preces rezerves līmeni, kas tika novietots sūtījumā ar debitoru.</span><span class="sxs-lookup"><span data-stu-id="54e88-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="54e88-105">Jūs varat arī pārraudzīt rezerves patēriņu, kad debitors uzņemas atbildību par krājumu.</span><span class="sxs-lookup"><span data-stu-id="54e88-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="54e88-106">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="54e88-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="54e88-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="54e88-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="54e88-108">Skatīt patērēto krājumu</span><span class="sxs-lookup"><span data-stu-id="54e88-108">View consumed inventory</span></span>
1. <span data-ttu-id="54e88-109">Dodieties uz Kreditoru sadarbība > Sūtījuma krājumi > No sūtījuma krājumiem saņemtās preces.</span><span class="sxs-lookup"><span data-stu-id="54e88-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="54e88-110">Sarakstā ir parādītas produktu ieejas plūsmas rindas, kas tika ģenerētas, kad sūtījuma krājumu īpašumtiesības tika mainīts no kreditora uz debitoru.</span><span class="sxs-lookup"><span data-stu-id="54e88-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="54e88-111">Jums var nākties ritināt pa labi, lai redzētu daudzumus un citu informāciju.</span><span class="sxs-lookup"><span data-stu-id="54e88-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="54e88-112">Jūs varat izmantot informāciju šajā sarakstā, lai ģenerētu rēķinus jūsu debitoram.</span><span class="sxs-lookup"><span data-stu-id="54e88-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="54e88-113">Jūs varat arī eksportēt datus uz Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="54e88-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="54e88-114">Noklikšķiniet uz Skatīt pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54e88-114">Click View purchase order.</span></span>
3. <span data-ttu-id="54e88-115">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="54e88-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="54e88-116">Rinda ir atzīmēta kā Sūtījums, un virsraksts norāda, ka pirkšanas pasūtījuma statuss ir Saņemts.</span><span class="sxs-lookup"><span data-stu-id="54e88-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="54e88-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54e88-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="54e88-118">Apskatīt rīcībā esošos krājumus</span><span class="sxs-lookup"><span data-stu-id="54e88-118">View on-hand inventory</span></span>
1. <span data-ttu-id="54e88-119">Dodieties uz Kreditoru sadarbība > Sūtījuma krājumi > Rīcībā esošie sūtījuma krājumi.</span><span class="sxs-lookup"><span data-stu-id="54e88-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="54e88-120">Sūtījuma rīcībā esošo krājumu lapā tiek rādīta rezerve, ka jums pieder debitora noliktavā.</span><span class="sxs-lookup"><span data-stu-id="54e88-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="54e88-121">Jūs varat rādīt papildu dimensijas, piemēram, vieta un noliktava, noklikšķinot cilnes Parādīt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="54e88-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

