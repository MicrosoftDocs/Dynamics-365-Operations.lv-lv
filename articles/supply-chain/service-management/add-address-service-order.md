---
title: Adreses pievienošana pakalpojuma pasūtījumam
description: Šajā tēmā aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570369"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="b6f1c-103">Adreses pievienošana pakalpojuma pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="b6f1c-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b6f1c-104">Šajā tēmā aprakstīts, kā pievienot debitora adresi pakalpojuma pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="b6f1c-105">Kad tiek veidots pakalpojuma pasūtījums, adresāta informācija tiek pārsūtīta no projekta, kuram šis pakalpojuma pasūtījums ir piesaistīts.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="b6f1c-106">Taču jūs varat atlasīt citu atrašanās vietu, izvēloties kādu no adresēm, kas jau ir ievadītas programmā Microsoft Dynamics AX debitoriem, kreditoriem, vietām, noliktavām, pakalpojumu pasūtījumiem un projektiem.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="b6f1c-107">Varat arī izveidot jaunu adresi.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-107">You can also create a new address.</span></span> <span data-ttu-id="b6f1c-108">Pēc noklusējuma jaunā adrese tiek pārsūtīta uz projektu.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="b6f1c-109">Tomēr var norādīt, ka jaunā adrese ir derīga tikai šai pakalpojuma instancei.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="b6f1c-110">Šajā gadījumā jaunā adrese netiek pārsūtīta uz projektu.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="b6f1c-111">Debitora adreses izveidošana pakalpojuma pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="b6f1c-111">Create a customer address for a service order</span></span>

<span data-ttu-id="b6f1c-112">Lai pievienotu adresi pakalpojuma pasūtījumam, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="b6f1c-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="b6f1c-113">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b6f1c-114">Atveriet pakalpojuma pasūtījumu, kuram vēlaties izveidot adresi.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="b6f1c-115">**Darbību rūtī** noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Virsraksta skatījums**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="b6f1c-116">Kopsavilkuma cilnē **Adrese** noklikšķiniet uz **Pievienot adresi**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="b6f1c-117">Veidlapā **Jauna adrese** ievadiet unikālu adreses nosaukumu un aizpildiet atlikušos laukus.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="b6f1c-118">Ja ievadāt tādu pašu nosaukumu kā esošai adresei, atlikušajos laukos ievadītā informācija pārrakstīs esošās adreses informāciju.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="b6f1c-119">Noklikšķiniet uz **Labi**, lai kopētu jaunu adresi uz pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="b6f1c-120">Alternatīvās adreses noteikšana pakalpojuma pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="b6f1c-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="b6f1c-121">Lai pievienotu alternatīvu adresi pakalpojuma pasūtījumam, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="b6f1c-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="b6f1c-122">Klikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b6f1c-123">Atveriet pakalpojuma pasūtījumu, kuram vēlaties ievadīt alternatīvo adresi.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="b6f1c-124">**Darbību rūtī** noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Virsraksta skatījums**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="b6f1c-125">Kopsavilkuma cilnē **Adrese** noklikšķiniet uz **Cita adrese**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="b6f1c-126">Veidlapā **Adreses atlase** laukā **Ieraksta tips** atlasiet **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="b6f1c-127">Atlasiet adresi un pēc tam noklikšķiniet uz **Labi**, lai to kopētu uz pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


