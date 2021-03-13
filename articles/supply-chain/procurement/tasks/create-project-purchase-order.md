---
title: Projekta pirkšanas pasūtījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot projekta pirkšanas pasūtījumu.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, PurchTablePart, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 825e374e9d450ee187e7ddb1ce5925c3d7e15f25
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016431"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="33356-103">Projekta pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="33356-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33356-104">Šajā procedūrā ir parādīts, kā izveidot projekta pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="33356-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="33356-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="33356-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="33356-106">Dodieties uz Projektu vadība un uzskaite > Projekti > Visi projekti.</span><span class="sxs-lookup"><span data-stu-id="33356-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="33356-107">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="33356-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="33356-108">Darbību rūtī noklikšķiniet uz Pārvaldīt.</span><span class="sxs-lookup"><span data-stu-id="33356-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="33356-109">Noklikšķiniet uz Krājumu uzdevums.</span><span class="sxs-lookup"><span data-stu-id="33356-109">Click Item task.</span></span>
5. <span data-ttu-id="33356-110">Noklikšķiniet uz Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="33356-110">Click Purchase order.</span></span>
6. <span data-ttu-id="33356-111">Ievadiet vai atlasiet vērtību laukā kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="33356-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="33356-112">Laukā Vieta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33356-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="33356-113">Šīs darbības nav obligātas, bet tās vienkāršo pirkšanas pasūtījumu, pirkšanas pasūtījuma rindām iestatot noklusējuma vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="33356-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="33356-114">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33356-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="33356-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33356-115">Click OK.</span></span>
10. <span data-ttu-id="33356-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="33356-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="33356-117">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33356-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="33356-118">Tas var būt krājuma kods vai sagādes kategorija.</span><span class="sxs-lookup"><span data-stu-id="33356-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="33356-119">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="33356-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="33356-120">Noklikšķiniet uz cilnes Projekts.</span><span class="sxs-lookup"><span data-stu-id="33356-120">Click the Project tab.</span></span>
    * <span data-ttu-id="33356-121">Pārbaudiet, vai ir pieejamas pārdošanas un izmaksu cenas.</span><span class="sxs-lookup"><span data-stu-id="33356-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="33356-122">Ja tās nav pieejamas, bet ir nepieciešamas, ievadiet informāciju.</span><span class="sxs-lookup"><span data-stu-id="33356-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="33356-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33356-123">Click Save.</span></span>

