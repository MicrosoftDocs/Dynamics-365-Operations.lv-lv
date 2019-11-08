---
title: Ienākošie un izejošie līdzekļi
description: Šajā tēmā paskaidrots, kā reģistrēt ienākošos un izejošos līdzekļus Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb318c24424c291f08ba7527b2258c0da4cba9a8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571672"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="36204-103">Ienākošie un izejošie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="36204-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="36204-104">Ja jūsu uzņēmums veic labošanas darbus vai uzturēšanas darbus līdzekļiem, kas saņemti no citām atrašanās vietām vai debitoriem, Līdzekļu pārvaldība var izsekot gan ienākošos līdzekļus, kas ir ceļā uz jūsu uzņēmumu, gan uz izejošos līdzekļus, kas tiek atgriezti.</span><span class="sxs-lookup"><span data-stu-id="36204-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="36204-105">Ja vēlaties izmantot ienākošos un izejošos dzīves cikla stāvokļus, lai pārvaldītu līdzekļus, kas ienāk un tiek atgriezti, jums ir jāiestata uzturēšanas pieprasījumu dzīves cikla stāvokļi un dzīves cikla modeļi šo darbību atbalstīšanai.</span><span class="sxs-lookup"><span data-stu-id="36204-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="36204-106">Papildinformāciju skatiet sadaļā [Uzturēšanas pieprasījumu iestatīšana](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="36204-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="36204-107">Līdzekļu pārvaldības iestatījumi nosaka, vai varat strādāt ar ienākošajiem un izejošajiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="36204-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="36204-108">Reģistrēt līdzekļus kā ienākošos</span><span class="sxs-lookup"><span data-stu-id="36204-108">Register assets as inbound</span></span>

1. <span data-ttu-id="36204-109">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="36204-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="36204-110">Atlasit uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="36204-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="36204-111">Atlasiet **Atjaunināt uzturēšanas pieprasījuma stāvokli**.</span><span class="sxs-lookup"><span data-stu-id="36204-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="36204-112">Atlasiet **Ienākošais** (vai cits dzīves cikla stāvoklis, ko esat izveidojis ienākošajiem līdzekļiem) un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36204-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Reģistrēt līdzekļus kā ienākošos](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="36204-114">Reģistrēt ienākošos līdzekļus kā saņemtus</span><span class="sxs-lookup"><span data-stu-id="36204-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="36204-115">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Ienākošie/izejošie** \> **Ienākošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="36204-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="36204-116">Atlasiet līdzekli vai uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="36204-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="36204-117">Atlasiet **Saņemt līdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="36204-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="36204-118">Laukā **Saņemts** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="36204-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="36204-119">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36204-119">Then select **OK**.</span></span> <span data-ttu-id="36204-120">Ieraksts tiek noņemts saraksta lapā **Ienākošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="36204-120">The record is removed from the **Inbound assets** list page.</span></span>

![Reģistrēt ienākošos līdzekļus kā saņemtus](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="36204-122">Reģistrēt līdzekļus kā izejošos</span><span class="sxs-lookup"><span data-stu-id="36204-122">Register assets as outbound</span></span>

<span data-ttu-id="36204-123">Kad esat pabeidzis uzturēšanas vai labošanas darbu, līdzekli var reģistrēt kā atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="36204-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="36204-124">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Uzturēšanas pieprasījumi** \> **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="36204-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="36204-125">Atlasit uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="36204-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="36204-126">Atlasiet **Atjaunināt uzturēšanas pieprasījuma stāvokli**.</span><span class="sxs-lookup"><span data-stu-id="36204-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="36204-127">Atlasiet **Izejošie** (vai cits dzīves cikla stāvoklis, ko esat izveidojis izejošajiem līdzekļiem) un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36204-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="36204-128">Reģistrēt izejošos līdzekļus kā piegādātus</span><span class="sxs-lookup"><span data-stu-id="36204-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="36204-129">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Ienākošie/izejošie** \> **Izejošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="36204-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="36204-130">Atlasiet līdzekli vai uzturēšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="36204-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="36204-131">Atlasiet **Piegādātie līdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="36204-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="36204-132">Laukā **Piegādāts** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="36204-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="36204-133">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36204-133">Then select **OK**.</span></span> <span data-ttu-id="36204-134">Ieraksts tiek noņemts saraksta lapā **Izejošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="36204-134">The record is removed from the **Outbound assets** list page.</span></span>
