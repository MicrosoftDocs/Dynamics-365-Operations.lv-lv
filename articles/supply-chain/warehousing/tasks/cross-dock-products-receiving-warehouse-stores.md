---
title: Preču no saņēmēja noliktavas pārkraušana sadales centrā uz veikaliem
description: Šajā procedūrā parādīts, kā izveidot un apstrādāt pārkraušanu sadales centrā, lai izplatītu preces no pirkšanas pasūtījuma saņemšanas vietas uz vienu vai vairākiem veikaliem.
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f297a9bbb8ad5d1cd701626783e7db75c94fa842
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148381"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="ecf0f-103">Preču no saņēmēja noliktavas pārkraušana sadales centrā uz veikaliem</span><span class="sxs-lookup"><span data-stu-id="ecf0f-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ecf0f-104">Šajā procedūrā parādīts, kā izveidot un apstrādāt pārkraušanu sadales centrā, lai izplatītu preces no pirkšanas pasūtījuma saņemšanas vietas uz vienu vai vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="ecf0f-105">Lietotājs var norādīt vairākas konfigurācijas, un sistēma ieteiks, kā sadalīt preces vai manuāli ievadīt veikalu, kur preces tiek sadalītas un kādu daudzumu sadalīt katrā veikalā.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="ecf0f-106">Procedūras laikā netiek iestatīti dati, ko var izmantot pārkraušanai sadales centrā, piemēram, papildināšanas kārtulas, organizācijas hierarhijas un preču svari veikalam.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="ecf0f-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ecf0f-108">Dodieties uz Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="ecf0f-109">Sarakstā atlasiet pirkšanas pasūtījumu un noklikšķiniet uz saites, lai atvērtu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="ecf0f-110">Darbību rūtī noklikšķiniet uz Retail un Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="ecf0f-111">Noklikšķiniet uz Pārkraušana sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-111">Click Cross docking.</span></span>
5. <span data-ttu-id="ecf0f-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-112">Click Edit.</span></span>
    * <span data-ttu-id="ecf0f-113">Kategoriju var izmantot, lai filtrētu krājumus sadaļā Rindas.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="ecf0f-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ecf0f-115">Laukā Daudzums pārkraušanai sadales centrā ievadiet vērtību, lai norādītu, kāds iegādājamās atlasītās preces daudzums ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="ecf0f-116">Laukā papildu daudzums pārkraušanai sadales centrā ievadiet vērtību, lai norādītu pieejamo iegādājamo preču sadalāmo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="ecf0f-117">Laukā Sadale ievadiet Vietas īpatsvars.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="ecf0f-118">Varat atlasīt citus veidus, kam lietot citādas sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="ecf0f-119">Laukā Papildināšanas hierarhija atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="ecf0f-120">Laukā Atbilstošie preču klāsti atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="ecf0f-121">Noklikšķiniet uz Aprēķināt daudzumus.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="ecf0f-122">Noklikšķiniet uz Izveidot pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-122">Click Create order.</span></span>
14. <span data-ttu-id="ecf0f-123">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-123">Click Yes.</span></span>
15. <span data-ttu-id="ecf0f-124">Sarakstā atrodiet un atlasiet noliktavu, kur preces tika saņemtas.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="ecf0f-125">Noklikšķiniet uz Pasūtījums, lai skatītu pasūtījumus, kas tika izveidoti atlasītajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="ecf0f-125">Click Order to view the orders that got created for the selected warehouse</span></span>

