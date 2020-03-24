---
title: Manuāli izveidot pārraudzītus ieteikumus
description: Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču sarakstus Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b39ef61e7dabdd8a53d5666926a95cb7b9e6b9a5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127725"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="8e85d-103">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="8e85d-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e85d-104">Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču ieteikumu sarakstus Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="8e85d-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="8e85d-105">Pārraudzīti saraksti ir atsevišķa satura kolekcijas, ko veido un pārrauga cilvēki.</span><span class="sxs-lookup"><span data-stu-id="8e85d-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="8e85d-106">Jauna saraksta izveide</span><span class="sxs-lookup"><span data-stu-id="8e85d-106">Create a new list</span></span>

<span data-ttu-id="8e85d-107">Lai izveidotu pārvaldītu preču rekomendāciju sarakstu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8e85d-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="8e85d-108">Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="8e85d-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-109">Select **New**.</span></span>
1. <span data-ttu-id="8e85d-110">Ievadiet vērtību laukā **Saraksta ID**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="8e85d-111">Ievadiet vērtību laukā **Saraksta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="8e85d-112">**Saraksta nosaukums** ir tā saraksta nosaukums, kas parādīsies moduļa **Preču kolekcijas** pārraudzītu sarakstu sadaļā.</span><span class="sxs-lookup"><span data-stu-id="8e85d-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="8e85d-113">Lai pievienotu preces sarakstam , atlasiet **Pievienot preces**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="8e85d-114">Lai sarakstā mainītu preču secību, ievadiet vērtību kolonnā **Rādīšanas secība**.</span><span class="sxs-lookup"><span data-stu-id="8e85d-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="8e85d-115">Ja divām precēm ir tāda pati rādīšanas secības vērtība, tad šo divu rezultātu gala secība var atšķirties no tās, kas ir operāciju uzskaites daļā.</span><span class="sxs-lookup"><span data-stu-id="8e85d-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="8e85d-116">Atlasiet **Saglabāt**, lai saglabātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8e85d-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="8e85d-117">Saraksta piemērs</span><span class="sxs-lookup"><span data-stu-id="8e85d-117">Example List</span></span>

![Pārraudzīta saraksta piemērs operāciju uzskaites daļā](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="8e85d-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8e85d-119">Additional resources</span></span>

[<span data-ttu-id="8e85d-120">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="8e85d-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8e85d-121">ADLS iespējošana Dynamics 365 Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="8e85d-121">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8e85d-122">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="8e85d-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8e85d-123">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="8e85d-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8e85d-124">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="8e85d-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8e85d-125">Preču ieteikumu sarakstu pievienošana e-komercijas vietnei</span><span class="sxs-lookup"><span data-stu-id="8e85d-125">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="8e85d-126">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="8e85d-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8e85d-127">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="8e85d-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8e85d-128">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="8e85d-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8e85d-129">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="8e85d-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8e85d-130">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="8e85d-130">Product recommendations FAQ</span></span>](faq-recommendations.md)
