---
title: Pakalpojumu pasūtījumu krājumu vajadzības
description: Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bbd15ca83ab116286a3d681887f076896653c76
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810586"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="81951-103">Pakalpojumu pasūtījumu krājumu vajadzības</span><span class="sxs-lookup"><span data-stu-id="81951-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="81951-104">Varat izveidot pakalpojuma pasūtījumu, lai izsekotu un pārvaldītu saviem debitoriem sniegtos pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="81951-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="81951-105">Ja pakalpojuma pasūtījumam ir nepieciešams rezervēt konkrētus krājumus, varat tam izveidot krājuma vienības vajadzības.</span><span class="sxs-lookup"><span data-stu-id="81951-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="81951-106">Krājumu vajadzību var nekavējoties patērēt no krājumiem, vai tā var uzsākt attiecīgā krājuma ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="81951-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="81951-107">Ja krājumu darījuma vietā izmantojat krājuma vajadzību, varat plānot piegādi tieši pirms krājuma faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut krājumu tirdzniecības līguma struktūrā un iekļaut krājuma vajadzību ražošanas plānošanā.</span><span class="sxs-lookup"><span data-stu-id="81951-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="81951-108">Krājumu vajadzības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu.</span><span class="sxs-lookup"><span data-stu-id="81951-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="81951-109">Lai pakalpojumu pasūtījumā izveidotu krājumu vajadzību, šim pakalpojumu pasūtījumam ir jābūt pievienotam pie projekta.</span><span class="sxs-lookup"><span data-stu-id="81951-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="81951-110">Tiklīdz kādam pakalpojuma pasūtījumam ir izveidota krājuma vajadzība, to var apskatīt no sadaļas **Projekts** attiecīgajā pakalpojuma pasūtījumā vai no formas **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="81951-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="81951-111">Krājuma vajadzības apskatīšana no pakalpojuma pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="81951-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="81951-112">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="81951-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="81951-113">Noklikšķiniet uz **Nosūtīt** un pēc tam noklikšķiniet uz **Krājuma vajadzība**, lai atvērtu formu **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="81951-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="81951-114">Noklikšķiniet uz cilnes **Projekts** un pārbaudiet lauku **Pakalpojuma pasūtījums**, lai redzētu krājuma vajadzības pakalpojumu pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="81951-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="81951-115">Dzēsiet pakalpojuma pasūtījumus ar elementa prasībām</span><span class="sxs-lookup"><span data-stu-id="81951-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="81951-116">Ja elementa prasības ir izveidotas pakalpojuma pasūtījumā, nebūs iespējams dzēst pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="81951-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="81951-117">Lai varētu dzēst pakalpojuma pasūtījumu, ir jāizdzēš krājumu vajadzība.</span><span class="sxs-lookup"><span data-stu-id="81951-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="81951-118">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="81951-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="81951-119">Noklikšķiniet uz **Nosūtīt** un pēc tam noklikšķiniet uz **Krājuma vajadzība**, lai atvērtu formu **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="81951-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="81951-120">Šajā formā ir uzskaitītas visas pakalpojuma pasūtījumā izveidotās krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="81951-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="81951-121">Atlasiet dzēšamo krājuma vajadzību un pēc tam noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="81951-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="81951-122">–vai–</span><span class="sxs-lookup"><span data-stu-id="81951-122">–or–</span></span>

1.  <span data-ttu-id="81951-123">Noklikšķiniet uz **Projektu pārvaldība un uzskaite** \> **Vispārīgi** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="81951-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="81951-124">Atveriet projektu, kuram ir pakalpojumu pasūtījums ar izveidoto krājumu vajadzību.</span><span class="sxs-lookup"><span data-stu-id="81951-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="81951-125">Formā **Projekti**, labajā rūtī noklikšķiniet uz **Krājumu vajadzības**.</span><span class="sxs-lookup"><span data-stu-id="81951-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="81951-126">Formā **Krājumu vajadzības** ir uzskaitītas krājumu vajadzības, kas ir saistītas ar atlasīto projektu.</span><span class="sxs-lookup"><span data-stu-id="81951-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="81951-127">Atlasiet dzēšamo krājuma vajadzību un pēc tam noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="81951-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="81951-128">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="81951-128">See also</span></span>

<span data-ttu-id="81951-129">[Krājumu vajadzības (forma)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="81951-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]