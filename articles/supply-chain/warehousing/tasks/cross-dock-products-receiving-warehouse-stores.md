---
title: Preču no saņēmēja noliktavas pārkraušana sadales centrā uz veikaliem
description: Šajā procedūrā parādīts, kā izveidot un apstrādāt pārkraušanu sadales centrā, lai izplatītu preces no pirkšanas pasūtījuma saņemšanas vietas uz vienu vai vairākiem veikaliem.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 033d4f72b626130c144faff30fe0d35349b26c6d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433164"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="21ced-103">Preču no saņēmēja noliktavas pārkraušana sadales centrā uz veikaliem</span><span class="sxs-lookup"><span data-stu-id="21ced-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21ced-104">Šajā procedūrā parādīts, kā izveidot un apstrādāt pārkraušanu sadales centrā, lai izplatītu preces no pirkšanas pasūtījuma saņemšanas vietas uz vienu vai vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="21ced-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="21ced-105">Lietotājs var norādīt vairākas konfigurācijas, un sistēma ieteiks, kā sadalīt preces vai manuāli ievadīt veikalu, kur preces tiek sadalītas un kādu daudzumu sadalīt katrā veikalā.</span><span class="sxs-lookup"><span data-stu-id="21ced-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="21ced-106">Procedūras laikā netiek iestatīti dati, ko var izmantot pārkraušanai sadales centrā, piemēram, papildināšanas kārtulas, organizācijas hierarhijas un preču svari veikalam.</span><span class="sxs-lookup"><span data-stu-id="21ced-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="21ced-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="21ced-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="21ced-108">Dodieties uz Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="21ced-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="21ced-109">Sarakstā atlasiet pirkšanas pasūtījumu un noklikšķiniet uz saites, lai atvērtu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="21ced-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="21ced-110">Darbību rūtī noklikšķiniet uz Retail un Commerce.</span><span class="sxs-lookup"><span data-stu-id="21ced-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="21ced-111">Noklikšķiniet uz Pārkraušana sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="21ced-111">Click Cross docking.</span></span>
5. <span data-ttu-id="21ced-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="21ced-112">Click Edit.</span></span>
    * <span data-ttu-id="21ced-113">Kategoriju var izmantot, lai filtrētu krājumus sadaļā Rindas.</span><span class="sxs-lookup"><span data-stu-id="21ced-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="21ced-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="21ced-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="21ced-115">Laukā Daudzums pārkraušanai sadales centrā ievadiet vērtību, lai norādītu, kāds iegādājamās atlasītās preces daudzums ir jāsadala.</span><span class="sxs-lookup"><span data-stu-id="21ced-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="21ced-116">Laukā papildu daudzums pārkraušanai sadales centrā ievadiet vērtību, lai norādītu pieejamo iegādājamo preču sadalāmo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="21ced-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="21ced-117">Laukā Sadale ievadiet Vietas īpatsvars.</span><span class="sxs-lookup"><span data-stu-id="21ced-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="21ced-118">Varat atlasīt citus veidus, kam lietot citādas sadales kārtulas.</span><span class="sxs-lookup"><span data-stu-id="21ced-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="21ced-119">Laukā Papildināšanas hierarhija atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="21ced-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="21ced-120">Laukā Atbilstošie preču klāsti atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="21ced-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="21ced-121">Noklikšķiniet uz Aprēķināt daudzumus.</span><span class="sxs-lookup"><span data-stu-id="21ced-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="21ced-122">Noklikšķiniet uz Izveidot pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="21ced-122">Click Create order.</span></span>
14. <span data-ttu-id="21ced-123">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="21ced-123">Click Yes.</span></span>
15. <span data-ttu-id="21ced-124">Sarakstā atrodiet un atlasiet noliktavu, kur preces tika saņemtas.</span><span class="sxs-lookup"><span data-stu-id="21ced-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="21ced-125">Noklikšķiniet uz Pasūtījums, lai skatītu pasūtījumus, kas tika izveidoti atlasītajai noliktavai.</span><span class="sxs-lookup"><span data-stu-id="21ced-125">Click Order to view the orders that got created for the selected warehouse</span></span>

