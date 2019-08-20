---
title: Projekta pirkšanas pasūtījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot projekta pirkšanas pasūtījumu.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 195fa23fc3d4f407ab82e1584fe870bfdd01c82a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838194"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="e2ba2-103">Projekta pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="e2ba2-103">Create project purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2ba2-104">Šajā procedūrā ir parādīts, kā izveidot projekta pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="e2ba2-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e2ba2-106">Dodieties uz Projektu vadība un uzskaite > Projekti > Visi projekti.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="e2ba2-107">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e2ba2-108">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e2ba2-109">Noklikšķiniet uz Krājumu uzdevums.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-109">Click Item task.</span></span>
5. <span data-ttu-id="e2ba2-110">Noklikšķiniet uz Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-110">Click Purchase order.</span></span>
6. <span data-ttu-id="e2ba2-111">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="e2ba2-112">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e2ba2-113">Šīs darbības nav obligātas, bet tās vienkāršo pirkšanas pasūtījumu, pirkšanas pasūtījuma rindām iestatot noklusējuma vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="e2ba2-114">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="e2ba2-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-115">Click OK.</span></span>
10. <span data-ttu-id="e2ba2-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e2ba2-117">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e2ba2-118">Tas var būt krājuma kods vai sagādes kategorija.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="e2ba2-119">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="e2ba2-120">Noklikšķiniet uz cilnes Projekts.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-120">Click the Project tab.</span></span>
    * <span data-ttu-id="e2ba2-121">Pārbaudiet, vai ir pieejamas pārdošanas un izmaksu cenas.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="e2ba2-122">Ja tās nav pieejamas, bet ir nepieciešamas, ievadiet informāciju.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="e2ba2-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2ba2-123">Click Save.</span></span>

