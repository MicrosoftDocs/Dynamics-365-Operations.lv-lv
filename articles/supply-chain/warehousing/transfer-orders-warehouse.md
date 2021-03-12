---
title: Noliktavu iestatīšana pārsūtīšanas pasūtījumiem
description: Šajā tēmā ir aprakstīts, kā var iestatīt noliktavas pārsūtīšanas pasūtījumiem.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7dfb215683b4ee5d186626492bd90116d1a06a1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976842"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="3ad28-103">Noliktavu iestatīšana pārsūtīšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="3ad28-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ad28-104">Var izmantot noliktavas līmeņus, lai izveidotu hierarhiju, kas atbalsta pārsūtīšanas pasūtījumus starp noliktavām.</span><span class="sxs-lookup"><span data-stu-id="3ad28-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="3ad28-105">Pamatojoties uz šo iestatījumu, vispārējā (grafika) plānošana aprēķina krājuma vajadzības atsevišķās noliktavas līmenī un izveido plānotos pārsūtīšanas pasūtījumus no piešķirtās avota noliktavas, lai tos izpildītu.</span><span class="sxs-lookup"><span data-stu-id="3ad28-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="3ad28-106">Noklikšķiniet uz **Krājumu vadība > Iestatījumi > Noliktavu sadalījums > Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="3ad28-107">Atlasiet noliktavu, kas jāuzpilda.</span><span class="sxs-lookup"><span data-stu-id="3ad28-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="3ad28-108">Kopsavilkuma cilnē **Vispārējā plānošana** atzīmējiet izvēles rūtiņu **Uzpilde**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="3ad28-109">Laukā **Galvenā noliktava** atlasiet to noliktavu, ko vēlaties piešķirt kā uzpildes noliktavu.</span><span class="sxs-lookup"><span data-stu-id="3ad28-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="3ad28-110">Vispārējā plānošana aprēķina pārsūtīšanas pieprasījumu atlasītajai noliktavai un ģenerē plānotās pārsūtīšanas pasūtījumu no piešķirtās **Galvenās noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="3ad28-111">Ja noņem atzīmi izvēles rūtiņā <STRONG>Uzpilde</STRONG>, atlasītajai noliktavai tiek piešķirts noliktavas līmenis saistībā ar <STRONG>Galveno noliktavu</STRONG>, bet <STRONG>Galvenā noliktava</STRONG> netiek iestatīta kā uzpildes noliktava.</span><span class="sxs-lookup"><span data-stu-id="3ad28-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="3ad28-112">Lai lietotu jauno iestatījumu, aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="3ad28-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="3ad28-113">Ja uzpildīšanai vēlaties piešķirt noliktavu, vispirms lapā <STRONG>Noliktavas dimensiju grupas</STRONG> ir jāiestata noliktava kā noliktavas dimensija.</span><span class="sxs-lookup"><span data-stu-id="3ad28-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="3ad28-114">Šajā lapā atlasiet noliktavai lauku <STRONG>Aktīva</STRONG> un lauku <STRONG>Vajadzības plāns pa dimensijām</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3ad28-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="3ad28-115">Transportēšanas izpildes laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3ad28-115">Set up transport lead time</span></span>

<span data-ttu-id="3ad28-116">Lapā **Transportēšanas dienas** ir jāiestata arī transportēšanas izpildes laiks starp noliktavām.</span><span class="sxs-lookup"><span data-stu-id="3ad28-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="3ad28-117">Atveriet sadaļu **Krājumu vadība > Iestatījumi > Sadale > Transportēšanas dienas**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="3ad28-118">Laukā **Saņemšanas punkts** atlasiet vienumu **noliktava**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="3ad28-119">Atlasiet **Nosūtītāja noliktava**, **Saņēmēja noliktava** un **Transportēšanas dienas**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="3ad28-120">(Nav obligāti) Varat arī iestatīt transportēšanas laiku atkarībā no piegādes veida cilnē **Transportēšanas dienas atbilstoši piegādes veidam**.</span><span class="sxs-lookup"><span data-stu-id="3ad28-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
