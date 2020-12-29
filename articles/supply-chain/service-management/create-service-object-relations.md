---
title: Pakalpojumu objekta attiecību veidošana
description: Šajā tēmā aprakstīts, kā izveidot pakalpojumu objektu attiecības pakalpojumu līgumam un pakalpojuma pasūtījumam.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 352d3b790da340102b7dbe116d9deeb2f3cbfc4e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432967"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="02de7-103">Pakalpojumu objekta attiecību veidošana</span><span class="sxs-lookup"><span data-stu-id="02de7-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="02de7-104">Šajā tēmā aprakstīts, kā izveidot pakalpojumu objektu attiecības pakalpojumu līgumam un pakalpojuma pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="02de7-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="02de7-105">Kad tiek izveidotas pakalpojumu objektu relācijas, pakalpojuma līgumam vai pakalpojuma pasūtījumam ir jāpiesaista pakalpojuma objekts.</span><span class="sxs-lookup"><span data-stu-id="02de7-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="02de7-106">Kad debitors pieprasa pakalpojumu krājumam, kas ir pakalpojuma objekts, varat atlasīt pakalpojuma objektu pakalpojumu objektu attiecību sarakstā.</span><span class="sxs-lookup"><span data-stu-id="02de7-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="02de7-107">Pakalpojumu objektu attiecību izveide pakalpojumu līgumam</span><span class="sxs-lookup"><span data-stu-id="02de7-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="02de7-108">Lai izveidotu pakalpojumu objektu attiecības pakalpojumu līgumam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="02de7-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="02de7-109">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="02de7-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="02de7-110">Sarakstā **Pakalpojumu līgumi** atlasiet esošu pakalpojumu līgumu vai noklikšķiniet uz **Jauns**, lai izveidotu jaunu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="02de7-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="02de7-111">Veidlapas **Pakalpojumu līgumi** **Darbību rūts** cilnē **Pakalpojumu līgums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.</span><span class="sxs-lookup"><span data-stu-id="02de7-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="02de7-112">Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="02de7-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="02de7-113">Lai pakalpojumu līgumam piešķirtu veidnes materiālu komplektu (MK), noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**.</span><span class="sxs-lookup"><span data-stu-id="02de7-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="02de7-114">Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni.</span><span class="sxs-lookup"><span data-stu-id="02de7-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="02de7-115">Pakalpojumu objektu attiecību izveide pakalpojuma pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="02de7-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="02de7-116">Lai izveidotu pakalpojumu objektu attiecības pakalpojuma pasūtījumam, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="02de7-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="02de7-117">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="02de7-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="02de7-118">Sarakstā **Pakalpojumu pasūtījumi** atlasiet esošu pakalpojuma pasūtījumu vai izveidojiet jaunu pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="02de7-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="02de7-119">Veidlapas **Pakalpojumu pasūtījumi** **Darbību rūts** cilnē **Pakalpojuma pasūtījums** grupā **Relācijas** noklikšķiniet uz **Pakalpojumu objekti**.</span><span class="sxs-lookup"><span data-stu-id="02de7-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="02de7-120">Veidlapā **Pakalpojumu objekti** noklikšķiniet uz **Jauns** un pēc tam atlasiet pakalpojuma objektu šim pakalpojuma pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="02de7-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="02de7-121">Lai pakalpojumu līgumam piešķirtu veidnes MK, noklikšķiniet uz **Funkcijas** un pēc tam atlasiet **Pievienot veidnes MK**.</span><span class="sxs-lookup"><span data-stu-id="02de7-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="02de7-122">Veidlapas **Veidnes MK atlasīšana** laukā **Veidnes MK** atlasiet veidni.</span><span class="sxs-lookup"><span data-stu-id="02de7-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="02de7-123">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="02de7-123">See also</span></span>

[<span data-ttu-id="02de7-124">Pakalpojumu objektu pārskats</span><span class="sxs-lookup"><span data-stu-id="02de7-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="02de7-125">Pakalpojumu objektu relācijas</span><span class="sxs-lookup"><span data-stu-id="02de7-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="02de7-126">Veidnes MK</span><span class="sxs-lookup"><span data-stu-id="02de7-126">Template BOMs</span></span>](template-boms.md)

  


