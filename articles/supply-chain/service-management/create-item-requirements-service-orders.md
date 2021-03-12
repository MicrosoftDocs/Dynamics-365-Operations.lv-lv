---
title: Izveidot krājumu prasības pakalpojumu pasūtījumiem
description: Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ae44088a1b53ac5e7e9ba09ed7ff611a08d2ed0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996704"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="96085-103">Izveidot krājumu prasības pakalpojumu pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="96085-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="96085-104">Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="96085-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="96085-105">Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības.</span><span class="sxs-lookup"><span data-stu-id="96085-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="96085-106">Krājumu vajadzību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="96085-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="96085-107">Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.</span><span class="sxs-lookup"><span data-stu-id="96085-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="96085-108">Krājumu vajadzības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu.</span><span class="sxs-lookup"><span data-stu-id="96085-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="96085-109">Lai pakalpojumu pasūtījumā izveidotu krājumu vajadzību, šim pakalpojumu pasūtījumam ir jābūt piešķirtam projektam.</span><span class="sxs-lookup"><span data-stu-id="96085-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="96085-110">Pēc tam, kad pakalpojuma pasūtījumam ir izveidota krājumu vajadzība, varat skatīt krājumu vajadzības atlasītā projekta veidlapā **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="96085-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="96085-111">Krājumu vajadzības izveide pakalpojuma pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="96085-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="96085-112">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="96085-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="96085-113">Atlasiet pakalpojuma pasūtījumu, kuram vēlaties izveidot krājumu vajadzību.</span><span class="sxs-lookup"><span data-stu-id="96085-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="96085-114">Sadaļas **Darbību rūts** cilnē **Nosūtīšana** noklikšķiniet uz **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="96085-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="96085-115">Veidlapā **Krājumu vajadzības** ievadiet informāciju par nepieciešamo krājumu.</span><span class="sxs-lookup"><span data-stu-id="96085-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="96085-116">Papildinformāciju par noteiktiem laukiem skatiet rakstā [Krājumu vajadzības (veidlapa)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="96085-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="96085-117">Krājumu vajadzības izveide pakalpojuma līgumam</span><span class="sxs-lookup"><span data-stu-id="96085-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="96085-118">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="96085-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="96085-119">Atveriet pakalpojuma līgumu, kuram vēlaties izveidot krājumu vajadzību.</span><span class="sxs-lookup"><span data-stu-id="96085-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="96085-120">Kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pievienot**, lai izveidotu jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="96085-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="96085-121">Laukā **Transakcijas veids** atlasiet vienumu **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="96085-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="96085-122">Laukā **Krājumu iestatījumi** atlasiet vienumu **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="96085-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="96085-123">Laukā **Krājuma kods** atlasiet krājumu, kurš ir nepieciešams pakalpojuma līgumam.</span><span class="sxs-lookup"><span data-stu-id="96085-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="96085-124">Kopsavilkuma cilnē **Detalizēta informācija par rindu** cilnes **Preču dimensijas** laukā **Atrašanās vieta** atlasiet krājuma vienības atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="96085-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="96085-125">Lai izveidotu pakalpojumu pasūtījumu no līguma rindas, kopsavilkuma cilnē **Rindas** noklikšķiniet uz **Pakalpojumu pasūtījumu izveide** un pēc tam ievadiet atbilstošo informāciju veidlapā **Pakalpojumu pasūtījumu izveide**.</span><span class="sxs-lookup"><span data-stu-id="96085-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="96085-126">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="96085-126">See also</span></span>

<span data-ttu-id="96085-127">[Automātiska pakalpojumu pasūtījumu izveide](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="96085-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


